Overview

This project focuses on predicting customer churn using subscription, billing, and service usage data. The objective is to identify customers who are likely to churn in advance so the business can take proactive retention actions instead of reacting after revenue is lost.

Business Problem

Customer churn directly impacts revenue and long-term growth. The goal of this project is to estimate churn likelihood at the customer level and segment customers into Low, Medium, and High risk groups to support targeted retention strategies.

Dataset

The Telco Customer Churn dataset contains customer-level records with information such as tenure, contract type, billing details, subscribed services, and churn status (Yes/No). The dataset includes both numerical and categorical features commonly seen in real-world enterprise data.

Approach
Data Cleaning

Converted TotalCharges to a numeric field and handled missing values

Removed non-predictive identifiers such as customerID

Feature Engineering

Created tenure-based buckets to represent customer lifecycle stages

Applied one-hot encoding to categorical variables for model compatibility

Modeling

Trained and compared Logistic Regression and Random Forest models

Evaluated model performance using Precision, Recall, ROC-AUC, and Confusion Matrix

Threshold Tuning

Tuned the probability threshold instead of using the default 0.5

Optimized for Recall to reduce missed churn customers, aligning with retention use cases

Explainability

Used feature importance to identify key drivers contributing to customer churn

Deployment-Ready Output

Generated churn probabilities and risk segments (Low / Medium / High)

Exported model output for Power BI reporting and analysis

Model Evaluation

The following metrics were used to evaluate model performance:

ROC-AUC to measure overall model discrimination

Precision and Recall to assess churn detection tradeoffs

Confusion Matrix to analyze false positives and false negatives

Key Insights

Customers on month-to-month contracts show significantly higher churn risk

Shorter tenure customers are more likely to churn

Higher monthly charges are often associated with increased churn probability

Risk segmentation helps prioritize retention efforts toward high-risk customers

Power BI Dashboard

The exported scoring file (outputs/churn_scoring_for_powerbi.csv) is designed for Power BI and supports:

Monitoring overall churn rate and high-risk customer volume

Analyzing customers by churn risk segment

Viewing churn probability distribution

Providing an operational list of customers for retention outreach

Project Files

notebooks/churn_model.ipynb – End-to-end data preparation, modeling, and evaluation

outputs/churn_scoring_for_powerbi.csv – Churn probabilities and risk segmentation

powerbi/ – Power BI dashboard file

images/ – Dashboard screenshots

Tech Stack

Python, pandas, scikit-learn, matplotlib, Power BI
