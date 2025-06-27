# Credit Card Fraud Detection using Machine Learning

## 📌 Overview

This project focuses on **detecting fraudulent credit card transactions** using machine learning techniques. With the increasing prevalence of online and card-based payments, identifying fraudulent activity is critical for both **financial institutions** and their **customers**.

We utilize a real-world dataset made available through a research collaboration between **Worldline** and the **Machine Learning Group**, featuring transactions by European cardholders.

---

## 🧠 Problem Statement

The goal is to build a machine learning model that can **accurately identify fraudulent transactions**. Out of **284,807** total transactions in the dataset, only **492 are fraudulent**, making this a highly **imbalanced classification problem**.

---

## 💼 Business Context

Banking fraud is a serious concern causing **financial losses**, **trust issues**, and **reputation damage**. With fraud losses projected to reach \$30 billion by 2020 (Nilson Report), banks must proactively detect and prevent unauthorized transactions.

Machine learning can **automate detection**, reduce **manual reviews**, and minimize **false positives** that inconvenience legitimate customers.

---

## 🔍 Data Description

* **Total Transactions:** 284,807
* **Fraudulent Transactions:** 492 (0.172%)
* **Features:**

  * `Time`: Seconds since the first transaction
  * `Amount`: Transaction value
  * `V1` to `V28`: Principal components from PCA to ensure confidentiality
  * `Class`: Target variable (1 = Fraud, 0 = Not Fraud)

---

## 📈 Project Pipeline

1. **Data Understanding**
   Load and inspect the structure of the dataset.

2. **Exploratory Data Analysis (EDA)**
   Analyze feature distributions and detect skewness. No Z-scaling needed due to PCA.

3. **Train/Test Split**
   Use **k-fold cross-validation** with a balanced representation of the minority class.

4. **Model Building & Hyperparameter Tuning**
   Train multiple machine learning models (e.g., Logistic Regression, Random Forest, XGBoost). Apply sampling techniques like **SMOTE** or **undersampling** to handle imbalance.

5. **Model Evaluation**
   Evaluate using metrics such as:

   * **Precision**
   * **Recall**
   * **F1-Score**
   * **ROC-AUC**
     Focus is on **maximizing detection of fraud** (Recall) without too many false positives.

---

## 🛠 Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn
* Imbalanced-learn (for sampling techniques)

---

## 📁 Dataset Source

The dataset can be downloaded from [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

---

## ⚠️ Note

Due to class imbalance, traditional accuracy is **not a good performance indicator**. The focus is on catching as many fraudulent transactions as possible while minimizing false alarms.

---

## 📌 Conclusion

This project provides a machine learning-based solution to detect fraudulent credit card transactions. By applying proper handling of imbalanced data and using effective evaluation metrics, banks can deploy better fraud prevention mechanisms and ensure customer trust.

