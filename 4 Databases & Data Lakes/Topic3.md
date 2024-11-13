# Impacts of upstream data modelling on downstream experience
## 5 things to ask before pushing schema change to production

- 1 Is a change management process embedded into your data engineering workflow? 

- 2 What is the structure of your data organisation? 

- 3 What impact up and downstream will the schema change have? 

- 4 How will you communicate schema changes with the broader data team? 

- 5 Are you measuring the impact of change management on your organisation?

## What are views ?
- A view in DBMS is a virtual table that is derived from one or more base tables or views. Similar to what Access calls a Query
## What is a Stored Procedure? 
- Also known as a stored proc, or a sproc, a stored procedure is a prepared SQL code. It is a user-created code snippet that Data Engineers upload to a database to  make it automatically perform a set of SQL queries and logical operations. The procedure is stored in the database. It saves you time as the code can be reused over and over again. So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it. Most SQL operations in stored procedures are so-called CRUD operations
  - C Create/Insert
  - R Read/Select
  - U Update
  - D Delete
## The importance of good data modelling

![image](https://github.com/user-attachments/assets/9e3305e7-780b-4308-a65c-fc736929b2d2)

- Conceptual Data Model - This model provides a high-level overview of the database without delving into technical details. It focuses on the broad structure of the database and the relationships between major entities in the system. It is often used for initial planning and agreement between stakeholders on the major entities and relationships in the system.
- Logical Data Model - This model describes the data in more detail but without concern for how they will be physically implemented in the database. It includes all entities, their attributes, and relationships, along with key constraints that should apply. It is used to translate the conceptual model into a more technical blueprint that database designers can understand and use.
- Physical Data Model - This model outlines how the database will be physically realised on the storage system. It details the complete structure of the database, including tables, columns, data types, constraints, indexes, and how they are physically stored on disk. This model is used to build the actual database according to the specified performance, security, and storage requirements.

## Key Definitions
- Triggers - Database triggers are procedures that automatically execute in response to specific events on a particular table or view in a database. They are used to maintain the integrity of the data across complex business rules and relationships.
- Views - Views are virtual tables based on SQL queries. They allow users to structure data in a way that users or classes of users find natural or intuitive, hiding the complexity of the database schema.
- Stored Procedures - Stored procedures are SQL code that you can save, so the code can be reused over and over again. They can perform complex operations, from data validation to batch processing with conditional logic, and can reduce traffic between an application and the database server by bundling commands.
- Normalisation - Normalisation is a systematic approach of decomposing tables to eliminate data redundancy (repetition) and undesirable characteristics like Insertion, Update, and Deletion Anomalies. It is a multi-step process that puts data into tabular form by removing duplicated data from the relational tables. Normalisation helps to reduce redundancy and dependency by organising fields and table of a database. The main aim of normalisation is to add, delete, or modify fields that can be made in a single table and then propagated through the rest of the database via the defined relationships.
- Redundancy - In the context of database management, redundancy occurs when the same piece of data is stored in two or more separate places, either within the same database or across multiple databases. Redundancy can lead to inconsistencies during data updates, increased storage requirements, and unnecessary complexity in data handling. While sometimes used intentionally for improving data retrieval performance and ensuring data availability, redundancy often requires careful management to avoid data integrity issues.
- Comprensive Data Types - These are specific kinds of data attributes that define the kind of data a column can hold in a database. They help in accurately describing the data characteristics, such as integers, decimals, dates, or strings, ensuring that data inputs are processed and stored correctly.
- Constraint Implementations - Constraints in a database ensure the accuracy and reliability of the data in the database. They enforce rules on the data fields, such as primary keys, foreign keys, unique, not null, and check constraints, to maintain data integrity and enforce business rules.
- Indexing Strategies - These are plans or methods implemented to improve database performance. Indexing strategies involve creating indexes on tables to speed up the retrieval of rows at the cost of additional writes and storage space to maintain the index data structures.
- Indexes - Indexes are special lookup tables that the database search engine can use to speed up data retrieval. Simply put, an index in a database is similar to an index in the back of a book.
- Database Business Requirements - These are specifications derived from business needs that outline what the business intends to achieve with the database. These requirements focus on what data needs to be stored and how it will be used to support business processes.
- Database User Requirements - These are detailed requirements that describe what the end-users need the database to do, from how data should be input, to how it should be manipulated, accessed, and presented. These are more focused on the usability and functionality of the database from the user's perspective.
# ACID and the Importance of Transactions
- The ACID properties (Atomicity, Consistency, Isolation, Durability) provide a foundation for reliable database transactions, ensuring that all operations within a transaction are completed successfully or not at all. This framework is essential in environments where data accuracy and reliability are paramount, such as financial systems, e-commerce platforms, and other business-critical applications.
- 
- A Atomicity Transactions are all or nothing. Atomicity guarantees that each transaction is treated as a single unit, which either succeeds completely or fails completely. If one part of the transaction fails, the entire transaction fails, and the database state is left unchanged.
- C Consistency Only Valid Data is saved. Consistency ensures that a transaction can only bring the database from one valid state to another, maintaining database invariants.
- I Isolation Transactions do not affect each other. Isolation ensures that concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed serially.Provides the illusion that each transaction is the only one interacting with the database at that time. This is achieved by various concurrency control mechanisms, ensuring that transactions do not affect each other adversely.
- D Durability Written data will not be lost. Durability guarantees that once a transaction has been committed, it will remain so, even in the event of a power loss, crashes, or errors.
# Writing Nested CRUD SQL Queries
