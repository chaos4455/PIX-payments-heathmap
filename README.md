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

![mapa_calor_ociosidade_por_hora_loja](https://github.com/user-attachments/assets/355f8769-7ebc-43e8-b3fb-aedc858fe30c)

![mapa_calor_precos_baixos_por_hora_cidade](https://github.com/user-attachments/assets/d6456d74-a6f0-4684-951a-e09e71733f65)

![mapa_calor_tempo_medio_por_hora_cidade](https://github.com/user-attachments/assets/46675733-dcf7-42cd-9771-d90d04b2ea45)

![mapa_calor_precos_baixos_por_dia](https://github.com/user-attachments/assets/33bdb700-9e83-48db-848f-d4dc88e475d9)

![mapa_calor_tempo_medio_por_dia](https://github.com/user-attachments/assets/2bebe6fc-77d4-414b-b318-a5129c105169)

![mapa_calor_media_transacoes_por_dia](https://github.com/user-attachments/assets/7252bfd5-8c8a-4de3-85c0-293d4aaf0b1e)

![mapa_calor_minimos_por_dia](https://github.com/user-attachments/assets/641ed4ea-a7b5-4fce-8fb4-74b483daa0eb)

![mapa_calor_tempo_medio_por_semana](https://github.com/user-attachments/assets/746ec069-3f1e-4f18-b769-d043ae08ddfc)

![mapa_calor_minimos_por_semana](https://github.com/user-attachments/assets/eff1f167-a8bd-4fbb-8a3d-b41724bade87)

![mapa_calor_dia_mean](https://github.com/user-attachments/assets/89ac3c92-3eca-484d-880c-337f537a00e9)

![mapa_calor_dia_min](https://github.com/user-attachments/assets/75cc5141-a6be-4b06-b615-17ace33617a7)

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

