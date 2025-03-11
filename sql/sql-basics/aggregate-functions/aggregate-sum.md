# Aggregate - SUM

The SUM function returns the total sum of a numeric column.

```
SELECT SUM(salary)
FROM employees;
```

1. WHERE condition can be used to specify conditions

```
SELECT SUM(salary)
FROM employees;
WHERE department = 'IT';
```

2. An alias can be used with AS keyword

```
SELECT SUM(salary) AS total_salary_exp
FROM employees;
```

3. GROUP BY clause can be sued to return sum of salaries for individual departments

```
SELECT SUM(salary) AS total_salary_exp_per_dept
FROM employees
GROUP BY department;
```

4. The parameter inside the SUM function can also be used as an expression&#x20;

Example - Let's say you have to convert the salary in rupees to Sri Lakan rupee which is 1 INR = 3.51 Sri Lankan Rupee, you can create an expression in the parameter like below:

```
SELECT SUM(salary*3.51) AS total_salary_exp_per_dept
FROM employees
```
