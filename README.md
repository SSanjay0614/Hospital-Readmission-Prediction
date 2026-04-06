# Hospital Readmission Prediction (Diabetes)

## Project Overview
This project focuses on predicting hospital readmission within 30 days for diabetic patients using predictive analytics and machine learning techniques. The goal is to develop an accurate and interpretable model that can assist healthcare providers in identifying high-risk patients and enabling proactive intervention.

The study is based on the **UCI Diabetes 130-US Hospitals Dataset**, and the framework is designed to be **generalizable to other diseases and healthcare prediction tasks**.

---

## Dataset
- Source: UCI Machine Learning Repository  
- Records: ~101,766 patient encounters  
- Features: 47 attributes  
- Domain: Healthcare (Diabetes)  
- Time Period: 1999–2008  

Each record represents a hospital encounter, including:
- Demographics (age, gender, race)
- Clinical data (diagnosis codes, lab results)
- Administrative details (admission/discharge)
- Treatment data (medications, procedures)

**Target Variable**:  
Readmission status (converted to binary: readmitted within 30 days vs others)

---

## Methodology

The project follows a structured predictive analytics pipeline:

1. Exploratory Data Analysis  
2. Data Cleaning  
3. Feature Engineering  
4. Data Transformation and Encoding  
5. Noise and Outlier Detection  
6. Class Imbalance Handling (SMOTE)  
7. Predictive Modeling  
8. Ensemble Learning  
9. Model Evaluation and Validation  
10. Model Interpretability (SHAP)

---

## Data Preprocessing

- Removed high-missing and irrelevant features  
- Handled missing values and inconsistencies  
- Created new features:
  - `patient_service`
  - `med_change`
  - `num_med`
- Grouped diagnosis codes into clinical categories  
- Applied encoding and scaling techniques  
- Addressed class imbalance using **SMOTE**

---

## Models Used

### Base Models
- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost  

### Ensemble Models
- Voting Classifier (Hard & Soft)  
- Stacking  
- Bagging  
- Gradient Boosting  
- AdaBoost  

---

## Evaluation Metrics

- Accuracy  
- Precision  
- Recall (important for healthcare)  
- F1 Score  
- ROC-AUC  
- Confusion Matrix  

---

## Results Summary

- Logistic Regression performed as baseline  
- Tree-based models significantly improved performance  
- **XGBoost achieved the best individual performance**  
- Ensemble methods (especially **Stacking and Gradient Boosting**) provided the most stable and accurate results  

---

## Model Interpretability

SHAP (SHapley Additive exPlanations) was used to interpret model predictions.

### Key Features Influencing Readmission:
- Time in hospital  
- Number of inpatient visits  
- Number of medications  
- Number of procedures and diagnoses  

These features align with clinical expectations, enhancing trust in model predictions.

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost, LightGBM  
- Imbalanced-learn (SMOTE)  
- Matplotlib, Seaborn  
- SHAP   

---


## 📜 License

This project is for academic and research purposes.
