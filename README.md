# Hospital Readmission Prediction

## 📌 Project Overview

This project predicts whether a patient will be readmitted to the hospital within 30 days using **Logistic Regression with L2 regularization**.

The project demonstrates a complete machine learning workflow including data preparation, exploratory data analysis, feature preprocessing, model training, evaluation using ROC-AUC, and analysis of false positives and false negatives.

> **Note:** The dataset used in this project is synthetic and was created for educational purposes. It does not contain real patient information and the model is not clinically validated.

## 🎯 Objective

The objective is to predict:

- `0` → No readmission within 30 days
- `1` → Readmission within 30 days

The main model used is Logistic Regression with L2 regularization.

## 📊 Dataset

The dataset contains 10,000 synthetic patient records with features including:

- Age
- Gender
- Heart rate
- Systolic blood pressure
- Diastolic blood pressure
- Temperature
- Oxygen saturation
- Number of prior visits
- Number of emergency visits
- Number of inpatient visits
- Number of diagnoses
- Length of stay
- Diabetes
- Hypertension
- Previous readmission

### Target Variable

`readmitted_30_days`

## 🤖 Machine Learning Model

**Algorithm:** Logistic Regression

**Regularization:** L2

The dataset is divided into training and testing sets using an 80/20 split. Numerical features are standardized using `StandardScaler`.

## 📈 Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve
- ROC-AUC

ROC-AUC is used as the main metric for evaluating the model's ability to distinguish between patients who are and are not readmitted within 30 days.

## 🏥 False Positives vs False Negatives

A **false negative** occurs when a patient who is actually readmitted within 30 days is predicted as not being readmitted.

A **false positive** occurs when a patient who is not readmitted is predicted as being at risk of readmission.

In a real healthcare setting, these errors can have different clinical and resource implications. The appropriate classification threshold would therefore need to be determined using validated clinical and operational considerations.

## 📁 Project Structure

```text
hospital-readmission-prediction/
│
├── data/
│   └── hospital_readmission.csv
│
├── notebooks/
│   ├── 01_Create_Synthetic_Hospital_Dataset.ipynb
│   └── 02_Hospital_Readmission_Prediction.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## ⚙️ How to Run

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open the notebooks using Jupyter Notebook or Google Colab.

Run:

1. `01_Create_Synthetic_Hospital_Dataset.ipynb`
2. `02_Hospital_Readmission_Prediction.ipynb`

The second notebook uses the generated `hospital_readmission.csv` dataset.

## ⚠️ Disclaimer

This project is for educational purposes only. The dataset is synthetic, and the model should not be used to make real-world medical or patient-care decisions.
