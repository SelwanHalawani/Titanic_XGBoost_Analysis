# Using XGBoost Model for Predicting Titanic Passenger Survival
## Project Overview
This project uses machine learning to analyze Titanic passenger data and predict survival outcomes. It includes preprocessing, handling missing values, and applying models like ***XBoost***, ***KNN***, and ***Decision Tree***. Models are evaluated and compared using metrics to identify the most effective algorithm for the dataset.

## Table of Contents

[1. Introduction](#1--introduction)

[2- Problem Definition](#2--problem-definition)

[3- Dataset Description](#3--dataset-description)

[4- Feature Engineering](#4--feature-engineering)

[5- Models and Techniques](#5--models-and-techniques)

[6- Evaluation Metric](6--evaluation-metric)

[7- Results](#7--results)

[8- Challenges](#8--challenges)

[9- Conclusion](#9--conclusion)

[10- References](#10--references)

________________________________________
## 1. Introduction
The 1912 Titanic disaster, one of the most infamous maritime tragedies, resulted in significant loss of life. This project leverages a historical dataset containing details about Titanic passengers, such as age, gender, ticket class, and survival status. The objective is to predict passenger survival using machine learning techniques. The project demonstrates how predictive analytics can provide meaningful insights into historical events by understanding patterns and relationships within the dataset.
## 2- Problem Definition
### The task is a binary classification problem: 
predicting whether a passenger survived (1) or did not survive (0) based on various characteristics.
## 3- Dataset Description
**Source:** [Kaggle's Titanic Dataset](https://www.kaggle.com/competitions/titanic/data?select=train.csv)

**Features :**

•	**Demographic:** Age, Sex

•	**Socioeconomic:** Pclass, Fare

•	**Family:** SibSp (siblings/spouses), Parch (parents/children)

•	**Travel:** Embarked, Ticket, Cabin

•	**Target Variable:** Survived (0 = Not Survived, 1 = Survived)

**Data Characteristics:**

•	**Rows:** 891

•	**Columns:** 12 (reduced after preprocessing)

## 4- Feature Engineering
### Handling Missing Values :

•	**Age & Fare:** Median imputation.

•	**Embarked:** Mode imputation.

### Encoding Categorical Variables :

•	**Sex:** Binary encoding.

•	**Embarked:** One-hot encoding.

### Irrelevant Features Removed :

•	**Passengerld**, **Name**, **Ticket**, **Cabin**.

### Scaling :

•	StandardScaler applied to numerical features

### Balancing Data :

•	Class weights were used to address the imbalance in the target variable, ensuring fair representation of both classes during training

## 5- Models and Techniques

•	***XGBoost:*** A gradient boosting framework with hyperparameter tuning (GridSearchCV).

•	***K-Nearest Neighbors (KNN):*** Distance-based classification with k=5.

•	***Decision Tree:*** Hierarchical splitting for predictions.

## 6- Evaluation Metrics
**Models were evaluated based on :**

•	Accuracy

•	Precision

•	Recall

•	F1-Score

•	AUC-ROC

## 7- Results
### Best Model :
•	XGBoost outperformed others with balanced precision and recall.

   ![Model Performence](https://github.com/user-attachments/assets/5131976d-8ab2-4788-9c0b-ae33881c7630)

   ![ROC Curves](https://github.com/user-attachments/assets/1c1aa229-482b-46c8-9b4b-59833a501f33)

 
### Overfitting Addressed :
•	Hyperparameter tuning reduced the training-test accuracy gap.

•	Before Tuning

  ![Before Tuning](https://github.com/user-attachments/assets/7acea44d-027c-49dd-b5d9-3b0de3f0eed3)

 
•	After tuning

  ![After Tuning](https://github.com/user-attachments/assets/eadaaaa1-7e1f-4dc2-8730-ff8ef002ca24)

### Performance Highlights :

•	Improved generalization

•	Balanced class predictions with class weights

  ![Balancing](https://github.com/user-attachments/assets/a0cb63d1-97b2-4853-87d0-f4e5d7c0d172)

 
## 8- Challenges
### Handling Missing Data:

•	Required manual imputation despite XGBoost's default capabilities.

### Overfitting:

•	Addressed via hyperparameter tuning (e.g., regularization techniques).

### Class Imbalance:

•	Managed using class weights for improved model robustness.

## 9- Conclusion
The study demonstrated the effectiveness of machine learning in predictive tasks. ***XGBoost*** emerged as the superior model, achieving high accuracy and generalization.
## 10- References
**Kaggle Titanic Dataset:** [Kaggle's Titanic Dataset](https://www.kaggle.com/competitions/titanic/data?select=train.csv)

**Key Publications:**

•	"***XGBoost:*** A Scalable Tree Boosting System" - Chen & Guestrin, 2016

•	Scikit-learn Documentation
