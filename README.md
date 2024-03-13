# Chotnipa_Ruttnaraweekool
### ⭐️ All my data project 

### 📈 Project Compairs_Avg5
**Fetching Stock Prices using SQL and Python from Yahoo Finance:**

- Utilize a Python library such as `yfinance` to retrieve historical stock prices from Yahoo Finance.
- This library empowers you to specify the stock symbol and the date range for data retrieval.

**Calculating Desired Metrics:**

- After obtaining the stock data, compute various metrics based on your predefined criteria.
- Examples include calculating the percentage change in stock price from one day's close to the next day's close and determining the average percentage change in trading volume over the past 5 days.

**Filtering Data Based on Criteria:**

- Following metric computation, filter the data according to specific conditions you've set.
- Conditions may encompass:
  - A percentage change in stock price exceeding 0.01%.
  - An average percentage change in volume over the past 5 days surpassing 100%.
  - Volume of stock traded on a particular day exceeding 10,000,000.

**Displaying Relevant Information:**

- Once data filtration is complete, present pertinent information.
- This may involve showcasing:
  - The date of the trading day.
  - The stock symbol/name.
  - Additional metrics such as the percentage change in stock price from the previous day's open to the next day's close, volume of stock bought and sold, and the percentage of volume bought.

**Automating Daily Updates with an API:**

- To ensure seamless daily operation, establish an API.
- This API will prompt the execution of your Python script, which retrieves the latest data, performs calculations, and updates the database or presents the results.
- Employ scheduling utilities like `cron` (on Unix-based systems) or `Task Scheduler` (on Windows) to schedule the API for execution at a predetermined time each day.

**Example Data:**

| Date       | Symbol | %Change_C2C | %CMPR | Volume    | %Change_O2C | BUY     | SELL    | %BUY   |
|------------|--------|-------------|-------|-----------|-------------|---------|---------|--------|
| 2024-03-08 | ABC    | X.XX        | YYY.YY  | ZZZZZZZZZ | A.AA        | XXXXXXX | YYYYYYY | ZZ.ZZ   |
| 2024-03-08 | DEF    | X.XX        | YYY.YY  | ZZZZZZZZZ | A.AA        | XXXXXXX | YYYYYYY | ZZ.ZZ   |




<br />

### 📈 Project Backtest_TFEX_S50

The backtest of stock prices is conducted using the `TA-Lib` library, which is a program library for technical analysis in stock trading and financial markets. This library has the capability to calculate and generate technical data sets used in analyzing graphs and price changes of various types, in order to compute SMA (Simple Moving Average) and CCI (Commodity Channel Index) as specified.

The data is retrieved from the database using a 5-minute timeframe for the S50 stock.

Long positions are opened when:

- Close(M5) > SMA50
- CCI > 150
- Close(M5) > the high of the previous 3 candlesticks

Short positions are opened when:

- Close(M5) < SMA50
- CCI < 150
- Close(M5) < the high of the previous 3 candlesticks

Additionally, statistical values are calculated to evaluate the backtest's performance:

| Sum Profit | Sum Loss | Max Profit | Max Loss | # Profit | # Loss | AVG Profit | AVG Loss | % Win | % Loss | # max cont profit | # max cont loss | Maximum Drawdown |
|------------|----------|------------|----------|----------|--------|------------|----------|-------|--------|-------------------|------------------|------------------|
| -87,000.60 | -0.29    | -321.04    | 271.00   | 667,105.43 | -754,106.03 | 61,374.26   | -20,902.34 | 81.00% | 187.00% | 8,235.87 | -4,032.65 | 0.30 | 0.69 | 3.00 | 13.00 | 0.45 |

Additionally, a graph is plotted to provide an overview.

![Backtest Graph](https://github.com/Chotnipa/Chotnipa_Project/assets/132806660/e6b855ce-5632-45bd-98d3-5411c6597e82)


<br />

### 📈 Project Webscreping_province_vis


Perform web scraping to gather tourism data from the website https://interstat.tat.or.th/mdgrp/ormap_new/report_thai_general.php. This data reflects the tourism situation in each province from the year 2557 to the present. Collect average accommodation rates per province for each month utilizing the `Selenium` library and `BeautifulSoup` library.

<p align="center">
    <img width="700" alt="Screenshot 2567-03-12 at 16 17 28" src="https://github.com/Chotnipa/Chotnipa_Project/assets/132806660/bbe428f4-3747-4d05-8610-5e37c7c2b24e">
</p>

**Example of the data obtained from web scraping :**
| Province       | Month    | Year | Average Occupancy Rate |
|----------------|----------|------|------------------------|
| Bangkok        | January  | 2562 | 89.32%                 |
| Krabi          | January  | 2562 | 82.91%                 |
| Kanchanaburi   | January  | 2562 | 56.24%                 |
| Kalasin        | January  | 2562 | 51.27%                 |
| ...            | ...      | ...  | ...                    |


https://lookerstudio.google.com/reporting/9786f108-5561-49a8-9b2e-5dc718ea6355
<img width="403" alt="Screenshot 2567-03-12 at 17 57 44" src="https://github.com/Chotnipa/Chotnipa_Project/assets/132806660/16a65fc4-e969-4616-b9e3-1b1830ef24e9">
