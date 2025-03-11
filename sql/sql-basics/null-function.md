# NULL Function

&#x20;The IS NULL function (called in MySQL) is used to provide an alternative values in the result if the value is null to provide meaningful results. Similarly, if the expression is not NULL, it returns the original value.&#x20;

In the below example - Since Emma's bonus is null, when the expression (salary + bonus) is calculated will provide the null value. However, since the salary of an employee cannot be null, it is useful to add a replacement\_value which is the salary itself.&#x20;

Note: The ISNULL still calcuates the salary the same even if it is not null for the entire expression and gives the final value.&#x20;

If both salary and bonus exist, the query adds them normally.\
If `bonus` is NULL, ISNULL ensures salary is returned instead of NULL.\
If salary itself is NULL, the result remains NULL.

```
SELECT *
       ISNULL(expression, replacement_value) AS ALIAS
FROM table

Example:
SELECT name, salary, 
       ISNULL(salary + bonus, salary) AS total_compensation
FROM salaries;
```
