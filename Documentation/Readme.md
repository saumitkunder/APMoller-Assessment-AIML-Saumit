
# Dataset Folder

This folder contains the dataset used in the project. The dataset provides valuable insights into sourcing information for various products.

## Contents

1. [Dataset File](#dataset-file)
2. [Data Description](#data-description)
3. [Data Source](#data-source)
4. [Preprocessing Steps](#preprocessing-steps)
5. [Purpose](#purpose)

## Dataset File

The dataset file is named [traindataset, testdataset] and is stored in [xlsx].

## Data Description

The dataset consists of the following features:

- **Manufacturer**: The manufacturer of the product.
- **Area Code**: The area code associated with the sourcing location.
- **Sourcing Channel**: The channel through which the product was sourced (e.g., wholesale, direct).
- **Product Size**: The size of the product (e.g., large, small).
- **Product Type**: The type of product.
- **Month of Sourcing**: The month in which the product was sourced.
- **Sourcing Cost**: The cost associated with sourcing the product.

## Data Source

The dataset is sourced from the internal database of [AP Moller company]. 

## Preprocessing Steps

The following preprocessing steps were applied to the dataset:

- **Handling Missing Values**: Checked and addressed any missing or null values.
- **Feature Engineering**: Extracted relevant features from datetime columns, such as year and month.
- **Encoding Categorical Variables**: Converted categorical variables into numerical format using one-hot encoding or similar techniques.

## Purpose

The purpose of the dataset is to provide insights into the sourcing behavior and costs associated with different products. It is used for analysis and modeling to optimize sourcing strategies and minimize costs.
