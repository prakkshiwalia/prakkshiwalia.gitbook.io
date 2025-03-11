# SELECT Statement

A SELECT statement is used to select data from a database

1. The basic syntax below is where the column1, column2 are the field names of the table you want to select data from and the table\_name represents the name of the table you want to select data from.

```
SELECT column1, column2, ...
FROM table_name;
```

2. If you want to return all columns without specifying every column name, you can use the SELECT \* syntax

```
SELECT * FROM table_name;
```

3. The SQL DISTINCT statement is used to return only the distinct (different) values

```
SELECT DISTINCT column1, column2,...
FROM table_name;
```

4. By using the DISTINCT keyword in a function called count, we can return all the unique values&#x20;

```
SELECT COUNT(DISTINCT column1) FROM table_name;
```

