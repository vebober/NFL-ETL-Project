# ETL Project
ETL Project Write Up

# Extract: 

There was a large amount of work determining what data we wanted to use before creating data frames to use for analysis. The API we used (sportsdata.io) is extensive. NFL statistics as a whole are extensive and complicated, and gambling information is no exception. Beyond the large list of player, team, stadium and even weather data, the NFL gambling API alone had 4 different data sources to choose from (pre-game odds, in-game odds, line changes, etc.). Extracting the relevant data and creating dataframes with only the data specific to pregame sports gambling odds in a Jupyter notebook was critical to save time. 

# Transform: 

We needed to determine what data was relevant for just a basic analysis of how gambling on the NFL works. We settled on general information for each game and their pregame odds for the first 6 weeks of the season. We pulled teams, scores, predicted point spread, moneyline and payouts, and more from the API and created data frames for each week. 

# Load: 

After creating CSVs for all 6 weeks of data, we uploaded each dataframe to Postgresql. We chose Postgres because it would make it easier to analyze the data for future use if we decided to use multiple sportsbooks for each game. This would allow us to utilize the one to many relationships you can have in a relational database. We would be able to figure out which sportsbooks (different odds makers) make the most realistic odds for games. Some sportsbooks will, for many different reasons, will lead to more successful or unsuccessful bets. Being able to compare the results from each of the 4-5 sportsbooks easily in Sql.
