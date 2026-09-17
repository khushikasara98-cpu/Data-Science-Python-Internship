# Week 2: SQL Data Analysis Project

## 📌 Overview
This project involves querying a sales dataset with 200 records using **MySQL Workbench** to derive actionable business insights. The analysis answers critical business questions regarding customer spending, order values, product categories, and regional sales distribution.

---

## 🛠️ Tools & Concepts
- **Database Engine:** MySQL Server / MySQL Workbench
- **SQL Functions & Clauses:** `SELECT`, `WHERE`, `GROUP BY`, `ORDER BY`, `SUM()`, `COUNT()`, `AVG()`, `ROUND()`, `TRIM()`

---

## 📊 SQL Queries & Result Outputs

### 1. Top 5 Customers by Revenue
Retrieves the highest-spending customers based on total revenue generated.
```sql
SELECT 
    customer_name, 
    SUM(total_price) AS total_spent,
    COUNT(order_id) AS total_orders
FROM sales_data
GROUP BY customer_name
ORDER BY total_spent DESC
LIMIT 5;
```
![Top Customers](Screenshot%202026-09-16%20140544.png)

### 2. Average Order Value (AOV)
Calculates the overall average spending per order across the dataset.
```sql
SELECT 
    ROUND(AVG(total_price), 2) AS average_order_value
FROM sales_data;
```
![Average Order Value](Screenshot%202026-09-16%20140604.png)

### 3. Category & Sub-Category Performance
Analyzes sales performance and units sold per category and sub-category.
```sql
SELECT 
    category,
    sub_category,
    SUM(quantity) AS total_units_sold,
    SUM(total_price) AS total_revenue
FROM sales_data
GROUP BY category, sub_category
ORDER BY total_revenue DESC;
```
![Category & Sub-Category Performance](Screenshot%202026-09-16%20140649.png)

### 4. Regional Sales Breakdown
Evaluates total revenue and order volume generated across different regions.
```sql
SELECT 
    region,
    COUNT(order_id) AS total_orders,
    SUM(total_price) AS regional_revenue
FROM sales_data
GROUP BY region
ORDER BY regional_revenue DESC;
```
![Regional Sales Breakdown](Screenshot%202026-09-16%20140718.png)
