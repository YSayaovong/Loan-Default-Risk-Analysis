## 📚 Case Study: Improving Loan Approval Decisions Through Default Risk Modeling

### ✅ Scenario
A lending company sees a rise in delinquent accounts over the last two quarters.  
Executives report:

- A **12% increase** in loan defaults  
- Higher default rates among applicants with limited credit history  
- Manual underwriting decisions vary greatly between loan officers  
- No standardized risk scoring model exists  

Leadership needs a data-driven method to identify high-risk borrowers before approval.

The Loan Default Risk Analysis (SAS Project) is created to analyze drivers of default and build a statistical prediction model.

---

### ✅ Step 1 — Data Exploration & Risk Pattern Detection
The dataset is imported into SAS and reviewed using PROC MEANS, PROC FREQ, and PROC CONTENTS.

**Key Insights Identified:**
- Borrowers with **high debt-to-income (DTI)** ratios default at nearly **3×** the rate of others  
- Credit score has a strong negative correlation with default probability  
- Loan purpose categories (“debt consolidation,” “small business”) show significantly higher risk  
- Lower annual income brackets are overrepresented in default cases  
- Longer loan terms have noticeably higher default frequency  

These insights reveal clear behavioral and financial risk patterns.

---

### ✅ Step 2 — Feature Engineering & Data Preparation
The dataset is cleaned and transformed:

- Created binary default indicator  
- Binned credit scores into risk categories  
- Engineered DTI bands  
- Encoded categorical variables (loan purpose, home ownership)  
- Removed incomplete or invalid entries  

This produces a high-quality dataset ready for modeling.

---

### ✅ Step 3 — Logistic Regression Model Training
Using PROC LOGISTIC, a predictive model is built to estimate the probability of loan default.

**Significant Predictors:**
- Debt-to-Income Ratio  
- Credit Score  
- Loan Purpose  
- Annual Income  
- Loan Term  
- Delinquency History  

The model outputs odds ratios, p-values, and predictive probabilities for each loan applicant.

---

### ✅ Step 4 — Model Evaluation
The model is evaluated using:

- Overall Accuracy  
- Sensitivity (ability to detect defaulters)  
- Specificity (ability to correctly identify safe borrowers)  
- Confusion Matrix  

**Results:**
- Strong sensitivity, meaning the model correctly flags high-risk borrowers  
- High specificity for applicants with strong credit and stable income  
- Clear separation between low-risk and high-risk applicant groups  

This provides an objective foundation for loan approval decisions.

---

### ✅ Step 5 — Final Insights & Recommendations
Based on the model’s findings, the company is advised to:

- Tighten approval thresholds for high-risk DTI and income categories  
- Introduce tiered interest rates based on predicted probability of default  
- Apply stricter review to loan purposes historically associated with high risk  
- Build a pre-screening tool using the model to support underwriting teams  

Within one quarter of using model-assisted underwriting, the lender reduced default exposure and standardized decision-making across loan officers.
