# fluffy-advertisement: Online Shopper Purchase Intentions Prediction

This repository contains a Machine Learning project where various classification models were applied to predict online shoppers' purchase intentions based on a dataset. The dataset provides information about online shoppers' behavior and includes a variety of features that can be used to predict whether a visitor will make a purchase (revenue) or not.

## Dataset Information

The dataset consists of the following information:

- Rows: 12,330
- Columns: 18

### Data Columns

1. Administrative (Numerical)
2. Administrative_Duration (Numerical)
3. Informational (Numerical)
4. Informational_Duration (Numerical)
5. ProductRelated (Numerical)
6. ProductRelated_Duration (Numerical)
7. BounceRates (Numerical)
8. ExitRates (Numerical)
9. PageValues (Numerical)
10. SpecialDay (Numerical)
11. Month (Categorical)
12. OperatingSystems (Numerical)
13. Browser (Numerical)
14. Region (Numerical)
15. TrafficType (Numerical)
16. VisitorType (Categorical)
17. Weekend (Boolean)
18. Revenue (Boolean)

## Data Preprocessing

### Independent Variables

The independent variables used for prediction include:
- Administrative
- Administrative_Duration
- Informational
- Informational_Duration
- ProductRelated
- ProductRelated_Duration
- BounceRates
- ExitRates
- PageValues
- SpecialDay
- Month
- OperatingSystems
- Browser
- Region
- TrafficType
- VisitorType
- Weekend

### Target Variable

The target variable for prediction is "Revenue."

### Data Exploration

Data visualization was performed to understand the relationships between various features and the target variable. Visualizations included graphs to explore the relationship between "Month" and "Revenue," "Weekend" and "Revenue," and "VisitorType" versus ("Administrative_Duration," "Informational_Duration," "ProductRelated_Duration").

### Data Encoding

Categorical data were encoded to make them suitable for machine learning models.

### Feature Scaling

Feature scaling was applied using the StandardScaler to standardize numerical features.

### Data Splitting

The dataset was split into a training set (70%) and a test set (30%) for model evaluation.

## Classification Models

Several classification models were applied to predict online shoppers' purchase intentions:

### Logistic Regression

- Training Accuracy: 0.89
- Testing Accuracy: 0.87

### Naive Bayes

- Training Accuracy: 0.81
- Testing Accuracy: 0.79

### K-Nearest Neighbors (KNN)

- Training Accuracy: 0.89
- Testing Accuracy: 0.87

### Decision Tree

- Training Accuracy: 0.87
- Testing Accuracy: 0.86

### Support Vector Machine (SVM)

- Training Accuracy: 0.89
- Testing Accuracy: 0.87

### Kernel SVM (RBF)

- Training Accuracy: 0.90
- Testing Accuracy: 0.88

### Random Forest

- Training Accuracy: 0.90
- Testing Accuracy: 0.89

## Model Evaluation

The models were evaluated using both training and test data to assess their performance. The Random Forest classification model emerged as the best-performing model with the following evaluation metrics on the test set:

- Confusion Matrix:
  ```
  [[2957  120]
   [ 266  356]]
  ```

- Accuracy Score: 0.8956

- Classification Report:
  ```
                precision    recall  f1-score   support

           0       0.92      0.96      0.94      3077
           1       0.75      0.57      0.65       622

    accuracy                           0.90      3699
   macro avg       0.83      0.77      0.79      3699
  weighted avg     0.89      0.90      0.89      3699
  ```

The Random Forest model achieved the highest accuracy and a reasonable balance between precision and recall for both classes, making it the preferred model for predicting online shoppers' purchase intentions.

Feel free to explore the code and the dataset to gain a deeper understanding of the analysis and model implementation.
