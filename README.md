# HR Dashboard


---


# Table of Contents

- [Problem Statement](https://github.com/jiang54/HR-Dashboard#Problem-Statement)
- [Data Sourcing](https://github.com/jiang54/HR-Dashboard#Data-Sourcing)
- [Data Preparation](https://github.com/jiang54/HR-Dashboard#Data-Preparation)
- [Data Modeling](https://github.com/jiang54/HR-Dashboard#Data-Modeling)
- [Data Analysis](https://github.com/jiang54/HR-Dashboard#Data-Analysis)
- [Data Visualization](https://github.com/jiang54/HR-Dashboard#Data-Visualization)
- [Insights](https://github.com/jiang54/HR-Dashboard#Insights)
- [Virtual Case Experience Link](https://github.com/jiang54/HR-Dashboard#Virtual-Case-Experience-Link)


---

# Problem Statement

The purpose of this analysis is to: 
- Create a visualisation for the HR manager that reflects all relevant Key Performance indicators(KPIs)
and metrics in the dataset.


# Data Sourcing

The Dataset used for this analysis was presented by [Data with Decision](https://drive.google.com/file/d/1ry1vckMKG_Koq71jRvKROHMy7rrdYQmR) and available at:

- [HR Analytics Data](https://github.com/jiang54/HR-Dashboard/blob/main/HR%20Analytics%20Data.csv)


---

# Data Preparation

The following measures used to define proper KPIs (Not include all):
- '%' of male
- '%' of female
- %Due for Promotion
- %Not Due
- %On Services
- %Retrench

---

Data transformation was done in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.

The HR Analytics Data dataset is given by a table named:

- `HR Manager` which has `38 columns and 1470 rows` of observation


The tabulation below shows the `HR Analytics Data` table with its column names and their description:

| Column Name | Description |
| ----------- | ----------- |
| Age | Represents the age of the employee. |
| Attrition | Describes if the employee has left the company. |
| BusinessTravel | Describes the frequency of the employee's business travel. |
| DailyRate | Represents the employee's daily rate of pay. |
| Department | Describes the department in which the employee works. |
| DistanceFromHome | Represents the distance between the employee's home and workplace. |
| Education | Represents the highest level of education achieved by the employee. |
| EducationField | Describes the field in which the employee's highest education degree was obtained. |
| EmployeeCount | Represents the number of employees in the same group as the employee. |
| EmployeeNumber | Represents the unique number assigned to the employee in the dataset. |
| EnvironmentSatisfaction | Represents the employee's level of satisfaction with the work environment. |
| Gender | Describes the gender of the employee. |
| HourlyRate | Represents the employee's hourly rate of pay. |
| JobInvolvement | Represents the employee's level of involvement in their job. |
| JobLevel | Represents the level of the employee's job within the organization. |
| JobRole | Describes the employee's job role. |
| JobSatisfaction | Represents the employee's level of job satisfaction. |
| MaritalStatus | Describes the marital status of the employee. |
| MonthlyIncome | Represents the employee's monthly income. |
| MonthlyRate | Represents the employee's monthly rate of pay. |
| NumCompaniesWorked | Represents the number of companies the employee has worked for. |
| Over18 | Describes if the employee is over 18 years old. |
| OverTime | Describes if the employee works overtime. |
| PercentSalaryHike | Represents the percentage increase in the employee's salary. |
| PerformanceRating | Represents the employee's performance rating. |
| RelationshipSatisfaction | Represents the employee's level of satisfaction with work relationships. |
| StandardHours | Represents the standard number of hours worked per day. |
| StockOptionLevel | Represents the employee's level of stock option grants. |
| TotalWorkingYears | Represents the total number of years the employee has worked. |
| TrainingTimesLastYear | Represents the number of times the employee received training in the last year. |
| WorkLifeBalance | Represents the employee's level of work-life balance. |
| YearsAtCompany | Represents the number of years the employee has worked at the company. |
| YearsInCurrentRole | Represents the number of years the employee has been in their current role. |
| YearsSinceLastPromotion | Represents the number of years since the employee's last promotion. |
| YearsWithCurrManager | Represents the number of years the employee has worked with their current manager. |
