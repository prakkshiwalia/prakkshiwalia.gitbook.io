# AGGREGATE - MIN & MAX

The most commonly used SQL aggregate functions are:

* `MIN()` - returns the smallest value within the selected column
* `MAX()` - returns the largest value within the selected column

!!! Database used for following examples is provided on the link below:

{% content-ref url="../../databases-used/aggregate.md" %}
[aggregate.md](../../databases-used/aggregate.md)
{% endcontent-ref %}

1. Where clause usage  in aggregate functions

The `WHERE` clause is used to filter **individual rows** based on a specified condition **before** selection. It applies **row-level filtering** before any grouping or aggregation functions (`MIN`, `MAX`, `SUM`, `COUNT`, etc.) are executed.

**Example 1**: The IT department is part of department category (variable name/ attribute) from which the filtering happens to get the highest salary only from all the employees in the IT dept.

```
SELECT MIN(Column_name)
FROM table_name;
WHERE condition

SELECT MAX(Column_name)
FROM table_name;
WHERE condition

Example 1:
SELECT MIN(salary) AS lowest_salary
SELECT MAX(salary) AS highest_salary
FROM employees
WHERE department = 'IT';
```

2. `GROUP BY Clause in aggregate functions`&#x20;

The `GROUP BY` clause is used to **group rows** that have the same    values in one or more columns. It **converts multiple rows into a single summary row per group**.

In the example below, Groups employees by department and finds the highest salary in each. Without the GROUP`BY`, `MAX(salary)` would return the overall max salary.

```
SELECT department, MAX(salary) AS highest_salary
FROM employees
GROUP BY department;
```

#### 3. HAVING Clause&#x20;

The `HAVING` clause is used to filter **groups** of data **after aggregation**. It works similarly to `WHERE`, but while `WHERE` filters **individual rows before aggregation**, `HAVING` filters **aggregated results after `GROUP BY` is applied**.

In the Example below, GROUP `BY` groups employees by department, then `MAX(salary)` finds the highest salary per department, and `HAVING` filters out groups where the max salary is ≤ 80,000.

```
SELECT department, MAX(salary) AS highest_salary
FROM employees
GROUP BY department
HAVING MAX(salary) > 80000;
```

#### 4. Difference between WHERE, GROUP BY and HAVING clause:

<table><thead><tr><th>Clause</th><th>Purpose</th><th width="40">Aggregate Functions Allowed?</th><th>Execution Order</th><th>Example Use Case</th></tr></thead><tbody><tr><td><code>WHERE</code></td><td>Filters individual rows before aggregation</td><td>❌ No</td><td>Before <code>GROUP BY</code></td><td>Find employees with salary > 50,000</td></tr><tr><td><code>GROUP BY</code></td><td>Groups rows and applies aggregate functions</td><td>✅ Yes</td><td>After <code>WHERE</code>, before <code>HAVING</code></td><td>Find the highest salary per department</td></tr><tr><td><code>HAVING</code></td><td>Filters aggregated results after <code>GROUP BY</code></td><td>✅ Yes</td><td>After <code>GROUP BY</code></td><td>Find departments where max salary > 80,000</td></tr></tbody></table>

5. `Using GROUP BY and WHERE clause together`&#x20;

`In the Example below: First`, `WHERE` filters out employees with a salary ≤ 50,000. Then, `GROUP BY` finds the max salary per department.

```
SELECT department, MAX(salary) AS highest_salary
FROM employees
WHERE salary > 50000
GROUP BY department;



```

* `COUNT()` - returns the number of rows in a set
* `SUM()` - returns the total sum of a numerical column
* `AVG()` - returns the average value of a numerical column

Aggregate functions ignore null values (except for `COUNT()`).
