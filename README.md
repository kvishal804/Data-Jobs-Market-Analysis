# Data-Jobs-Market-Analysis
This project analyzes the global data jobs market using Power BI, focusing on job demand, salary trends, required skills, and hiring platforms.  The project is divided into two analytical reports  
- Job Market: Overview Dashboard
- Skills vs Salary Analysis Report

 It provides insights to help aspiring data professionals make datadriven career decisions.
 
 Tools & Technologies
This project was developed using the following tools and technologies:

- Power BI – for data visualization and dashboard creation
- DAX (Data Analysis Expressions) – for building calculated measures and KPIs
- Power Query (M Language) – for data cleaning, transformation, and ETL processes
- Data Modeling – for creating relationships between tables and optimizing performance

Key Measures

Job Count = DISTINCTCOUNT('data jobs'[job id])

Skill Count = COUNT('data skills'[Value])

Skills Per Job = DIVIDE([Skill Count], [Job Count])

Median Salary India = 
CALCULATE(
    MEDIAN('data jobs'[Salary Average Yearly]),
    'data jobs'[job_country] = "India"
)

Median Salary Non India = 
CALCULATE(
    MEDIAN('data jobs'[Salary Average Yearly]),
    'data jobs'[job_country] <> "India"
)
