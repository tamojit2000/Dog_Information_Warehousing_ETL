# 🐶 Dog Allergy Data ETL Pipeline (Databricks + PySpark)

## 📌 Project Overview

This repository contains an **end-to-end ETL pipeline** built using **PySpark on Databricks**. The pipeline ingests dog-related data from a **public API**, cleans and transforms the JSON response, and loads the processed data into **Delta Lake tables** following the **Medallion Architecture (Bronze, Silver, Gold)**.

The project focuses on separating **allergenic** and **non-allergenic dog breeds**, optimizing Delta Lake writes, and orchestrating the complete workflow using **Databricks Jobs**.

---

## 🏗️ Architecture (Medallion Pattern)

```
Public Dog API
      |
      v
Bronze Layer (Raw JSON Data)
      |
      v
Silver Layer (Cleaned & Structured Data)
      |
      v
Gold Layer (Allergic vs Non-Allergic Dogs)
```

---

## ⚙️ Tech Stack

- **Programming Language:** Python
- **Big Data Framework:** PySpark
- **Platform:** Databricks
- **Storage Format:** Delta Lake
- **Architecture Pattern:** Medallion Architecture
- **Orchestration:** Databricks Jobs

---

## 🔄 ETL Workflow

### 1️⃣ Data Ingestion (Bronze Layer)
- Fetches dog-related data from a **public API**
- Stores raw JSON responses with minimal processing
- Preserves source data for traceability and reprocessing

---

### 2️⃣ Data Cleaning & Structuring (Silver Layer)
- Parses and normalizes JSON responses
- Handles nulls, invalid values, and inconsistent formats
- Converts cleaned data into a structured **PySpark DataFrame**

---

### 3️⃣ Business Transformations (Gold Layer)
- Applies transformation logic to classify dog breeds into:
  - **Allergic Dogs**
  - **Non-Allergic Dogs**
- Produces analytics-ready Delta tables

---

## 🚀 Delta Lake Optimizations

The following optimization techniques are implemented:

- Efficient write strategies to Delta format
- Minimized small file issues
- Post-load **OPTIMIZE** operations on Delta tables
- Improved read and query performance

---

## 🗄️ Archive Utility

- Custom utility developed to archive temporary and intermediate files
- Helps maintain clean storage paths
- Improves operational efficiency and storage management

---

## ⏱️ Orchestration

- The complete ETL pipeline is orchestrated using **Databricks Jobs**
- Jobs can be triggered manually or scheduled
- Ensures reliable and repeatable execution

---

## 📁 Project Structure

```
├── notebooks/
│   ├── bronze_ingestion.py
│   ├── silver_transformation.py
│   ├── gold_transformation.py
│
├── utils/
│   ├── archive_utility.py
│
├── jobs/
│   ├── databricks_job_config.json
│
├── README.md
```

---

## ✅ Key Features

- End-to-end ETL implementation
- Medallion architecture using Delta Lake
- PySpark-based transformations
- Delta Lake performance optimizations
- Custom archive utility
- Databricks Jobs orchestration

---

## 🔮 Future Enhancements

- Add data quality checks and validations
- Implement incremental data loading
- Add unit tests for transformations
- Integrate monitoring and alerting
- Schema enforcement and evolution

---

## 👤 Author

**Tamojit Das**  
Data Engineer | PySpark | Databricks | Delta Lake
