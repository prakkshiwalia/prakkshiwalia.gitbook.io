# UPDATE & DELETE statement

This statement is used to modify existing records in a statement. It is used to update one or more columns for selected rows that match a specified condition.

**Note:** Be careful when updating records in a table! The `WHERE` clause specifies which records that should be updated otherwise all the records in the table will be updated!

In the syntax below, the table\_name is used to inform which table has to be updated, SET specifies the column and their new value and WHERE determines which rows should be updated like below :

```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

### DELETE STATEMENT

A delete statement is used to delete records (rows) from an existing table.

**Note:** Be careful when deleting records in a table! The `WHERE` clause specifies which records should be deleted otherwise all records in the table will be deleted!

Syntax:

```
DELETE 
FROM table_name 
WHERE condition;
```

1. You can delete the records from the table without deleting the table using syntax:

```
DELETE 
FROM table_name
```

2. To delete the table completely using the DROP BY, the following syntax is used:

```
DROP BY table_name;
```
