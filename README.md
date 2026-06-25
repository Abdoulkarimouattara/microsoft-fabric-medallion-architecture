# 🚀 Microsoft Fabric Medallion Architecture (Online Retail Analytics)

## 📌 Overview

This project demonstrates the design and implementation of an **end-to-end analytics platform using Microsoft Fabric**.

The solution follows the **Medallion Architecture (Bronze → Silver → Gold)** to transform raw e-commerce data into trusted, business-ready datasets for reporting and decision-making.

The project showcases several core Microsoft Fabric capabilities:

- OneLake
- Lakehouse
- Dataflow Gen2
- Notebooks (PySpark)
- Semantic Models
- Power BI

---

## 📊 Dashboard Preview

This section will be updated as the project progresses.

[![Dashboard](./architecture/dashboard.png)](./architecture/dashboard.png)

---

## 🎯 Business Use Case

An online retail company wants to:

- 📊 Monitor sales performance
- 📈 Analyze revenue trends
- 📦 Identify top-selling products
- 👥 Understand customer purchasing behavior
- 🎯 Segment customers based on spending patterns

---

## 🏗️ Architecture

```
Online Retail Dataset (CSV)
            │
            ▼
     OneLake / Lakehouse
            │
            ▼
       Bronze Layer
        (Raw Data)
            │
            ▼
      Dataflow Gen2
(Data Cleaning & Enrichment)
            │
            ▼
       Silver Layer
      (Curated Data)
            │
            ▼
    Fabric Notebook
         (PySpark)
            │
            ▼
        Gold Layer
            │
            ▼
      Semantic Model
            │
            ▼
     Power BI Dashboard
```
---
## 📸 Architecture Diagram

⚙️ Technologies Used

🏢 Microsoft Fabric
OneLake

Lakehouse

Dataflow Gen2

Fabric Notebooks

Semantic Models

💻 Data Engineering
PySpark

SQL

📊 Analytics & Visualization
Power BI

---

## 📁 Repository Structure
```
project/
│
├── architecture/
│   ├── architecture.png
│   ├── bronze_layer.png
│   ├── dataflow_gen2.png
│   ├── silver_layer.png
│   ├── notebook_processing.png
│   ├── gold_layer.png
│   └── dashboard.png
│
├── data/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── notebooks/
│   └── silver_to_gold_analytics.ipynb
│
└── README.md
```
---

## 🏗️ Architecture & Pipeline Workflow

### 1️⃣ Bronze Layer – Data Ingestion

The Online Retail dataset is manually uploaded into the Fabric Lakehouse and loaded into the Bronze layer without modification.

**Objectives:**
- Preserve source data
- Ensure traceability
- Support future reprocessing

**Source:**
- Kaggle Online Retail Dataset

📸 Bronze Layer

![Bronze Layer](./architecture/bronze_layer.png)

---

### 2️⃣ Silver Layer – Data Transformation

Dataflow Gen2 is used to clean, standardize, and enrich the raw data.

**Transformations include:**
- Missing value handling
- Data type corrections
- Duplicate removal
- Column standardization
- Revenue calculations

**New features created:**
- `line_total`
- `year`
- `month`
- `is_return`

📸 Dataflow Gen2

![Dataflow Gen2](./architecture/dataflow_gen2.png)

📸 Silver Layer

![Silver Layer](./architecture/silver_layer.png)

---

### 3️⃣ Gold Layer – Business Processing

Fabric Notebooks (PySpark) are used to generate business-ready analytical datasets.

**Business Analytics:**

#### Revenue Analytics
- Total Revenue
- Revenue by Month
- Revenue by Country
- Revenue Growth Trends

#### Order Analytics
- Total Orders
- Average Order Value
- Order Volume Trends

#### Product Analytics
- Top Products by Revenue
- Top Products by Quantity Sold

#### Customer Analytics
- Top Customers by Spending
- Customer Lifetime Value
- RFM Segmentation

📸 Notebook Processing

![Notebook](./architecture/notebook_processing.png)

📸 Gold Layer

![Gold Layer](./architecture/gold_layer.png)

---

### 4️⃣ Reporting & Visualization

Power BI consumes Gold layer datasets through a Semantic Model to deliver business insights and interactive dashboards.

📸 Dashboard

![Dashboard](./architecture/dashboard.png)

## 📊 Key Insights
The final dashboard provides insights into:

Revenue performance over time

Customer purchasing behavior

Product profitability

Seasonal sales trends

Customer segmentation opportunities

---

## 🧠 What I Learned

Through this project, I gained hands-on experience with:

Microsoft Fabric architecture

OneLake and Lakehouse concepts

Dataflow Gen2 transformations

Data engineering with Fabric Notebooks

Medallion Architecture implementation

Semantic Modeling

Business Intelligence with Power BI

---

## 🚀 Project Value
This project demonstrates:

End-to-end analytics engineering workflow

Microsoft Fabric best practices

Modern Lakehouse architecture

Data transformation and enrichment

Business-oriented analytics design

Dashboard development and reporting

---

## 🔮 Future Enhancements 

Incremental data loading

Real-time analytics

Fabric Pipelines orchestration

Machine Learning integration

Advanced customer segmentation

---

## 👨‍💻 Author

Aboudoul Karim OUATTARA

Azure Data Engineer | Microsoft Fabric Analytics Engineer | Power BI Developer

📫 LinkedIn: https://www.linkedin.com/in/aboudoul-karim-ouattara-5baaba226/