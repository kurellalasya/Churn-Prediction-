# Churn-Prediction
# E-Commerce Customer Churn Prediction

## Project Overview

Customer churn is one of the most important business challenges for e-commerce companies. Acquiring new customers is often more expensive than retaining existing ones. This project aims to identify customers who are likely to stop purchasing from the platform and provide actionable insights for retention strategies.

Using a synthetic but realistic e-commerce dataset, multiple machine learning models were trained and evaluated to predict customer churn based on customer demographics, purchasing behavior, engagement metrics, and satisfaction indicators.

---

## Problem Statement

Build a machine learning model capable of predicting whether a customer is likely to churn (leave the platform) based on historical behavioral and transactional data.

**Target Variable:**

* `churn = 1` → Customer is likely to churn
* `churn = 0` → Customer is likely to remain active

---

## Dataset

### Dataset Characteristics

* **Records:** 5,000 customers
* **Features:** 21 customer attributes
* **Problem Type:** Binary Classification

### Feature Categories

#### Customer Demographics

* Age
* Gender
* City Tier
* Tenure Months

#### Transactional Features

* Number of Orders
* Average Order Value
* Total Spend
* Number of Returns
* Return Rate

#### Engagement Features

* Number of Sessions
* Average Session Duration
* Email Open Rate
* App Usage
* Coupon Redemption
* Discount Usage Rate

#### Customer Experience Features

* Satisfaction Score
* Support Tickets

---

## Exploratory Data Analysis (EDA)

Comprehensive EDA was performed to identify patterns associated with churn.

### Key Findings

* Customers inactive for longer periods showed significantly higher churn rates.
* Higher return rates were strongly associated with customer churn.
* Customers with low satisfaction scores were more likely to leave.
* App users demonstrated lower churn rates compared to non-app users.
* Tier-3 city customers exhibited relatively higher churn behavior.

---

## Data Preprocessing

The following preprocessing techniques were applied:

* Removal of unnecessary identifiers
* Label Encoding for categorical variables
* Train-Test Split (80:20)
* Feature Scaling using StandardScaler
* Class Imbalance Handling using SMOTE

### Class Distribution

Before SMOTE:

* Retained Customers: 3,705
* Churned Customers: 295

After SMOTE:

* Retained Customers: 3,705
* Churned Customers: 3,705

---

## Machine Learning Models

The following models were trained and compared:

1. Logistic Regression
2. Random Forest Classifier
3. Gradient Boosting Classifier

### Validation Strategy

* Stratified 5-Fold Cross Validation
* ROC-AUC used as the primary evaluation metric

---

## Model Performance

| Model               | ROC-AUC         |
| ------------------- | --------------- |
| Logistic Regression | Evaluated       |
| Random Forest       | Evaluated       |
| Gradient Boosting   | Best Performing |

### Best Result

* **ROC-AUC Score:** 0.7952
* **Evaluation Method:** Holdout Test Set

The selected model demonstrated strong generalization performance and effectively distinguished churn-prone customers from retained customers.

---

## Visualizations

### EDA Overview

![EDA Overview](fig1_overview_eda.png)

### Behavioral Analysis

![Behavioral Analysis](fig2_behavioral_eda.png)

### Correlation Heatmap

![Correlation Heatmap](fig3_correlation.png)

### Model Evaluation Dashboard

![Model Evaluation](fig4_model_evaluation.png)

---

## Business Insights

### High-Risk Customer Segments

#### Tier-3 City Customers

* Churn Rate: ~16%

#### Customers with High Return Rates (>20%)

* Churn Rate: ~29.4%

#### Low Satisfaction Customers

* Significantly higher likelihood of churn

#### Inactive Customers

* Long periods without purchases strongly correlated with churn

---

## Retention Recommendations

Based on model predictions and feature analysis:

1. Launch re-engagement campaigns for customers inactive for more than 45 days.
2. Prioritize support resolution for customers raising multiple tickets.
3. Encourage app adoption among web-only users.
4. Create loyalty programs targeting Tier-3 city customers.
5. Follow up with customers reporting low satisfaction scores.
6. Investigate customers with high product return rates.

---

## Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Imbalanced-Learn (SMOTE)

---

## Project Workflow

1. Synthetic Dataset Generation
2. Data Cleaning and Exploration
3. Feature Engineering
4. Class Imbalance Handling (SMOTE)
5. Model Training
6. Cross Validation
7. Model Evaluation
8. Business Insight Generation
9. Retention Strategy Recommendations

---

## Future Improvements

* Deploy the model using Streamlit
* Build an interactive churn prediction dashboard
* Integrate real-world e-commerce datasets
* Implement automated retention recommendation systems
* Experiment with XGBoost and LightGBM

---

## Author

Developed as a Machine Learning project to demonstrate:

* Data Analysis
* Feature Engineering
* Classification Modeling
* Model Evaluation
* Business Insight Generation
* Customer Retention Analytics
