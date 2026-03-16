# Data Warehouse and Analytics Project

Welcome to the **Data Warehouse and Analytics Project** repository!

This project demonstrates an end-to-end **Data Warehouse and Analytics solution**, starting from data ingestion and transformation to generating analytical insights.

The project is designed as a **portfolio project** to showcase practical skills in **Data Engineering, Data Modeling, and SQL Analytics**, following industry best practices.
---

## 📑 Table of Contents
- [Tech Stack](#-tech-stack)
- [Project Requirements](#project-requirements)
- [Data Warehouse Workflow](#-data-warehouse-workflow)
- [Data Architecture](#-data-architecture)
- [Data Integration](#-data-integration)
- [Data Model](#-data-model-sales-data-mart)
- [Data Flow](#-data-flow)
- [ETL Pipeline](#-etl-pipeline)
- [Repository Structure](#-repository-structure)
- [License](#license)
- [About Me](#-about-me)



## 🛠️ Tech Stack
- **SQL Server** – Data Warehouse implementation
- **SQL** – Data transformation and analytics
- **Draw.io** – Architecture and data modeling diagrams
- **CSV Files** – Source data format
- **Git & GitHub** – Version control and project collaboration
-------
# Project Requirements

## 1. Building the Data Warehouse (Data Engineering)

### Objective
Develop a modern **Data Warehouse** using **SQL Server** to consolidate sales data from multiple source systems and enable efficient analytical reporting and data-driven decision-making.

### Specifications

#### Data Sources
Import data from two source systems:

- **ERP System**
- **CRM System**

The data is provided as **CSV files**.

#### Data Quality
Perform data cleaning and resolve common data quality issues such as:

- Missing values
- Duplicate records
- Data format inconsistencies

#### Data Integration
Integrate data from both systems into a **single analytical data model** that is optimized for analytical queries and reporting.

#### Scope
The project focuses only on the **latest available dataset**.

Historical tracking (**historization**) is **not required** in this project.

#### Documentation
Provide clear documentation of the **data model**, including:

- Table descriptions
- Column definitions
- Relationships between tables

This documentation supports both:

- Business stakeholders
- Analytics teams

---
### BI: Analytics & Reporting (Data Analysis)

#### Objective
Develop SQL-based analytics to deliver detailed insights into:
- **Customer Behavior**
- **Product Performance**
- **Sales Trends**

These insights empower stakeholders with key business metrics, enabling strategic decision-making.  

For more details, refer to [docs/requirements.md](docs/requirements.md).

-----
## ⚙️ Data Warehouse Workflow

The project follows a layered **Medallion Architecture** approach:
1. **Bronze Layer** – Raw data ingestion from CSV files
2. **Silver Layer** – Data cleaning, transformation, and standardization
3. **Gold Layer** – Analytical data model using Star Schema
## 🏗️ Data Architecture

![Data Architecture](docs/data_architecture.png)

The data architecture for this project follows the **Medallion Architecture**, which organizes data into three layers: **Bronze, Silver, and Gold**.

### 🥉 Bronze Layer (Raw Data Layer)
The Bronze layer stores raw data exactly as it is received from the source systems.  
In this project, data is ingested from **CSV files** and loaded directly into a **SQL Server database** without transformations.  
This layer acts as the historical record of the source data.

### 🥈 Silver Layer (Cleaned and Standardized Data)
The Silver layer is responsible for data cleansing, transformation, and normalization.  
In this stage, inconsistencies, missing values, and formatting issues are resolved.  
The data is standardized and structured to ensure accuracy and consistency for downstream processes.

### 🥇 Gold Layer (Business-Ready Data)
The Gold layer contains curated, business-ready datasets optimized for analytics and reporting.  
Data in this layer is modeled using a **Star Schema**, making it suitable for business intelligence tools and analytical queries.

------
## 🔗 Data Integration

![Data Integration](docs/data_integration.png)

This diagram illustrates how data from the **CRM** and **ERP** systems is integrated.

The CRM system provides transactional sales data, customer information, and product details, while the ERP system provides additional product categories, customer attributes, and location data.

These datasets are joined using common keys such as **product identifiers** and **customer identifiers** to create a unified data foundation for downstream analytics.
-----
## ⭐ Data Model (Sales Data Mart)

![Data Model](docs/data_model.png)

The Gold layer contains the **Sales Data Mart**, modeled using a **Star Schema** to support analytical queries.

The central **fact_sales** table stores transactional sales data, including order information, sales amount, quantity, and price.

Two dimension tables provide descriptive context:

- **dim_customers** – Contains customer attributes such as name, country, gender, and birthdate.
- **dim_products** – Contains product details including category, subcategory, product line, and cost.

This design improves query performance and simplifies reporting and business intelligence analysis.
----
## 🔄 Data Flow

![Data Flow](docs/data_flow.png)

This diagram shows the overall data flow within the data warehouse architecture.

Data is first ingested from the **CRM** and **ERP** source systems into the **Bronze Layer**, where raw data is stored.

The data is then cleaned, standardized, and transformed in the **Silver Layer**.

Finally, curated datasets are created in the **Gold Layer**, where the data is modeled into a **star schema** to support analytics and reporting.

## ⚙️ ETL Pipeline

![ETL Pipeline](docs/ETL.png)

This diagram illustrates the **ETL (Extract, Transform, Load) pipeline** used to process data from operational systems into the analytical warehouse.

- **Extract** – Data is extracted from the source systems (**CRM** and **ERP**) in the form of CSV files.

- **Transform** – Data is cleaned, standardized, and transformed through multiple processing stages to ensure consistency and quality.

- **Load** – The transformed data is loaded into the **SQL Server Data Warehouse**, following the **Bronze, Silver, and Gold** layered architecture.

This pipeline ensures that raw operational data is converted into structured, high-quality datasets ready for analytical queries and business intelligence.

## 📂 Repository Structure
```
data-warehouse-project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── etl.drawio                      # shows ETL techniques and pipeline design
│   ├── data_architecture.drawio        # Draw.io file shows the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow.drawio                # Draw.io file for the data flow diagram
│   ├── data_models.drawio              # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
├── .gitignore                          # Files and directories to be ignored by Git
└── requirements.txt                    # Dependencies and requirements for the project
```
---

# License

This project is licensed under the **MIT License**.

You are free to:

- Use
- Modify
- Share
------

# 🌟 About Me

Hi, I'm **Bahgat Zakaria** 👋

I am a **Data Engineering enthusiast** with a strong interest in building **Data Warehouses** and **ETL pipelines**.

I enjoy working with data, transforming **raw datasets** into **structured and meaningful insights**.

🎯 **My Goal**  
My goal is to become a **professional Data Engineer** and build **scalable, reliable data platforms** that support data-driven decision making.

## 🔗 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amir-zakaria-70a03a295?utm_source=share_via&utm_content=profile&utm_medium=member_android)


