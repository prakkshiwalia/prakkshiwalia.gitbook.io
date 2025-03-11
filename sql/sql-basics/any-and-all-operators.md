# ANY & ALL Operators

The ANY and ALL operators is used to perform a comparison between a single column value and a range of other values.  Both of these operators are typically used with SELECT, WHERE and HAVING statements

### The SQL ANY Operator

The ANY operator checks if any of the values matches the condition with the subquery.&#x20;

In the below example, SQL interprets the subquery and get all the salaries from IT department(70k, 85k, 78k) and then compares the smallest value (70k) due to the operation and the ANY operator with the salary column in the main query. This returns the records matching the main query based on what is asked for in the SELECT statement by naming all the employees with its employee\_ids for whom the salary is more than 70k.&#x20;

```
SELECT column_name(s)
FROM table_name
WHERE column_name >/</>=/<=,<>,!= ANY
  (SELECT column_name
  FROM table_name
  WHERE condition);
  
Example: 
SELECT name, salary
FROM employees
WHERE salary > ANY (
    SELECT salary FROM employees WHERE department = 'IT'
```

### The SQL ALL Operator

The ALL operator checks if the value meets all the values using the condition in the subquery. &#x20;

In the below example, the subquery will get all salaries for the IT dept. which is (70k, 85k, and 78k) and will take the highest (85k) due to the operator (> and ALL used) to compare it with all the salaries and return the ones which earn more than the highest salary in the IT dept.&#x20;

```
SELECT ALL column_name(s)
FROM table_name
WHERE condition;

Example: 
SELECT name, salary
FROM employees
WHERE salary > ALL 
    (SELECT salary FROM employees WHERE department = 'IT');
```

All syntax with WHERE or HAVING&#x20;

```
SELECT column_name(s)
FROM table_name
WHERE column_name operator ALL
  (SELECT column_name
  FROM table_name
  WHERE condition);
```

**Difference between ANY and ALL**&#x20;

<table data-header-hidden><thead><tr><th width="196"></th><th></th><th></th></tr></thead><tbody><tr><td>Feature</td><td><code>ANY</code></td><td><code>ALL</code></td></tr><tr><td><strong>Condition</strong></td><td>True if <strong>at least one</strong> value satisfies the condition</td><td>True only if <strong>all values</strong> satisfy the condition</td></tr><tr><td><strong>Comparison Scope</strong></td><td>Compares to <strong>one or more</strong> values</td><td>Compares to <strong>every single</strong> value</td></tr><tr><td><strong>Example (<code>> ANY</code>)</strong></td><td>Greater than <strong>at least one</strong> value in the subquery</td><td>Greater than <strong>every</strong> value in the subquery</td></tr><tr><td><strong>Example (<code>> ALL</code>)</strong></td><td>Greater than <strong>at least one</strong> value (like <code>MIN()</code>)</td><td>Greater than <strong>all values</strong> (like <code>MAX()</code>)</td></tr></tbody></table>
