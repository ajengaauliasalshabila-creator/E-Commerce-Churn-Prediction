# E-Commerce-Churn-Prediction

## **A. Business Problem Understanding**

**Context**

A leading e-commerce company aims to better understand customer churn behavior. In the online retail industry, the cost of acquiring new customers is significantly higher than the cost of retaining existing ones. Therefore, having the ability to identify customers who are likely to churn is crucial for minimizing revenue loss and optimizing retention strategies.

The company has access to historical customer data, including transaction volume, shopping frequency, purchase value, customer service interactions, and other behavioral indicators that reflect customer engagement. Using this information, the company seeks to build a predictive churn model.

**Target / Label**  

1 : Churn  
0 : Not churn

Since the company’s primary goal is to detect customers who are at high risk of leaving the platform so that appropriate promotional offers can be provided, the positive class for the model is churn (1).

**Problem Statement**  

The company currently lacks a systematic way to identify customers who are at risk of churning. As a result, retention promos are often sent broadly and inefficiently, increasing marketing costs while failing to reach customers who truly need intervention. This inefficiency leads to unnecessary spending and missed opportunities to prevent revenue loss.  

To address this, the company needs a machine learning model that can predict each customer's likelihood of churn.

**Goals**  

- Build a classification model to identify customers likely to churn.  
- Generate churn probability scores to help prioritize retention efforts.  
- Minimize false negatives, ensuring customers who are at risk of churning are not overlooked.

**Analytic Approach**

- Conducting Exploratory Data Analysis (EDA) to understand churn patterns and customer behavior.
- Performing data cleaning, handling missing values, encoding categorical variables, and treating imbalance.
- Training multiple classification models (Logistic Regression, Decision Tree, Random Forest, XGBoost, LightGBM, KNN, GradientBoosting, SVM).
- Using SMOTE or oversampling techniques to address class imbalance.
- Evaluating and comparing models using relevant metrics.
- Selecting the best-performing model.

**Metric Evaluation**

- Type 1 Error (False Positive)
The model predicts that a customer will churn when in reality they will not.  
**Consequence:** promotional offers are sent to customers who do not need them, leading to unnecessary marketing expenses and reduced efficiency in the retention strategy. Although this results in wasted budget, it does not directly harm long-term revenue because these customers were not going to leave.

- Type 2 Error (False Negative)
The model predicts that a customer will not churn when in fact they will.  
**Consequence:** truly at-risk customers do not receive retention promotions, causing missed opportunities to prevent churn and potential revenue loss. This outcome is more detrimental to the business, as losing customers directly impacts long-term profitability.  

Given these consequences, **reducing False Negatives is more critical**. The company’s main objective is to accurately identify customers who are likely to churn so that timely and targeted promotions can be deployed.  

Therefore, the primary evaluation metric selected for this case is **Recall**, which measures the model’s ability to correctly capture actual churners and minimize false negatives.
