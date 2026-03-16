# Introduction to Database -- Day 1 (Detailed Lecture Notes)

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

# 11. Introduction to SQL

**SQL (Structured Query Language)** is used to communicate with
relational databases.

SQL can: - Create tables - Insert data - Update data - Delete data -
Retrieve data

Example:

``` sql
SELECT * FROM Students;
```

This command retrieves all records from the Students table.

------------------------------------------------------------------------
 
 