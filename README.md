<p align="center">
  <img src="https://raw.githubusercontent.com/BathulaVenuGopal9/-Customer-Churn-Analysis-Predictive-Insights--Power-BI-Project/main/c4062968-ad50-4f65-b573-9ed8f514b271.png" alt="Customer Churn Analysis Banner" width="100%">
</p>

# Customer Churn Analysis & Predictive Insights | Power BI Project

##  Project Overview
An end-to-end Power BI project analyzing telecom customer churn using advanced data visualization, DAX measures, segmentation analysis, and predictive indicators. The dashboard explores demographics, service usage, billing patterns, contract types, and customer behavior to uncover key churn drivers. It also includes AI-based churn risk scoring, high-risk customer identification, revenue impact analysis, and actionable business recommendations to improve retention.

---

##  Business Problem
Telecom companies lose significant revenue because customers discontinue services (churn). Understanding which customers churn and why is critical to improving long-term profitability.

This project helps answer:
- Who is most likely to churn?
- What factors drive churn?
- What is the revenue impact of churn?
- Which customer segments should be retained aggressively?
- How can churn be reduced using insights?

---

##  Skills Demonstrated
- **Power BI Desktop** – Data modeling, interactive dashboards, custom visuals  
- **DAX Measures** – Creating KPIs, churn calculations, segmentation logic  
- **EDA (Exploratory Data Analysis)** – Trend analysis, behavioral patterns  
- **Predictive Analysis Concepts** – AI-driven churn risk insights  
- **Customer Segmentation** – High/Medium/Low churn risk grouping  
- **Data Storytelling** – Presenting insights via dashboard + PPT  
- **BI Reporting** – Churn rate, revenue impact, tenure, ARPU  
- **SQL Concepts** – Data preparation understanding (industry expectation)  
- **Python (Optional Extension)** – Base for ML churn model enhancement  

---

##  Data Model & Schema

The project uses a simplified star-schema model optimized for analytical reporting.

###  Customer Table
- CustomerID  
- Gender  
- SeniorCitizen  
- Partner / Dependents  
- Tenure  
- Contract Type  
- Payment Method  
- Paperless Billing  
- Monthly Charges  
- Total Charges  
- Churn (Yes/No)

###  Services Table
- Internet Service (DSL / Fiber / None)  
- Online Security  
- Online Backup  
- Device Protection  
- Tech Support  
- Streaming TV  
- Streaming Movies  
- Phone Service  

---

##  Key DAX Measures

```DAX
Churn Rate =
DIVIDE(
    CALCULATE(COUNT(Customer[CustomerID]), Customer[Churn] = "Yes"),
    COUNT(Customer[CustomerID])
)

Churned Customers =
CALCULATE(COUNT(Customer[CustomerID]), Customer[Churn] = "Yes")

Total Customers =
COUNT(Customer[CustomerID])

Avg Monthly Charges =
AVERAGE(Customer[MonthlyCharges])

Avg Tenure =
AVERAGE(Customer[Tenure])

Revenue Lost =
CALCULATE(SUM(Customer[TotalCharges]), Customer[Churn] = "Yes")
# Key Insights & Analysis
1. Demographic Insights
Senior citizens churn significantly more.

New customers (tenure ≤ 12 months) show the highest churn.

Long-term customers exhibit strong retention.

2. Service Usage Trends
Fiber Optic users have the highest churn rate.

Customers with fewer add-on services churn more.

Multi-service bundles increase loyalty.

3. Contract & Billing Behavior
Month-to-month customers: highest churn

One-year contracts: moderate churn

Two-year contracts: lowest churn

Electronic check users: highest churn among payment methods

Auto-payment customers are more loyal

4. Revenue Impact
Customers on short-term plans produce high churn-related revenue loss.

Two-year contract users contribute the highest total revenue.

# Predictive Insights (AI-Based)
The Power BI AI Visual identifies high-risk churn profiles:

Short tenure (0–12 months)

High monthly charges

Month-to-month contracts

Fiber optic internet

Electronic check payments

Senior citizens (slightly higher risk)

These segments require targeted retention efforts.

# Churn Risk Segmentation
The dashboard categorizes customers into:

High Risk – Short tenure, high charges, electronic check, month-to-month

Medium Risk – Moderate service usage and charges

Low Risk – Loyal long-term customers with bundled services

# Business Recommendations
Improve onboarding for customers in the first 12 months.

Encourage migration from month-to-month to annual contracts.

Enhance Fiber Optic service quality and tech support.

Promote automatic payment methods to reduce churn.

Offer discounts or loyalty benefits to high-risk segments.

Cross-sell bundled services to increase retention.

Use AI churn scores to prioritize retention campaigns.

# Project Files
Customer_Churn_Analysis.pbix – Main Power BI dashboard

Customer_Churn_Presentation.pptx – Final project explanation

/Screenshots/ – Dashboard visuals (optional)

banner.png – Repo banner image (optional)

# Author
Bathula Venu Gopal
Data Science & BI Enthusiast
Power BI | SQL | Python | ML | Analytics | Storytelling

## Thank You ##
