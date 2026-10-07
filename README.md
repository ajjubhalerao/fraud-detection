# Fraud Detection using Machine Learning

## Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning techniques.

The dataset is highly imbalanced, with fraudulent transactions representing only a very small percentage of all transactions. Therefore, appropriate evaluation metrics such as Precision, Recall, F1-Score, and AUC-ROC are used instead of relying only on accuracy.

## Dataset

The project uses the **Credit Card Fraud Detection** dataset from Kaggle.

The dataset contains:

- 284,807 transactions
- 284,315 normal transactions
- 492 fraudulent transactions
- 28 anonymized features (V1–V28)
- Transaction Time
- Transaction Amount
- Class as the target variable

Where:

- `0` = Normal transaction
- `1` = Fraudulent transaction

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Workflow

1. Load and explore the dataset
2. Check missing values
3. Analyze class imbalance
4. Perform exploratory data analysis
5. Analyze transaction amounts
6. Analyze fraudulent transactions by hour
7. Split data using stratified train-test split
8. Handle class imbalance using SMOTE
9. Train Logistic Regression
10. Train Random Forest
11. Evaluate model performance
12. Analyze feature importance
13. Analyze confusion matrix
14. Evaluate ROC-AUC
15. Discuss scalability for high-volume transactions

## Models Used

### Logistic Regression

- Precision: 11.61%
- Recall: 89.80%
- F1-Score: 20.56%
- AUC-ROC: 97.53%

### Random Forest

- Precision: 84.54%
- Recall: 83.67%
- F1-Score: 84.10%
- AUC-ROC: 97.95%

## Model Comparison

Random Forest provided a better balance between Precision and Recall compared with Logistic Regression.

Although Logistic Regression achieved slightly higher Recall, its Precision was very low, resulting in many false positive fraud alerts.

Random Forest achieved strong Precision, Recall, F1-Score, and AUC-ROC, making it the preferred model in this project.

## Feature Importance

The most important features identified by the Random Forest model were:

1. V14
2. V10
3. V4
4. V12
5. V11

## Handling Class Imbalance

SMOTE (Synthetic Minority Over-sampling Technique) was applied to the training data to balance the minority fraud class.

The test data was kept unchanged to provide a realistic evaluation of model performance.

## Important Evaluation Metrics

**Recall** is important because missing a fraudulent transaction can result in financial loss.

**Precision** is also important because too many false positive alerts can inconvenience genuine customers.

Therefore, a practical fraud detection system should maintain a good balance between Precision and Recall.

## Scalability

For handling very large transaction volumes such as 1 million transactions per hour, the system could be scaled using:

- Real-time prediction APIs
- Apache Kafka
- Apache Spark
- Parallel processing
- Cloud infrastructure
- Auto-scaling
- Model monitoring and periodic retraining

## Dataset Source

Kaggle - Credit Card Fraud Detection

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

## Project Files

```text
Fraud_Detection/
│
├── .gitignore
├── fraud_detection.ipynb
└── creditcard.csv
