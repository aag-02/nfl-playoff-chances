# playoff-chances
In this project, my goal was to predict the chance of a team making the playoffs in both the current year and the following year. If given a dataset of  player stats, accolades, and various records for a team, could I predict if that team makes the playoffs? Likewise, if given historical data of a team, can I predict if they'll make the playoffs the following year, where I have no knowledge of that year's data?

Methodolody:
To begin the project, I needed to brainstorm the predictor variables to include in my model. Instead of using team statistics for offense, I wanted to create individual ratings for each position as a team's success is highly dependent on individual players, espeically quarterback. For this, I scraped the seasonal statistics for each offensive player from ProFootballRefrence. I used the same website to scrape defensive team statistics.
