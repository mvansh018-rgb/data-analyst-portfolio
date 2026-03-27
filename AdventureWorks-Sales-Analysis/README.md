## Objective

This project analyzes the AdventureWorks sales dataset to identify trends in product performance, regional sales distribution, and overall revenue growth.

The goal was to clean the dataset, perform analysis, and build interactive dashboards using Excel, Power BI, and Tableau.

---

## Business Problem 

The business wants to analyze its sales performance to better understand revenue trends, product demand, and regional sales distribution.

The objective of this analysis is to explore the AdventureWorks sales dataset and identify key insights related to sales performance, product popularity, and customer purchasing patterns.

Through data analysis and visualization, this project aims to help stakeholders make data-driven decisions by identifying trends, high-performing products, and potential areas for business improvement.

---

## 📂 Dataset
AdventureWorks sales dataset comprising structured data on sales transactions, customers, products, and regional performance.

---

## Tools Used

- Excel
- SQL
- Power BI
- Tableau

---

##  Project Workflow
- Collected and prepared data using Excel for analysis  
- Performed data analysis using SQL to extract insights  
- Built interactive dashboards using Power BI/Tableau  
- Delivered insights to support data-driven decision-making  

---

## Key Metrics(KPI'S)
Key business metrics used to evaluate sales performance and profitability:
- Total Sales
- Total Orders
- Total Products
- Total Profit
- Total Customers
- Avg Order Value
- Total Production Cost
  
---

## Dashboards & Visualization
- Developed dashboards using Excel, Power BI, and Tableau to analyze sales performance and key metrics.  

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

1. Total Sales-
   SELECT CONCAT(ROUND(SUM(SalesAmount)/1000000), ' M') AS TotalSales
   FROM factsales;

2. Total Profit-
   SELECT CONCAT(ROUND(SUM(Profit)/1000000), ' M') AS TotalProfit
   FROM factsales;

3. Sales by Year-
   SELECT d.CalendarYear,
   CONCAT(ROUND(SUM(SalesAmount)/1000), ' K') AS TotalSales
   FROM factsales f
   JOIN DimDate d
   ON f.DateKey = d.DateKey
   GROUP BY d.CalendarYear
   ORDER BY d.CalendarYear;
   
---

## Key Insights
- Quarter 4 generated the highest sales, indicating strong seasonal demand during the year-end period  
- Mountain Bikes emerged as the top-performing product category, contributing significantly to overall revenue  
- Sales showed a notable increase in 2013, reflecting business growth over time  
- Certain regions contributed a higher share of revenue, highlighting key markets for business focus  
