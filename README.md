# 📊 E-Commerce Customer & Sales Analytics

![Excel](https://img.shields.io/badge/Excel-Analysis-green?logo=microsoft-excel&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Analytics-blue?logo=mysql&logoColor=white)
![Power%20BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)
![Portfolio](https://img.shields.io/badge/Portfolio-Project-purple)

An end-to-end **data analytics portfolio project** analyzing transactional e-commerce data from a UK-based online retailer.  
This project demonstrates a complete analytics workflow using **Excel for data cleaning and exploratory analysis**, **MySQL for business querying and customer segmentation**, and **Power BI for dashboard development**.

The dataset contains **~541,000 raw transaction rows** covering **December 2010 to December 2011** across **38 countries**. After cleaning, the final analysis dataset contains **397,884 rows**.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Objective](#-business-objective)
- [Dataset Information](#-dataset-information)
- [Tools & Skills Used](#-tools--skills-used)
- [Project Structure](#-project-structure)
- [Phase 1: Data Cleaning in Excel](#-phase-1-data-cleaning-in-excel)
- [Phase 2: Excel Analysis](#-phase-2-excel-analysis)
- [Phase 3: SQL Analysis in MySQL](#-phase-3-sql-analysis-in-mysql)
- [Phase 4: Power BI Dashboard](#-phase-4-power-bi-dashboard)
- [Key Insights](#-key-insights)
- [Screenshots](#-screenshots)
- [What I Learned](#-what-i-learned)
- [How to Reproduce](#-how-to-reproduce)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 🎯 Project Overview

**Project Name:** E-Commerce Customer & Sales Analytics  
**Dataset:** [Online Retail Dataset (Kaggle)](https://www.kaggle.com/datasets/vijayuv/onlineretail)  
**Source Type:** Real-world transactional retail data  
**Tools Used:** Microsoft Excel (Mac), MySQL Workbench, Power BI Web Service  
**Project Type:** Portfolio project for recruiter evaluation  

This project was built to demonstrate practical data analytics skills across the full workflow:

- cleaning raw transactional data
- preparing analysis-ready datasets
- performing business analysis in Excel
- writing SQL queries for KPI reporting and segmentation
- creating customer segmentation models
- building an interactive dashboard in Power BI

---

## 💼 Business Objective

The goal of this project was to analyze customer behavior, product performance, sales trends, and revenue concentration in an e-commerce business.

Key questions explored include:

- Which countries generate the most revenue?
- Which products and customers drive the highest sales?
- How does revenue change month to month?
- What customer segments contribute the most value?
- Which customers are champions, loyal, at-risk, or lost based on RFM analysis?
- How can the data be visualized for business decision-making?

---

## 🗂 Dataset Information

The dataset contains invoice-level transactions for a UK-based online retail company between **December 2010 and December 2011**.

### Raw Dataset
- **Rows:** ~541,000
- **Coverage:** 13 months / 38 countries
- **Granularity:** Transaction line level
- **Fields included:** Invoice number, stock code, description, quantity, invoice date, unit price, customer ID, country

### Cleaned Dataset
- **Rows:** 397,884
- **Columns:** 13
- **Country coverage:** ~37–38 countries
- **Unique customers:** 4,362
- **Approx. unique products:** ~3,600
- **Approx. total revenue:** €8.3M+

### Data Cleaning Summary
The following issues were addressed before analysis:

- Removed rows with blank `CustomerID`
- Removed negative and zero quantities
- Removed zero `UnitPrice` rows
- Converted `UnitPrice` from text to numeric
- Standardized mixed `InvoiceDate` values into real date format
- Removed blank/error rows
- Converted formulas to values for workbook stability

### Final Analytical Columns
- Invoice
- StockCode
- Description
- Qty
- InvoiceDate
- Unit Price
- Customer ID
- Country
- Revenue
- Year
- Month
- YearMonth
- DayOfWeek

---

## 🛠 Tools & Skills Used

### Tools
- **Microsoft Excel (Mac)**
- **MySQL / MySQL Workbench**
- **Power BI Web Service**
- **Kaggle / UCI dataset**

### Excel Skills
- Data cleaning
- Data type correction
- Pivot tables
- Charts
- Lookup logic
- Customer segmentation
- Target vs actual analysis

### SQL Skills
- Aggregations (`COUNT`, `SUM`, `AVG`)
- Filtering (`WHERE`, `NOT IN`)
- Sorting and grouping (`GROUP BY`, `ORDER BY`)
- Conditional logic (`CASE WHEN`)
- Joins (`INNER JOIN`, `LEFT JOIN`, self-join)
- Subqueries and correlated subqueries
- CTEs
- Window functions
- RFM segmentation
- Table creation and data import

### Power BI Skills
- Data modeling
- Power Query cleaning
- Relationship setup
- DAX measures
- KPI dashboard design
- Interactive filtering and drill-down

---

## 📁 Project Structure

```bash
ecommerce-customer-sales-analytics/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── online_retail_raw.xlsx
│   └── processed/
│       └── ecommerce_cleaned_data.xlsx
│
├── excel/
│   ├── ecommerce_analysis_workbook.xlsx
│   ├── pivot_tables/
│   └── screenshots/
│
├── sql/
│   ├── 01_data_import.sql
│   ├── 02_kpi_summary.sql
│   ├── 03_top10_analysis.sql
│   ├── 04_time_trends.sql
│   ├── 05_customer_segments.sql
│   ├── 06_cte_analysis.sql
│   ├── 07_window_functions.sql
│   ├── 08_rfm_analysis.sql
│   └── schema_notes.md
│
├── powerbi/
│   ├── dashboard_notes.md
│   ├── dax_measures.md
│   ├── screenshots/
│   └── ecommerce_dashboard.pbix   # if available later
│
├── docs/
│   ├── data_cleaning_summary.md
│   ├── business_insights.md
│   ├── methodology.md
│   └── portfolio_case_study.md
│
└── assets/
    ├── images/
    │   ├── excel_monthly_revenue.png
    │   ├── excel_top_countries.png
    │   ├── excel_top_products.png
    │   ├── excel_customer_lookup.png
    │   ├── sql_results_preview.png
    │   └── powerbi_dashboard_preview.png
    └── icons/
