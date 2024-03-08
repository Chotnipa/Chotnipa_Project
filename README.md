# Chotnipa_Ruttnaraweekool
⭐️ All my data project 
<h3>Compairs_Avg5.ipynb</h3> 
step1: ดึงรายชื่อหุ้นปุัจจุบันทั้งหมดจาก database และนำรายชื่อหุ้นทั้งหมดไปดึงข้อมูลจาก yahoo finance
<br />step2: หาหุ้นที่มีเงื่อนไขต่างๆดังนี้

-  %Change_C2C > 0.01
-  %CMPR > 100
-  Volume > 10,000,000
<br /><br />หากเจอหุ้นที่ตรงตามเงื่อนไขด้านบนจะระบุข้อมูลเพิ่มเติมคือ

 - %Change_O2C
 - Volume BUY
 - Volume SELL
 - %BUY 
<br /><br />ตัวอย่างข้อมูลที่ได้:

| Date       | Symbol | %Change_C2C | %CMPR | Volume    | %Change_O2C | BUY     | SELL    | %BUY   |
|------------|--------|-------------|-------|-----------|-------------|---------|---------|--------|
| 2024-03-08 | ABC    | X.XX        | YYY.YY  | ZZZZZZZZZ | A.AA        | XXXXXXX | YYYYYYY | ZZ.ZZ   |
| 2024-03-08 | DEF    | X.XX        | YYY.YY  | ZZZZZZZZZ | A.AA        | XXXXXXX | YYYYYYY | ZZ.ZZ   |


<br />

<br /> <h3>backtest_TFEX_S50.ipynb</h3> 
backtest ของราคาหุ้น โดยใช้ไลบรารี่ TA-Lib(Technical Analysis Library) ซึ่งเป็นไลบรารีโปรแกรมสำหรับการวิเคราะห์ทางเทคนิคในการซื้อขายหุ้นและตลาดทางการเงิน ซึ่งมีความสามารถในการคำนวณและสร้างชุดข้อมูลเชิงทางเทคนิคที่ใช้ในการวิเคราะห์กราฟและความเปลี่ยนแปลงของราคาหลาย ๆ ประเภทมาเพื่อนำมาคำนวน SMA CCI ตามกำหนด
