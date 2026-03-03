# HR-Attrition-Analysis
SQL and Power BI project analyzing employee attrition patterns
HR Attrition Analysis Dashboard
📌 Project Overview

This project analyzes employee attrition patterns using SQL and Power BI.

🛠 Tools Used

SQL

Power BI

DAX

📊 Key KPIs

Total Employees

Employees Left

Attrition Rate

Attrition by Department

Attrition by Age Group

🔎 Key Insights

16% overall attrition rate

Highest attrition in first 2 years

Sales department shows higher turnover

Age group 26–35 most affected<img width="1920" height="1080" alt="dashboard png" src="https://github.com/user-attachments/assets/15bc505f-57c8-4a72-9d48-df85addcd958" />
 select count(case when Attrition = 'Yes' then 1 end)* 100.0/count(*) 
 As Attrition_rate from employees_cleaned;
 select Department, count(*) As total_employees,sum(case when Attrition = 'yes' 
then 1 ELSE 0 END) As Employees_left,sum(case when Attrition ='yes' then 1 ELSE 0 END )*
 100.0/ count(*) As Attrition_rate  from employees_cleaned group by department ;
 select Attrition, count(*) As employee_count  from employees_cleaned 
group by Attrition ;

