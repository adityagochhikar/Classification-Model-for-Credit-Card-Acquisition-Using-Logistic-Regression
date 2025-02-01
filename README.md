# 📊 Credit Card Purchase Prediction using Logistic Regression

# 🎯 Objective

This project aims to predict whether a customer will purchase a credit card based on demographic and behavioural factors. The goal is to build a logistic regression model to estimate the probability of purchase and evaluate the model's performance using key classification metrics.

# 📂 Dataset Overview

The dataset originates from a bank marketing campaign, where the target variable is:

# 📌 Dependent Variable (Target):

✔ Purchase (0 = No, 1 = Yes)

# 📌 Independent Variables (Features):

✔ Age – Older individuals may have higher purchasing power.

✔ Dispatch Local Time – Time of email dispatch, potentially influencing customer engagement.

✔ On Mobile Device – Whether the email was opened on a mobile device or not.

✔ Traveled Abroad – Customers who have travelled abroad may have different spending behaviours.

# 🔄 Step-by-Step Model Building Process

Step 1: Exploratory Data Analysis (EDA) 📊

✔ Univariate Analysis to understand the distribution of features.

# ✔ Key Performance Indicators (KPIs):

On Mobile Device KPI: Conversion rate is 15% for desktop users and 26% for mobile users.

Travel Abroad KPI: Similar conversion rates observed across both categories.

Dispatch Local Time KPI: Campaigns over the weekend show a higher conversion rate.

Age KPI: Older customers tend to have higher conversion rates.

Step 2: Data Preprocessing & Encoding

✔ Converted categorical variables into numerical values using encoding.

✔ Checked for missing values and outliers.

# 🏗️ Building the Logistic Regression Model

The logistic regression model equation:

# 𝑃 =  P=11+e−(β0+β1X1+β2X2+β3X3+...+βnXn) 

​
 
# 📌 Coefficients Obtained:

✔ Intercept (β₀): -6.012

✔ Age (β₁): 0.119

✔ Dispatch Local Time (β₂): -1.661

✔ On Mobile Device (β₃): 0.848

✔ Travel Abroad (β₄): 0.028

# 📊 Model Evaluation & Confusion Matrix

Training Set Confusion Matrix

Predicted	Actual No	Actual Yes

 No	7,248	342
 
 Yes	1 ,230	716
 
# 📌 Key Performance Metrics:

✔ Accuracy: 84%

✔ Sensitivity (Recall): 37% → Indicates how well the model identifies actual buyers.

✔ Specificity: 95% → High ability to identify non-buyers correctly.

# 📈 ROC Curve & Cutoff Selection

We experimented with different probability cutoffs to balance Sensitivity & Specificity:

Cutoff	Sensitivity	Specificity	Accuracy

0.1	89%	51%	59%

0.2	75%	73%	73%

0.3	61%	85%	80%

0.4	51%	92%	83%

0.5	37%	95%	84%

# 📌 Optimal Cutoff: 0.2

✔ At cutoff 0.2, sensitivity and specificity are balanced (75% & 73%).


# 🏆 Model Validation on Test Data

✔ Split: 60% training, 40% testing

✔ Test Set Confusion Matrix:

Predicted	Actual No	Actual Yes

No	2,449	913

Yes	219	618

# 📌 Test Set Performance:

✔ Accuracy: 73%

✔ Sensitivity: 74%

✔ Specificity: 73%

# 🔬 Advanced Statistical Analysis

In addition to logistic regression, the following models and techniques were implemented for deeper insights:

✔ Simple Linear Regression (SLR) & Ordinary Least Squares (OLS) for understanding variable relationships.

✔ Multiple Linear Regression (MLR) for feature impact analysis.

✔ Statistical Validation:

R² Score – Evaluates model fit.

p-values – Identifies statistically significant predictors.

Variance Inflation Factor (VIF) – Checks for multicollinearity among independent variables.

✔ Residual Analysis & Model Refinements to improve prediction accuracy.

# 🚀 Final Insights & Business Implications

✔ The model is stable across training and test data, making it reliable for real-world predictions.

✔ Optimal cutoff of 0.2 provides a balanced trade-off between correctly predicting buyers (sensitivity) and avoiding false positives (specificity).

✔ Banks can use this probability-based model to target marketing campaigns more effectively, focusing on high-probability buyers.

✔ The insights from this model can help in personalized credit card recommendations, leading to improved customer acquisition rates.

# 🔮 Future Recommendations & Next Steps

# 📌 Further Model Enhancements:

✔ Implement Random Forest & Gradient Boosting Models for better predictive power.

✔ Incorporate additional customer behavior data for enhanced feature engineering.

✔ Experiment with ensemble methods to improve model robustness.

# 📌 Business Strategy Applications:

✔ Use a dynamic customer segmentation approach to refine marketing strategies.

✔ Optimize email campaign timings based on Dispatch Local Time insights.

✔ Leverage predictive analytics for personalized customer offers.


