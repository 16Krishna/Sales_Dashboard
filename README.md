# Sales_Dashboard
Sales Insights Dashboard – Business Insights Report using Microsoft Fabric


# 📊 Sales Analytics — Microsoft Fabric End-to-End Project

An end-to-end **Sales Analytics solution built using Microsoft Fabric**, covering data ingestion, transformation, Medallion Architecture, data warehousing, dimensional modeling, semantic modeling, and Power BI reporting.

The project demonstrates how raw sales data can be transformed into a business-ready Power BI dashboard using Microsoft Fabric.

---

## 🏗️ Project Architecture

<img width="1939" height="811" alt="Sales_Data_Architecture" src="https://github.com/user-attachments/assets/85306783-84c9-4365-8729-8a033ffa06f0" />


### End-to-End Flow

CSV Sales Data
↓
Microsoft Fabric Pipeline
↓
Lakehouse
↓
Medallion Architecture(Bronze → Silver → Gold) 
↓
Fabric Warehouse
↓
Star Schema
↓
Power BI Semantic Model
↓
Power BI Sales Dashboard

---

## 🎯 Business Objective

The objective of this project is to build a centralized sales analytics solution that enables business users to analyze:

- Sales revenue
- Sales quantity
- Order volume
- Revenue trends
- Product/category performance
- Regional performance
- Customer performance
- Average revenue/order
- Average quantity/order

The final output is an interactive Power BI dashboard that allows stakeholders to explore sales performance using filters and visualizations.

---

# 🛠️ Technologies Used

Microsoft Fabric
OneLake & Lakehouse
Data Pipelines
Medallion Architecture
PySpark / Notebooks
Fabric Warehouse
SQL
Star Schema & Data Modeling
Power BI & DAX
Semantic Models
Data Analysis & Visualization
KPI & Business Insights
Sales & Trend Analysis

---

# 📥 1. Data Source
The project starts with a sales dataset in CSV format.

The dataset contains information related to:

- Orders
- Customers
- Products
- Product Categories
- Regions
- Dates
- Revenue
- Quantity

The CSV file is ingested into Microsoft Fabric using a Fabric Data Pipeline.

---

# 🔄 2. Data Pipeline

### Pipeline Flow


Copy Raw Sales Data
        ↓
Copy Data to Delta
        ↓
Bronze → Silver Transformation
        ↓
Build Gold Layer
        ↓
Transform / Prepare Warehouse Data
        ↓
Load Dimension Tables
        ↓
Load Fact_Sales
        ↓
Create Star Schema
        ↓
Create Power BI Semantic Model
        ↓
Build Power BI Dashboard

## ⭐ 3. Data Model — Star Schema

The sales data is organized using a Star Schema to make the data easier to analyze and maintain.

### Fact Table

**Fact_Sales** contains the transactional sales data:

- Order ID
- Order Date Key
- Customer Key
- Product Key
- Region Key
- Revenue
- Quantity

### Dimension Tables

The fact table is connected to four dimension tables:

- **Dim_Date** — Date, Year, Month, Quarter
- **Dim_Customer** — Customer information
- **Dim_Product** — Product and category information
- **Dim_Region** — Regional information

<img width="1912" height="815" alt="Star_Schema" src="https://github.com/user-attachments/assets/738203ee-8366-4f64-9235-b1c007f398af" />

---

## 📊 4. Dashboard Overview

The Power BI dashboard was developed and published in Microsoft Fabric to provide an interactive view of overall sales performance.

### Key KPIs

- **Total Revenue:** ₹13.64M
- **Total Quantity:** 10K
- **Total Orders:** 1,250
- **Average Quantity per Order:** 8.03

### Analysis Areas

The dashboard focuses on:

- Monthly revenue and order trends
- Revenue by region
- Revenue by product category
- Quantity by product category
- Orders by region
- Top customers by revenue

<img width="1915" height="862" alt="Sales" src="https://github.com/user-attachments/assets/1a7a3e4a-c819-4527-8be9-45d79366f327" />

---

## 🔍 5. Key Findings

Based on the dashboard:

- **Electronics generates the highest revenue** among the product categories.
- **North and West regions** generate the highest revenue.
- **Office Supplies has the highest quantity contribution**, despite generating significantly less revenue than Electronics.
- The dashboard highlights a group of **top customers contributing significantly to overall revenue**.
- Monthly revenue and order volumes vary across the year, indicating changes in sales performance over time.

---

## 🎯 6. Business Recommendations

Based on these findings, the business should focus on:

### Product Performance
Electronics could receive greater focus, as it generates the highest revenue.

### Regional Performance
North and West could continue to receive attention, as they contribute the highest revenue.

### Product Mix
Office Supplies has high sales quantity but relatively lower revenue, suggesting an opportunity to review pricing, margins, and product mix.

### Customer Concentration
Greater focus on high-value customers could help support customer retention and repeat purchases.

### Sales Trends
Monthly revenue and order trends can be used to identify growth periods, declines, and potential seasonal patterns.

---
