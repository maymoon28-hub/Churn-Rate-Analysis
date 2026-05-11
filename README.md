# From Data to Decisions: Client Churn Analysis in a Digital Finance Platform
![Client churn analysis poster0] <img width="1066" height="799" alt="image" src="https://github.com/user-attachments/assets/628454c2-929c-4902-a5e6-a85856fd2287" />

End‑to‑end analytics project for a digital financial services provider, focused on understanding and predicting client churn so the business can take proactive retention actions. 

## Project Overview

Client churn directly impacts revenue for digital finance platforms, especially in competitive markets where customers can easily switch to other providers. This project builds an analysis and machine learning pipeline to help a financial institution identify which customers are at risk of leaving and why.

**Goal:** Transform raw client data into actionable insights and a churn prediction model that supports data‑driven retention strategies. 

## Tools Used

This project was implemented using:

- **Microsoft Excel** – for data cleaning, feature engineering, exploratory data analysis, descriptive analytics, and visualisations (charts, summary tables, pivot tables). 
- **Orange** – for implementing and evaluating machine learning models (Logistic Regression, Random Forest, AdaBoost) using the cleaned dataset exported from Excel. 

This combination reflects a realistic workflow where business analysts work primarily in Excel and collaborate with data scientists on modelling tools. 

## Key Business Questions

- What is the overall churn rate and how serious is the problem?   
- Are inactive customers significantly more likely to leave than active ones? 
- Which age groups and product usage patterns are associated with higher churn?
- Can we build a predictive model that flags high‑risk customers early enough for intervention? 

These questions align with the priorities of digital banks and fintechs in the UAE/GCC, where customer retention is critical and acquisition costs are high. 

## Data and Preparation

The dataset represents clients of a digital financial services provider, with demographic, behavioural, and financial variables plus a churn label (`Left_Service`).

- 5,031 initial records with multiple numeric and categorical fields.  
- 5 missing and 21 duplicate records detected and removed in Excel using filters, conditional formatting, and deduplication tools.  
- Final working dataset: **5,000 unique clients** with consistent, analysis‑ready variables. 

To improve interpretability for business stakeholders, several grouped features were engineered in Excel: 
- `Age_Group` (e.g. Young, Middle, Older)  
- `Balance_Band`  
- `Income_Band`  
- `Membership_Band`  
These groupings make it easier to see which customer segments drive churn in pivot tables and charts.

## Exploratory Data Analysis & Descriptive Analytics

Most of the exploratory analysis and descriptive statistics were performed in Excel using pivot tables and charts. 

**Key findings:** 

- Overall churn rate of around **20.7%**, meaning roughly one in five customers has left the service.  
- The majority of customers are still active, but a meaningful minority has churned, indicating clear room for retention improvement.  
- **Activity_Status:** Inactive customers churn at a much higher rate than active ones, well above the company average, making inactivity a strong early warning sign.  
- **Age_Group:** The oldest age group churns the most, followed by middle‑aged customers, while the youngest group churns the least.  
- **Product_Count:** Customers with many products show higher churn, suggesting potential issues with multi‑product bundles or complexity.  

These insights were communicated with bar charts, pie charts, and grouped column charts summarised in the project poster. 

## Machine Learning Proposal and Implementation (Orange)

This is a **binary classification** problem where the target variable `Left_Service` indicates whether a client has left the platform or is still a customer. 

### Features

The model uses a mix of demographic, behavioural, and financial variables, including: [file:3]

- Age and `Age_Group`  
- `Membership_Length` and `Membership_Band`  
- `Product_Count`  
- `Activity_Status`  
- `Risk_Score`  
- `Annual_Earnings` and `Income_Band`  
- `Account_Value` and `Balance_Band`  
- `CreditCard_Flag`  
- `Region` and `Gender`  

The cleaned Excel dataset was exported as a CSV and imported into Orange for modelling. 

### Algorithms Evaluated

Using 10‑fold cross‑validation in Orange, the following models were compared:

- Logistic Regression  
- Random Forest  
- AdaBoost  

**Random Forest** was selected as the final model because: 

- It handles both numerical and categorical variables effectively.  
- It captures complex, non‑linear relationships in churn behaviour.  
- It delivered the strongest predictive performance on this dataset.  

### Performance Summary

Key metrics from the Orange evaluation:

- **Logistic Regression** – Recall: 80.7%, Precision: 77.6%  
- **Random Forest** – Recall: 84.7%, Precision: 83.5%  
- **AdaBoost** – Recall: 79.3%, Precision: 79.4%  

The Random Forest model achieved the best balance of identifying churners (recall) while limiting false positives (precision), making it suitable for targeting retention campaigns efficiently. 

## Business Insights and Recommended Actions

Translating the analytics into actions for a digital finance provider:

- **Monitor and act on inactivity.**  
  Inactive customers churn at a much higher rate, so prolonged inactivity should trigger automated re‑engagement campaigns (reminders, offers, or personalised outreach).  

- **Support older and middle‑aged customers.**  
  These age groups churn more, suggesting potential issues with usability, digital literacy, or product fit; targeted support, simplified journeys, and tailored communication can help retain them.  

- **Review multi‑product offerings.**  
  Higher churn among customers with many products may indicate complexity or dissatisfaction with bundled services; simplifying packages and improving onboarding can reduce this risk.  

These recommendations are directly actionable for product, marketing, and customer success teams in UAE and GCC‑based digital banks and fintechs.

## Files in This Repository

- `Client Churn Analysis.pdf` – Project poster summarising business context, methodology, visualisations, and key findings.   
- `Client-Churn.xlsx` – Cleaned and structured dataset used for Excel analysis and exported to Orange for modelling.
-  `Model implementation.ows`- Orange workflow file for the machine learning implementation.
- `README.md` – Project documentation for recruiters and hiring managers.  

## Skills Demonstrated

This project showcases skills that are highly relevant for data analyst and junior data scientist roles: 

- Business understanding and problem framing for financial services.  
- Data cleaning and preparation in Excel, including handling missing values, duplicates, and creating business‑friendly feature groupings.
- Exploratory data analysis and visual storytelling with Excel charts and pivot tables.   
- Supervised machine learning in Orange, including model comparison, evaluation metrics, and confusion matrix interpretation.   
- Translating technical results into practical retention strategies for stakeholders in digital banking and fintech. 
