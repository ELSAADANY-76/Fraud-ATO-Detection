# Business Cost Matrix

## 1. Business Problem

Fintech companies process large numbers of financial transactions every day.

Their fraud detection systems must identify fraudulent transactions while minimizing unnecessary declines of legitimate customer transactions.

Our project aims to balance fraud prevention with customer experience.

## 2. Classification Outcomes

Our fraud detection system produces four possible outcomes:

| Actual Class | Predicted Class | Result |
|---|---|---|
| Legitimate | Legitimate | True Negative (TN) |
| Legitimate | Fraud | False Positive (FP) |
| Fraud | Legitimate | False Negative (FN) |
| Fraud | Fraud | True Positive (TP) |

## 3. Business Impact

### False Positive (FP)

A legitimate transaction is incorrectly classified as fraudulent.

Potential consequences:
- Legitimate customer transactions are declined.
- Customer inconvenience.
- Lost transaction revenue.
- Reduced customer trust.

### False Negative (FN)

A fraudulent transaction is incorrectly classified as legitimate.

Potential consequences:
- Direct financial losses.
- Additional unauthorized transactions.
- Potential customer compensation costs.
- Increased investigation expenses.

### True Positive (TP)

A fraudulent transaction is correctly identified.

Benefits:
- Fraud can be prevented or investigated.
- Potential financial losses are reduced.

### True Negative (TN)

A legitimate transaction is correctly identified.

Benefits:
- Normal customer transactions continue.
- Unnecessary transaction declines are avoided.

## 4. Business Cost Matrix

| Actual / Predicted | Legitimate | Fraud |
|---|---|---|
| Legitimate | No fraud-related cost (TN) | False decline cost (FP) |
| Fraud | Missed fraud cost (FN) | Fraud detection cost (TP) |

The financial cost of a false negative may be significantly higher than the cost of a false positive, depending on the transaction amount and business circumstances.

## 5. Business Priorities

Our system should:

1. Detect as many fraudulent transactions as possible.
2. Minimize legitimate transactions incorrectly flagged as fraud.
3. Maintain a reasonable balance between precision and recall.
4. Consider the financial impact of different classification errors.

## 6. Evaluation Metrics

We will use the following metrics:

- Precision: Measures how many flagged transactions are actually fraudulent.
- Recall: Measures how many actual fraudulent transactions are detected.
- F1-score: Balances precision and recall.
- Confusion Matrix: Shows the four classification outcomes.
- Average Precision: Summarizes performance across different precision-recall thresholds.

## 7. Baseline Model Results and Business Metric

Logistic Regression baseline (cleaned dataset, threshold 0.5):

| Metric | Result |
|---|---:|
| Precision | 6.62% |
| Recall | 89.19% |
| F1-score | 12.32% |
| Average Precision | 76.08% |

The model detected 66 of 74 fraudulent transactions and flagged 931 legitimate transactions.

### Business metric (assumptions)

- A missed fraud costs its transaction amount (Amount column, EUR).
- A false decline costs an assumed EUR 10 (manual review and customer friction).

| Item | Value |
|---|---:|
| Fraud loss avoided (caught fraud) | EUR 5,378.78 |
| Fraud loss missed | EUR 2,348.89 |
| False declines | 931 x EUR 10 = EUR 9,310 |
| Net saving vs no model | EUR -3,931.22 |

At the default 0.5 threshold, the cost of false declines exceeds the fraud loss avoided. The model catches 89% of fraud cases but only 70% of fraud value. This motivates the cost-optimal threshold selection planned for Phase 2.

## 8. Future Improvements

In Phase 2, we plan to investigate:

- Comparing class weights with resampling techniques.
- Comparing multiple machine learning algorithms.
- Optimizing the classification threshold based on business costs.
- Using SHAP to explain suspicious transactions.
- Testing model performance under data drift.

## 9. Conclusion

The business cost analysis demonstrates that fraud detection requires more than maximizing accuracy.

Our system must consider both financial losses caused by missed fraud and customer impact caused by incorrectly blocked transactions.
