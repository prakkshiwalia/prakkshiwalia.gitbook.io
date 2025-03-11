# SQL Basics

* A record, also known as a row, represents each individual entry in a table. A record is a horizontal entity in a table.
* SQL keywords are not case-sensitive: `select` is the same as `SELECT`.
* A column is a vertical entity in a table that contains all information associated with a specific field.
* Most of the actions you need to perform on a database are done with SQL statements.
* SQL statements consist of keywords that are easy to understand.
*   Some database systems require a semicolon at the end of each SQL statement.

    Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.
* How to put comments in SQL?

```
-- Any text between -- and the end of the line will be ignored (will not be executed

/*Multi-line comments start with /* and end with */.

Any text between /* and */ will be ignored. It is also used to just ignore a part of the statement */
```

| **Category**   | **Type**                               | **Examples**                                                      | **Purpose**                                  |
| -------------- | -------------------------------------- | ----------------------------------------------------------------- | -------------------------------------------- |
| **Operators**  | **Arithmetic Operators**               | `+`, `-`, `*`, `/`, `%`                                           | Perform mathematical calculations.           |
|                | **Comparison Operators**               | `=`, `!=`, `<`, `>`, `<=`, `>=`                                   | Compare values in queries.                   |
|                | **Logical Operators**                  | `AND`, `OR`, `NOT`                                                | Combine multiple conditions in `WHERE`.      |
|                | **Bitwise Operators**                  | `&`, \`                                                           | `,` ^`,` \~`,` <<`,` >>\`                    |
|                | **String Operators**                   | \`                                                                |                                              |
|                | **LIKE & Wildcards**                   | `LIKE`, `%`, `_`                                                  | Pattern matching in text searches.           |
| **Statements** | **Data Query Language (DQL)**          | `SELECT`                                                          | Retrieve data from tables.                   |
|                | **Data Manipulation Language (DML)**   | `INSERT`, `UPDATE`, `DELETE`                                      | Modify records in tables.                    |
|                | **Data Definition Language (DDL)**     | `CREATE`, `ALTER`, `DROP`, `TRUNCATE`                             | Define and modify database structures.       |
|                | **Data Control Language (DCL)**        | `GRANT`, `REVOKE`                                                 | Manage permissions in the database.          |
|                | **Transaction Control Language (TCL)** | `COMMIT`, `ROLLBACK`, `SAVEPOINT`                                 | Control transactions (ensuring consistency). |
| **Clauses**    | **Filtering Clauses**                  | `WHERE`, `HAVING`                                                 | Filter records based on conditions.          |
|                | **Sorting & Limiting**                 | `ORDER BY`, `LIMIT`, `TOP`                                        | Sort or limit the number of records.         |
|                | **Grouping**                           | `GROUP BY`                                                        | Aggregate data into groups.                  |
|                | **Join Clauses**                       | `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL JOIN`, `SELF JOIN` | Combine data from multiple tables.           |
|                | **Subquery Clauses**                   | `EXISTS`, `IN`, `ANY`, `ALL`                                      | Use queries within queries.                  |
|                | **Set Operators**                      | `UNION`, `UNION ALL`, `INTERSECT`, `EXCEPT`                       | Combine results from multiple queries.       |

#### **Key Takeaways**

**Operators** → Help perform calculations, comparisons, and logic in queries.\
**Statements** → Define **what action** is performed (`SELECT`, `INSERT`, etc.).\
**Clauses** → Modify the behavior of SQL statements (`WHERE`, `ORDER BY`, `GROUP BY`).
