
### Dataset  
🔗 [NYC Taxi Trip Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

---

## 🚀 Azure Data Engineering Pipeline with Medallion Architecture & Delta Lake

This project demonstrates a complete end-to-end data engineering solution built on **Azure Databricks**, following the **Medallion Architecture** (Bronze, Silver, Gold) and utilizing **Delta Lake** for optimized data management. The pipeline is designed to process, clean, and transform NYC Taxi trip data, delivering high-quality, analytics-ready datasets.

---

### 🛠️ Pipeline Architecture

#### 🔹 Bronze Layer – Raw Data Ingestion
- Used **Azure Data Factory** to dynamically ingest raw CSV/Parquet files into **Azure Data Lake Storage Gen2 (ADLS Gen2)**.
- Designed a dynamic pipeline capable of adapting to changing data patterns and file sizes for scalable ingestion.

#### 🔸 Silver Layer – Data Transformation
- Processed data in **Azure Databricks** using **PySpark** to clean, enrich, and apply business logic.
- Added derived columns such as `trip_date` and `trip_year`.
- Implemented data quality checks and stored the cleaned data back in ADLS in **Parquet** format.

#### 🟡 Gold Layer – Aggregation & Final Output
- Aggregated and optimized datasets were stored in **Delta Lake** format to support efficient querying and **time travel** capabilities.
- Created **Delta tables** (e.g., `trip_zone`, `trip_type`, `tripdata2023`) and leveraged **SQL** for analysis and insights.
- Enabled **schema evolution** to handle structural changes in source data seamlessly.

---

### 🔧 Technologies Used

- ✅ **Azure Data Lake Storage Gen2**
- ✅ **Azure Databricks**
- ✅ **Delta Lake**
- ✅ **PySpark**
- ✅ **Azure Data Factory (Dynamic Pipelines)**
- ✅ **Microsoft Entra ID** for authentication

---

### 🌟 Key Highlights

- **Scalability:** Designed a flexible pipeline that adjusts to data volume and complexity.
- **Data Quality:** Applied thorough validations and cleaning steps for trustworthy data.
- **Performance:** Leveraged **Delta Lake** for optimized storage and blazing-fast queries.
- **Versioning & Time Travel:** Maintained historical context with Delta Lake's versioning features.
