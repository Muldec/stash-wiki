# Scrapers
Scrapers are the way to retrieve information from websites for your movies/scenes/galleries/performers...etc. Using scrapers wisely, you can avoid typing information manually and repetitively. They can help you quickly establish links between movies/scenes and performers/studios, add relative tags, then download covers/posters for easy recognition. It's a great feature to organize your video or image collections.

## Installation
To install a scraper:
  1) Make sure you have the "scrapers" folder in the same location of your Stash app. If you don't have it, create that folder/directory. You can also specify the name of this folder in the config.yml.
  2) Go to the [community scrapers repo](https://github.com/stashapp/CommunityScrapers) and download the scraper you want. Read the [scrapers list](https://github.com/stashapp/CommunityScrapers/blob/master/SCRAPERS-LIST.md) and make sure which one to download. All scrapers are in .yml format. Some of them requires Python, if you use those, you need to install Python in your machine, and don't forget to get the corresponding .py file as well.
Note: For Python scrapers, it's also helpful to read the .py file. Some of them require extra python components installed to work.
  3) Once the new scrapers are in position, you need to go to "Settings->Scraping" and click on "Reload Scrapers" button. You should see your scrapers listed in the list below that button.
  4) Navigate to the scene/gallery/movie/performer you want to scrape.
* If that's a URL scraper, you need to paste the URL in its "URL" blanket, and the scrape icon next to it should light up.
* If that's a Search-By-Name scraper, you can provide the name and choose "Scrape With...", and the scraper should fetch the list of potential matches for you.
5) You will preview the scrape result before you commit the change. Check on the left will keep the original value, check on the right will make the change.

## More Details
You can view the [detail information about scrapers here](https://github.com/stashapp/stash/blob/develop/ui/v2.5/src/docs/en/Scraping.md) .

## Create your own.
To create your own scraper, there is [detail information about that as well](https://github.com/stashapp/stash/blob/develop/ui/v2.5/src/docs/en/ScraperDevelopment.md). Best way to start is to read the simple ones and understand how xpath works. The [XPath Cheetsheet](https://devhints.io/xpath) is quite useful in creating a yml file. In Firefox you can use xpath search in "Web Developer Tools (F12)". The "search HTML" bar actually accepts xpath searches. You can use it to verify your xpath queries.

## Contribution
The Scraper community always welcome new members. If you create a nice scraper and find it stable and useful, you can share it via [the GitHub repo](https://github.com/stashapp/CommunityScrapers). Create a pull request, and let the mod review your work. It will be a great feeling once your contribution is accepted by the community.