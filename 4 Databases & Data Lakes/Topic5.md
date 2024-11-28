# NoSQL Fundamentals
Not Only SQL (NoSQL) brings flexibility, scalability, and speed to handle the massive variety of unstructured data.
They are particularly useful when dealing with a large volume of data where the data's nature does not require a relational model.
The importance of NoSQL databases stems from their ability to handle varied data types, including unstructured and semi-structured data. Their flexible and scalable nature makes them ideal for handling large volumes of data, leading to faster, more efficient data processing.

## Example:
### SQL
![image](https://github.com/user-attachments/assets/b0bd7fbe-8fef-4f99-a239-9518bb74e3f7)
![image](https://github.com/user-attachments/assets/46068ccc-1e41-4a65-8796-69ac4411cd2c)
![image](https://github.com/user-attachments/assets/5ef8002a-3b92-488f-b2e7-be66eb4e9206)

A traditional SQL database would struggle to accommodate this kind of varied, unstructured data efficiently. To make SQL work, we would have to create a vast table with many null entries for missing attributes, which is messy, inefficient and can make data retrieval slower.
## NoSQl
A NoSQL database can store each of these data records as separate documents without any need for a predefined schema
![image](https://github.com/user-attachments/assets/a61add0f-0a7f-4569-a9d7-32332ac91f77)
JSON format

![image](https://github.com/user-attachments/assets/9fbcf659-a7d2-4ace-91d9-cfac8fadd27a)

## Types of NoSQL databases
- Document Based
  - Document databases store data in documents like JSON (JavaScript Object Notation) objects. Each document contains pairs of fields and values. The values can typically be a variety of types including strings, numbers, booleans, arrays, or objects, and their structure doesn't have to be predefined.Eg. Mongo Db
 ![image](https://github.com/user-attachments/assets/cf07fe01-d45b-463f-a63d-1109f83b134a)

    
- Key Value stores
  - Key-value stores are the simplest type of NoSQL database. Every single item in the database is stored as an attribute name (or 'key'), together with its value. They are great for caching, session management, and maintaining a shopping cart for an e-commerce website. Eg Redis
- Column-Family Stores
  - These databases store data in columns instead of rows which can be quickly searched and aggregated. They can query large data volumes faster than relational databases. They're best for analysing large datasets and are often used in data warehousing and big data space. Eg Cassandra is a column-family NoSQL database. A large telecommunications company might use Cassandra to store call records. The call time, duration, caller id, and receiver id might all be stored in separate columns.
- Graph Based
  - Graph databases use graph structures (a network of nodes and edges) for semantic queries. Nodes represent entities and edges represent relationships between entities. They are ideal for handling data where relationships are at the core, like social networks, recommendation engines, etc.Neo4j is a popular graph database. In a social network application, each user could be a node and each relationship (like a friend connection) could be an edge.

All NoSQL types are designed to be more scalable than traditional Relational Database Management System (RDBMSs), but they each achieve scalability differently. Columnar databases, for instance, are particularly suited for scaling large, read-heavy workloads, while key-value stores can scale out easily but might have more limitations in querying capabilities.

## Mongo Db
How MongoDB stores data:
- Collections - Analogous (equivalent) to tables in SQL databases. A collection holds documents, and does not require its documents to have the same schema
- Documents - Consists of key-value pairs and are the basic unit of data in MongoDB. They are analogous to rows in an SQL table but can contain data of any type and structure.

MongoDB stores data records as Binary JSON (BSON) documents. BSON is a binary representation of JSON documents, it follows the same structure as JSON, though it contains more data types.
BSON spec - http://www.bsonspec.org/
BSON types - https://www.mongodb.com/docs/manual/reference/bson-types/


toddyuk1973
Mongo password 5qMyG9UZN223zAeK
