# Bank Marketing Prediction using Logistic Regression
## Overview
This project focuses on predicting whether a customer will subscribe to a term deposit (YES/NO) using a machine learning model.
The dataset contains customer information such as age, job, balance, contact details, and previous campaign data.

## Objective
The main goal is to build a classification model that can:
- Predict customer response (Yes/No)
- Handle imbalanced data
- Evaluate model performance using proper metrics

## Dataset Description
- File: `bank-full.csv`
- Total Records: 45,211
- Features: 16 input features + 1 target variable (`y`)
- Target:
  - `yes` → 1
  - `no` → 0

## Methodology
### 1. Data Loading
- Dataset loaded from Google Drive using `pandas`

### 2. Data Preprocessing
- Converted target variable (`y`) into numeric values (0 and 1)
- Applied **One-Hot Encoding** to categorical features using `pd.get_dummies()`
- Dropped unnecessary columns after encoding

### 3. Train-Test Split
- Split dataset into:
  - 80% Training Data
  - 20% Testing Data

### 4. Feature Scaling
- Used `StandardScaler` to normalize numerical values
- Helps improve model performance

### 5. Model Selection
- Used **Logistic Regression**
- Parameters:
  - `max_iter = 2000`
  - `class_weight = 'balanced'` (to handle imbalanced data)

### 6. Model Training
- Model trained using training dataset

### 7. Prediction
- Predictions made on test dataset

### 8. Evaluation Metrics
Model performance evaluated using:
- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1-score)

## Results
### Accuracy:
- **84.25%**

### Confusion Matrix:
    [[6713 1239]
    [ 185  906]]

### Classification Report:
| Class | Precision | Recall | F1-score |
|------|----------|--------|----------|
| 0 (No) | 0.97 | 0.84 | 0.90 |
| 1 (Yes) | 0.42 | 0.83 | 0.56 |

## Observations
- The model performs well overall with **high accuracy (84%)**
- It predicts **"No" class very accurately**
- It has **high recall (83%) for "Yes" class**, meaning:
  - It can detect most potential customers
- However, **precision for "Yes" is low (42%)**:
  - Some predictions are incorrect (false positives)

## Challenges
- Dataset is **imbalanced** (more "No" than "Yes")
- This affects precision and overall model balance

## Tools & Libraries
- Python
- Pandas
- Scikit-learn
- Google Colab

## Future Improvements
- Try advanced models like:
  - Random Forest
  - XGBoost
- Tune hyperparameters
- Use ROC-AUC score for better evaluation
- Perform feature selection for better accuracy

## Conclusion
This project demonstrates a complete beginner-friendly machine learning pipeline:
- Data preprocessing
- Model training
- Evaluation
The model is effective for predicting customer responses, especially identifying potential customers, but still has room for improvement.
