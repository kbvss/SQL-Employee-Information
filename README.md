# SQL Employyee Information Database 
This repository holds the code and queries for this project

# Employee data base
This repository was migrated from [Launchpad](https://launchpad.net/test-db).
See usage in the [MySQL docs](https://dev.mysql.com/doc/employee/en/index.html)

# Where it comes from
The original data was created by Fusheng Wang and Carlo Zaniolo at 
Siemens Corporate Research. The data is in XML format.
http://timecenter.cs.aau.dk/software.htm

# As part of this project I ran queries to explore the data using SELECT, FROM, WHERE statments

Show the top 3 rows of the data

SELECT *
FROM employees.employees
LIMIT 3;

![Total Employees](https://github.com/kbvss/SQL-Employyee-Information/blob/main/Top%203%20rows.PNG?raw=true)

How many employee records are there?

SELECT COUNT(emp_no) as Total_Employees
FROM employees.employees;

![Total Employees](https://github.com/kbvss/SQL-Employyee-Information/blob/main/Total%20Employees.PNG?raw=true)

Which departments does this company consist of?

SELECT *
FROM Employees.departments
ORDER BY dept_no asc;

![Departments](https://github.com/kbvss/SQL-Employyee-Information/blob/main/Departments.PNG?raw=true)

What titles can employees have?
SELECT Distinct title
FROM employees.titles

![Departments](https://github.com/kbvss/SQL-Employyee-Information/blob/main/Job%20Titles.PNG?raw=true)


