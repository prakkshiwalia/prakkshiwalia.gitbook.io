# IN and BETWEEN Operator

### IN Operator

The IN operator allows you to specify multiple values in a WHERE clause, Often used as a shortand for multiple OR conditions

```
SELECT *
FROM employees
WHERE department IN ('IT', 'HR')
-- Shorthand version of WHERE department = 'IT' OR department = 'HR'
```

1. Same can be done for the opposite by using the 'NOT IN', NOT keyword in front of the IN operator.
2. IN can also be used with SELECT as a subquery in the WHERE clause. The main query would present all the records from the subquery

```
SELECT *
FROM salaries
WHERE employee_id IN (SELECT employee_id FROM bonus > 3500)
```

3. NOT IN operator used with SELECT can be used with subqueries as well to return the records for the same above example to give employee\_ids of all the employees with bonus less than 3500.&#x20;

### BETWEEN Operator&#x20;

The BETWEEN operator selects values within a given range which can be numbers, text, or dates. It includes the begin and end values.

```
SELECT *
FROM salaries
WHERE bonus BETWEEN 3000 AND 7000;
```

1. NOT BETWEEN can be used to provide the records outside the range provided.
2. BETWEEN is used to provide range while IN can be used in the same code to filter it out from a few columns like below:

```
SELECT *
FROM salaries 
WHERE bonus BETWEEN 2500 AND 9000
AND employee_id IN (103-109);
```

3. BETWEEN Text values can be used to provide records between two text values and same can be done using the NOT BETWEEN to get all the records except for the values in the text values.&#x20;

```
SELECT *
FROM employees
WHERE name BETWEEN 'DAVID' AND 'HANNAH'
ORDER BY name
```

4. BETWEEN can be used to get values between certain dates in the format 'YYYY-MM-DD'

```
SELECT *
FROM salaries
WHERE salary_date BETWEEN '2024-01-01' AND '2024-01-16';
```
