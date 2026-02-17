# Healthcare-No-Show-Risk-Modeling
End-to-end machine learning system predicting healthcare appointment no-shows (ROC-AUC: 0.72), incorporating class imbalance handling, threshold optimization, and revenue impact analysis.

---

## 📌 Problem Statement

Missed medical appointments (no-shows) lead to significant revenue loss and inefficient resource utilization in healthcare systems.  

This project builds a predictive model to identify high-risk patients in advance and proposes an overbooking strategy to reduce idle slot losses.

---

## 🎯 Objectives

- Predict patient no-show probability
- Handle class imbalance effectively
- Optimize decision threshold for business tradeoffs
- Estimate potential revenue impact
- Deploy model for real-time prediction

---

## 📊 Dataset Overview

- Healthcare appointment dataset
- Imbalanced target (~20% no-show rate)
- Key features:
  - LeadTime
  - Age
  - SMSReceived
  - Hypertension
  - Diabetes
  - Alcoholism
  - AppointmentDayOfWeek

---

## 🔍 Exploratory Data Analysis

Key findings:

- **Lead Time** is the strongest predictor of no-shows.
- Patients booking far in advance are more likely to miss appointments.
- SMS reminders show moderate impact.
- Clear class imbalance justified SMOTE usage.

---

## 🤖 Model Development

- Algorithm: Random Forest Classifier
- Class imbalance handled using **SMOTE**
- Hyperparameter tuning via **GridSearchCV**
- Decision threshold optimized for business balance

### ✅ Best Model Performance

- ROC-AUC: **0.72**
- Optimized Threshold: **0.6**
- No-Show Recall: **57%**
- Accuracy: **68%**

---

## 💰 Business Impact

- Estimated Revenue Loss: ₹38,230,000
- Suggested Overbooking Buffer: 16.15%
- Model enables proactive scheduling intervention

---

## 🚀 Streamlit Application

An interactive Streamlit app is included for real-time prediction and decision support.
Features:
- Patient-level no-show probability prediction
- Adjustable decision threshold
- Business impact insights

Run locally:

```bash
pip install -r requirements.txt
python main.py
streamlit run app/app.py
