- UI
	- Show on the quote range, buyboxes from buyers so that teh salesperson sees where they cluster
	- User Clicks "Get Quote" Button
		- First thing it does, is take screenshots of multipel angles and use AI to evlauate?
	- (Optional) Manually Enter Teardown Comps
		- Redfin

## Data Sources

```
buy_boxes      → territory + starting price range + gradient
buyer_quotes   → real offers, baked into gradient
properties     → location point + lot size
comps          → real sold lots, reference only
```

---

## Buy Box Types

```
Buyer given    → range never changes, gradient builds on top from quotes
System created → range adapts over time from quotes + comps
```

---

## Initializing a Buy Box

**Buyer given** → Use exactly what they said. Never changes.

**System created** → Query nearby comps, use avg sold $/sqft as starting midpoint → No comps? Use manual estimate → Range width is set manually (e.g. $20 spread around midpoint)

---

## When a Quote Comes In

```
1. Append to price_gradient on matching buy_boxes (ST_Contains check)
2. If system generated → check if range needs to drift toward quote reality
```

**Adaptation rules:**

- Per buyer → quotes drift their own buy box range slowly over time
- Per market → if ALL buyers in an area are consistently quoting way off the starting range → correct starting range for all system generated boxes in that area
- Buyer given → never adapts, gradient builds on top only
- Minimum 3 quotes before any adaptation kicks in

---

## Buy Box Gradient

Each buy box stores a `price_gradient` array on the `buy_boxes` row:

```json
[
  { "quote_id": "abc", "lat": 29.751, "lng": -95.367, "price_per_sqft": 65, "created_at": "..." },
  { "quote_id": "def", "lat": 29.743, "lng": -95.371, "price_per_sqft": 72, "created_at": "..." }
]
```

- Polygon shape never changes
- Price range on the polygon drifts over time (system generated only)
- Gradient is always calculated real time at read time
- Frontend renders gradient as a heat map layer over the polygon using Turf.js

---

## When Get Estimate Is Clicked

**Step 0 — Property data** Pull from `properties`:

```
properties.pin_geom      → location point
properties.lot_size_sqft → for multiplier calculation
```

**Step 1 — Find all matching buy boxes** Spatial query against `buy_boxes` using `properties.pin_geom`:

```
ST_Contains(buy_boxes.geom, properties.pin_geom)
WHERE is_active = true
```

**Step 2 — Sample gradient on each buy box** For each matching buy box, load `price_gradient` from `buy_boxes` and run gaussian decay:

```
weight = exp(-0.5 × (distanceMeters / 800)²)

close quotes  → pull hard toward what they paid
far quotes    → barely matter
no quotes     → fall back to (min_price_per_lot_sqft + max_price_per_lot_sqft) / 2
```

Blend formula:

```
effective $/sqft = (gradient price × confidence) + (midpoint × (1 - confidence))
```

**Step 3 — Apply lot size multiplier** Pull `lot_size_sqft` from `properties`:

```
< 5k sqft    → × 0.90
5k - 10k     → × 1.00  (baseline)
10k - 20k    → × 1.10
20k+         → × 1.20
```

**Step 4 — Collect all buyer prices** One effective $/sqft per buyer after multiplier applied:

```
Buyer A → $77/sqft
Buyer B → $89/sqft
Buyer C → $71/sqft
```

**Step 5 — Build the offer**

```
Floor       → lowest buyer $/sqft × lot_size_sqft
Ceiling     → highest buyer $/sqft × lot_size_sqft
Sweet spot  → weighted avg $/sqft × lot_size_sqft

Offer low   → sweet spot × 0.80
Offer high  → sweet spot × 0.90
```

**Step 6 — Triangulate with attached comps (if any)** If comps are manually attached to this property via `parcel_comp`:

```
Buyer quotes  → weighted 70%
Attached comps → weighted 30%
→ adjusted sweet spot
```

---

## Confidence

```
3+ nearby quotes  → high   (quotes are truth)
1-2 nearby quotes → medium (slight pull)
0 nearby quotes   → low    (stated range only)
```

---

## Distance Math

```
Backend only  → haversine, no library needed
Frontend grid → Turf.js
```

---

## What Shows On Screen

```
Offer low     → sweet spot × lot sqft × 0.80
Offer high    → sweet spot × lot sqft × 0.90
Sweet spot    → single best number
Confidence    → high / medium / low
Active buyers → buy box clusters shown on map
Comps         → nearby sold lots shown as reference only
```

---

---

# Comps System (Separate from Buyers)

---

## What They Are

Real sold listings — teardown lots and vacant land only. Not attached to any buyer. Org-scoped, reusable across properties.

## Where They Come From

- Manually uploaded from Zillow, Redfin, or MLS
- Imported via listing URL
- Teardown lots / built before 1975 preferred
- Sold within last 6-12 months
- Internal observations — our own knowledge of what areas trade at
- User can add a new comp on the fly from the Get Estimate screen

## Storage

```
comps table    → single source of truth for all comps (global/org-scoped)
parcel_comp    → join table linking comps to a specific property quote
  property_id
  comp_id
  attached_by
  created_at
```

## How They Are Used

**1. Seed system generated buy boxes** When a system generated buy box is created with no quotes yet: → Query `comps` table for nearby sold lots → Use avg sold $/sqft as starting midpoint → Range width set manually around that midpoint

**2. Get Estimate screen** User picks 2-3 nearby comps from existing `comps` table OR adds a new one on the spot:

- New comps save to `comps` table first (reusable going forward)
- Then link to property via `parcel_comp`
- Shown on screen as reference next to the offer

**3. Triangulation** When comps are attached to a property they influence the sweet spot:

```
Buyer quotes   → weighted 70%
Attached comps → weighted 30%
```

Note: Actual implementation uses track 1 (teardown comps), track 2 (new construction comps), and quotes as separate inputs in the pricing engine. The 70/30 is a simplified representation.

## When Comps Are NOT Used

- Buyer given buy boxes — these never change
- Automatic gradient updates — comps don't punch into the gradient like quotes do
- Any math unless manually attached to a property OR seeding a system generated buy box

---

## Implementation Status

```
Done:
  → Shared comp storage (comps table)
  → Per-property linking (parcel_comp)
  → Add comp on the fly (manual + listing URL import)
  → Attached comp influence on estimate
  → Comps not tied to any buyer

Not done:
  → Seeding system generated buy boxes from nearby comps at creation time

Not matching spec:
  → Weighting model is more complex than 70/30
    (track 1 teardown / track 2 new construction / quotes as separate inputs)
  → Intake rules not fully enforced
    (built before 1975, sold only, 6-12 months)
```