# Phase 1 – Baseline Model Results

## 1. Model Information

- Algorithm: Logistic Regression
- Class Weight: Balanced
- Maximum Iterations: 1000
- Random State: 42

## 2. Dataset Information

The original dataset contained 284,807 transactions.

After removing 1,081 exact duplicate records, the cleaned dataset contained 283,726 transactions.

## 3. Dataset Split

| Description | Number |
|---|---:|
| Training transactions | 226,980 |
| Testing transactions | 56,746 |
| Training fraud cases | 399 |
| Testing fraud cases | 74 |

A chronological 80/20 split was used.

## 4. Evaluation Results

| Metric | Result |
|---|---:|
| Precision | 0.0662 |
| Recall | 0.8919 |
| F1-score | 0.1232 |
| Average Precision | 0.7608 |

## 5. Confusion Matrix

| Actual / Predicted | Legitimate | Fraud |
|---|---:|---:|
| Legitimate | 55,741 | 931 |
| Fraud | 8 | 66 |

## 6. Results Interpretation

The Logistic Regression model detected 66 out of 74 fraudulent transactions.

The model achieved approximately 89.19% fraud recall, demonstrating that it detected most fraudulent transactions.

However, precision was approximately 6.62%, indicating that many legitimate transactions were incorrectly flagged as fraudulent.


## 7. Conclusion

The baseline model provides an initial machine learning solution for identifying fraudulent financial transactions.

Further improvements will focus on reducing false positives while maintaining strong fraud detection performance.
