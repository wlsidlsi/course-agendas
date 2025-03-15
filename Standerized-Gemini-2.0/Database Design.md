**I. Relational Database Fundamentals**

*   Understanding Database Concepts
    *   Defining databases, tables, records, and fields.
    *   Understanding primary keys, foreign keys, and composite keys.
    *   Database normalization: 1NF, 2NF, 3NF.
*   Relational Model Principles
    *   Entities, attributes, and relationships.
    *   Entity-Relationship (ER) diagrams.
        *   Drawing ER diagrams for simple scenarios.
        *   Understanding cardinality (one-to-one, one-to-many, many-to-many).
*   SQL Basics
    *   Data Definition Language (DDL): `CREATE`, `ALTER`, `DROP`.
    *   Data Manipulation Language (DML): `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
    *   Basic `SELECT` statements with `WHERE` clauses.
    *   Ordering results with `ORDER BY`.

**II. Advanced SQL**

*   Joins
    *   Understanding `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL OUTER JOIN`.
    *   Joining multiple tables.
    *   Self-joins.
*   Subqueries
    *   Using subqueries in `WHERE` clauses.
    *   Correlated subqueries.
    *   Subqueries in `SELECT` clauses.
*   Aggregate Functions
    *   `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`.
    *   Using `GROUP BY` and `HAVING`.
*   Window Functions
    *   Understanding `OVER()`, `PARTITION BY`, `ORDER BY` within window functions.
    *   Examples: `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`.
*   Transactions and Concurrency Control
    *   ACID properties: Atomicity, Consistency, Isolation, Durability.
    *   `BEGIN TRANSACTION`, `COMMIT`, `ROLLBACK`.
    *   Understanding locking mechanisms.

**III. Database Design Principles**

*   Normalization in Detail
    *   Reviewing 1NF, 2NF, 3NF, BCNF.
    *   Identifying and resolving data anomalies.
    *   Denormalization: reasons and strategies.
*   Data Modeling
    *   Conceptual, logical, and physical data models.
    *   Creating a logical data model from business requirements.
    *   Mapping a logical data model to a physical database schema.
*   Indexing
    *   Understanding different types of indexes.
    *   Creating indexes for query optimization: `CREATE INDEX`.
    *   Analyzing query execution plans.
*   Database Security
    *   User authentication and authorization.
    *   Role-based access control (RBAC).
    *   SQL injection prevention.

**IV. Database Management Systems (DBMS)**

*   Exploring Different DBMS
    *   MySQL
    *   PostgreSQL
    *   SQL Server
    *   Oracle
    *   MongoDB (NoSQL - document database)
*   DBMS Architecture
    *   Understanding the components of a DBMS (e.g., query processor, storage manager, transaction manager).
    *   Client-server architecture.
*   Backup and Recovery
    *   Implementing backup strategies.
    *   Performing database recovery.
    *   Disaster recovery planning.
*   Performance Tuning
    *   Identifying performance bottlenecks.
    *   Optimizing queries.
    *   Database configuration parameters.

**V. NoSQL Databases**

*   Introduction to NoSQL
    *   Understanding NoSQL concepts: key-value, document, column-family, graph databases.
    *   CAP Theorem: Consistency, Availability, Partition Tolerance.
    *   When to use NoSQL vs. Relational Databases.
*   MongoDB
    *   Document structure (JSON-like).
    *   CRUD operations (Create, Read, Update, Delete).
        *   `db.collection.insert()`, `db.collection.find()`, `db.collection.update()`, `db.collection.remove()`.
    *   Aggregation framework.
    *   Indexing in MongoDB.
*   Other NoSQL Databases (Overview)
    *   Cassandra (Column-family)
    *   Redis (Key-Value)
    *   Neo4j (Graph)

**VI. Database Project**

*   Designing and implementing a database for a real-world application.
    *   Example: E-commerce website, library management system, social media platform.
*   Project Phases
    *   Requirements gathering.
    *   ER diagram design.
    *   Schema creation.
    *   Data population.
    *   Query development.
    *   Application integration (if applicable).
    *   Testing and optimization.
