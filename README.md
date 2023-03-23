# HR Dashboard


---
![image](https://user-images.githubusercontent.com/24377958/227189737-396e6aea-baa5-45ea-b80d-35b6f559b299.png)


# Table of Contents

- [Problem Statement](https://github.com/jiang54/HR-Dashboard#Problem-Statement)
- [Data Sourcing](https://github.com/jiang54/HR-Dashboard#Data-Sourcing)
- [Data Preparation](https://github.com/jiang54/HR-Dashboard#Data-Preparation)
- [Data Modeling](https://github.com/jiang54/HR-Dashboard#Data-Modeling)
- [Data Analysis](https://github.com/jiang54/HR-Dashboard#Data-Analysis)
- [Data Visualization](https://github.com/jiang54/HR-Dashboard#Data-Visualization)
- [Insights](https://github.com/jiang54/HR-Dashboard#Insights)


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


Data Cleaning for the dataset was done in power query as follows:

- Rows with missing values may carry important information and should not be indiscriminately removed
- Each of the columns in the table were validated to have the correct data type 

---

# Data Modeling

After the dataset was cleaned and transformed, it was ready to be add measures(using Power BI Desktop).

- The fact and dimension have been combined into one table and is shown in the data model below
![image](https://user-images.githubusercontent.com/24377958/227189926-2271cccb-016f-4f64-aa24-9b4cf5a1201c.png)
# Data Analysis
Add Necessary Measures

![image](https://user-images.githubusercontent.com/24377958/227189977-16799a85-6c1d-496d-9feb-99a7ae1becca.png)
% Female = DIVIDE('All Measures'[Total Female],'All Measures'[Total Employee],"ERROR")
% male = DIVIDE([Total Male],[Total Employee],"ERROR")
%Due for Promotion = DIVIDE([Due for Promotion],[Total Employee],"ERROR")
%Not Due = DIVIDE([Not Due],[Total Employee],"ERROR")
%On Services = [On services]/[Total Employee]
%Retrench = [Will be retrenched]/[Total Employee]
Due for Promotion = if(ISBLANK(CALCULATE([Total Employee],'HR Analytics Data'[Promotion Status]  = "due for promotion")),0,CALCULATE([Total Employee],'HR Analytics Data'[Promotion Status]  = "due for promotion"))
Not Due = CALCULATE([Total Employee],'HR Analytics Data'[Promotion Status]  = "Not Due")
On services = if(ISBLANK(CALCULATE([Total Employee],'HR Analytics Data'[Retrenchedment Status] = "On Services")),0,CALCULATE([Total Employee],'HR Analytics Data'[Retrenchedment Status] = "On Services"))
Total Employee = COUNTROWS('HR Analytics Data')
Total Female = CALCULATE([Total Employee],'HR Analytics Data'[Gender] = "Female")
Total Male = CALCULATE('All Measures'[Total Employee],'HR Analytics Data'[Gender] = "Male")
Will be retrenched = if(ISBLANK(CALCULATE([Total Employee],'HR Analytics Data'[Retrenchedment Status] = "Will be retrenched")),0,CALCULATE([Total Employee],'HR Analytics Data'[Retrenchedment Status] = "Will be retrenched"))


# Data Visualization

Data visualization for the dataset is done in 2 parts to ensure a clearer and more effective presentation of the data.
![image](https://user-images.githubusercontent.com/24377958/227189737-396e6aea-baa5-45ea-b80d-35b6f559b299.png)

# Insights

Shown in [Data Visualization](https://github.com/jiang54/HR-Dashboard#Data-Visualization):


- It can be seen that in this organization, the ratio of male to female is about 6:4. In addition, the remaining ratios (such as length of service, promotion plan, job level, etc.) are also 6:4, which shows that the organization has a certain degree of balance in these aspects, or tends to maintain relative justice and equality.
---

