What is SQL
===========

_By Bernardo Blanchet_.

[Back to home](./index.md)

Introduction
------------

SQL (Structured Query Language) is a language used to read and write data to relational databases. It provides a standardized way to interact with databases, allowing users to create, read, update, and delete data using simple commands.

Sql vs. Other Storage Solutions
-------------------------------

SQL is better than other storage solutions for several reasons:

1. **Structured Data**: SQL databases are designed to handle structured data, making it easy to organize and retrieve information efficiently.
2. **ACID Compliance**: SQL databases ensure data integrity through ACID (Atomicity, Consistency, Isolation, Durability) properties, which guarantee reliable transactions.
3. **Standardization**: SQL is a standardized language, meaning it can be used across different database systems with minimal changes.
4. **Complex Queries**: SQL allows for complex queries, enabling users to retrieve and manipulate data in powerful ways.
5. **Scalability**: SQL databases can handle large volumes of data and are suitable for both small and large applications.

Sql Commands
------------

### The SELECT Statement

The `SELECT` statement is used to retrieve data from a database.

Example:

SELECT id, name, email
FROM users
WHERE active=1;

### The INSERT Statement

The `INSERT` statement is used to insert new data into a database table.

Example:

INSERT INTO users (id, name, email)
VALUES (1, 'John Doe', 'john.doe@example.com');

### The UPDATE Statement

The `UPDATE` statement is used to modify existing data in a database table.

Example:

UPDATE users
SET name = 'Jane Doe'
WHERE id = 1;

### The DELETE Statement

The `DELETE` statement is used to remove data from a database table.

Example:

DELETE FROM users
WHERE id = 1;

Sql Clauses
-----------

### The WHERE Clause

The `WHERE` clause is used to filter records that meet certain conditions.

Example:

SELECT name 
FROM users 
WHERE active=1;

### The ORDER BY Clause

The `ORDER BY` clause is used to sort the result set in either ascending or descending order.

Example:

SELECT name 
FROM users 
ORDER BY name ASC;

### The GROUP BY Clause

The `GROUP BY` clause is used to group rows that have the same values in specified columns into summary rows.

Example:

SELECT COUNT(*), country 
FROM users 
GROUP BY country;

### The LIMIT Clause

The `LIMIT` clause is used to specify the number of records to return.

Example:

SELECT name 
FROM users 
LIMIT 10;

Other Sql Commands
------------------

### The CREATE TABLE Command

The `CREATE TABLE` command is used to create a new table in the database.

Example:

CREATE TABLE users (
    id int primary key,
    name varchar(255),
    active tinyint
);

### The ALTER TABLE Command

The `ALTER TABLE` command is used to modify an existing table structure.

Example:

ALTER TABLE users
ADD COLUMN email varchar(255);

### The DROP TABLE Command

The `DROP TABLE` command is used to delete a table and all of its data from the database.

Example:

DROP TABLE users;
