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
