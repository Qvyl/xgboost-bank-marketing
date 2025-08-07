# 📈 Term Deposit Subscription Prediction Using XGBoost

## 🎯 Goal

The goal of this project is to predict whether a bank client will subscribe to a term deposit based on their personal attributes, past interactions, and economic conditions. This is treated as a binary classification problem where the target variable is `result`, indicating whether the client subscribed (`yes - 1`) or not (`no - 0`).

---

## 🗂️ Dataset

This project uses the **Bank Marketing Dataset** from the [UCI Machine Learning Repository].

- **Source**: [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing)
- **Description**: Data collected from phone-based direct marketing campaigns run by a Portuguese banking institution. The dataset includes:
  - **Client data**: age, job, marital status, education, default status, housing loan, personal loan
  - **Campaign data**: number of contacts, last contact duration, days since last contact, outcome of previous campaigns
  - **Economic indicators**: employment variation rate, consumer price index, confidence index, etc.
- **Size**: 41,188 records and 20 input features (in `bank-additional-full.csv`)

The dataset is imbalanced, with significantly more "no" than "yes" outcomes.

---

## ⚙️ Model – XGBoost

I used **XGBoost (Extreme Gradient Boosting)**, a powerful ensemble learning algorithm known for its speed, regularization, and ability to handle structured data well.

### Key Steps:
- **Preprocessing**:
  - Categorical features were encoded using **target encoding**
  - Data was split using **stratified train-test split** to preserve class proportions
- **Training**:
  - The model was trained on the processed data with default or tuned hyperparameters
- **Evaluation**:
  - Model performance was evaluated using metrics such as **precision**, **recall**, **F1-score**, and **ROC AUC**
- **Interpretation**:
  - Feature importance was analyzed to understand which features influenced predictions the most

XGBoost was chosen for its ability to:
- Handle missing data
- Avoid overfitting through regularization (`lambda`, `alpha`)
- Efficiently capture complex interactions in tabular datasets

---

This project demonstrates a full machine learning pipeline—from dataset preparation to model evaluation—using a real-world banking dataset.
