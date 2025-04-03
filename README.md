HR-Analytics-Dashboard

Problem Statement

The HR Analytics Dashboard provides insights into workforce trends, employee performance, attrition rates, and other key HR metrics. It helps HR teams make data-driven decisions to improve employee satisfaction, reduce turnover, and optimize workforce planning. By monitoring key HR indicators, businesses can enhance their talent management strategies and create a more engaged workforce.

Steps Followed

Step 1 : Loaded HR data (CSV format) into Power BI Desktop.

Step 2 : Opened Power Query Editor and checked column quality, distribution, and profile.

Step 3 : Ensured column profiling was based on the entire dataset.

Step 4 : Identified and handled null or incorrect values in columns like Salary, Attrition, and Performance Rating.

Step 5 : Created calculated columns and measures using DAX for KPI tracking.

Step 6 : Applied visual filters (slicers) for fields like Department, Job Role, Gender, and Employment Type.

Step 7 : Designed the dashboard layout using Power BI visualizations such as bar charts, line charts, and card visuals.

Step 8 : Created an HR performance KPI section with calculated metrics.

Step 9 : Inserted branding elements like the company logo, title, and tagline.

Step 10 : Published the report to Power BI Service for sharing and collaboration.

DAX Calculations

1. Total Employees

Total Employees = COUNT(HRData[Employee ID])

2. Employee Attrition Rate (%)

Attrition Rate =
VAR TotalEmployees = [Total Employees]
VAR AttritedEmployees = COUNTROWS(FILTER(HRData, HRData[Attrition] = "Yes"))
RETURN DIVIDE(AttritedEmployees, TotalEmployees) * 100

3. Average Employee Tenure (Years)

Average Tenure = AVERAGE(HRData[Years at Company])

4. Average Salary

Average Salary = AVERAGE(HRData[Salary])

5. Employee Satisfaction Score

Satisfaction Score = AVERAGE(HRData[Job Satisfaction])

6. Employee Turnover by Department

Turnover Rate =
VAR TotalDeptEmployees = COUNT(HRData[Employee ID])
VAR AttritedDeptEmployees = COUNTROWS(FILTER(HRData, HRData[Attrition] = "Yes"))
RETURN DIVIDE(AttritedDeptEmployees, TotalDeptEmployees) * 100

Dashboard Snapshots

Power BI Desktop Report

![HR Analytics Dashboard Snapshot - Desktop]

![Image](https://github.com/user-attachments/assets/1b7de19e-1597-4f85-a956-62aff4987e8f)
![Image](https://github.com/user-attachments/assets/99a3e2fd-e776-48e9-a0c2-e2838d621172)
![Image](https://github.com/user-attachments/assets/d0c18249-1a7e-468e-ae18-7e7bc87bbd70)

Conclusion

The HR Analytics Dashboard provides in-depth insights into employee performance, satisfaction, and retention trends. HR teams can use these insights to develop data-driven strategies for improving workplace satisfaction and reducing turnover. Future improvements can include predictive modeling for attrition and AI-driven insights for workforce optimization.

Developed Using: Power BI | DAX | Data Analytics

