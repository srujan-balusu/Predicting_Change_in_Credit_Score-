# Credit Score Movement Classification

## Objective
The objective of this project is to classify customers according to the movement of their credit scores — whether it will most probably **increase**, **decrease**, or stay **stable** — utilizing a synthetic dataset. These findings assist companies in taking proactive financial actions to reduce credit risk and detect business opportunity for growth.

---

## Target Definition
The target variable `target_credit_score_movement` is derived on the basis of financial behavior rules:

### Decrease (High Risk)
- Days Past Due (DPD) in the previous 3 months more than 60
- Credit Utilization Ratio more than 0.8
- Hard inquiries more than 2 in the past 6 months

### Increase (High Opportunity)
- EMI to Income ratio less than 0.3
- Repayment History Score 70 or higher

### Stable
- All other instances

---

## Data and Preprocessing
- A synthetic dataset of approximately **25,000 customer records** was employed

### Preprocessing steps involved:
- Encoding categorical variables like gender and location
- Feature scaling with `StandardScaler`
- Class imbalance handling with **SMOTE** to obtain approximately equal class distribution

---

## Overview of Model
- **Model employed:** Random Forest Classifier
- **Multiclass classification** with labels: `increase`, `decrease`, `stable`

### Metrics used for evaluation:
- **Accuracy:** 97 percent

**F1-Score by class:**
- Increase: 0.92
- Decrease: 1.00
- Stable: 0.98

---

## SHAP Explainability
**SHAP (SHapley Additive exPlanations)** was used to understand how different features affect the model’s predictions.

### Important features for predicting an increase in credit score:
- High repayment history
- Low EMI burden
- Low credit utilization

### Important features for predicting a decrease in credit score:
- High DPD
- High utilization ratio
- Frequent hard inquiries

### Visualizations included:
- SHAP summary plots for global understanding
- SHAP waterfall plots for single prediction explanation

---

## Business Takeaways

### High-Risk Segment (Predicted to Decrease)
These customers will likely default or experience financial stress.

**Recommended interventions:**
- Trigger credit risk notifications
- Provide EMI restructuring opportunities
- Send repayment reminders
- Send credit behavior education material

### High-Opportunity Segment (Predicted to Increase)
These customers reflect good financial behavior and will be likely to remain loyal.

**Recommended interventions:**
- Provide improved credit terms or reduced interest charges
- Provide pre-approved credit or loans
- Roll out loyalty reward schemes
- Market financial growth solutions like insurance or investment products
