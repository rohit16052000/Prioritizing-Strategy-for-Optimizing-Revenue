# E-Commerce Revenue Optimization using OLS Regression

Identifies key drivers of annual customer spending for an e-commerce company to prioritize investment between mobile app and website development.

## Problem Statement

An NYC-based clothing e-commerce company wanted to decide whether to focus development efforts on their mobile app or website. This project builds a multivariate OLS regression model to quantify the impact of each customer touchpoint on yearly revenue.

## Dataset

- Source: Ecommerce Customers dataset
- Records: 486 (after dropping nulls from 500)
- Features: Avg. Session Length, Time on App, Time on Website, Length of Membership
- Target: Yearly Amount Spent (USD)

## Approach

- EDA with jointplots, pairplots, and lmplots to explore feature correlations
- Null value removal and Winsorization (5%) to handle outliers in Yearly Amount Spent
- OLS regression (Statsmodels) with all 4 features — R² = 0.945
- Dropped Time on Website (p-value = 0.737, statistically insignificant)
- Final model with 3 features — Adj. R² = 0.945
- Residual analysis: normally distributed residuals, Durbin-Watson = 2.081

## Results

- Adj. R²: 0.945 | MAE: 12.10 | RMSE: 18.69
- Length of Membership has the highest impact (+$52.87 per year)
- Time on App drives +$33.50 per year vs. Time on Website (non-significant)
- Business recommendation: prioritize mobile app development over website

## Tech Stack

- Python, Pandas, NumPy, Scikit-learn, Statsmodels, SciPy
- Matplotlib, Seaborn

## Files

- `Linear regression Ecommerce.ipynb` — Full pipeline: EDA, preprocessing, OLS modeling, evaluation, and business interpretation
- `Ecommerce Customers.csv` — Dataset
