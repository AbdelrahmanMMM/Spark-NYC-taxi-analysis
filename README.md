# 🚖 NYC Taxi Data Analysis using Apache Spark

## 📌 Overview

This project analyzes NYC taxi trip data using Apache Spark to compute taxi utilization and trip patterns.

The goal is to understand how efficiently taxis operate based on location and time.

---

## 🎯 Objectives

* Calculate average idle time between trips per borough
* Count trips within the same borough
* Count trips across different boroughs

---

## 🧰 Technologies Used

* Apache Spark (PySpark)
* Python
* Shapely (Geospatial processing)
* GeoJSON
* Pandas (optional)

---

## ⚙️ Data Processing Steps

### 1. Data Enrichment

* Convert latitude/longitude into borough names
* Use GeoJSON + Shapely to map coordinates to regions

### 2. Data Cleaning

* Remove invalid trips (negative or very long duration)
* Compute trip duration using timestamps

### 3. Feature Engineering

* Calculate trip duration
* Compute idle time between trips using Spark Window functions

### 4. Analysis

* Average idle time per destination borough
* Trips within same borough
* Trips across boroughs

---

## 🔍 Key Concepts Demonstrated

* Spark DataFrames & transformations
* UDFs (User Defined Functions)
* Window functions
* Geospatial data processing
* Batch data pipeline design

---

## 📊 Sample Workflow

1. Load taxi dataset
2. Load GeoJSON borough data
3. Map coordinates → boroughs
4. Clean and transform data
5. Perform aggregations

---

## 🚀 How to Run

1. Install requirements:

```bash
pip install -r requirements.txt
```

2. Open the notebook:

```bash
jupyter notebook
```

---

## 📌 Notes

* Dataset is sampled due to size
* GeoJSON is broadcasted for performance optimization

---

## 💡 Future Improvements

* Convert notebook into production pipeline
* Use Spark Streaming
* Deploy on AWS EMR or Glue
