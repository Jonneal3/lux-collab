- Inbox
- Smarter Contact Into This
- Direct Mail

Jon
- Make active markets in settings setting pulls in and imports zip codes etc - simply see on a map where we are active for business - we already have the data in our DB
	- Then we can connect into a buyer search type agent (in tha AI section) etc athat will then go ahead and start to pull in buyers (with various reserach methods we will continue to add, with LEGA scrapers etc) and we can pull in companies etc. Let =s get most of the bones here setup to do that. We are making a DSPy ai direcotry in another chat right now


- Gotta go through and still figure out how to notify the builders vs contacts and tons of builders have some weird dummy contact added to them
- Estimator
	- ARV shouldnt be a solid numberit is also a range - we should have a slider for this
	- Build sqft
	- Buld SQFt os baesd on builder and also ARVS
	- How much should "get pricing" estimator use FOR SALE right now data?
	- Add in to build estiamtor the ARV # after build etc


- External Estiamtor
	- Front end form for scott and mae to enter property into when they get one < I dont see this where is it? You should have it maybe as a dropdown form from property menu of like property form link clikc to open<<< SO i want 2 things.. one of them is an intake form of a property from an outsider that can go into my system. The other is basically the explore tab that is externallly used. Liek a person can enter their property and find their propery value estiamteion, meant for like a particualr person who wants to know the value of 1 property/front end link to and estiamte tool that (homeonwer or perpoty) owners can go to and check their peropetries value (this will be accesed outside the app) just get teh bones raeady < Where di you put this?

Buyer Finding/Enrichment
- Add an ARV redfin/zillow builder finder agent - Like put in a point on the map, a radius, and look at descriptions and parse them and find buyers companies in masse for all builds in that area

Market Finders
- Find hot pockets in the US where deals are clustering for new builds recently sold for high values

Oh- Know who has or hasnt actually been blasted a particualr property in the notify pipeline and what went through or didnt
- For all pipelines, we should have certain things be added when moving to that stage that we need - so like for moving a step, certain things ha
- Start data enrichment for agents/ builders etc.
- SMS push mclean

- Gather FTL properties and push
- Have enrichment right in the CRM system and builder finders scraper etc
- Push to FB
- How could i basically use imessages in my conversation dash too? Still using my iphone right now - people use my cell
- Convert using gmail or email to SMTP etc 
- Where do i begin on scheduled sends and followups for emiasl etc. 



- Sweep up and re push other old ones
- How do gmail API's / IMAP work?
- How to do followups in this ?
 - Did we:
	 - Pull in phone calls?
	 - We need to:
		 - Merge some buyers
		 - Rename Contacts better
		 - Connect contacts to buyers/ create new buyers if not exist
		 - Start annotating buyers
		 - Go through existing converations with buyers and pull in:
			 - Buy boxes
			 - Quotes
			 - Start Having AI score them for like "stringy-ness" or something
		- Start warming an email for notificaitions




- Fix the pricing formula
	- The formula:
		- Break everything down into a grid based on this
			- Data points weighted on:
				- Type
					- Select or manually add more comps
						- Need to be more accurate - 	- Comps are not all accurately tear downs - Some are reno's etc
							- **Listing description keywords** — Redfin usually includes the listing description in scraped data. Words like "renovated", "updated kitchen", "new roof", "remodeled", "hardwood floors refinished" are strong signals. This is easy to run with a keyword scan.
								- Solution: 
									- Have an AI image gen model look at the pictures
									- Have a keyword match/AI scoring mechanism
							- **Assessed value jumps** — if you can cross-reference county assessor data, a big assessed value increase mid-ownership usually follows a permit/reno
								- Solution: This isnt always reported thought right?
					- Quotes pull in on a gradient automatically
					- Hearsay projects
				- Proximity (distance)
				- Time (when)


- What about a scatterplot of quotes i nwhich we come up with the correct data to leave out? Like a rgression model taht finds likely outliers for price/sqft and leaves them removed if there s a lot of comps in an area
- Hover over the pin or comp and it highlights vce versa 
- Comp card not displaying the right stuff on teh right
- The checkmark pboxes should be above comp section
- Is not pulling in all comps when chanign rdius size or on open seems to show differnt comps every time
- Im not seeing a manually add a comp button




	- No finding parcel size from the parcel data so its thrwing of fteh math

	- Is there a way of calcuating land value / sqft better - form a more builder perspective - ARV / sqft


- Past projects
	- Add a "hearsay" version - Guys will say "i bought an $x lot down teh street on elm that was .4 acre"
- The go through my sticky note and :
	- Add an adjust buy boxes/ quotes and other info
	- We need to add lot size into buy boxes of what they want
		- Scott sent me nicks buy box criteria
	- Go through texts and connect buyers, quotes and outcomes into already existing properties
- Admin mode grid view






- Add a system suggested buybox fill in feature
	- it will basically use teardown comps in any given buybox for a new buyer to basically set a starting price floor area



Done
- ~~Contacts Need Addresses too etc.~~
	- ~~For lone buyers~~
- ~~Easily email properties to buyers who are intersted in real time - select the properties to attach~~
- ~~Finish zip code update (atlanta, WPB)~~
- ~~Re-compile comps for all zips~~
- ~~Add Teardown Comps into active areas
- ~~Active markets~~
 - ~~Create a script to merge and de-duplicate buyers and contacts~~
- ~~Buyers~~
	- ~~Add more stuff like selecting spec or custom etc.~~
	- ~~Add in "previous builds" and or "current builds"~~
		- ~~The same comp selector and or adding in or connecting previous builds directly to a buyer~~
		- ~~Website URL, redfin or zillow~~
- ~~Properties~~
	- ~~What happened to comps connected to property?~~
- ~~Add Starting buybox templates for each active market~~
- ~~Add starting buy boxes in bulk~~ 
	- ~~Then go back and adjust the ones that were custom~~ 
