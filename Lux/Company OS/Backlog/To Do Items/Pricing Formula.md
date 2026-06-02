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


Estimator
- Im starting to noticed that, reference addresses can serve 2 data points. Same with ARV's. - If we know what the owner bought a lot for and sold it at, we have 2 data points for same property comp in these scenarios right? Like redfin or zillow usually shows the alst purchase price and date. So when adding a refernce to a buyer we need to basically pull out the bought for comp and the ARV value - same with the ARV (in teh ARV table) and even same with properties table adding comps
- Save Pricing reference estimator to the property itself (if we keep the record) - Like when we go through the explore tab and step 1-3, and then go back to left sidebar, when we click add, it maybe we should add fields into our DB to save the price calcualtor info?

- Estimator
	- ARV shouldnt be a solid numberit is also a range - we should have a slider for this
	- Build sqft
	- Buld SQFt os baesd on builder and also ARVS
	- How much should "get pricing" estimator use FOR SALE right now data?
	- Add in to build estiamtor the ARV # after build etc

- Is there a way of calcuating land value / sqft better - form a more builder perspective - ARV / sqft

What about a scatterplot of quotes i nwhich we come up with the correct data to leave out? Like a rgression model taht finds likely outliers for price/sqft and leaves them removed if there s a lot of comps in an area


- Make the pricing estiamte tool more liek a clacualtor with a few adjustments

 - Fix math equation from comps to ARV
	 - Price/sqft / per sqft (to account for lot size as well like bigger lots are more valuable)

