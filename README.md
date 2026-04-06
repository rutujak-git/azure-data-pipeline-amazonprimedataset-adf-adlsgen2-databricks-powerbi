# azure-data-pipeline-amazonprimedataset-adf-adlsgen2-databricks-powerbi
End-to-end data engineering pipeline using Azure Data Factory (HTTP ingestion), Azure Databricks (PySpark), and ADLS Gen2 implementing Medallion Architecture on the Amazon Prime Movies &amp; TV Shows dataset, with Power BI reporting.

# End-to-End Data Engineering Pipeline using Azure & Databricks

<img width="2563" height="1442" alt="image" src="https://github.com/user-attachments/assets/7015abaf-d86e-4b58-8f06-b973014a79bf" />


## 📌 Overview
This project demonstrates a real-world, etl data pipeline built using Azure services and Databricks, based on the Amazon Prime Movies & TV Shows dataset.

The pipeline simulates enterprise ingestion patterns by sourcing data from GitHub via HTTP and processing it through a Medallion Architecture.

---

## 🏗️ Architecture

Kaggle → GitHub → Azure Data Factory → ADLS (Bronze) → Databricks (Silver & Gold) → Power BI

<img width="1913" height="1079" alt="image" src="https://github.com/user-attachments/assets/2700c9d7-dc95-428d-b0e0-b65cfcf71577" />


---

## ⚙️ Tech Stack

- Azure Data Factory (ADF)
- Azure Data Lake Storage Gen2 (ADLS)
- Azure Databricks (PySpark)
- Delta Lake
- Power BI
- GitHub

---

## 🔄 Pipeline Flow

### 🔹 Data Source
- Dataset: Amazon Prime Movies & TV Shows (Kaggle)
- Hosted on GitHub for HTTP-based ingestion

### 🔹 Ingestion (ADF)
- ADF Copy Activity pulls data from GitHub (HTTP)
- Stores raw data in ADLS Bronze layer

### 🔹 Bronze Layer
- Raw, unprocessed data
- Stored in Delta format
- Append-only ingestion

### 🔹 Silver Layer
- Data cleaning and transformation
- Incremental processing using watermark logic
- Deduplication and schema enforcement

### 🔹 Gold Layer
- Business-level aggregations
- Analytics-ready datasets

### 🔹 Visualization
- Power BI connected to Gold layer for reporting

---

## 🚀 Key Features

- End-to-end pipeline using Azure ecosystem
- HTTP-based ingestion using ADF
- Medallion architecture (Bronze, Silver, Gold)
- Incremental data processing
- Delta Lake MERGE operations
- Scalable and modular design

---

## 📂 Project Structure
(Add your folder structure here)

---

## ▶️ How to Run

1. Upload dataset to GitHub
2. Configure ADF pipeline to pull data via HTTP
3. Load data into ADLS Bronze layer
4. Run Databricks notebooks for:
   - Silver transformations
   - Gold aggregations
5. Connect Power BI to Gold layer

---

## 🎥 YouTube Walkthrough
https://youtu.be/J1cyf5B1wWU?si=3Njr9bu4oxWTc5lw

---

## 📌 Dataset
Amazon Prime Movies & TV Shows (Kaggle) : https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbVBzZXJSdjZMYkhWTDI4Qk96WXNaNTFSOXRxUXxBQ3Jtc0trck5Da1hpbFF4NmdTMEF2bDNWUXJla0RtSEQ0YkpGVVlheEtnNmpyLS00NlhEblVuYjFmeXQxbUZvV3U4REFoY2JvTnJCZnl6c2NFdXo3Z3JMSVpKQ2JyTTZtRy1DMUpmZlFCOFlxOVctRThWazBiSQ&q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fshivamb%2Famazon-prime-movies-and-tv-shows&v=J1cyf5B1wWU
