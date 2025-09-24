# SQL Aggregate Functions

Aggregate functions in SQL are used to perform calculations on multiple rows of a table’s column and return a single value. These functions are commonly used with the `GROUP BY` clause but can also be used without it.

---

## COUNT()
Returns the number of rows that match a specified condition.

```sql
-- Count total employees
SELECT COUNT(*) AS TotalEmployees
FROM Employees;

-- Count employees in the 'IT' department
SELECT COUNT(*) AS IT_Employees
FROM Employees
WHERE Department = 'IT';


##SUM()

Returns the total sum of a numeric column.

-- Sum of all salaries
SELECT SUM(Salary) AS TotalSalary
FROM Employees;

-- Sum of salaries in 'Sales' department
SELECT SUM(Salary) AS SalesTotalSalary
FROM Employees
WHERE Department = 'Sales';

##AVG()

Returns the average value of a numeric column.

-- Average salary of all employees
SELECT AVG(Salary) AS AvgSalary
FROM Employees;

-- Average salary in 'HR' department
SELECT AVG(Salary) AS HR_AvgSalary
FROM Employees
WHERE Department = 'HR';

##MIN()

Returns the minimum value in a column.

-- Minimum salary of all employees
SELECT MIN(Salary) AS MinSalary
FROM Employees;

-- Earliest hire date
SELECT MIN(Hire_Date) AS EarliestHire
FROM Employees;

##MAX()

Returns the maximum value in a column.

-- Maximum salary of all employees
SELECT MAX(Salary) AS MaxSalary
FROM Employees;

-- Latest hire date
SELECT MAX(Hire_Date) AS LatestHire
FROM Employees;

##GROUP BY Example

Aggregate functions are often used with GROUP BY to calculate values per group.

-- Total salary per department
SELECT Department, SUM(Salary) AS TotalSalary
FROM Employees
GROUP BY Department;

-- Average salary per department
SELECT Department, AVG(Salary) AS AvgSalary
FROM Employees
GROUP BY Department;
