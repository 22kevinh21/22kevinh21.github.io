# Kevin Hernandez - Actuarial & Data Science Portfolio

Welcome to my portfolio! I am an aspiring actuarial analyst with a degree in Applied Mathematics and a professional background in mathematics education. 

My experience managing high school math classrooms has given me a unique advantage in the data world: I know how to translate complex mathematical logic into clear, actionable insights for any audience. Having recently passed the Actuarial Probability Exam (Exam P), I am actively building my technical skill set across Excel, Python, SQL, and data visualization.

Below you will find a collection of my technical projects, demonstrating my ability to handle everything from pure premium calculations to predictive data science models.

### [Marine Liability Insurance Pricing Model](https://github.com/22kevinh21/Commercial-Insurance-Premium-Model)
**Tools:** Microsoft Excel
*   Built a pure premium pricing model for a commercial marine liability portfolio.
*   Conducted exploratory data analysis (EDA) to map historical loss frequency and severity.
*   Adjusted for inflation, capped policy limits, and isolated 1-in-20-year catastrophic risks.
*   Drafted a complete executive report detailing the final premium calculations and stress-tested the model using a 6% severity increase sensitivity analysis.


### [Insurance Financial Forecasting Model](https://github.com/22kevinh21/Insurance_Financial_Forecasting_Model)
**Tools:** Microsoft Excel
* Imported and structured over 9,000 records of daily financial data to track collected premiums, incurred claims, and administrative expenses.
* Aggregated raw data into a monthly analysis table to calculate overall profitability and per-member financial performance metrics.
* Built a dynamic lookup tool and applied historical trend factors to forecast future per-member costs and revenues.
* Conducted a variance analysis comparing projected aggregate financial results against actual outcomes to evaluate model accuracy.


### [Auto Insurance Churn Prediction Model](https://github.com/22kevinh21/AutoInsurancePricing)
**Tools Used:** Python, Pandas, SQL (SQLite), XGBoost, Scikit-learn, SMOTE 
**Objective:** To engineer a predictive classification model that identifies high-risk policyholders before cancellation to maximize Customer Lifetime Value (CLV) and reduce acquisition-related losses.
**Summary:** 
* Queried and aggregated raw demographic, geographic, and financial policyholder data using SQL and Pandas.
* Addressed a highly imbalanced dataset (~12% churn rate) by applying SMOTE to synthetically generate high-risk examples for model training.
* Demonstrated the limits of linear models for conditional financial behavior by showing how a baseline Logistic Regression model achieved 87% accuracy but critically low recall (8%).
* Built a non-linear XGBoost classifier that increased recall to 30% by successfully mapping complex "if/then" scenarios and seasonal churn patterns.
* Extracted feature importance scores, revealing that familial stability (College Degree, Home Ownership) and localized geographic risk (specific Texas counties) were stronger churn predictors than standard financial metrics like pure income or tenure.


### [Insurance Pricing Optimization & Algorithmic Bias Audit](https://github.com/22kevinh21/AutoInsuranceChurnAnalysis)
**Tools Used:** Python, Pandas, Scikit-learn (Random Forest Regressor), Seaborn, Matplotlib 
**Objective:** To mathematically evaluate whether non-risk proxy variables heavily influence the final price charged to consumers, detecting potential socio-economic algorithmic bias.  
**Summary:**
* Constructed a unified analytical pipeline by joining consumer-level premium data with geographic lookup definitions and localized macroeconomic census metrics.
* Engineered a new target variable (Markup Percentage) to quantify the relative premium markup over the pure actuarial risk baseline, successfully eliminating target leakage from accounting variables.
* Fitted a Random Forest Regressor to predict the final markup percentage, achieving an R² score of 0.4938.
* Uncovered a "Loyalty Tax" through exploratory data analysis, where massive, non-risk-based premium hikes were occasionally applied to highly retained customers with 4 to 5 years of tenure.
* Proved mathematically that the pricing algorithm heavily leveraged Median Household Income over driver age or loyalty, resulting in structural penalty markups for lower-to-middle-income zip codes ($50,000 - $75,000).

