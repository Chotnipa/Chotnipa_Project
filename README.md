# Chotnipa_Ruttnaraweekool
### ⭐️ All my data project 

### 📈 Project Compairs_Avg5
##### Fetching Stock Prices using SQL and Python from Yahoo Finance:

- Utilize a Python library such as `yfinance` to retrieve historical stock prices from Yahoo Finance.
- This library empowers you to specify the stock symbol and the date range for data retrieval.

##### Calculating Desired Metrics:

- After obtaining the stock data, compute various metrics based on your predefined criteria.
- Examples include calculating the percentage change in stock price from one day's close to the next day's close and determining the average percentage change in trading volume over the past 5 days.

##### Filtering Data Based on Criteria:

- Following metric computation, filter the data according to specific conditions you've set.
- Conditions may encompass:
  - A percentage change in stock price exceeding 0.01%.
  - An average percentage change in volume over the past 5 days surpassing 100%.
  - Volume of stock traded on a particular day exceeding 10,000,000.

##### Displaying Relevant Information:

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

<br /> <h3>backtest_TFEX_S50.ipynb</h3> 
backtest ของราคาหุ้น โดยใช้ไลบรารี่ TA-Lib(Technical Analysis Library) ซึ่งเป็นไลบรารีโปรแกรมสำหรับการวิเคราะห์ทางเทคนิคในการซื้อขายหุ้นและตลาดทางการเงิน ซึ่งมีความสามารถในการคำนวณและสร้างชุดข้อมูลเชิงทางเทคนิคที่ใช้ในการวิเคราะห์กราฟและความเปลี่ยนแปลงของราคาหลาย ๆ ประเภทมาเพื่อนำมาคำนวน SMA CCI ตามกำหนด

โดยดึงข้อมูลจาก database ใช้ TimeFrame ที่ 5 นาที หุ้น S50
<br />โดยในโปรเจกกำหนดเปิด long ,เปิด short ดังนี้

เปิด long เมื่อ

- Close(M5) > SMA50
- CCI>150
- Close(M5) > hight 3 แท่งเทียน(ก่อนหน้า)

เปิด short เมื่อ

- Close(M5) < SMA50
- CCI < 150
- Close(M5) < hight 3 แท่งเทียน(ก่อนหน้า)

และหาค่าทางสถิติออกมาเพื่อพิจารณา backtest ว่าได้ผลดีหรือไม่
| Sum Profit | Sum Loss | Max Profit | Max Loss | # Profit | # Loss | AVG Profit | AVG Loss | % Win | % Loss | # max cont profit | # max cont loss | Maximum Drawdown |
|------------|----------|------------|----------|----------|--------|------------|----------|-------|--------|-------------------|------------------|------------------|
| -87,000.60 | -0.29    | -321.04    | 271.00   | 667,105.43 | -754,106.03 | 61,374.26   | -20,902.34 | 81.00% | 187.00% | 8,235.87 | -4,032.65 | 0.30 | 0.69 | 3.00 | 13.00 | 0.45 |

และพล็อตกราฟเพื่อดูภาพรวม

<img width="857" alt="Screenshot 2567-03-08 at 14 34 36" src="https://github.com/Chotnipa/Chotnipa_Project/assets/132806660/e6b855ce-5632-45bd-98d3-5411c6597e82">



