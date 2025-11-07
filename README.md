## 📚 Case Study: Improving Loan Approval Decisions Through Default Risk Modeling

### ✅ Scenario
A lending company sees a rise in delinquent accounts over the last two quarters.  
Executives report:

- A **12% increase** in loan defaults  
- Higher default rates among applicants with limited credit history  
- Manual underwriting decisions vary widely between loan officers  
- No standardized risk scoring model exists  

Leadership needs a data-driven method to identify high-risk borrowers before approval.

The **Loan Default Risk Analysis (SAS Project)** is created to analyze drivers of default and build a predictive statistical model.

---

### ✅ Step 1 — Data Exploration & Risk Pattern Detection
The dataset is imported into SAS and reviewed using PROC IMPORT, PROC CONTENTS, PROC MEANS, and PROC FREQ.

**Data Import into SAS**  
![Import](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/Import%20the%20Data%20into%20SAS.PNG)

**Variable Review (PROC CONTENTS)**  
![Contents](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/contents_procedure.PNG)

**Variable Attributes**  
![Attributes](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/alphabetic_list_variables_attributes.PNG)

**Summary Statistics (PROC MEANS)**  
![Means](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/means.PNG)

**Frequency Tables (PROC FREQ)**  
![FREQ](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/freq_procedures.PNG)

**Key Insights Identified:**
- Borrowers with **high debt-to-income (DTI)** ratios default at nearly **3×** the rate of others  
- Credit score correlates strongly (negatively) with default probability  
- Loan purposes such as *debt consolidation* and *small business* carry higher risk  
- Lower annual income brackets show elevated default frequency  
- Longer-term loans default more often  

These patterns form the foundation for predictive modeling.

---

### ✅ Step 2 — Feature Engineering & Data Preparation
The dataset is cleaned and transformed:

- Created binary default indicator  
- Binned credit scores into risk tiers  
- Engineered DTI risk bands  
- Encoded categorical fields (loan purpose, home ownership)  
- Removed incomplete or invalid rows  

The transformation produces a clean, modeling-ready dataset.

---

### ✅ Step 3 — Logistic Regression Model Training
A logistic regression model is trained using **PROC LOGISTIC**.

**Logistic Regression Output (Part 1)**  
![Logistic 1](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics.PNG)

**Logistic Regression Output (Part 2)**  
![Logistic 2](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics_2.PNG)

**Logistic Regression Output (Part 3)**  
![Logistic 3](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics_3.PNG)

**Logistic Regression Output (Part 4)**  
![Logistic 4](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/logistics_4.PNG)

**Significant Predictors Identified:**
- Debt-to-Income Ratio  
- Credit Score  
- Loan Purpose  
- Annual Income  
- Loan Term  
- Past Delinquencies  

These factors are converted into a borrower-level probability of default.

---

### ✅ Step 4 — Model Evaluation
The model is assessed using accuracy, sensitivity, specificity, and confusion matrix metrics.

**Risk Band Visualization**  
![Risk Band](https://github.com/YSayaovong/Loan-Default-Risk-Analysis-SAS-Project/blob/main/images/risk_band.PNG)

**Evaluation Findings:**
- Strong sensitivity (model effectively flags risky borrowers)  
- High specificity for high-credit, stable-income applicants  
- Distinct separation between low-risk and high-risk groups  
- Predictive outputs improve underwriting consistency  

---

### ✅ Step 5 — Final Insights & Recommendations
Based on the model’s findings, the lender is advised to:

- Tighten approval thresholds for high-risk DTI and income categories  
- Introduce tiered interest rates tied to predicted risk  
- Apply stricter review for loan purposes associated with historical defaults  
- Implement a pre-screening risk score in the underwriting workflow  

Within one quarter of using the predictive model:

- Default exposure decreased  
- Approval decisions became standardized  
- Underwriters gained a reliable, data-driven decision support tool  

The SAS-based analysis now forms the foundation for risk-aware lending at the organization.
