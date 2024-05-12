
# Project Code

This Python script file contains code for conducting exploratory data analysis (EDA), preprocessing the dataset, and training machine learning models. It serves as the main code file for the project, covering all essential steps from data exploration to model building.

## Purpose

The purpose of this script is to provide a comprehensive solution for analyzing the dataset, preparing it for modeling, and training predictive models to achieve the project objectives.

## Overview

The code file is organized into several sections, each serving a specific purpose:

1. **Exploratory Data Analysis (EDA):**
   - This section explores the dataset's characteristics, distributions, and relationships between variables.
   - It includes visualizations and statistical analysis to gain insights into the data.

2. **Data Preprocessing:**
   - This section preprocesses the dataset to prepare it for modeling.
   - Tasks include handling missing values, feature engineering, and encoding categorical variables.

3. **Model Training:**
   - This section trains machine learning models using the preprocessed data.
   - It includes code for splitting the dataset into train and test sets, training various models, and evaluating model performance.

## Features

- **Main Script:** The main script file contains all the code for EDA, preprocessing, and model training.

## Dependencies

The script relies on the following Python libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn


## Data

the dataset used in this project is sourced from the AP Moller company itself. It is stored in an Excel file format (.xlsx) and contains information about various aspects related to sourcing and product details.

### Dataset Description:
- Source: AP Moller company
- Format: Excel (.xlsx)
- Contents:
  The dataset includes information about sourcing details, such as manufacturer, area code, sourcing channel, product size, product type, month of sourcing, and sourcing       cost.
  Additionally, it may contain other relevant features related to the sourcing process.

## Models

The script trains multiple machine learning models, including:
- Random Forest
- Gradient Boosting
- KNN
- Linear Regression

Model evaluation metrics such as mean squared error (MSE), mean absolute error (MAE), and R-squared are used to assess model performance.

## Results 
Comparing Scores of various models 
<img width="905" alt="Screenshot 2024-05-12 at 7 56 03 AM" src="https://github.com/saumitkunder/Maersk-Assessment-AIML-Saumit/assets/109196162/8b42d0a1-be09-4dcd-9073-0d83c1b457da">

Best Perfroming model visualisation 


<img width="701" alt="Screenshot 2024-05-12 at 8 04 54 AM" src="https://github.com/saumitkunder/Maersk-Assessment-AIML-Saumit/assets/109196162/d4e1cc14-b1b1-49a0-a56b-5007d8ac9313">

## Additional Notes

- The code is thoroughly documented with comments to explain each step and enhance readability.
- Feel free to explore and modify the code to suit your specific requirements or extend its functionality.

For detailed implementation and instructions, refer to the code comments and documentation within the script.

