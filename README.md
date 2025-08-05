# Demand Forecasting for Retail Stores

## Project Overview

This project focuses on forecasting weekly sales for retail stores using historical sales data. The goal is to build a predictive model that minimizes the **Weighted Mean Absolute Error (WMAE)**, emphasizing accurate predictions during key holidays like Thanksgiving and Christmas.

The project includes:

- Exploratory Data Analysis (EDA)
- Feature Engineering (Lag Variables, Holiday Proximity, K-Means Clustering)
- Model Training & Evaluation using WMAE

---

## Problem Statement

Retail sales are significantly influenced by seasonal trends and holiday events. The challenge is to predict weekly sales at a store-department level while accounting for holiday-driven demand spikes and store-level variations.

---

## Dataset

The dataset includes:

- **Store Information:** Store ID, Store Type, Size
- **Sales Data:** Store, Department, Date, Weekly Sales, IsHoliday
- **Economic Indicators:** Temperature, Fuel Price, CPI, Unemployment

---

## Approach

### 1. Exploratory Data Analysis (EDA)

- Analyzed overall sales trends and holiday effects.
- Visualized sales distributions across store types and departments.
- Identified outliers and seasonal demand patterns.

### 2. Feature Engineering

- Created **Lag Features** (1, 2, 3-week sales lags) to capture recent sales momentum.
- Engineered **Days Until Next Holiday** feature to model holiday proximity effects.
- Applied **K-Means Clustering** to segment stores based on size, average sales, and economic indicators.
- Encoded categorical variables (Store Type, Department) for model input.

### 3. Modeling & Evaluation

- Built a **baseline model** using previous week's sales.
- Trained RandomeForest and XGboost regression models to predict weekly sales.
- Evaluated using **WMAE**, prioritizing accuracy during holiday periods.
- Achieved WMAE reduction from **1806 to 1417** through iterative feature engineering.

---

## Results

- **22% reduction in WMAE** over baseline.
- Successfully captured holiday sales spikes.
- Built a robust prediction pipeline suitable for store-level demand forecasting.

---

## Tech Stack

- Python
  - Pandas, NumPy
  - Scikit-learn
  - Matplotlib, Seaborn
- Jupyter Notebook
