# Multivariate Joint Forecasting: Remittance, Exchange Rate & Inflation (Bangladesh)

Forecasting three interlinked Bangladeshi macroeconomic indicators — **wage remittance inflows**, the **USD/BDT exchange rate**, and **CPI inflation** — using machine learning (XGBoost, LSTM) to capture the cross-variable relationships that univariate models miss.

## Problem Statement

Remittances, exchange rate, and inflation are economically interdependent in Bangladesh: remittances drive foreign currency supply, which affects the exchange rate, which in turn affects import prices and inflation. These are typically forecast in isolation. This project builds a joint, multivariate ML-based forecasting pipeline instead.

## Project Objectives

- Collect and preprocess monthly data for all three indicators from official sources
- Engineer lag, rolling-window, and seasonal/calendar features
- Build and compare ML models (XGBoost, LSTM) for joint forecasting
- Evaluate with RMSE, MAE, MAPE against classical baselines
- Interpret lead-lag relationships between the three series

## Data Sources

| Dataset | Source | Format |
|---|---|---|
| Remittance | [Bangladesh Bank](https://www.bb.org.bd/en/index.php/econdata/wageremitance) | Monthly HTML table |
| USD/BDT Exchange Rate | [Bangladesh Bank](https://www.bb.org.bd/en/index.php/econdata/exchangerate) | Daily, queryable by date range |
| Consumer Price Index (Bangladesh) | [World Bank](https://data.worldbank.org/indicator/FP.CPI.TOTL?locations=BD) | Annual CSV/Excel (supplement with BBS monthly CPI) |

## Repository Structure

```
├── database/
│   ├── bangladesh_macro_indicators_2010_2026.csv
│   ├── bangladesh_monthly_inflation_2010_2026.csv
│   ├── bangladesh_monthly_remittance_2010_2026.csv
│   └── USD_to_BDT_Monthly_Exchange_Rates_2010_2026.csv
├── project/
│   └── Multivariate_Joint_Forecasting.ipynb               
├── report/
│   └── cse427.pdf
└── README.md
```

## Setup

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install pandas numpy matplotlib scikit-learn xgboost tensorflow jupyter
jupyter notebook notebooks/remittance_eda.ipynb
```

## License

This project is for academic purposes.
