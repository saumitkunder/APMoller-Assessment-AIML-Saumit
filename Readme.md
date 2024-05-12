# SAUMIT-AIML-ASSESSMENT
## TASK
Every row represents the sourcing of one unit of a particular product combination.
A unique product combination comprises of attributes mentioned in Columns A,B,C,D,E,F
Since each row represents 1 unit of sourcing; therefore, you will find multiple rows with the same combination in the training dataset. Imagine buying 1 quantity being represented as a single row.
July 20 to May 21 is your training set and June 21 is your test set; So using the 11 months data (Training Set: June 2020 to May 2021) you'd have the forecast / predict the June 2021 number (Test Set)
June 2021 has only a single value for each combination as that is your test set (target).
Hint: You may need to download this dataset to work  upon it.

Iterate on ML models to come up closest to the Test set data using the Training Set Data.

Understand the data set (even with the open questions you have)
Do Exploratory Data Analysis.
Use Python and it's libraries for all your development needs.
Have a strategy for handling outliers / poor data quality on some rows.
Come up with approaches for forecasting the June 21 test set.
Compare and explain the different approaches you might have considered. (In your notebook)
Explain the final approach you have taken and why.
## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Data](#data)
4. [Models](#models)
5. [Evaluation](#evaluation)


## Introduction

This project aims to forecast the sourcing quantity or cost of various products based on historical data. By leveraging machine learning algorithms and exploratory data analysis techniques, we seek to identify patterns and trends in sourcing behavior, enabling more accurate predictions for future procurement needs. Through this project, we aim to optimize inventory management and procurement strategies, ultimately improving operational efficiency and cost-effectiveness.

## Features

Data preprocessing: The project involves preprocessing raw data, handling missing values, encoding categorical variables, and feature engineering to prepare the dataset for machine learning models.
Exploratory Data Analysis (EDA): Conducting EDA to gain insights into the dataset, including visualizations to understand the distribution of variables, relationships between features, and identifying patterns.
Model Training: Training machine learning models such as Random Forest and Gradient Boosting Regressors to forecast sourcing quantity or cost based on historical data.
Model Evaluation: Evaluating the performance of trained models using metrics like Mean Squared Error (MSE), Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R2) score to assess predictive accuracy.
Visualization: Generating visualizations like histograms, box plots, and heatmaps to visualize data distributions, correlations, and model performance.
Feature Importance: Identifying important features contributing to sourcing quantity or cost predictions using techniques like feature importance scores.

## Data

The dataset used in this project contains information related to product sourcing. It provides insights into various attributes of the products sourced by AP Moller company.

### Dataset Contents

The dataset includes the following key features:

- **Manufacturer:** The manufacturer of the product.
- **Area Code:** The area code associated with the sourcing location.
- **Sourcing Channel:** The channel through which the product was sourced (e.g., wholesale, direct).
- **Product Size:** The size of the product (e.g., large, small).
- **Product Type:** The type or category of the product.
- **Month of Sourcing:** The date when the product was sourced.
- **Sourcing Cost:** The cost associated with sourcing the product.

### Source

The dataset was obtained directly from AP Moller company. Unfortunately, we don't have a link to share as it's proprietary data.

### Format

The dataset is provided in Excel format (.xlsx).

### Preprocessing

Before using the dataset in the project, the following preprocessing steps were applied:

- The 'Month of Sourcing' column was converted to datetime format to extract additional features such as year and month.
- Missing or null values were checked and handled appropriately.
- Feature engineering was performed to create additional features from existing ones.
## Models

In this project, we employed four machine learning algorithms to predict the sourcing cost of products. Each algorithm offers unique advantages and was chosen based on its suitability for the task at hand.

### 1. K-Nearest Neighbors (KNN)

K-Nearest Neighbors is a non-parametric algorithm used for classification and regression tasks. It predicts the value of a target variable by averaging the values of its k nearest neighbors. In our project, KNN was utilized to capture local patterns in the data and make predictions based on similarity to neighboring data points.

### 2. Random Forest

Random Forest is an ensemble learning method that builds multiple decision trees during training and outputs the mean prediction of the individual trees. It is robust to overfitting and handles high-dimensional data well. Random Forest was chosen for its ability to capture complex relationships between features and the target variable.

### 3. Linear Regression

Linear Regression is a simple and widely-used algorithm for regression tasks. It models the relationship between the independent variables and the target variable by fitting a linear equation to the observed data. Despite its simplicity, Linear Regression can be effective in cases where the relationship between variables is approximately linear.

### 4. Gradient Boosting

Gradient Boosting is an ensemble learning technique that builds a series of weak learners (usually decision trees) sequentially. Each new model corrects errors made by the previous ones, leading to a strong predictive model. Gradient Boosting is known for its high predictive accuracy and robustness to overfitting.

### Outlier Detection Techniques

In addition to modeling, outlier detection techniques were employed to identify and handle outliers in the dataset:

- **Z-Score:** Z-score, also known as standard score, measures the number of standard deviations a data point is from the mean of the dataset. Data points with a z-score above a certain threshold (e.g., 3) are considered outliers and can be removed or treated separately.

- **Interquartile Range (IQR):** The IQR is a measure of statistical dispersion, defined as the difference between the third quartile (Q3) and the first quartile (Q1) in a dataset. Outliers are identified as data points that fall below Q1 - 1.5 * IQR or above Q3 + 1.5 * IQR. These outliers can be trimmed or replaced using appropriate techniques.



## Evaluation

<img width="905" alt="Screenshot 2024-05-12 at 7 56 03 AM" src="https://github.com/saumitkunder/Maersk-Assessment-AIML-Saumit/assets/109196162/d78629c1-177b-4c04-8c8d-c052c75ab000">
This evaluation compares various regression models to determine which performs best under different data scaling conditions. We analyzed the performance using four metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE), R-squared (R²), and Root Mean Squared Error (RMSE). The models were evaluated with two scaling techniques: Interquartile Range (IQR) and Z-score normalization.

