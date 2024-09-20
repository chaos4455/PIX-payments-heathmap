# 📊 Payment Transaction Heatmap Analysis for PIX in POS System

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-1.3.3-green)
![Flask](https://img.shields.io/badge/Flask-2.0.1-orange)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13.3-yellowgreen)

## 🚀 Introduction

This project involves the analysis of **historical data** from a **POS system** after the implementation of **automation**. The focus is on **PIX payment transactions**, examining timeframes and metrics to identify patterns in transaction values. 

By using **heatmaps**, we can visualize areas of interest, ranging from low to high transaction values, and provide insights into key performance indicators. The heatmaps use a color gradient that spans from **light yellow** 🌼, indicating low values, to **orange** 🍊 and **red** 🔴, highlighting areas of higher transaction concentration.

---

## 🎯 Objectives

The main objectives of this analysis are:

- **Evaluate transactional behavior** post-automation in a POS environment.
- **Identify anomalies** or patterns in transaction values across various timeframes.
- **Present visual insights** through heatmaps that help stakeholders to quickly understand transaction trends and points of interest.

---

## 🛠️ Technical Stack

The following technologies and libraries were utilized in the analysis and generation of heatmaps:

- **Python 3.9+**: Core programming language for data analysis and visualizations.
- **Pandas** 📊: Data manipulation and analysis library.
- **Matplotlib & Seaborn** 🌈: Libraries for generating heatmaps and other types of visualizations.
- **Numpy** ➗: For numerical computations.
- **Flask** 🚀: Backend framework for serving the data and API.
- **PostgreSQL** 🗄️: Database for storing transaction data.
- **Docker** 🐳: For containerization and environment consistency.
- **JWT Authentication** 🔑: Used for securing API endpoints that provide transaction data.
- **Qdrant** 🌐: For vector database management and optimized querying.
- **YAML** 📜: For configuration management of servers and endpoints.

---

## 📈 Heatmaps


A set of **heatmaps** was generated to provide insights into the **PIX transactions** over time, focusing on different metrics. Each heatmap visualizes the concentration and distribution of transaction values, allowing for easier identification of areas requiring attention or optimization. Below are the primary heatmaps included in the analysis:

### 🌟 Heatmap 1: Maximum Adjusted Transaction Values
![heatmap_adjusted_max_transacao](images/heatmap_adjusted_max_transacao_c635f47f129c4536c674651124343db9.png)

This heatmap displays the **maximum adjusted transaction values**. The brighter areas in **red** 🔴 highlight points where transaction values were significantly higher than the average, indicating potential peak usage periods or anomalies.

---

### 🌟 Heatmap 2: Minimum Adjusted Transaction Values
![heatmap_adjusted_min_transacao](images/heatmap_adjusted_min_transacao_480e36f8ad70b93fba0b7560971a2bd1.png)

This heatmap focuses on the **minimum adjusted transaction values**, helping to identify periods where transaction amounts dropped significantly, potentially pointing to low traffic or operational inefficiencies.

---

### 🌟 Heatmap 3: Mean Transaction Values
![heatmap_mean_transacao](images/heatmap_mean_transacao_d32c0c3f1088e1a3db9947e21776430f.png)

This heatmap displays the **mean transaction values**, offering insights into the average transaction amounts during specific timeframes. Areas with **orange** 🍊 or **red** 🔴 indicate higher mean values, while lighter colors point to lower averages.

---

### 🌟 Heatmap 4: Maximum Transaction Values
![heatmap_max_transacao](images/heatmap_max_transacao_987198a6695bb4487c25c839e548f819.png)

This heatmap captures the **maximum transaction values** across the dataset. High-value transactions are highlighted in **red** 🔴, signaling times where the system processed larger payments.

---

### 🌟 Heatmap 5: Minimum Transaction Values
![heatmap_min_transacao](images/heatmap_min_transacao_907499c2e6b67948cc1cf525b504f44a.png)

This heatmap provides insights into the **minimum transaction values**, allowing stakeholders to identify when the smallest transactions occurred, which can help in pricing analysis and understanding customer behavior.

---

## 🔄 Data Processing Workflow

The data processing pipeline for this analysis follows these key steps:

1. **Data Ingestion** 📥: Data is extracted from the **PostgreSQL database**, which stores all the relevant PIX transaction records.
   
2. **Preprocessing** 🧹: The data is cleaned and formatted using **Pandas**, ensuring that missing or inconsistent entries are handled. Date and time features are also processed to align the data across the timeframe.

3. **Metric Calculation** 🔢:
   - **Maximum Adjusted Transaction**: Calculated by normalizing transaction values to account for inflation or operational changes.
   - **Minimum Adjusted Transaction**: Similar to the maximum but focuses on the lowest values.
   - **Mean Transaction**: Average value calculated for each timeframe.
   - **Maximum and Minimum Transaction**: Basic metrics showing extremes in transaction values.

4. **Visualization** 🎨: Using **Matplotlib** and **Seaborn**, the cleaned data is passed into the heatmap function to generate the visualizations.

