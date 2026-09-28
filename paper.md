# Heart Disease Prediction Using Machine Learning

## Abstract

Heart disease is one of the major health concerns worldwide, making early risk prediction an important area of research. This study investigates the use of machine learning models for predicting the presence of heart disease using clinical patient data. The study uses the UCI Heart Disease dataset and applies data preprocessing techniques, including handling missing values, feature preparation, and stratified train-test splitting. Two supervised machine learning models, Logistic Regression and Random Forest, are trained and evaluated. Model performance is assessed using accuracy, precision, recall, and F1-score. The experimental results provide a comparison of the predictive performance of the two models and demonstrate the potential of machine learning for supporting heart disease risk prediction. The findings also highlight the importance of appropriate preprocessing and model evaluation when working with clinical datasets.

## 1. Introduction

Heart disease is a major health concern and early identification of individuals at risk can support timely clinical assessment and treatment. Machine learning has been increasingly investigated for heart disease prediction because it can learn patterns from clinical data and use these patterns to classify patients according to their risk or disease status. The UCI Heart Disease dataset is a commonly used dataset for this type of classification problem and contains clinical attributes that can be used to predict the presence of heart disease.

Previous studies have investigated several machine learning techniques for heart disease classification. The literature reviewed for this study shows that models such as Logistic Regression, Random Forest, Support Vector Machine, and K-Nearest Neighbors can be applied to structured clinical data. Research comparing different machine learning approaches also demonstrates that model performance can vary depending on the characteristics of the dataset, preprocessing procedures, and evaluation methods. These findings motivate the comparison of multiple machine learning models rather than relying on a single algorithm.

This study focuses on predicting the presence of heart disease using the UCI Heart Disease dataset. Logistic Regression and Random Forest are selected as the two classification models for the experiment. The data are preprocessed before model training, and the models are evaluated using accuracy, precision, recall, and F1-score.

The research question addressed in this study is: **How effectively can Logistic Regression and Random Forest predict the presence of heart disease using the UCI Heart Disease dataset?** The study aims to compare the performance of these two models and examine their potential for heart disease prediction using structured clinical data.

Methodology

1. Research Question

Can machine learning models predict the presence of heart disease using clinical features from the UCI Heart Disease dataset?

2. Dataset Description

The UCI Heart Disease dataset contains 303 patient records and 13 input features. The features include age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting electrocardiographic results, maximum heart rate, exercise-induced angina, ST depression, slope, number of major vessels, and thalassemia-related information.

The target variable represents the diagnosis of heart disease. For this experiment, the target will be converted into a binary classification problem:

0 = absence of heart disease
1 = presence of heart disease
The dataset contains both numerical and categorical variables. Some variables contain missing values, particularly the ca and thal features.

3. Data Cleaning Plan

The following preprocessing steps will be performed:

Load the UCI Heart Disease dataset.
Check the dataset shape and data types.
Identify missing values.
Replace missing values using median imputation.
Convert the target into binary form.
Separate input features from the target variable.
Split the data into training and testing sets.
Use stratified splitting to maintain similar class proportions in both sets.
Standardize features for Logistic Regression.
4. Feature Engineering

The original clinical variables will be used as model features. No unnecessary features will be created because the dataset is relatively small.

Categorical variables are represented numerically in the UCI dataset. Numerical feature scaling will be applied for Logistic Regression because it can help the model operate more consistently when variables have different numerical ranges.

Random Forest does not require feature scaling, but the experiment will use an appropriate preprocessing pipeline to avoid data leakage.

5. Train-Test Split

The dataset will be divided into:

80% training data
20% testing data
A fixed random state will be used so that the experiment is reproducible.

6. Machine Learning Models

Two machine learning classification models will be trained.

Logistic Regression

Logistic Regression will be used as a baseline classification model. It is suitable for binary classification and provides a relatively simple model for comparison.

Random Forest

Random Forest will be used as a second model. It combines multiple decision trees and can model nonlinear relationships between clinical features and the target.

Using two different algorithms allows their performance to be compared on the same test data.

7. Evaluation Metrics

The models will be evaluated using:

Accuracy
Precision
Recall
F1-score
ROC-AUC
Confusion Matrix
Accuracy measures the overall proportion of correct predictions. Precision measures the proportion of predicted positive cases that are actually positive. Recall measures how many actual positive cases are correctly identified. F1-score combines precision and recall. ROC-AUC measures the model's ability to distinguish between the two classes.

8. Limitations

The dataset is relatively small, containing 303 records. Therefore, model performance may vary depending on the train-test split. The dataset also represents a limited population and should not be treated as sufficient for clinical deployment. The experiment is intended for educational machine-learning research rather than medical diagnosis.

9. Expected Outcome

The experiment will compare Logistic Regression and Random Forest using the same dataset and evaluation metrics. The final conclusion will be based on the measured test-set results rather than assuming that one model will perform better before the experiment is conducted.
