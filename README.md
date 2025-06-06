# Auto Insurance Claim Prediction

This project aims to build a predictive model that determines the likelihood of a policyholder filing an auto insurance claim. The model is designed to help insurance companies manage risk more effectively, offer fair premium pricing, and reduce potential fraud.

---

## Problem Statement

In the auto insurance industry, accurately predicting which customers are likely to file a claim is crucial for managing risk, optimizing premiums, and detecting fraudulent activities. This project was developed in response to a request from a fictional insurance company to build a model that accurately identifies high-risk policyholders using available customer and vehicle data.

---

## Objectives

- Develop and compare multiple classification models to predict the likelihood of an insurance claim.
- Evaluate models using the ROC-AUC metric due to class imbalance.
- Improve model performance through hyperparameter tuning and feature engineering.

---

## 🧾 Dataset Overview

- **Source**: [Kaggle]([https://www.kaggle.com/](https://www.kaggle.com/datasets/ifteshanajnin/carinsuranceclaimprediction-classification/data))
- **Size**: 58,000 rows, 44 columns
- **Target Variable**: `is_claim` (1 = claim filed, 0 = no claim)
- **Data Includes**:
  - Customer information
  - Vehicle information
  - other details

---

## Workflow Summary

1. **Data Preprocessing**
   - Handled missing values
   - Feature encoding and transformation
   - Feature scaling and normalization

2. **Modeling**
   - Trained Logistic Regression, Decision Tree, Random Forest, and XGBoost models
   - Evaluated performance using cross-validation and test ROC-AUC scores

3. **Model Selection**
   - Chose XGBoost as the final model based on best performance (ROC-AUC: 0.66)
   - Handled class imbalance using `class_weight` and evaluation-based selection

4. **Model Choice explanation**
   - SHAP values are planned for future integration to interpret model decisions

---

## Final Results

| Model              | Test ROC-AUC |
|-------------------|--------------|
| Logistic Regression | 0.586        |
| Decision Tree       | 0.510        |
| Random Forest       | 0.649        |
| XGBoost             | **0.660**    |

---

## 📌 Business Recommendations

- **Flag High-Risk Customers**: Use the model to identify customers likely to file a claim and flag them for manual underwriting.
- **Improve Fraud Detection**: Incorporate predictions into fraud detection workflows to detect suspicious patterns early.
- **Proactive Risk Management**: Offer targeted programs such as safer driving incentives to high-risk customers.

---

## 🔮 Future Work

- Engineer more complex and meaningful features to enhance model learning.
- Explore advanced ensemble models (e.g., CatBoost, LightGBM, Stacking).
- Apply advanced resampling methods (e.g., ADASYN) to better handle class imbalance.

---

## 📁 Project Structure
├── data                       
├── .gitignore                          
├── README.md  
├── Car_Insurance_Prediction.pdf     
├── Index.ipynb                                                          

