# 🍕 Pizza Sales Analysis | SQL + Power BI

## 📌 Project Overview

This project focuses on analyzing pizza sales data using **PostgreSQL** for data processing and **Power BI** for visualization.
The goal is to extract meaningful business insights such as revenue trends, best-selling products, and customer ordering behavior.

---

## 🛠️ Tools & Technologies

* SQL (PostgreSQL)
* Power BI
* Data Cleaning & Transformation
* Data Visualization

---

## 📂 Project Structure

```
📁 Pizza-Sales-Analysis
│── 📄 SQL_Queries.sql
│── 📊 PowerBI_Dashboard.pbix
│── 🖼️ dashboard_1.png
│── 🖼️ dashboard_2.png
│── 🖼️ sql_preview.png
│── README.md
```

---

## 🧠 Key Business Questions Answered

* What is the total revenue and average order value?
* Which pizzas generate the highest revenue?
* What are the busiest days and times?
* Which categories and sizes contribute most to sales?
* What are the best and worst-performing products?

---

## 📊 SQL Analysis

SQL was used to:

* Aggregate total revenue, orders, and quantities
* Calculate KPIs like:

  * Average Order Value
  * Average Pizzas per Order
  * Percentage contribution of categories/sizes
* Perform time-based analysis:

  * Daily trends
  * Monthly trends
  * Quarterly insights

### Example Query

```sql
SELECT 
    pizza_category, 
    SUM(total_price) AS total_sales,
    SUM(total_price) * 100.0 / SUM(SUM(total_price)) OVER () AS percentage
FROM pizza_sales
GROUP BY pizza_category;
```

📌 Add your SQL screenshot below:
![SQL Preview](sql_preview.png)

---

## 📈 Power BI Dashboard

### 🔹 Dashboard 1: Sales Performance

* Total Revenue: **817.86K**
* Total Orders: **21,350**
* Total Pizzas Sold: **49,574**
* Average Order Value: **38.31**
* Best & Worst Sellers by:

  * Revenue
  * Quantity
  * Orders

![Dashboard 1](dashboard_1.png)

---

### 🔹 Dashboard 2: Trends & Insights

* Daily order trends (peak on weekends)
* Monthly trends (highest in July)
* Sales distribution by:

  * Category
  * Size
* Performance insights:

  * Classic category leads sales
  * Large size dominates revenue

![Dashboard 2](dashboard_2.png)

---

## 🔍 Key Insights

* 🍕 **Thai Chicken Pizza** generates the highest revenue
* 📦 **Classic Deluxe Pizza** leads in quantity and orders
* 📅 Orders peak on **weekends (Friday & Saturday evenings)**
* 📈 Sales peak in **July**
* 🥇 **Classic category** contributes the most to revenue
* 📏 **Large size pizzas** dominate total sales

---

## 🚀 How to Use This Project

1. Load dataset into PostgreSQL
2. Run SQL queries from `SQL_Queries.sql`
3. Connect Power BI to PostgreSQL
4. Open `.pbix` file to explore dashboard

---

## 🎯 Skills Demonstrated

* SQL querying & aggregation
* Data modeling
* KPI development
* Business insight generation
* Dashboard design in Power BI

---

## 📬 Future Improvements

* Add customer segmentation
* Predict sales using time series
* Automate data pipeline

---

## ⭐ Final Thought

This project demonstrates how raw data can be transformed into actionable insights using SQL and Power BI—bridging the gap between data and decision-making.
