# 💰 Smart Expense & Investment Tracker
### Built with Power BI | 12,000+ Transactions | 5 Indian Cities

---

## 📌 Project Overview
This is an end-to-end interactive Power BI dashboard 
built to analyze personal finance data including 
income, expenses, savings, and investments across 
5 major Indian cities over 2 years (2024-2025).

This project demonstrates real-world data analytics 
skills including data cleaning, DAX measures, and 
interactive dashboard design.

---

## 🎯 Dashboard Pages

### Page 1: Expense Tracker Analytics Overview
- Total Income, Total Expense, Net Savings, 
  Savings Rate % KPI Cards
- Monthly Income vs Expense Trend (Line & 
  Clustered Column Chart)
- City-wise Expense Breakdown (Bar Chart)
- Expense by Category (Donut Chart)
- Payment Mode Analysis (Pie Chart)
- Interactive Slicers: City, Date, Category

### Page 2: Expense Analysis
- Top Expense Categories (Bar Chart)
- Payment Mode Split (Donut Chart)
- Monthly Expense Heatmap (Matrix)
- Interactive Slicers: Category, Date

### Page 3: Savings & Investment Tracker
- Net Savings, Savings Rate %, 
  Total Investment KPI Cards
- Monthly Savings Trend (Line Chart)
- SIP vs Stocks Comparison (Bar Chart)
- Freelance vs Salary Income (Column Chart)
- Investment Breakdown (Donut Chart)
- Interactive Slicers: Year, City

---

## 📈 Key Metrics
| Metric | Value |
|--------|-------|
| Total Income | 119M |
| Total Expense | 47M |
| Net Savings | 72M |
| Savings Rate | 60.15% |
| Total Transactions | 12,000+ |
| Total Investment | 7M |
| Cities Covered | 5 |
| Time Period | 2024 - 2025 |

---

## 🗂️ Dataset Details
| Column | Description |
|--------|-------------|
| Transaction_ID | Unique ID for each transaction |
| Date | Transaction date |
| Category | Main category (Food, Bills, etc.) |
| Sub_Category | Sub category (Zomato, SIP, etc.) |
| Amount | Transaction amount in INR |
| Payment_Mode | UPI, Card, Cash, Net Banking, Auto Debit |
| Merchant | Merchant name |
| City | City of transaction |
| Income_or_Expense | Type of transaction |

### Categories Covered:
- 🍔 Food (Zomato, Swiggy, Restaurant, Groceries)
- 📱 Bills (Electricity, Internet, Water Bill)
- 🚗 Transport (Uber, Metro, Petrol)
- 🛍️ Shopping (Amazon, Flipkart, Clothes)
- 🎬 Entertainment (Movies, OTT Subscription)
- 🏥 Health (Medical, Pharmacy)
- 💹 Investment (SIP, Stocks)
- 💼 Salary (Monthly Salary, Bonus)
- 💻 Freelance (Project Payment, Consulting)

---

## 🔧 Tools & Technologies
| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard Creation |
| Power Query | Data Cleaning & Transformation |
| DAX | Measures & Calculations |
| Excel/CSV | Data Source |

---

## 🧮 DAX Measures Used
```dax
Total Income = 
CALCULATE(SUM(Expense_Tracker[Amount]), 
Expense_Tracker[Income_or_Expense] = "Income")

Total Expense = 
CALCULATE(SUM(Expense_Tracker[Amount]), 
Expense_Tracker[Income_or_Expense] = "Expense")

Net Savings = [Total Income] - [Total Expense]

Savings Rate % = 
DIVIDE([Net Savings], [Total Income]) * 100

Total Investment = 
CALCULATE([Total Expense], 
Expense_Tracker[Category] = "Investment")

Freelance Income = 
CALCULATE([Total Income], 
Expense_Tracker[Category] = "Freelance")

Salary Income = 
CALCULATE([Total Income], 
Expense_Tracker[Category] = "Salary")

MoM Expense Growth = 
VAR CurrentMonth = [Total Expense]
VAR PrevMonth = CALCULATE([Total Expense], 
DATEADD(Expense_Tracker[Date], -1, MONTH))
RETURN DIVIDE(CurrentMonth - PrevMonth, 
PrevMonth) * 100
```

---

## 💡 Key Insights
- 🏙️ **Chennai** highest spending city (10M)
- 🏥 **Health & Transport** top expense categories
- 💹 **SIP (50.93%)** slightly higher than 
  Stocks (49.07%) in investments
- 💼 **Freelance income** comparable to Salary
- 💳 **Card & UPI** most used payment modes
- 💰 Healthy savings rate of **60.15%**

---

## 📂 Files in Repository
| File | Description |
|------|-------------|
| `Personal_Finance_Dashboard.pbix` | Power BI File |
| `Expense_Tracker.csv` | Dataset |
| `README.md` | Project Documentation |

---

## 👨‍💻 Author
**Gowtham**
- 2 Years Experience as Analyst at Wipro
- Skills: Power BI, DAX, SQL, Excel

---

⭐ If you found this project helpful, 
please give it a star!
