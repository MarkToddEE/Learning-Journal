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
- Nested Create - While SQL doesn't directly support nested 'CREATE' statements, complex 'CREATE' operations can involve subqueries to define or populate new tables based on existing data. For example, creating a new table that aggregates existing customer data but only includes those who meet certain spending thresholds.
- Nested Read - This is commonly used in reports and data analysis, where information from different parts of the database needs to be consolidated. For example, selecting customer data where the customer’s spending is above the average within their demographic.
- Nested Update - Useful in scenarios where the update criteria or the values to be updated depend on another query. For instance, increasing the price of products in a catalogue only if their stock levels are below a certain threshold.
- Nested Delete - Applied when certain deletion criteria are complex and depend on other data elements. For example, deleting records of a promotional campaign that did not reach any customers in specific regions.

UPDATE Inventory
SET status = 'Low Stock'
WHERE product_id IN (
    SELECT product_id
    FROM Sales
    WHERE sale_date BETWEEN DATE_SUB(NOW(), INTERVAL 1 MONTH) AND NOW()
    GROUP BY product_id
    HAVING SUM(sales_quantity) > 0.75 * (SELECT stock_quantity FROM Inventory 
WHERE Inventory.product_id = Sales.product_id)
) AND restocking_date > DATE_ADD(NOW(), INTERVAL 2 WEEK);

Sets the 'status' field in the 'Inventory' table to "Low Stock" using 'product_id' as a common field
All product id's from Sales that have a Sales date in the last month and the quantity sold is 3/4 of the 'stock quantity' from Inventory
And, where the restocking date is > 2 weeks away

## Understanding Nested and Correlated Queries in SQL
### Correlated Queries

SELECT * FROM Customers c
WHERE EXISTS (
  SELECT 1 FROM Orders o
  WHERE o.CustomerID = c.CustomerID
);

- Corelated Queries run for each outer row but as a result can be slower to run. Rely on outer queries. Use correlated queries for complex conditions involving row comparisons. 
- Nested queries run once, are quicker and are independant

## Joins and Database Normalisation

### The Role of Joins
  - Joins are critical in relational databases as they facilitate the retrieval of information dispersed across multiple tables. The ability to join tables allows databases to store information in a normalised form while still being able to present a unified view of related data when necessary.
![SQL Join 2](https://github.com/user-attachments/assets/a262060d-2c6e-45e3-aad1-035ecfeaa72a)


- Inner Join - Retrieves rows that have matching values in both tables.
  SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC

  ![image](https://github.com/user-attachments/assets/5148cf68-b698-436a-8ee7-968dd75bc5bb)
  ![image](https://github.com/user-attachments/assets/0168373d-79d8-41aa-9a63-628187352d54)
![image](https://github.com/user-attachments/assets/6e7daaa8-7e50-4598-9855-610c3348ed0a)


- Outer Join (Left, Right and Full) - Retrieves matching rows in both tables and some unmatched rows in one or both tables, depending on the type of outer join.
SELECT column, another_column, …
FROM mytable
INNER/LEFT/RIGHT/FULL JOIN another_table 
    ON mytable.id = another_table.matching_id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;

  ![image](https://github.com/user-attachments/assets/dafffc9d-95f8-4d6b-9588-eb2fa218bc39)

- Dealing with Nulls
SELECT column, another_column, …
FROM mytable
WHERE column IS/IS NOT NULL
AND/OR another_condition
AND/OR …;
![image](https://github.com/user-attachments/assets/5d8ffabd-ecc3-4eea-b73d-718be45759e5)
![image](https://github.com/user-attachments/assets/6893014b-412f-4095-868d-8875ce30e2a0)

  
- Cross Join - Produces a Cartesian product of the rows in the tables involved in the join.
- Queries with expressions
- 
  SELECT col_expression AS expr_description, …
FROM mytable;
![image](https://github.com/user-attachments/assets/bfbe564e-cdde-4ae0-a2d7-65aad2be6036)
![image](https://github.com/user-attachments/assets/c2ba7a44-cd2f-43df-9fc4-2a11f3545b5f)
% is the Modulus after dividing by 2 ie the remainder


### Normalisation
- First Normal Form - Ensures all columns hold atomic values and each record is unique.
- Second Normal Form - Requires that all non-key attributes are fully functional dependent on the primary key.
- Third Normal Form - Ensures that no transitive dependencies exist between non-key attributes and the primary key.

https://www.dummies.com/article/technology/programming-web-design/sql-first-second-and-third-normal-forms-160848/

## GroupBy, Aggregation, and Windowing in SQL
![image](https://github.com/user-attachments/assets/c0545c23-6a48-44d9-9241-6312dbc80816)

SELECT AGG_FUNC(column_or_expression) AS aggregate_description, …
FROM mytable
WHERE constraint_expression
GROUP BY column;

![image](https://github.com/user-attachments/assets/795c0b3f-35bf-433e-8011-df6215f44769)
![image](https://github.com/user-attachments/assets/58f1f462-5c1e-4308-ba6c-4c6447d9451b)

Select query with HAVING constraint
SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …
FROM mytable
WHERE condition
GROUP BY column
HAVING group_condition;

![image](https://github.com/user-attachments/assets/fc7198f7-b887-41f2-935d-d355b422c96e)

![image](https://github.com/user-attachments/assets/19facd42-d03f-48da-95bb-3c85f3c598d2)

## Order of execution of a Query

1. FROM and JOINs
The FROM clause, and subsequent JOINs are first executed to determine the total working set of data that is being queried. This includes subqueries in this clause, and can cause temporary tables to be created under the hood containing all the columns and rows of the tables being joined.

2. WHERE
Once we have the total working set of data, the first-pass WHERE constraints are applied to the individual rows, and rows that do not satisfy the constraint are discarded. Each of the constraints can only access columns directly from the tables requested in the FROM clause. Aliases in the SELECT part of the query are not accessible in most databases since they may include expressions dependent on parts of the query that have not yet executed.

3. GROUP BY
The remaining rows after the WHERE constraints are applied are then grouped based on common values in the column specified in the GROUP BY clause. As a result of the grouping, there will only be as many rows as there are unique values in that column. Implicitly, this means that you should only need to use this when you have aggregate functions in your query.

4. HAVING
If the query has a GROUP BY clause, then the constraints in the HAVING clause are then applied to the grouped rows, discard the grouped rows that don't satisfy the constraint. Like the WHERE clause, aliases are also not accessible from this step in most databases.

5. SELECT
Any expressions in the SELECT part of the query are finally computed.

6. DISTINCT
Of the remaining rows, rows with duplicate values in the column marked as DISTINCT will be discarded.

7. ORDER BY
If an order is specified by the ORDER BY clause, the rows are then sorted by the specified data in either ascending or descending order. Since all the expressions in the SELECT part of the query have been computed, you can reference aliases in this clause.

8. LIMIT / OFFSET
Finally, the rows that fall outside the range specified by the LIMIT and OFFSET are discarded, leaving the final set of rows to be returned from the query.

![image](https://github.com/user-attachments/assets/4d64148e-6277-418c-a266-f7cf31eac834)
![image](https://github.com/user-attachments/assets/abd7dab2-90a7-4ba4-b646-6d98c10345d0)

