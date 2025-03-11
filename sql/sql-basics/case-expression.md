# Case Expression

The CASE expression goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause. If there is no ELSE part and no conditions are true, it returns NULL. In the following example, the END keyword marks the completion of the CASE statement.

Case Expression makes raw data more readable (instead of just numbers). Groups data into meaningful categories without needing extra tables. Helps in reporting & filtering, like fetching only high salary employees for presentation.&#x20;

**When is it Used?**

* To categorize data (e.g., classifying salaries as High, Medium, Low).
* &#x20;To replace values dynamically in a SELECT statement.
* To apply conditional logic within queries.
* To avoid complex IF statements in SQL.

In the following example, the AS salary\_category part renames the result of the CASE statement into a new column called salary\_category adding a new column to the output categorizing salaries into low salary, medium salary and high salary based on the conditions.

```
SELECT column_name,
       CASE 
           WHEN condition1 THEN result1
           WHEN condition2 THEN result2
           ELSE default_result
       END AS new_column
FROM table_name;

Example:
SELECT name, salary,
       CASE 
           WHEN salary < 60000 THEN 'Low Salary'
           WHEN salary BETWEEN 60000 AND 80000 THEN 'Medium Salary'
           WHEN salary > 80000 THEN 'High Salary'
           ELSE 'Unknown'
       END AS salary_category
FROM employees;
```
