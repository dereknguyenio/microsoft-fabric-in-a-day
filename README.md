# Microsoft Fabric in a Day

> A curated, hands-on learning path for **Microsoft Fabric** — Microsoft's unified, end-to-end analytics platform that brings together data engineering, data warehousing, data science, real-time analytics, and business intelligence on a single SaaS foundation built on **OneLake**.

📖 **Browse the rendered exercises:** <https://dereknguyenio.github.io/microsoft-fabric-in-a-day/>
🗺️ **Suggested learning path:** see [CURRICULUM.md](./CURRICULUM.md)
🤝 **Want to contribute?** see [.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md)

---

## 📋 Table of Contents

- [What's inside](#-whats-inside)
- [Who this is for](#-who-this-is-for)
- [Prerequisites](#-prerequisites)
- [Lab catalog](#-lab-catalog)
- [Notebooks](#-notebooks)
- [Getting started](#-getting-started)
- [Repository structure](#repository-structure)
- [Reporting issues](#-reporting-issues)
- [Contributing](#-contributing)
- [Code of Conduct](#-code-of-conduct)
- [License](#-license)

---

## 🧭 What's inside

This repository hosts hands-on exercises that accompany the [Microsoft Fabric learning modules on Microsoft Learn](https://aka.ms/learn-fabric). Each lab is a self-contained, step-by-step walkthrough that you complete in the Microsoft Fabric portal.

The labs are grouped by Fabric **workload (experience)** so you can either follow the full "Fabric in a Day" journey or jump straight to the area that interests you.

## 👤 Who this is for

- **Data engineers** building lakehouses, pipelines, and notebooks on OneLake and Delta Lake
- **Data warehouse developers** modernizing onto the Fabric Warehouse
- **Data scientists** training and tracking ML models with MLflow inside Fabric
- **Analytics engineers** designing medallion (Bronze / Silver / Gold) architectures
- **Real-time analytics engineers** working with KQL databases and eventstreams
- **MCTs and trainers** delivering Fabric workshops who need ready-to-use lab content

## ✅ Prerequisites

To complete any of the exercises you will need:

1. A **Microsoft Fabric license**. The fastest way is to start a [free Fabric trial](https://learn.microsoft.com/fabric/get-started/fabric-trial). You'll need a Microsoft **work** or **school** account (a personal `@outlook.com` / `@gmail.com` account won't work). If you don't have one, [sign up for a Microsoft 365 trial](https://www.microsoft.com/microsoft-365/business/compare-more-office-365-for-business-plans).
2. A modern desktop browser (Microsoft Edge or Google Chrome are recommended).
3. Basic familiarity with **SQL** and (for the Spark / Data Science labs) **Python** is helpful but not required.

> **Tip:** Each lab is self-contained and tells you what to download. There is **nothing to install on your machine** — everything runs in the Fabric SaaS portal.

## 📚 Lab catalog

Each lab takes roughly 30–45 minutes. Labs build on shared concepts (workspaces, lakehouses, OneLake) but every lab creates its own resources, so you can start anywhere.

### 🛠️ Data Engineering & Lakehouse

| # | Lab | What you'll learn |
| - | --- | --- |
| 01 | [Create a Microsoft Fabric Lakehouse](./Instructions/Labs/01-lakehouse.md) | Create a workspace and lakehouse, upload files to OneLake, load data into a Delta table, query it with SQL and visualize it in Power BI. |
| 02 | [Analyze data with Apache Spark](./Instructions/Labs/02-analyze-spark.md) | Use Fabric notebooks and Spark to load, transform, and analyze data with PySpark and Spark SQL. |
| 03 | [Use Delta tables in Apache Spark](./Instructions/Labs/03-delta-lake.md) | Create managed and external Delta tables, perform ACID updates, time-travel queries, and streaming reads/writes. |
| 03b | [Create a medallion architecture in a Fabric lakehouse](./Instructions/Labs/03b-medallion-lakehouse-updated.md) | Organize a lakehouse using the **Bronze / Silver / Gold** pattern with notebooks, pipelines, and SQL endpoints. |
| 10 | [Ingest data with Spark and Microsoft Fabric notebooks](./Instructions/Labs/10-ingest-notebooks.md) | Build a notebook-based ingestion flow into a lakehouse using Spark. |

### 🔁 Data Integration (Pipelines & Dataflows)

| # | Lab | What you'll learn |
| - | --- | --- |
| 04 | [Ingest data with a pipeline in Microsoft Fabric](./Instructions/Labs/04-ingest-pipeline.md) | Use a Data Factory pipeline to copy data from an external source into a lakehouse, then transform it with a notebook activity. |
| 05 | [Create and use Dataflows (Gen2) in Microsoft Fabric](./Instructions/Labs/05-dataflows-gen2.md) | Build low-code data transformations with **Power Query** and land the results in a lakehouse table. |

### 🏛️ Data Warehouse

| # | Lab | What you'll learn |
| - | --- | --- |
| 06 | [Analyze data in a data warehouse](./Instructions/Labs/06-data-warehouse.md) | Create a Fabric Warehouse, model a star schema with dimensions and facts, query it with T-SQL, and build a Power BI report. |

### ⚡ Real-Time Analytics

| # | Lab | What you'll learn |
| - | --- | --- |
| 07 | [Get started with Real-Time Analytics in Microsoft Fabric](./Instructions/Labs/07-real-time-analytics.md) | Create a KQL database, ingest data, and query it with the Kusto Query Language (KQL). |
| 09 | [Get started with eventstreams in Real-Time Analytics](./Instructions/Labs/09-real-time-analytics-eventstream.md) | Capture, transform, and route streaming events into a KQL database and a lakehouse with **Eventstreams**. |

### 🤖 Data Science

| # | Lab | What you'll learn |
| - | --- | --- |
| 08 | [Train a classification model to predict customer churn](./Instructions/Labs/08-data-science.md) | Explore data, engineer features, train and compare models with **MLflow**, and register the best model for inference. |

> 📌 The full recommended ordering and "Fabric in a Day" workshop agenda lives in **[CURRICULUM.md](./CURRICULUM.md)**.

## 📓 Notebooks

The [`notebooks/`](./notebooks) folder contains ready-to-import Fabric notebooks that complement the labs. See [`notebooks/README.md`](./notebooks/README.md) for a description of each notebook and how to import it into your Fabric workspace.

## 🚀 Getting started

You **do not need to clone this repository** to complete the labs. The easiest way is:

1. Open the [rendered lab site](https://dereknguyenio.github.io/microsoft-fabric-in-a-day/).
2. Pick a lab from the table above.
3. Open [Microsoft Fabric](https://app.fabric.microsoft.com) in another tab and follow along.

If you'd rather work from a local copy (for example, to contribute changes), clone the repo:

```bash
git clone https://github.com/dereknguyenio/microsoft-fabric-in-a-day.git
cd microsoft-fabric-in-a-day
```

To preview the Jekyll site locally:

```bash
# Requires Ruby + Bundler. See https://jekyllrb.com/docs/installation/
bundle init
bundle add jekyll
bundle exec jekyll serve
```

## Repository structure

```text
.
├── Allfiles/                 # Supporting assets used by the labs
├── Instructions/Labs/        # Step-by-step lab markdown (rendered by Jekyll)
│   └── Images/               # Lab screenshots
├── notebooks/                # Fabric notebooks (e.g. medallion demo)
├── .github/                  # Issue & PR templates, contributing guide, workflows
├── _config.yml               # Jekyll site configuration
├── _build.yml                # Azure DevOps content-build pipeline
├── index.md                  # Jekyll landing page (rendered as the site home)
├── CURRICULUM.md             # Recommended learning path / workshop agenda
├── CODE_OF_CONDUCT.md
├── SECURITY.md
└── README.md
```

## 🐛 Reporting issues

If you hit a problem in any exercise, please open an [issue](../../issues/new/choose). Use the **Bug report** template and include:

- The **lab file** and **step number** where you got stuck
- What you expected vs. what happened
- Screenshots or error messages if relevant

> **Scope:** This repo only covers issues with the **exercise content**. For problems with the Microsoft Fabric service itself, please use [Fabric support](https://support.fabric.microsoft.com/support/).

## 🤝 Contributing

Contributions are very welcome — fixes for typos, broken links, outdated screenshots, or entirely new exercises. Please read [.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md) before opening a pull request.

The high-level flow:

1. Fork the repository.
2. Create a branch: `git checkout -b fix/lab-01-typo`.
3. Make your change and commit it with a clear message.
4. Open a pull request using the [PR template](./.github/PULL_REQUEST_TEMPLATE.md) and reference the related issue.

## 📜 Code of Conduct

This project adopts the [Microsoft Open Source Code of Conduct](./CODE_OF_CONDUCT.md). By participating you agree to abide by its terms.

## 🔒 Security

To report a security vulnerability, please follow the process described in [SECURITY.md](./SECURITY.md) — **do not** open a public GitHub issue.

## 📄 License

This project is licensed under the **MIT License**. See [LICENSE](./LICENSE) for details.

---

### Useful links

- [Microsoft Fabric documentation](https://learn.microsoft.com/fabric/)
- [Microsoft Learn — Fabric learning paths](https://aka.ms/learn-fabric)
- [Microsoft Fabric blog](https://blog.fabric.microsoft.com/)
- [Microsoft Fabric Community](https://community.fabric.microsoft.com/)

Happy learning! 🎉
