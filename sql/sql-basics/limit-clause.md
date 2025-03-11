# LIMIT Clause

The `SELECT TOP clause` is used to specify the number of records to return.

The `SELECT TOP` clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

```
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number;
```

1. `ORDER BY` keyword is added when you want to sort the result, and return the first 3 records of the sorted result.

```
SELECT * 
FROM table_name
ORDER BY Column_name DESC
LIMIT 3;

```

