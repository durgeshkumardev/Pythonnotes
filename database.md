# Introduction to Database 

## 1. What is Data?

**Data** refers to raw facts, numbers, symbols, or observations that are
collected for reference or analysis. Data by itself does not always
provide clear meaning, but when it is processed, organized, and
interpreted, it becomes useful information.

In simple terms:

> Data is the smallest unit of information that can be stored and
> processed by a computer system.

### Examples of Data

  Name      Age   Course
  --------- ----- --------
  Durgesh   20    BCA
  Rahul     21    BBA

Each individual value like **Durgesh**, **20**, or **BCA** is considered
data.

------------------------------------------------------------------------

## Types of Data

### 1. Numeric Data

Numeric data contains numbers that can be used in calculations.

Examples: - Age → 20 - Marks → 85 - Salary → 30000

Example table:

  Student   Marks
  --------- -------
  Durgesh   85
  Rahul     78

------------------------------------------------------------------------

### 2. Text Data

Text data contains characters or strings.

Examples: - Name - Address - Course Name

Example:

  Name      City
  --------- ---------
  Durgesh   Lucknow
  Priya     Delhi

------------------------------------------------------------------------

### 3. Date and Time Data

Used to store date or time values.

Examples: - Date of Birth - Admission Date - Order Date

  Student   Admission Date
  --------- ----------------
  Durgesh   2024-07-10

------------------------------------------------------------------------

# 2. What is Information?

Information is processed or organized data that has meaning and
usefulness.

In simple words:

> Information is meaningful data that helps in decision making.

### Example

Raw Data: Marks → 85, 78, 90

Information: - Priya scored the highest marks. - The class average is
84.

------------------------------------------------------------------------

# 3. What is a Database?

A **database** is a structured collection of related data that is stored
electronically in a computer system so it can be easily accessed,
managed, and updated.

### Simple Definition

> A database is an organized collection of data stored digitally for
> easy access and management.

### Example

  StudentID   Name      Course   Fee
  ----------- --------- -------- -------
  1           Durgesh   BCA      15000
  2           Rahul     BBA      20000
  3           Priya     MCA      25000

This table represents a part of a **college database**.

A real database may contain many tables such as: - Students - Courses -
Teachers - Fees - Attendance - Exams

------------------------------------------------------------------------

# 4. Real-Life Examples of Databases

## Banking System

Banks store: - Account Number - Customer Name - Balance - Transactions

Example:

  AccountNo   Name      Balance
  ----------- --------- ---------
  1001        Durgesh   25000
  1002        Rahul     30000

------------------------------------------------------------------------

## E-Commerce Systems

Online stores store: - Products - Customers - Orders - Payments

Example:

  ProductID   Product   Price
  ----------- --------- -------
  1           Laptop    50000
  2           Mobile    20000

------------------------------------------------------------------------

## Social Media

Social platforms store: - User profiles - Posts - Comments - Followers

Example:

  UserID   Username      Followers
  -------- ------------- -----------
  1        durgesh_dev   1200

------------------------------------------------------------------------

# 5. What is DBMS?

**DBMS (Database Management System)** is software used to create,
manage, and maintain databases.

### Definition

> A Database Management System is software that allows users to define,
> create, maintain, and control access to a database.

### Examples

-   MySQL
-   Microsoft SQL Server
-   Oracle Database
-   PostgreSQL
-   MongoDB

### Real Life Analogy

Think about a **library**:

-   Books → Data\
-   Library → Database\
-   Librarian → DBMS

The librarian organizes and helps find books easily, just like DBMS
manages data.

------------------------------------------------------------------------

# 6. Components of a Database

## Tables

Tables store data in rows and columns.

Example:

  StudentID   Name      Course
  ----------- --------- --------
  1           Durgesh   BCA
  2           Rahul     BBA

------------------------------------------------------------------------

## Rows (Records)

