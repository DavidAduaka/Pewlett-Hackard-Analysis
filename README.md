# Pewlett-Hackard-Analysis

## Challenge Overview
Upon completion of his SQL queries and data he exported for his manager, Bobby recieved two more assingments from his manager: determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. After the data is stored, Bobby and I will need to write a report that summarizes our analysis and helps prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age. 

## Resources 
- Data Source: departments.csv, dept_emp.csv, dept_info.csv, dept_manager.csv, emp_info.csv, employees.csv, manager_info.csv, retirement_info.csv, retirement_titles.csv, salaries.csv, titles.csv     
- Software: Anaconda 4.10.1, pgAdmin 4 5.2

## Results
- The title that has the largest number of people who are going to retire is senior engineers. 
- The title that has the third largest number of people who are going to retire is engineers. So one can say that an influx of assistant engineers is needed to combact this sliver tsunami, assumning all the assistant engineers that are eligble to mentored move into these vacant positions. 
- The management department will have the easiet transition when its wave of employees retires. 
- There are 1940 employees that are eligible for the mentorship program. 

## Challenge Summary 
As the "silver tsunami" begins to make an impact there are 90,398 roles that need to be filled. Pewlett Hackard hdoes not have enough employees that are eligible to mentored in for these roles. To combact this the company, a "unique_mentorship" table needs to be created to identifty the count of mentorship eligible employees for each title. Also the company needs to create a table called "tenure" and determine the minimum amount of years needed for a certain title to be able to mentor someone to fill their role in the foreseable future. For example after five years an engineer can mentor an assistant engineer on how to function in that role. 
