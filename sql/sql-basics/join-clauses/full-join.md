# Full Join

The `FULL OUTER JOIN` keyword returns all records when there is a match in left (table1) or right (table2) table records.

Tip: `FULL OUTER JOIN` and `FULL JOIN` are the same.

```
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name
WHERE condition;
```

**Note:** `FULL OUTER JOIN` can potentially return very large result-sets!

Full Join is used for the following reasons:

* When you need all records from both tables, even if they don't match.
* Useful in data comparison, reporting, and handling missing data.
* Can be used when merging datasets that may have gaps in information.
