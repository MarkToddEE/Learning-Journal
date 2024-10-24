# Storing and Querying data
## The Economics of Data Storage
![image](https://github.com/user-attachments/assets/5831af4f-1eea-43e6-8b2c-f9c182d2afcc)
  - Chief Data Officer
    - What they do:
    - Lead the data and analytics agenda of an organisation.
    - Establish and deliver technologies, tools, approaches and methodologies to unlock the value in enterprise data assets of an organisation.
    - Manage data as a strategic asset and operational data governance, data quality and other controls to sustain the integrity of the data of an organisation.
    - Serve as trusted partner to key business executives focused on the customer, enterprise risk management, regulatory compliance and finance.
    - Fosters innovation leveraging emerging Big Data and analytics technologies. 
## Data Marketplace
  - Data marketplaces are online platforms where individuals and organisations can buy, sell, or exchange various types of data. These platforms serve as intermediaries, connecting data providers with data consumers, and facilitating transactions between them. Data marketplaces offer a wide range of datasets, including demographic data, consumer behavior data, financial data, and more. They play a crucial role in the data economy by enabling organisations to access additional data sources to enhance their analytics, decision-making, and innovation efforts.

## Storing Files: HDFS, Key-Value Stores, Columnar – Parquet Format, Filesystems
  - Hadoop Distributed File System (HDFS)
  - This innovative approach allowed for cheap commodity storage, offering resilience by storing three copies of each file and distribution by ensuring each file resides on at least three different machines. This configuration not only provided a cost-effective solution for managing vast amounts of data but also enhanced data accessibility and analysis capabilities.
  - Key-value stores
    - Key-value stores offer a straightforward yet efficient method for storing and retrieving data based on a unique key, tailoring their approach for scenarios where quick data access is critical. Meanwhile, the Parquet format, designed for efficiency in analytic queries, employs a columnar storage strategy that significantly reduces disk I/O, facilitating faster data processing and enabling schema evolution with minimal overhead.
    - Aggregations on a per-key basis refer to the ability to perform data aggregation operations, such as summing, averaging, or counting, for each unique key in a dataset. In the context of key-value stores or similar data storage systems, each key typically corresponds to a unique identifier associated with a specific data entry. By aggregating data on a per-key basis, organisations can analyse and summarise information for individual entities or categories represented by these keys. This approach allows for granular analysis and facilitates insights into trends, patterns, or behaviors associated with each key, enabling more targeted decision-making and actionable insights.
  - Selecting a Storage Format
  - 

 
## Data Lakes
  - For high volume unstructured data
## Data Warehouse
  - Highly structured for data analysis and reporting
## Operational Data Stores (ODS)
  - Real-Time Data Processing: Operational data stores are designed for the real-time processing of transactional data, supporting day-to-day business operations. They enable the immediate availability of operational data for analysis and decision-making, acting as a bridge between transactional databases and data warehouses or data lakes.
  - 
