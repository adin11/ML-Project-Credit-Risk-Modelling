![banner](assets/banner.png)  
Banner [source](https://banner.godori.dev/)

![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-lightgrey)
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

## Key Insights:

### 1. Default % By Age Bins:
![Kde Plot](assets/age.png)

** **

### 2. Fraud % Per City:
![Loan Months](assets/city.png)


** **


### 3. Fraud % Per Loan Purpose:
![Loan Months](assets/loan_purpose.png)


** **


### 4. Relationship between credit utilization ratio and DPD affecting Default:
![Loan Months](assets/credit_util.png)


** **

### 5. Default % by residency type and employment status:
![Loan Months](assets/residency.png)


** **

### 6. Roc, Auc Curve:
![Roc auc curve](assets/roc.png)
**False positive rate vs True positive rate, Area under the curve = 0.98**

### 7. Feature Importances:
![Feature Importance](assets/fc.png)
**All the three ratios indicate as Important feature for the model**

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

## 📌 Key Findings:
- Features like `Loan-to-Income Ratio` and `Delinquency Ratios` are strong predictors.
- High recall in default class improves proactive risk control.
- Risk band classification helps in better credit policy alignment.

---

> 🚀 **The final model deployed is a Logistic Regression classifier with custom SMOTE handling, served through FastAPI and visualized via Streamlit.**
