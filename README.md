# 🏦 Bank Marketing Campaign Analysis

This project analyzes the **Bank Marketing Dataset** from the UCI Machine Learning Repository. The dataset captures the results of direct telemarketing campaigns (phone calls) conducted by a Portuguese banking institution, aimed at promoting term deposit subscriptions.

## 🎯 Objectives

- Analyze customer behavior and key attributes that influence subscription decisions.
- Build and evaluate machine learning models to predict whether a client will subscribe to a term deposit.
- Identify the most important features that drive successful marketing campaigns.

## 📂 Dataset Information

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)
- **File used**: `bank-full.csv`
- **Records**: 45,211
- **Target Variable**: `y` (Has the client subscribed to a term deposit?)

## 🔍 Project Steps

### 1. Data Loading and Exploration
- Loaded `bank-full.csv`
- Explored data shape, types, and class imbalance

### 2. Data Cleaning & Preprocessing
- Removed duplicates and treated outliers (e.g., age, duration)
- Handled categorical variables using one-hot encoding
- Scaled numerical features with `StandardScaler`

### 3. Exploratory Data Analysis (EDA)
- Visualized numerical and categorical features using histograms and count plots
- Analyzed correlations using a heatmap

### 4. Model Building
Trained and evaluated the following models:

| Model                  | Accuracy | AUC  |
|------------------------|----------|------|
| Logistic Regression    | ~0.88    | ~0.89|
| Decision Tree          | ~0.87    | ~0.88|
| Random Forest          | **~0.91**| **~0.93**|
| Gradient Boosting      | ~0.90    | ~0.92|
| XGBoost                | **~0.91**| **~0.93**|
| Support Vector Machine | ~0.88    | ~0.89|

### 5. ROC Curve Analysis
- Compared ROC curves for all models
- Random Forest and XGBoost showed the best balance between sensitivity and specificity

### 6. Feature Importance
- Used XGBoost to rank top features
- Important features: `duration`, `contact_cellular`, `poutcome_success`, `month`, etc.

## 🏁 Conclusion

- Random Forest and XGBoost were the most accurate models (~91%) and achieved the highest AUC scores (~0.93).
- Feature importance analysis helps identify key drivers behind customer conversion.
- These insights can improve future marketing strategies by targeting the right customers at the right time.

## ✅ Requirements

- Python 3.x
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- xgboost

Install dependencies:
```bash
pip install -r requirements.txt
