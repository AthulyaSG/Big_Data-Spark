### Stock Market
* The process of buying and selling stocks involves transactions in the stock market
* Companies secure capital in the stock market through the sale of shares, or equity, to investors
* A stock signifies ownership in a company or organization, entailing a proportional stake in its assets and earnings
* Stock exchanges serve as secondary markets where shareholders can engage in transactions (Hayes, 2023)
## PySpark
* To facilitate the integration of Spark and Python
* The Python API for Apache Spark, an open-source distributed computing framework and collection of libraries for processing massive amounts of data in real-time
* PySpark not only offers an API for Spark but also aids in connecting with Resilient Distributed Datasets (RDDs)
* Contrast between Pandas and Spark dataframes lies in their execution
* In PySpark, operations are postponed until they are specifically requested in the pipeline (PySpark, n.d.)
## Long Short-Term Memory
* Long Short-Term Memory (LSTM) stands out for its proficiency in capturing intricate patterns and dependencies within historical data
* LSTM shows promise for understanding the unpredictable nature of the stock market
* LSTM uses memory cells, gates, and well-designed connections to selectively store and transmit information over extended time periods, allowing these models to effectively capture complex temporal patterns in sequential data, especially in predicting time series data like stock prices (Chauhan, 2023)
## Data Characteristics
- Number of rows: 68522038
- Number of columns: 8
![image](https://github.com/user-attachments/assets/92ea9f82-3195-46ce-a120-7df79a69ab6a)

- Minimum and maximum dates are determined
- Timeframe from January 2, 2015, to July 2, 2020
![image](https://github.com/user-attachments/assets/0bb4da6f-7f6b-43e5-9cdc-aaf49c22810b)
- Total count of distinct company symbols
- Presence of 6335  companies
![image](https://github.com/user-attachments/assets/f9af7d1b-54f4-4b5b-b2a6-4e30117b97e8)

## Data
- Date: Date of each transaction from 2015 to 2020
- Open: Opening price, denoting the initial transaction price per share in the beginning of a day
- High: The highest price during the trading in a day
- Low: The lowest price for the trading in a day
- Close: Closing price, representing the transaction price at the end of a trading day
- Close Adjusted: The adjusted closing price is adjusted to dividends and stock splits
- Volume: The number of stocks of a company transacted in a day
- Symbol: The unique identifier or ticker for a stock of a company

![image](https://github.com/user-attachments/assets/a57f1187-76d7-455d-af88-97cb5fd4dbf2)
### Data Categorization
* Temporal Features: Date (Timestamp)
* Quantitative Features/Continuous Variables: Volume, Open, High, Low, Close, Adjclose
* Qualitative Features: Symbol/Ticker
  
![image](https://github.com/user-attachments/assets/4ff2fbc9-e5a7-4eb4-a28c-f3791470b8e4)

- symbol -> string
- date -> date format and is used for storing date-related information
- volume -> long (i.e., integer)
- open, high, low, close, and adjclose -> double (i.e., floating point)

## Data Preprocessing
- Check for missing values
- No null values

![image](https://github.com/user-attachments/assets/6f2a99de-9a77-4e91-8936-260e9780c5d9)

- Filtered a list of company using symbols
- Calculated the number of occurrences
- Arranged in descending order
1. Apple -> AAPL
2. Amazon -> Amazon
3. Google -> Google
4. Microsoft -> MSFT
5. Tesla -> TSLA

 ![image](https://github.com/user-attachments/assets/6ef774b2-b2b8-4a1e-8141-4f8a3ed25f99)

## Visualization
### Boxplots

- Visualized outliers
- Plotted each attribute of all 5 stocks
- Eventhough there are outliers, it cannot be removed/modified as it will remove the important values

![image](https://github.com/user-attachments/assets/255bdecf-160c-488a-ac14-4baf20b638d0)

- Plotted each stock separately based on features
- Large volume: MSFT, followed by AAPL
- Highest price: AMZN
- Open is not considered, as previous day close is same as the open for the next day

![image](https://github.com/user-attachments/assets/f24194e8-4d07-4f33-9a85-e4b85aa534aa)

### Bar Chart

- Plotted bar chart for volume of each stocks
- APPL has the largest volume, followed by MSFT

![image](https://github.com/user-attachments/assets/d594d7c3-757e-44da-9b36-98099863095a)

### Histograms
- Histograms are used for continuous variables.
- APPL and AMZN have the highest volume
- The highest price rate (high, low, close, and adjclose) is for AMZN
- The lowest for MSFT

![image](https://github.com/user-attachments/assets/1ade71fd-f63e-47e7-a538-9b3033684303)


## Descriptive Analysis

** AAPL **
- Mean close : 168.11
- SD : 60.89
- Minimum close : 90.34
- Maximum close : 366.53

![image](https://github.com/user-attachments/assets/ea858804-a9ee-49f5-ae33-8a2b517b1084)


** GOOG **
- Mean close : 954.07
- SD : 257.03
- Minimum close : 491.20
- Maximum close : 1526.69

![image](https://github.com/user-attachments/assets/60f30429-e79a-43ed-8f96-8f6e7704fdf6)

** AMZN **
- Mean close : 1213.50
- SD : 601.22
- Minimum close : 286.95
- Maximum close : 2890.30

![image](https://github.com/user-attachments/assets/2c797445-3ffe-4a32-9fe8-13ce78bcda90)

** MSFT **
- Mean close : 89.55
- SD : 40.84
- Minimum close : 40.29
- Maximum close : 206.26

![image](https://github.com/user-attachments/assets/d7803982-3269-4d0a-9f7f-05acbd61c563)

** TSLA **
- Mean close : 310.69
- SD : 152.18
- Minimum close : 143.67
- Maximum close : 1208.66

![image](https://github.com/user-attachments/assets/fde030c1-cfae-4f38-85cf-10249e5594d1)

## Time Series Analysis

- To identify historical patterns, model price movements, and make predictions
- AMZN: Upward trend, exponential growth after 2018
- GOOG: In 2015, exhibited the highest stock price, but later surpassed by AMZN, after mid-2016
- TSLA: Steady till 2020
- AAPL and MSFT: No major changes

![image](https://github.com/user-attachments/assets/1b3557ec-9874-4b51-89a1-7f90c5d58e58)

## Daily Return

- To check the day-to-day fluctuations in pricing of each stock
- AMZN: High daily return percentage, touching 1000 in 2019
- TSLA: Initially high, then dropped to 100 mid-2019
- GOOG and APPL: Less volatility with some overlaps
- MSFT: Not much daily returns

![image](https://github.com/user-attachments/assets/786fed9c-ac6f-4b81-81e2-69929071e397)

## Moving Average

- Help identify trends by reducing noise in price
- 30-day and 50-day rolling averages: calculating the average value of a stock price over a specified window of time
- Overall trend: Upward

![image](https://github.com/user-attachments/assets/072fe0eb-16d5-4e94-b80f-6bfcb51278d2)

## Volume Analysis

- MSFT exhibits higher average trading volumes
- AAPL is closely followed by MSFT
- AMZN, GOOG, and TSLA have no noticeable movement

![image](https://github.com/user-attachments/assets/9bccec98-c94c-4214-9fa7-f22c8c6d959a)

## Correlation

- To identify where the majority of values lie
- To determine whether there is any relationship between each feature

![image](https://github.com/user-attachments/assets/6438e704-f068-4732-b184-19e02bc8273c)

- Distribution of values for the numerical column
- Open, close, high, low, and adjclose are similar

![image](https://github.com/user-attachments/assets/009c2d13-d476-4ab6-bd27-47b3e7108aeb)

To check the correlation,
- if the value is near to -1, then it is strong negative correlation
- if the value is near to 0, then it is weak correlation
- if the value is near to +1, then it is strong positive correlation
- As the values of high, low, close, and adjclose are the same, all the correlation is represented as 1.

![image](https://github.com/user-attachments/assets/5911dd84-7f1a-4b10-b7a6-c136483c2429)

- AAPL stock is decreased till 2016
- After 2016, there was an upward trend eventhough it decreases in later years
- No visible variations in high, low, close, and adjclose values, indicating all are more similar to one another.

![image](https://github.com/user-attachments/assets/f2480b34-935f-47f1-ac46-53a37a5f24c0)

## Model

- Filter the stock to be predicted
- In this case, AAPL is considered from 5 stocks
- Target variable: close

![image](https://github.com/user-attachments/assets/23ff6057-1a0a-41ec-9fca-236065254e52)

![image](https://github.com/user-attachments/assets/3a0ef87a-bb3d-434e-b684-9fe47b68cb08)

### Data Preprocessing

Normalization of the values is performed to make all the values to be consistent
- All values are treated equally
- Optimization algorithms work faster

![image](https://github.com/user-attachments/assets/f71e8106-437b-4d8d-8864-48db0225acee)

### Train and Test Split

- Training: 80% of the data
- Testing: 20% of the data

![image](https://github.com/user-attachments/assets/980b4399-872d-4b8b-98dc-7a92e7bd1d60)



















