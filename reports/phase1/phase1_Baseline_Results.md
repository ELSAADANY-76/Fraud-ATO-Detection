# Phase 1 – Final Baseline Results

## 1. Model Configuration

- Algorithm: Logistic Regression
- Class Weight: Balanced
- Maximum Iterations: 1000
- Random State: 42

## 2. Dataset Information

- Original records: 284,807
- Duplicate records removed: 1,081
- Cleaned records: 283,726
- Missing values: 0

## 3. Train/Test Split

| Description | Records |
|---|---:|
| Training | 226,980 |
| Testing | 56,746 |
| Training fraud cases | 399 |
| Testing fraud cases | 74 |

A chronological 80/20 split was applied.

## 4. Evaluation Metrics

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

## 6. Interpretation

The model detected 66 out of 74 fraudulent transactions.

It achieved approximately 89.19% recall, demonstrating its ability to identify most fraudulent transactions.

However, precision was approximately 6.62%, indicating a high number of false-positive predictions.

## 7. Conclusion

The Logistic Regression model provides our initial fraud detection baseline.

Future improvements will focus on reducing false positives while maintaining high fraud detection performance.
