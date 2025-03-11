# INSERT INTO SELECT statement

INSERT INTO SELECT statement copies data from one table and inserts it into another&#x20;

```
INSERT INTO table2
SELECT * FROM table1
WHERE condition;

-- To copy a few statements from the old table, the following syntax is used:
INSERT INTO table2 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table1
WHERE condition;
```

When to use join and when to use Insert into select statement -

| Feature            | `JOIN`                                               | `INSERT INTO SELECT`                        |
| ------------------ | ---------------------------------------------------- | ------------------------------------------- |
| **Purpose**        | Combine & display data from multiple tables          | Copy/move data from one table to another    |
| **Modifies Data?** | No                                                   | Yes                                         |
| **Use Case**       | Viewing related data (e.g., Employees & Departments) | Creating backups or inserting filtered data |

