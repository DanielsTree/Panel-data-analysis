Panel-data-analysis
Ironhack Final project 12/2020. Socio-economic time-panel analysis in Python, based of self-constructed paneltable using different Regression models

Prework Excel:
1. I checked all corona related indicators on Eurostats: https://ec.europa.eu/eurostat/web/covid-19/data
 Which ones I could use. My first approach was using quarterly measured indicators. Decided which to choose and built up a time panel database. 
 But after discussing the strength a model could have with the few datapoints I had decided to build a new database.
2. Downloaded data tables as .tsv file and imported them to Excel.
3. Major prework/data manipulation for the time-panel analysis did in Excel, The imported tables looked like this when raw:
a) checked the data tables and values to get a feeling about the data
b) deleted columns freq, currency, bop_item, sector_10, sectorpart, stk_flow, partner
c) changed column name geo/time period to country.
d) cleaned the tables. deleted all letters and colons out of the numeric fields. Had to do this in different steps as datatype changed when simply replaced.
4. When data was clean to work with, I had a look on the time series, and countries I could use for Analysis. As seen in graphic above in some table some 
countries had missing data, or no data at all.
The countries were randomly chosen by availability of data. Decided to go for 13 countries because 13th is my birthday. And I didn ́t want to spend 
too much time on creating a time series panel table. For each of the 13 countries there exist 8 indicators and 129 data points for each indicator, 
leads to a total datapoints for modelbuilding in machine learning analysis of:
Total: 13.416
5. Next step was to transpose each table
6. After finishing transposing the tables I built a time-panel-master.xlsx, where I did import the data in. Next page is seen a section of final version 
time-panel-master.xlsx to be imported in Python to be analyzed by descriptive, inferential, and advanced analytical models.

Panel-analyis Python:
1. Scope of Analysis

1.1 Description of analysis
1.2 Methodology
1.3 Hypothesis
2. Importing tools and data
3. Checking the data
4. Data manupulation / Preprocessing

4.1 Changing the categorical columns to numerical
4.2 Setting column Time to datetime format
4.3 Dealing with NAN values
5. EDA: Data explained by descriptive statistics

5.1 Describing the data
5.2 Analyzing Unemployment_rate and Youth_unemployment_rate over time
5.3 Plotting and interpretating the results of time series analysis
5.4 Analysing mean average of youth unemployment and total unemployment from researched countries
5.5 Plotting results
5.6 Analyzing average mean of all used indicators over time intervall 2010 - 2020
5.7 Plotting Balance Payment and Trade Volume over time 01/2010 - 09/2020 by lineplot
5.8 Scatterplot Sentiment indicator & Balance Payment and Trade Volume over time 01/2010 - 09/2020 by lineplot
5.9 Plotting Inflation rate, Rental housing, Sentiment_indicators, Slaughtering_in_slaughterhouses over time 01/2010 - 09/2020 by lineplot
5.10 Interpretation of Lineplot 

6. EDA: Analyzing linear relation between Economic Sentiment Indicator and independent indicators by scatterplot visualisation containing regression line

7. Inferential statistics

7.1 Hypothesis prove of Economic Sentiment Indicator by one-sided T-test
7.2 P-value

8. Correlation

8.1 Correlation Matrix
8.2 Interpretation of results
8.3 Autocorrelation
8.4 Conclusion of the results so far and the next steps

9. Panel analysis: modeling regression on Economic Sentiment Indicator
9.1 Using Train/Test Split on Dataframe
9.2 Defining models for linear Regression Sklearn
9.3 Using SVR Model, KNeighbors Regressor, DecisionTree Regressor, Gradient Booster, RandomForest Regressor, MLP Regressor
9.4 Interpretation of results Regression on Economic Sentiment Indicator

10. Panel analysis: modeling regression on Youth Unemployment Rate
10.1 Using Train/Test Split on Dataframe
10.2 Defining models for linear Regression Sklearn
10.3 Using SVR Model, KNeighbors Regressor, DecisionTree Regressor, Gradient Booster, RandomForest Regressor, MLP Regressor
10.4 Interpretation of results Regression sklearn-models on Youth unemployment rate 10.5 Multiple Regression on Youth Unemployment Rate with Statsmodels
10.6 Multiple linear Regression on Youth Unemployment Rate with Statsmodels 10.7 Visualisation of choosen single linear relations by plotting with regression scatter plots 10.8 Interpretation of results

11. Conclusion of Analysis
