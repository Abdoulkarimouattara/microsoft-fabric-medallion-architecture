<p align="center">
  <img src="./images/banner.png" alt="Microsoft Fabric Unified Analytics Platform Banner">
</p>

<h1 align="center">🚀 Microsoft Fabric Unified Analytics Platform</h1>

<p align="center">
Designing a modern unified analytics platform with Microsoft Fabric
</p>

<p align="center">
A production-inspired end-to-end Data Engineering case study demonstrating how Microsoft Fabric unifies data ingestion, transformation, modeling, and business intelligence within a single analytics platform.
</p>

<p align="center">

<a href="#-solution-architecture">Architecture</a> • <a href="#-lakehouse-overview">Lakehouse</a> • <a href="#-data-engineering-workflow">Workflow</a> • <a href="#-dashboard-preview">Dashboard</a> • <a href="#-technical-case-study">Case Study</a>

</p>

---

# 📖 Executive Summary

Modern organizations often rely on multiple disconnected services to ingest, process, model, and visualize data. Managing these distributed architectures introduces operational complexity, governance challenges, and increased maintenance effort.

This project demonstrates how **Microsoft Fabric** simplifies the modern analytics lifecycle by providing a unified Software-as-a-Service (SaaS) platform where data engineering, analytics, semantic modeling, and business intelligence coexist within a single environment.

Using a retail analytics scenario, the solution follows the **Medallion Architecture (Bronze → Silver → Gold)** while leveraging **OneLake**, **Dataflow Gen2**, **Fabric Notebooks**, **Semantic Models**, and **Power BI** to deliver trusted business insights.

Beyond the technical implementation, this repository documents the architectural decisions, engineering practices, and production considerations behind the solution, making it a comprehensive technical case study.

---

# 📊 Project at a Glance

| Category              | Details                              |
| --------------------- | ------------------------------------ |
| **Industry**          | Retail & E-commerce                  |
| **Scenario**          | Unified Analytics Platform           |
| **Platform**          | Microsoft Fabric                     |
| **Storage**           | OneLake                              |
| **Architecture**      | Lakehouse + Medallion                |
| **Data Integration**  | Dataflow Gen2                        |
| **Data Processing**   | Fabric Notebooks (PySpark)           |
| **Analytics**         | Semantic Model                       |
| **Visualization**     | Power BI                             |
| **Engineering Focus** | Unified Analytics & Data Engineering |

---

# ⭐ Key Highlights

* End-to-End Microsoft Fabric Analytics Solution
* Unified SaaS Analytics Platform
* Lakehouse Architecture
* Medallion Architecture (Bronze → Silver → Gold)
* Dataflow Gen2 for data transformation
* Fabric Notebooks with PySpark
* Semantic Model
* Native Power BI Integration
* Production-inspired architecture
* Complete technical case study

# 💡 Why Microsoft Fabric?

This project was intentionally built on **Microsoft Fabric** to demonstrate how a unified analytics platform can simplify modern Data Engineering.

Unlike traditional architectures that rely on multiple cloud services, Microsoft Fabric brings data ingestion, storage, transformation, semantic modeling, and business intelligence into a single SaaS platform.

Using the same retail analytics scenario as the companion Azure project, this case study highlights how a unified platform can reduce architectural complexity while maintaining enterprise-grade Data Engineering practices.

# 🏗️ Unified Analytics Architecture

> **A single platform. One unified analytics experience.**

![Microsoft Fabric Architecture](./architecture/architecture.png)

Microsoft Fabric brings together every stage of the analytics lifecycle into a unified SaaS platform. Instead of integrating multiple independent services, the platform provides a seamless experience where data engineers, analysts, and business users collaborate using a shared architecture and a single storage layer powered by **OneLake**.

---

# ⚙️ Data Engineering Workflow

The solution follows a modern **Lakehouse architecture**, where data progressively evolves from raw transactional records to trusted business insights. Each Microsoft Fabric workload plays a dedicated role in this journey while sharing the same storage foundation through **OneLake**.

---

## 🏠 Lakehouse Organization

The journey begins in the **Microsoft Fabric Lakehouse**, where data is organized using the **Medallion Architecture**. This layered design separates raw, cleansed, and business-ready data, ensuring traceability, maintainability, and consistent analytics.

| Layer     | Purpose                          |
| --------- | -------------------------------- |
| 🟤 Bronze | Preserve raw source data         |
| ⚪ Silver  | Store cleansed and enriched data |
| 🟡 Gold   | Deliver business-ready datasets  |

📸 **Bronze Layer**

![Bronze Layer](./architecture/bronze_layer.png)

---

## 🔄 Dataflow Gen2

Once the raw data is available in the Bronze layer, **Dataflow Gen2** applies low-code transformations to improve data quality before publishing the results to the Silver layer.

**Key Transformations**

* Missing value handling
* Duplicate removal
* Data type standardization
* Business enrichment

📸 **Dataflow Gen2**

![Dataflow Gen2](./architecture/dataflow_gen2.png)

📸 **Silver Layer**

![Silver Layer](./architecture/silver_layer.png)

---

## 📓 Fabric Notebook (PySpark)

With clean and standardized data available, **Fabric Notebooks** use **PySpark** to implement business logic and generate curated Gold datasets optimized for analytics and reporting.

**Generated Data Products**

* Business KPIs
* Revenue Trends
* Product Performance
* Customer Analytics
* RFM Segmentation

📸 **Fabric Notebook**

![Fabric Notebook](./architecture/notebook_processing.png)

📸 **Gold Layer**

![Gold Layer](./architecture/gold_layer.png)

---

## 🧩 Semantic Model

The curated Gold datasets are then exposed through a **Semantic Model**, creating a centralized business layer where KPIs, relationships, and metrics are defined once and reused consistently across reports.

**Business Layer**

* Trusted KPIs
* Reusable business metrics
* Consistent reporting model

📸 **Semantic Model**

![Semantic Model](./architecture/semantic_model.png)

---

## 📊 Power BI Analytics

Finally, Power BI connects directly to the Semantic Model, allowing business users to explore interactive dashboards built on trusted, business-ready data without additional transformations.

**Business Insights**

* Revenue Performance
* Product Performance
* Customer Behavior
* Executive KPIs

📸 **Power BI Report**

![Power BI Report](./architecture/online_retail_report.png)
