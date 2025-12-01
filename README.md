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
## Key DAX Measures

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



