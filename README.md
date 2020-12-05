# UFCProject
The goal of this project is an attempt to beat the odds of Vegas when it comes to UFC events. The project was started for two reasons. Firstly, we enjoy watching UFC events and this allows us to put our passion towards data science to try to predict the outcome of what we enjoy. The second reason was we wanted to pick a problem that had a measurable outcome. In this case, it will be how well we can predict the outcome relative to Vegas' odds and the expected value of our bets if we were to follow the predictions of our model. We do not expect to beat Vegas but we felt that this gave us a metric that was more meaningful than just accuracy. We scraped the data from Sherdog.com ourselves and we stored the data in a postgres database that we hosted. While you cannot use our database, the necessary Python and SQL scripts are available if you want to recreate our process. If not we have included CSV files that contain the same information that we read and write from SQL.

The files are broken down as follows:

1) WebScrape.ipynb -- Scrapes the necessary information from the Sherdog webiste
2) DB build -- SQL commands needed to set up the database that we used to store our information
3) ETL.ipynb -- this file takes the raw scraped data, cleans and transforms it, and then writes it to our database.
4) Model Building.ipynb -- this file queries our database, creates features, and then uses that data for model selection
