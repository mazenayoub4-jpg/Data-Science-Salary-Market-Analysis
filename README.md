# Data-Science-Salary-Market-Analysis
​"End-to-end Business Intelligence solution analyzing global Data Science compensation trends (2020-2024). Developed using Star Schema modeling, advanced DAX logic for multi-currency standardization, and AI-driven narrative reporting."
 Project Overview
​This repository features an end-to-end Business Intelligence solution that analyzes global salary trends in the Data Science sector. Using a dataset of over 10,000 records, I transformed raw data into a strategic dashboard that evaluates compensation across geographic regions, experience levels, and remote-work models.
​🛠️ Technical Stack
​Tool: Microsoft Power BI
​Language: DAX (Data Analysis Expressions)
​Modeling: Star Schema / Relational Modeling
​AI: Smart Narrative (Generative Insights)
​🧠 Key Technical Achievements
​ Data Modeling & Architecture
​I architected a robust Star Schema to optimize report performance. By separating dimension tables (Experience, Geography, Job Roles) from the fact table, I ensured high-speed cross-filtering and data integrity.
​ Advanced DAX Engineering
​I developed custom business logic using advanced DAX to standardize global metrics.
​Dynamic Performance Benchmarking: Implemented SWITCH(TRUE()) logic to categorize salary levels against global targets.
​Complex Context Filtering: Leveraged CALCULATE and ALL to create comparative KPIs that stay accurate regardless of slicer selection.
​ UI/UX & Executive Reporting
​Slate Grey & Navy Theme: Designed for a professional corporate aesthetic to reduce cognitive load for stakeholders.
​Interactive Storytelling: Integrated Smart Narratives that use natural language generation to explain "The Why" behind the numbers automatically.
​📈 Featured Measures
​In this project, I utilized the following standardized measures:
​Global_Mean_Compensation_USD: Standardized average salary across all job titles.
​Comp_Performance_Benchmark: A logic-based indicator for market value status.
​YoY_Compensation_Variance: Tracking year-over-year growth in data science roles.

### Salary_Status = 
```dax
VAR AvgSalary = [Global_Mean_Compensation_USD]
VAR Target = 150000 -- Global Baseline
RETURN 
SWITCH( TRUE(),
    AvgSalary >= Target, "Elite Tier",
    AvgSalary >= Target * 0.75, "Market Average",
    "Below Benchmark"
)
Dynamic KPIs:
​I utilized CALCULATE and KEEPFILTERS to ensure that the year-over-year growth and geographic distributions remained accurate even when multiple slicers (like Seniority and Employment Type) were applied simultaneously.
​🎨 Design & UX Strategy
​I chose a Slate Grey & Navy aesthetic to maintain a professional "SaaS" feel.
​Navigation: Instead of standard dropdowns, I used Tile Slicers for 'Experience Level' (EN, MI, SE, EX). This makes the interface touch-friendly and intuitive.
​AI-Integration: I integrated a Smart Narrative engine. It doesn't just show data; it explains the "why" behind the trends in real-time as you filter the report.
​Geospatial Analysis: Used conditional formatting on maps to highlight high-concentration "Salary Hubs" instantly.

### Market Performance Logic:
```dax
Salary_Status = 
VAR AvgSalary = [Global_Mean_Compensation_USD]
VAR Target = 150000 
RETURN 
SWITCH( TRUE(),
    AvgSalary >= Target, "Elite Tier",
    AvgSalary >= Target * 0.75, "Market Average",
    "Below Benchmark"
)
