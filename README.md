# Loan Default Prediction

## 📘 Overview

Loan defaults can significantly impact a financial institution’s stability. With rising credit demands, it becomes crucial to identify high-risk borrowers early. Manual loan evaluations are time-consuming, inconsistent, and prone to human bias. This project uses machine learning to automate the loan approval process and predict whether a client is likely to default, improving efficiency and reducing financial risk.

---

## 🎯 Problem Statement

A bank wants to streamline its home loan approval process by creating a credit scoring model that is both accurate and interpretable. The aim is to replace manual evaluations with a data-driven approach while ensuring compliance with fair lending practices. The model should help assess the probability of a customer defaulting, based on their financial and credit profile.

---

## 📌 Objective

- Build and compare multiple classification models to predict loan default.
- Identify the most influential features contributing to loan risk.
- Recommend a model that balances accuracy, recall, and interpretability.

---

## 🧾 Dataset Description

Source: [Kaggle - HMEQ Dataset](https://www.kaggle.com/datasets)

This dataset includes information on loan applicants, their financial background, and whether they defaulted.
The target variable is `BAD` (1 = defaulted, 0 = not defaulted).

**Features:**

- `LOAN`: Requested loan amount  
- `MORTDUE`: Existing mortgage due  
- `VALUE`: Property’s market value  
- `REASON`: Purpose of loan (`HomeImp`, `DebtCon`)  
- `JOB`: Applicant’s job title  
- `YOJ`: Years at current job  
- `DEROG`: Count of major derogatory credit events  
- `DELINQ`: Count of delinquent credit lines  
- `CLAGE`: Age of oldest credit line (months)  
- `NINQ`: Number of recent credit inquiries  
- `CLNO`: Number of existing credit lines  
- `DEBTINC`: Debt-to-income ratio  
- `BAD`: Target variable (1 = default, 0 = repaid)

---

## ⚙️ Models Used

- **Decision Tree (baseline & tuned)**
- **Random Forest (baseline & tuned)**
- **XGBoost (baseline & tuned)**

Each model was evaluated on key classification metrics: **accuracy**, **recall**, and **precision**.

---

## 🔍 Key Insights

- All models show high training accuracy, but some overfit the training data.
- Random Forest and XGBoost (both tuned and untuned) delivered the best test accuracy (~0.905).
- Recall is slightly higher in Random Forest and XGBoost than Decision Trees, making them better for minimizing false negatives.
- Precision is highest in tuned Random Forest and XGBoost, making them reliable for reducing false positives.
- Decision Tree models are simpler and easier to interpret but slightly underperform in generalization.

---

## 🏁 Conclusion

Tuned **Random Forest** and **XGBoost** performed the best overall. However, depending on the institution's risk preference, **high recall (to catch more defaulters)** or **high precision (to avoid false flags)** can be prioritized. Interpretability can also be improved using feature importance plots or SHAP values.

---

## 📦 Tech Stack

- Python (Pandas, NumPy, Scikit-learn)
- XGBoost
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 💡 Author

*Saransh Dhage*  
Data Scientist | Machine Learning Enthusiast  