Each row represents one record.

  StudentID   Name      Course
  ----------- --------- --------
  1           Durgesh   BCA

------------------------------------------------------------------------

## Columns (Fields)

Columns represent attributes.

Example columns: - StudentID - Name - Course

------------------------------------------------------------------------

# 7. Types of Databases

Major database types:

1.  Relational Database\
2.  NoSQL Database\
3.  Hierarchical Database\
4.  Network Database\
5.  Object-Oriented Database

------------------------------------------------------------------------

# 8. Relational Databases

Relational databases store data in **tables** and use relationships
between tables.

Example:

Students Table

  StudentID   Name
  ----------- ---------
  1           Durgesh

Courses Table

  CourseID   CourseName
  ---------- ------------
  101        BCA

Enrollment Table

  StudentID   CourseID
  ----------- ----------
  1           101

### Popular Relational Databases

-   MySQL
-   SQL Server
-   Oracle
-   PostgreSQL

### Advantages

-   Structured data
-   Strong relationships
-   Data integrity
-   Standard SQL queries

------------------------------------------------------------------------

# 9. NoSQL Databases

NoSQL databases store data in flexible formats such as:

-   JSON Documents
-   Key-Value pairs
-   Graph structures

------------------------------------------------------------------------

## Document Database Example

``` json
{
  "name": "Durgesh",
  "course": "BCA",
  "age": 20
}
```

Examples: - MongoDB - CouchDB

------------------------------------------------------------------------

## Key-Value Database Example

    name : Durgesh
    course : BCA
    age : 20

Examples: - Redis - DynamoDB

------------------------------------------------------------------------

## Graph Database

Stores relationships.

Example:

Durgesh → Friend → Rahul\
Rahul → Friend → Priya

Example systems: - Neo4j

------------------------------------------------------------------------

# 10. Advantages of Databases

## Data Organization

Data is stored in structured tables.

## Data Security

Access control can be applied.

Example: - Admin → Full access - User → Limited access

## Data Sharing

Multiple users can access the database simultaneously.

## Data Integrity

Ensures accuracy and consistency.

## Backup and Recovery

Databases support backup and restore features.

------------------------------------------------------------------------
# SQL Database vs NoSQL Database (Detailed Explanation)

## 1. What is an SQL Database?

An **SQL Database (Structured Query Language Database)** is a type of
database that stores data in **tables consisting of rows and columns**
and uses SQL as the language to manage and query the data.

These databases are also called **Relational Databases (RDBMS)** because
the data is organized into **tables that are related to each other**.

### Definition

> An SQL database is a relational database system that stores structured
> data in tables with predefined schemas and uses Structured Query
> Language (SQL) to insert, update, delete, and retrieve data.

------------------------------------------------------------------------

## Example of SQL Database Table

  StudentID   Name      Course   Age
  ----------- --------- -------- -----
  1           Durgesh   BCA      20
  2           Rahul     BBA      21
  3           Priya     MCA      22

-   **Table** → Students\
-   **Row** → Individual student record\
-   **Column** → Attributes (Name, Course, Age)

### Example SQL Query

``` sql
SELECT * FROM Students;
```

------------------------------------------------------------------------

## Popular SQL Databases

-   MySQL
-   Microsoft SQL Server
-   PostgreSQL
-   Oracle Database

------------------------------------------------------------------------

## Characteristics of SQL Databases

### Structured Data

  ProductID   Product   Price
  ----------- --------- -------
  1           Laptop    50000
  2           Mobile    20000

### Fixed Schema

``` sql
CREATE TABLE Students (
ID INT,
Name VARCHAR(50),
Course VARCHAR(50)
);
```

### Relationships Between Tables

Students Table

  StudentID   Name
  ----------- ---------
  1           Durgesh

Courses Table

  CourseID   CourseName
  ---------- ------------
  101        BCA

Enrollment Table

  StudentID   CourseID
  ----------- ----------
  1           101

