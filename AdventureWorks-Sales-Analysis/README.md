## Project Overview

This project analyzes the AdventureWorks sales dataset to identify trends in product performance, regional sales distribution, and overall revenue growth.

The goal was to clean the dataset, perform analysis, and build interactive dashboards using Excel, Power BI, and Tableau.

---

## Dataset Description

The dataset used in this project is the AdventureWorks sales dataset.  
It consists of 8 tables including fact and dimension tables.

Fact Tables:
- Sales Table 1
- Sales Table New

Dimension Tables:
- Product
- Product Subcategory
- Product Category
- Customer
- Sales Territory
- Date

These tables were combined and cleaned before performing analysis.

--

## Tools Used

- Excel
- SQL
- Power BI
- Tableau

---

## Project Workflow

1. Data Cleaning  
Cleaned raw dataset and removed inconsistencies.

2. Data Transformation  
Merged fact tables and joined product category, subcategory, and product tables.

3. Data Analysis  
Performed exploratory data analysis using Excel and SQL.

4. Dashboard Development  
Created interactive dashboards in Excel, Power BI, and Tableau.

5. Insights Generation  
Analyzed sales trends, product performance, and regional sales distribution.

--

## KPIs Used

- Total Sales
- Total Orders
- Total Products
- Total Profit
- Total Customers
- Avg Order Value
- Total Production Cost
  
---

## Dashboards Created

1. Excel Sales Dashboard
2. Power BI Interactive Dashboard
3. Tableau Visualization Dashboard

---

## Live Dashboards

🔗 Tableau Dashboard  
https://public.tableau.com/views/AdventureWorksSalesPerformanceDashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

🔗 Power BI Dashboard  
https://app.powerbi.com/links/5hsfSeKcdD?ctid=6e170c50-17f0-464b-9ac1-8683fb59a3b9&pbi_source=linkShare

---

## Dashboard Preview

### Excel Dashboard
[Excel Dashboard]<img width="1149" height="603" alt="Excel-Dashbaord" src="https://github.com/user-attachments/assets/34680e42-1d5e-48ef-a6d6-05c220bdc3d7" />

### Power BI Dashboard
[Power BI Dashboard]<img width="1189" height="681" alt="PowerBI-Dashboard" src="https://github.com/user-attachments/assets/f67c1065-6192-4c15-a4b0-6220afc01311" />

### Tableau Dashboard
[Tableau Dashboard]<img width="1402" height="688" alt="Tableau-Dashboard" src="https://github.com/user-attachments/assets/ba26ba1b-5de2-4669-8841-92600b41e187" />

---

## SQL Analysis

SQL was used to extract insights from the AdventureWorks dataset by performing aggregations, joins, and filtering operations.

1. Total Sales
   SELECT CONCAT(ROUND(SUM(SalesAmount)/1000000), ' M') AS TotalSales
   FROM factsales;

2. Total Profit
   SELECT CONCAT(ROUND(SUM(Profit)/1000000), ' M') AS TotalProfit
   FROM factsales;

3. Sales by Year
   SELECT d.CalendarYear,
   CONCAT(ROUND(SUM(SalesAmount)/1000), ' K') AS TotalSales
   FROM factsales f
   JOIN DimDate d
   ON f.DateKey = d.DateKey
   GROUP BY d.CalendarYear
   ORDER BY d.CalendarYear;

4. Top 10 Products by order quantity
   SELECT ProductKey,EnglishProductName,SUM(OrderQuantity) AS TotalOrders
   FROM factsales
   GROUP BY ProductKey, EnglishProductName
   ORDER BY TotalOrders DESC
   LIMIT 10;

5. Sales by Region
   SELECT t.SalesTerritoryRegion, t.SalesTerritoryCountry,
   CONCAT(ROUND(SUM(SalesAmount)/1000), ' K') AS TotalSales
   FROM factsales f JOIN dimsalesterritory t
   ON f.SalesTerritoryKey = t.SalesTerritoryKey
   GROUP BY t.SalesTerritoryRegion, t.SalesTerritoryCountry
   ORDER BY TotalSales DESC;
   
---

## Key Insights

- Q4 generated the highest sales.
- Mountain bike products were top-performing.
- Sales increased significantly in 2013.
- Some regions contributed more revenue than others.
