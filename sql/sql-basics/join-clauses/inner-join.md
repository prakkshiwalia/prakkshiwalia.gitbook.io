# Inner Join

The `INNER JOIN` keyword presents records that have matching values in both tables.

```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

**Key Points to Remember**&#x20;

* Returns only matching records from both tables.
* Excludes rows that do not have a match.
* Used to retrieve related data from multiple tables.
* &#x20;Requires a **common column** for joining.
* Naming the columns - It is a good practice to name the columns in SQL statement to make it look cleaner and easier to understand.

**Syntax for joining three tables is as below:**

The below example joins departments by matching employees to their departments using `employee_id. The joins salaries` by matching employees to their salaries using `employee_id`. The `SELECT` statement retrieves employee details, department names, and salaries.

```
SELECT 
    table1.column1, 
    table2.column2, 
    table3.column3
FROM table1
JOIN table2 ON table1.common_column = table2.common_column
JOIN table3 ON table2.common_column = table3.common_column;

Example from the database:
SELECT 
    e.employee_id, 
    e.name, 
    d.department_name, 
    s.salary
FROM employees e
JOIN departments d ON e.employee_id = d.employee_id
JOIN salaries s ON e.employee_id = s.employee_id;
```

Employee, Department & Salary Data

| employee\_id | name    | department\_id | department\_name | salary |
| ------------ | ------- | -------------- | ---------------- | ------ |
| 1            | Alice   | 101            | HR               | 50000  |
| 2            | Bob     | 102            | IT               | 60000  |
| 3            | Charlie | 103            | Finance          | 55000  |
| 4            | David   |                |                  | 70000  |