------------------------------------------------------------------------

## Advantages of SQL Databases

-   Data Integrity
-   Strong Relationships
-   Powerful Queries
-   Standard Language

------------------------------------------------------------------------

## Disadvantages of SQL Databases

-   Difficult horizontal scaling
-   Schema must be predefined
-   Not flexible for unstructured data

------------------------------------------------------------------------

# 2. What is a NoSQL Database?

A **NoSQL database (Not Only SQL)** is a type of database designed to
store and manage **unstructured or semi-structured data**.

Unlike SQL databases, NoSQL databases do **not rely on tables and fixed
schemas**.

### Definition

> A NoSQL database is a non-relational database system that allows
> flexible data models and is designed to handle large volumes of
> structured, semi-structured, or unstructured data.

------------------------------------------------------------------------

## Example of NoSQL Data (JSON Document)

``` json
{
 "name": "Durgesh",
 "course": "BCA",
 "age": 20
}
```

------------------------------------------------------------------------

## Popular NoSQL Databases

-   MongoDB
-   Redis
-   Apache Cassandra
-   Firebase

------------------------------------------------------------------------

## Types of NoSQL Databases

### Document Database

``` json
{
 "studentId": 1,
 "name": "Durgesh",
 "course": "BCA"
}
```

Examples: - MongoDB - CouchDB

------------------------------------------------------------------------

### Key-Value Database

    name : Durgesh
    course : BCA
    age : 20

Examples: - Redis - DynamoDB

------------------------------------------------------------------------

### Graph Database

Durgesh → Friend → Rahul\
Rahul → Friend → Priya

Example system: - Neo4j

------------------------------------------------------------------------

### Column Database

Examples: - Cassandra - HBase

------------------------------------------------------------------------

## Advantages of NoSQL Databases

-   Flexible Schema
-   High Scalability
-   High Performance
-   Handles Unstructured Data

------------------------------------------------------------------------

## Disadvantages of NoSQL Databases

-   Weak data relationships
-   No standard query language
-   Possible consistency issues

------------------------------------------------------------------------

# SQL vs NoSQL Comparison

  Feature          SQL Database      NoSQL Database
  ---------------- ----------------- -----------------------
  Data Structure   Tables            Documents / Key-Value
  Schema           Fixed             Flexible
  Relationships    Strong            Weak
  Query Language   SQL               Different APIs
  Scalability      Vertical          Horizontal
  Best For         Structured Data   Big Data

------------------------------------------------------------------------

# Real World Example

## Banking System

Banks use **SQL databases** because they require: - Strong data
consistency - Reliable transactions

## Social Media Platforms

Social media platforms often use **NoSQL databases** because they
handle: - Huge amounts of data - Flexible data structures

------------------------------------------------------------------------

# Simple Analogy

SQL Database → Excel sheet with fixed columns.

NoSQL Database → JSON documents where structure can change.

 
------------------------------------------------------------------------

 

# Introduction to SQL (Structured Query Language)

## What is SQL?

**SQL (Structured Query Language)** is a standard programming language
used to communicate with relational databases. It is used to create,
manage, manipulate, and retrieve data stored in database tables.

In simple terms:

> SQL is the language used to interact with databases.

Using SQL, users can perform operations such as:

-   Creating databases
-   Creating tables
-   Inserting data
-   Updating data
-   Deleting data
-   Retrieving data

SQL works with Relational Database Management Systems (RDBMS) such as:

-   MySQL
-   Microsoft SQL Server
-   Oracle Database
-   PostgreSQL

------------------------------------------------------------------------

# Why SQL is Important

SQL is important because almost every modern application uses databases.

Examples:

## Banking System

SQL is used to: - Check account balance - Transfer money - Store
transaction records

## E‑Commerce Websites

SQL manages: - Products - Customers - Orders - Payments

## Social Media Platforms

SQL manages: - User accounts - Posts - Comments - Likes

