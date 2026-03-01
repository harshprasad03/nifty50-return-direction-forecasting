📊 NIFTY 50 Return Direction Forecasting
MSc Financial Analytics Case Study
📌 Project Overview

This project investigates whether next-day NIFTY 50 index direction can be predicted using technical indicators and machine learning models.

The objective is not only to build predictive models, but to evaluate whether such models generate economically meaningful trading strategies after risk adjustment.

The study follows a structured financial analytics workflow:

Data Collection

Feature Engineering

Model Comparison & Selection

Financial Strategy Evaluation

🎯 Research Question

Can daily technical indicators and lagged return features provide predictive power for next-day NIFTY 50 return direction?

📂 Project Structure
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
📈 Methodology
1️⃣ Data Collection

Historical NIFTY 50 index data

Cleaning and formatting

Log return computation

Stationarity testing (ADF test)

2️⃣ Feature Engineering

Technical indicators constructed include:

Simple Moving Averages (SMA 10, 20, 50)

Exponential Moving Average (EMA 10)

Volatility measures (rolling standard deviation)

Relative Strength Index (RSI)

Lagged returns (1, 2, 3 days)

Volume change features

All features were engineered using past information only to prevent data leakage.

3️⃣ Modeling

Models evaluated:

Logistic Regression (linear benchmark)

Random Forest (nonlinear ensemble)

Key modeling principles:

Chronological train-test split (80/20)

Baseline comparison (majority class)

Feature scaling where appropriate

Overfitting analysis

ROC-AUC evaluation

Feature importance analysis

The final selected model was Logistic Regression, based on generalization stability.

4️⃣ Strategy Evaluation

Model predictions were converted into a trading strategy:

Long position when model predicts upward movement

No position otherwise

Performance metrics evaluated:

Cumulative returns

Sharpe ratio

Volatility

Maximum drawdown

Comparison against Buy & Hold

Transaction costs were discussed conceptually.

📊 Key Findings

Model accuracy was close to baseline.

Random Forest exhibited overfitting.

Logistic Regression demonstrated stable but weak predictive power.

Strategy performance was comparable to Buy & Hold.

Results are consistent with weak-form market efficiency.

Daily index-level forecasting remains challenging due to high noise and limited exploitable signal.

⚠️ Limitations

Transaction costs not explicitly modeled

Only daily frequency considered

No hyperparameter optimization

No regime-based modeling

🔮 Future Improvements

Incorporate macroeconomic variables

Use higher-frequency data

Apply walk-forward validation

Explore ensemble stacking methods

Include transaction cost simulation

🧠 Academic Contribution

This project demonstrates:

Proper time-series modeling discipline

Financially grounded evaluation

Risk-adjusted performance analysis

Realistic interpretation of predictive limits

🛠 Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Statsmodels

👨‍🎓 Author

Harsh Prasad
MSc Data Science – Financial Analytics Case Study
