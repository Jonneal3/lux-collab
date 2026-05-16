**Parcel Layer — Data Sources & Scorability**

| Factor                    | Data Source                                         | Scorable?                             |
| ------------------------- | --------------------------------------------------- | ------------------------------------- |
| **Fundamentals**          |                                                     |                                       |
| **==Historic District==** | **==NPS ArcGIS==**                                  | **==✅ Binary yes/no==**               |
| **==Busy / Main Roads==** | **==Google Traffic / TomTom API==**                 | **==✅ Traffic volume score==**        |
| **==Flood Zone==**        | **==FEMA API==**                                    | **==✅ Binary or zone rating==**       |
| **==Lot Size==**          | **==Parcel API (Regrid/ATTOM)==**                   | **==✅ Direct — ties to sqft comps==** |
| **==Lot Dimensions==**    | **==Parcel API==**                                  | **==✅ Width esp. matters==**          |
| **==Lot Shape==**         | **==AI inference from parcel geometry==**           | **==⚠️ Harder, proxy only==**         |
| **==Slope==**             | **==Google Elevation API / USGS==**                 | **==✅ Grade % is quantifiable==**     |
| **Location Score**        | **Near beach, views, good vs bad areas Buy boxes)** | **✅ Simple radius**                   |
| Trees                     | Google Maps / county GIS                            | ⚠️ Hard to automate                   |
| Height Restrictions       | City Zoning API / scrape                            | ✅ Max stories/ft                      |
| Lot Coverage              | City Zoning API / scrape                            | ✅ % is direct                         |
| Frontage / Setbacks       | City Zoning API / scrape                            | ✅ Buildable area calc                 |
| Pool Markets              | Climate data + local comp analysis                  | ⚠️ Market-level not parcel            |
| Surrounding Uses          | Google Places API                                   | ✅ POI density/type                    |
- Parcel Layer: This layer basically gives us feedback on specific parcels we come across
	- Land Value Factors
		- Slope
		- ==Zoning:== 
			- ==Historic Districts:== 
				- ==NPS Arc Gis==
				- ==Is there a way to find this in the parcel info itself?==
				- ==Not needed on map==
			- ==Flood Zone:== 
				- ==FEMA==
				- ==Is there a way to find this in the parcel info itself?==
				- ==Not Needed on Map==

		- Can be added in later
			- ==Height restrictions:== 
				- ==City Zoning Map==
				- ==Maybe we can triangulate with the zoning bylaws, the actual zone info and a screenshot of the zoning map too==
			- ==Buildable Sqft==
				- ==City Zoning Map==
				- ==Maybe we can triangulate with the zoning bylaws, the actual zone info and a screenshot of the zoning map too==
			- ==Frontage==
				- ==City Zoning Map==
				- ==Maybe we can triangulate with the zoning bylaws, the actual zone info and a screenshot of the zoning map too==
		- End Buyer Preferences
			- Views etc.
			- Busy Streets
			- Some places "need" pools
			- Whats around it
			- Corner vs. Interior lots
		- Proximity (Area/Neighborhood)
			- Bad/ Good parts
			- Near beaches
			- Near Schools