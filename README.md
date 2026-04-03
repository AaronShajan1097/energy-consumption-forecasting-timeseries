# ⚡ Energy Consumption Forecasting

## 📌 Project Overview

This project focuses on forecasting household energy consumption using time series analysis techniques. The goal is to build accurate short-term prediction models that can help optimize energy usage, reduce costs, and support efficient energy management.

Two models were implemented and compared:

* **Prophet** (final selected model)
* **SARIMA** (baseline statistical model)

---

## 🎯 Objectives

* Perform exploratory data analysis (EDA) to understand trends and seasonality
* Preprocess and clean time series data
* Handle missing values using interpolation
* Resample data to hourly frequency
* Test stationarity using ADF test
* Build forecasting models using Prophet and SARIMA
* Evaluate models using MAE, RMSE, and MAPE
* Generate forecasts with confidence intervals
* Compare models and select the best-performing approach

---

## 🧠 Approach

### 1. Data Preprocessing

* Converted date and time into datetime format
* Set datetime as index
* Converted all features to numeric
* Handled missing values using time-based interpolation
* Resampled data to hourly frequency

### 2. Time Series Analysis

* Checked stationarity using Augmented Dickey-Fuller (ADF) test
* Performed time series decomposition to analyze:

  * Trend
  * Seasonality
  * Residuals

### 3. Modeling

#### 🔹 Prophet

* Captures trend and multiple seasonalities automatically
* Supports uncertainty intervals
* Minimal manual tuning required

#### 🔹 SARIMA

* Traditional statistical model
* Requires manual parameter tuning
* Used as a baseline for comparison

---

## 📊 Model Evaluation

| Model   | MAE   | RMSE  |
| ------- | ----- | ----- |
| Prophet | 0.494 | 0.639 |
| SARIMA  | 0.511 | 0.663 |

### ✅ Final Model Selection

**Prophet** was selected because:

* Lower error metrics (MAE, RMSE)
* Better handling of seasonality
* Built-in uncertainty estimation
* Less manual tuning required

---

## 📈 Key Features

* ✔ Time series preprocessing pipeline
* ✔ Stationarity testing (ADF Test)
* ✔ Prophet forecasting with confidence intervals
* ✔ SARIMA baseline model
* ✔ Hyperparameter tuning for both models
* ✔ Walk-forward validation
* ✔ Prediction interval coverage
* ✔ 24-hour future forecasting
* ✔ Anomaly detection (stretch goal)

---

## 📉 Prediction Interval Coverage

The Prophet model achieved strong coverage, indicating reliable uncertainty estimation:

* **Coverage ≈ 87%**

---

## 🔍 Anomaly Detection

Anomaly detection was implemented using statistical thresholds on residuals to identify unusual energy consumption patterns.

---

## ⚠️ Limitations

* External factors (e.g., weather, holidays) were not included
* SARIMA tuning was limited due to computational constraints
* MAPE can be unstable due to near-zero values in the dataset
* Long-term forecasts may be less accurate

---

## 🚀 Future Improvements

* Incorporate external regressors (weather, holidays)
* Deploy model as an API or dashboard
* Explore deep learning models (LSTM, TCN)
* Build ensemble models combining Prophet and SARIMA

---

## 📁 Project Structure

```
data/
│
├── raw/
│   └── individual+household+electric+power+consumption.rar
├── processed/
│   └── energy_hourly.csv
│
notebooks/
├── 01_eda.ipynb
├── 02_preprocessing.ipynb
├── 03_decomposition.ipynb
├── 04_prophet_model.ipynb
├── 05_sarima_model.ipynb
├── 06_evaluation.ipynb
├── 07_anomaly_detection.ipynb
└── Final_Energy_Forecasting.ipynb
│
requirements.txt
README.md
```

---

## ⚙️ Installation

### 1. Clone Repository

```
git clone https://github.com/AaronShajan1097/energy-consumption-forecasting-timeseries.git
cd energy-consumption-forecasting-timeseries
```

### 2. Create Virtual Environment (Recommended)

```
python -m venv venv
venv\Scripts\activate   # Windows
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

---

## ▶️ Usage

### Run notebooks:

```
notebooks/Final_Energy_Forecasting.ipynb
```

Or open the Colab notebook:

👉 **Colab Link:** *(https://colab.research.google.com/drive/1ibOfD6QU9dqHFQEISK25x6ydBFzjE9Dl?usp=sharing)*

---

## 🎥 Demo Video

👉 **YouTube (Unlisted):** *(Add your link here)*

---

## 📌 Submission Links

* **GitHub Repository:** *(https://github.com/AaronShajan1097/energy-consumption-forecasting-timeseries.git)*
* **Colab Notebook:** *(https://colab.research.google.com/drive/1ibOfD6QU9dqHFQEISK25x6ydBFzjE9Dl?usp=sharing)*
* **YouTube Video:** *(Add your link here)*

---

## 📊 Business Impact

Accurate energy forecasting enables:

* Efficient energy distribution
* Cost reduction
* Demand planning
* Sustainable energy usage

---

## ✅ Conclusion

This project demonstrates a complete end-to-end time series forecasting pipeline.

The Prophet model proved to be the most effective due to its ability to capture seasonality, provide uncertainty estimates, and deliver accurate predictions with minimal tuning.

---

## 👨‍💻 Author

**Aaron Shajan**
AI/ML Engineer