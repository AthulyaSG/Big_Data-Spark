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
## Feature Categorization
* Temporal Features: Date (Timestamp)
* Quantitative Features/Continuous Variables: Volume, Open, High, Low, Close, Adjclose
* Qualitative Features: Symbol/Ticker
![image](https://github.com/user-attachments/assets/2df0d202-9108-43b8-b7f5-5497b4c14a27)
- symbol -> string
- date -> date format and is used for storing date-related information
- volume -> long (i.e., integer)
- open, high, low, close, and adjclose -> double (i.e., floating point)















