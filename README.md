# Credit Card Data Analysis Report

This Power BI project presents an in-depth analysis of credit card data for financial institutions and marketing strategists. The dashboard includes three main views: **Credit Card Revenue Report**, **Customer Report**, and **Weekly Performance Snapshot**, all filtered by demographic and behavioral dimensions.

---

## 🎯 Objective
To monitor and analyze:
- Weekly and monthly revenue trends
- Customer segmentation and satisfaction
- Transaction behavior by profession, income, and card usage
- Delinquency and acquisition costs


---

## 🗂️ Data Tables
### Fact Tables
- **Public CC Details**: Revenue, interest, volume, card type, delinquency, etc.
- **Public Cust Detail**: Demographic data like age, gender, income, job, dependents

### Date Table
- **Week_Start_Date**: Hierarchies for week number, quarter, and year

---

## 📊 Key DAX Measures
```dax
Current Week Revenue = 
CALCULATE(
    SUM('Public CC Details'[Revenue]),
    FILTER(ALL('Public CC Details'),
        'Public CC Details'[Week Number] = MAX('Public CC Details'[Week Number]))
)

Previous Week Revenue = 
CALCULATE(
    SUM('Public CC Details'[Revenue]),
    FILTER(ALL('Public CC Details'),
        'Public CC Details'[Week Number] = MAX('Public CC Details'[Week Number]) - 1))

Wow Revenue = DIVIDE([Current Week Revenue] - [Previous Week Revenue], [Previous Week Revenue])
```
---

## 📈 Visuals & Dashboards

### Dashboard
---
![image](https://github.com/user-attachments/assets/d9d4aa8f-2031-469a-a664-4ecfc2c053a2)

### Transaction Report
---
![image](https://github.com/user-attachments/assets/08373175-55b8-4040-bcf4-a0f70fd090e8)

### Customer Report
---
![image](https://github.com/user-attachments/assets/bc13286c-14b9-4c56-82ed-f0a63a5b8ae5)



