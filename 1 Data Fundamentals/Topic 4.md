# Introduction to reliable data architectures

## Unlocking data architecture success with diagrams

  - Unified modelling language (UML) diagrams
    ![image](https://github.com/user-attachments/assets/a355cb5d-c664-4ab1-9912-922d3be3e792)
  
    ### Sequence Diagrams
      - Visualising interactions - Sequence diagrams offer a clear visual representation of how different components work together, simplifying the understanding of complex systems.
      - Enhancing communication - These diagrams improve communication by detailing the sequence of interactions, the roles of the participants, and the nature of the messages exchanged.
      - Validation - Sequence diagrams act as a blueprint for project validation, ensuring that the system or process operates as designed.
        
![image](https://github.com/user-attachments/assets/71ffc118-64ca-487c-819a-8eb11358e0db)

  ### Use Case Diagram
  - Use case diagrams play a crucial role in system analysis and design by providing a visual representation of user-system interactions, aiding in communication between stakeholders, and guiding the development process towards building a system that fulfils user requirements effectively.

  ![image](https://github.com/user-attachments/assets/aa63eb0c-d480-463e-9854-f8b8031e1505)

  ### Entity relationship diagram (ERD)
  
  ![image](https://github.com/user-attachments/assets/2b457328-46e2-473c-8f00-7ebde3088ec2)

  ### Logical Overview
   -  Logical diagrams are designed to illustrate the high-level flow of data within our system without referencing any specific vendors.
   -  They focus on depicting the structure of data across different stages, providing a conceptual overview of how information moves through our architecture. 
![image](https://github.com/user-attachments/assets/bd755b71-b588-4965-aa26-46d33a82efc0)
  ### Solution Diagram
   - A solution diagram provides a more detailed representation of our system architecture, including specific vendor solutions or platforms.
   - It highlights the exact systems and technologies involved at each stage of data processing, offering a more concrete view of our solution landscape. 
    ![image](https://github.com/user-attachments/assets/5f884dda-a8a7-42c2-8dcb-c758ca20a937)

# Layered Architecture
![image](https://github.com/user-attachments/assets/a74704e2-ada0-4d6c-85a7-feb6636f65ad)

## Data Storage Layer
  - This layer is where all the data utilised by the system is stored, encompassing both structured and unstructured data like text, images, and video. It is commonly managed using a relational database management system (RDBMS), a NoSQL database, or a data lake.
  - Scalability: Separating data storage from processing allows the system to scale more efficiently to handle larger volumes of data.
  - Security: It is possible to secure the data storage layer independently, which helps mitigate the risk of unauthorised access.
  - Data integrity: The data storage layer maintains data consistency and accuracy by enforcing data integrity constraints like unique keys and foreign key relationships.
## Data Processing Layer
  - This layer handles operations on the data, such as filtering, sorting, aggregation, and transformation. It typically uses data processing frameworks like Apache Spark or Apache Flink, or stream processing engines like Apache Kafka.
  - Performance: By processing data in parallel, this layer can achieve high throughput and low latency.
  - Flexibility: The data processing layer supports a diverse range of data processing tasks, from simple filtering to complex machine learning algorithms.
  - Resilience: It provides fault tolerance and automatic recovery, helping the system handle failures smoothly and stay operational.
## Data Presentation Layer
  - The data presentation layer is responsible for displaying the data to end-users in a useful manner, this layer is usually implemented through a web application or business intelligence tools like Tableau or Power BI.
  - Usability: A user-friendly interface makes it straightforward for end-users to interact with the data and gain insights.
  - Customisation: The presentation layer can be tailored to meet a wide array of use cases and user preferences, offering a flexible and adaptable interface.
  - Integration: It can integrate with other applications and services to provide a seamless user experience, enabling users to utilise the data across different contexts.

# Microservices architectures
  - Decentralised services - Each service is a separate codebase, managed by a small development team, allowing for faster development cycles and easier maintenance.
  - Independent deployment - Services can be updated and deployed independently, without impacting the rest of the application, enabling faster bug fixes and feature releases.
  - Polygot programming - Services can be written in different programming languages and technologies, allowing teams to choose the best tools for their specific needs.
  - Scalability - Individual services can be scaled independently based on demand, optimising resource utilisation and improving cost-efficiency.
  - Fault isolation - If one service fails, it does not bring down the entire application, ensuring better resilience and availability.
  - API Gateway - The API gateway acts as a single-entry point for clients, decoupling them from the internal services and enabling cross-cutting concerns like authentication, logging, and load balancing.
# Designing data products visually
  - Data Product -valuable assets created by transforming raw data into actionable insights, tools, or services that deliver tangible value to the organisation and its stakeholders.
    - Dahboards - Visual interfaces that display key metrics, KPIs, and trends in real-time, allowing stakeholders to monitor performance and make data-driven decisions.
    - Reports - Detailed analyses and summaries of data, often presented in written or visual formats, to provide insights into specific business areas or trends.
    - APIs - Interfaces that allow different software applications to communicate and exchange data, enabling seamless integration and automation of processes.
    - Data Feeds - Streams of raw or processed data delivered in real-time or batch mode, often used for analytics, machine learning, or feeding other systems and applications.
   
## Visual Modelling
  - Wireframes
    - Purpose: Provide a basic structural outline of the data product, emphasising functionality over aesthetics.
    - Example: A wireframe for an HR dashboard shows the arrangement of elements and user interactions without detailed styling.
  - Mockups
    - Purpose: Add aesthetic elements like colour schemes and fonts to wireframes, offering stakeholders a more realistic view of the final product.
    - Example: A mockup of the HR dashboard includes colour, typography, and preliminary interactive designs.
  - Prototypes
    - Purpose: Simulate user interactions with the product, instrumental in identifying usability issues before final development.
    - Use in usability testing: Central to testing user interactions and behaviours, providing insights for improvement.
    - 
# Navigating data seas with architectural governance

  - The Open Group Architecture Framework (TOGAF) serves as a governance framework that ensures alignment with business goals, compliance with regulatory requirements, and promotes standardisation in data architecture. 
  - Usage patterns - Understanding how different user groups interact with the system aids in designing user-centric architectures.
  - Data flow - Visualising how data moves through systems identifies potential bottlenecks and security risks.
  - Physical setup - Considering the physical deployment of resources impacts performance, redundancy, and disaster recovery strategies.
  - Networking - Outlining network topologies and protocols ensures efficient data transfer and compliance with security policies.
  - Integrating these features enhances data governance as follows:
  ![image](https://github.com/user-attachments/assets/73f77e03-a2f8-4472-a49b-1f55fd7ea273)

  - Diagrams should enforce and track compliance with both internal policies and external regulations, as follows:
      - Illustrating compliance checkpoints: Showing where and how compliance checks are integrated within the architecture
      - Role-based access control: Mapping out data access permissions ensures only authorised personnel can access sensitive data, supporting compliance with data protection regulations
      - Security protocols: Visualising security mechanisms reinforces the system’s defence against breaches.


  # Summary
  - Diagrams act as visual maps to simplify complexity and promote alignment among teams in project management
  - Sequence diagrams are a type of UML diagram used to visualise the timing and interactions between components within a system
  - Use case diagrams provide a visual representation of how users interact with a system, aiding in understanding functional requirements
  - Entity Relationship Diagrams (ERDs) illustrate the relationships between different data entities within an application or database
  - In a three-layered data architecture:
    - Data storage layer uses databases or data lakes for data persistence
    - Data processing layer uses frameworks like Apache Spark for operations like filtering, sorting, transformation
    - Presentation layer displays data to end-users via dashboards or reports
  - A microservices architecture breaks down an application into small, independent services focused on specific business capabilities that can be developed, deployed, and scaled independently
  - The API gateway acts as the entry point for clients in a microservices architecture, decoupling them from internal services and enabling cross-cutting concerns like authentication and logging
    

