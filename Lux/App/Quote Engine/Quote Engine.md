- User Type in address
	- Zoom in
- User Clicks "Get Quote" Button
	- First thing it does, is take screenshots of multipel angles

- Comps
	- Parcel score directly tied to the property weight and quote
	- Quotes
		- Specific quotes they have given for certain properties
	- Comps (Scrape Zillow, MLS, or Redfin)
		- Recently (up to 1 year) sold likely teardown lots (or vacant land) built before 1975
			- What likely dirt has gone for recently






Main things I did:

- Pulled the shared zoning source note up to the category level instead of repeating it 3x
- Removed the redundant "is there a way to find this" notes (can live elsewhere)
- Tightened the wording on a few items

Want to add a **data source** column to any of these, or keep it notes-only for now?


		- Can be added in later
		



Build Plan
- Adding quotes is already simple
- Admin flag
	- Scrape redfin in the area for teardown comps and. visually select yes. or no to add to the DB
	- I can also manually add some if missed by scraper 1 by 1
	








		- Recently sold (up to 1 year ) new constructions selling for $2mm+
			- What are possible ARV's in the area
			- How many high value newly built homes are in the area (hot spot)
			- How long did they sit on the market


- Internal Observations
		- Like we have gathered enough information about a certain area to know that X area properties go around $Y whereas the other half of the neighborhood goes for $Z
	- Zillow/ Redfin Comps
			- Sold within the last year at high end ARVs (for recent teardown lots)