# Bank Customer Churn Prediction 🏦

## 1. Project Overview & Business Problem
In the highly competitive banking sector, customer retention is a critical challenge. Since acquiring a new customer is significantly more expensive than retaining an existing one, predicting which customers are likely to leave (Churn) provides immense economic value.

The objective of this project is to develop a Machine Learning model that identifies at-risk customers based on their demographic and financial profiles.

### The Primary Metric: Recall
In this analysis, we prioritized **Recall** as our key performance indicator. 
**Business Justification:** For a bank, the cost of "missing" a customer who is actually about to leave (False Negative) is much higher than the cost of a "false alarm" (False Positive). We aim to capture as many potential churners as possible to enable proactive retention efforts.

---

## 2. Data Preprocessing
To prepare the raw dataset for modeling, the following steps were performed:
* **Feature Engineering:** Categorical variables (Geography, Gender) were converted into numerical format using One-Hot Encoding.
* **Feature Scaling:** Min-Max Scaling was applied to normalize numerical variables, ensuring that features with larger ranges (e.g., Balance) do not disproportionately influence the model.
* **Imbalance Handling:** Utilized `class_weight='balanced'` to address the minority class of churned customers.

---

## 3. Modeling & Results
We evaluated three different models to find the most effective solution:

| Model | Recall (Churn Class) | Observation |
| :--- | :--- | :--- |
| **Logistic Regression** | **0.19** | Failed to capture the majority of churners. |
| **Decision Tree** | **0.75** | Significant improvement by balancing class weights. |
| **Random Forest** | **Optimized** | Final model selected for its stability and predictive power. |

---

## 4. Business Insights (Feature Importance) 📊
Analysis of the final **Random Forest** model revealed the primary drivers of customer churn:

1. **Age (45.2% Importance):** Older customers show a much higher tendency to leave the bank.
2. **Number of Products (23.9% Importance):** The variety of products a customer holds is a major factor in their loyalty (stickiness).
3. **Activity Level:** "Inactive Members" represent a high-risk segment that requires immediate attention.

---

## 5. Actionable Recommendations
Based on the data-driven insights, we recommend the following strategies for the bank:
* **Targeted Loyalty Programs:** Create specific retention campaigns for customers aged 40 and above.
* **Strategic Bundling:** Encourage customers to adopt more products to increase their engagement and reduce the likelihood of switching banks.
* **Proactive Engagement:** Prioritize outreach to "Inactive" customers with personalized offers before they decide to leave.

---
**Developed by:** Yarin Siton| Final Year Economics & Management Student (Data Science Specialization).
