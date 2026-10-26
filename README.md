# FMCG Demand Forecasting and Inventory Optimization

## Authors : Diya Tilwani & Twinkle Chauhan
## StudentIDs : 202618011 & 202618049

## 1. Project Overview

This project aims to develop a Machine Learning-based system for demand forecasting and inventory optimization in the Fast-Moving Consumer Goods (FMCG) domain.

The system will analyze historical retail sales data, identify demand patterns, predict future product demand, and generate inventory replenishment recommendations. The overall goal is to support better inventory decisions, reduce potential stockouts, and avoid unnecessary excess inventory.

**Project Status:** Initial dataset inspection and planning.

## 2. Problem Statement

Retailers must maintain sufficient inventory to meet customer demand while minimizing excess stock and inventory-related costs.

Traditional inventory decisions based only on intuition or historical averages may not account for demand patterns, discounts, holidays, weather conditions, and stock availability.

This project will investigate how Machine Learning-based demand forecasting, combined with inventory management techniques, can support more informed replenishment decisions.

## 3. Dataset

**Dataset name:** FreshRetail-Net50k

**Dataset source:** [Dataset reference](https://share.google/2rJLsjpAsgnZyVzNd)

The downloaded data is currently available in two files:

- `dashboard_clean_15k.csv`
- `train_batched.csv`

The preliminary inspection of `dashboard_clean_15k.csv` showed 20,000 records and 21 columns. The training file preview showed 19 columns, including product and store identifiers, dates, sales, discounts, weather variables, and stock-related information.

These files have not yet been confirmed as compatible or non-overlapping. Their schemas, record counts, and relationship will be investigated before combining or selecting records.

### Potentially Useful Features

- Store and product identifiers
- Product category identifiers
- Date (`dt`)
- Recorded sales (`sale_amount`)
- Discount
- Holiday and activity flags
- Precipitation
- Average temperature
- Average humidity
- Average wind level
- Stockout and stock availability information

The exact meaning of the sales variable and the suitability of each feature will be verified before model development.

## 4. Project Objectives

1. Understand and assess the quality of the available dataset.
2. Select an appropriate working dataset of approximately 20,000–25,000 records, if supported by the data structure.
3. Perform Exploratory Data Analysis (EDA) to identify demand patterns and data-quality issues.
4. Engineer relevant temporal, lag, and rolling statistical features.
5. Develop and compare suitable demand forecasting models.
6. Tune model hyperparameters using time-aware validation.
7. Evaluate forecasting performance using appropriate error metrics.
8. Apply inventory management techniques to estimate safety stock, reorder points, and replenishment quantities.
9. Develop a Streamlit dashboard to present forecasts and inventory recommendations.
10. Document the methodology, assumptions, limitations, and results for the final evaluation.

## 5. Planned Project Workflow

1. Dataset loading and structural inspection
2. Data quality assessment
3. Data cleaning and record selection
4. Exploratory Data Analysis and visualization
5. Time-series preparation and feature engineering
6. Chronological training, validation, and testing
7. Baseline forecasting
8. Machine Learning model development
9. Hyperparameter tuning
10. Model evaluation and comparison
11. Inventory optimization
12. Streamlit dashboard development
13. Documentation and Chalk Talk preparation

## 6. Planned Exploratory Data Analysis

The following visualizations will be considered based on the actual dataset:

- Sales distribution to understand variability and skewness
- Sales trends over time to investigate changes in demand
- Monthly or weekly demand patterns to explore seasonality
- Product-wise sales comparisons to identify high-demand products
- Box plots to investigate unusual observations
- Correlation analysis to examine relationships among numerical variables
- Stockout analysis to investigate possible supply constraints

Each visualization will include its purpose, observations, and interpretation. Graphs will be selected based on their relevance rather than included solely for quantity.

## 7. Planned Machine Learning Methodology

Potential forecasting approaches include:

- Naive forecasting baseline
- Linear Regression
- Random Forest Regressor
- Gradient Boosting or XGBoost, if suitable

The final model selection will depend on dataset suitability and validation performance.

Feature engineering may include:

- Calendar features
- Lagged demand
- Rolling averages
- Rolling demand variability
- Discount and weather features, where appropriate

A chronological evaluation strategy will be used to prevent future information from leaking into model training.

## 8. Model Evaluation

Potential evaluation metrics include:

- **MAE:** Mean Absolute Error
- **RMSE:** Root Mean Squared Error
- **WAPE:** Weighted Absolute Percentage Error
- **MAPE:** Mean Absolute Percentage Error, where suitable

Models will be compared using consistent evaluation periods. Hyperparameter tuning will use training and validation data, while the final test set will remain separate for an unbiased performance assessment.

## 9. Inventory Optimization

Forecasted demand will be connected to inventory management calculations, potentially including:

- Lead-time demand
- Safety stock
- Reorder point
- Replenishment quantity
- Stockout risk and excess inventory scenarios

Inventory calculations will clearly state their assumptions. If current stock, supplier lead time, service-level requirements, or inventory costs are unavailable, configurable assumptions or scenarios will be used instead of treating those values as observed data.

## 10. Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook or VS Code
- Streamlit
- Git and GitHub

Additional libraries may be introduced if required by the final methodology.

## 11. Expected Deliverables

- Documented and prepared dataset
- EDA notebook with explanations and visualizations
- Feature-engineering pipeline
- Trained and evaluated forecasting models
- Hyperparameter tuning results
- Inventory optimization module
- Interactive Streamlit dashboard
- Project README and methodology documentation
- Final evaluation and Chalk Talk preparation material

## 12. Current Limitations and Pending Decisions

- Confirm the relationship between the two downloaded files.
- Verify the meaning and units of `sale_amount`.
- Determine the appropriate forecasting granularity.
- Investigate stockouts and missing product-date observations.
- Confirm whether external data enrichment is feasible.
- Establish realistic inventory assumptions.
- Finalize model selection based on empirical results.

**Note:** This README is a preliminary project plan. Final methods, model performance, findings, and conclusions will be added only after the corresponding analyses have been completed.