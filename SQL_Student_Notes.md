# SQL — Student Notes

## 1. What is SQL?

**SQL = Structured Query Language**

SQL is a language used to communicate with and manage relational databases.

> If a database is a place where data is stored, SQL is the language we use to ask the database to store, find, change, or delete data.

Example:

```sql
SELECT * FROM students;
```

Meaning: Show all records from the `students` table.

---

## 2. Database vs DBMS vs SQL

### Database
An organized collection of data.

### DBMS
**Database Management System** — software used to create, store, manage, and access databases.

Examples:
- MySQL
- PostgreSQL
- Oracle Database
- Microsoft SQL Server
- SQLite

### Important distinction

```text
SQL   → Language
MySQL → DBMS
```

---

## 3. Relational Database

A relational database stores data in tables.

### Example: students

| id | name | email | course |
|---:|---|---|---|
| 1 | Rahul | rahul@gmail.com | AWS |
| 2 | Priya | priya@gmail.com | Cyber Security |
| 3 | Amit | amit@gmail.com | DevOps |

```text
Database
   ↓
Tables
   ↓
Rows + Columns
```

- **Row:** One complete record.
- **Column:** One attribute/type of information.

---

## 4. SQL Command Categories

```text
SQL
│
├── DDL
├── DML
├── DQL
├── DCL
└── TCL
```

### DDL — Data Definition Language

Used to define/change database structure.

```text
CREATE
ALTER
DROP
TRUNCATE
```

### DML — Data Manipulation Language

Used to modify data.

```text
INSERT
UPDATE
DELETE
```

### DQL — Data Query Language

Used to retrieve data.

```text
SELECT
```

### DCL — Data Control Language

Used for permissions/access.

```text
GRANT
REVOKE
```

### TCL — Transaction Control Language

Used for transactions.

```text
COMMIT
ROLLBACK
SAVEPOINT
```

---

# 5. Create Database

```sql
CREATE DATABASE studentdb;
```

Check databases:

```sql
SHOW DATABASES;
```

Select database:

```sql
USE studentdb;
```

> `USE` tells MySQL which database we want to work with.

---

# 6. Create Table

```sql
CREATE TABLE students (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(150),
    phone VARCHAR(20),
    course VARCHAR(100)
);
```

Important concepts:

```text
id              → Student identifier
INT             → Integer
VARCHAR(100)    → Text up to 100 characters
PRIMARY KEY     → Uniquely identifies a record
AUTO_INCREMENT  → Automatically generates the next ID
```

---

# 7. Check Tables

```sql
SHOW TABLES;
```

Table structure:

```sql
DESCRIBE students;
```

or:

```sql
DESC students;
```

---

# 8. INSERT — Add Data

```sql
INSERT INTO students
(name, email, phone, course)
VALUES
('Rahul', 'rahul@gmail.com', '9876543210', 'AWS');
```

Another record:

```sql
INSERT INTO students
(name, email, phone, course)
VALUES
('Priya', 'priya@gmail.com', '9876543211', 'Cyber Security');
```

Check data:

```sql
SELECT * FROM students;
```

---

# 9. SELECT — Read Data

All columns:

```sql
SELECT * FROM students;
```

Specific columns:

```sql
SELECT name, email
FROM students;
```

> `*` means all columns.

---

# 10. WHERE — Filter Data

```sql
SELECT *
FROM students
WHERE course = 'AWS';
```

Another example:

```sql
SELECT *
FROM students
WHERE id = 1;
```

> `WHERE` tells the database which records we are interested in.

---

# 11. UPDATE — Modify Data

```sql
UPDATE students
SET course = 'DevOps'
WHERE id = 1;
```

Verify:

```sql
SELECT * FROM students;
```

### Important warning

Avoid:

```sql
UPDATE students
SET course = 'DevOps';
```

without a `WHERE` condition because it can update every row.

