# 🧠 Getting Started with SQL

## 🗂️ Introduction to Databases

### What is SQL?

**SQL** (Structured Query Language) is a declarative programming language used to query and manipulate **relational databases**. It enables data practitioners to extract, filter, and transform structured data with precision and control.

---

### What is a Database?

A **database** is a digital repository designed to store, organize, and retrieve data efficiently. It facilitates operations such as insertion, deletion, querying, and updating of records.

---

### Relational Databases

**Relational databases** organize data into tabular structures — rows represent individual records, while columns denote attributes. These tables can be interlinked via relationships, thus forming the "relational" aspect. This paradigm enables normalized data modeling and ensures integrity across large datasets.

---

### DBMS vs. RDBMS

- A **Database Management System (DBMS)** is software that handles the storage, retrieval, and modification of data.
- A **Relational Database Management System (RDBMS)** specifically supports tabular data structures and enforces relationships between entities.

> Examples include: **MySQL**, **Oracle**, **DB2 Warehouse**, and **DB2 on Cloud** — all widely deployed across sectors from banking to healthcare.

---

## ⚙️ Essential SQL Commands

SQL syntax is highly readable and designed for clarity. Though case-insensitive, it is best practice to use uppercase for SQL keywords. Most statements are terminated with a semicolon (`;`) to delimit queries.

### 🧾 Core SQL Statements

#### 🏗️ CREATE  
Define a new table or database structure.

#### ✍️ INSERT  
Populate tables with one or more rows of data.

#### 🔎 SELECT  
Retrieve data based on specific conditions.

#### 📝 UPDATE  
Modify existing records within a table.

#### ❌ DELETE  
Remove records from a table.

---

## 🔍 SELECT Statements and Filtering

### Basic Syntax:
```sql
SELECT column1, column2 FROM table_name;
````

This retrieves specific columns, and the order displayed always matches the order listed in the `SELECT` clause.

### Select All

```sql
SELECT * FROM COUNTRY;
```

Retrieves all columns from the `COUNTRY` table.

### Filtering Results

```sql
SELECT * FROM COUNTRY WHERE ID < 5;
SELECT * FROM COUNTRY WHERE CCODE = 'CA';
```

Character-based column values must be enclosed in single quotes.

**Valid Comparison Operators:**

* `=` Equal to
* `<>` Not equal to
* `>` Greater than
* `<` Less than
* `>=` Greater than or equal to
* `<=` Less than or equal to

### Combining WHERE Clauses

```sql
SELECT F_NAME, L_NAME 
FROM EMPLOYEES
WHERE (SALARY BETWEEN 60000 AND 70000) AND (DEP_ID = 5);
```

---

## 🧮 `COUNT`, `DISTINCT`, `LIMIT` Statements

### `COUNT`

```sql
SELECT COUNT(*) FROM tablename;
SELECT COUNT(COUNTRY) FROM MEDALS WHERE COUNTRY = 'Canada';
```

Returns the number of rows matching a condition.

### `DISTINCT`

```sql
SELECT DISTINCT columnname FROM tablename;
SELECT DISTINCT COUNTRY FROM MEDALS WHERE MEDALTYPE = 'GOLD';
```

Returns unique values by eliminating duplicates.

### `LIMIT`

```sql
SELECT * FROM tablename LIMIT 10;
```

Restricts the number of returned rows.

---

## ➕ `INSERT` Statements

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

Example — inserting multiple rows:

```sql
INSERT INTO Instructor(ins_id, lastname, firstname, city, country)
VALUES 
  (5, 'Doe', 'John', 'Sydney', 'AU'),
  (6, 'Doe', 'Jane', 'Dhaka', 'BD');

SELECT * FROM Instructor;
```

---

## ✏️ `UPDATE` and ❌ `DELETE` Statements

### `UPDATE`

```sql
UPDATE Instructor 
SET city = 'Dhaka', country = 'BD' 
WHERE ins_id = 4;
```

Updates values conditionally. **Always** include a `WHERE` clause to avoid unintended updates.

### `DELETE`

```sql
DELETE FROM Instructor
WHERE firstname = 'Hima';

SELECT * FROM Instructor;
```

Deletes specific rows. **Be cautious**: omitting `WHERE` will delete all rows.

---

> *“SQL is the grammar of structured inquiry — a precision tool for orchestrating logic, relationships, and insight within vast universes of data.”*
