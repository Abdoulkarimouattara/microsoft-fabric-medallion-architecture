# 04 — Solution Architecture

| Document Information |                                             |
| -------------------- | ------------------------------------------- |
| **Project**          | Microsoft Fabric Unified Analytics Platform |
| **Case Study**       | Nova Retail Group                           |
| **Document**         | Solution Architecture                       |
| **Version**          | 1.0                                         |
| **Author**           | Aboudoul Karim OUATTARA                     |
| **Last Updated**     | June 2026                                   |

---

# Executive Summary

The solution was designed as a modern analytics platform built entirely on Microsoft Fabric. By leveraging native Fabric workloads, the architecture delivers an end-to-end analytics workflow while reducing the operational complexity typically associated with distributed cloud solutions.

---

# Architecture Overview

The platform follows a **Lakehouse architecture** implementing the **Medallion Architecture (Bronze → Silver → Gold)**.

Each workload has a clearly defined responsibility while sharing the same storage foundation through **OneLake**.

### High-Level Workflow

```text
Raw Dataset
      │
      ▼
Bronze Lakehouse
      │
      ▼
Dataflow Gen2
      │
      ▼
Silver Lakehouse
      │
      ▼
Fabric Notebook (PySpark)
      │
      ▼
Gold Lakehouse
      │
      ▼
Semantic Model
      │
      ▼
Power BI
```

---

# Workload Responsibilities

| Workload            | Responsibility                                        |
| ------------------- | ----------------------------------------------------- |
| **Lakehouse**       | Store data across Bronze, Silver, and Gold layers     |
| **Dataflow Gen2**   | Clean and standardize raw transactional data          |
| **Fabric Notebook** | Apply business logic and generate analytical datasets |
| **Semantic Model**  | Centralize KPIs and business metrics                  |
| **Power BI**        | Deliver interactive business reports                  |

---

# Design Principles

The architecture was designed around four key principles:

* Separation of concerns through the Medallion Architecture.
* Reusable analytical datasets.
* Centralized business logic.
* Native integration between Microsoft Fabric workloads.

These principles help improve maintainability, scalability, and consistency across the analytics platform.

---

**Previous Document ←** `03-why-microsoft-fabric.md`

**Next Document →** `05-lakehouse-design.md`
s