> **Always verify your WHERE condition before UPDATE or DELETE.**

---

# 12. DELETE — Remove Data

```sql
DELETE FROM students
WHERE id = 2;
```

Verify:

```sql
SELECT * FROM students;
```

Be careful with:

```sql
DELETE FROM students;
```

It can delete all records.

---

# 13. ORDER BY

Ascending:

```sql
SELECT *
FROM students
ORDER BY name ASC;
```

Descending:

```sql
SELECT *
FROM students
ORDER BY name DESC;
```

---

# 14. LIMIT

```sql
SELECT *
FROM students
LIMIT 2;
```

Useful when working with large datasets.

---

# 15. LIKE

Search using patterns:

```sql
SELECT *
FROM students
WHERE name LIKE 'R%';
```

Meaning: names beginning with R.

Patterns:

```text
R%      → starts with R
%a      → ends with a
%ha%    → contains "ha"
```

---

# 16. AND / OR

### AND

Both conditions must be true:

```sql
SELECT *
FROM students
WHERE course = 'AWS'
AND name = 'Rahul';
```

### OR

Either condition can be true:

```sql
SELECT *
FROM students
WHERE course = 'AWS'
OR course = 'DevOps';
```

---

# 17. NULL

`NULL` means no value / unknown value.

Do not use:

```sql
WHERE phone = NULL;
```

Use:

```sql
SELECT *
FROM students
WHERE phone IS NULL;
```

Or:

```sql
WHERE phone IS NOT NULL;
```

---

# 18. Primary Key

A **Primary Key** uniquely identifies each record.

Example:

```text
1 → Rahul
2 → Priya
3 → Amit
```

Analogy:

> A primary key is like a unique roll number.

---

# 19. Foreign Key

A foreign key creates a relationship between tables.

### students

```text
id
name
course_id
```

### courses

```text
id
course_name
```

Relationship:

```text
students.course_id
        ↓
courses.id
```

---

# 20. SQL JOIN

Example tables:

### students

| id | name | course_id |
|---:|---|---:|
| 1 | Rahul | 101 |
| 2 | Priya | 102 |

### courses

| id | course_name |
|---:|---|
| 101 | AWS |
| 102 | Cyber Security |

Query:

```sql
SELECT students.name, courses.course_name
FROM students
JOIN courses
ON students.course_id = courses.id;
```

Result:

| name | course_name |
|---|---|
| Rahul | AWS |
| Priya | Cyber Security |

> **JOIN allows us to retrieve related information from multiple tables.**

---

# 21. Aggregate Functions

## COUNT

```sql
SELECT COUNT(*)
FROM students;
```

## MAX

```sql
SELECT MAX(id)
FROM students;
```

## MIN

```sql
SELECT MIN(id)
FROM students;
```

## AVG

For a numerical column:

```sql
SELECT AVG(marks)
FROM students;
```

## SUM

```sql
SELECT SUM(marks)
FROM students;
```

---

# 22. GROUP BY

```sql
SELECT course, COUNT(*)
FROM students
GROUP BY course;
```

Possible result:

```text
AWS             10
DevOps           7
Cyber Security   8
```

> `GROUP BY` groups similar records so we can perform calculations on each group.

---

# 23. HAVING

`HAVING` filters groups.

```sql
SELECT course, COUNT(*)
FROM students
GROUP BY course
HAVING COUNT(*) > 5;
```

Simple distinction:

```text
WHERE
 ↓
filters rows

HAVING
 ↓
filters groups
```

---

# 24. SQL + AWS 3-Tier Project

Your Student Registration application uses:

```text
Browser
   ↓
Nginx / Web Tier
   ↓
PHP / Application Tier
   ↓
MySQL / Database Tier
```

When a student submits:

```text
Name: Rahul
Email: rahul@gmail.com
Course: AWS
```

PHP can execute:

```sql
INSERT INTO students
(name, email, course)
VALUES
('Rahul', 'rahul@gmail.com', 'AWS');
```

