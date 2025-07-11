
# Part 2: Case Study Application

## Scenario
A hospital wants an AI system to predict patient readmission risk within 30 days of discharge.

---

## 1. Problem Scope (5 points)

**Problem:**  
Predict the likelihood of a patient being readmitted within 30 days after hospital discharge.

**Objectives:**
1. Identify high-risk patients at discharge.
2. Reduce readmission rates to improve patient outcomes.
3. Optimize hospital resource allocation.

**Stakeholders:**
- Hospital administrators.
- Healthcare providers (doctors, nurses).

---

## 2. Data Strategy (10 points)

**Data Sources:**
1. Electronic Health Records (EHRs): medical history, medications, vital signs.
2. Demographics: age, gender, socio-economic status.

**Ethical Concerns:**
1. **Patient Privacy:** Ensuring HIPAA-compliant handling of sensitive health data.
2. **Bias in Data:** Certain populations may be underrepresented, leading to unfair predictions.

**Preprocessing Pipeline:**
- **Data Cleaning:** Remove duplicates and handle missing values in vital signs and history.
- **Feature Engineering:**
  - Time since last admission.
  - Number of comorbidities.
  - Medication adherence metrics.
- **Normalization:** Scale numeric features (e.g., lab results) for model stability.
- **Categorical Encoding:** One-hot encode categorical variables (e.g., gender, insurance type).

---

## 3. Model Development (10 points)

**Chosen Model:** Gradient Boosting Machine (e.g., XGBoost)

**Justification:**
- Handles tabular healthcare data effectively.
- Provides interpretability using SHAP values to explain predictions.
- High accuracy with imbalanced datasets.

---

### **Hypothetical Confusion Matrix:**

|                   | Predicted Readmit | Predicted No Readmit |
|-------------------|-------------------|----------------------|
| **Actual Readmit**     | 80                | 20                   |
| **Actual No Readmit**  | 15                | 85                   |

---

**Calculations:**

- **Precision:**
  \[
  \text{Precision} = \frac{TP}{TP + FP} = \frac{80}{80 + 15} = 0.842
  \]

- **Recall:**
  \[
  \text{Recall} = \frac{TP}{TP + FN} = \frac{80}{80 + 20} = 0.80
  \]

---

## 4. Deployment (10 points)

**Integration Steps:**
1. Deploy the model as a REST API using FastAPI.
2. Connect API to the hospital’s EHR system for real-time predictions.
3. Provide clinicians with a dashboard displaying patient risk scores.

**Compliance with Healthcare Regulations:**
- Use encryption for data in transit and at rest.
- Maintain audit trails of data access.
- Ensure all data processing aligns with HIPAA guidelines and local health data laws.

---

## 5. Optimization (5 points)

**Method to Address Overfitting:**
- **Cross-Validation:** Perform k-fold cross-validation during training.
- **Early Stopping:** Monitor validation loss and stop training when improvement plateaus to prevent overfitting.

---



