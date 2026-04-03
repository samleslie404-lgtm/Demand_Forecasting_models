# Demand Forecasting & Supply Chain Analytics

## Overview

This project focuses on building an end-to-end demand forecasting pipeline using a large-scale dataset (1M+ records) across multiple product categories, warehouses, and time periods. 
The goal is to generate accurate demand forecasts and uncover insights to support inventory planning and supply chain decision-making.

---

## Business Problem

The company operates globally with long production and shipping lead times. This creates a gap between production decisions and actual demand fulfillment. 
Accurate short-term demand forecasting is critical to:

* Reduce stockouts
* Avoid excess inventory
* Improve supply chain efficiency

---

## Dataset

* ~1,000,000+ records (after cleaning)
* 2,157 products
* 33 product categories
* 4 warehouses (Brampton, Oshawa, Surrey, St John’s)
* Time range: 2015–2019

---

## Data Pipeline

The project follows a structured pipeline:

1. Data Cleaning

   * Removed missing dates and negative demand values
   * Converted date fields to datetime

2. Data Transformation

   * Aggregated demand to monthly level
   * Filtered relevant time periods

3. Exploratory Data Analysis (EDA)

   * Demand distribution by category and warehouse
   * Time series trends and seasonality
   * Product-level variability analysis

4. Anomaly Handling

   * Identified a major demand drop in January 2019
   * Tested removal and imputation strategies

5. Data Modelling
   * Tested multiple machine learning algorithms to forecast demand
   * Review results using error calculations

---

## Key Insights

* **Demand concentration in product category:** One product category accounts for ~84% of total demand
* **Warehouse imbalance:** Brampton handles ~66% of demand
* **Demand variability in products:** Significant fluctuations at the product level
* **Anomaly impact:** Handling a single anomaly improved model accuracy by ~50%

---

## Modeling Approach

Implemented and compared multiple forecasting models:

* Naive
* Moving Average (MA)
* Weighted Moving Average (WMA)
* Simple Exponential Smoothing (SES)

### Best Model

* **Weighted Moving Average (3-month window)**
* Achieved lowest RMSE (~6.49M)

---

## Results

* RMSE improved by ~50% after data cleaning and anomaly handling
* Simple models outperformed more complex approaches
* Data quality had a larger impact than model complexity

---

## Key Takeaways

* Data cleaning is critical for accurate forecasting
* Simple, interpretable models can be highly effective
* Analytics is not just modeling - it is about asking the right questions
* Business insights come from understanding patterns, not just predictions

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook

---

## Future Improvements

* Implement ARIMA / SARIMA models
* Explore machine learning approaches (e.g., XGBoost)
* Incorporate external data (market trends, seasonality drivers)
* Build automated forecasting pipelines

---

## Authors

Sam Leslie
Banshi Keshwala
Labdhi Zatakia
Yash Pratap Singh
Mohit Dabas
