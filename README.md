# public-utility-company-regression-model
# Hotzel Steam Revenue Prediction with Linear Regression

## Overview

This project demonstrates how to build and evaluate simple linear regression models in Python using historical business data from Hotzel Steam. The objective is to predict monthly revenue using different independent variables and compare each model's forecasting performance.

The analysis was completed in Google Colab using the **pandas**, **NumPy**, **Matplotlib**, and **Statsmodels** libraries.

---

## Project Objectives

- Import and prepare historical operational data.
- Explore relationships between variables using correlation analysis.
- Split the dataset into training and testing datasets.
- Build multiple Ordinary Least Squares (OLS) regression models.
- Evaluate model accuracy using Mean Absolute Percentage Error (MAPE).
- Visualize actual versus predicted revenue.

---

## Dataset

The dataset contains **48 monthly observations** with the following variables:

| Variable | Description |
|----------|-------------|
| `type` | Indicates whether a record belongs to the training or testing dataset |
| `date` | Monthly observation date |
| `revenue` | Monthly revenue (dependent variable) |
| `production` | Monthly production volume |
| `coolDD` | Cooling Degree Days |
| `heatDD` | Heating Degree Days |

The first 36 observations are used for model training, while the remaining 12 observations are reserved for testing.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Statsmodels

---

## Data Preparation

Before modeling, the following preprocessing steps were completed:

- Imported required Python libraries.
- Loaded the CSV dataset.
- Converted the `date` column to datetime format.
- Disabled scientific notation for readability.
- Examined dataset structure using `.info()`.
- Calculated correlations between quantitative variables.
- Split data into training and testing datasets.

---

## Regression Models

### Model 1: Revenue vs. Production

This model predicts revenue using production volume as the independent variable.

#### Process

- Define revenue as the dependent variable.
- Define production as the predictor.
- Add an intercept (constant).
- Train an OLS regression model.
- Generate predictions on the testing dataset.
- Calculate prediction error using MAPE.
- Plot actual versus predicted revenue.

#### Results

- **Predictor:** Production
- **Evaluation Metric:** Mean Absolute Percentage Error (MAPE)
- **Test MAPE:** **25.4%**

---

### Model 2: Revenue vs. Heating Degree Days

The second regression model predicts revenue using Heating Degree Days (`heatDD`).

The same workflow is repeated:

- Prepare variables.
- Train the regression model.
- Predict testing observations.
- Calculate MAPE.
- Compare performance with Model 1.

---

## Model Evaluation

Model performance is evaluated using **Mean Absolute Percentage Error (MAPE)**.

\[
MAPE = \frac{1}{n}\sum \left|\frac{Actual - Predicted}{Actual}\right|
\]

Lower MAPE values indicate more accurate predictions.

---

## Visualization

The project includes line charts comparing:

- Actual monthly revenue
- Predicted monthly revenue

These visualizations help assess how closely each regression model tracks real business performance.

---

## Learning Outcomes

This project demonstrates practical applications of:

- Data preprocessing
- Exploratory data analysis
- Correlation analysis
- Simple linear regression
- Ordinary Least Squares (OLS)
- Model testing and validation
- Forecast accuracy measurement using MAPE
- Data visualization

---

## Repository Structure

```text
.
├── AICPA_regressionAnalysisData.csv
├── regression_analysis.ipynb
├── README.md
└── images/
    └── revenue_prediction.png
```

*File names may vary depending on your project organization.*

---

## Future Improvements

Potential enhancements include:

- Build a multiple linear regression model using several predictors.
- Engineer additional features such as seasonality indicators.
- Perform cross-validation for stronger model validation.
- Compare regression performance with machine learning models such as Random Forest and XGBoost.
- Evaluate additional performance metrics including RMSE and MAE.

---

## Author

**Seana Maennling**

Academic project completed for **AFM 244**, demonstrating regression analysis and predictive modeling using Python.
