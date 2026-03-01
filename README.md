# 📊 NIFTY 50 Return Direction Forecasting

### MSc Financial Analytics Case Study

---

## 📌 Project Overview

This project investigates whether next-day **NIFTY 50 index direction** can be predicted using technical indicators and machine learning models.

The objective is not only to build predictive models, but to evaluate whether such models generate **economically meaningful trading strategies after risk adjustment**.

The study follows a structured financial analytics workflow:

* Data Collection
* Feature Engineering
* Model Comparison & Selection
* Financial Strategy Evaluation

---

## 🎯 Research Question

> Can daily technical indicators and lagged return features provide predictive power for next-day NIFTY 50 return direction?

---

## 📂 Project Structure

```
financial_analytics_casestudy/
│
├── data/
│   ├── nifty50_raw_cleaned.csv
│   ├── nifty50_features.csv
│   └── evaluation_data.csv
│
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_modeling.ipynb
│   └── 04_evaluation.ipynb
│
├── report/
│
└── README.md
```

---

## 📈 Methodology

### 1️⃣ Data Collection

* Historical NIFTY 50 index data
* Data cleaning and formatting
* Log return computation
* Stationarity testing using the Augmented Dickey-Fuller (ADF) test

---

### 2️⃣ Feature Engineering

The following technical indicators were constructed:

* Simple Moving Averages (SMA 10, 20, 50)
* Exponential Moving Average (EMA 10)
* Rolling Volatility (10-day, 20-day)
* Relative Strength Index (RSI)
* Lagged Returns (1, 2, 3 days)
* Volume Change and Volume-based features

All features were engineered using **past information only** to prevent data leakage.

---

### 3️⃣ Modeling

**Models Evaluated:**

* Logistic Regression (Linear Benchmark)
* Random Forest (Nonlinear Ensemble Model)

**Modeling Principles:**

* Chronological Train-Test Split (80% / 20%)
* Baseline Comparison (Majority Class)
* Feature Scaling where required
* Overfitting Analysis
* ROC-AUC Evaluation
* Feature Importance Analysis

The final selected model was **Logistic Regression**, based on generalization stability and interpretability.

---

### 4️⃣ Strategy Evaluation

Model predictions were converted into a trading strategy:

* 📈 Long position when the model predicts an upward movement
* 🚫 No position otherwise

**Performance Metrics Evaluated:**

* Cumulative Returns
* Sharpe Ratio
* Volatility
* Maximum Drawdown
* Comparison against Buy & Hold

Transaction costs were discussed conceptually as a practical limitation.

---

## 📊 Key Findings

* Model accuracy was close to baseline performance.
* Random Forest exhibited signs of overfitting.
* Logistic Regression demonstrated stable but weak predictive power.
* Strategy performance was comparable to Buy & Hold.
* Results are consistent with **weak-form market efficiency**.

Daily index-level forecasting remains challenging due to high noise and limited exploitable signal.

---

## ⚠️ Limitations

* Transaction costs not explicitly modeled
* Only daily frequency considered
* No hyperparameter optimization performed
* No regime-based or macroeconomic modeling included

---

## 🔮 Future Improvements

* Incorporate macroeconomic indicators
* Use higher-frequency intraday data
* Apply walk-forward validation
* Explore ensemble stacking techniques
* Explicitly model transaction costs

---

## 🧠 Academic Contribution

This project demonstrates:

* Proper time-series modeling discipline
* Financially grounded evaluation
* Risk-adjusted performance analysis
* Realistic interpretation of predictive limits

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Statsmodels

---

## 👨‍🎓 Author

**Harsh Prasad**
MSc Data Science – Financial Analytics Case Study

---
