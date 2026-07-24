### 1. Auto Insurance Churn Prediction Model
**Tools Used:** Python, Pandas, SQL (SQLite), XGBoost, Scikit-learn, SMOTE 
**Objective:** To engineer a predictive classification model that identifies high-risk policyholders before cancellation to maximize Customer Lifetime Value (CLV) and reduce acquisition-related losses.
**Summary:** 
* Queried and aggregated raw demographic, geographic, and financial policyholder data using SQL and Pandas.
* Addressed a highly imbalanced dataset (~12% churn rate) by applying SMOTE to synthetically generate high-risk examples for model training.
* Demonstrated the limits of linear models for conditional financial behavior by showing how a baseline Logistic Regression model achieved 87% accuracy but critically low recall (8%).
* Built a non-linear XGBoost classifier that increased recall to 30% by successfully mapping complex "if/then" scenarios and seasonal churn patterns.
* Extracted feature importance scores, revealing that familial stability (College Degree, Home Ownership) and localized geographic risk (specific Texas counties) were stronger churn predictors than standard financial metrics like pure income or tenure.

[**View the Jupyter Notebook and Source Code on GitHub**]([[link-to-your-repo](https://github.com/22kevinh21/AutoInsurancePricing)

---

### 2. Insurance Pricing Optimization & Algorithmic Bias Audit
**Tools Used:** Python, Pandas, Scikit-learn (Random Forest Regressor), Seaborn, Matplotlib 
**Objective:** To mathematically evaluate whether non-risk proxy variables heavily influence the final price charged to consumers, detecting potential socio-economic algorithmic bias.  
**Summary:**
* Constructed a unified analytical pipeline by joining consumer-level premium data with geographic lookup definitions and localized macroeconomic census metrics.
* Engineered a new target variable (Markup Percentage) to quantify the relative premium markup over the pure actuarial risk baseline, successfully eliminating target leakage from accounting variables.
* Fitted a Random Forest Regressor to predict the final markup percentage, achieving an R² score of 0.4938.
* Uncovered a "Loyalty Tax" through exploratory data analysis, where massive, non-risk-based premium hikes were occasionally applied to highly retained customers with 4 to 5 years of tenure.
* Proved mathematically that the pricing algorithm heavily leveraged Median Household Income over driver age or loyalty, resulting in structural penalty markups for lower-to-middle-income zip codes ($50,000 - $75,000).

[**View the Jupyter Notebook and Source Code on GitHub**](https://github.com/22kevinh21/AutoInsuranceChurnAnalysis)
