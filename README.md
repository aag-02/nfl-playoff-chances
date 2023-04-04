# playoff-chances
In this project, my goal was to predict the chance of a team making the playoffs in both the current year and the following year. If given a dataset of  player stats, accolades, and various records for a team, could I predict if that team makes the playoffs? Likewise, if given historical data of a team, can I predict if they'll make the playoffs the following year, where I have no knowledge of that year's data?

Methodolody:

Download HTML: This is the first file in the project. Since I wanted data from the past 20 years for multiple categories, multiple websites sensed that I was "spam" as I had sent numerous requests. To avoid this, I decided on downloading the webpage's HTML into a folder and then scraping the files in the folder instead. This way, I would not get restircted from sites by sending multiple requests. In 'DownloadHTML', I used Selenium Webdriver to download the website HTML into its respective folders. There are 8 total folders, each containing HTML of the 2000-2022 seasons (passingstats, rushingstats, receivingstats, defense, probowl, playoffs, standings, all-pro)

Scrape_Awards: This file was where I scraped all the awards that I was going to use as predictor variables (MVP, Offensive Player of the Year, Defensive Player of the Year, Rookie of the Year, All Pro, Pro Bowl). For this, I used Beauitful Soup to scrape the website, "Pro Football Refrence". Unlike the other variables I discussed in "Download HTML", I was able to scrape the awards directly from the site because it was only one page of awards, instead of 20+ pages as above. Once I scraped the data, I saved each award into a csv file.

Awards_Records: 

To begin the project, I needed to brainstorm the predictor variables to include in my model. Instead of using team statistics for offense, I wanted to create individual ratings for each position as a team's success is highly dependent on individual players, espeically quarterback. For this, I scraped the seasonal statistics for each offensive player from ProFootballRefrence. I used the same website to scrape defensive team statistics.
