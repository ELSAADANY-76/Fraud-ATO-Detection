# Phase 1 – Baseline Model Results

## 1. Model Information

**Algorithm:** Logistic Regression

**Class Weight:** Balanced

**Maximum Iterations:** 1000

**Random State:** 42

## 2. Dataset Split

Training samples: 227,845

Testing samples: 56,962

Testing fraud cases: 75

## 3. Evaluation Results

| Metric | Score |
|---|---:|
| Precision | 0.0707 |
| Recall | 0.8933 |
| F1-score | 0.1311 |
| Average Precision | 0.7611 |

## 4. Confusion Matrix

| | Predicted Legitimate | Predicted Fraud |
|---|---:|---:|
| Actual Legitimate | 56,007 | 880 |
| Actual Fraud | 8 | 67 |

## 5. Initial Interpretation

The Logistic Regression model successfully detected 67 out of 75 fraudulent transactions.

The model achieved high fraud recall (89.33%), meaning it detected most fraudulent transactions.

However, its precision was relatively low (7.07%), indicating that many legitimate transactions were incorrectly flagged as fraudulent.

This demonstrates the importance of balancing fraud detection with minimizing false positives.

## 6. Conclusion

The baseline model provides a starting point for fraud detection.

Further improvements will focus on reducing false positives while maintaining strong fraud detection performance.

Future work will include model comparison, class imbalance strategies, threshold optimization, and explainability.
