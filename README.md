# Telco Customer Churn Analysis

<!--
## Table of Contents

- ## Table of Contents

- [📂 Project Overview](#-project-overview)
- [Key Objectives](#key-objectives)
- [Data Preparation](#data-preparation)
- [Dataset Used](#dataset-used)
- [Analysis Goals](#analysis-goals)
-->
  
## 📂 Project Overview
This repository contains an analysis of customer churn for a telecommunications company. The dataset includes customer demographics, service details, account information, and whether the customer churned (left the service). The goal of this analysis is to identify patterns and factors that influence customer churn and provide actionable insights to reduce churn rates.

## 🧰 Key Objectives
- Analyze customer churn trends based on contract types, tenure, and gender.
- Derive and utilize additional metrics to support clearer insights.
- Identify segments with high churn rates and opportunities for retention.

## 📊 Dataset Used
<a href="https://github.com/judefrank/CustomerChurnAnalysis/raw/main/Churn%20Analysis%20Project.xlsx" target="_blank">Customer Churn Analysis Data Set</a>

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

- Churn Rate: Defined as -->

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
- Billing System
- Partnership Status

#### 🧮 Values:
- Total Counter: total number of customers in each segment.
- Churn Rate: proportion of customers who churned.
- Average Monthly Charges: financial weight of each customer segment.

#### 🧠 Analysis Goals
1. Exploratory Data Analysis (EDA): Understand the distribution of features and their relationship with churn.
2. Feature Importance: Identify which features are most predictive of churn.
3. Predictive Modeling: Build a model to predict customer churn.
4. Actionable Insights: Provide recommendations to reduce churn based on the analysis.

## 📊 Visualizations
Excel charts were created to visualize churn rate trends and churn comparison across different segments:


<!--
### Objectives
- Perform Exploratory Data Analysis (EDA) on customer data.
- Identify trends and patterns in churn behavior.
- Build predictive models to classify customers likely to churn.
- Provide actionable insights and business recommendations.
-->

### Dashboard (Analysis Per Contract Type)
![Analysis Per Contract Type](https://github.com/user-attachments/assets/023b8483-0c22-4ee5-b146-da7746f19c2d)

### Insights:

- Month-to-month contracts show significantly higher churn (42.7%), despite having only a slightly higher monthly charge than longer-term plans.
- Customers on Two-year contracts have extremely low churn (2.8%), indicating stronger loyalty.
- Incentivizing longer contract commitments (possibly with minor discounts) could significantly reduce churn.

### Dashboard (Analysis Per Gender)
![Analysis Per Gender](https://github.com/user-attachments/assets/65b287c3-61f2-4b5e-8398-ce1908dd58b0)

### Insights:
- Gender has minimal impact on churn in your dataset (less than 1% difference).
- Monthly charges are also similar. Gender may not be a valuable segmentation variable for churn intervention.

### Dashboard (Analysis Per Partnership Status)
![Analysis Per Partnership Status](https://github.com/user-attachments/assets/19eaf199-b76f-4360-beb2-313dfb646211)

### Insights:
- Non-partnered individuals churn 68% more than partnered ones.
- Despite paying less, non-partnered users churn more, suggesting that financial burden isn’t the only driver. It could relate to perceived value or engagement levels.
- Consider engagement programs targeted at single customers, e.g., loyalty perks, social referrals, or content-based retention campaigns.

### Dashboard (Analysis Per Billing System)
![Analysis Per Billing System](https://github.com/user-attachments/assets/4a2befcf-6060-4f21-8b01-cff49e3b3881)

### Insights:
- Paperless billing customers churn twice as much as those on paper-based billing.
- They also pay much higher monthly fees (₦73.55 vs. ₦51.99).
- This suggests a possible price sensitivity or digital fatigue effect. Customers paying more (and possibly seeing less human interaction) may feel less loyalty.
- Investigate whether digital bill recipients are getting sufficient value communication. Consider personalized outreach or bundling benefits with e-billing.

## 🔍 Overall Strategic Insights:
1. Contract length is the strongest predictor of churn — targeting customers on month-to-month contracts for upgrades could significantly reduce churn.
2. Partnership status and billing type are high-influence behavioral factors; they might reflect lifestyle and digital preferences that can be strategically addressed.
3. Gender has little impact, so interventions should focus more on contract type, billing behavior, and relationship status.
4. Higher-paying customers are not necessarily more loyal, especially those using paperless billing — you need to improve perceived value for high spenders.









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