## College Management Systems

SQL manages: - Student records - Course information - Fees - Attendance

------------------------------------------------------------------------

# Characteristics of SQL

## 1. Simple Language

SQL has a simple and readable syntax.

``` sql
SELECT * FROM Students;
```

## 2. Standard Language

SQL is an international standard used by most database systems.

## 3. Powerful Data Retrieval

SQL allows complex queries to retrieve specific information.

## 4. Data Integrity

SQL helps maintain consistency and accuracy of data.

------------------------------------------------------------------------

# Types of SQL Commands

SQL commands are divided into five categories:

1.  DDL (Data Definition Language)
2.  DML (Data Manipulation Language)
3.  DQL (Data Query Language)
4.  DCL (Data Control Language)
5.  TCL (Transaction Control Language)

------------------------------------------------------------------------

# 1. DDL -- Data Definition Language

DDL commands define and manage database structure.

Common commands:

-   CREATE
-   ALTER
-   DROP
-   TRUNCATE

## CREATE Command

``` sql
CREATE TABLE Students (
    StudentID INT,
    Name VARCHAR(50),
    Course VARCHAR(50),
    Age INT
);
```

## ALTER Command

``` sql
ALTER TABLE Students
ADD Email VARCHAR(100);
```

## DROP Command

``` sql
DROP TABLE Students;
```

## TRUNCATE Command

``` sql
TRUNCATE TABLE Students;
```

------------------------------------------------------------------------

# 2. DML -- Data Manipulation Language

DML commands manipulate data inside tables.

Commands:

-   INSERT
-   UPDATE
-   DELETE

## INSERT Command

``` sql
INSERT INTO Students (StudentID, Name, Course, Age)
VALUES (1, 'Durgesh', 'BCA', 20);
```

Insert multiple rows:

``` sql
INSERT INTO Students VALUES
(2,'Rahul','BBA',21),
(3,'Priya','MCA',22);
```

## UPDATE Command

``` sql
UPDATE Students
SET Age = 21
WHERE StudentID = 1;
```

## DELETE Command

``` sql
DELETE FROM Students
WHERE StudentID = 2;
```

------------------------------------------------------------------------

# 3. DQL -- Data Query Language

DQL retrieves data from tables.

Main command:

-   SELECT

## SELECT Example

``` sql
SELECT * FROM Students;
```

Select specific columns:

``` sql
SELECT Name, Course
FROM Students;
```

Using WHERE condition:

``` sql
SELECT * FROM Students
WHERE Course = 'BCA';
```

------------------------------------------------------------------------

# 4. DCL -- Data Control Language

DCL controls access permissions.

Commands:

-   GRANT
-   REVOKE

Example:

``` sql
GRANT SELECT ON Students TO User1;
```

------------------------------------------------------------------------

# 5. TCL -- Transaction Control Language

TCL manages transactions.

Commands:

-   COMMIT
-   ROLLBACK
-   SAVEPOINT

Example:

``` sql
COMMIT;
```

------------------------------------------------------------------------

# Basic SQL Example

## Step 1 -- Create Table

``` sql
CREATE TABLE Students (
    ID INT,
    Name VARCHAR(50),
    Course VARCHAR(50)
);
```

## Step 2 -- Insert Data

``` sql
INSERT INTO Students VALUES (1,'Durgesh','BCA');
INSERT INTO Students VALUES (2,'Rahul','BBA');
INSERT INTO Students VALUES (3,'Priya','MCA');
```

## Step 3 -- Retrieve Data

``` sql
SELECT * FROM Students;
```

Result:

  ID   Name      Course
  ---- --------- --------
  1    Durgesh   BCA
  2    Rahul     BBA
  3    Priya     MCA

------------------------------------------------------------------------

# Advantages of SQL

-   Easy to learn
-   High performance
-   Standardized language
-   Data security

------------------------------------------------------------------------

 ### Database Data Types and Constraints

