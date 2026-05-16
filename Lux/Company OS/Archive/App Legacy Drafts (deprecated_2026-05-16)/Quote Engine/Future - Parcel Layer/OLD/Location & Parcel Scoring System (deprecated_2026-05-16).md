Location Score JSON
- Binary - For now, se these to no quote, BUT, then affix a discount % on each based on the market
	- Historic District _(NPS ArcGIS — not needed on map)_
	- Flood Zone _(FEMA — not needed on map)_
	- Busy Road:
		- Convert each adjacent road’s OSM `highway` type into a traffic score  
		- Take the **highest (worst) score** if multiple roads are present  
		- If that score is **7 or higher** (primary or larger), mark:  
			- `busy_road = true`  
		- Otherwise:  
			- `busy_road = false`


- Parcel Score
	- Lot size: Cost Per Sqft.
		- This is baked right into the parcel
		- The bigg


	- ==Lot Dimensions:==
	- ==Lot Shape:==
	- ==Slope:== 

- Directionality from comps
	- Distance from comps
