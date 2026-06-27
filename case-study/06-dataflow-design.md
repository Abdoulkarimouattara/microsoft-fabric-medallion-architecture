# 06 — Dataflow Engineering

| Document Information |                                             |
| -------------------- | ------------------------------------------- |
| **Project**          | Microsoft Fabric Unified Analytics Platform |
| **Case Study**       | Nova Retail Group                           |
| **Document**         | Dataflow Engineering                        |
| **Version**          | 1.0                                         |
| **Author**           | Aboudoul Karim OUATTARA                     |
| **Last Updated**     | June 2026                                   |

---

# Executive Summary

Data quality is the foundation of every successful analytics platform. Before business insights can be generated, raw transactional data must be cleaned, standardized, and enriched.

For this project, **Dataflow Gen2** was selected to perform these operations using a low-code approach, producing reliable Silver datasets for downstream analytics.

---

# Why Dataflow Gen2?

Instead of implementing data preparation in custom code, the project leverages **Dataflow Gen2** to handle repeatable data quality operations.

This approach improves readability, simplifies maintenance, and allows transformation logic to be managed visually within Microsoft Fabric.

### Responsibilities

* Clean raw transactional data.
* Standardize data types.
* Remove duplicate records.
* Enrich business attributes.
* Publish trusted Silver datasets.

---

# Data Quality Transformations

The following transformations are applied before data reaches the Silver layer:

### Data Cleansing

* Missing value handling
* Duplicate removal
* Data type standardization

### Business Enrichment

Additional analytical attributes are generated to simplify downstream processing:

* `line_total`
* `year`
* `month`
* `is_return`

These enriched datasets provide a clean and consistent foundation for business transformations performed later in the Fabric Notebook.

---

# Engineering Decision

Dataflow Gen2 was intentionally limited to **data preparation**.

Business calculations, KPI generation, and analytical aggregations are performed separately within **Fabric Notebooks**, ensuring a clear separation between data quality operations and business logic.

This design improves maintainability and makes the analytics workflow easier to understand and extend.

---

**Previous Document ←** `05-lakehouse-design.md`

**Next Document →** `07-notebook-processing.md`
