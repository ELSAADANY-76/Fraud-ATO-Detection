# Exploratory Data Analysis (EDA) Findings

## 1. Dataset Overview

The Credit Card Fraud Detection dataset contains financial transactions made by European cardholders during September 2013.

The dataset is used to investigate patterns associated with fraudulent and legitimate transactions.

### Dataset Statistics

| Property | Value |
|---|---:|
| Total Transactions | 284,807 |
| Total Features | 30 |
| Total Columns | 31 |
| Legitimate Transactions | 284,315 |
| Fraudulent Transactions | 492 |
| Fraud Percentage | 0.172% |
| Legitimate Percentage | 99.828% |

## 2. Data Structure

The dataset contains the following features:

- Time: Seconds elapsed between each transaction and the first transaction.
- V1–V28: Anonymized features obtained through Principal Component Analysis (PCA).
- Amount: Transaction amount.
- Class: Target variable.

### Target Variable

- 0: Legitimate transaction.
- 1: Fraudulent transaction.

## 3. Missing Values and Duplicates

Missing values and duplicate records were investigated during data exploration.

- Missing values: 0 (No missing values were found in the dataset).
- Duplicate records Total: 1081 .

Duplicate records were investigated before deciding whether any removal was appropriate.

## 4. Fraud Distribution Analysis

The fraud distribution visualization demonstrates a significant imbalance between legitimate and fraudulent transactions.

Fraudulent transactions represent approximately 0.172% of the entire dataset.

This imbalance makes fraud detection challenging because a model could achieve high accuracy while failing to identify fraudulent transactions.

Therefore, class imbalance handling is necessary.

## 5. Transaction Amount Analysis

Transaction amounts were investigated using statistical summaries and boxplots.

This analysis helps explore differences in transaction amounts between legitimate and fraudulent transactions.

## 6. Feature Correlation Analysis

A correlation heatmap was generated to investigate relationships between numerical features and the target variable.

This provides an overview of potential relationships that may help identify fraudulent transactions.

## 7. Main Findings

The EDA process revealed the following:

1. The dataset contains 284,807 financial transactions.
2. Fraudulent transactions represent a very small proportion of the dataset.
3. The dataset is highly imbalanced.
4. Most features are anonymized PCA-transformed numerical variables.
5. Class imbalance must be considered when developing the machine learning model.

## 8. Conclusion

The exploratory data analysis provided an understanding of the dataset structure, feature characteristics, and fraud distribution.

The findings support the use of machine learning techniques designed to handle imbalanced classification problems.

The next stage involves preprocessing the data and developing a baseline Logistic Regression model.
