# SQL Server Data Warehouse: CRM + ERP

A data warehouse built with **SQL Server** following the **Medallion** architecture (Bronze → Silver → Gold), using six CSV files from two source systems: a CRM and an ERP.

> Project based on the educational project by [Data With Baraa](https://github.com/DataWithBaraa/sql-data-warehouse-project) (MIT license).

## 🎯 Objective

Consolidate sales data from two sources into a clean, integrated model that is ready for analysis.

## 🏗️ Architecture


- **Bronze**: raw data loaded from the CSV files (`BULK INSERT`).
- **Silver**: cleaned and standardized data.
- **Gold**: star schema (`fact_sales`, `dim_customers`, `dim_products`).



## 🧹 Main Transformations (Silver)

- Duplicate removal (one record per customer)
- Label normalization (gender, marital status, country, product line)
- Correction of inconsistent dates and amounts
- Handling of missing values (`n/a`, `0`, `NULL`)



## ▶️ Execution

```sql
EXEC bronze.load_bronze;
EXEC silver.load_silver;
```

## 🛠️ Tools

SQL Server · SSMS · Git · draw.io

## 👤 Author

**Oumaima El Haouari**, [LinkedIn](https://www.linkedin.com/in/oumaima-el-haouari-57a800250/?isSelfProfile=true)
