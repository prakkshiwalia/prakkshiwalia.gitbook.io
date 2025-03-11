# INSERT INTO Statement

INSERT INTO statement is used to insert new records into statements.

There are 2 ways to use INSERT INTO statement as follows:

1. i) Specify both the column names and the values to be inserted:

```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

ii) If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the `INSERT INTO` syntax would be as follows:

```
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

2. It is possible to only insert in specific columns using code in i)
3. Multiple values of rows could be added using the insert into statement&#x20;

```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1.1, value1.2, value1.3, ...),
(value2.1, value2.2, value2.3, ...),
(value3.1, value3.2, value3.3, ...),
```
