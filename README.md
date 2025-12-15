# Stock-Price-Prediction-Using-Advanced-Modeling

This repository contains a comprehensive pipeline for forecasting daily stock prices using historical data from **NSE-TATAGLOBAL**. The project demonstrates a rigorous comparative analysis, moving beyond traditional statistical models (ARIMA) to implement advanced **Machine Learning (XGBoost)** and **Deep Learning (LSTM)** techniques.

## 🚀 Key Project Highlights

| Metric | Result | Conclusion |
| :--- | :--- | :--- |
| **Model Selection** | **XGBoost Regressor** | Optimal model for capturing non-linear market patterns. |
| **Best RMSE** | **₹9.03** | Lowest forecast error achieved. |
| **Improvement** | **26.6% Reduction in Error** | Outperformed the Moving Average baseline (₹12.30). |

* **Advanced Techniques:** Benchmarked performance across XGBoost, LSTM (Deep Learning), and statistical methods (ARIMA/SARIMA), demonstrating proficiency in both traditional and modern forecasting.
* **Feature Engineering:** Successfully engineered **Technical Indicators** (RSI, MA-50/200, Volatility) that drove superior predictive power for the non-linear models.

## ⚙️ Methodology and Pipeline

The project followed a production-ready time-series modeling pipeline:

### 1. Robust ETL & Data Integrity
* Handled data quality issues by performing business-day resampling.
* Corrected for **112 missing trading days** using a forward-filling (FFILL) imputation strategy.
* Corrected volume/turnover logic for imputed days (set to zero) to avoid false indicators of trading activity.

### 2. Exploratory Data Analysis (EDA)
* Conducted **Correlation Analysis** to identify redundant features (multicollinearity between OHLC data).
* Performed **Augmented Dickey-Fuller (ADF) Tests** for stationarity on raw and differenced log-prices.

### 3. Feature Engineering
* Created **Lag Features** to establish a supervised learning structure.
* Generated multiple **Technical Indicators** (RSI, MA-50, MA-200, Volatility).

### 4. Model Benchmarking and Selection
* **Established Baseline:** Moving Average (RMSE: ₹12.30).
* **Statistical Models:** Trained Auto-ARIMA and SARIMA models after validating stationarity.
* **Advanced Models:** Trained XGBoost and LSTM (Deep Learning) for non-linear forecasting.
* **Conclusion:** Selected **XGBoost** as the final model due to its ability to capture complex non-linear relationships between technical indicators and future price, validating the superiority of the Machine Learning approach over traditional statistical methods for this specific stock market regime.

## 🛠️ Setup and Requirements

This project requires the following libraries:

```bash
pandas
numpy
matplotlib
seaborn
statsmodels
pmdarima      # For Auto-ARIMA
```
scikit-learn  # For RMSE and scaling
xgboost       # For XGBoost Regressor
keras/tensorflow # For LSTM
