# DataLakeHouseProject

# Data Lakehouse Project (Databricks + Delta Lake + Unity Catalog)

A hands-on **Lakehouse** project built on **Databricks** using **Apache Spark / PySpark / Spark SQL**, **Delta Lake**, and **Unity Catalog**.  
It follows the **Medallion Architecture** (Bronze → Silver → Gold) to ingest raw data, clean/transform it, and publish analytics-ready tables.

---

## Tech Stack
- Databricks
- Apache Spark (PySpark)
- Spark SQL
- Delta Lake
- Unity Catalog (governance + permissions)

---

## Project Architecture (Medallion)
**Bronze (Raw / Ingest)**
- Load raw source data as-is (minimal transformations)
- Store as Delta tables for reliability and replayability

**Silver (Clean / Conform)**
- Clean & standardize data (types, null handling, deduping)
- Apply business rules and create conformed datasets

**Gold (Business / Analytics)**
- Curated tables for reporting/BI
- Aggregations and final analytics outputs

Repo structure:
├── Bronze/
├── Silver/
├── Gold/
└── README.md

---

## What This Project Demonstrates
- Building a **Lakehouse pipeline** end-to-end
- Using **Delta Lake** features (ACID tables, schema enforcement/evolution if applied)
- Using **Spark SQL** + **PySpark** transformations
- Organizing a project into **Bronze/Silver/Gold** layers
- Governance approach using **Unity Catalog** (catalog/schema/table organization + access control)

---

## How to Run (Databricks)
### Option A — Import notebooks from GitHub into Databricks
1. In Databricks workspace: **Repos** → **Add Repo**
2. Paste this repo URL:
   https://github.com/kdeepika11/DataLakeHouseProject
3. Open notebooks in order:
   1) `Bronze/` notebooks  
   2) `Silver/` notebooks  
   3) `Gold/` notebooks

### Option B — Download + Import
1. Download the repo as ZIP from GitHub
2. Upload notebooks into your Databricks workspace
3. Run Bronze → Silver → Gold

---

## Unity Catalog Setup (example)
> Adjust names based on your workspace standards.

Example object layout:
- Catalog: `lakehouse_demo`
- Schema: `bronze`, `silver`, `gold`

Typical flow:
1. Create catalog/schema
2. Write Delta tables into the correct schema by layer
3. Grant permissions as needed (UC governance)

---

## Outputs
- **Bronze tables:** raw ingested Delta tables
- **Silver tables:** cleaned + conformed Delta tables
- **Gold tables:** analytics-ready curated tables / aggregates

---

## Future Improvements
- Add data quality checks (expectations)
- Add incremental loads (Auto Loader / structured streaming)
- Add orchestration (Databricks Workflows)
- Add unit tests / validation queries
- Add a simple dashboard (Power BI / Databricks SQL)

---

## Author
Deepika Kalaimani  
GitHub: https://github.com/kdeepika11

