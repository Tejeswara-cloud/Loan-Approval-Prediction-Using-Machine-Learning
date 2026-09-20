# 🏦 Loan Approval Prediction Using Machine Learning

## 📌 Project Overview

This project develops a supervised machine learning system to predict whether a loan application will be **approved or rejected** based on borrower and loan-related information.

The project focuses on data preprocessing, handling missing values, categorical encoding, feature scaling, class imbalance handling using **SMOTE**, and comparing multiple machine learning algorithms.

---

## 🎯 Objectives

* Clean and preprocess loan application data.
* Handle missing values and inconsistent data.
* Encode categorical variables.
* Scale numerical features.
* Handle class imbalance using SMOTE.
* Compare multiple classification algorithms.
* Evaluate models using Precision, Recall, F1-Score, and ROC-AUC.
* Select the best-performing model.
* Optimize the prediction threshold.
* Provide business-oriented insights for loan approval decisions.

---

## 📂 Dataset

https://www.kaggle.com/datasets/bhanupratapbiswas/loan-approval-prediction-case-study

The dataset contains information about loan applicants, including:

* Gender
* Marital Status
* Number of Dependents
* Education
* Self-Employment Status
* Applicant Income
* Coapplicant Income
* Loan Amount
* Loan Amount Term
* Credit History
* Property Area
* Loan Status

### Target Variable

`Loan_Status`

* `1` → Loan Approved
* `0` → Loan Rejected

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Imbalanced-learn
* Matplotlib
* Seaborn
* Joblib
* Jupyter Notebook

---

## 🔄 Project Workflow

```text
Data Collection
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
Train-Test Split
      ↓
Categorical Encoding
      ↓
Feature Scaling
      ↓
SMOTE Class Balancing
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Comparison
      ↓
Threshold Optimization
      ↓
Final Model Selection
      ↓
Business Interpretation
```

---

## 🤖 Machine Learning Algorithms

Three classification algorithms were trained and compared:

### 1. Logistic Regression

Used as an interpretable baseline model and selected as the final model based on overall performance.

### 2. Decision Tree

Used to capture nonlinear relationships between borrower characteristics and loan approval.

### 3. Random Forest

Used as an ensemble tree-based model to improve robustness and capture complex feature relationships.

---

## ⚖️ Handling Class Imbalance

The target classes were analyzed for imbalance.

**SMOTE (Synthetic Minority Over-sampling Technique)** was applied to the training data to improve representation of the minority class.

SMOTE was applied only to the training set to avoid data leakage into the test set.

---

## 📊 Model Evaluation

The models were evaluated using:

| Metric    | Purpose                                                 |
| --------- | ------------------------------------------------------- |
| Precision | Measures the correctness of positive predictions        |
| Recall    | Measures how many actual positive cases were identified |
| F1-Score  | Balances precision and recall                           |
| ROC-AUC   | Measures overall classification discrimination          |
| Accuracy  | Measures overall prediction correctness                 |

---

## 🏆 Model Comparison

| Model                   |  Precision |     Recall |   F1-Score |    ROC-AUC |
| ----------------------- | ---------: | ---------: | ---------: | ---------: |
| **Logistic Regression** | **85.23%** |     88.24% | **86.71%** | **87.03%** |
| Random Forest           |     83.52% | **89.41%** |     86.36% |     82.07% |
| Decision Tree           |     83.75% |     78.82% |     81.21% |     76.11% |

---

## 🥇 Final Model

### Logistic Regression

Logistic Regression was selected as the final model because it achieved the strongest overall balance across the evaluation metrics.

Key results:

* **Precision:** 85.23%
* **Recall:** 88.24%
* **F1-Score:** 86.71%
* **ROC-AUC:** 87.03%

It also provides better interpretability, which is important for understanding factors influencing loan approval predictions.

---

## 🎯 Threshold Optimization

Instead of relying only on the default probability threshold of `0.50`, multiple thresholds were evaluated.

The threshold was optimized by analyzing the trade-off between:

* Precision
* Recall
* F1-Score

This approach helps support a more business-oriented deployment decision.

---

## 💼 Business Interpretation

The model can assist financial organizations in evaluating loan applications by identifying patterns associated with loan approval.

Potential business benefits include:

* Faster preliminary loan screening.
* More consistent application evaluation.
* Identification of important borrower characteristics.
* Reduction of manual screening workload.
* Support for data-driven lending decisions.

The model should be treated as a **decision-support tool**, rather than the sole basis for approving or rejecting a loan.

---

## 📈 Visualizations

The project includes:

* Loan approval distribution
* Credit history vs loan approval
* Education vs loan approval
* Property area vs loan approval
* Class distribution
* Confusion matrices
* Model comparison charts
* ROC curves
* Feature importance
* Threshold optimization analysis

---

## 📁 Project Structure

```text
loan-approval-prediction/
│
├── loan_approval_prediction.ipynb
├── README.md
├── requirements.txt
│
├── loan_model_comparison.csv
├── loan_threshold_analysis.csv
├── loan_feature_importance.csv
│
└── loan_prediction_cleaned.csv
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/loan-approval-prediction.git
```

### 2. Navigate to the project

```bash
cd loan-approval-prediction
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open:

```text
loan_approval_prediction.ipynb
```

Run the cells sequentially.

---

## 🔮 Future Improvements

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
* Cross-validation for more robust model evaluation.
* Testing additional algorithms such as XGBoost.
* Cost-sensitive threshold optimization.
* Deployment using Streamlit or Flask.
* Development of an interactive loan prediction interface.
* Model monitoring after deployment.

---

## 👨‍💻 Author

**Tejeswara**

This project was developed as part of a practical machine learning and data analytics portfolio.

---

## ⭐ Conclusion

The project demonstrates an end-to-end machine learning workflow for loan approval prediction, from data preprocessing and class imbalance handling to model comparison, evaluation, threshold optimization, and business interpretation.

**Final Model: Logistic Regression 🏆**
