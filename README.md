![banner](assets/banner.png)  
Banner [source](https://banner.godori.dev/)

![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-grey)
![GitHub last commit](https://img.shields.io/github/last-commit/adin11/ML-Project-Credit-Risk-Modelling)
![Type of ML](https://img.shields.io/badge/Type%20of%20ML-Classification-blue)
![License](https://img.shields.io/badge/License-MIT-green)
[![FastAPI App](https://img.shields.io/badge/Deployed%20with-FastAPI-red)]()
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

# 💳 Credit Risk Modelling

##### App Link: [RiskRadar - Live Credit Scoring Engine](https://riskradar.onrender.com)
---
## 🔍 Business Problem:
Money Lending instituitions often struggle to identify which applicants might default on loans. This leads to financial losses and operational risks. The goal is to build a solution that accurately classifies applicants based on their creditworthiness, making the loan approval process more efficient and secure.

---

## Overview:
A powerful, production-ready Credit Risk Scoring System built for financial institutions. Mimicking a CIBIL-like credit scorecard. It classifies applicants into different risk bands using financial and behavioral indicators. Designed to support smarter, faster lending decisions while reducing default risk, this real-time system is fair, scalable, and data-driven.
---
## Demo
https://github.com/user-attachments/assets/4bb24da3-ff39-4984-b5cd-980bcc0c37d5

---

## Power BI Dashboard:
![dashboard](assets/dashboard.png)

**Power Bi Dashboard for analyzing default patterns.**

---

# Key Insights:
**Important: In the Context of Credit Risk Modelling and loan defaults, default refers to when the person is unable to pay the loan**

## 1. Default % By Age Bins:
![Kde Plot](assets/age.png)

**The Age Group 18-25 have higher default rate (12%) followed By 26-40 (9.7 %) and above 40 (6.8 %)**
**Younger age groups are more prone to default than the elder ones.**

## 2. Default % By City:
![Loan Months](assets/city.png)


**This Bar chart illustrates default% by each city.**
**Pune has the highest no of defaults (9.1%) whereas hyderabad has least defaults (8.2%).**


## 3. Default% By Loan Purpose:
![Loan Months](assets/loan_purpose.png)


**Majority of the defaults were caused by home loans (15%), Education loans contributed to (9.9%) of defaults.**
**Personal and auto type of loans did not default much (4 to 5 %).**


## 4. Relationship between credit utilization ratio and DPD affecting Default:
![Loan Months](assets/credit_util.png)


**The above scatter chart shows the relationship of credit utilization ratio and total days past due with size set to default %.**
**Higher the credit utilization ratio and days past due more chance of it to default.**

## 5. Default % by residency type and employment status:
![Loan Months](assets/residency.png)


**Individuals with rented residency tend to default more (16%).**
**People who have mortgage on their homes contribute to 9.4 % default and professionals who own their homes have very less default rate 5.5 %.**
**Salaried professionals defaulted slightly more (9.1) as compared to self-employed professionals**

## 6. Roc, Auc Curve:
![Roc auc curve](assets/roc.png)

## 7. Feature Importances:
![Feature Importance](assets/fc.png)

**The most essential features affecting model performance are credit utilization ratio, loan to income ratio, delinquency ratio, avg days past due per delinquncy.**

--- 

## ⚙️ Tech Stack:
- Python (3.10+)
- Pandas, Numpy, Matplotlib, Seaborn
- FastAPI (for scoring backend)
- Streamlit (UI)
- Optuna (Hyperparameter tuning)
- SMOTE-Tomek (Class imbalance handling)
- Render (deployment)

---

## 🧪 Methods:

### 📥 Data Preprocessing
- Prevented data leakage by separating features (`X`) and target (`y`) early.
- Applied identical pipelines to train/test sets independently.

### 📊 Exploratory Data Analysis
- Used histograms and KDE plots to visualize key predictors.
- Explored risk segments across demographics.

### 🧠 Feature Engineering
- Created meaningful features like `Loan-to-Income Ratio`, `Delinquency Ratios`, and `Avg Days Past Due`.
- Applied domain expertise for better interpretability.

### 🧮 Feature Selection
- Checked multicollinearity with VIF.
- Evaluated categorical features using WoE & IV for business relevance.

### 🤖 Model Development
- Trained Logistic Regression, Random Forest, and XGBoost.
- Used SMOTE-Tomek Links to balance default vs non-default classes.

### 🛠️ Hyperparameter Tuning
- Fine-tuned models using Optuna to reduce false negatives and improve recall.

---

## 📈 Evaluation Metrics
- **ROC AUC:** 0.983  
- **KS Statistic:** 85 (top 3 deciles)  
- **Gini Coefficient:** High discriminatory power  
- **Decile Analysis:** Effective risk segmentation

---

## 📌 Top Conclusions:

- Factors like Loan-to-Income Ratio and Delinquency Rates are strong indicators of risk.
- A High recall for defaults helps in identifying risky borrowers early, improving risk management.
- Classifying borrowers based on their risk level helps lenders manage loans more safely and avoid bad debts

---

> 🚀 **The final model deployed is a Logistic Regression classifier with custom SMOTE handling, served through FastAPI and visualized via Streamlit.**
