# 🎶 Spotify End-to-End ETL Data Engineering Project on AWS 🚀

This project demonstrates how to build a fully automated, scalable **ETL (Extract, Transform, Load)** data pipeline using **Spotify API** and **AWS services** like Lambda, S3, Glue, and Athena.

The project extracts Spotify's **Top 50** playlist data, processes it through transformations, and stores structured datasets for analytics — all running automatically without manual intervention.

---

## 📌 Project Objective

- Extract Spotify weekly **Top Songs - Global** playlist data.
- Store raw JSON data in Amazon S3.
- Process and transform raw data into structured **Artist**, **Album**, and **Song** tables.
- Store transformed CSV files in S3.
- Catalog the data using AWS Glue.
- Query the data using Amazon Athena.

---

## 🛠️ Solution Architecture

![Solution Architecture](aws_services_used_1.png)
![Solution Architecture](aws_services_used_2.png)

---

## 🎧 Integration with Spotify API

- A developer account is required to access Spotify Web APIs.
- API credentials (Client ID and Secret) are used for secure access.
- Data is pulled from the playlist endpoint using Python's **Spotipy** library.

---

## ☁️ AWS Services Used

| AWS Service | Purpose |
|-------------|---------|
| **AWS Lambda** | Serverless compute for extraction and transformation |
| **Amazon S3** | Storage for raw and transformed data |
| **AWS Glue** | Schema inference and Data Catalog |
| **Amazon Athena** | SQL query engine for S3-based data |
| **Amazon EventBridge** | Trigger Lambda functions on a schedule |

---

## 🛠️ Project Components

| Component | Details |
|-----------|---------|
| **First Lambda Function (Extraction)** | Fetches Spotify playlist JSON and stores it in `raw/to_be_processed/` S3 folder |
| **Second Lambda Function (Transformation)** | Converts raw JSON into structured CSVs (Artist, Album, Song) and stores in `transformed/` |
| **Glue Crawlers** | Auto-detects schema for transformed data and creates Athena query tables |
| **Athena Queries** | Analyze top songs, album counts, and release year trends |

---

## 📂 S3 Bucket Structure
