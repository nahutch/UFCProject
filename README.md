# UFCProject
The goal of this project is an attempt to beat the odds of Vegas when it comes to UFC events. The project was started for two reasons. Firstly, we enjoy watching UFC events and this allows us to put our passion towards data science to try to predict the outcome of what we enjoy. The second reason was we wanted to pick a problem that had a measurable outcome. In this case, it will be how well we can predict the outcome relative to Vegas' odds and the expected value of our bets if we were to follow the predictions of our model. We do not expect to beat Vegas but we felt that this gave us a metric that was more meaningful than just accuracy. We scraped the data from Sherdog.com ourselves and we stored the data in a postgres database that we hosted. While you cannot use our database, the necessary Python scripts are available if you want to recreate our process. If not we have included CSV files that contain the same information that we read and write from SQL.

The files are broken down as follows:

Scripts
1) WebScrape.ipynb -- Scrapes the necessary information from the Sherdog webiste 
2) ETL.ipynb -- this file takes the raw scraped data, cleans and transforms it, and then writes it to our database. This script also creates the tables within the dataframe.
3) Model Building.ipynb -- this file queries our database, creates features, and then uses that data for model selection

CSV's 
Under the UFC Data Folder
1) raw_total_fights -- contains information on UFC fighters that was taken from Kaggle. Necessary for the ETL script.
2) scraped_fights -- contains the information scraped from Sherdog.com. Necessary for the ETL script.
3) fight_data_cleaned - contains the cleaned fight data that was added to our database. Necessary for the Model Building script.
4) fighter_data_cleaned -- contains the cleaned fighter data that was added to our database. Necessary for the Model Building script.
