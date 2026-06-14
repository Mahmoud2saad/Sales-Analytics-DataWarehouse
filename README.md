## 🏨 Sales Analytics Data Warehouse & Business Intelligence Solution

An end-to-end Business Intelligence (BI) and Data Warehousing project that transforms transactional sales data into actionable business insights. The solution leverages Microsoft BI technologies to build a scalable data warehouse, automate ETL processes, create a multidimensional analytical model, and deliver interactive dashboards for decision-making.

---

## 📖 Project Overview

This project demonstrates the complete lifecycle of a modern BI solution:

* Extracting data from operational source systems
* Transforming and cleansing data through ETL pipelines
* Loading data into a Star Schema Data Warehouse
* Building an OLAP cube using SSAS
* Creating interactive Power BI dashboards for business analysis

The architecture follows industry-standard Data Warehousing practices, including Slowly Changing Dimensions (SCD), Incremental Loading, and Multidimensional Modeling.

---

## 🛠️ Technologies & Tools

| Technology                             | Purpose                                        |
| -------------------------------------- | ---------------------------------------------- |
| SQL Server                             | Data storage and Data Warehouse implementation |
| SSIS (SQL Server Integration Services) | ETL development and automation                 |
| SSAS (SQL Server Analysis Services)    | OLAP Cube and analytical model                 |
| Power BI                               | Data visualization and reporting               |
| T-SQL                                  | Data transformation and warehouse scripting    |

---

## 🏗️ Data Warehouse Architecture

### Star Schema Design

#### Fact Table

**Fact_Sales**

Business Measures:

* Extended Sales
* Extended Cost
* Tax Amount
* Freight
* Quantity Sold
* Profit

Foreign Keys:

* Order Date Key
* Product Key
* Customer Key
* Territory Key

#### Dimension Tables

* Dim_Date
* Dim_Product
* Dim_Customer
* Dim_Territory

---

## 🔄 Slowly Changing Dimensions (SCD)

### Dim_Product

**Type 1 Attributes**

* Color
* Model Name
* Product Category
* Product Subcategory
* Standard Cost

**Type 2 Attributes**

* Reorder Point

### Dim_Customer

**Type 1 Attributes**

* Customer Name
* Address 1
* Address 2
* City

**Type 2 Attributes**

* Phone Number

### Historical Tracking Columns

Implemented across all dimensions (except Dim_Date):

* Start Date
* End Date
* Is Current Flag
* Source System Code

---

## ⚙️ ETL Implementation (SSIS)

### Key Features

✅ Data Extraction from source systems

✅ Data Cleansing and Transformation

✅ Lookup Transformations for surrogate key generation

✅ Derived Columns for business rules implementation

✅ Slowly Changing Dimension processing

✅ Incremental Loading using Control Tables

✅ Dynamic Date Dimension generation

### Incremental Load Strategy

A control table stores the latest successful load date (`Last_Load_Date`) to ensure that only new or modified records are processed during subsequent executions.

---

## 📊 SSAS Multidimensional Cube

An OLAP cube was built on top of the Data Warehouse to provide high-performance analytical querying.

### Measures

* Total Sales
* Total Cost
* Profit
* Tax Amount
* Freight
* Quantity Sold

### Analysis Dimensions

* Time
* Product
* Customer
* Territory

The cube enables drill-down and slice-and-dice analysis across multiple business perspectives.

---

## 📈 Power BI Dashboard

Interactive dashboards were developed to answer key business questions and support strategic decision-making.

### Business Insights Delivered

1. Sales trends over time
2. Revenue performance by product
3. Top customers by sales value
4. Product profitability analysis
5. Customer purchasing behavior
6. Most profitable products
7. Quarterly sales performance
8. Weekend and holiday sales impact
9. Top-selling products by quantity
10. Peak sales periods and seasonality

### KPI Metrics

* Total Revenue
* Total Cost
* Total Profit
* Total Tax
* Total Freight
* Total Quantity Sold

---

## 📂 Repository Structure

```text
Sales-Analytics-DWH-Project/
│
├── SSIS-Packages/
├── SQL-Scripts/
├── SSAS-Cube/
├── PowerBI-Report/
├── Images/
└── README.md
```

---

## 🎯 Key Data Engineering & BI Concepts Demonstrated

* Data Warehousing
* Star Schema Modeling
* ETL Development
* Incremental Data Loading
* Slowly Changing Dimensions (Type 1 & Type 2)
* OLAP Cubes
* Business Intelligence Reporting
* Data Visualization
* Performance Optimization

---

## 📬 Contact

**Mahmoud Saad**

Junior Data Engineer | Data Scientist | Kaggle Expert

LinkedIn:
https://www.linkedin.com/in/mahmoud-saad0/

Email:
[mahmoud_165797@fci.sohag.edu.eg](mailto:mahmoud_165797@fci.sohag.edu.eg)