Display students:

```sql
SELECT * FROM students;
```

Update:

```sql
UPDATE students
SET course = 'DevOps'
WHERE id = 1;
```

Delete:

```sql
DELETE FROM students
WHERE id = 1;
```

Application flow:

```text
Frontend
   ↓
PHP
   ↓
SQL
   ↓
MySQL
   ↓
Student Data
```

---

# 25. SQL Injection — Cybersecurity Connection

SQL Injection happens when untrusted user input is incorrectly incorporated into SQL queries.

### Unsafe example

```php
$sql = "SELECT * FROM students WHERE email = '$email'";
```

The problem is that user input is directly inserted into the SQL statement.

### Safer approach: Prepared Statements

Example with PDO:

```php
$stmt = $pdo->prepare(
    "SELECT * FROM students WHERE email = :email"
);

$stmt->execute([
    'email' => $email
]);
```

### Teaching point

> **Never trust user input. Use prepared statements when application code interacts with SQL.**

---

# 26. Student SQL Practical

## Task 1 — Create Database

```sql
CREATE DATABASE companydb;
USE companydb;
```

## Task 2 — Create Employees Table

Create an `employees` table with:

```text
id
name
email
department
salary
```

## Task 3 — Insert Data

Insert at least **5 employees**.

## Task 4 — Display All Employees

```sql
SELECT * FROM employees;
```

## Task 5 — Filter IT Employees

```sql
SELECT *
FROM employees
WHERE department = 'IT';
```

## Task 6 — Update Salary

Update one employee's salary.

## Task 7 — Delete Employee

Delete one employee using their ID.

## Task 8 — Sort by Salary

```sql
SELECT *
FROM employees
ORDER BY salary DESC;
```

## Task 9 — Count Employees

```sql
SELECT COUNT(*)
FROM employees;
```

## Task 10 — Search Names

Find employees whose names start with `A`:

```sql
SELECT *
FROM employees
WHERE name LIKE 'A%';
```

---

# 27. Quick Revision Sheet

| Command | Purpose |
|---|---|
| `CREATE DATABASE` | Create database |
| `USE` | Select database |
| `CREATE TABLE` | Create table |
| `INSERT` | Add data |
| `SELECT` | Read data |
| `WHERE` | Filter data |
| `UPDATE` | Modify data |
| `DELETE` | Remove data |
| `ORDER BY` | Sort |
| `GROUP BY` | Group |
| `JOIN` | Combine related tables |
| `COUNT` | Count records |
| `LIKE` | Pattern search |
| `ALTER` | Modify structure |
| `DROP` | Remove database/table |
| `TRUNCATE` | Remove all rows |

---

# 28. Core SQL Flow

Students should remember:

```text
CREATE
  ↓
INSERT
  ↓
SELECT
  ↓
UPDATE
  ↓
DELETE
```

For the AWS project:

```text
HTML/CSS/JS
     ↓
   Nginx
     ↓
    PHP
     ↓
    SQL
     ↓
   MySQL
     ↓
Student Data
```

---

# 29. Trainer Teaching Strategy

For the first SQL session, focus on:

1. Database vs DBMS vs SQL
2. Tables, rows, columns
3. DDL/DML/DQL basics
4. CREATE DATABASE
5. CREATE TABLE
6. INSERT
7. SELECT
8. WHERE
9. UPDATE
10. DELETE
11. Primary Key
12. Basic JOIN
13. SQL Injection and prepared statements

Do not try to cover every SQL feature in one session.

The strongest practical progression is:

```text
CREATE DATABASE
      ↓
CREATE TABLE
      ↓
INSERT DATA
      ↓
SELECT DATA
      ↓
FILTER DATA
      ↓
UPDATE DATA
      ↓
DELETE DATA
      ↓
JOIN TABLES
      ↓
SECURITY: SQL Injection
```
