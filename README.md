## Application of PySpark in the Stock Market
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
## Features
- Date: Date of each transaction from 2015 to 2020
- Open: Opening price, denoting the initial transaction price per share in the beginning of a day
- High: The highest price during the trading in a day
- Low: The lowest price for the trading in a day
- Close: Closing price, representing the transaction price at the end of a trading day
- Close Adjusted: The adjusted closing price is adjusted to dividends and stock splits
- Volume: The number of stocks of a company transacted in a day
- Symbol: The unique identifier or ticker for a stock of a company

![image](https://github.com/user-attachments/assets/a57f1187-76d7-455d-af88-97cb5fd4dbf2)
### Feature Categorization
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

## Boxplots

- Visualized outliers
- Plotted each attribute of all 5 stocks
- Eventhough there are outliers, it cannot be removed/modified as it will remove the important values

  ![image](https://github.com/user-attachments/assets/fa504397-e5fe-4609-99f8-4b4ed047dec5)

- Plotted each stock separately based on features
- Large volume: MSFT, followed by AAPL
- Highest price: AMZN
- Open is not considered, as previous day close is same as the open for the next day

  ![image](https://github.com/user-attachments/assets/f24194e8-4d07-4f33-9a85-e4b85aa534aa)

### Visualization

- Plotted bar chart for volume of each stocks
- APPL has the largest volume, followed by MSFT

![image](https://github.com/user-attachments/assets/d817ef64-95d2-45fe-9fb7-79778af891b9)

- Histograms are used for continuous variables.
- APPL and AMZN have the highest volume
- The highest price rate (high, low, close, and adjclose) is for AMZN
- The lowest for MSFT

![image](https://github.com/user-attachments/assets/e44e5355-0997-48a9-a05e-6afa054995cf)



















