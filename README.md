# 📊 Retail Sales Analysis Project  
An end-to-end Data Analytics project using **Python, SQL, and Power BI** to analyze retail sales performance, uncover business insights, and build a complete analytics pipeline.

---

## 🏆 Project Summary  

This project simulates a real-world retail analytics scenario.  
It covers everything from **data cleaning → SQL insights → dashboards**, demonstrating the complete workflow a Data Analyst performs in an organization.

You will see:

- ✔ Python for Data Preparation  
- ✔ SQL for Analytics & Business Queries  
- ✔ Power BI for Dashboarding  
- ✔ Real business insights that support decision-making  

---

## 🧱 Project Architecture

Raw Data → Python Cleaning → SQLite Database → SQL Insights → Power BI Dashboard → Business Insights


---

## 📁 Folder Structure

Retail-Sales-Analysis-Project/
│
├── data_sales_raw.csv
├── data_sales_cleaned.csv
├── data_products_cleaned.csv
├── data_customers_cleaned.csv
├── data_stores_cleaned.csv
│
├── retail_analytics.db
│
├── python/
│ ├── data_cleaning.py
│ └── eda.py
│
├── sql/
│ ├── 01_total_sales_monthly.sql
│ ├── 02_top_products.sql
│ ├── 03_top_customers.sql
│ ├── 04_repeat_new_customers.sql
│ └── 05_sales_by_region.sql
│
├── reports/
│ ├── monthly_sales.png
│ └── top10_products.png
│
├── EDA_notebook.ipynb
└── README.md


---

## 🧹 Data Cleaning (Python)

Performed using Pandas & NumPy:

- Handling missing values  
- Standardizing product and store data  
- Extracting Year, Month, Day from dates  
- Calculating **TotalSales** & **Profit**  
- Removing duplicates  
- Preparing cleaned datasets for SQL & Power BI  

---

## 📈 Exploratory Data Analysis (EDA)

Key analyses include:

- Monthly sales trends  
- Category-wise performance  
- Region-wise revenue  
- Top-selling products  
- High-value customers  
- Repeat vs new customer patterns  

Sample visuals are included in `reports/`.

---

## 🗃️ SQL Insights  

SQL was used to generate meaningful business insights.  

### 🔹 Monthly Sales Summary  
```sql
SELECT Year, Month, SUM(TotalSales) AS MonthlySales
FROM Sales
GROUP BY Year, Month
ORDER BY Year, Month;
SELECT ProductID, SUM(TotalSales) AS Sales
FROM Sales
GROUP BY ProductID
ORDER BY Sales DESC
LIMIT 10;

SELECT Region, SUM(TotalSales)
FROM Sales
JOIN Stores ON Sales.StoreID = Stores.StoreID
GROUP BY Region;
Total Sales = SUM(Sales[TotalSales])
AOV = [Total Sales] / DISTINCTCOUNT(Sales[OrderID])
YoY Growth =
VAR PrevYear = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Sales[OrderDate]))
RETURN DIVIDE([Total Sales] - PrevYear, PrevYear)

## 🚀 How to Run This Project  

### ▶ Python Scripts  
Install dependencies and run data processing:

pip install -r requirements.txt
python python/data_cleaning.py
python python/eda.py

### ▶ SQL  
Open the SQLite database file:

retail_analytics.db

Use DB Browser for SQLite (or any SQL tool) to run queries.

### ▶ Power BI  
1. Open Power BI Desktop  
2. Load the cleaned CSV files:
   - data_sales_cleaned.csv  
   - data_products_cleaned.csv  
   - data_customers_cleaned.csv  
   - data_stores_cleaned.csv  
3. Create relationships  
4. Add DAX measures  
5. Build visual dashboards  


