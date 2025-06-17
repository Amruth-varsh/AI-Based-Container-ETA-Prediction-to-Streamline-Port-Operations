# AI-Based Container ETA Prediction to Streamline Port Operations

Predicting the Estimated Time of Arrival (ETA) of shipping containers is a critical challenge in global logistics. In this project, we present a machine learning–based solution to estimate the ETA of vessels using vessel AIS data, inspired by DP World's vision of building a smarter and more connected trade ecosystem.

---

## 🚀 Problem Statement


Even with extensive logistics insights, unpredictable factors like weather, sea traffic, and dynamic port conditions can affect container arrivals. This project aims to use AI to reduce that uncertainty and make port operations more predictable and efficient.

---

## 📊 Dataset

We used a **simulated AIS dataset** that mimics real-world ship behavior, including the following features:

| Feature                | Description                          |
|------------------------|--------------------------------------|
| MMSI                   | Ship ID                              |
| Latitude, Longitude    | Current vessel coordinates           |
| Speed_knots            | Current speed of the ship            |
| Destination_Port       | Target port of arrival               |
| Distance_to_Port_km    | Estimated distance remaining         |
| Weather_Condition      | Real-time weather at ship’s location |
| ETA_hours (target)     | Actual time to arrive (in hours)     |

---

## 🧠 Machine Learning Approach

We framed this as a **regression problem** and used the following approach:

1. **Data Preprocessing**:
   - Label encoded categorical features (`Destination_Port`, `Weather_Condition`)
   - Selected relevant features for modeling

2. **Model**: 
   - Used **XGBoost Regressor**, a powerful and efficient tree-based model
   - Trained on 80% of data, tested on 20%

3. **Evaluation**:
   - Metrics: MAE, RMSE
   - Visualization: Predicted vs Actual ETA plot

---

## 📈 Results

- MAE: 14.02 hours
- RMSE: 16.70 hours
- Predictions closely followed actual ETA trends, proving feasibility even with small datasets.



---



- Accurate ETA predictions help:
  - Reduce port congestion
  - Improve berth and crane scheduling
  - Minimize idle time for containers and trucks
  - Boost overall supply chain efficiency

> This model is a **proof-of-concept** and can be scaled with real-time AIS feeds, port traffic data, and external APIs (like weather or congestion data).

---

## 🛣️ Future Work

- Integrate real AIS data from sources like MarineCadastre or exactEarth
- Add live weather + port congestion APIs
- Build a **Streamlit dashboard** for real-time visualizations
- Deploy the model as an API for smart port decision systems

---


