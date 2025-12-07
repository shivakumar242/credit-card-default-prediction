# credit-card-default-prediction

# Credit Card Default Prediction

---

## Project Overview

This project predicts whether a customer will default on next month's credit card payment using demographic, financial, and repayment behavior data (30,000 records).
By performing data preprocessing, EDA, and machine learning modeling, the project identifies key factors influencing default risk and builds a system that can assist banks in credit decision-making.

---

## Objectives

* Clean and preprocess the credit card dataset.
* Understand customer behavior using EDA.
* Engineer meaningful financial & repayment features.
* Build and compare ML models for default prediction.
* Identify impactful features influencing default.
* Prepare the best model for deployment.

---

## Tools & Technologies Used

* **Python**
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, SciPy
* **Environment:** Google Colab
* **Models:** Logistic Regression, Random Forest, XGBoost

---

## Steps Involved

### **1. Data Understanding & Cleaning**

* Corrected invalid category values.
* Converted categorical variables.
* No missing values found.
* Identified class imbalance (78% non-default, 22% default).

---

### **2. Exploratory Data Analysis (EDA)**

* Payment delays (PAY_0) strongly influence default.
* Customers with low credit limits show higher default rates.
* High bill amounts combined with low payments increase risk.
* Age & demographics show weak predictive power.

---

### **3. Feature Engineering**

Created new meaningful features:

* `BILL_AVG` – Average bill amount.
* `PAY_AVG` – Average payment amount.
* `TOTAL_DELAY_COUNT` – Number of delayed months.
* `TOTAL_DELAY_SEVERITY` – Severity of delays.

Redundant correlated features were removed.

---

### **4. Data Preprocessing**

* Outlier handling using **IQR capping**.
* Scaling using **StandardScaler**.
* Label encoding for categorical data.
* Handled imbalance using **class_weight='balanced'**.

---

## Model Building

### **Models Used**

* Logistic Regression
* Random Forest
* XGBoost (Final Model)

---

### **Final Model Performance (XGBoost)**

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 73.9% |
| Precision | 0.43  |
| Recall    | 0.62  |
| F1 Score  | 0.51  |
| ROC-AUC   | 0.758 |

---

## Key Insights

* Payment delay history is the strongest risk indicator.
* Low credit limit customers default more.
* High bill but low payment customers are high-risk.
* Demographics contribute minimally.

---

## Model Saving & Deployment

Model saved as:

```
best_model_xgboost.joblib
```

Successfully tested on unseen data.

---

## Future Improvements

* Add SHAP explainability.
* Deploy using Streamlit/FastAPI.
* Try LightGBM & CatBoost.
* Use Optuna for automated tuning.

---

## Author

**Shivakumar L R**
Master’s in AI & ML
📧 [shivakumar.lr25@gmail.com](mailto:shivakumar.lr25@gmail.com)
