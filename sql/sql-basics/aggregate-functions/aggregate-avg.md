# Aggregate - AVG

The AVG function is use to return the average value of a numeric column, null values are ignored&#x20;

```
SELECT AVG(column_1) AS [Average salary]
FROM table_name
WHERE condition;

SELECT AVG(salary)
FROM employees
WHERE department = 'IT';
```

1. To list all the salaries higher than the average salary, we can use the AVG function in a subquery

```
SELECT * 
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees AS [Average Salary])

```

2. Similarly, the GROUP BY function is used to return the avergae salary for each department in the employees table.

```
SELECT AVG(salary) AS [Average Salary], Department 
FROM employees 
GROUP BY department;
```
