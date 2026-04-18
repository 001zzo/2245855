Project Title : Water Potability Prediction
Introduction
This project aims to predict whether water is safe to drink based on its chemical properties. The dataset includes features such as pH, hardness, solids, and other indicators of water quality. The problem is formulated as a binary classification task, where 0 represents non-drinkable water and 1 represents drinkable water.
Machine learning models are applied to identify patterns in the data and make predictions. The project follows a complete machine learning pipeline, including data exploration, preprocessing, model building, and evaluation. Different models are compared to determine the most effective approach for this task.
The final model is tested on unseen data to evaluate its performance and reliability.

Business objectives
The main objective of this project is to build a reliable model that can predict water potability. The goal is to correctly classify water samples and improve the detection of drinkable water (class 1). Since this is a classification problem, the focus is not only on accuracy but also on the model’s ability to correctly identify both classes.

ML Pipeline
The machine learning pipeline starts with data collection and ends with evaluating the model on unseen data. Each step is designed to ensure that the model performs reliably and generalizes well.

1. Data collection
The dataset was obtained from Kaggle and contains 3276 samples with 10 features. The data was loaded using pandas and checked for consistency using methods such as info() and describe(). Missing values were identified and handled by replacing them with the mean of each column. The dataset was then split into training and testing sets using an 80/20 ratio.

2. EDA
The dataset was explored using basic statistical methods. It was observed that some features contain missing values and that all variables are numerical. The target variable is binary, but the dataset is slightly imbalanced, with more non-drinkable samples than drinkable ones. This imbalance affects model performance and must be considered during modeling.

3. Model building
Two main models were used in this project:
Logistic Regression (baseline model)
Random Forest (main model)
Logistic Regression was chosen as a simple baseline to understand the data. However, it performed poorly due to the non-linear nature of the dataset.
Random Forest was selected because it can capture complex patterns and interactions between features. Hyperparameters such as the number of trees (n_estimators) and tree depth (max_depth) were adjusted to improve performance.

4. Model evaluation
Models were evaluated using:
Accuracy
Confusion Matrix
Classification Report (precision, recall, F1-score)
The Logistic Regression model showed weak performance, especially for detecting drinkable water. Random Forest significantly improved accuracy and provided a better balance between classes.
Hyperparameter tuning slightly improved accuracy, but did not significantly enhance detection of class 1. This indicates that further improvement may require more advanced techniques or feature engineering.

5. Prediction
The final model was tested on unseen data from the test set. Additionally, a single sample prediction was performed to demonstrate how the model works in practice. The predicted value was compared with the actual value, confirming that the model can make correct predictions on new data.