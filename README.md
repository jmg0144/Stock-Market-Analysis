# Stock Market Time Series Analysis
Author: Justin Giovatto
## Business Problem
A stock market investor is looking to invest in a portfolio consisting of three technology companies, three healthcare companies, as well as one cryptocurrency for the next six month period. The investor also would like to minimize risk in the protfolio. 
## Overview/Methods
This notebook will analyze the top ten tech and healthcare stocks according to volume traded as well the top five cryptocurrency stocks by volume traded. The stocks will then be analyzed according to past future returns dating back to January 2016. The stocks' volitility over that period as well as price to earnings ratios (P/E ratios) will also be taken into account for the tech and healthcare stocks in order to analyze potential risk. A sarima model and Facebook Prophet model will then be run on each of the stocks in order to predict future returns over the next six month period. Model results will then be compared and analyzed, and portfolio investment reccomendations will then be provided based on the analysis. 

## Data
The stock data used for this project is from the Yahoo Finance API. The top 10 stocks with at least 5 years of trading data, according to volume traded in the technology and healthcare sectors will be analyzed. Also the top 5 cryptocurrency stocks with at least 5 years of trading data, according to volume traded will also be analyzed. The start date for the stocks is January 1st, 2016 and the end date is June 1st, 2021. The stocks will then be broken up into individual dataframes as well as combined into three seperate dataframes according to sector. The stocks are formated into daily data and provides the following features: "High", "Low", "Open", "Close", "Volume", and "Adj Close". An additional column for "Stock" (name), "Returns", and "Cumulative Returns" will also be added onto the data for analysis.

![Screen Shot 2021-09-14 at 2 15 01 PM](https://user-images.githubusercontent.com/66973223/133312926-7576720c-99a5-4fd4-b1bb-c2ea1f5eadd3.png)

![Screen Shot 2021-09-14 at 2 16 13 PM](https://user-images.githubusercontent.com/66973223/133313030-3b25dba1-19c4-4f97-a7f9-350261d5d4e4.png)

![Screen Shot 2021-09-14 at 2 16 40 PM](https://user-images.githubusercontent.com/66973223/133313074-b4aa4557-cba1-41f9-8cf9-31d399d79d01.png)

## Results & Conclusions  
* Top 3 Tech Stocks to invest in:
 1. Nvida
 2. Tesla
 3. TSMC

![Screen Shot 2021-09-14 at 2 19 10 PM](https://user-images.githubusercontent.com/66973223/133313840-9e68237a-8603-49b4-a215-f239e058ef52.png)

![Screen Shot 2021-09-14 at 2 19 24 PM](https://user-images.githubusercontent.com/66973223/133313892-e0e45f48-57cf-4e0a-8746-68af3de823b6.png)
     
* Top 3 Healthcare Stocks to invest in:
 1. Bio-Rad
 2. United Health
 3. HCA

     
* Top Cryptocurrency to invest in:
 1. Ethereum

![Screen Shot 2021-09-14 at 2 19 34 PM](https://user-images.githubusercontent.com/66973223/133313949-f1894a33-2bbe-4933-afeb-7c41b172ab8c.png)
 
## Future Work
 - Would like to add another model type such as an RNN for further model comparisons.
 
 
 - Would like to analyze more stocks in each sector in order to find potentially better portfolio recommendations.
 
 
 - Would like to look into more stock evaluation metrics in order to improve recommendations further.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/Stock-Market-Analysis/blob/main/Stock-Market-Analysis.ipynb) 

For additional information contact Justin Giovatto at justin.giovatto@gmail.com

## Repository Structure

├── README.md

├── Stock_Market_Analysis.pdf

└── Stock-Market-Analysis.ipynb
