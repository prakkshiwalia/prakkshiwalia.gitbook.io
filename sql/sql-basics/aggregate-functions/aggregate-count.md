# Aggregate - COUNT

The `COUNT()` function returns the number of rows that matches a specified criteria, including the NULL values&#x20;

Note - If you specify a column name instead of `(*)`, NULL values will not be counted.

```
SELECT COUNT(column_name)/ COUNT(*)
FROM table_name;
```

!!! Database used in the below examples is&#x20;

{% content-ref url="../../databases-used/aggregate.md" %}
[aggregate.md](../../databases-used/aggregate.md)
{% endcontent-ref %}

1. Add a WHERE clause to add a condition before counting/ aggregation&#x20;

```
SELECT COUNT(column_name)
FROM table_name 
WHERE condition 1;

SELECT COUNT(name)
FROM employees
WHERE salary > 65000;
```

2. To ignore the duplicate values, use the DISTINCT keyword in the COUNT function

In the Example below, it is used to count the different values of salaries, avoiding the one that are repeated.

```
SELECT COUNT(DISTINCT column_name)
FROM table_name;

SELECT COUNT(DISTINCT salary)
FROM employees;
```

3. Use an alias using the keyword AS to make the records simpler by counting all the rows, including the NULL values &#x20;

```
SELECT COUNT(*) AS [Number of records]
FROM employees;

-- However, if you put the column_name instead of *, the
-- null values of that particular variable will not be 
-- calculated. 
```

4. Using COUNT BY with GROUP BY&#x20;

In the Example below, the query counts the number of employees in each department. It groups the employees by `department` and applies `COUNT(*)` to each group separately.

```
SELECT COUNT(*) AS [Number of records], department
FROM employees
GROUP BY department;
```
