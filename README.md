Predicting 30-Day Hospital Readmissions
##Project Overview

Hospital readmissions within 30 days are a major quality-of-care metric and a source of significant cost for healthcare systems.

**Objective:**
Predict whether a patient will be readmitted within 30 days of discharge using structured electronic health record (EHR) data.

**Use case:**

* Risk stratification at discharge
* Targeted post-discharge interventions
* Quality improvement & cost reduction

---
Dataset

**Source:** Kaggle – *Diabetes 130-US Hospitals for Years 1999–2008*

* ~100,000 patient encounters
* 130 U.S. hospitals
* De-identified EHR-style data

**Target Variable:**

'readmit_30' → 1 if readmitted within 30 days, else 0

Modeling Approach

Baseline Model

* Logistic Regression
* Interpretable and clinically intuitive

Advanced Model

* **LightGBM Classifier**
* Handles high-cardinality categorical features efficiently
* Strong performance on tabular healthcare data

Evaluation Metrics

* ROC-AUC (primary)
* Precision / Recall
* Class imbalance awareness

---

Model Explainability

SHAP (SHapley Additive exPlanations) is used to:

* Explain individual predictions
* Identify globally important risk factors
* Support clinical trust and transparency

The model is positioned as a decision-support tool, not a replacement for clinicians.

---

Bias & Ethical Considerations

* Readmission rates analyzed across demographic groups
* Discussion of socioeconomic confounding
* Emphasis on responsible deployment and monitoring

---

Key Findings

* Prior utilization (inpatient + ED visits) strongly predicts readmission
* Medication complexity increases readmission risk
* Certain demographic disparities are observable and require caution

---

Future Improvements

* Add temporal modeling (sequence of visits)
* Incorporate social determinants of health
* Hyperparameter tuning with cross-validation
* Deployment simulation (risk scoring service)
