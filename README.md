# 🛒 Store Item Demand Forecasting  

**Author:** Onur Can Memiş  

This project tackles the [Kaggle Demand Forecasting Challenge](https://www.kaggle.com/competitions/demand-forecasting-kernels-only), where the goal is to predict daily sales for **50 items across 10 stores over 5 years**.  

Accurate forecasts = fewer stockouts, lower costs, smarter inventory.  

---

## 📊 What’s Inside
- A **Jupyter Notebook** (`HW3_DemandForecast.ipynb`) with the full analysis.  
- A **train/test dataset** (from Kaggle).  
- **Submission CSV** in Kaggle competition format.  

---

## 🚀 What I Did
- **Explored the data**: seasonality, long-term trends, and correlations.  
- **Feature engineered**:  
  - Calendar features (day, month, year, holidays).  
  - Rolling averages and lag features.  
  - Fourier features for seasonality.  
  - Both **categorical encoding** (for boosting) and **one-hot encoding** (for linear/MLP).  
- **Benchmarked models**:  
  - Classical: *Simple Exponential Smoothing, Holt-Winters*.  
  - ML: *Linear/Ridge/Lasso, XGBoost, LightGBM, CatBoost*.  
  - Deep Learning: *MLP, LSTM, GRU*.  
- **Evaluated** with:  
  - **SMAPE** (Symmetric Mean Absolute Percentage Error).  
  - **MSE** (Mean Squared Error).  
  - **Runtime complexity** (how long each takes).  
- **Explained results** with **feature importance** and **SHAP plots**.  

---

## ⚖️ What It Compares
- **Simple vs. advanced models** → does complexity really pay off?  
- **Tree-based boosting vs. deep learning** → which handles 500 time series better?  
- **Categorical encoding vs. one-hot encoding** → tradeoff between simplicity and scalability.  

---

## ✅ What Came Out at the End
- **LightGBM with tuned hyperparameters** was the best overall performer (balance of accuracy + speed).  
- Deep learning (LSTM/GRU) worked but required heavy compute and didn’t outperform boosted trees.  
- Classical methods gave **fast but weak** baselines.  
- Feature importance showed **date-related features (month, day-of-week)** and **lags** are most predictive.  

---

## 🎯 Value of the Project
- End-to-end workflow: **EDA → Features → Models → Evaluation → Interpretation → Submission**.  
- Combines **classical time series + modern ML/DL** in one notebook.  
- Connects forecasts to **real-world retail impact**: better stocking, reduced waste, and cost savings.  

---

## ⚙️ How to Run
1. Clone the repo  
2. Install requirements:  
   ```bash
   pip install -r requirements.txt
