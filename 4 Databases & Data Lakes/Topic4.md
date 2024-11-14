# Database administration and optimisation

## Database Administration Best Practices
- Scalability - Scalability refers to the ability to handle increasing data volumes and user loads
- Performance - Performance focuses on efficient query processing and response times
- Data Consistency - Data consistency ensures data integrity and consistency across the database
- Transaction - Transaction support handles concurrent transactions and maintains data consistency
## When evaluating specific application requirements, it's essential to consider:
 - The data structure and relationships
 - Expected data volume and growth
 - Query patterns and performance expectations
 - Consistency and availability trade-offs.
## Designing for scalability and performance involves considering:
- Data volume and growth rate, 
- Query patterns and performance, 
- Partitioning and sharding, 
- Caching mechanisms, 
- Monitoring and performance tuning
## Database Performance Metrics
- Query Performance
  - Poorly formatted or overly general queries can introduce slowdowns
- User and Query Conflicts
  - Slowdowns can occur when multiple users are accessing the database.
- Business Transactions
  - Look at end-user experience of real-time performance
- Capacity
  - Consider CPUs, disk performance, memory, configurations and network connections.
- Configuration
  - Be sure to change default settings for elements like buffer and query caches.
- Tips
  - Optimise Queries
  - Improve Indexes
  - Defragment Data
  - Increase Memory
  - Strengthen CPU
  - Review Access
## Partitioning and sharding
Partitioning and sharding techniques distribute data across multiple nodes or servers, either through horizontal partitioning (sharding) based on a key or range or vertical partitioning based on columns or data types. This improves query performance and scalability. Caching mechanisms, such as implementing caching layers (e.g., Redis, Memcached) and storing frequently accessed data in memory, reduce database load and improve response times. Regular monitoring of database metrics, identifying performance bottlenecks and slow queries, tuning database parameters and configurations, and analysing and optimising query execution plans are essential for maintaining optimal performance.

## Security

