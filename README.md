# Challenge-20 report

Overview of the Analysis
In this analysis, we aimed to build and evaluate machine learning models to predict the likelihood of a loan being classified as either "healthy" (label 0) or "high-risk" (label 1). The purpose of this analysis is to help financial institutions assess the risk associated with lending decisions, thereby mitigating potential losses from high-risk loans.

Financial Information and Prediction Target
The dataset contained financial information related to loans, including various attributes that can influence loan performance. The primary task was to predict whether a loan is high-risk (1) or healthy (0).

Variables and Initial Exploration
Target Variable: Loan status (0 for healthy, 1 for high-risk).
Feature Variables: Various financial metrics and attributes relevant to the loans.
Class Distribution:
python
print(lending_data_df['loan_status'].value_counts())
loan_status
0    75036
1     2500
Name: count, dtype: int64
This indicates an imbalanced dataset, with a majority of loans being healthy.

Machine Learning Process
The machine learning process involved the following stages:

Data Preprocessing:

Read the dataset.
Separate features (X) and labels (y).
Split the data into training and testing sets using train_test_split.
Model Selection and Training:

Chose LogisticRegression for its simplicity and effectiveness in binary classification tasks.
Trained the logistic regression model on the training set.
Evaluation:

Made predictions on the testing set.
Evaluated model performance using confusion matrix and classification report metrics, including accuracy, precision, and recall.
Methods Used
Logistic Regression: A linear model for binary classification tasks, effective and easy to interpret.
Evaluation Metrics: Accuracy, Precision, Recall, F1-score, and Confusion Matrix.
Results
Machine Learning Model 1: Logistic Regression
Accuracy: 0.99
Precision and Recall Scores:
Class 0 (Healthy Loan):
Precision: 1.00
Recall: 0.99
F1-score: 1.00
Class 1 (High-Risk Loan):
Precision: 0.86
Recall: 0.94
F1-score: 0.90
Summary
Model Performance and Recommendation
The logistic regression model performs exceptionally well, with an overall accuracy of 99%. It achieves near-perfect precision and recall for healthy loans (class 0) and strong performance for high-risk loans (class 1) with an F1-score of 0.90.

Performance Considerations
Importance of Predicting High-Risk Loans: In financial applications, correctly identifying high-risk loans is crucial to avoid potential losses. While the model has a high recall (0.94) for high-risk loans, its precision (0.86) indicates some false positives.
Balanced Performance: The model maintains a good balance between predicting healthy and high-risk loans, making it a reliable choice for practical use.
Recommendation
Given its high accuracy and balanced performance, the logistic regression model is recommended for predicting loan status. The model's ability to accurately identify high-risk loans makes it valuable for mitigating financial risks associated with lending decisions.


I got help from class and Chatgpt for the coding.
