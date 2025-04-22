# 🏏 Cricket Data ETL Project (Snowflake)

This project processes cricket match data (28 JSON files) through a complete ETL pipeline using **Snowflake**, following modern data lakehouse architecture. The workflow includes data movement from raw JSON to structured, analytics-ready tables, and finally to a presentation layer for visualization.

---

## 📊 Project Architecture

![Snowflake ETL Diagram](https://drive.google.com/uc?export=view&id=1D_s1AWLstfglBNOLt9vzmGW2AFuRZYpB)

---

## ❄️ What is Snowflake?

Snowflake is a fully-managed, cloud-native data platform used for data storage, transformation, and analytics. It separates compute and storage, supports semi-structured data like JSON, enables time travel, and offers seamless scaling for workloads across AWS, Azure, and GCP. It's commonly used for modern data pipelines and BI use cases.

---

## ✅ Layers Implemented

### 🔹 Landing Layer
- Imported 28 local JSON files using a **Named Stage**
- Defined **file format** for JSON
- Simulated AWS input using direct upload to Snowflake

### 🔸 Raw Layer
- Copied raw JSON into Snowflake without flattening
- Explored metadata and structure for understanding
- Performed light data profiling

### 🟩 Clean Layer
- Flattened deeply nested JSON arrays (players, deliveries)
- Created clean, structured tables with logical entities
- Transformed data to support analysis

### 🟢 Consumption Layer
- Created **Fact and Dimension tables**
- Established relationships for querying and reporting
- Ensured cleaned data was ready for BI tools

### 📊 Presentation Layer
- Connected structured Snowflake tables to a BI dashboard
- Enabled final visual insights using clean and organized datasets

---

## ⚙️ Automation
- Used **Streams** and **Tasks** in Snowflake to automate:
  - JSON ingestion
  - Periodic table updates
  - Incremental processing

---

## 🧰 Tech Stack
- **Snowflake** (Streams, Tasks, Transient Tables, Stages)
- **AWS S3** (assumed source)
- **SQL** (FLATTEN, VARIANT, COPY INTO, joins)
- **JSON** data format

---

## 🎯 Outcome
A fully operational Snowflake-based ETL pipeline for cricket match data — transforming raw JSON into structured, analyzable, and visualized insights.

