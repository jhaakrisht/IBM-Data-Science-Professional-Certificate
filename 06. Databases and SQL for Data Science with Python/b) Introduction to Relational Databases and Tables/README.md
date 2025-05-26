# 🧮 Introduction to Relational Databases and Tables

## 🧠 Relational Database Concepts

### 🔷 The Relational Model

The **relational model** is the foundation of modern database systems. It organizes data into **tables**, offering multiple layers of abstraction:

- **Logical data independence**: You can change the logical structure without affecting how the data is accessed.
- **Physical data independence**: You can modify how data is stored without impacting the database schema.
- **Physical storage independence**: The underlying storage mechanisms are separated from the database's logical design.

---

### 🧩 The Entity-Relationship (ER) Model

The **Entity-Relationship (ER) model** is a widely-used method for designing relational databases. It visually maps the structure of a database before its physical implementation.

- **Entities** represent real-world objects or concepts (e.g., a Book) and are depicted as **rectangles**.
- **Attributes** represent characteristics of entities (e.g., title, author) and are drawn as **ovals**.

> A database can be visualized as a collection of entities, each with a set of attributes. In relational databases:
> 
> - **Entities** correspond to **tables**
> - **Attributes** correspond to **columns**
> - A **Primary Key** uniquely identifies each row in a table

Example:  
An entity `Book` with attributes like `Title`, `Author`, `ISBN` would result in a table `Book`, with the attributes as columns.

---

## 📘 Types of SQL Statements: DDL vs. DML

SQL provides two primary categories of statements:

### 📐 Data Definition Language (DDL)

DDL statements define and manage the **structure** of database objects such as tables. These include:

#### ✅ `CREATE`
Defines a new table with specified columns:
```sql
CREATE TABLE table_name (
  column1 datatype,
  column2 datatype,
  ...
);
````

#### 🔧 `ALTER`

Modifies existing tables (e.g., adding, dropping, renaming columns, or changing data types):

```sql
ALTER TABLE table_name
ADD COLUMN column_name data_type;

ALTER TABLE table_name
DROP COLUMN column_name;

ALTER TABLE table_name
ALTER COLUMN column_name SET DATA TYPE new_data_type;

ALTER TABLE table_name
RENAME COLUMN old_name TO new_name;
```

#### 🧹 `TRUNCATE`

Deletes all data in a table, but preserves the table structure:

```sql
TRUNCATE TABLE table_name IMMEDIATE;
```

#### 🗑️ `DROP`

Completely deletes the table and all its data:

```sql
DROP TABLE table_name;
```

---

### 🛠️ Data Manipulation Language (DML)

DML statements are used to manage the **data** within tables and are commonly referred to as **CRUD operations** (Create, Read, Update, Delete):

* `INSERT` – Adds data to a table
* `SELECT` – Retrieves data from a table
* `UPDATE` – Modifies existing records
* `DELETE` – Removes records from a table

Example DML statements:

```sql
-- Insert new record
INSERT INTO Books (ISBN, Title, Author) VALUES ('1234567890', 'Data Science Handbook', 'J. Doe');

-- Retrieve records
SELECT * FROM Books WHERE Author = 'J. Doe';

-- Update data
UPDATE Books SET Title = 'Advanced Data Science' WHERE ISBN = '1234567890';

-- Delete data
DELETE FROM Books WHERE ISBN = '1234567890';
```

---

## 🧠 Practical Tips for Querying Relational Databases

### 🆔 Column Names with Spaces or Special Characters

* Spaces are converted to underscores:
  `"Name of Dog"` → `Name_of_Dog`
* Special characters (e.g., brackets) are also replaced with underscores:
  `"Breed (dominant breed if not pure breed)"` → `Breed__dominant_breed_if_not_pure_breed_`

> ✅ Use **underscores** (`_`) to replace spaces and special characters in SQL column names.

---

### 🔡 Querying Mixed Case Columns

Column names that are **case-sensitive** must be enclosed in **double quotes**:

```sql
SELECT "Id" FROM DOGS;
```

> 🔍 Querying with `"ID"` (uppercase) will return no result if the actual column is named `"Id"` (mixed-case).

---

### 🔄 Writing Multi-line SQL Queries in Notebooks

To split queries across multiple lines in Jupyter Notebooks or similar environments:

```sql
%sql SELECT "Id", "Name_of_Dog", \
FROM dogs \
WHERE "Name_of_Dog" = 'Huggy'
```

Alternatively, using `%%sql` allows multi-line queries without needing backslashes:

```sql
%%sql
SELECT "Id", "Name_of_Dog"
FROM dogs
WHERE "Name_of_Dog" = 'Huggy';
```

---

> *“A well-structured relational database is like a well-architected city — organized, efficient, and built to grow with purpose.”*
