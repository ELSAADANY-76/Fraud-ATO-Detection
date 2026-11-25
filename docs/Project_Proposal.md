# Fraud and Account-Takeover Detection for Fintech

## 1. Problem Statement

The increasing use of digital payments and mobile financial services has created opportunities for financial fraud. Fintech companies must identify fraudulent transactions while avoiding unnecessary declines of legitimate customer transactions.

Our project aims to develop a machine learning-based fraud detection system that analyzes financial transaction patterns and classifies transactions as legitimate or fraudulent.

## 2. Target Customer

- Digital payment providers.
- Fintech startups.
- E-commerce platforms.

## 3. Proposed Solution

We propose an AI-powered fraud detection system using machine learning classification techniques.

The system will:
- Analyze financial transaction data.
- Identify suspicious transaction patterns.
- Predict the probability of fraudulent activity.
- Help reduce financial losses and false transaction declines.

Account-takeover detection will be considered as a potential extension.

## 4. Dataset

**ULB Credit Card Fraud Detection Dataset**

Source: Kaggle – Credit Card Fraud Detection.

The dataset contains 284,807 transactions, including 492 fraudulent transactions.

Target variable:
- 0: Legitimate transaction.
- 1: Fraudulent transaction.

## 5. Business Impact

The system must balance two important business costs:

- False Negative: Fraudulent transaction classified as legitimate, resulting in potential financial loss.
- False Positive: Legitimate transaction classified as fraudulent, potentially blocking a genuine customer.

Our objective is to minimize both errors while prioritizing fraud detection.

## 6. Proposed Methodology

1. Dataset collection and exploration.
2. Data cleaning and preprocessing.
3. Time-based training and testing split.
4. Feature scaling using a preprocessing pipeline.
5. Baseline model development using Logistic Regression.
6. Model evaluation using a confusion matrix, precision, recall, F1-score and precision-recall curve.

## 7. Success Metrics

The initial model will be evaluated using:

- Precision
- Recall
- F1-score
- Confusion Matrix
- Precision-Recall Curve

Recall and precision will be particularly important because of the highly imbalanced nature of financial fraud datasets.

Success targets (on the time-based test set):

- Phase 1 baseline: Average Precision of at least 0.70 (achieved: 0.761).
- Phase 2 final model: recall of at least 80% with precision of at least 30%, and a positive net saving under our cost assumptions (the baseline is EUR -3,931).

## 8. Team Members

| Member | Responsibility |
|---|---|
| Selim | Preprocessing pipeline, baseline model, leakage check |
| Lojain | Repository setup, README, EDA |
| Ammar | Business cost matrix, business metric, presentation |

## 9. Expected Outcome

A working baseline machine learning model capable of identifying potentially fraudulent financial transactions, supported by an evaluated preprocessing pipeline and documented experimental results.
