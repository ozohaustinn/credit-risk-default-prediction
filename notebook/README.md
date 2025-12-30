# Credit Risk Default Prediction – Modeling Notebook

## Overview
This notebook contains the complete end-to-end credit risk modeling workflow used to predict the **probability of default (PD)** for credit card clients. The analysis is designed to reflect industry-standard credit risk practices, with an emphasis on interpretability, risk ranking, and business decision-making rather than pure predictive accuracy.

The notebook progresses from data exploration through model validation and risk segmentation, closely mirroring how credit risk models are developed and assessed in financial institutions.

---

## Dataset
**Source:** UCI Machine Learning Repository (via Kaggle)  
**Dataset:** Default of Credit Card Clients  

**Target Variable**
- `default.payment.next.month`
  - `1` = Default
  - `0` = No Default

The dataset includes demographic information, credit limits, billing amounts, and historical payment behavior.

---

## Notebook Structure

### 1. Business Objective
- Define the credit risk problem
- Explain the importance of predicting default risk
- Describe the modeling goal (PD estimation)

### 2. Data Loading & Initial Review
- Load raw dataset
- Inspect structure and dimensions
- Review target distribution and class imbalance

### 3. Exploratory Data Analysis (EDA)
- Distribution analysis of key variables
- Correlation analysis
- Identification of relationships relevant to default behavior

### 4. Data Preparation
- Feature selection
- Train–test split
- Handling class imbalance considerations

### 5. Modeling Approach
- Logistic Regression selected as a baseline model
- Class
