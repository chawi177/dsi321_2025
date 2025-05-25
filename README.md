# Near Real-Time PM2.5 Data Pipeline with Prefect, Streamlit, and ARIMA Forecasting

![Created at](https://img.shields.io/github/created-at/chawi177/dsi321_2025)
![Last Commit](https://img.shields.io/github/last-commit/chawi177/dsi321_2025)

## 📌 Project Overview

This project is a final assignment for the **DSI321: Big Data Infrastructure** course. It builds an automated data pipeline that collects, processes, and visualizes real-time PM2.5 air quality data in Bangkok using **Prefect**, **Docker**, and **Streamlit**. 

Beyond data ingestion and visualization, the project implements **time series forecasting** with **ARIMA models** to predict PM2.5 levels and help stakeholders anticipate air quality trends.

---

## 📊 Motivation

Air pollution, especially PM2.5, remains a critical health issue in Bangkok. This project aims to provide an end-to-end system that not only tracks real-time data but also forecasts future pollution levels to support early warnings and planning.

---

## 🚀 Features

### ✅ Automated ETL Pipeline (Prefect)
- Hourly scheduled data collection from Air4Thai API
- Data cleaning, transformation, and storage in CSV and Parquet formats
- Data versioning with LakeFS

### ✅ Forecasting (ARIMA)
- Time series modeling of PM2.5 data using ARIMA
- Hourly prediction of next hour PM2.5 levels per station
- Visualized forecast alongside historical data in Streamlit dashboard

### ✅ Visualization Dashboard (Streamlit)
- Interactive charts for real-time and forecasted PM2.5
- Station selection and time range filtering
- Auto-refresh every 60 seconds

### ✅ Containerized Environment (Docker)
- Services include Prefect orchestration, LakeFS, Streamlit UI, JupyterLab

---

## 🧬 Data Schema

| Column           | Type        | Description                            |
|------------------|-------------|----------------------------------------|
| timestamp        | datetime    | Timestamp of the reading               |
| stationID        | string      | Station ID                             |
| nameTH, nameEN   | string      | Station name (Thai & English)          |
| areaTH, areaEN   | string      | Area name (Thai & English)             |
| stationType      | string      | Type of station                        |
| lat, long        | float       | Coordinates                            |
| PM25.color_id    | integer     | Visualization color coding             |
| PM25.aqi         | float       | PM2.5 Air Quality Index                |
| year, month, day, hour | int   | Timestamp components                   |

---

## 🔧 Technologies Used

| Tool          | Purpose                              |
|---------------|---------------------------------------|
| Prefect       | Workflow orchestration and scheduling |
| Docker        | Containerization                      |
| Streamlit     | Dashboard visualization               |
| LakeFS        | Data versioning and rollback          |
| ARIMA (statsmodels) | Time series forecasting            |
| Air4Thai API  | Real-time PM2.5 data source           |
| JupyterLab    | Development & experimentation         |

---

## 🛠 How to Run

1. **Clone the repository**

```bash
git clone https://github.com/chawi177/dsi321_2025.git
cd dsi321_2025
