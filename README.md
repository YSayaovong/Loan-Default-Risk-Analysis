# 🏛️ Case Study: Improving Loan Approval Decisions Through Default Risk Modeling  
**SAS-Based Credit Risk Analysis for Predictive Underwriting**

## ✅ Executive Summary  
A lending institution reported a **12% rise in loan defaults** over two quarters.  
Underwriting decisions varied widely between officers, and the absence of a standardized risk model made loan approvals inconsistent and financially risky.

This SAS project develops a **predictive default risk model** that quantifies borrower risk, strengthens underwriting consistency, and reduces portfolio credit exposure.

---

# ✅ Step 1 — Data Exploration & Early Risk Signals  
Loan application and performance data were imported into SAS for initial exploration using:

- `PROC IMPORT`
- `PROC CONTENTS`
- `PROC MEANS`
- `PROC FREQ`

### 📄 Data Import  
![Import](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/Import%20the%20Data%20into%20SAS.PNG)

### 📄 Variable Review (PROC CONTENTS)  
![Contents](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/contents_procedure.PNG)

### 📄 Variable Attributes  
![Attributes](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/alphabetic_list_variables_attributes.PNG)

### 📄 Summary Statistics (PROC MEANS)  
![Means](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/means.PNG)

### 📄 Frequency Checks  
![FREQ](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/freq_procedures.PNG)

## ✅ Early Insights  
Exploratory analysis revealed several consistent indicators of credit stress:

- Borrowers with **high DTI** default nearly **3×** more often  
- **Credit score** has a strong negative correlation with default  
- *Debt consolidation* and *small business* loans show elevated risk  
- Lower annual income brackets produce higher delinquency  
- **Longer loan terms** correlate with increased default probability  
- Past delinquencies are a strong predictor of future default  

These patterns form the basis for feature engineering and model development.

---

# ✅ Step 2 — Feature Engineering & Data Preparation  

To build a production-quality model, the dataset was transformed and standardized:

### ✅ Transformations Completed  
- Created binary **Default Indicator** for modeling  
- Binned **credit scores** into risk tiers (A–D)  
- Engineered **DTI risk bands**  
- Encoded categorical fields (loan purpose, home ownership)  
- Removed incomplete or invalid entries  
- Normalized skewed financial variables  

This produced a clean, consistent dataset suitable for predictive modeling.

---

# ✅ Step 3 — Logistic Regression Model (PROC LOGISTIC)

A logistic regression model was trained to estimate borrower probability of default (PD).

### 📄 Regression Output (Part 1)  
![Logistic 1](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics.PNG)

### 📄 Regression Output (Part 2)  
![Logistic 2](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics_2.PNG)

### 📄 Regression Output (Part 3)  
![Logistic 3](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics_3.PNG)

### 📄 Regression Output (Part 4)  
![Logistic 4](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics_4.PNG)

## ✅ Significant Predictors Identified  
The model confirmed statistically significant contributors to default risk:

- **DTI ratio**  
- **Credit score**  
- **Loan purpose**  
- **Annual income**  
- **Loan term length**  
- **Prior delinquencies**

Each borrower receives a **Probability of Default (PD)** score based on these inputs.

---

# ✅ Step 4 — Model Evaluation & Risk Segmentation  

The model was evaluated using confusion matrix metrics, sensitivity, specificity, and ROC analysis.

### 📸 Risk Band Visualization  
![Risk Band](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/risk_band.PNG)

## ✅ Evaluation Results  
- High sensitivity—model successfully flags high-risk borrowers  
- High specificity among low-risk, high-credit applicants  
- Clear score separation between risk tiers  
- Predictive consistency improves underwriting reliability  

Risk bands now support structured decision-making in both automated and manual underwriting workflows.

---

# ✅ Step 5 — Strategic Recommendations  

Based on model findings, the lending institution was advised to:

### ✅ Portfolio-Level Recommendations  
- Tighten approval thresholds for **high DTI** and **low income** segments  
- Introduce **tiered interest rates** based on PD score  
- Reduce exposure to historically high-risk loan purposes  
- Apply enhanced documentation reviews for high-risk applicants  

### ✅ Underwriting Process Enhancements  
- Embed PD score into the underwriting workflow  
- Standardize approval rules using model cutoffs  
- Automate pre-screening to reduce underwriter workload  

---

# ✅ Outcome & Business Impact  

Within one quarter of implementing the risk model:

- ✅ Default exposure declined  
- ✅ Approval decisions became standardized across officers  
- ✅ Underwriters gained a reliable risk-scoring tool  
- ✅ Portfolio quality improved  
- ✅ High-risk loans were priced with greater accuracy  

This SAS-driven credit risk model now forms the foundation of the organization’s risk-aware lending strategy.

---

# ✅ Tools & Technologies  
- SAS (PROC IMPORT, PROC MEANS, PROC FREQ, PROC LOGISTIC)  
- Feature Engineering & Data Cleaning  
- Statistical Modeling & Probability Scoring  
- Financial Risk Analytics  
- Git/GitHub for version control  

---

# ✅ Summary  
This project demonstrates a complete **default risk modeling pipeline** used by lending institutions to reduce exposure, strengthen underwriting, and standardize loan approval decisions.  
It applies enterprise-grade SAS analytics to improve financial outcomes and support data-driven lending.

