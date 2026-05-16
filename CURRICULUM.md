# Microsoft Fabric in a Day — Curriculum Guide

This guide proposes a **recommended ordering** for the labs in this repository and a sample **one-day workshop agenda**. It's designed for trainers running "Fabric in a Day" sessions and for self-learners who want a coherent end-to-end journey through Microsoft Fabric.

> 📚 Looking for the lab catalog instead? See the [README](./README.md).

## 🎯 Learning outcomes

By the end of this curriculum you will be able to:

1. Describe the Microsoft Fabric SaaS platform, its workloads, and the role of **OneLake**.
2. Create and organize a **lakehouse** following the **medallion (Bronze / Silver / Gold)** pattern.
3. Ingest data using **pipelines**, **Dataflows Gen2**, and **Spark notebooks**.
4. Query data with **SQL** (Warehouse) and **KQL** (Real-Time Analytics).
5. Train, track, and register a machine-learning model with **MLflow** in Fabric.
6. Build a basic Power BI report on top of curated lakehouse / warehouse data.

## 🧱 Foundational concepts (read first)

Before the first lab, skim these short Microsoft Learn pages — they give you the vocabulary used throughout the labs:

- [What is Microsoft Fabric?](https://learn.microsoft.com/fabric/get-started/microsoft-fabric-overview)
- [OneLake — the OneDrive for data](https://learn.microsoft.com/fabric/onelake/onelake-overview)
- [Workloads and experiences in Fabric](https://learn.microsoft.com/fabric/get-started/decision-guide-experience)
- [Delta Lake table format](https://learn.microsoft.com/fabric/data-engineering/lakehouse-and-delta-tables)

## 🗺️ Recommended learning path

The labs are designed to be self-contained, but completing them in this order gives the smoothest narrative — each lab introduces a new Fabric workload that builds on what you've just learned.

| Step | Lab | Why it's next |
| ---- | --- | ------------- |
| 1 | [01 — Create a Lakehouse](./Instructions/Labs/01-lakehouse.md) | Introduces workspaces, OneLake, files vs. tables, and the SQL endpoint. |
| 2 | [02 — Analyze data with Apache Spark](./Instructions/Labs/02-analyze-spark.md) | Adds the notebook + Spark experience on top of the lakehouse. |
| 3 | [03 — Use Delta tables in Apache Spark](./Instructions/Labs/03-delta-lake.md) | Goes deeper on Delta: ACID, time travel, managed vs. external tables, streaming. |
| 4 | [03b — Medallion architecture in a lakehouse](./Instructions/Labs/03b-medallion-lakehouse-updated.md) | Puts it all together into a Bronze / Silver / Gold lakehouse. |
| 5 | [04 — Ingest data with a pipeline](./Instructions/Labs/04-ingest-pipeline.md) | Introduces Data Factory pipelines for orchestrated ingestion. |
| 6 | [05 — Dataflows (Gen2)](./Instructions/Labs/05-dataflows-gen2.md) | Adds a low-code Power Query-based ingestion option. |
| 7 | [10 — Ingest data with Spark and notebooks](./Instructions/Labs/10-ingest-notebooks.md) | Compares the code-first ingestion path with the previous low-code paths. |
| 8 | [06 — Analyze data in a Data Warehouse](./Instructions/Labs/06-data-warehouse.md) | Contrasts the lakehouse with the T-SQL Warehouse experience. |
| 9 | [07 — Real-Time Analytics with KQL](./Instructions/Labs/07-real-time-analytics.md) | Introduces KQL databases for time-series / log data. |
| 10 | [09 — Eventstreams in Real-Time Analytics](./Instructions/Labs/09-real-time-analytics-eventstream.md) | Adds streaming ingestion on top of Real-Time Analytics. |
| 11 | [08 — Train a classification model](./Instructions/Labs/08-data-science.md) | Brings the data-science experience and MLflow into the picture. |

## 🕘 Sample one-day workshop agenda

A realistic "Fabric in a Day" agenda. Times include short breaks and Q&A buffer.

| Time | Block | Content |
| ---- | ----- | ------- |
| 09:00 – 09:30 | Welcome & overview | What is Fabric? OneLake, workspaces, capacities, trial setup. |
| 09:30 – 10:30 | **Lakehouse fundamentals** | Lab 01 — Create a Lakehouse. |
| 10:30 – 10:45 | ☕ Break | |
| 10:45 – 12:15 | **Spark & Delta** | Labs 02 and 03. |
| 12:15 – 13:15 | 🍽️ Lunch | |
| 13:15 – 14:15 | **Medallion architecture** | Lab 03b. |
| 14:15 – 15:15 | **Data integration** | Lab 04 (pipelines) and a quick tour of Lab 05 (Dataflows Gen2). |
| 15:15 – 15:30 | ☕ Break | |
| 15:30 – 16:15 | **Warehouse** | Lab 06. |
| 16:15 – 17:00 | **Real-Time or Data Science** (instructor's choice) | Lab 07 / 09 or Lab 08. |
| 17:00 – 17:30 | Wrap-up, Q&A, next steps | |

## 🧑‍🏫 Tips for trainers

- **Pre-provision workspaces** for each attendee where possible — workspace creation can occasionally take a few minutes during a class.
- Ask attendees to **start their Fabric trial 24 hours before** the workshop so account propagation issues surface early.
- Each lab tells students which sample files to download — point them at the public `MicrosoftLearning/dp-data` GitHub raw URLs that the labs reference.
- Encourage attendees to **delete their workspace** at the end of the day to avoid using trial capacity on idle artifacts.

## 🧑‍🎓 Tips for self-learners

- Treat the labs as a launchpad: after each lab, take 10 minutes to **break something on purpose** (rename a table, drop a column) and watch how Fabric responds. You'll learn the platform far faster.
- Pair each lab with the matching Microsoft Learn module — the modules go deeper on the "why".
- Join the [Microsoft Fabric Community](https://community.fabric.microsoft.com/) to ask questions and see what others are building.

## 🔗 Where to go next

- [Microsoft Fabric documentation](https://learn.microsoft.com/fabric/)
- [Fabric end-to-end tutorials](https://learn.microsoft.com/fabric/get-started/end-to-end-tutorials)
- [Power BI learning paths](https://learn.microsoft.com/training/powerplatform/power-bi)
- [DP-600: Fabric Analytics Engineer certification](https://learn.microsoft.com/credentials/certifications/fabric-analytics-engineer-associate/)