### Models Evaluated
- **Random Forest**
- **K-Nearest Neighbors (KNN)**
- **Linear Regression**
- **Gradient Boosting**

### Scaling Techniques
- **IQR Scaling:** Focuses on robustness by using the interquartile range, reducing the impact of outliers.
- **Z-score Scaling:** Utilizes mean and standard deviation to normalize data, ensuring uniform contribution from all features.

### Results

#### Random Forest
- **IQR**: MSE = 364.873, MAE = 9.07736, R² = 0.882912, RMSE = 19.1016
- **Z-score**: MSE = 483.167, MAE = 9.80829, R² = 0.851515, RMSE = 21.9811

#### KNN
- **IQR**: MSE = 448.944, MAE = 9.91425, R² = 0.855933, RMSE = 21.1883
- **Z-score**: MSE = 622.358, MAE = 10.8541, R² = 0.808739, RMSE = 24.9471

#### Linear Regression
- **IQR**: MSE = 700.621, MAE = 17.0217, R² = 0.77517, RMSE = 26.4693
- **Z-score**: MSE = 851.789, MAE = 17.7759, R² = 0.738231, RMSE = 29.1854

#### Gradient Boosting
- **IQR**: MSE = 723.86, MAE = 18.2859, R² = 0.767712, RMSE = 26.9047
- **Z-score**: MSE = 842.889, MAE = 18.7076, R² = 0.740967, RMSE = 29.0325

### Conclusion
The **Random Forest** model with **IQR scaling** showed the best overall performance, indicating its effectiveness for datasets with outlier influences and complex patterns. Linear Regression models were the least effective, particularly with Z-score normalization, indicating potential issues with high variance data or outlier sensitivity. Future work should explore parameter tuning and consider alternative models based on the specific characteristics of the dataset.



