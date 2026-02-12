# 📊 Customer Churn Prediction – End-to-End ML Project

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Machine Learning](https://img.shields.io/badge/ML-Classification-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 🚀 Project Overview

Customer churn is a critical challenge for subscription-based businesses. Losing customers directly impacts revenue and growth.  

This project builds a complete end-to-end machine learning pipeline to predict whether a customer will churn based on historical behavioral and demographic data.

The system includes:

- Data preprocessing
- Feature engineering
- Model training
- Model comparison
- Hyperparameter tuning
- Cross-validation
- ROC-AUC evaluation
- Feature importance analysis
- Model serialization for deployment

---

## 🧠 Problem Statement

Given structured customer data, predict whether a customer will:

- **1 → Churn**
- **0 → Not Churn**

The objective is to help businesses proactively identify high-risk customers and take retention actions.

---

## 📂 Project Structure

---

## 📊 Dataset Features

Example features used in the model:

- Age
- Tenure
- Monthly Charges
- Contract Type
- Total Charges
- Other behavioral attributes

Target variable:

---

## ⚙️ Machine Learning Pipeline

### 1️⃣ Data Preprocessing
- Handling missing values  
- Encoding categorical variables  
- Feature scaling (where required)  

### 2️⃣ Train-Test Split
- 80/20 split  
- Ensures fair evaluation on unseen data  

### 3️⃣ Models Implemented

#### 🔹 Logistic Regression (Baseline)
- Interpretable  
- Probabilistic output  
- Strong baseline model  

#### 🔹 Random Forest (Improved Model)
- Ensemble of decision trees  
- Handles non-linearity  
- Reduces overfitting  
- Feature importance extraction  

---

## 📈 Model Evaluation Metrics

The models were evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC (Primary Metric)  

### Why ROC-AUC?

ROC-AUC measures the model’s ability to distinguish between churn and non-churn customers across all thresholds, making it ideal for imbalanced classification problems.

---

## 🔍 Cross-Validation & Hyperparameter Tuning

- K-Fold Cross Validation  
- GridSearchCV for optimal hyperparameters  

Tuned parameters:
- `n_estimators`
- `max_depth`
- `min_samples_split`

This ensures robust and generalizable performance.

---

## 🌳 Feature Importance Analysis

Using Random Forest feature importances:

- Identified key churn drivers  
- Determined most influential features  
- Extracted business insights  

### Key Insight Example:

Customers with lower tenure and higher monthly charges show higher churn probability.

---

## 💾 Model Saving & Deployment Ready

The final model is serialized using:

```python
joblib.dump(model, "churn_model.pkl")

