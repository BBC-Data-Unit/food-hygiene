# Delays in food hygiene inspections a 'serious public health issue' 

![](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/data/Delays%20in%20food%20hygiene%20inspections%20a%20serious%20public%20health%20issue.png)

In July 2024 we [revealed](https://www.bbc.co.uk/news/articles/c1rr1qqqny0o) that one in five restaurants and takeaways had not been seen by food inspectors for more than two years.

## Methodology

We used Food Standards Agency (FSA) open data on the food hygiene ratings and status of every establishment in England, Wales, Northern Ireland and Scotland at https://ratings.food.gov.uk/open-data.

We downloaded data from every local authority as of April 10 2024. This was filtered to establishments in four categories: Restaurant/Cafe/Canteen; Pub/bar/nightclub; Takeaway/sandwich shop; and Mobile caterer (see notebooks below). 

The data was cleaned to remove a small percentage (<1%) of duplicate entries: where an establishment with the same name and latitude, or the same name and postcode, appeared more than once in the same authority’s data, the row with the most recent inspection date was retained and the other removed. 

Each establishment was classified to determine whether it had been inspected since January 1 2022 (i.e. within the last two years and three months) or not, or whether it was still awaiting inspection. 

A second set of data was downloaded on April 25 focusing on wholesale outlets. This was filtered to establishments in three categories: Manufacturers/packers; Importers/Exporters; and Distributors/Transporters. 

*Note: some establishments will have since been inspected, added, or removed since the data was compiled.*


## Get the data

* [FSA data API](https://ratings.food.gov.uk/open-data)
* [URLs of data files](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/data/foodHygieneURLs.xlsx) (generated from IDs)
* [Ratings for wholesalers since 2022 with analysis](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/data/FSAwholesalers_dedupedAPR25_ANALYSIS.xlsx)

*The ratings data for other establishments is too big to host on GitHub*.

## Code

Scripts were written in Python to loop through and download the data files for each local authority, filter and analyse. OpenRefine was also used to identify potential duplication in the FSA dataset - the steps have been exported as a JSON file.

* Python notebook: [Analysing food hygiene data](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/code/FoodHygieneProject.ipynb)
* Python notebook: [Analysing food hygiene data: wholesalers](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/code/FoodHygieneProject_wholesalers.ipynb)
* JSON: [Checking for duplicates in OpenRefine](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/code/food%20safety%20-%20OpenRefine%20checks.json) - an [explanation is in the Readme](https://github.com/BBC-Data-Unit/food-hygiene/blob/main/code/readme.md)

## Partner usage

* Andover Advertiser: [Data shows backlog of Test Valley food hygiene inspections](https://www.andoveradvertiser.co.uk/news/24479015.data-shows-backlog-test-valley-food-hygiene-inspections/)
* Banbury FM: [Crisis in food safety](https://banburyfm.com/news/crisis-in-food-safety/)
* BelfastLive: [Lisburn & Castlereagh tops NI hygiene poll as UK wide food safety concerns raised](https://www.belfastlive.co.uk/news/northern-ireland/lisburn--castlereagh-tops-ni-29636915)
* Belfast Telegraph: [Concern for food safety in NI as one in five UK eateries have not been inspected in two years](https://www.belfasttelegraph.co.uk/business/food-drink-hospitality/concern-for-food-safety-in-ni-as-one-in-five-uk-eateries-have-not-been-inspected-in-two-years/a844310017.html)
* Birmingham Live: [Midlands town where over half of restaurants and takeaways have not had hygiene inspections for two years](https://www.birminghammail.co.uk/black-country/midlands-town-over-half-restaurants-29640138?utm_source=app)
* Bristol Live: [Food hygiene ratings: one in ten Bristol businesses not inspected for over two years](https://www.bristolpost.co.uk/news/bristol-news/food-hygiene-ratings-one-ten-9454370)
* Cambrian Live: [Food inspections backlog putting health at risk](https://www.cambrian-news.co.uk/news/food-inspections-backlog-putting-health-at-risk-709093)
* Grimsby Telegraph: [Half of North East Lincolnshire's food outlets have not had a food hygiene inspection in two years](https://www.grimsbytelegraph.co.uk/news/grimsby-news/half-north-east-lincolnshires-food-9444120)
* Hull Daily Mail: [Hull one of the best councils in the country at regular food hygiene inspections](https://www.hulldailymail.co.uk/news/hull-east-yorkshire-news/hull-one-best-authorities-country-9444982)
* iNews: [Food hygiene ratings mapped: The areas with the worst inspection backlogs](https://inews.co.uk/news/consumer/food-hygiene-ratings-mapped-areas-inspection-backlogs-3197836)
* Kent Online: [Figures show Folkestone and Hythe, Canterbury and Dover councils struggling to inspect food businesses within two years](https://www.kentonline.co.uk/kent/news/serious-public-health-issue-as-1-in-10-kent-restaurants-ov-310608/)
* KL1 Radio: [How many restaurants and takeaways in our area have had recent hygiene checks?](https://kl1radio.co.uk/how-many-restaurants-and-takeaways-in-our-area-have-had-recent-hygiene-checks/)
* Lincs Online: [Which Lincolnshire councils have biggest backlog in food hygiene inspection?](https://www.lincsonline.co.uk/skegness/backlog-in-food-hygiene-inspections-is-a-serious-public-hea-9376602/)
* MyLocal Lincolnshire: [North East Lincolnshire's food hygiene inspection backlog revealed](https://mylocal.co.uk/feed/232364/north-east-lincolnshire-s-food-hygiene-inspection-backlog-revealed)
* The Lincolnite: [Almost 850 food venues in Lincolnshire waiting over two years for hygiene inspection](https://mylocal.co.uk/feed/232446/almost-850-food-venues-in-lincolnshire-waiting-over-two-years-for-hygiene-inspection?election-hub=true)
* BBC Lincolnshire: [Councils among worst for food hygiene inspections](https://www.bbc.co.uk/news/articles/c147jp874nqo)
* Lincolnshire Live: [Council boss claims food hygiene inspections are happening despite worrying data](https://www.lincolnshirelive.co.uk/news/local-news/council-boss-claims-food-hygiene-9454751)
* Lynn News: [How many restaurants and takeaways in King’s Lynn, West Norfolk, Breckland and North Norfolk haven’t received food hygiene ratings in past two years?](https://www.lynnnews.co.uk/news/how-many-restaurants-and-takeaways-in-our-area-have-been-che-9376647/)
* The Mirror: [Food safety backlog mapped as public 'at risk of major food poisoning'](https://www.mirror.co.uk/news/uk-news/food-safety-backlog-mapped-public-33353907)
* Southampton Daily Echo: [Half of Southampton's food sites go without inspection since 2021](https://www.dailyecho.co.uk/news/24486666.half-southamptons-food-sites-go-without-inspection-since-2021/)

