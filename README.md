# Stockscraper
This project consists of the program taking and storing information from YahooFinance, then visualizing the acquired data in an appropriate format.
The goal of the project is to create a stock market index for the swedish large cap industrial companies and compare the result to the Stockholm market index for the 30 most traded stocks (OMXS30).

The program works in the following way:
- First, a MySQL database and a empty table is created ready to be filled in with information about the companies.
- Secondly a webscraper is created that is able to gather the information from the chosen website through iteration within a while-loop
- Thirdly a second table is created within the database that temporarily stores the acquired data, which then is merged with the first table.
- Fourthly, When the tables are merged the insertion of the data from the temporary table begins, where the data from the first table is already available i.e the tickersymbols for the stocks.
- Fifthly, the data is visualized through plots, in this case stock charts.

In order to test the validity of the acquired information, each stock is visualized in a plot. An average of each company is calculated through the summation of all stocks closing value at ervery given date divided by the number of stocks, the average is then visualized as the index. Because the growth of the stocks is the main point of interest in this project, not the actual prices, the growth percentage are the values represented on the Y-axis of the plot. The percentage is calculated by taking the first value of every given stock, i.e the closing price for september 9th 2011 and dividing that value by every dated value after that point, the quotient is then multiplied by 100 and 100 is then subtracted from the product to give the value we want, which is the percentage.

Finally, the evenly weighted average of the collected stocks, i.e the index is visualized through a plot along with the OMXS30 to compare the performance of the large cap industrial companies of Sweden with the local market average for the 30 most traded stocks.
