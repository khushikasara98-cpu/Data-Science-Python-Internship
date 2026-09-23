# Executive Financial Performance Analysis (End-to-End Case Study)

An end-to-end financial data analysis project combining **Python (Pandas)** for exploratory data analysis and data cleaning, followed by **Power BI Desktop** for building an interactive, executive-level visual dashboard.

---

## 📌 Project Overview
The objective of this project is to analyze global sales, profitability, market segments, and cost structure using the `Financial Sample` dataset (700 rows, 16 features). The project provides actionable business insights to optimize net margins across products and geographic regions.

---

## 🛠️ Tech Stack & Tools
- **Data Wrangling & EDA:** Python (Pandas)
- **Business Intelligence & Dashboard:** Power BI Desktop
- **Documentation:** Markdown / PDF Report

---

## 📊 Key Business Insights (KPI Summary)
- **Total Units Sold:** 1.13 Million
- **Total Revenue / Sales:** $118.73 Million
- **Total Profit:** $16.89 Million
- **Cost of Goods Sold (COGS):** $102.00 Million

---

## 💻 Python EDA & Data Cleaning
- Handled non-discounted transactions in `Discount Band` (53 missing values) by filling them with `'None'`.
- Verified zero critical null values across financial metrics.
- Cleaned column whitespace formatting.

```python
import pandas as pd

# Load dataset
df = pd.read_excel('Sample data (1).xlsx')

# Clean headers & missing values
df.columns = df.columns.str.strip()
df['Discount Band'] = df['Discount Band'].fillna('None')

# Financial summary
print(df[['Units Sold', 'Sales', 'COGS', 'Profit']].describe())
```

---

## 📈 Power BI Interactive Dashboard
The dashboard includes:
 - **Header Banner:** Modern dark navy layout with clear typography.
 - **KPI Cards:** Units Sold, Total Sales, Total Profit, and COGS.
 - **Line Chart:** Sales & Profit Trend (2013 vs 2014 growth).
 - **Clustered Bar Chart:** Country-wise Sales breakdown (US as market leader).
 - **Donut Chart:** Segment Profitability (Government segment driving highest revenue).
 - **Stacked Column Chart:** Top Performing Products (`Paseo` as top seller).
 - **Interactive Slicers:** Dynamic filtering by Year (2013/2014) and Segment.

![Power BI Interactive Dashboard](Screenshot%202026-09-22%20171242.png)

---

## 🚀 Key Strategic Recommendations
1. **Optimize COGS:** COGS accounts for ~$102M out of $118.73M revenue; reducing production costs will directly improve net profit margins.
2. **Focus on Government Contracts:** The Government segment contributes over 65% of profits.
3. **Expand High-Performing Product Lines:** Scale marketing for `Paseo` across lower-performing geographies like Mexico.
