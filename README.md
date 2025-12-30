# Credit Risk Default Prediction (Python)

## Project Overview
This project implements an end-to-end credit risk modeling workflow to predict the probability of default (PD) for credit card clients. The objective is to simulate an industry-style credit risk framework that emphasizes interpretability, risk ranking, and business decision-making rather than pure predictive accuracy.

A logistic regression model was developed as a baseline due to its transparency and widespread use in regulated financial environments. Model performance was evaluated using industry-standard metrics such as ROC-AUC, KS statistic, and risk band validation.

---

## Business Problem
Financial institutions must assess the likelihood that a borrower will default on their obligations. Accurately identifying high-risk customers while minimizing the rejection of creditworthy applicants is critical for managing credit losses and profitability.

**Target Variable**
- `default.payment.next.month`
  - 1 = Default
  - 0 = No Default

---

## Dataset
**Source:** UCI Machine Learning Repository (via Kaggle)  
**Dataset:** Default of Credit Card Clients  

**Key Characteristics**
- ~30,000 observations
- Demographic, credit limit, billing, and payment history variables
- Binary default indicator

---

## Methodology

### 1. Data Preparation & EDA
- Missing value checks
- Distribution analysis
- Correlation analysis
- Class imbalance assessment

### 2. Modeling Approach
- Logistic Regression with class weighting to address class imbalance
- Model trained to output probability of default (PD) rather than binary labels

### 3. Model Evaluation
Performance was assessed using:
- ROC Curve & AUC
- KS Statistic
- Confusion Matrix (after threshold tuning)
- Recall for default cases

### 4. Threshold Tuning
Instead of using the default 0.5 cutoff, probability thresholds were evaluated to balance:
- Default detection (recall)
- Rejection of creditworthy customers

A threshold of **0.40** was selected to reflect a conservative but realistic credit risk policy.

### 5. Risk Segmentation & Validation
Predicted PDs were segmented into quintile-based risk bands:
- Very Low
- Low
- Medium
- High
- Very High

Observed default rates increased monotonically across these bands, validating the model’s ability to correctly rank credit risk.

---

## Key Results

- Strong discriminatory power as shown by ROC-AUC
- High recall for default cases after threshold tuning
- Clear and monotonic increase in observed default rates across risk bands
- Model outputs suitable for credit decisioning and risk segmentation


## Repository Structure

credit-risk-default-prediction/
│
├── data/
│ └── raw/
│ └── credit_card_default.csv
│
├── notebooks/
│ ├── credit_risk_model.ipynb
│
├── reports/
│ └── credit_risk_model_report.pdf
│
├── requirements.txt
└── README.md


---

## Tools & Libraries
- Python
- pandas, numpy
- scikit-learn
- matplotlib, seaborn

---

## Key Takeaways
- Credit risk modeling prioritizes risk ranking and interpretability over accuracy
- Class imbalance handling and threshold selection are critical
- Risk band validation provides strong evidence of model usefulness in real-world credit decisioning

---

## Future Enhancements
- Compare performance with non-linear models (Gradient Boosting, Random Forest)
- Perform probability calibration
- Incorporate business cost and expected loss analysis
- Extend to stress testing scenarios

---

## Author
Augustine Ozoemena 
Credit Risk / Data Science Portfolio Project
