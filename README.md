# Care-Research_household-occupancy-prediction
"A project to predict whether a household is single or multiple occupancy using motion sensor data. Includes data preprocessing, model training with XGBoost, and evaluation using accuracy and F1 score."

**Project Overview**

project aims to predict whether a household is single or multiple occupancy using motion sensor data. This involves:

1.Loading and cleaning the data.

2.Merging sensor data with occupancy labels.

3.Preprocessing and feature engineering.

4.Building and evaluating a predictive model.

**Details of what have been done can be found on the notebook**


**Python Libraries Used:**

**1. pandas** – For data manipulation, loading, and cleaning CSV files (import pandas as pd).

**2. scikit-learn (sklearn)** – For preprocessing, model evaluation, cross-validation, and hyperparameter tuning:


1.KFold, GridSearchCV for cross-validation and hyperparameter tuning.

2.MinMaxScaler for normalizing data.

3.f1_score for evaluating model performance.


**3. xgboost** – For building and training the XGBoost model, which is an ensemble learning algorithm based on gradient boosting (import xgboost as xgb).

**4. shap** – For SHAP (SHapley Additive exPlanations) analysis, which explains the output of machine learning models by quantifying feature contributions (import shap).

**5. numpy** – For numerical operations such as concatenating arrays and handling matrices (import numpy as np).



**Explanation of the Machine Learning Model and Steps:**
The project uses **XGBoost**, a gradient-boosting ensemble method for **classification**, which belongs to the class of **supervised learning**. Specifically, it is used to predict household occupancy (single or multiple) based on motion sensor data. The model goes through the following key steps:

**1. Data Preprocessing:** The raw motion sensor data is cleaned and processed by extracting relevant features such as time-based features (hour, day of the week), and the data is normalized using MinMaxScaler.

**2. Cross-Validation:** The data is split using KFold cross-validation to ensure the model is robust. In each fold, the training and testing data are separated, and hyperparameter tuning is performed using GridSearchCV to find the best model configuration.

**3. Model Training:** The XGBoost model is trained on the balanced and scaled data for each fold, and the best model is chosen based on its performance.

**4. Evaluation:** The model is evaluated using accuracy and F1 scores to measure its effectiveness in predicting occupancy. Both scores help handle a class imbalance in the data.

**5. Model Interpretation:** After training the model, SHAP is used to interpret the predictions by calculating feature contributions. SHAP provides both individual-level explanations (waterfall plots) and global feature importance (summary plots), giving insights into how specific features influence predictions.

