# 03 — Why Microsoft Fabric

| Document Information |                                             |
| -------------------- | ------------------------------------------- |
| **Project**          | Microsoft Fabric Unified Analytics Platform |
| **Case Study**       | Nova Retail Group                           |
| **Document**         | Why Microsoft Fabric                        |
| **Version**          | 1.0                                         |
| **Author**           | Aboudoul Karim OUATTARA                     |
| **Last Updated**     | June 2026                                   |

---

# Executive Summary

Selecting the right analytics platform is an architectural decision rather than a technology preference. The chosen solution must satisfy business requirements while remaining scalable, maintainable, and easy to operate.

For this project, **Microsoft Fabric** was selected because it provides a unified analytics platform capable of managing the complete data lifecycle within a single environment.

---

# Why Microsoft Fabric?

Traditional analytics solutions often rely on multiple independent services for data ingestion, storage, transformation, modeling, and reporting. While this approach offers flexibility, it also increases operational complexity and platform management.

Microsoft Fabric simplifies this architecture by bringing these capabilities together in a unified SaaS platform.

### Key Advantages

* Unified analytics experience
* OneLake as a centralized storage layer
* Native integration between Fabric workloads
* Consistent governance and security
* Built-in Power BI integration

---

# Architecture Decisions

The following architectural choices guided the implementation of this solution:

| Decision            | Rationale                                                     |
| ------------------- | ------------------------------------------------------------- |
| **Lakehouse**       | Organize analytical data using the Medallion Architecture.    |
| **Dataflow Gen2**   | Perform low-code data cleansing and standardization.          |
| **Fabric Notebook** | Implement advanced business transformations with PySpark.     |
| **Semantic Model**  | Centralize KPIs and business logic for consistent reporting.  |
| **Power BI**        | Deliver interactive business insights using trusted datasets. |

Together, these components create a unified analytics workflow with minimal data movement and simplified platform management.

---

# Conclusion

Microsoft Fabric was selected not because it replaces every analytics architecture, but because it aligns well with the business and technical requirements of this project.

By combining data engineering, storage, semantic modeling, and business intelligence within a single platform, Fabric enables the delivery of trusted analytics while reducing architectural complexity.

---

**Previous Document ←** `02-business-challenges.md`

**Next Document →** `04-solution-architecture.md`
