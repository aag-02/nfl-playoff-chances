# playoff-chances
In this project, my goal was to predict the chance of a team making the playoffs in both the current year and the following year. If given a dataset of  player stats, accolades, and various team records, could I predict if a certain team makes the playoffs? Likewise, if given historical data of a team, can I predict if they'll make the playoffs the following year, where I have no knowledge of that year's data?

Methodology:

Download HTML: This is the first file in the project. Since I wanted data from the past 20 years for multiple categories, multiple websites sensed that I was "spam" as I had sent numerous requests. To avoid this, I decided on downloading the webpage's HTML into a folder and then scraping the files in the folder instead. This way, I would not get restricted from sites by sending multiple requests. In 'DownloadHTML', I used Selenium Webdriver to download the website HTML into its respective folders. There are 8 total folders, each containing HTML of the websites for the various stats for the 2000-2022 seasons (passingstats, rushingstats, receivingstats, defense, probowl, playoffs, standings, all-pro)

Scrape_Awards: This file was where I scraped all the awards to use as predictor variables (MVP, Offensive Player of the Year, Defensive Player of the Year, Rookie of the Year, All Pro, Pro Bowl). For this, I used Beautiful Soup to scrape the website "Pro Football Reference". Unlike the other variables I discussed in "Download HTML", I was able to scrape the awards directly from the site because it was only one page of awards, instead of 20+ pages as above. Once I scraped the data, I saved each award into a csv file.

Awards_Records: Once the awards from "Scrape_Awards" were converted into a csv file, I imported them into a new notebook called "Awards_Records". In this file, I created a function that dropped unwanted columns, filtered the 'year' column to be greater than 1999, and uses a dictionary to abbreviate the team name (for example, the row value containing 'Green Bay Packers' gets changed to 'GNB'). Once the individual awards were finalized, I merged them into one dataset which I simply called 'awards'. This merged dataset allowed me to use Seaborn and Matplotlib to perform exploratory data analysis, such as visualizing teams with most MVPs since 2000, most Powbowls per team since 2000, and most AllPros since 2000. The next step was to find the win-loss record and playoff performance for every team. For this, I used the same process of using Beautiful Soup to scrape table data on websites such as ProFootballReference and Wikipedia. 

NFL read rosters: The purpose of this file was to find the starting offensive lineups for each team.

NFL Playoffs player stats: 

To begin the project, I needed to brainstorm the predictor variables to include in my model. Instead of using team statistics for offense, I wanted to create individual ratings for each position as a team's success is highly dependent on individual players, especially quarterback. For this, I scraped the seasonal statistics for each offensive player from ProFootballReference. I used the same website to scrape defensive team statistics.
