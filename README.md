Credit Score Movement Classification
Objective
The goal of this project is to classify customers based on the movement of their credit scores — whether it is likely to increase, decrease, or remain stable — using a synthetic dataset. These insights help businesses take proactive financial decisions to minimize credit risk and identify growth opportunities.

Target Definition
The target variable target_credit_score_movement is created based on financial behavior rules:

Decrease (High Risk)

Days Past Due (DPD) in the last 3 months greater than 60

Credit Utilization Ratio greater than 0.8

More than 2 hard inquiries in the last 6 months

Increase (High Opportunity)

EMI to Income ratio less than 0.3

Repayment History Score greater than or equal to 70

Stable

All other cases

Data and Preprocessing
A synthetic dataset with around 25,000 customer records was used

Preprocessing steps included:

Encoding categorical features such as gender and location

Feature scaling using StandardScaler

Handling class imbalance using SMOTE to achieve a roughly equal class distribution

Model Overview
Model used: Random Forest Classifier

Multiclass classification with labels: increase, decrease, stable

Evaluation metrics:

Accuracy: 97 percent

F1-Score by class:

Increase: 0.92

Decrease: 1.00

Stable: 0.98

SHAP Explainability
SHAP (SHapley Additive exPlanations) was used to understand how different features affect the model’s predictions.

Important features for predicting an increase in credit score:

High repayment history

Low EMI burden

Low credit utilization

Important features for predicting a decrease in credit score:

High DPD

High utilization ratio

Frequent hard inquiries

Visualizations included:

Summary plots for global insights

Waterfall plots for individual prediction explanation

Business Takeaways
High-Risk Segment (Predicted to Decrease)
These customers are more likely to default or face financial distress.

Suggested interventions:

Send credit risk alerts

Offer EMI restructuring options

Provide repayment reminders

Deliver credit behavior education content

High-Opportunity Segment (Predicted to Increase)
These customers show strong financial habits and are likely to stay loyal.

Suggested interventions:

Offer better credit terms or lower interest rates

Provide pre-approved loans or credit cards

Launch loyalty reward programs

Promote financial growth products such as insurance or investment plans
