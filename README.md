# Crypto Price Analysis: XRP

The cryptocurrency market has experienced unprecedented growth and volatility in recent years. As a prominent player in this dynamic ecosystem, XRP has garnered significant attention from investors, traders, and researchers alike. Understanding the price behavior of XRP is crucial for making informed decisions and identifying potential investment opportunities.

![image](https://github.com/user-attachments/assets/a6fafbd6-1584-4d95-80ef-967af644ce31)

<div align="center">Fig.1 Architecture frameworFig. Graph generated for gold price, XRP, and US inflation rate yoyk</div>



This analysis delves into the intricate world of XRP price data, aiming to uncover patterns, trends, and correlations that can shed light on the factors influencing its value.  By employing advanced data analysis techniques, this study aims to provide valuable insights into XRP's price movements, contributing to a deeper comprehension of this complex asset.

![image](https://github.com/user-attachments/assets/d19c2e6d-f14d-4011-b289-65aadddbf706)

<div align="center">Fig.1 Architecture framework</div>

## 1. Data Collection
   
Collect all available XRP data from May 2018 to December 2022 from Binance’s public data from the link below:

https://data.binance.vision/?prefix=data/spot/monthly/klines/XRPUSDT/1d/

![image](https://github.com/user-attachments/assets/c0ca1b1f-050c-4ba9-8305-7173fcf35a54)

<div align="center">Fig.2 Binance’s public data</div>

![image](https://github.com/user-attachments/assets/edba70cc-b6b3-4f70-bd94-8dc72eedeea2)

<div align="center">Fig.4 Import data in Python</div>


## 2. Import the data

Import the data in an Excel  or Google spreadsheet and combined in a CSV after that importthe data using Python Pandas.

![image](https://github.com/user-attachments/assets/a091eaa5-5089-42cd-8c25-c7638c53732a)

<div align="center">Fig.3 Excel spreadsheet</div>

## 3. Specify Parameters
   
The data is representing the SPOT – Klines, information refer to the link below:

https://github.com/binance/binance-public-data/

![image](https://github.com/user-attachments/assets/8374417a-e413-44bc-8926-3b81f8e9f408)

<div align="center">Fig.5 XRP data in CSV file</div>

- Open time is the specific time period during which a financial market is open and available for trading. The US stock market is open Monday to Friday from 9:30 a.m. to 4:00 p.m. Eastern Time. Here's an overview of stock market opening hours in different US time zones: 

![image](https://github.com/user-attachments/assets/666a4a2a-0cda-4661-a516-53d765d1aefb)

<div align="center">Fig.6 Stock market opening hours [1]</div>

- Open is the price of an asset at the beginning of a trading session or period. The first trade price for any listed stock is its daily opening price. The opening price is an important marker for that day's trading activity, particularly for those interested in measuring short-term results.
- High is the highest price that an asset has reached during a given trading session or period.
- Low is the lowest price that an asset has reached during a given trading session or period.
- Close is the price of an asset at the end of a trading session or period.
- Volume is the number of shares, contracts, or units of an asset that have been traded during a given period of time, such as a day, week, or month.
- Close time is the specific time period during which a financial market is closed and no longer available for trading.
- Quote asset volume is the total trading volume of a particular asset that is used as the quote currency in a trading pair and to measure the liquidity of a trading pair. Quote asset volume is used to measure the liquidity of a trading pair, as well as the popularity of a particular asset as a quote currency. High quote asset volume generally indicates a high level of liquidity and interest in the trading pair, and can make it easier for traders to enter and exit positions in the market. Low quote asset volume, on the other hand, may indicate lower liquidity and make it more difficult for traders to execute trades.
- Number of trades is the total number of transactions that have been made for a particular asset during a given period of time and is used to identify potential buying and selling opportunities. Number of trades is considered to be an important indicator of market activity and liquidity, as it can provide insight into the level of interest in a particular asset. High number of trades generally indicates strong investor interest in an asset, while low number of trades may indicate a lack of interest. Moreover, it can also be used to identify potential buying and selling opportunities, as changes in the number of trades can indicate changes in investor sentiment. An increase in the number of trades can indicate that a trend is gaining momentum, while a decrease in the number of trades can indicate that a trend is losing strength.
- Taker buy quote asset volume is the total volume of the quote asset (in a trading pair) that is used to buy the base asset and consumed by taker orders. Taker orders are orders that are executed immediately against the existing orders on the order book. When a taker order is executed, it is matched with one or more existing orders on the order book, and the volume of the quote asset used to buy the base asset is considered as taker buy quote asset volume. High taker buy quote asset volume generally indicates strong buying interest in the asset, while low taker buy quote asset volume may indicate a lack of buying interest.

## 4. Data Cleanup
   
The data was cleaned for duplicate, missing values, and any format errors by using Python in Fig.7 and specifying a summary of the cleaning done in Fig.8 and the result achieved.

![image](https://github.com/user-attachments/assets/0c2a9abf-5131-4e5d-b9d2-ab400bcb28e1)

<div align="center">Fig.7 Data cleanup in Python</div>

![image](https://github.com/user-attachments/assets/0210fc3e-0f6b-48cd-8efe-ee140dc9a3ed)

<div align="center">Fig.8 Summary of data cleanup in Python</div>

## 5. Data Analysis  
1. Descriptive Analysis
  
Descriptive analysis is a summary statistic that quantitatively describes or summarizes features from a collection of information.

Perform descriptive analysis by Python in Fig.9 to specify the important statistics (like min, max,average, median, standard deviation) for the different parameters of price, volume etc. Also specifythe distribution of data and identify the first, second and third quartiles.

![image](https://github.com/user-attachments/assets/7e3ae5c0-cb9a-497b-bd38-3f266e9f79b1)

<div align="center">Fig.9 Descriptive analysis in Python</div>

2. Relative Strength Index (RSI)
  
The relative strength index (RSI) is a momentum oscillator used in the analysis of financial market to measure the speed and change of price movements. Momentum is the rate of the rise or fall in price. The RSI oscillates between zero and 100.

Calculating RSI:

  - Step 1 - The average gain or loss used in this calculation is the average percentage gain or loss during a look-back period. The standard number of periods used to calculate the initial RSI value is 14.
    
   <p align="center">
    <img width="400" src= https://github.com/user-attachments/assets/92154ecf-3cff-4b99-a3e5-af836861b3ef>
</p>
 

  - Step 2 - Once there are 14 periods of data available, the second calculation can be done. Its purpose is to smooth the results so that the RSI only nears 100 or zero in a strongly trending market.
    
    <p align="center">
    <img width="400" src= https://github.com/user-attachments/assets/066ce4f1-ddd9-4daf-bdcd-d6196b714e12>
</p>

    
The relationship between RSI and XRP close price:

![image](https://github.com/user-attachments/assets/3d7c2d8e-6201-41a9-83f7-2f0160e47a11)

<div align="center">Fig.10 Scatter plot of close price and RSI</div>

Analysis: This shows the correlation between the close price and the RSI. There is a positive correlation between the 2 attributes.

3. Exploratory Analysis
   
Exploratory analysis is an approach to analyzing and summarizing data sets to identify patterns, anomalies, relationships, and other features of interest. It will be applied to answer the following questions:
 1. What is the trend in price data?
    
    ![image](https://github.com/user-attachments/assets/59f58bbf-2ec9-4e4f-b2a6-9163abd5c7cc)
    
<div align="center">Fig.11 Closing price trend</div>


Analysis:The chart shows that there is a fluctuation in closing price over the last 5 years between2018 to 2022. The closing trend reached its spike in the first quarter of the year 2021. From thecurrent chart it looks like it’s very unlikely that the XRP Price will break the resistance and lookslike it’ll continue a general downward trend.

![image](https://github.com/user-attachments/assets/5600dc08-3d30-4327-9f36-a6f695c12437)

<div align="center">Fig.12 Closing price trend of SMA and EMA</div>

Analysis: In here, the SMA or EMA is used to find a trend in the data, but it only showed us the same trend described in the previous slide, that it’s looking like a downwards trend.

 2. What is the volume trend?
   
![image](https://github.com/user-attachments/assets/dc769d46-f9a8-4497-9361-0e2b2f836880)

<div align="center">Fig.13 Volume trend of SMA and EMA</div>


Analysis: There is a regular spike in each quarter of the years. Here we see that aside from the spike that happened in third quarter in 2021, the regular trend is that there is a spike in volumealmost once a quarter, which became apparent when we explored all of the data. 

 3. Are there certain days in the month where volume is higher or lower than normal?
    
![image](https://github.com/user-attachments/assets/946b92c9-cb80-4ebb-9764-a7fa42788cc1)

<div align="center">Fig.14 Mean volume and volume by day</div>


Analysis: Mean volume by day is usually reached the highest average volume near the end of the month which is on 23 and the lowest average volume at the beginning of the month on 3. If we recheck the scatter plot of volume by day also shows the same trend however there is the outlier shown on the first day of the month which might screw the average volume at the beginning of the month.

 4. Are there certain months where prices are higher or lower than normal?
    
    ![image](https://github.com/user-attachments/assets/890030fe-3440-4000-9865-4005cefe6d89)


<div align="center">Fig.15 Mean volume and volume by month</div>


Analysis: Mean volume by month which is usually February has the highest volume but if we seeat the scatter plot of volume per month, the highest volume is actually in April and February hasshown the outlier which screws the average volume so the outlier helps to check in order to seethe outlier. And in December usually, by the end of the year, there is a lot of volumes as well but might not reflect as heavy in the mean volume.

 5. Is there a correlation between “Volume” and “Quote Asset Volume”?
![image](https://github.com/user-attachments/assets/abd300ac-7f86-4f6a-8fae-8550aba01d2b)

<div align="center">Fig.16 Scatter plot of quote asset volume and volume with correlation value</div>


Analysis: From the correlation between volume and quote asset volume which is approximately0.82 which means that there is a positive correlation between them, so whenever volume increasesquote asset volume also increases.

 6. Is there a trend in “Number of trades”? What does it specify?
    ![image](https://github.com/user-attachments/assets/4ab672c7-ccea-4856-af76-30d0ae6acdea)

  <div align="center"> Fig.17 Trend of number of trades by year</div>
 

Analysis: There is a spike in each quarter and reached its peak at the first quarter of year 2021. The trend of the number of trades seems to be the same as the volume trend.

  7. Further data correlation
    - Volume by Price
     ![image](https://github.com/user-attachments/assets/12205057-519e-459e-abe8-0df060fd831f)

     <div align="center"> Fig.18 Volume trend by price</div>
     
Analysis: Here, we tried to do further exploration to see if there any effect on the volume based on the closing price, but the data looked regular.
    - Heatmap correlation
    ![image](https://github.com/user-attachments/assets/8e9373f4-ba11-4b4d-a284-3093ff1d6252)

  <div align="center"> Fig.19 Heatmap correlation
    </div>
    
Analysis: Here we just made a heatmap correlation to see if any variable has any effect on theother variables and we found out that the volume and number of trades data don’t have anymajor effect on price data.

  8. Based on the data given, predict the price of XRPUSDT in the next months.
  
  ![image](https://github.com/user-attachments/assets/f1723a68-72cf-418f-a0de-d45e9048331d)

<div align="center"> Fig.20 XRPUSDT Price in next 6 months by Random forest and XGBoost models</div>

Random forest and eXtreme Gradient Boosting (XGBoost) are applied for the prediction sinceRandom forest is a commonly-used machine learning algorithm trademarked, which combines theoutput of multiple decision trees to reach a single result and it handles both classification andregression problems. 

XGBoost is eXtreme Gradient Boosting which is an open-source software library for gradient boosting models. It is used for supervised learning problems such as classification and regression. The main advantage of XGBoost is its ability to handle large datasets with a high number of features and perform well on both linear and non-linear problems. A Gradient Boosting Decision Trees (GBDT) is a decision tree ensemble learning algorithm similar to Random forest, for classification and regression. Ensemble learning algorithms combine multiple machine learning algorithms to obtain a better model. Both random forest and GBDT build a model consisting of multiple decision trees.

Analysis: The predicted trend seems to be repeated the same way as the previous 6 months in 2022and also gets the same trend prediction for both Random forest and XGBoost model methods. Themodel might not be 100 percent accurate but we can observe the probability of trend from this model prediction.

## REFERENCES:

[1] K. Gunnars, “What Time Do Stock Markets Around the World Open and Close?,” 1 January2023. [Online]. Available: https://stockanalysis.com/article/stock-market-hours/. [Accessed12 January 2023].

    








