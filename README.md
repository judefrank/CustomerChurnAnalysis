# Telco Customer Churn Analysis

## Table of Contents

- [Project Overview](#project-overiew)
- [Key Objectives](#key-objectives)
-  [Data Preparation](#data-preparation)
- [Dataset](#dataset)
- [Analysis Goals](#analysis-goals)

### 📂 Project Overview
This repository contains an analysis of customer churn for a telecommunications company. The dataset includes customer demographics, service details, account information, and whether the customer churned (left the service). The goal of this analysis is to identify patterns and factors that influence customer churn and provide actionable insights to reduce churn rates.

### 🧰 Key Objectives
- Analyze customer churn trends based on contract types, tenure, and gender.
- Derive and utilize additional metrics to support clearer insights.
- Identify segments with high churn rates and opportunities for retention.

### 📊 Dataset
- customerID: Unique identifier for each customer.
- gender: Customer's gender (Male/Female).
- SeniorCitizen: Indicates if the customer is a senior citizen (1) or not (0).
- Partner: Whether the customer has a partner (Yes/No).
- Dependents: Whether the customer has dependents (Yes/No).
- tenure: Number of months the customer has stayed with the company.
- PhoneService: Whether the customer has a phone service (Yes/No).
- MultipleLines: Whether the customer has multiple lines (Yes/No/No phone service).
- InternetService: Type of internet service (DSL, Fiber optic, No).
- OnlineSecurity: Whether the customer has online security (Yes/No/No internet service).
- OnlineBackup: Whether the customer has online backup (Yes/No/No internet service).
- DeviceProtection: Whether the customer has device protection (Yes/No/No internet service).
- TechSupport: Whether the customer has tech support (Yes/No/No internet service).
- StreamingTV: Whether the customer has streaming TV (Yes/No/No internet service).
- StreamingMovies: Whether the customer has streaming movies (Yes/No/No internet service).
- Contract: Type of contract (Month-to-month, One year, Two year).
- PaperlessBilling: Whether the customer uses paperless billing (Yes/No).
- PaymentMethod: Payment method (Electronic check, Mailed check, Bank transfer, Credit card).
- MonthlyCharges: Monthly charges for the customer.
- TotalCharges: Total charges for the customer.
- Churn: Whether the customer churned (Yes/No).

## 🧹 Data Preparation
Several new fields were created in Excel to support enhanced analysis:

- **Tenure in Years**  
  Converted the `tenure` field from months to full years:
  =ROUNDDOWN(tenure / 12, 0)
  
- **Churn Counter**  
Created a boolean flag for churned customers:
=IF(Churn = "Yes", 1, 0)

- **Total Counter**  
Ensured no duplicate customer IDs using `COUNTIF`:
=COUNTIF(customerID_range, customerID)

- Churn Rate: Defined as:
=Churn Counter / Total Counter
Used in pivot tables to evaluate churn intensity across segments.


- **Churn Rate**  
Calculated churn rate within each group (used in pivot tables):


These derived columns allowed for meaningful segmentation and aggregation in pivot table analysis, enabling clearer insights on churn behavior across demographics and service categories.


## 📈 Exploratory Analysis (Pivot Table)
Pivot tables were created to examine churn behavior across key segments:

#### 🎯 Rows:
- Contract Type
- Gender
- Tenure in Years

#### 🧮 Values:
- Total Counter – total number of customers in each segment.
- Churn Rate – proportion of customers who churned.
- Average Monthly Charges – financial weight of each customer segment.

#### 🧮 Analysis Goals
1. Exploratory Data Analysis (EDA): Understand the distribution of features and their relationship with churn.
2. Feature Importance: Identify which features are most predictive of churn.
3. Predictive Modeling: Build a model to predict customer churn.
4. Actionable Insights: Provide recommendations to reduce churn based on the analysis.

<!--
### Objectives
- Perform Exploratory Data Analysis (EDA) on customer data.
- Identify trends and patterns in churn behavior.
- Build predictive models to classify customers likely to churn.
- Provide actionable insights and business recommendations.
-->

### Visuals
![Response Payload](https://github.com/user-attachments/assets/ed615960-9614-4716-9b26-69c28939ed56)


<!--
### Business Insights
- Customers with longer call durations but low customer support interaction are less likely to churn.
- Monthly contract customers are at higher risk of churn than annual contract customers.
- Churn is significantly higher among customers with high service issues and low engagement.

### Data Sources
Source: Kaggle
Size: ~7,000 records
Features: Demographics, Account Info, Usage Patterns, Contract Type, Churn Status

### Tools
- MS Excel - Data Cleaning
  - [Download here](https://microsoft.com)
- SQL Server - Data Analysis
- Power BI - Creating reports

### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection
2. Handling missing values
3. Data cleaning and formatting

### Recommendations
Based on the findings, the following business actions are recommended:

1. Encourage Long-Term Contracts:
Offer discounts or incentives for customers to move from monthly to yearly contracts.
2. Improve Onboarding Experience:
Reduce early churn by enhancing support and engagement during the first 3–6 months.
3. Review Pricing Strategy:
High monthly charges were linked with higher churn, especially for low-tenure users—consider bundling or discounts.
4. Target At-Risk Customers:
Use predictive churn scores to prioritize customer retention campaigns and personalized outreach.
5. Digital Payment Engagement:
Promote use of auto-pay or credit card payments which are associated with lower churn compared to electronic checks.

### Limitations

💻
|S/N|Tools|
|---|---|
|1|Excel|
|2|SQL|
|3|PowerBI|

`column1`


**bold**


*italic*

