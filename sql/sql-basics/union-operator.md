# Union Operator

The `UNION` operator is used to combine the result-set of two or more `SELECT` statements, without repeating the duplicate records by default.  Every `SELECT` statement within `UNION` must have the same number of columns or else SQL returns an error. The columns must also have similar data types. The columns in every `SELECT` statement must also be in the same order matching with their respective data types.&#x20;

```
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```

1. The `UNION` operator selects only distinct values by default. To allow duplicate values, use `UNION ALL`:

```
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```

Note: The column names in the result-set are usually equal to the column names in the first `SELECT` statement.

2. WHERE clause and ORDER BY&#x20;

```
SELECT column_name(s)
FROM table1
UNION ALL
SELECT column_name(s)
FROM table2
WHERE condition
ORDER BY column_name;
```
