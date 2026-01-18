# 🛍️ Customer Shopping Behavior Analysis

This project is an end-to-end data analysis pipeline that explores customer shopping trends, analyzing data from ingestion to visualization. The workflow involves data cleaning and feature engineering using **Python (Pandas)**, storing and querying data in **MS SQL Server**, and creating an interactive dashboard in **Power BI**.

## 🚀 Project Overview

The goal of this project is to understand purchasing behaviors, shipping preferences, and customer segmentation to drive better business decisions.

**Key Workflow:**
1.  **Data Cleaning (Python):** Processed raw CSV data, handled missing values, and engineered new features.
2.  **Database Management (SQL Server):** Loaded cleaned data into a relational database for structured querying.
3.  **Exploratory Data Analysis (SQL):** Executed complex queries to extract key insights.
4.  **Visualization (Power BI):** Built a dynamic dashboard to visualize trends and KPIs.

## 🛠️ Technologies Used

* **Programming Language:** Python 3.x
* **Libraries:** Pandas, SQLAlchemy, PyODBC
* **Database:** Microsoft SQL Server (Express)
* **Visualization:** Microsoft Power BI
* **IDE:** Jupyter Notebook / VS Code

## 📊 Data Processing (ETL)

The raw data (`customer_shopping_behavior.csv`) was processed using Pandas. Key transformation steps included:

* **Handling Null Values:** Imputed missing `Review Rating` values using the median rating of their respective categories.
* **Standardization:** Renamed columns to snake_case (e.g., `purchase_amount_(usd)` -> `purchase_amount`) for database compatibility.
* **Feature Engineering:**
    * `age_group`: Segmented customers into *Young Adult, Adult, Middle-Aged,* and *Senior* using quartile binning (`pd.qcut`).
    * `purchase_frequency_days`: Mapped categorical frequency text (e.g., "Fortnightly") to numeric day values (e.g., 14).
* **Data Validation:** Verified consistency between `discount_applied` and `promo_code_used`, removing redundant columns.

## 💾 PowerBI-Dashboard
<img width="1380" height="757" alt="image" src="https://github.com/user-attachments/assets/724e6e71-279a-4e6a-a684-2a142a29de7d" />

