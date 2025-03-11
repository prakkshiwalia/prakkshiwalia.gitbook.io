# NULL value

A field with a null value is a field no value.&#x20;

Note: A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!

1. To test for a null value, following syntax is used:

```
SELECT column_names/ *
FROM table_name
WHERE column_name IS NULL;
```

2. To test if a value is not null, the following syntax is used:

```
SELECT column_names/ *
FROM table_name
WHERE column_name IS NOT NULL;
```
