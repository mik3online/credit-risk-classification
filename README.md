# credit-risk-classification


**Module 12 Report**

## Overview of the Analysis

In this analysis, the goal was to develop machine learning models to predict the creditworthiness of borrowers using financial information. The primary objective was to distinguish between "healthy" loans (0) and "high-risk" loans (1). The analysis involved the following stages:

1. **Split the Data**: The data was split into training and testing sets to facilitate model training and evaluation.

2. **Original Logistic Regression Model**: A logistic regression model was built using the original data, and its performance was assessed.

3. **Random Over Sampler Model**: A logistic regression model was created with oversampled data using the RandomOverSampler from the imbalanced-learn library.

## Results

### Original Logistic Regression Model

- **Accuracy Score:** 0.99
- **Balanced Accuracy Score:** 0.95

**Confusion Matrix:**
- True Positives (Correct High-Risk Predictions): 461
- False Positives (Healthy Loans Incorrectly Predicted as High-Risk): 75
- True Negatives (Correct Healthy Loan Predictions): 14926
- False Negatives (High-Risk Loans Incorrectly Predicted as Healthy): 46

**Classification Report:**
- Precision for High-Risk Loans (1): 0.86
- Recall for High-Risk Loans (1): 0.91
- F1-score for High-Risk Loans (1): 0.88
- Precision for Healthy Loans (0): 1.00
- Recall for Healthy Loans (0): 1.00
- F1-score for Healthy Loans (0): 1.00

### Random Over Sampler Model

- **Accuracy Score (Resampled Model):** 0.99
- **Balanced Accuracy Score (Resampled Model):** 0.99

**Confusion Matrix (Resampled Model):**
- True Positives (Correct High-Risk Predictions): 504
- False Positives (Healthy Loans Incorrectly Predicted as High-Risk): 86
- True Negatives (Correct Healthy Loan Predictions): 14915
- False Negatives (High-Risk Loans Incorrectly Predicted as Healthy): 3

**Classification Report (Resampled Model):**
- Precision for High-Risk Loans (1): 0.85
- Recall for High-Risk Loans (1): 0.99
- F1-score for High-Risk Loans (1): 0.92
- Precision for Healthy Loans (0): 1.00
- Recall for Healthy Loans (0): 0.99
- F1-score for Healthy Loans (0): 1.00

## Summary

The performance of both machine learning models is very good, but the Random Over Sampler Model demonstrates slightly improved results:

- The Random Over Sampler Model achieves a balanced accuracy score of 0.99, indicating excellent performance in distinguishing between healthy and high-risk loans. The original model also performs well with a balanced accuracy score of 0.95.

- Both models have high precision, recall, and F1-scores for both healthy and high-risk loans. However, the Random Over Sampler Model achieves higher recall for high-risk loans, which is crucial for identifying potentially problematic loans.

In summary, the Random Over Sampler Model slightly outperforms the original model in predicting both healthy and high-risk loan labels. It is recommended for use by the company due to its exceptional performance in identifying high-risk loans, which is of high importance in the lending industry.