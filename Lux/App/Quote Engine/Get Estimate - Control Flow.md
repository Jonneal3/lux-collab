- UI
	- Show on the quote range, buyboxes from buyers so that teh salesperson sees where they cluster

- (Optional) Manually Enter Teardown Comps
	- Redfin

### Step 1 — Bake quotes into the buy box
- Every time a buyer quotes a property, that quote gets added to the buy box it falls inside. The buy box now "remembers" what was paid where.

### Step 2 — Drop the property onto the buy box
- When we need a price, we drop the property's point onto the buy box and ask: _"What did nearby quotes pay?"_ Close quotes pull hard. Far quotes barely matter.

### Step 3 — Return a price
- If quotes are nearby → price comes from them
- If no quotes nearby → falls back to the buy box stated price
- Multiply by lot sqft → offer range



- Select a few
	- Buybox
		- Area Averages
		- ARV Averages



Formula
- Determine a price per sqft range



- Busy Road:
		- Convert each adjacent road’s OSM `highway` type into a traffic score  
		- Take the **highest (worst) score** if multiple roads are present  
		- If that score is **7 or higher** (primary or larger), mark:  
			- `busy_road = true`  
		- Otherwise:  
			- `busy_road = false`



Front End


We choose comps on front end:
- pick 2 or 3
- Comp
	- All Buyer Related
		- Buy box
			- $/sqft
	- Only Exact Nearby Comps in Refin Manually Uploaded
		- Sold Last 3-6 Months



Real Time Formula