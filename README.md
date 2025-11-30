# IT-Expenditure-Analysis-
Interactive Power BI report with KPI tracking, cost analysis, region-wise breakdown, trend analysis, and actionable insights for IT budget optimization.
# IT Expenditure Analysis Dashboard  
### Developed in Power BI | End-to-End Data Analytics Project

This project provides a complete analysis of **Global IT Expenditure** across Business Areas, IT Areas, Regions, and Cost Categories.  
The dashboard delivers actionable insights by comparing **Actual vs Plan vs Forecast**, and highlights major cost drivers across the organization.

---

## Project Overview

The objective of this dashboard is to help organizations:

- Understand **where IT budget is being spent**
- Identify **top cost drivers** (Labor, Infra, Software etc.)
- Analyze spending by **Region, Business Area, IT Area & Sub-Areas**
- Compare **Actual vs Plan vs Forecast** performance
- Identify opportunities for **cost optimization and operational efficiency**

This is a 3-page Power BI report designed for leadership-level review.

---

##  Dataset Details

The dataset contains the following key fields:

- **Date (Month)**
- **Business Area**
- **Region & Country**
- **IT Area & IT Sub-Area**
- **Cost Element Group & Sub-Group**
- **Actual Spend**
- **Forecast**
- **Plan**

A custom **Date Table** is created to support time intelligence functions.

---

##  Report Pages

###  Page 1 – Global Overview**
This page gives a high-level summary including:

- Total Actual Spend  
- Total Forecast  
- Total Plan  
- Variance & Variance %  
- YoY Growth  
- Cost Element Group Breakdown  
- Business Area Breakdown  
- IT Area Spend (Donut Chart)  
- Monthly Trend  
- Actual vs Plan vs Forecast comparison  

This page is designed for executive-level decision making.

---

### **📌 Page 2 – Deep Dive Analysis**
This page focuses on detailed breakdowns:

- Country-wise IT Spend (Filled Map)  
- IT Sub-Area Spend  
- Cost Element Group Detailed Breakdown  
- Complete transaction-level table  
- Region/Function/Category drilldown support using slicers  

Helps identify root causes and deep insights.

---

###  Page 3 – Key Insights & Recommendations**
Summarizes the analysis:

#### **Key Insights**
- Labor is the largest IT cost driver  
- North America shows the highest regional spend  
- Infrastructure and Administration consume major IT budget  
- Actual spend is 28% below Plan (cost-saving opportunity)

#### **Recommendations**
- Optimize labor allocation & outsourcing  
- Review infrastructure modernization  
- Monitor Q2–Q4 spend drop  
- Improve forecast accuracy  
- Strengthen cost transparency  

This page is ideal for presentations and business reviews.

---

## Tools & Technologies Used

- **Power BI** – Data Modeling, DAX, Visualizations  
- **Power Query** – Data Cleaning & Transformation  
- **DAX** – Measures (Variance, YoY, MoM, Forecasting, etc.)  
- **Excel** – Base Dataset  

---

## Key DAX Measures

```dax
Total Actual = SUM('Data'[Actual])

Total Forecast = SUM('Data'[Forecast])

Total Plan = SUM('Data'[Plan])

Variance = [Total Actual] - [Total Plan]

Variance % = DIVIDE([Variance], [Total Plan])

Actual LY = CALCULATE([Total Actual], SAMEPERIODLASTYEAR(DateTable[Date]))

YoY Growth % = 
DIVIDE([Total Actual] - [Actual LY], [Actual LY])
