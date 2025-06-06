
# 🧪 Tuberculosis Incidence Forecasting Model

## 📌 Project Overview

This project focuses on the development of a time series forecasting model to predict the **monthly incidence rate of tuberculosis (TB)** in **Guangxi, China**, using historical data from **January 2012 to June 2019**. The model aims to inform public health interventions, resource allocation, and policy planning.

---

## 🎯 Study Objectives

1. **Analyze** historical TB incidence data for temporal trends and seasonal patterns.
2. **Build** a robust ARIMA-based time series forecasting model.
3. **Evaluate** the stationarity and goodness-of-fit of the model.
4. **Forecast** TB incidence for the next 8 years (up to mid-2027).
5. **Provide** actionable insights and recommendations for TB control and prevention strategies.

---

## 📊 Dataset Summary

- **Source**: [Dataset Name Redacted for Confidentiality]
- **Period**: Jan 2012 - Jun 2019
- **Frequency**: Monthly
- **Metric**: TB incidence per 100,000 population

```r
# Sample of the dataset:
| Time       | TB Incidence (per 100,000) |
|------------|-----------------------------|
| 2012-01-31 | 13.0                        |
| 2012-02-29 | 17.1                        |
| 2012-03-31 | 20.2                        |
```

---

## 🧠 Methodology

### 1. 📈 Time Series Visualization
- Initial plots revealed **seasonal fluctuations** and **general downward trend** in TB incidence.
- Seasonality identified via decomposition and monthly aggregation.

### 2. 📉 Stationarity Checks
- **ADF Test**: p = 0.333 ➝ Not stationary  
- **KPSS Test**: p = 0.01 ➝ Not stationary  
- Differencing required to stabilize mean and variance.

### 3. 🔁 Model Development
- Used `auto.arima()` for optimal model selection.
- Final model: `ARIMA(0,0,1)(0,1,1)[12] with drift`
- Evaluated via AIC, BIC, RMSE, and MAPE.

### 4. ✅ Model Diagnostics
- Residuals: Normally distributed, uncorrelated.
- **Ljung-Box Test**: p = 0.9997 ➝ Model residuals are white noise.

### 5. 🔮 Forecasting
- Forecast horizon: **96 months** (8 years).
- Visualized with `forecast` and `ggplot2`.

---

## 📉 Forecast Highlights

- Projected continued **decline** in TB incidence.
- Seasonal pattern remains consistent over time.
- Lower confidence intervals suggest possible significant reduction if trends persist.

---

## 📌 Recommendations

1. **Public Health Focus**: Leverage predictions to target TB control campaigns during seasonal peaks.
2. **Resource Allocation**: Shift funding and medical resources towards high-risk months/years.
3. **Policy Planning**: Align national TB strategy with long-term forecasts.
4. **Ongoing Monitoring**: Continuously update the model with fresh data for improved accuracy.

---

## 🧰 Key Libraries Used

```r
library(forecast)
library(tseries)
library(ggplot2)
library(readxl)
```

---

## 📁 Repository Structure

```
├── TB-Incidence-Forecasting-Model.pdf
├── README.md
├── data/
│   └── 12879_2020_5033_MOESM1_ESM.xlsx
├── scripts/
│   └── tb_forecasting_model.R
```

---

## 👤 Author

**Enock Bereka**  
*Data Science Enthusiast | Time Series Analyst*  
📅 January 26, 2025

---

## 📬 Contact & Collaboration

For feedback or collaboration, feel free to reach out via [LinkedIn](https://linkedin.com) or email.

---

## 📝 License

This project is for educational and research purposes. Please cite appropriately when using insights or code from this work.
