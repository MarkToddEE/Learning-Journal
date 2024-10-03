# Introduction to Data Quality
![image](https://github.com/user-attachments/assets/b7d9ab18-c469-417a-8124-416d10f530b8)

# FAIR data standard

![image](https://github.com/user-attachments/assets/6057bac4-c842-4d4d-93e7-48c8f03b11fe)
- ![image](https://github.com/user-attachments/assets/db8696c0-7d6c-4855-8590-b738ea746ad4)
- ![image](https://github.com/user-attachments/assets/8ba3fcee-9b9b-4700-9169-f66939b09069)
- ![image](https://github.com/user-attachments/assets/a154ac47-d711-4647-8e5a-e34c1b1c0e6a)
- ![image](https://github.com/user-attachments/assets/c28a0cb1-8302-4dc8-a926-2dca088dc607)

- Metadata plays a key role in data management. OpenMetadata, an open standard, serves as a toolkit for creating detailed metadata maps. These maps, akin to navigational aids on a map, provide data engineers and users with crucial information about data's meaning, origin, context, and constraints.
# Other Example standards
  - Open Banking Standards
  - The NHS Digital Interoperability Toolkit
  - UK Data Service - https://ukdataservice.ac.uk/learning-hub/research-data-management/collaborative-research/standards/

# Dublin Core Metadata Initiative


# Challenges of Unstanardised data
![image](https://github.com/user-attachments/assets/8d7ef0d3-b932-466c-9ee4-b5cc9ae8571c)

# Data Formats
![image](https://github.com/user-attachments/assets/12a89e4d-7106-4328-bf6e-d047ed809fe4)
  - Structured Data
    - ![image](https://github.com/user-attachments/assets/e3f55219-3ffa-47a1-bfc1-64c765435344)
    - Data with a defined data type, format, and structure. Mostly in the form of tables. Examples include relational databases, CSVs, and spreadsheets. 
  - Unstructured data
    - ![image](https://github.com/user-attachments/assets/82747598-52ef-4a71-ad51-b55333824b8c)
    - Data that has no inherent structure and is usually stored as different types of files such as text documents, PDFs, images, and video. 
  - Semi Structured
    -  Textual data files with a discernable pattern that allows them to be parsed easily. Examples include XMLs and JSONs. 

# Extensible Markup Language (XML)
  - ![image](https://github.com/user-attachments/assets/4aa8127b-b4dc-42a6-a40f-482788214fa0)
  - Strengths
    - ![image](https://github.com/user-attachments/assets/e66bcbb4-d20c-4048-9c42-97689311587e)
  - Weaknesses
    - ![image](https://github.com/user-attachments/assets/767598cc-096a-4c14-8f5b-efb1deddd039)
- Challenges
- 1. Parsing Errors
  - Parsing errors occur when XML documents have improper structure or syntax, leading to failures during parsing, which is the process of converting XML data into a usable format.
  - These errors can result from missing or mismatched tags, incorrect nesting of elements, or invalid characters.
  - To mitigate these issues, it's essential to validate XML documents against predefined schemas, use robust XML parsers, implement error handling mechanisms, sanitise data before parsing, and conduct regular testing and validation.
  2. Character encoding
  - Character encoding issues arise when XML documents contain characters that are not properly encoded or use inconsistent encoding schemes.
  - This can lead to data corruption, rendering issues, or difficulties in processing the XML data correctly.
  - It's crucial to ensure consistent and appropriate character encoding to maintain data integrity.
  - To mitigate character encoding issues in XML documents, several measures can be taken, including:
      1. Standardise character encoding: Use a consistent character encoding scheme throughout XML documents, such as UTF-8 or UTF-16, to ensure compatibility across different systems and platforms
      2. Encode special characters: Properly encode special characters, such as &, <, >, ", and ', using their corresponding character entities (&, <, >, ", and ') to prevent parsing errors and data corruption
      3. Validate encoding: Validate XML documents to ensure that character encoding declarations match the actual encoding used within the document. This helps detect and correct inconsistencies or mismatches in encoding
  3. Schema Validation
  - Schema validation involves verifying that XML documents adhere to a predefined schema or structure, which defines the allowable elements, attributes, and their relationships.
  - Non-compliance with the schema can lead to data inconsistency, interoperability issues, and errors during data processing.
  - Adhering to a defined schema helps maintain data consistency and ensures compatibility with other systems or applications that rely on the XML data.
# Comma-Separated Values (CSV)
  - Strengths
    - ![image](https://github.com/user-attachments/assets/8af10074-c067-45b8-8b27-7936fea08ce9)
  - Weaknesses
    - ![image](https://github.com/user-attachments/assets/0596173c-1ff7-4170-bfe0-47c16b236c14)
  - Challenges
  - 1. Inconsistent formats
    - Inconsistencies in delimiters, encapsulators, or line terminators across CSV files can disrupt data parsing and interpretation.
    - To mitigate this challenge and data quality issue you can standardise the use of delimiters, encapsulators, and line terminators across all CSV files.
    - Implement robust parsing algorithms capable of handling variations in formats. 
    2.  Data type mismatch
    - The absence of explicit data types in CSV files can result in misinterpretation of data, leading to incorrect analysis.
    - To mitigate this challenge and data quality issue you can provide metadata or schema information alongside CSV files to specify data types.
    - You can also perform data validation and type casting during parsing to ensure consistency.
    3. Header Misalignment
    - Missing or misaligned headers in CSV files can lead to errors in data mapping and processing.
    - To mitigate this challenge and data quality issue its important to ensure that all CSV files have consistent headers and alignment.
    - Implement error handling mechanisms to detect and rectify header misalignment issues.  
# JavaScript Object Notation (JSON)
  - A lightweight data interchange format that offers simplicity and efficiency. It facilitates human readability and machine parsing while providing flexibility in data structuring through key-value pairs and arrays.
  - JSON has become the preferred data format for web applications and Application Programming Interfaces (APIs) due to its simplicity, flexibility, and compatibility with JavaScript. It is widely used for transmitting data between a server and a web application, making it an integral part of modern web development.
  - 

   
      





