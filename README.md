# 🛠️ dbt (data build tool) — Introduction & Intermediate

![dbt](https://img.shields.io/badge/dbt--core-1.8-FF694B?logo=dbt&logoColor=white)
![DuckDB](https://img.shields.io/badge/Warehouse-DuckDB-FFF000?logo=duckdb&logoColor=black)
![SQL](https://img.shields.io/badge/Language-SQL%20%7C%20Jinja%20%7C%20YAML-blue)
![Platform](https://img.shields.io/badge/Platform-DataCamp-03EF62?logo=datacamp&logoColor=black)
![Courses](https://img.shields.io/badge/Courses-2-orange)
![Level](https://img.shields.io/badge/Level-Intermediate-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

> **Platform:** DataCamp  
> **Instructor:** Mike Metzger — Data Engineer

---

## 📖 About This Repository

**dbt** is the industry-standard tool for the **Transform** step of modern **ELT** pipelines: it turns raw warehouse tables into tested, documented and version-controlled data models using SQL, Jinja and YAML.

Across two courses I built the `nyc_yellow_taxi` project end-to-end on the **NYC Yellow Taxi trip records (January 2023)** with **DuckDB** as the warehouse — from `dbt init` and the first SQL model, to data-quality tests, sources, seeds, SCD Type 2 snapshots and a production run with `dbt build`.

Each course folder contains a **notebook that presents what I learned**: the theory in my own words plus every hands-on exercise in order, with the code I wrote and screenshots of the results as evidence.

---

## 🗂️ Course Structure

| # | Folder | Course | Key topics |
|---|--------|--------|------------|
| 1 | [`Course1_IntroToDbt`](./Course1_IntroToDbt) | Introduction to dbt | `dbt init`, `profiles.yml`, models, `dbt run`, docs, Jinja, `ref()` & DAG |
| 2 | [`Course2_IntermediateDbt`](./Course2_IntermediateDbt) | Intermediate dbt | Built-in / singular / generic tests, sources, seeds, snapshots (SCD2), `dbt build` |

```
dbt/
├── Course1_IntroToDbt/
│   ├── dbt_Course1_IntroToDbt.ipynb      ← showcase notebook
│   ├── Ch1..Ch3 *.pdf                     ← lesson slides
│   └── screenshots/                       ← exercise evidence
└── Course2_IntermediateDbt/
    ├── dbt_Course2_IntermediateDbt.ipynb  ← showcase notebook
    ├── Ch1..Ch2 *.pdf                     ← lesson slides
    └── screenshots/                       ← exercise evidence
```

---

## 📚 Course Details

### 📌 Course 1 — Introduction to dbt
> Notebook: [`dbt_Course1_IntroToDbt.ipynb`](./Course1_IntroToDbt/dbt_Course1_IntroToDbt.ipynb)

Foundations of dbt and the ELT workflow. Creating and configuring a project against DuckDB, writing SQL models over Parquet data and materializing them as views/tables, answering a business request with a new model, generating and serving documentation, dynamic SQL with Jinja, and building model hierarchies (DAG) with `ref()`.

---

### 📌 Course 2 — Intermediate dbt
> Notebook: [`dbt_Course2_IntermediateDbt.ipynb`](./Course2_IntermediateDbt/dbt_Course2_IntermediateDbt.ipynb)

Data quality and production readiness. Built-in tests (`unique`, `not_null`, `accepted_values`, `relationships`), singular tests and reusable generic tests with Jinja; debugging failing tests; declaring sources with `source()`; loading reference data with seeds; tracking history with SCD Type 2 snapshots; and running the full pipeline with `dbt build` before publishing the docs.

---

## 🧰 Skills Demonstrated

- Designing a dbt project structure and configuring warehouse connections (`profiles.yml`, `dbt_project.yml`)
- Writing modular SQL models and managing dependencies with `ref()` / `source()`
- Implementing data-quality testing strategies (built-in, singular and generic tests)
- Handling reference data (seeds) and historical changes (SCD2 snapshots)
- Running production pipelines with `dbt build` and generating lineage documentation
- Debugging compilation and runtime errors in a dbt project

---

## 🚀 How to View

```bash
git clone https://github.com/JuanCGJ/dbt.git
cd dbt
jupyter notebook
```

Or open the `.ipynb` files directly on GitHub — the notebooks are fully rendered with their screenshots.

---

*Built with 🤍 as part of a continuous learning journey in Data Analytics & Data Engineering.*
