# sql-challenge
# Employee Management Database
## Overview
This database is designed to manage employee information, including titles, departments, employee details, department assignments, and salaries. It maintains the relationships between employees, their titles, departments, and salary information. Here's a brief explanation of each table in the database:

## titles Table
- This table stores information about job titles.
- Each title is identified by a unique title_id.
- The title column contains the name or description of the job title.
- The title_id column is the primary key, ensuring each title has a unique identifier.
- 
## employees Table
- This table holds information about individual employees.
- Each employee is identified by a unique emp_no.
- Employee details include their birth date, first name, last name, gender (sex), and hire date.
- The emp_title_id column is a foreign key that references the title_id in the titles table, connecting employees to their job titles.
- The emp_no column is the primary key, ensuring each employee has a unique identifier.

## departments Table
- This table contains information about different departments within an organization.
- Each department is identified by a unique dept_no.
- The dept_name column stores the name or description of the department.
- The dept_no column is the primary key, ensuring each department has a unique identifier.
  
## dept_emp Table
- This table establishes the relationships between employees and the departments they are assigned to.
-  The emp_no column is a foreign key that references the emp_no in the employees table, connecting employees to their respective departments.
- The dept_no column is a foreign key that references the dept_no in the departments table, connecting departments to their assigned employees.
- The combination of emp_no and dept_no forms the primary key, ensuring each department-employee assignment is unique.

## dept_manager Table
- This table maintains information about department managers.
- The dept_no column is a foreign key that references the dept_no in the departments table, indicating which department a manager is assigned to.
- The emp_no column is a foreign key that references the emp_no in the employees table, connecting managers to their employee records.
- The combination of dept_no and emp_no forms the primary key, ensuring each department has only one manager.

## salaries Table
- This table stores information about employee salaries.
- Each salary record is identified by a combination of emp_no and salary.
- The emp_no column is a foreign key that references the emp_no in the employees table, connecting salary information to individual employees.
- The salary column stores the employee's salary as a floating-point number.
- The combination of emp_no and salary forms the primary key, ensuring each employee's salary is unique.
