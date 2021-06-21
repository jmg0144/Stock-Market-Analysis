# Stock Market Time Series Analysis
Author: Justin Giovatto
## Business Problem
A stock market investor is looking to invest in a portfolio consisting of three technology companies, three healthcare companies, as well as one cryptocurrency for the next six month period. The investor also would like to minimize risk in the protfolio. 
## Overview/Methods
This notebook will analyze the top ten tech and healthcare stocks according to volume traded as well the top five cryptocurrency stocks by volume traded. The stocks will then be analyzed according to past future returns dating back to January 2016. The stocks' volitility over that period as well as price to earnings ratios (P/E ratios) will also be taken into account for the tech and healthcare stocks in order to analyze potential risk. A sarima model and Facebook Prophet model will then be run on each of the stocks in order to predict future returns over the next six month period. Model results will then be compared and analyzed, and portfolio investment reccomendations will then be provided based on the analysis. 

## Data
The stock data used for this project is from the Yahoo Finance API. The top 10 stocks with at least 5 years of trading data, according to volume traded in the technology and healthcare sectors will be analyzed. Also the top 5 cryptocurrency stocks with at least 5 years of trading data, according to volume traded will also be analyzed. The start date for the stocks is January 1st, 2016 and the end date is June 1st, 2021. The stocks will then be broken up into individual dataframes as well as combined into three seperate dataframes according to sector. The stocks are formated into daily data and provides the following features: "High", "Low", "Open", "Close", "Volume", and "Adj Close". An additional column for "Stock" (name), "Returns", and "Cumulative Returns" will also be added onto the data for analysis.


## Results & Conclusions  
 - Top 3 Tech Stocks to invest in:
     1. Nvida
     2. Tesla
     3. TSMC
     
     
 - Top 3 Healthcare Stocks to invest in:
     1. Bio-Rad
     2. United Health
     3. HCA
     
     
 - Top Cryptocurrency to invest in:
     1. Ethereum

 
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