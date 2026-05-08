# 🏦 Bank Marketing Subscription Predictor

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)
![Accuracy](https://img.shields.io/badge/Accuracy-79%25-green.svg)
![Recall](https://img.shields.io/badge/Recall-84%25-brightgreen.svg)

## 📋 Project Overview
This project uses a **Decision Tree Classifier** to predict whether a customer will subscribe to a bank term deposit based on demographic and behavioral data. Using the classic **Bank Marketing Dataset (UCI)**, the goal is to provide the bank with a strategic "Sales Ruleset" to maximize marketing ROI.

## 🚀 The Pipeline
1. **Data Loading:** Importing the dataset from the UCI Repository.
2. **Data Cleaning:** - Handled missing values (labeled as `unknown`).
   - Fixed `pdays` logic (converting `999` to `-1`).
3. **Feature Engineering:** - One-Hot Encoding for categorical variables.
   - Binary mapping for the target variable.
4. **Class Balancing:** Utilized `class_weight='balanced'` to address the high number of non-subscribers.
5. **Modeling:** Trained a `DecisionTreeClassifier` with `max_depth=6`.
6. **Evaluation:** Detailed analysis using Accuracy, Precision, and Recall.

## 📊 Key Results
The model is optimized for **Recall**, ensuring the bank finds as many potential subscribers as possible.

| Metric | Result |
| :--- | :--- |
| **Training Accuracy** | 80.73% |
| **Testing Accuracy** | 79.04% |
| **Recall (Subscribers)** | **0.84** |
| **Precision (Subscribers)** | 0.75 |

> **Insight:** The small gap (1.69%) between Training and Testing accuracy proves that the model is highly stable and generalizes well to new data.

## 💡 Strategic Insights
* **Engagement:** `duration` is the highest predictor of success.
* **Loyalty:** Clients who subscribed in previous campaigns (`poutcome_success`) are significantly more likely to subscribe again.
* **Focus:** By following the Decision Tree rules, the bank can identify **84%** of all potential subscribers while avoiding 75% of uninterested leads.

## 💻 How to Run
1. Clone this repository.
2. Install dependencies:
   ```bash
   pip install pandas scikit-learn seaborn matplotlib
