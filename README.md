---
description: Introduction
---

# SQL

Why will SQL be important for a career in Product Management?

A complaint from a user that looks like it could be a general issue? Let's analyze. A stakeholder says fixing something is vital? Let's see if the problem is really that big. We have an intuition about a major problem? Let’s make sure with data. Curious about what our super users have in common? Let’s dig in.

This data can be accessed through Tableau and Power BI in visual formats and SQL provides freedom of creativity and speed for such activities.&#x20;

The process is usually like this:

1. **Extract the Data**
   * I have access to a production database replica where I can run queries.
   * I pull all the related raw data I think I’ll need.
   * I throw it into Google Sheets or Excel.
2. **Look for Patterns**
   * I start grouping the data by different parameters (but not all at once).
   * When I find a grouping that seems useful, I make a quick chart to spot weird details.
   * If the chart isn’t helpful, I tweak it or try a different grouping.
3. **Dig Deeper**
   * Eventually, something strange or interesting shows up.
   * That raises new questions, so I go back to step 1 and refine the data search.

Knowing SQL is a great skill—it gives me freedom to explore in-depth and lets me get answers fast.

## **Database Basics**

### **1. What is a Database?**

* A database may be defined as a collection of interrelated data stored together to serve multiple applications and is utilised in the decision-making processes in the companies. Furthermore, a common and controlled approach is used in adding new data and in modifying and retrieving existing data within the database.

### **2. What is a DBMS?**

* A DBMS refers to a software that is responsible for storing, maintaining and utilizing databases. A database along with a DBMS is referred to as database system. Different departments use the data and make their different end user view from this data which is derived from the common overall data structure.
* **Database System** = DBMS + Database.

### **3. What is the Relational Database Model?**

* In relational database model, the data is organised into tables (i.e., rows and columns). These tables are called relations. A row in a table represents a relationship among a set of values. Since a table is a collection of relationships, it is generally referred to the mathematical term relation, from which relational data model derives its name.
* Uses **SQL** for queries, insertions, updates, and deletions.

### **4. Components of a Table**

* **Byte** – A group of 8 bits, used to store a character.
* **Data Item (Field)** – Smallest unit of named data (column).
* **Record** – A complete set of related data items (row).
* **Table** – A collection of records (entire dataset).
* **Tuples** – Rows in a table.
* **Attributes** – Columns in a table.

### **5. Tuples and attributes in a table**

**Example:**

`In the below employees` table:

| employee\_id | name    | age | department |
| ------------ | ------- | --- | ---------- |
| 101          | Alice   | 30  | HR         |
| 102          | Bob     | 28  | IT         |
| 103          | Charlie | 35  | Finance    |

* **Tuple** represents a **single row** in a database table/ the values of the variables. One tuple is one entire row which has different variable values. Each tuple is a **unique entry** in the table.
* The row **(101, Alice, 30, HR)** is a **tuple**.
* The table consists of **three tuples**.

whereas,

* An **attribute** is the name of the **column/ variable names** in a database table.&#x20;
*   In the same `employees` table, the attributes (columns) are:

    `employee_id, name, age, department`

    Each attribute holds values for all tuples in that column.

**Key Differences Between Tuples and Attributes**

| Feature         | Tuple (Row)                 | Attribute (Column)                  |
| --------------- | --------------------------- | ----------------------------------- |
| **Definition**  | A single record in a table  | A property/field of the table       |
| **Represents**  | A specific data entry       | A characteristic of the entity      |
| **Example**     | (101, Alice, 30, HR)        | employee\_id, name, age, department |
| **Total Count** | Number of rows in the table | Number of columns in the table      |

### **6. Key Relational Database Operations**

* Querying tables.
* Inserting, updating, and deleting rows.
* Using **relational query languages** (SQL, relational algebra).

### **7. Popular Open-Source RDBMS**

* **MySQL, PostgreSQL, SQLite**

### **8. Importance of SQL**

* SQL enables querying, updating, and manipulating large datasets.
* Python can be used to connect to databases and execute SQL queries efficiently.

### **9. Relational Databases & RDBMS**

* **Database**: A repository of data.
* **DBMS**: Software that manages the database.
* **RDBMS**: DBMS for relational databases (e.g., MySQL, PostgreSQL).
* Used across industries like banking, healthcare, and transportation.

