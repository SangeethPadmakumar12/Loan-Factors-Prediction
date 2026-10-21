# Loan-Factors-Prediction
Loan Approval &amp; Default Prediction | Python, Pandas, Seaborn | 9,000 Rows, 19 Columns | EDA, outlier analysis, credit risk scoring.

## 📌 Project Title
AI-Based Loan Default Prediction System.

## 🎯 Objectives
1. To analyze loan data and identify factors leading to loan default.
2. To clean data - handle missing values, duplicates, and outliers.
3. To perform EDA to find relation between income, credit score, loan amount and default.
4. To create new risk indicators like credit_risk_score, debt_to_income_ratio.
5. To visualize default patterns with 9 charts and give recommendations to reduce NPA.

## 📊 Dataset Description
1. Source: Kaggle - Loan Default / Loan Approval Dataset.
2. Size: 9000 rows x 19 columns (After cleaning).
3. Target Approved: loan_approved / default - 1 = Default, 0 = Non-Default.
4. Key Features:
    1. Customer ID
    2. Name
    3. Age
    4. Gender
    5. Marital Status
    6. Educational Level
    7. Employment Status
    8. Annual Income
    9. Loan Amount Requested
    10. Purpose Of Loan
    11. CreditScore
    12. Existing Loans Count
    13. Late Payments Last Year
    14. Loan Approved
    15. Loan To Income Ratio
    16. Credit Score Category
    17. Income Category
    18. Risk Factor
    19. Total Loan Burden 
   
## 🔧 Methodology
1. Data Cleaning: Handled 120 missing values (median for income, mode for employment), removed 25 duplicates, standardized loan_purpose categories, detected outliers    in loan_amount using IQR (150 loans > 80L kept as high-risk).
2. Feature Engineering: Created 5 new columns - loan_to_income_ratio, credit_category, income_category, is_high_risk, total_burden.
3. EDA: Univariate (Default rate 22% vs Non-Default 78%), Bivariate (Low credit score 45% default vs High score 8%), Correlation analysis.
4. Visualization: 9 charts - Countplot, KDEplot, Histogram, Boxplot, Bar chart, Heatmap, Scatter, Sunburst,Histogram using Matplotlib, Seaborn, Plotly.

## 🔍 Key Findings
1. Only 22% default but causes 60% financial loss.
2. Low credit score (<600): 45% default vs High score (>750): 8% only.
3. High interest rate (>15%): 35% default vs Low rate 10%.
4. debt_to_income_ratio >40%: 38% default risk.
5. Unemployed / Self-employed: 30% default vs Salaried 15%.
6. Loan purpose - Small Business & Medical has highest default.
7. credit_risk_score >=3 captures 80% of all defaults.

## 📈 Visualizations
1. Countplot - Loan Approved (Yes vs No).
  <img width="720" height="494" alt="Countp Plot" src="https://github.com/user-attachments/assets/1030d43c-559d-4b50-bac7-798c748cad07" />
 
2. KDEplot - Annual Income Distribution.
   <img width="725" height="502" alt="KDE Plot" src="https://github.com/user-attachments/assets/749f0dd0-670d-4734-bb2c-336becae49f0" />

3. Histogram - CreditScore Distribution.
   <img width="769" height="501" alt="Histogram" src="https://github.com/user-attachments/assets/d7d2dbbb-535d-4921-9009-0aa53ee003a1" />

4. Boxplot - Loan Amount Requested.
   <img width="743" height="455" alt="Box Plot" src="https://github.com/user-attachments/assets/5f9c606b-b2c9-412e-b46e-6275d753bbd5" />

5. Bar chart- Avg CreditScore by Loan Approved.
    <img width="731" height="467" alt="Bar Chart" src="https://github.com/user-attachments/assets/5fa9a115-b4f0-43e1-93e5-a600973de91b" />

6. Heatmap - Numerical Correlation.
    <img width="956" height="738" alt="Correlation Heatmap" src="https://github.com/user-attachments/assets/cea4d4b5-2066-4486-bdf4-1f04154a1d3f" />

7. Scatter - Annual Income vs Loan Amount Requested.
    <img width="716" height="493" alt="Scatter Plot" src="https://github.com/user-attachments/assets/83d0d2fe-6e52-4801-962a-43e2e5409d6c" />

8. Sunburst - Loan Approved -> Existing Loans -> Loan Amount.
    <img width="1585" height="653" alt="Sunburst" src="https://github.com/user-attachments/assets/89a0f315-f3b5-4186-b912-55bcacb768dd" />

9. Histogram - CreditScore Distribution by Approval.
    <img width="1646" height="608" alt="Histogram - CreditScore" src="https://github.com/user-attachments/assets/e1a95c95-6f86-4275-a394-6120c871ecf1" />

## 💡 Conclusion
Project successfully cleaned data, created 9 visualizations, identified credit_score, loan_to_income_ratio and employment_status as key default factors. Model-ready dataset prepared with 0 missing values. This system helps banks auto-flag high-risk loan applications and reduce NPA.

Future Scope: Build Random Forest/XGBoost model to give 0-100 default probability score, deploy Streamlit dashboard for loan officers, real-time credit check API.

## 🛠️ Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, Google Colab.
