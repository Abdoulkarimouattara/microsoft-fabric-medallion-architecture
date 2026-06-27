# 07 — Notebook Processing

| Document Information |                                             |
| -------------------- | ------------------------------------------- |
| **Project**          | Microsoft Fabric Unified Analytics Platform |
| **Case Study**       | Nova Retail Group                           |
| **Document**         | Notebook Processing                         |
| **Version**          | 1.0                                         |
| **Author**           | Aboudoul Karim OUATTARA                     |
| **Last Updated**     | June 2026                                   |

---

# Executive Summary

Once the Silver layer provides clean and standardized data, **Fabric Notebooks** are used to perform advanced business transformations using **PySpark**.

Rather than focusing on data cleansing, the notebook is dedicated to generating business-ready datasets that can be consumed directly by the Semantic Model and Power BI.

---

# Why Fabric Notebooks?

Fabric Notebooks provide the flexibility of **PySpark** for implementing complex business logic while taking advantage of the native integration with the Lakehouse.

### Responsibilities

* Read Silver Lakehouse tables.
* Apply business transformation logic.
* Compute analytical KPIs.
* Generate curated Gold datasets.

---

# Business Data Products

Instead of exposing raw transactional tables, the notebook produces reusable analytical datasets tailored for business reporting.

### Generated Tables

* `kpis`
* `monthly_trends`
* `top_revenue`
* `top_quantity`
* `top_customers`
* `rfm_segmentation`

These curated tables form the Gold layer and are optimized for reporting, ensuring that business users interact only with trusted analytical data.

---

# Engineering Decision

Business calculations are intentionally performed within the Notebook rather than inside Power BI.

This approach centralizes business logic within the data platform, allowing multiple reports to reuse the same curated datasets while keeping the reporting layer lightweight and easier to maintain.

---

**Previous Document ←** `06-dataflow-engineering.md`

**Next Document →** `08-semantic-model-design.md`
