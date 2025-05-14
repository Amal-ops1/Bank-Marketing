🏦 Bank Marketing Campaign Analysis

This project analyzes the **Bank Marketing Dataset** from the UCI Machine Learning Repository. It contains data from direct telemarketing campaigns (phone calls) conducted by a Portuguese banking institution to promote **term deposit subscriptions**.


🎯 Objective

- Analyze customer behavior and identify factors that influence subscription decisions.
- Build and evaluate machine learning models to **predict whether a client will subscribe to a term deposit**.
- Identify the **most important features** that drive successful campaign outcomes to improve future marketing strategies.


📂 Dataset Overview

- **Source**: [UCI Machine Learning Repository – Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)
- **Records**: ~41,000 customer contacts
- **Features**: Age, job, marital status, education, contact type, previous outcomes, etc.
- **Target**: `y` (binary - yes/no, whether the client subscribed to a term deposit)


 ⚙️ Preprocessing Steps

- Removed duplicates and outliers
- Handled missing values
- Encoded categorical variables using one-hot encoding
- Standardized numerical features using `StandardScaler`
- Balanced class distribution using stratified splitting


 📊 Exploratory Data Analysis (EDA)

- Count plots and histograms for understanding distributions
- Correlation heatmaps for feature relationships
- Outlier detection for `age` and `duration`


 🤖 Machine Learning Models Used

| Model                    | Description                         |
|-------------------------|-------------------------------------|
| Logistic Regression      | Baseline linear classifier          |
| Decision Tree            | Tree-based simple model             |
| Random Forest            | Ensemble of decision trees          |
| Gradient Boosting        | Boosted trees for better accuracy   |
| XGBoost                  | High-performance gradient boosting  |
| Support Vector Machine   | Kernel-based classification         |

---

🏁 Model Evaluation

Each model was evaluated using:

- **Accuracy**
- **AUC (Area Under ROC Curve)**
- **Confusion Matrix**
- **Classification Report**


 🏆 Best Performing Model

✅ The **Random Forest Classifier** achieved the highest accuracy of **91%**, followed closely by **XGBoost** with strong AUC performance.  
These models showed excellent generalization and are ideal for predicting subscription behavior.


 🔍 Feature Importance

Using XGBoost, the most influential features identified were:

- `duration` of the call
- `contact` method (cellular, telephone)
- `month` of contact
- `poutcome` (previous campaign outcome)
- `balance` and `housing` status


 📈 Visualization Highlights

- ROC curve comparison of all models
- Confusion matrices
- Feature importance bar chart


 ✅ Conclusion

This project demonstrated that **ensemble models (Random Forest, XGBoost)** are highly effective in predicting term deposit subscriptions.  
With the identified key features and strong performance metrics, this analysis can directly support **better-targeted marketing campaigns**.
