# Task 3: Energy Consumption Time Series Forecasting  

---

## Overview  
This repository contains the solution for **Task 3: Energy Consumption Time Series Forecasting**, completed as part of my AI & Data Science Internship tasks.

---

## Objective  
The objective of this task is to forecast short-term household electricity consumption using historical time-series data.  
The task focuses on understanding temporal patterns and comparing statistical and machine learning forecasting models.

---

## Dataset  
**Dataset Name:** Household Power Consumption Dataset  
**Type:** Time Series Dataset (minute-level recordings)

---

## Dataset Description  
**Total Records:** ~2 Million time entries  
**Target Variable:** `Global_active_power` (household energy consumption)

### Features:
**Time Information**
- Date
- Time

**Electrical Measurements**
- Global_reactive_power
- Voltage
- Global_intensity

**Appliance Usage**
- Sub_metering_1
- Sub_metering_2
- Sub_metering_3

The dataset contains chronological electricity usage readings, requiring datetime parsing, resampling, and temporal feature engineering before forecasting.

---

## Tools & Technologies Used
- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- statsmodels (ARIMA)
- Prophet
- XGBoost
- Scikit-learn
- Jupyter Notebook / Google Colab

---

## Approach  

### 1️⃣ Data Loading
- Loaded dataset using `pandas.read_csv()`
- Combined Date and Time columns into a datetime index

### 2️⃣ Data Cleaning
- Replaced missing values (`?`) with NaN
- Converted columns to numeric format
- Filled missing values using forward fill method

### 3️⃣ Time Series Processing
- Resampled minute data into **hourly averages**
- Prepared data for time-based analysis and modeling

### 4️⃣ Feature Engineering
Created temporal features:
- Hour of day
- Day of week
- Month
- Weekend indicator

### 5️⃣ Exploratory Data Analysis (EDA)
- Plotted energy consumption over time
- Analyzed daily usage trends
- Observed repeating usage patterns

### 6️⃣ Model Training & Testing
Three forecasting models were implemented:

**ARIMA**
- Statistical model using past values and errors

**Prophet**
- Decomposition model capturing trend and seasonality

**XGBoost**
- Machine learning model using engineered time features

### 7️⃣ Model Evaluation
Models evaluated using:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Square Error)

---

## Results & Insights
- ARIMA captured historical patterns but struggled with sudden fluctuations
- Prophet handled seasonal patterns better than ARIMA
- XGBoost achieved the lowest error due to time-based feature learning
- Energy consumption shows strong hourly and weekly behavior patterns

---

## Conclusion
This task demonstrates a complete time-series forecasting workflow including preprocessing, feature engineering, model comparison, and visualization.  
Machine learning models like XGBoost performed best because they learn behavioral patterns rather than relying only on past values.

---

## Skills Gained
- Time series forecasting
- Temporal feature engineering
- Model comparison (Statistical vs ML)
- Forecast evaluation (MAE, RMSE)
- Data visualization for time series analysis
