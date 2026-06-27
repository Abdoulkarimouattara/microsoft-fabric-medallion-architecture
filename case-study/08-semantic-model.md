# 08 — Semantic Model Design

| Document Information |                                             |
| -------------------- | ------------------------------------------- |
| **Project**          | Microsoft Fabric Unified Analytics Platform |
| **Case Study**       | Nova Retail Group                           |
| **Document**         | Semantic Model Design                       |
| **Version**          | 1.0                                         |
| **Author**           | Aboudoul Karim OUATTARA                     |
| **Last Updated**     | June 2026                                   |

---

# Executive Summary

The **Semantic Model** serves as the business layer of the analytics platform, exposing trusted datasets to Power BI while hiding the complexity of the underlying Lakehouse architecture.

Its primary objective is to provide a consistent and governed reporting experience across all business dashboards.

---

# Why a Semantic Model?

Rather than connecting reports directly to Lakehouse tables, the solution introduces a centralized Semantic Model that exposes curated business datasets.

### Responsibilities

* Connect Power BI to the Gold layer.
* Define relationships between analytical tables.
* Provide a single source of truth for reporting.
* Simplify dashboard development.

---

# Design Decision

Unlike many reporting solutions, business calculations are **not implemented inside Power BI**.

Instead, KPIs and analytical datasets are generated upstream in the **Fabric Notebook** and stored in the Gold layer.

This keeps the Semantic Model lightweight, easier to maintain, and focused on delivering trusted business data rather than performing complex transformations.

---

# Business Benefits

This design provides several advantages:

* Consistent KPIs across all reports.
* Faster report development.
* Reduced duplication of business logic.
* Better maintainability as the analytics platform evolves.

---

**Previous Document ←** `07-notebook-processing.md`

**Next Document →** `09-production-readiness.md`
