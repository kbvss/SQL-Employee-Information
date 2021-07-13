# SQL Employyee Information Database 
This repository holds the code and queries for this project

# As part of this project I ran queries to explore the data using SELECT, FROM, WHERE and JOIN statements

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

Showing a list of mployees hired before the year 2000

	SELECT emp_no, first_name, last_name, hire_date
	FROM employees.employees
	WHERE hire_date >= 12-31-1999


![Departments](https://github.com/kbvss/SQL-Employyee-Information/blob/main/Hired%20before%202000.PNG?raw=true)


Showing the department manager names

	SELECT dm.emp_no, 
		   dm.dept_no, 
	       employees.departments.dept_name, 
	       /*employees.employees.emp_no,*/
		   employees.employees.first_name,
	       employees.employees.last_name
	   FROM employees.dept_manager dm
	   JOIN employees.departments ON dm.dept_no = employees.departments.dept_no
	   JOIN employees.employees ON dm.emp_no = employees.employees.emp_no;

![Daprtment Manager Names](https://github.com/kbvss/SQL-Employyee-Information/blob/main/Join%201%20for%20manager.PNG?raw=true)


















