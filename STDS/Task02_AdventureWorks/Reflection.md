# 💭 Reflection - Adventure Works Project

## 💡 What I Learned
- **Advanced SQL Techniques:** I learned how to use **Dynamic SQL** and `sp_executesql` to loop through columns and check for NULLs automatically, instead of checking each column manually.
- **Data Integrity:** Understanding the importance of Foreign Keys when joining tables (SalesPerson, Region, Targets) to avoid data loss.
- **KPI Calculation:** How to calculate complex metrics like "Profit Margin" within Pivot Tables using Calculated Fields.

## 🚧 What Was Challenging
- **Handling Nulls & Duplicates:** Writing the SQL logic to identify duplicates without deleting important records was tricky.
- **Data Consistency:** Dealing with inconsistent categorical data (e.g., standardizing color names) before moving the data to Excel.
- **Model Relationships:** Ensuring the "Sales" table correctly mapped to "Resellers" and "Regions" to get accurate summaries in the Dashboard.

## 📈 Improvements
- **Automated Cleaning:** Unlike previous tasks where I cleaned data manually in Excel, I used **SQL Scripts** this time. This makes the process repeatable and much faster for larger datasets.
- **Dashboard Layout:** I improved the visual hierarchy of my Excel Dashboard, placing key numbers (KPIs) at the top for immediate impact.