# 1. What is a Data Type?

Definition:
> A Data Type specifies the type of data that can be stored in a column of a table.

It tells the database whether the column will store:

- Numbers

- Text

- Dates

- Boolean values

- Binary data

```
CREATE TABLE Student
(
    Id INT,
    Name VARCHAR(50),
    Age INT,
    DOB DATE
);
```
# Explanation

| Column | Data Type | Description            |
| ------ | --------- | ---------------------- |
| Id     | INT       | Stores integer numbers |
| Name   | VARCHAR   | Stores text            |
| Age    | INT       | Stores numbers         |
| DOB    | DATE      | Stores date values     |


# 1. Numeric Data Types

- Numeric data types are used to store numbers.

| Data Type | Description                        | Example |
| --------- | ---------------------------------- | ------- |
| INT       | Stores integer numbers             | 10      |
| BIGINT    | Stores very large integers         | 100000  |
| SMALLINT  | Stores small integers              | 200     |
| TINYINT   | Stores values from 0 to 255        | 50      |
| DECIMAL   | Stores exact decimal numbers       | 10.25   |
| FLOAT     | Stores approximate decimal numbers | 15.23   |


# 2. Character (String) Data Types

- Character data types are used to store text or string values.

| Data Type    | Description                    |
| ------------ | ------------------------------ |
| CHAR(n)      | Fixed-length string            |
| VARCHAR(n)   | Variable-length string         |
| VARCHAR(MAX) | Large text data                |
| NCHAR(n)     | Unicode fixed-length string    |
| NVARCHAR(n)  | Unicode variable-length string |


# 3. Date and Time Data Types

These data types are used to store date and time values.

| Data Type | Description                       |
| --------- | --------------------------------- |
| DATE      | Stores only date                  |
| TIME      | Stores only time                  |
| DATETIME  | Stores both date and time         |
| DATETIME2 | More accurate version of DATETIME |

# 4. Boolean Data Type
- SQL Server does not have a direct Boolean type. Instead it uses BIT.
| Value | Meaning |
| ----- | ------- |
| 0     | False   |
| 1     | True    |


### 2. What is a Constraint?
Definition:
> A Constraint is a rule applied to a column to control the type of data that can be inserted.
> Constraints help maintain data accuracy and integrity in the database.

- Example
```
Name VARCHAR(50) NOT NULL
```
- This means the Name column cannot contain NULL values.


### Types of Constraints in SQL Server
# 1. Primary Key
- A Primary Key uniquely identifies each record in a table.
Rules

- Values must be unique

- NULL values are not allowed

- Each table can have only one primary key

Example
```
CREATE TABLE Student
(
    Id INT PRIMARY KEY,
    Name VARCHAR(50)
);
```

# 2. NOT NULL Constraint
- The NOT NULL constraint ensures that a column cannot store NULL values.

Example
```
Name VARCHAR(100) NOT NULL
```
# 3. UNIQUE Constraint

- The UNIQUE constraint ensures that all values in a column are different.
# Example
```
Email VARCHAR(100) UNIQUE
```

# 4. FOREIGN KEY

- A Foreign Key creates a relationship between two tables.

> It references the Primary Key of another table.

# Example
```
CREATE TABLE Orders
(
   OrderId INT PRIMARY KEY,
   UserId INT,
   FOREIGN KEY (UserId) REFERENCES Users(Id)
);
```

# 5. CHECK Constraint

- The CHECK constraint ensures that values meet a specific condition.

```
Age INT CHECK (Age >= 18)
```

# 6. DEFAULT Constraint
- The DEFAULT constraint assigns a default value when no value is provided.

```
IsActive BIT DEFAULT 1
```

```
CREATE TABLE Student
(
    Id INT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    Age INT CHECK (Age >= 18),
    IsActive BIT DEFAULT 1,
    CreatedDate DATETIME DEFAULT GETDATE()
);
```

