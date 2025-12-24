# 🚲 Task: Adventure Works Sales Analysis

## 🎯 Task Objective
The goal of this project was to analyze the sales performance of "Adventure Works" (a bicycle manufacturing company). The objective was to clean the raw relational data using SQL and then build an interactive dashboard in Excel to track KPIs like Total Sales, Profit Margins, and Reseller Performance.

## 🛠 Tools & Technologies
- **SQL Server (T-SQL):** Used for Data Cleaning, Exploration, and handling NULL values.
- **Microsoft Excel:** Used for creating Pivot Tables, calculating KPIs, and building the final Dashboard.

## 📝 Key Analysis Steps
1.  **Data Exploration (SQL):**
    - Wrote SQL queries (`SQLQuery2.sql`) to check row counts across tables (`Product`, `Sales`, `Reseller`).
    - Implemented **Dynamic SQL** to automatically detect and count NULL values in all columns.
2.  **Data Cleaning (SQL):**
    - Standardized data (e.g., updating 'NA' values in the *Color* column to 'UNKNOWN').
    - Identified and handled duplicates using **CTEs**.
3.  **Data Visualization (Excel):**
    - Imported cleaned data into Excel.
    - Created **Pivot Tables** to analyze Monthly Sales trends and Profit Margins by Category.
    - Designed a **KPI Dashboard** showing Total Sales (77M+), Total Profit, and Quantity Sold.

## 🚀 Deliverables
- SQL Script for Data Cleaning (`SQLQuery2.sql`).
- Excel Dashboard with Slicers and KPIs (`Book1.xlsx`).