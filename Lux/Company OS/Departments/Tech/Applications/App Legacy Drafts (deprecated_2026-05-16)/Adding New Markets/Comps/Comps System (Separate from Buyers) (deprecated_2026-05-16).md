What they are

Real sold listings — teardown lots and vacant land only. Not attached to any buyer.

## Where they come from

- Manually uploaded from Zillow, Redfin, or MLS
- Built before 1975, sold within last 6-12 months
- Internal observations — our own knowledge of what areas trade at
- User can add a new comp on the fly from the Get Estimate screen

## Storage

```
comps table          → single source of truth for all comps
property_comps table → links comps to a specific property quote
  property_id
  comp_id
  attached_by
  created_at
```

## How they're used

**1. Seed system generated buy boxes** When a system generated buy box is created with no quotes yet — query nearby comps, use avg sold $/sqft as the starting midpoint.

**2. Get Estimate screen** User picks 2-3 nearby comps from existing `comps` table OR adds a new one on the spot. New comps save to `comps` table first for future reuse, then link via `property_comps`. Shown on screen as reference next to the offer.

**3. Triangulation (optional)** If comps are attached to a property quote, they can influence the sweet spot:

```
Buyer quotes  → weighted 70%
Attached comps → weighted 30%
```

## When comps are used

- Seeding system generated buy boxes at creation
- Manually attached to a property on Get Estimate screen → influences triangulation
- Reference on screen next to the offer

## When comps are NOT used

- Buyer given buy boxes — these never change
- Automatic gradient updates — comps don't punch into the gradient like quotes do