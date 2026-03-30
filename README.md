# USDA Production Analysis Dashboard (SQL + Power BI)

##  Project Overview

This project analyzes historical USDA production data across multiple commodities such as cheese, milk, eggs, coffee, honey, and yogurt.

The goal was to:

* Clean and transform raw datasets using SQL
* Build a structured data model
* Create an interactive Power BI dashboard
* Generate business insights using KPIs like YoY growth and CAGR

---

##  Tools & Technologies

* **MySQL Workbench** – Data cleaning & transformation
* **Power BI** – Dashboard & visualization
* **SQL** – Data modeling and preprocessing

---

## Dataset Description

The dataset contains production data by:

* Year
* State (State_ANSI)
* Commodity
* Production Value

Data was originally spread across multiple tables:

* cheese_production
* milk_production
* egg_production
* coffee_production
* honey_production
* yogurt_production

---

##  Data Cleaning & Preparation

### Key Challenges Faced

* Non-numeric values like `(NA)` and `(D)`
* Comma-separated numbers (e.g., `1,000,000`)
* Incorrect data types (TEXT instead of numeric)

---

### Cleaning Steps Performed

* Replaced `(NA)` and `(D)` with `NULL`
* Removed commas using `REPLACE()`
* Trimmed whitespace using `TRIM()`
* Converted `Value` column to `DECIMAL(15,2)`
* Ensured proper data types:

  * `Year → INT`
  * `State_ANSI → INT`
  * `Value → DECIMAL`

---

##  Data Modeling

* Created structured tables in MySQL
* Added **Primary Key (ID)**
* Optimized column types using `VARCHAR` instead of `TEXT`
* Managed the relationships btw tables in PowerBI.
* Created the Masterdata table in PowerBI by appending queries.

---

##  Power BI Dashboard Features

<img width="1292" height="729" alt="image" src="https://github.com/user-attachments/assets/06acc005-d8c4-43c8-b2fa-60bf659773e9" />



### Key KPIs

* Total Production – Aggregated production values
* Average Production – Mean production across dataset
* Year-over-Year (YoY) Growth %
* CAGR (Compound Annual Growth Rate)

---

### Visualizations

*  Line Chart → Production trends over time
*  Bar Chart → State-wise comparison
*  Map → Geographic distribution
*  Slicers → Year & Commodity filters

---

##  Key Insights

* Significant long-term growth in dairy production
* Variation across states highlights regional specialization
* YoY growth fluctuates due to seasonal and economic factors

---

##  What I Learned

* Handling real-world messy data in SQL
* Importance of correct data types in analytics
* Difference between INT, BIGINT, and DECIMAL
* Building KPI metrics (YoY, CAGR) in Power BI
* Debugging SQL errors like:

  * Error 1366 (Incorrect decimal)
  * Error 1175 (Safe update mode)
  * Out-of-range integer errors

---

##  Future Improvements

* Create a unified fact table (star schema)
* Add a Date dimension table
* Enhance dashboard UI/UX
* Automate ETL pipeline

---

##  Conclusion

This project demonstrates end-to-end data analysis:

* Raw data → Cleaning → Modeling → Visualization

It taught me practical skills required for a **Data Analyst role**, including SQL, data cleaning, and dashboarding.
