# SHADOWFOX-INTERMEDIATE
# 🚗 Car Price Prediction with Random Forest (ML Pipeline + Hyperparameter Tuning)

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)](https://jupyter.org)

This project builds a car price prediction pipeline using **Random Forest Regression**, complete with **data preprocessing**, **feature engineering**, **hyperparameter tuning using RandomizedSearchCV**, and **model evaluation**.  
It also exports the model using `joblib` and demonstrates feature importance and sample predictions.

---

## 📁 Files

- `car.csv` – Dataset (local)
- `car_price_prediction_pipeline.pkl` – Exported ML pipeline
- `README.md` – Project documentation
- `main.py` or `car_price_prediction.ipynb` – Python code/notebook for training & evaluation

---

## 📊 Dataset Description

The dataset contains historical data of used cars and includes the following features:

| Feature         | Description                         |
|----------------|-------------------------------------|
| `Car_Name`      | Name of the car (dropped)           |
| `Year`          | Year of purchase (used to derive age) |
| `Selling_Price` | Price at which the car is sold      |
| `Present_Price` | Current ex-showroom price (in lakhs)|
| `Kms_Driven`    | Distance driven                     |
| `Fuel_Type`     | Fuel type (Petrol, Diesel, etc.)    |
| `Seller_Type`   | Individual or Dealer                |
| `Transmission`  | Manual or Automatic                 |
| `Owner`         | Number of previous owners           |

Derived Feature:
- `Car_Age` = 2025 - `Year`

---

## 🧠 Model Pipeline Overview

This ML pipeline includes:

- **Preprocessing**:  
  - OneHotEncoding for categorical features (dropping first to avoid dummy trap)  
  - StandardScaler for numerical features  

- **Model**:  
  - RandomForestRegressor  
  - Hyperparameter tuning with `RandomizedSearchCV` (CV=5, scoring: RMSE)

- **Evaluation Metrics**:  
  - RMSE  
  - MAE  
  - R² Score  

---


