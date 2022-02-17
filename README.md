# Stock Market Data Analysis
## Business Objective
A stock market investor is looking to invest in a portfolio consisting of three technology companies, three healthcare companies, as well as one cryptocurrency for the next six month period. The investor also would like to minimize risk in the protfolio.

## Data
The stock data used for this project is from the Yahoo Finance API. The top 10 stocks with at least 5 years of trading data, according to volume traded in the technology and healthcare sectors will be analyzed. Also the top 5 cryptocurrency stocks with at least 5 years of trading data, according to volume traded will also be analyzed. The start date for the stocks is January 1st, 2016 and the end date is June 1st, 2021. The stocks will then be broken up into individual dataframes as well as combined into three seperate dataframes according to sector. The stocks are formated into daily data and provides the following features: "High", "Low", "Open", "Close", "Volume", and "Adj Close". An additional column for "Stock" (name), "Returns", and "Cumulative Returns" will also be added onto the data for analysis.

![Screen Shot 2021-09-14 at 2 15 01 PM](https://user-images.githubusercontent.com/66973223/133312926-7576720c-99a5-4fd4-b1bb-c2ea1f5eadd3.png)
 - Apple appears to following a general upward trend which appears to be increasing since late 2019. Apple also appears to have a seasonal component with spikes during the early and late parts of the year.

![Screen Shot 2021-11-11 at 2 46 25 PM](https://user-images.githubusercontent.com/66973223/141359646-22c2aebc-a7ca-4bd6-971f-b6c40248d7aa.png)
 - United Health appears to be autocorrelated up to about 6 lags.

![Screen Shot 2021-11-11 at 2 51 01 PM](https://user-images.githubusercontent.com/66973223/141360030-3e74a401-0b53-406f-8ca6-5f65525c2c35.png)
 - Of the top three crypto stocks Dodgecoin looks to be the most volatile with high returns over 2.5 as well as many returns in the .5 to 1 range. Bitcoin and Ethereum look to have similar volatility though Bitcoin appears to be slightly more stable. Compared to the tech and tealthcare sectors, the cryptocurrencies are clearly the most volatile of the three with a much greater range of returns. 

![Screen Shot 2021-11-11 at 2 46 41 PM](https://user-images.githubusercontent.com/66973223/141359693-1d656e54-ac42-4593-bce9-11d11beff1f2.png)
 - Microsoft appears to follow a fairly steady upward 6 month trend, while Apple follows a similar trend despite a slight dip during 2019 and 2020, before finally beginning to pulling ahead of Microsoft in 2021. Overall Google follows a flatter upward trend than the other two before beginning to slightly increase in 2021. All three stocks appear to be following an upward 6 month trend. 

![Screen Shot 2021-11-11 at 2 46 50 PM](https://user-images.githubusercontent.com/66973223/141359716-a41cefcc-8d70-4b5e-bfb3-58f3f9821e79.png)
 - Overall United Health looks to have most steady increase in 6 month returns despite a slight dip in 2019. HCA seems to be the most volatile of the three, though it does appear to be sharply rising since late 2020. CVS looks to be experiencing a slow, flat downward trend over the past 5 years.

![Screen Shot 2021-11-11 at 2 46 58 PM](https://user-images.githubusercontent.com/66973223/141359746-0773cdae-bbfd-4a8c-8162-a4b66e1c9de5.png)
 - Overall Ethereum seems to be the most volatile of the three crypto stocks wit a sharp increase in 6 month trend during mid 2017 to mid 2018 before sharply dropping again until mid 2019 where it remained flat until late 2020 where it has since dramatically risen to an almost 2000% cumulative return. Bitcoin and Dogecoin also remained fairly flat until mid 2021 where Dogecoin sharply rose to about 900% cumulative return, while Bitcoin also began to steadily increase. Overall this could indicate that Crypto stocks are experiencing a sharp rise in cumulative returns and will be interesting to see if it continues going forward.

## Overview/Methods
This notebook will analyze the top ten tech and healthcare stocks according to volume traded as well the top five cryptocurrency stocks by volume traded. The stocks will then be analyzed according to past future returns dating back to January 2016. The stocks' volitility over that period will also be taken into account in order to analyze potential risk. A sarima model and Facebook Prophet model will then be run on each of the stocks in order to predict future returns over the next six month period. Model results will then be compared and analyzed, and portfolio investment reccomendations will then be provided based on the analysis.

![Screen Shot 2021-11-11 at 2 47 37 PM](https://user-images.githubusercontent.com/66973223/141359797-1d246782-7d7e-4ddf-8072-9259442f0473.png)
 - According to the SARIMA model forecast, the top tech stock was Nvidia with a predicted 25.83% increase over the next 6 month period.

![Screen Shot 2021-11-11 at 2 58 49 PM](https://user-images.githubusercontent.com/66973223/141361055-68bb68cb-9413-499b-917f-eeb6293f369f.png)

![Screen Shot 2021-11-11 at 2 47 46 PM](https://user-images.githubusercontent.com/66973223/141359817-f2c38cac-5e29-4d48-b77e-dc4874fe6e44.png)
 - The top healthcare stock according to the SARIMA model was Bio-Rad with a predicted increase of 5.17% over the next 6 month period.

![Screen Shot 2021-11-11 at 2 58 58 PM](https://user-images.githubusercontent.com/66973223/141361114-de5f955c-24f0-4393-8db5-3769c8f117c1.png)

![Screen Shot 2021-11-11 at 2 47 54 PM](https://user-images.githubusercontent.com/66973223/141359839-6be734ad-800f-429e-a975-3a5f298cce88.png)
 - The top cryptocurrency according to the SARIMA model was Dogecoin with a predicted increase of 4,534.25% over the next 6 month period.

![Screen Shot 2021-11-11 at 2 59 06 PM](https://user-images.githubusercontent.com/66973223/141361139-291721ef-521d-4dd1-a6f6-145b5963f5ec.png)

## Results & Conclusions

Based on the above model comparison charts, our two main Tech sector recommendations will be Nvidia and Tesla due to high SARIMA forecasts as well as high min. lower confidence interval predictions. Both these stocks feature the highest main evaluation metric forecasts. The third tech stock recommendation will be TSMC. This stock produces the third highest SARIMA 6 month forecast in comparison to the other stocks in the sector.  

For the healthcare sector I would recommend BIO, HCA, and UNH as these stocks are the highest healthcare stocks in terms of SARIMA forecast and min. lower confidence intervals as seen in the graph below.

Finally for the crypto sector recommendation, although DOGE has the highest SARIMA foercast it also has a significantly lower min. lower confidence interval than ETH, as observed in the above graph. Because avoiding risk is a big factor in choosing this portfolio I would instead recommend ETH over DOGE for this reason.

![Screen Shot 2021-09-14 at 2 19 10 PM](https://user-images.githubusercontent.com/66973223/133313840-9e68237a-8603-49b4-a215-f239e058ef52.png)

![Screen Shot 2021-09-14 at 2 19 24 PM](https://user-images.githubusercontent.com/66973223/133313892-e0e45f48-57cf-4e0a-8746-68af3de823b6.png)

![Screen Shot 2021-09-14 at 2 19 34 PM](https://user-images.githubusercontent.com/66973223/133313949-f1894a33-2bbe-4933-afeb-7c41b172ab8c.png)

* Top 3 Tech Stocks to invest in:
 1. Nvida
 2. Tesla
 3. TSMC
     
* Top 3 Healthcare Stocks to invest in:
 1. Bio-Rad
 2. United Health
 3. HCA
  
* Top Cryptocurrency to invest in:
 1. Ethereum
 
## Future Work
 - Would like to add another model type such as an RNN for further model comparisons.
 
 
 - Would like to analyze more stocks in each sector in order to find potentially better portfolio recommendations.
 
 
 - Would like to look into more stock evaluation metrics in order to improve recommendations further.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/Stock-Market-Analysis/blob/main/Stock-Market-Analysis.ipynb) 
