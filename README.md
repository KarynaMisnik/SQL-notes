# SQL-notes

## Table of Contents

- [Database and its Concepts](#database-and-its-concepts)
  - [Database Management System](#database-management-system)
  - [Data Models](#data-models)
    - [Data models and the relational model](#data-models-and-the-relational-model)
  - [SQL](#SQL)
- [Database Queries](#database-queries)
- [Manipulating Data](#manipulating-data)
- [Designing Database Structure](#designing-database-structure)
- [Normalization](#normalization)
- [Database Performance](#database-performance)
- [Database Security](#database-security)
- [Open Interfaces and NoSQL](#open-interfaces-and-nosql)

# Database and its Concepts

A computer database is an organized collection of electronic data designed for efficient storage, retrieval, and manipulation by authorized users. Similar in concept to traditional index cards but far more advanced, databases store only necessary, standardized data tailored to the needs of their users. Their size and complexity can range from simple home recipe collections to massive systems managing millions of customer transactions.

A database contains only data relevant to its defined purpose, excluding any unnecessary or unrelated information. During its design, the intended use is clearly specified, ensuring all stored data is logically connected. For example, a library database would include information about loanable items and their details but not unrelated data like weather forecasts. This purposeful organization distinguishes a true database from random, unstructured data collections.

A database is designed with specific, known users in mind, as its purpose is to serve their needs. Identifying users is essential to determine what data should be stored. For instance, a library database is tailored for visitors and staff, providing information relevant to their requirements, such as item details and availability. This user-focused design distinguishes databases from random data collections.

Every database follows a specific data model that defines how data is stored, presented, and manipulated with precision. The model determines the structure of data units (records), their types, and the relationships between them, shaping how users view and interact with the data. It enables the creation of complex information by connecting simple data records through defined semantic relationships.

**Key Features:**

|                                                                      Structured Data |                                                                                        Scalability |                                                      Integrity and Security |                                                      Persistence |
| -----------------------------------------------------------------------------------: | -------------------------------------------------------------------------------------------------: | --------------------------------------------------------------------------: | ---------------------------------------------------------------: |
| Data is stored in tables that are connected, keeping it organized and easy to search | Databases can manage more data and users efficiently using methods like splitting and copying data | Databases keep data accurate with rules and protect it with access controls | Committed data stays saved even if the system restarts or crashe |

### Database Management System

**A Database Management System (DBMS)** is essential software that enables users to interact with databases, which are typically <ins>too complex</ins> for direct access. Acting as an intermediary between users and the database, the DBMS allows for creating, modifying, and managing databases through standardized communication, such as SQL in relational databases. While it simplifies database operations, effective use often requires knowledge of SQL and the data model, which is why client programs frequently handle this interaction for end-users.

**A Database Management System (DBMS)** is essential for handling the inherent complexity of modern, multi-user databases. Commercial database products primarily provide a DBMS, as it enables creating, accessing, and maintaining databases. The DBMS also determines the supported data models, meaning a relational DBMS is required for managing relational databases and performing key administrative tasks.

<p align="center">
  <img src="img/dbms.png" alt="Database flow diagram" width="500"/>
</p>

_Figure 1: SQL sends queries to the DBMS, which interacts with the database._

### Data Models

**A data model** defines the logical structure and rules for how data is presented and manipulated in a database but does not determine its physical storage. The physical structure—how data is written, stored, and retrieved—is handled by the database software and remains hidden from users. Thus, databases using the same data model, such as the relational model, appear similar to users while functioning differently internally.

**The relational model** is a standardized data model used in relational databases, which adhere strictly to its principles. However, some relational DBMSs support extended forms, such as object-relational databases, that integrate object-oriented features. These hybrid models combine aspects of relational and object-oriented approaches but are usually vendor-specific and non-standard.

#### Data models and the relational model

The relational model centers on the concept of <ins>relations</ins>, which represent all data and operations within the system. Its strength lies in providing semantic meaning by defining how data items relate to each other, enabling users to extract meaningful information rather than just isolated data. For example, in a library database, relations can link books to authors, publishers, and borrowing history, creating valuable insights from connected data rather than standalone records.

### SQL

**SQL (Structured Query Language)** is a standardized language used mainly in <ins>relational databases</ins> for querying, manipulating, and managing data. While integral to relational systems, it does not fully adhere to the relational model, allowing structures that may violate strict relational rules (e.g., duplicate rows, missing primary keys). Users must understand the relational model to apply SQL correctly, and DBMSs often enforce constraints to prevent improper use.

```sql
SELECT first_name, last_name
FROM employees;
```
