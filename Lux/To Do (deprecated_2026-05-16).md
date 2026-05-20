- Inbox
- Smarter Contact Into This
- Direct Mail

Jon
- ~~Twilio stuff~~
- ~~Maps coloration still bad in oterh views~~
- ~~How can I get imessages to download?~~ 

- Add an AI parser quick add feature where I can just dump info into an area and spit out either adding a property owner, multiple buyers, etc. -- have this in buyers, buy boxes, properties start there
- Add an ARV redfin/zillow builder finder agent - Like put in a point on the map, a radius, and look at descriptions and parse them and find buyers companies in masse for all builds in that area
- Update email sending order and style looks shitty - make it separate each message, the thread type view is very messy
- Add property inserts into emails and texts (almost like merge field but full property info) - could be its own separate full property blurb field -- almost like mail merge feature but for entire property- easiest way to do this is probabaly simply make migration file and push a new column to properties called "marketing_description" and we can pull this in for each property in our list
- Add docuemnt attachments into SMS, emails and store and see them in here - to proeprties etc. In generl we need to create a documents DB, where we can upload documents and the should have relationship with buyers, properties etc - Like for each we can just uploaed dcs that are relevant - pictures of the propety, site sutveyrs etc so add a descitption dfield that we can name teh doc keep it simple to start
- Add cotact "title" fields- make it a input and basiucally htis is like the person position at teh compaby
- What happened to conversations for that particular contact? We should also maybe add this for buyer level too where we can select the contact to send to withn that company- basically this is a way to look at teh conversation email/SMS for that contact and text or email teh mindividually. SHould be jsut as good as converstions tab i nterms on cleanliness minimlaist and featreset
- Pipeline flow viewer for all pipeline charts -SANKEY diagram for the dashbaord as well as what we currentl;y have. Also move the pipeline that we have there to the properties tab - so we have pipeline ofproperties and each property has its own pipeline
- add more stages liek responded etc  to the property pipeline should be able to scroll and more simply move to other stages - I noticed that the column headers are not always visible when they should be and I should be able to drag and drop and move stufff visibily easily
- Make calls through my system and record them- we bascially need to add the basics of a telephony systemi nto this.so add a teltphone top right where we can dial and call. But also some clock to dial feature beside phone numbers in contacts and buyers in the UI. The telpny system should again reor the calls, time, store teh recording, log it, allow dialing etc -= start there
- Add in making calls in this/tracking activirty in logs like calls etc
- Start using AI in terms of reading transtipons of recods calls, transalting that to thngs it shuld do, and using AI to translate into buyboxes, to do items etc
- Front end form for scott and mae to enter property into when they get one
- Also, lets get the bones ready fro a front end link to and estiamte tool that (homeonwer or perpoty) owners can go to and check their peropetries value (this will be accesed outside the app) just get teh bones raeady 


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
- 
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
