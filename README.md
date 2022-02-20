# Pewlett-Hackard-Analysis by David Aduaka

## Overview of the Pewlett Hackard Analysis
Pewlett Hackard is a large company with several thousand employees. With Baby-Boomers retiring, it has tasked its HR group to do two main tasks. First, it wants to know how many of its employees are retirement eligible. Second, it wants to know what positions will become vacant so that it can adequately plan to fill them in the future. Furthermore, I am to determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program.

## Resources 
- Data Sources: employees.csv, departments.csv, titles.csv, salaries.csv, dept_emp.csv, dept_manager.csv
- Software: PostGreSQL 11, pgAdmin 4, Visual Studio Code

## Results
#### Deliverable 1: The Number of Retiring Employees by Title

The first deliverable was to create tables that listed all employees who were retirement eligible, and then a final table that has the number of retirement-age employees by their most recent job title. This filtered the employees.csv by those born between 1952 and 1955, and joining it with the titles.csv to determine the employees' titles. By utilizing INNER JOIN, DISTINCT ON, ORDER BY, and COUNT(), I created the following list.

![image](https://user-images.githubusercontent.com/70069730/154860298-ddfe7307-1595-4fc8-936e-992e3ca03338.png)

The table shows that Pewlett Hackard has 29,414 Senior Engineers and 28,254 Senior Staff employees who are retirement eligible. In total, 90,398 employees could retire. But it begs a question; how much is that compared to Pewlett Hackard's entire workforce? This will be explored in the summary.

#### Deliverable 2: The Employees Eligible for the Mentorship Program

The second deliverable sought to determine how many employees were eligible for the Mentorship program. These were individual 10 years from retirement (aged 55) and could train and advise new hires/promoted employees in their functions. Again, I employed functions like INNER JOIN, DISTINCT ON, ORDER BY, and COUNT() on the Employees and Department Employees tables. The resulting Mentorship Eligibility Table was exported as a csv and is shown here. 1,549 would be eligible under the

![image](https://user-images.githubusercontent.com/70069730/154860336-729af6d2-1757-4043-9736-1e0bcc28d568.png)

1,549 Pewlett Hackard employees would be eligible under the current requirements of the Mentorship program. A pivot table of the csv shows that most of the eligible mentors were hired in 1999 and have 21 years in their title. On average, the eligible mentors have 27 years experience.

![image](https://user-images.githubusercontent.com/70069730/154860352-c99e2130-662b-4ab9-a8d4-a96f5dd72005.png)

## Summary 

  #### How many roles will need to be filled as the "silver tsunami" begins to make an impact?
 
Based on Deliverable 1, 90,398 Pewlett Hackard employees are retirement eligible. If they all decide to retire, all 90,398 positions would need to be filled.

  #### Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
  
Based on Deliverable 2, there are only 1,549 eligible employees that could be part of the mentorship program. On a 1-to-1 training basis, this would certainly not be enough to mentor all new hires and promotions.

  #### Additional questions and views:
  
As mentioned before, while 90,398 retirement eligible employees is a large amount, what is that in comparison to the entire organization? The following table answers that very question.

The following query joined the total employee table with the titles table, and then summarized the count of each title.

![image](https://user-images.githubusercontent.com/70069730/154860554-155c779c-58bc-4886-9958-d9cc3a0d86f8.png)

Then, using an INNER JOIN to the retiring_titles table, it compared the counts of the retiring titles to the total counts, and calculated the percentage. Below is the code and the resulting table.

![image](https://user-images.githubusercontent.com/70069730/154860572-9b85e5bc-11b2-45e6-a2e0-1dd58fab43fc.png)

![image](https://user-images.githubusercontent.com/70069730/154860591-af0f0fdb-7ffd-40c4-b19d-dbec4133f2f7.png)

We see that in all cases, except for Manager, Pewlett Hackard could lose approximately 30% of its workforce. This would be devastating for their operations, and would require aggressive hiring.

Second, I stated that a 1-to-1 Mentoring model would not be possible given the number of eligible mentors. The following code examined how many mentees would each mentor have if all vacancies from retirement-eligible employees needed to be filled and all mentorship-eligible employees agreed to mentor.

![image](https://user-images.githubusercontent.com/70069730/154860603-5839858a-b605-4a2c-b09f-d4a489d58c2d.png)