![image](https://github.com/user-attachments/assets/e65f6dfd-1f7c-4b02-9ca1-4c5a2e254038)

- Authorisation & Access control
  - Access controls and authentication mechanisms, such as setting up user accounts and roles, implementing strong authentication, and restricting access based on the principle of least privilege, help in securing the database. Role-based access control (RBAC) allows defining user roles and permissions, granting access based on user roles and responsibilities, and regularly reviewing and updating role assignments.
- Data Encryption
  - Data encryption, using strong encryption algorithms and key management, protects sensitive data at rest and in transit, mitigating the risk of unauthorized access and data breaches.
- Data Integrity Verification
  - Implementing regular data backups, testing backup integrity and restore procedures, establishing a disaster recovery plan, and ensuring data availability and minimising downtime are essential for data protection and business continuity.
 
## SQL and NoSQL databases

- The differences between SQL and NoSQL approaches lie in their data models, scalability, query languages, and consistency guarantees.
### NoSQL

- NoSQL databases are suitable for applications with large volumes of unstructured or semi-structured data, high scalability and performance requirements, and flexible and evolving data schemas. Examples include social networks, real-time analytics, and content delivery networks.
  
- Designed to handle large volumes of unstructured or semi-structured data.
- Utilise non-relational data models, such as key-value stores (data stored as key-value pairs), document databases (data stored as semi-structured documents like JSON or XML), columnar databases (data stored in columns instead of rows), and graph databases (data represented as nodes and edges in a graph structure).
- Offer a flexible schema, allowing for dynamic and evolving data structures. They follow a schema-less or schema-on-read approach, accommodating unstructured and semi-structured data. 
- NoSQL databases are designed for horizontal scalability across multiple servers, with a distributed architecture for handling large-scale data. They are optimised for high-performance read and write operations. 
- NoSQL databases often prioritise eventual consistency, relaxing strict consistency in favour of availability and partition tolerance. This allows for temporary inconsistencies that are eventually resolved, making them suitable for applications that can tolerate eventual consistency.

### Database changes and costs
- Schema changes, such as adding or modifying columns in SQL databases, may require updates to downstream applications, whereas NoSQL databases have more flexibility to accommodate schema changes.
- Processing and storage costs vary between SQL and NoSQL databases. SQL databases typically have lower storage costs due to efficient storage of structured data but can have higher processing costs for complex queries involving joins and aggregations. NoSQL databases may have higher storage costs due to the overhead of storing unstructured or semi-structured data but often have lower processing costs for simple queries and high-volume data ingestion. Factors affecting costs include data volume and growth rate, query complexity and frequency, indexing and partitioning strategies, hardware and infrastructure requirements, and licensing and support costs.

## Monitoring and Optimising Database Performance

### Monitoring metrics
- Response time - Query response time measures the time taken to execute and return the results of a query, helping identify slow-running queries that may impact overall performance and optimize query execution and indexing strategies.
- Throuput - Throughput tracks the number of queries or transactions processed per unit of time, measuring the system's capacity to handle a certain workload and identifying performance bottlenecks and scaling requirements.
- Concurrency - Concurrency monitors the number of concurrent users or connections accessing the database, ensuring the database can handle the expected level of concurrency and identifying contention issues and optimising resource allocation.
- Resource utilisation - Resource utilisation metrics include CPU usage, which monitors the utilisation of CPU resources by the database processes, memory usage, which tracks the memory consumption of the database and its components, and disk I/O, which measures the read and write operations performed on the storage disks. These metrics help in identifying resource-intensive queries and optimising system resources
- Indexing - Indexing effectiveness analyses the usage and performance of indexes, identifies missing or inefficient indexes that impact query performance, and helps optimise indexing strategies based on query patterns.
  

# In your learning journal, research the third-party database monitoring solutions that your company uses.

### Query profiling
- Query logging and analysis, also known as query profiling,  involves examining executed queries from users and their performance metrics, analysing query logs to identify slow queries, inefficient patterns of usage, and opportunities for improving things – such as rewriting queries or reshaping tables. Regular performance reviews are conducted to assess database health, identify improvement areas, analyse trends, identify bottlenecks, make data-driven optimization decisions, and collaborate with stakeholders to align performance goals with business requirements.
- https://www.geeksforgeeks.org/explain-in-sql/
### Indexing Strategies
- Indexing strategies focus on creating appropriate indexes on frequently queried columns, choosing the right index types based on data characteristics and query patterns, and monitoring index usage and performance to identify redundant or underutilised indexes.
- Indexing is one of the best practices that you can use to maintain performance and effectiveness. When you index your data, it helps reduce the amount of I/O required to retrieve information from your tables.It also improves performance by reducing the number of disks required to read disk data.
- Creating an index for every table in your database is not necessary. But it is recommended that you create an index for tables containing lots of columns, those most commonly used, and those with high cardinality.
- If there are several indexes for a single table, each index would have a small set of rows. Likewise, each index would have a different set of rows. For example, a single customer document can include customer information, customer orders, customer shipping information, and customer billing information.
  
### Database configuration
- Database configuration tuning involves adjusting database configuration parameters to optimize performance, such as memory allocation, buffer sizes, caching mechanisms, and parallelism settings, based on workload characteristics and hardware resources. Horizontal scaling (sharding) distributes data across multiple database instances or servers, partitioning data based on a key or range to distribute the workload and enable parallel processing and improved scalability for large datasets. Vertical scaling adds more resources (CPU, memory, storage) to a single database server, suitable for scenarios where the database can benefit from increased hardware capabilities but requires careful capacity planning and monitoring to avoid resource saturation.
### Collaboration
- Collaboration between data engineers and database administrators (DBAs) is essential for smooth integration and optimization of databases within the data ecosystem. Data engineers focus on data pipelines, data integration, and overall data architecture, while DBAs specialize in database management, performance tuning, and security. Effective communication, regular discussions on database requirements, performance goals, and optimization strategies, and collaboration on database design, schema changes, and migration plans are crucial. Knowledge sharing, conducting joint performance reviews and analysis sessions, and continuously learning from each other's expertise help improve overall database management.

https://learn.bpp.com/pluginfile.php/1326275/mod_resource/content/1/L5DE%20M2T4%20v1.pdf

## Data profiling:
https://www.ibm.com/products/infosphere-information-analyzer

## Database Archiving

https://aws.amazon.com/s3/storage-classes/glacier/
https://www.oracle.com/a/ocom/docs/archivesolutionbriefv3e-2176210.pdf
https://www.druva.com/glossary/what-is-data-archiving-definition-and-related-faqs#:~:text=The%20advantages%20of%20archiving%20data,backup%20and%20recovery%20runs%20faster.

## SQL Query Optimisation

