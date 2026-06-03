- Inbox
- Smarter Contact Into This
- Direct Mail

Jon

- Autosave
- AI messaging (simple chatbot)
- 



- Document upload error
- Phone
	- We aren't receiving inbound SMS
	- Connect Twilio for call forwarding?
- Affiliates section and payouts
- SMS messages in convo arent good

Estimator
- Im starting to noticed that, reference addresses can serve 2 data points. Same with ARV's. - If we know what the owner bought a lot for and sold it at, we have 2 data points for same property comp in these scenarios right? Like redfin or zillow usually shows the alst purchase price and date. So when adding a refernce to a buyer we need to basically pull out the bought for comp and the ARV value - same with the ARV (in teh ARV table) and even same with properties table adding comps
- Save Pricing reference estimator to the property itself (if we keep the record) - Like when we go through the explore tab and step 1-3, and then go back to left sidebar, when we click add, it maybe we should add fields into our DB to save the price calcualtor info?


- Im noticing that we still have loading issue thorugh out the app.. Very slow to tab through. I thought we did a massive update on this in which we load all data i nteh app into caceh on login and then jsut access it all when tabbing and difernt pages? Should never need to load rarely yet we still do allllll over the app. Still has loading issue within sub tabs form some reason everythng should alreayd be loaded.
- Find buyer dropdown to add to property needs a even more detailed search or filter mechanism
- When adding buyers we need to make sure that its required we add a city and state (also make these dropdowns from active markets so that its easy to select and more uniform in DB)
- Merge contacts - im noticing duplicate contacts in teh Db - make a simple system to merge 2 contacts or buyers or properties - ask the user which one to preserve and maybe always merge or fold that merged ones data (all of it - note setc) into a new note on the newst one as an option to retain the data


- Also Ai button template to automatically make marketing description from template or AI to make it for a property
- Make the pricing estiamte tool more liek a clacualtor with a few adjustments
- Reference addresses can serve 2 data points - If we know what the owner bought a lot for and sold it at, we have 2 data points for same property comp
- We could probably store more redfin fields in properties for more accuracy - build sqft, year built etc
- Setup Mac Shortcuts app
- inbound call forwarding to my cdll phone
- Follow ups - n8n

- Testing
	- When adding contact automatically have them selected. Then when we select contacts to blast, we can just pick and choose there from ones selected. Default is yes
- make a realt iem dev mode tagging system for isseus that are synced with github or obsidian or both etc- the point being that i can have superset conenct right into my local githib and take orders from the logs and just debug autoamticlly fro mtehre

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

-
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



