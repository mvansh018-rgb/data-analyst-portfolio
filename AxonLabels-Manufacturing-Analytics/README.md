## 📌 Objective
To design an interactive dashboard to track production performance, analyze rejection rates, and improve operational efficiency through data-driven insights.

---

## 💼 Business Problem
The manufacturing business required a centralized dashboard to monitor production, rejection rates, and operational efficiency. Lack of visibility into machine-level and employee-level performance made it difficult to identify inefficiencies and control wastage.

---

## 📂 Dataset
Pre-cleaned manufacturing dataset containing production, sales, cost, and operational performance data.

---

## 🛠 Tools Used
- Excel  
- Tableau
- SQL
- Power BI

---

## 📌 Key Metrics (KPIs)
- Produced Quantity  
- Manufactured Quantity  
- Rejected Quantity  
- Wastage Percentage  
- Employee Performance  
- Machine-wise Production  
  
---

## 🔄 Project Workflow
- Analyzed business requirements related to production and quality metrics  
- Designed dashboards using Excel, Power BI and Tableau
- Performed data analysis using SQL to extract insights
- Visualized production, rejection, and efficiency metrics  
- Derived insights to identify inefficiencies and improvement areas  

---

## SQL Analysis

SQL was used toSQL was used to extract insights from the AdventureWorks dataset by performing aggregations, joins, and filtering operations.

1. Total Manufactured Quantity-
   SELECT CONCAT(ROUND(SUM(todayManufacturedqty)/1000000,2), 'M') AS TotalManufacturedqty
   FROM MannufacturedData;

 2. Total Wastage %-
    SELECT CONCAT(ROUND(SUM(RejectedQty) * 100.0/ SUM(todayManufacturedqty), 2), '%') AS TotalWastage%
    FROM ManufacturedData;
    
 3. Employee Wise Rejected Quantity-
    Select EmpName, Concat(Round(Sum(RejectedQty)/1000, 2), 'K') AS TotalRejectedQty
    FROM ManufacturedData
    GROUP BY EmpName
    ORDER BY SUM(RejectedQty) DESC;

---    

## 📊 Dashboard & Visualization
- Developed dashboards using Excel, Power BI and Tableau to monitor key manufacturing and sales metrics  
- Designed user-friendly visuals for tracking performance and trends  

### 🔗 Live Dashboard
- Tableau Dashboard: https://public.tableau.com/app/profile/vansh.mittal8700/viz/AxonLabelManufacturinganalysisDashboard/Dashboard1
- Power Bi Dashboard: https://app.powerbi.com/groups/me/reports/2ffa9bee-27c3-48f3-bff4-4455c0eaa5cb/6eacd8633011e1bf3d23?experience=power-bi

---

## 📊 Key Insights
- Total production reached 60M units, with a relatively low wastage rate of 0.82%, indicating efficient manufacturing operations  
- Department-wise analysis shows consistent manufacturing output, but rejection levels vary across departments  
- Machine MC027 recorded the highest rejected quantity, highlighting a potential area for process improvement  
- Employee-level analysis indicates that certain operators contributed more to rejected quantities, suggesting training opportunities  
- Monthly production trends remained stable throughout the year, with slight fluctuations indicating operational consistency
  
---

## 💼 Business Impact
- Identified high-rejection machines to improve operational efficiency  
- Enabled monitoring of employee-level performance for quality control  
- Improved visibility into production and wastage metrics  
- Supported data-driven decisions to reduce rejection rates and optimize processes  

---

## 📸 Dashboard Preview

### Excel Dashboard
<img width="1081" height="618" alt="Excel-Dashboard" src="https://github.com/user-attachments/assets/3bb8c885-e111-40a2-90d3-e3e417679fb3" />

### Tableau Dashboard
<img width="1185" height="836" alt="Tableau" src="https://github.com/user-attachments/assets/20904ec3-af0b-4628-9c04-7abfa4a211b2" />

### Power BI Dashboard
<img width="1286" height="720" alt="Powerbi" src="https://github.com/user-attachments/assets/abd946b5-8a7a-4df1-a388-9171d724f843" />



