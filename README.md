# Retail Analytics Project

This repository contains a complete end-to-end retail analytics project including:
- Synthetic dataset (Sales, Products, Customers, Stores)
- Data cleaning scripts (Python)
- Exploratory analysis (notebook + scripts)
- SQL scripts for common analytics queries
- SQLite database with loaded data
- Sample plots and dashboard placeholders

## Structure
```
Retail-Analytics-Project/
  data_sales_raw.csv
  data_sales_cleaned.csv
  data_products_cleaned.csv
  data_customers_cleaned.csv
  data_stores_cleaned.csv
  retail_analytics.db
  EDA_notebook.ipynb
  sql/
  python/
  reports/
  README.md
  requirements.txt
```

## How to run
1. Clone the repo.
2. Install dependencies: `pip install -r requirements.txt`
3. Run cleaning script: `python python/data_cleaning.py`
4. Open `EDA_notebook.ipynb` for exploration or run `python python/eda.py`

## Power BI
- Connect Power BI Desktop to the `retail_analytics.db` SQLite file or use the cleaned CSVs in the `data_*.csv` files.
- Build pages: Sales Overview, Customer Insights, Store Performance.
- Add KPIs: Total Sales, Total Orders, Profit, AOV, YoY Growth.
- Use SQL folder for pre-written queries to transform or aggregate data prior to visuals.

## Files created by script (generated on 2025-12-08 09:48:50 UTC)
- data_sales_raw.csv (synthetic)
- data_sales_cleaned.csv
- data_products_cleaned.csv
- data_customers_cleaned.csv
- data_stores_cleaned.csv
- retail_analytics.db (SQLite)
- SQL query scripts in /sql
- Python scripts in /python
- EDA_notebook.ipynb

## License
Feel free to use and modify this project for your portfolio. Attribution to the generator is optional.