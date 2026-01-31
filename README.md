# Vendor Performance Analysis using Python, SQL, and Power BI

## Project Overview

This project demonstrates an end-to-end **industry-standard data analytics workflow** involving:

- SQL for data extraction and aggregation
- Python for data cleaning, feature engineering, EDA, statistics, and hypothesis testing
- Power BI for dashboard development and business reporting

The objective of this project is to analyze **vendor and brand performance** to help the business make data-driven decisions related to:

- Pricing strategy
- Vendor dependency
- Inventory management
- Bulk purchasing strategy
- Promotion of low-selling but high-margin brands

This project simulates how real-world data analysts work in companies by transforming large raw transactional data into a **clean, optimized analytical dataset** and then building insights and dashboards on top of it.

---

## Business Problem

The company deals with thousands of products and hundreds of vendors. The raw data is spread across multiple large tables (sales, purchases, inventory), making analysis slow and inefficient.

The key challenges were:

- Heavy joins on very large tables (10M+ records)
- Slow performance when running repeated queries
- Difficulty in performing analysis directly on raw transactional data
- Lack of a summarized dataset for reporting and dashboarding

---

## Solution Approach

### Step 1: SQL Performance Optimization

Instead of running heavy joins repeatedly on large tables:

- Created **Sales Summary**
- Created **Purchase Summary**
- Joined them into a single **Vendor Sales Summary** table
- Reduced data from **10M+ records to ~10,000 meaningful records**

This aggregated table was saved back into the database for reuse in dashboards and analysis.

---

### Step 2: Data Cleaning and Feature Engineering (Python)

Performed data cleaning and resolved inconsistencies:

- Removed missing values
- Fixed incorrect data types
- Removed white spaces in vendor names
- Converted volume to float
- Removed inconsistent records (zero sales, negative profit, etc.)

Created new analytical features:

- Gross Profit
- Profit Margin (%)
- Stock Turnover
- Sales to Purchase Ratio
- Unsold Inventory Value

---

### Step 3: Exploratory Data Analysis (EDA)

Analyzed:

- Distribution of numerical variables (Histograms, Boxplots)
- Outliers and their business meaning (premium brands, bulk purchases)
- Correlation heatmap between variables
- Vendor and brand frequency distribution

---

### Step 4: Business Research Questions Answered

The project answers critical business questions such as:

1. Which brands have **low sales but high profit margin** (require promotion)?
2. Which vendors and brands generate **highest sales**?
3. Which vendors contribute the most to **total purchases**?
4. How dependent is procurement on **top vendors**?
5. Does **bulk purchasing reduce unit cost**?
6. Which vendors have **low inventory turnover**?
7. How much capital is locked in **unsold inventory**?
8. Is there a **statistically significant difference** between profit margins of top and low performing vendors?

---

### Step 5: Statistical Validation

Applied:

- Confidence Interval (95%)
- T-test Hypothesis Testing

To validate that low-performing vendors have **significantly higher profit margins** compared to top-performing vendors.

---

### Step 6: Power BI Dashboard

Built an interactive dashboard using the final cleaned dataset.

#### Dashboard KPIs

- Total Sales
- Total Purchases
- Gross Profit
- Profit Margin
- Unsold Capital

#### Visualizations Included

- Top Vendors by Sales
- Top Brands by Sales
- Purchase Contribution (Donut + Cumulative Chart)
- Low Performing Vendors (Funnel Chart)
- Low Performing Brands (Scatter Plot)

---

## Power BI Report Link

[View Published Power BI Dashboard](https://app.powerbi.com/groups/me/reports/2975f83b-7098-40bf-ac7e-3b07ff0b26c9/bf6f9b19a93187348302?experience=power-bi)

---

## Key Insights

- Only **10 vendors contribute ~66%** of total purchases (high vendor dependency)
- Bulk purchasing reduces unit cost by **~72%**
- **$2.7 Million** capital is locked in unsold inventory
- 198 brands identified with **low sales but high margins** (promotion opportunity)
- Low-performing vendors have significantly **higher profit margins**
- Several vendors show **very low stock turnover**, indicating overstocking

---

## Tech Stack Used

| Tool | Purpose |
|-----|--------|
| SQL | Data aggregation and performance optimization |
| Python (Pandas, NumPy, Seaborn, Matplotlib, SciPy) | Cleaning, EDA, Feature Engineering, Statistics |
| SQLite | Database storage |
| Power BI | Dashboard and reporting |

---

## Project Workflow

1. Extract large data using SQL
2. Create summarized vendor-level table
3. Clean and engineer features using Python
4. Perform EDA and statistical analysis
5. Answer business research questions
6. Build professional Power BI dashboard
7. Prepare final business report with recommendations

---

## Files in This Repository

- `Vendor_Performance_Analysis.ipynb` – Full Python analysis notebook
- `get_vendor_summary.py` – Automated script for table creation and cleaning
- `inventory.db` – Database containing final vendor summary table
- `PowerBI_Dashboard.pbix` – Power BI dashboard file
- `FINAL_PROJECT_VENDOR_PERFORMANCE_ANALYSIS_PROJECT.pdf` – Detailed project report

---

## Business Recommendations

- Promote low-selling high-margin brands
- Reduce dependency on top vendors
- Encourage bulk purchasing for better margins
- Optimize inventory for low turnover vendors
- Adjust pricing strategy for top-performing vendors
- Improve distribution and marketing for low-performing vendors

---

## What This Project Demonstrates

This project reflects **real company-level data analytics work**, including:

- Query optimization
- Data warehousing concept (aggregated table)
- Data cleaning at scale
- Feature engineering
- EDA and statistical testing
- Dashboard creation for stakeholders
- Business insight generation

---
##Dataset Link:
https://drive.google.com/drive/folders/1Lj2KvphmtDumwCeFKjJsX6KbH53isH5e?usp=sharing

## Author

Prashant Gautam  
B.Tech, Electronics and Communication Engineering  
IIT (ISM) Dhanbad  

Aspiring Data Analyst | Data Science Enthusiast | Business Analytics

---