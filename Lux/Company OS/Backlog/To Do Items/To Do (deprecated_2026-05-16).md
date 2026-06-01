- Inbox
- Smarter Contact Into This
- Direct Mail

Jon

- ~~When adding a new property - Enrich from redfin autoamtically and show siggestions in the fields
- Phone
	- We arent receiving inbound SMS
	- Connect Twilio for call forwarding?
- Affiliates section and payouts



- Add social post template dropdown in that area of the UI too to simply just add teh social post template into that area easily
- Im starting to noticed that, reference addresses can serve 2 data points. Same with ARV's. - If we know what the owner bought a lot for and sold it at, we have 2 data points for same property comp in these scenarios right? Like redfin or zillow usually shows the alst purchase price and date. So when adding a refernce to a buyer we need to basically pull out the bought for comp and the ARV value - same with the ARV (in teh ARV table) and even same with properties table adding comps
- New emails in buyer and contact view - Firstly, we should be able to choose a contact within the buyer conversations tab, within that company to email. Any ANY time, we should be able to start a new conversation with any contact. Right now, if we change contact info for a contact, it wont create a new conversation (jsut says, continuing thread) or something.
- Save Pricing reference estimator to the property itself (if we keep the record) - Like when we go through the explore tab and step 1-3, and then go back to left sidebar, when we click add, it maybe we should add fields into our DB to save the price calcualtor info?
- Cants edit notes all cross the board - allow this
- What happened to teh toggle of notify buyers or whatnot? Like how do we denote notifying buyer contacts vs the business info email?
- ~~Gmail setup error - I just added my emai lthrough nango which is good but it says SMAIL INBOX ERROR and i cant send email thogh i dont know why - its not pulling in from my nango app list~~
- Still have the weird double scroll going on on buyers pages lke we can scroll main page and the dropdown section which is weird - i suspect this is happening on lots of those pages too like contacts etc.
- Im noticing that we still have loading issue thorugh out the app.. Very slow to tab through. I thought we did a massive update on this in which we load all data i nteh app into caceh on login and then jsut access it all when tabbing and difernt pages? Should never need to load rarely yet we still do allllll over the app. Still has loading issue within sub tabs form some reason everythng should alreayd be loaded.
- Find buyer dropdown to add to property needs a search or filter mechanism
- When adding buyers we need to make sure that its required we add a city and state (also make these dropdowns from active markets so that its easy to select and more uniform in DB)
- Merge contacts - im noticing duplicate contacts in teh Db - make a simple system to merge 2 contacts or buyers or properties - ask the user which one to preserve and maybe always merge or fold that merged ones data (all of it - note setc) into a new note on the newst one as an option to retain the data


- Also Ai button template to automatically make marketing description from template or AI to make it for a property
- Make the pricing estiamte tool more liek a clacualtor with a few adjustments
- Reference addresses can serve 2 data points - If we know what the owner bought a lot for and sold it at, we have 2 data points for same property comp
- We could probably store more redfin fields in properties for more accuracy - build sqft, year built etc
- Setup Mac Shortcuts app
- inbound call forwarding to my cdll phone
- Follow ups - n8n

- make a realt iem dev mode tagging system for isseus that are synced with github or obsidian or both etc- the point being that i can have superset conenct right into my local githib and take orders from the logs and just debug autoamticlly fro mtehre

- Something in the app is eating up my supabase data egress
	- 
- Make active markets in settings setting pulls in and imports zip codes etc - simply see on a map where we are active for business - we already have the data in our DB
	- Then we can connect into a buyer search type agent (in tha AI section) etc athat will then go ahead and start to pull in buyers (with various reserach methods we will continue to add, with LEGA scrapers etc) and we can pull in companies etc. Let =s get most of the bones here setup to do that. We are making a DSPy ai direcotry in another chat right now


- Gotta go through and still figure out how to notify the builders vs contacts and tons of builders have some weird dummy contact added to them
- Estimator
	- ARV shouldnt be a solid numberit is also a range - we should have a slider for this
	- Build sqft
	- Buld SQFt os baesd on builder and also ARVS
	- How much should "get pricing" estimator use FOR SALE right now data?
	- Add in to build estiamtor the ARV # after build etc

- Gettign erros when uploading documents


 - Fix math equation from comps to ARV
	 - Price/sqft / per sqft (to account for lot size as well like bigger lots are more valuable)

- AI Modules
	- First, start by implementing DSPy into its own separate proejct module in buyer and or seller - Is pythn so you haev to find the simplest easier way of impel,ementing into anext proejct. Then, we wanttoadd separrte directroy, moduesl and signaltures for all AI "aprts" of this app. Then add examples. Lets start wit hteh parts and fucntions below
	- Add an AI parser quick add features for adding properties, buyers etc where I can just dump info into an area and spit out suggestions to add either adding a property owner, multiple buyers etc. -- have this in buyers,  contacts, buy boxes, properties start there
	- Start using AI in terms of reading transtipons of recods calls, transalting that to thngs it shuld do, and using AI to translate into buyboxes, to do items etc > I dont see any of this but lets wait on that anwyay make it capale from call transcripts and recordings etc 
	- Ise a simple model with GROQ, OpenAi or replicaet make it so. i can add those api keys and easily switch models. 

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
