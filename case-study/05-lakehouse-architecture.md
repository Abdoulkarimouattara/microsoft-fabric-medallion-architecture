# 05 — Lakehouse Design

| Document Information |                                             |
| -------------------- | ------------------------------------------- |
| **Project**          | Microsoft Fabric Unified Analytics Platform |
| **Case Study**       | Nova Retail Group                           |
| **Document**         | Lakehouse Design                            |
| **Version**          | 1.0                                         |
| **Author**           | Aboudoul Karim OUATTARA                     |
| **Last Updated**     | June 2026                                   |

---

# Executive Summary

The Lakehouse is the foundation of the Microsoft Fabric analytics platform. It combines scalable storage with analytical capabilities, providing a single location where all Fabric workloads can access the same data through **OneLake**.

For this project, the Lakehouse was designed using the **Medallion Architecture**, ensuring that data quality improves progressively from ingestion to business reporting.

---

# Medallion Architecture

The platform separates data into three logical layers, each serving a specific purpose within the analytics lifecycle.

| Layer         | Purpose                                                          |
| ------------- | ---------------------------------------------------------------- |
| 🟤 **Bronze** | Preserve raw transactional data exactly as received.             |
| ⚪ **Silver**  | Store cleansed, standardized, and enriched datasets.             |
| 🟡 **Gold**   | Deliver curated business-ready datasets optimized for analytics. |

This layered approach improves data traceability, simplifies maintenance, and ensures that business users always consume trusted information.

---

# Why This Design?

The Lakehouse architecture was selected to support long-term scalability while keeping each layer focused on a single responsibility.

### Design Principles

* Preserve raw data for traceability.
* Isolate data quality transformations.
* Separate business logic from data preparation.
* Deliver reusable analytical datasets.

This separation of concerns makes the platform easier to maintain and extend as new business requirements emerge.

---

# OneLake Integration

All Lakehouse tables are stored in **OneLake**, allowing Microsoft Fabric workloads—including Dataflow Gen2, Fabric Notebooks, the Semantic Model, and Power BI—to access the same datasets without unnecessary duplication.

This unified storage model simplifies collaboration across workloads while ensuring a single source of truth for the organization.

---

**Previous Document ←** `04-solution-architecture.md`

**Next Document →** `06-dataflow-engineering.md`
