# AI-ML-Classification-Project

# Customer Churn Prediction using Machine Learning

## Project Overview

This project predicts whether a customer will churn or not using machine learning classification algorithms.

The project covers the complete machine learning workflow, including data preparation, preprocessing, handling class imbalance using SMOTE, model training, evaluation, and hyperparameter tuning using GridSearchCV.

## Dataset

The dataset contains 30 customer records with the following features:

* Age
* Monthly_Charges
* Tenure
* Support_Calls
* Contract
* Churn — Target variable

### Target Variable

* `0` → Customer will not churn
* `1` → Customer will churn

## Machine Learning Models

The following classification algorithms were implemented:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest
* Gradient Boosting
* XGBoost

## Data Preprocessing

The following preprocessing techniques were used:

* Train-Test Split
* Stratified splitting
* StandardScaler for numerical features
* OneHotEncoder for categorical features
* ColumnTransformer
* Pipeline
* SMOTE for handling class imbalance

SMOTE was applied inside the pipeline so that oversampling is performed only on the training data during model training and cross-validation.

## Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Confusion Matrix

Since customer churn is an imbalanced classification problem, **F1 Score and ROC-AUC** were considered important evaluation metrics rather than relying only on accuracy.

## Hyperparameter Tuning

GridSearchCV was used to tune the important hyperparameters of each model.

### Logistic Regression

* C
* Solver

### KNN

* n_neighbors
* weights
* metric

### Decision Tree

* max_depth
* min_samples_split
* min_samples_leaf

### Random Forest

* n_estimators
* max_depth
* min_samples_split
* min_samples_leaf

### Gradient Boosting

* n_estimators
* learning_rate
* max_depth

### XGBoost

* n_estimators
* learning_rate
* max_depth
* subsample

The models were tuned using **5-fold cross-validation** with **F1 score** as the scoring metric.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn
* XGBoost
* Google Colab
* GitHub

## Machine Learning Workflow

```text
Dataset
   ↓
Train-Test Split
   ↓
Feature Separation
   ↓
Scaling + One-Hot Encoding
   ↓
SMOTE
   ↓
Model Training
   ↓
Model Evaluation
   ↓
GridSearchCV
   ↓
Best Model Selection
```

## Project Goal

The main goal of this project is to understand and implement an end-to-end classification machine learning workflow and compare different classification algorithms to identify the best-performing model for customer churn prediction.

## Conclusion

Multiple classification models were trained and evaluated. Hyperparameter tuning was then performed using GridSearchCV to improve model performance.

The final model can be selected based primarily on **F1 Score**, while also considering Precision, Recall, ROC-AUC, and the Confusion Matrix.


