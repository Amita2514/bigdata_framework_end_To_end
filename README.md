# 🚖 NYC Taxi Trip Data Analytics & Machine Learning with PySpark

## 📌 Overview
This project implements an **end-to-end big data analytics pipeline** using **Apache Spark (PySpark)** to process and analyze the **New York City Taxi Trip Records Dataset**.  
It includes:
- **Data ingestion** from Kaggle
- **Data cleaning** and preprocessing
- **Exploratory Data Analysis (EDA)**
- **Feature engineering**
- **Machine learning models** using Spark MLlib (Regression, Classification, Clustering)
- **Interactive visualizations** with Matplotlib and Plotly

The pipeline demonstrates **Spark’s scalability, distributed processing capabilities, and machine learning integration** for large-scale transportation analytics.

---

## 📂 Dataset
**New York City Taxi Trip Records Dataset**
- **Source:** [Kaggle – NYC Yellow Taxi Trip Data](https://www.kaggle.com/elemento/nyc-yellow-taxi-trip-data)
- **Data Types:** Yellow, Green, FHV, and HVFHS taxi trips
- **Key Columns:** Pickup & drop-off times, passenger count, trip distance, fare amount, tip amount, payment type, coordinates
- **Size:** Millions of rows across multiple monthly CSV files

---

## 🎯 Project Objectives
- Build a scalable pipeline to **ingest and preprocess large-scale NYC taxi data**
- Perform **data cleaning** to handle missing or inconsistent values
- Conduct **EDA** using PySpark SQL and visualizations
- Engineer new features such as:
  - Trip distance (Haversine formula)
  - Trip duration
  - Average speed
- Train and evaluate **Spark MLlib** models for:
  - **Regression** — Predict fare amounts
  - **Classification** — Identify high tip trips
  - **Clustering** — Segment trips with K-Means
- Export trained pipelines for deployment

---

## 🛠 Methodology

### 1️⃣ Data Ingestion
- Download dataset from Kaggle using the API
- Load CSV into PySpark DataFrames
- Store processed data in **Parquet format** for faster queries

### 2️⃣ Data Cleaning
- Handle missing values in key fields
- Remove invalid trips (zero distance, negative fare)
- Standardize column names and data types

### 3️⃣ RDD Transformations
- Apply `map`, `filter`, and `reduce` for distributed processing
- Aggregate trip counts, distances, and fares

### 4️⃣ Spark SQL Exploration
- Register DataFrames as SQL temporary views
- Query busiest pickup locations, peak hours, and fare trends

### 5️⃣ Feature Engineering
- Compute **trip distance** using Haversine formula
- Calculate **trip duration** and **average speed**
- Encode categorical features for MLlib models

### 6️⃣ Machine Learning
- **Regression:** Linear Regression for fare prediction
- **Classification:** Logistic Regression for high-tip classification
- **Clustering:** K-Means for trip pattern segmentation
- Evaluate with RMSE, accuracy, and silhouette score

### 7️⃣ Visualization
- **Matplotlib** and **Plotly** for:
  - Trip duration histograms
  - Fare vs. distance scatter plots
  - Cluster visualizations

---

## 📊 Results
- **Regression:** Low RMSE for fare predictions
- **Classification:** Good precision and recall for high-tip prediction
- **Clustering:** Clear trip segments (short trips, airport trips, long-haul rides)
- Visualizations confirmed patterns between trip distance, fare, and location

---

## ⚙️ Setup Instructions

### 🔹 Prerequisites
- Python 3.8+
- Apache Spark 3.5.1
- Kaggle API Key
- Jupyter Notebook or Google Colab

### 🔹 Installation
```bash
pip install pyspark==3.5.1 kaggle plotly matplotlib pyngrok
