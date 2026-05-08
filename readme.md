# Telco Customer Churn Analysis

## Problem Statement
Customer churn remains a major challenge in the telecommunications industry. Telecom companies often struggle to identify customers who are likely to discontinue their services owing to factors such as charges, contract type, and tenure. Without a  predictive model, businesses may fail to implement timely retention strategies for at-risk customers, which ultimately affect their revenues and business continuity


## Project Overview
In this project I have analysed customer churn in a historical dataset of a telecommunications company and developed predictive models to identify at-risk customers. Most importantly,the key objective is to provide actionable insights and recommendations to reduce churn and improve customer retention.

To achieve this, I performed a number of tasks which are highlighted in the workflow section. 


## Language and Libraries
- Python
- Pandas
- Matplotlib
- SckitLearn


## Dataset
The project uses the following dataset:
- `Telco_Customer_Churn_Dataset.csv`

The dataset include attributes, including gender, tenure, senior citizen status, monthly charges, total charges, payment method contract types, diverse subscription services, and churn category.  


## Workflow
This includes the following steps:

### Task 1: Data Preparation
Loading and preprocess the dataset, and EDA

1. **Data loading**: Importing required libraries, loading the dataset into a Pandas DataFrame.

2. **Exploratory Data Analysis (EDA)** 
- Previewing dataset records
- Inspecting dataset structure and data types
- Checking descriptive statistics
- Checking for missing values and duplicates
- Performing grouped analysis on churn, tenure, monthly charges, gender, and contract types Senior Citizenship.
- Visualising trends and relationships with plots.

### Tasks 2: Feature Selection
Selecting relevant features influencing churn prediction

1. **Features**: The feature variables used to train the machine learning model are `tenure`,`MonthlyCharges`, `SeniorCitizen`, `Contract`.
2. **Target**: The target variable is `Churn`.

Label encoding is applied on categorical columns of the features  while the lambda function is used to convert the `Churn` categories in binary formats.

### Tasks 3: Train-Test Split and Feature Scaling
Dividing the data into training (80%) and testing (20%) sets for model training and evaluation. Also, performing feature scaling

### Tasks 4 -6: Model Selection, Training and Evaluation
Choosing a suitable binary classification algorithm. Training the model. Evaluating model's performance

The classification algorithm used are:
- Logistic regression
- DecisionTree classifier
- RandomForest classifier
- XGB Classifier

The performance metrics used for the models evaluation are:
- Accuracy score,
- Precision
- Recall
- F1-score


## Results

*XGB Classifier model* performs best with

**Accuracy score** of 0.8055358410220014

Classification Report: 
               precision    recall  f1-score   support

           0       0.85      0.90      0.87      1049
           1       0.65      0.52      0.58       360

    accuracy                           0.81      1409
   macro avg       0.75      0.71      0.73      1409
weighted avg       0.80      0.81      0.80      1409


## Recommendations

### Business Recommendations
1. Retention efforts should be focused on short-tenure customers. Customers early in their subscription lifecycle are more likely to churn.

2. Higher monthly charges may contribute to churn. Hence, review pricing strategies. 

3. Encourage one year and two year contracts. Customers on long-term contracts are more stable.


### Machine Learning Recommendations

1. Adding more evaluation metrics including Confusion Matrix.

2. Non churn customer are far more than churn customers. Therefore, addressing this imbalance using SMOTE or class weight can improve churn predicion quality

3. Deploying the best performing model (XGB model) for use.


## Installation

Clone the repository:
```bash

```

## License

This project is released under the MIT License.