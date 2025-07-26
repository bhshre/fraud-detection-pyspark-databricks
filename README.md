#  Financial Transactions Fraud Detection using PySpark and Spark SQL on Databricks

This project demonstrates end-to-end analysis of financial transactions to identify fraudulent behavior using PySpark and Spark SQL in Databricks (Community Edition). The focus is on building a real-time data pipeline simulating a real-world lakehouse architecture: **Raw → Cleansed → Curated → Serving Layer (Insights)**.

---

##  Project Overview

- **Tech Stack**: PySpark, Spark SQL, Databricks (CE), Google Colab (for versioning)
- **Objective**: Identify fraud patterns, evaluate fraud detection effectiveness, and highlight high-risk transaction types and anomalies.

---

##  Pipeline Architecture

### 1. Raw Layer
- Load the raw CSV dataset into Spark.
- Schema inference and initial data preview.

### 2. Cleansed Layer
- Handle nulls, data type casting, and standardization of column names.
- Filter irrelevant or corrupted records.

### 3. Curated Layer
- Transform data to include:
  - Fraud labels
  - Balance difference checks
  - Aggregated summaries per transaction type
  - High-value fraud filters

### 4. Serving Layer (Insights)
- Transaction Type Summary
- Total Amount Transacted Per Type
- Fraud Detection Summar

---

##  Key Insights

1. **CASH_OUT** and **TRANSFER** are the most frequent and high-value transaction types.
2. Fraud is exclusively found in **CASH_OUT** and **TRANSFER** types.
3. **1,142 real frauds** exist, but **0 flagged** — indicating complete failure of the system's fraud detection logic.
4. High-value frauds (up to 10 million units) are predominantly through **TRANSFER**.
5. Funds not credited to destination in fraud cases — highlighting **balance manipulation**.

---

## My Project file
[Databricks_notebook](https://github.com/bhshre/fraud-detection-pyspark-databricks/blob/main/bank_project_new.ipynb)

---

## About Me
This project was created by Shreya Bhattacharjee, MSC in data science, Diploma in Data Science an Big Data, an aspiring Data Scientist and Data Engineer passionate about solving real-world problems through data.

Let's connect on [LinkedIn](https://www.linkedin.com/in/shreya-bhattacharjee-47b01129a/) or check out more projects on [GitHub](https://github.com/bhshre)


