# Demand Forecasting for Retail Stores

## Overview
This project focuses on forecasting weekly sales for retail stores using advanced machine learning techniques. The objective is to build a predictive model that minimizes the Weighted Mean Absolute Error (WMAE), placing higher importance on accurate forecasts during major holidays and sales events.

The project involves end-to-end development including Exploratory Data Analysis (EDA), feature engineering, model training, hyperparameter tuning, and evaluation on business-relevant metrics.

## Problem Statement
Retail sales data is highly influenced by factors such as holidays, promotions, store characteristics, and economic indicators. The challenge is to accurately predict weekly sales for each store and department, taking into account seasonality and event-driven demand spikes.

## Dataset
The dataset consists of:
- Store attributes: Store ID, Store Type, Size
- Weekly Sales: Store, Department, Date, Weekly Sales, IsHoliday
- Economic Indicators: Temperature, Fuel Price, CPI, Unemployment
- Holiday Calendar: Super Bowl, Labor Day, Thanksgiving, Christmas

## Approach

### Exploratory Data Analysis (EDA)
- Analyzed overall sales trends and seasonality patterns.
- Identified sales spikes around major holidays.
- Visualized sales distribution by store type and size.
- Detected and analyzed outliers using the IQR method.

### Feature Engineering
- Created lag features (1-week, 2-week, 3-week sales lags) to capture sales momentum.
- Engineered rolling mean features (3-week moving averages) to smooth weekly fluctuations.
- Added proximity to holidays feature (days until next major holiday).
- Mapped holidays to specific event types (e.g., Thanksgiving, Christmas).
- Clustered stores based on size, average sales, and macroeconomic variables.
- Encoded categorical variables (Store Type, Department) for model compatibility.

### Modeling and Evaluation
- Built a baseline model using previous week's sales.
- Trained Random Forest Regressor and XGBoost Regressor for prediction.
- Performed hyperparameter tuning to optimize XGBoost performance.
- Evaluated model performance using WMAE to prioritize business-critical weeks.
- Achieved WMAE reduction from 1806 to 1417 by engineering lag and rolling features.

## Results
- Achieved a 22% reduction in WMAE through iterative feature engineering and model tuning.
- Successfully modeled sales spikes during major holidays.
- Developed a robust predictive pipeline capable of generalizing across different store types and departments.

## Future Improvements
- Experiment with model ensembles (XGBoost, LightGBM, Random Forest).
- Develop specialized models for different store clusters.
- Add additional time-based features such as week of year and end-of-month flags.
- Incorporate promotional markdown data to enhance demand sensitivity modeling.

## Business Impact
Accurate demand forecasting enables better inventory management, optimized staffing, and improved supply chain operations. It allows retailers to prepare for high-demand periods, reduce stockouts, and improve overall profitability.

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn, XGBoost
- Matplotlib, Seaborn
- Jupyter No
