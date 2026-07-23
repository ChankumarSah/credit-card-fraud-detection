# 💳 Credit Card Fraud Detection using Machine Learning
## 💳 Business-Focused Fraud Detection & Risk Scoring System

📌 **End-to-End Project:** Python → Data Analysis → Feature Engineering → Machine Learning → Model Serialization (Joblib)

⭐ **Highlight:** Built a fraud detection system capable of identifying high-risk credit card transactions using Machine Learning while addressing an extremely imbalanced dataset.

---

# 🚀 Project Overview

This project is an end-to-end Machine Learning solution developed to detect fraudulent credit card transactions and minimize financial losses caused by fraud.

The project demonstrates the complete machine learning workflow from data preprocessing to model deployment readiness.

📊 Dataset includes:

- Credit card transaction records
- Transaction amount
- Time-based transaction information
- PCA-transformed transaction features
- Fraud labels

### 🎯 Project Goals

- Detect fraudulent transactions
- Handle highly imbalanced data
- Build a reusable Machine Learning pipeline
- Evaluate fraud detection performance
- Save the trained model using Joblib
- Prepare the model for deployment

---

# 🎯 Business Problem

Credit card fraud causes millions of dollars in financial losses every year.

Traditional rule-based systems often fail to identify new fraud patterns while generating large numbers of false positives.

### Business Challenges

- Detect fraud accurately
- Reduce financial losses
- Minimize false alarms
- Identify suspicious transactions in real time

### Key Question

**How can Machine Learning identify fraudulent transactions while maintaining high recall and minimizing missed fraud cases?**

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

# 🔄 Data Processing

### Data Cleaning

- Duplicate Check
- Missing Value Verification
- Feature Inspection

### Data Preprocessing

- Train-Test Split
- RobustScaler
- SMOTE (Handling Class Imbalance)

### Feature Engineering

- Feature Scaling
- Data Transformation
- Balanced Training Dataset

---

# 🤖 Machine Learning Models

The following Machine Learning algorithms have been implemented within the project.

| Model | Status |
|--------|--------|
| Logistic Regression | ✅ Successfully Trained |
| Decision Tree | ✅ Pipeline Implemented |
| Random Forest | ✅ Pipeline Implemented |
| XGBoost | ✅ Pipeline Implemented |
| LightGBM | ✅ Pipeline Implemented |

---

# ⚠ Hardware Limitation

The project was developed on a personal laptop with limited RAM and computational resources.

The implementation code and machine learning pipelines for:

- Decision Tree
- Random Forest
- XGBoost
- LightGBM

have been successfully written.

However, training these computationally intensive ensemble models on the complete dataset exceeded the available hardware resources.

Therefore, **Logistic Regression** was selected as the final deployed model because it successfully trained within the available system resources while demonstrating a complete end-to-end machine learning workflow.

The remaining models can be trained on higher-memory environments such as:

- Google Colab Pro
- Kaggle
- AWS
- Azure ML
- Google Cloud Platform

---

# 🔄 Machine Learning Workflow

```text
Dataset
      │
      ▼
Data Cleaning
      │
      ▼
EDA
      │
      ▼
Train-Test Split
      │
      ▼
RobustScaler
      │
      ▼
SMOTE
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Pipeline Creation
      │
      ▼
Model Serialization (Joblib)
```

---

# 📊 Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report

---

# 💾 Model Serialization

The trained Logistic Regression model is saved using Joblib.

```python
import joblib

joblib.dump(
    logistic_pipeline, "logistic_regression_pipeline.pkl"
)
```

Loading the model:

```python
model = joblib.load("logistic_regression_pipeline.pkl")
```

---

# 📁 Project Structure

```text
credit-card-fraud-detection/

│── creditcard_fraud_detection.ipynb

│── logistic_regression_pipeline.pkl

│── requirements.txt

│── README.md

└── app.py )
```

---

# 📊 Key Insights

- Fraudulent transactions represent only a very small percentage of the dataset.
- Handling class imbalance is essential for reliable fraud detection.
- Logistic Regression provides strong recall for fraud detection while remaining computationally efficient.
- Machine Learning pipelines simplify preprocessing and deployment.

---

# 💡 Business Recommendations

- Deploy fraud detection as an early warning system.
- Prioritize high-recall models to reduce missed fraud cases.
- Continuously retrain the model using updated transaction data.
- Deploy on scalable cloud infrastructure for larger datasets.

---

# 🎯 Project Impact

✔ Built a complete fraud detection pipeline

✔ Addressed severe class imbalance using SMOTE

✔ Implemented reusable Machine Learning pipelines

✔ Serialized the trained model using Joblib

✔ Created a deployment-ready Machine Learning workflow

---

# ⭐ Future Enhancements

- Streamlit Deployment
- Flask REST API
- Docker Containerization
- Hyperparameter Optimization
- Cross Validation
- Threshold Optimization
- SHAP Explainability
- Cloud Deployment
- Train Random Forest
- Train XGBoost
- Train LightGBM

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/credit-card-fraud-detection.git
```

Navigate to the project

```bash
cd credit-card-fraud-detection
```

Install dependencies

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

---


# 📊 Model Performance

The final deployed model is **Logistic Regression**, trained on a preprocessed dataset using **RobustScaler** and **SMOTE** to address class imbalance.

| Metric | Score |
|---------|-------|
| Accuracy | **99.11%** |
| Precision | **14.11%** |
| Recall | **85.26%** |
| F1-Score | **24.22%** |
| ROC-AUC | **96.07%** |

---

## 📋 Classification Report

| Class | Precision | Recall | F1-Score | Support |
|-------|----------:|-------:|---------:|--------:|
| Legitimate (0) | **1.00** | **0.99** | **1.00** | **56,651** |
| Fraud (1) | **0.14** | **0.85** | **0.24** | **95** |

**Overall Accuracy:** **99.11%**

---

## 📉 Confusion Matrix

| Actual \ Predicted | Legitimate | Fraud |
|-------------------|-----------:|------:|
| **Legitimate** | **56,158** | **493** |
| **Fraud** | **14** | **81** |

---

## 📌 Interpretation

- ✅ Correctly identified **81 out of 95 fraudulent transactions**.
- ✅ Achieved a **high Recall (85.26%)**, ensuring most fraudulent transactions were detected.
- ⚠️ Precision is relatively low because fraud detection is an **extremely imbalanced classification problem**, where prioritizing fraud detection (high recall) often results in more false positives.
- ✅ Achieved an **ROC-AUC score of 96.07%**, indicating strong class discrimination capability.
- ✅ The model correctly classified **56,158 legitimate transactions**, while only **14 fraudulent transactions** were missed.

---

## 💡 Business Impact

- Detects the majority of fraudulent transactions before financial loss occurs.
- Can be integrated into a real-time fraud monitoring system.
- Supports risk-based transaction review by prioritizing suspicious transactions.
- Helps financial institutions reduce fraud-related losses while maintaining high detection performance.

---

# 👨‍💻 Author

## Chandan Sah

**Data Analyst | Machine Learning Enthusiast | Python | SQL | Power BI**



---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

---

