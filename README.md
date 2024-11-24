# Logistic Regression from Scratch: A Beginner’s Guide in Python

Understanding Customer Churn with Logistic Regression - A Beginner's Project

Customer churn is a critical metric for any business, especially in subscription-based industries. Companies aim to reduce churn to retain their customers and maximize revenue. In this project, we dive into building a Logistic Regression model to predict customer churn, using fundamental techniques and addressing challenges like class imbalance. This blog will walk you through the steps, insights, and solutions we explored to build a robust churn prediction model.


Project Objective

The primary goal of this project is to create a Logistic Regression model that predicts whether a customer will churn (1) or stay (0) based on their historical data.


Dataset Overview

The dataset consists of customer activity and demographic details, with features such as:

Age: Age of the customer.
Number of days subscribed: Total days the customer has been subscribed.
Weekly minutes watched: Time spent on the platform weekly.
Mail subscribed: Whether the customer is subscribed to emails.
Multi-screen: If the customer uses multiple screens.
Customer support calls: Number of times the customer contacted support.
Churn: Target variable indicating whether the customer churned (1) or not (0).

Steps in the Project

1. Data Preparation

Before building the model, we ensured the data was cleaned, missing values were handled, and categorical variables were encoded for analysis. Some key steps included:

Removing unnecessary columns like customer ID and phone numbers.
Encoding categorical variables like gender, multi-screen, and mail subscription into numerical values.

2. Building the Logistic Regression Model

Logistic Regression is a supervised machine learning algorithm used for binary classification tasks. We used StatsModels and Scikit-Learn libraries to fit the model and evaluate its performance. Key metrics like coefficients, p-values, and pseudo R-squared were analyzed to understand the model's behavior.


Insights from the Initial Model

The first Logistic Regression model gave some valuable insights:

Features like age, number of customer support calls, and weekly max night minutes were significant in predicting churn.
However, the model struggled with imbalanced data, where the number of churned customers (1) was far smaller than non-churned customers (0).
Handling Class Imbalance

Class imbalance often causes machine learning models to favor the majority class. We tried several techniques to address this issue:

Class Weights: Adjusted the weights of classes (0 and 1) to give more importance to the minority class.

Oversampling with SMOTE: Used Synthetic Minority Oversampling Technique (SMOTE) to create synthetic samples of the minority class.
Resampling: Rebalanced the dataset by resampling the minority and majority classes to equal sizes.

Model Evaluation

We evaluated the model using:

Classification Report: Metrics like precision, recall, and F1-score for both classes.
ROC Curve: Plotted the Receiver Operating Characteristic (ROC) curve to visualize the model's ability to distinguish between classes.

Key Takeaways:

Age and customer support calls are strong predictors of churn.
Handling class imbalance is critical in churn prediction to ensure the minority class is not ignored.
Techniques like SMOTE and class weighting are effective in improving model fairness.

What's Next?

This project gave us a strong foundation in using Logistic Regression for churn prediction. As a next step, we plan to:

Experiment with more advanced models like Random Forests or XGBoost.
Incorporate more features to improve prediction accuracy.
Deploy the model to predict churn for real-time customer data.