# BigMart Sales Prediction

## Overview

This project aims to predict sales for BigMart outlets using machine learning techniques. The dataset consists of sales data for 1559 products across 10 stores from 2013, along with various product and store attributes.

By analyzing this data, we aim to identify key factors influencing sales and build a predictive model to estimate sales for new data points.

## Problem Statement

BigMart wants to understand the relationship between product attributes, store features, and sales. The goal is to develop a machine learning model that can predict sales for different products at various outlets.

## Dataset

The dataset consists of two files:

Train Data (8523 records): Includes sales figures (target variable).

Test Data (5681 records): No sales data; the model will predict sales for these instances.

The dataset includes:

Product-related features: Item type, item weight, MRP, visibility, etc.

Store-related features: Outlet size, outlet location, outlet type, and establishment year.

## Data Challenges

Missing values due to reporting errors.

Categorical variables requiring encoding.

Feature scaling needed for numerical variables.

Approach

1️⃣ Data Preprocessing

Handling missing values (e.g., mean imputation for numerical data).

One-hot encoding for categorical features.

Feature engineering (e.g., creating an "Outlet Age" feature).

Standardization of numerical features.

2️⃣ Model Training & Evaluation

Multiple models were trained and evaluated:

Linear Regression

Decision Tree

Random Forest

XGBoost (Best Performing Model)

Evaluation Metrics Used:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² Score

3️⃣ Model Deployment

The final XGBoost model was saved using joblib for future predictions.

Predictions on test data were saved as test_predictions.csv.


Installation & Usage

1️⃣ Clone the Repository

git clone https://github.com/kinkiniM/BigMart-Sales-Prediction.git
cd BigMart-Sales-Prediction

2️⃣ Install Dependencies

pip install -r requirements.txt

3️⃣ Run the Prediction Script

Ensure the trained model is available in the directory (xgboost_model.pkl).

python predict.py

This will generate test_predictions.csv containing predicted sales values.

Future Improvements

Hyperparameter tuning for better performance.

Feature selection techniques to reduce complexity.

Deploying the model using Flask or FastAPI.

Contributors

Kinkini Majumdar
