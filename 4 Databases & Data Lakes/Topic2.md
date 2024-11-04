# Schemas & Integration
## OLAP (Online Analytical Processing) vs OLTP (Online Transaction Processing) 
![image](https://github.com/user-attachments/assets/5a83d9a6-1d9f-4ab1-bc88-57adc39df819)
![image](https://github.com/user-attachments/assets/e1ebb76a-ba2b-4e41-b779-630c85dd03c0)



## Relational Models
![image](https://github.com/user-attachments/assets/64218e78-4815-402c-80ff-cb6ef4a81a5e)
  - Primary Key is a unique identifier for records in a table
  - Foreign Keys are fields in a table that match the Primary key of another table that can be linked to form relationships
![image](https://github.com/user-attachments/assets/bb1628d5-f656-4ea4-a95f-561cc70a2788)

## Schemas & Metadata
  - Star Schema One large table with 'facts' and smaller 'dimension' tables linked by keys to enable more detail
  - Snowflake Schema An extension of the star schema where dimension tables are normalized into multiple related tables, resulting in a more complex database structure that resembles a snowflake with branches radiating from  central node.
![image](https://github.com/user-attachments/assets/8ad183c0-5235-454f-9672-7c6708a59fed)
![image](https://github.com/user-attachments/assets/2665d28f-b5d4-48a0-bf63-4ab05494ae47)
## Normalised vs Denormalised
![image](https://github.com/user-attachments/assets/b6e40a31-cb7c-4f8a-a289-1b4697513b2a)


  - 
## Comparison of SQL Databases
- Understanding the nuances between different database systems is crucial for optimising data architecture. Amazon Redshift and PostgreSQL offer distinct advantages, but cater to different needs. While PostgreSQL is a widely-used open-source relational database system known for its robustness and flexibility in handling complex SQL operations, Amazon Redshift is a cloud-based data warehousing service optimised for online analytical processing (OLAP) tasks. Redshift is designed to handle large scale data analytics workflows more efficiently than PostgreSQL due to its columnar storage and parallel query execution. The importance of open-source solutions like PostgreSQL cannot be overstated. They provide transparency, flexibility, and a community-driven approach to development, which fosters innovation and provides a safety net against vendor lock-in. This open-source nature allows organisations to customise their database systems extensively according to their specific needs without the constraints imposed by proprietary software.
- However, when choosing a database solution, it is essential to consider vendor-specific differences. These can include unique features, performance optimisations, cost implications, and integration capabilities with other tools and services. For instance, Redshift integrates seamlessly with other AWS services, making it a preferable choice for businesses already embedded within the AWS ecosystem.Moreover, adherence to SQL standards plays a significant role in determining the ease of migrating and integrating data across different systems. While both Redshift and PostgreSQL support SQL, there are variations in their SQL dialects and extensions. Understanding these differences is crucial for database administrators and developers to ensure efficient data operations and to make informed decisions about which database system best meets their operational requirements and strategic goals.

## Metadata Repositories
## Data Marts
## Apache Iceberg
## SQL
- Databases i use
  - Access - Limited use of SQL, Access writes its own SQL code based on predfined functions. I have used SQL to create Union commands. Access uses JetSQL which is limited use in itself
  - https://www.devguru.com/content/technologies/jetsql/home.html
  - Access is resticted to opening locally, although can be stored on the cloud and read via other MS applications such as Power BI
  - Training is available through the companies training portal but only at a high level usage rather than developing
  - 

