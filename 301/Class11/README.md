# MongoDB and Mongoose

## nosql vs sql
1. List five differences between SQL and NoSQL databases:
    - SQL
        1. SQL databases are primarily relational databases that store data in tables.
        2. SQL databases have a predefined schema, meaning the structure and relationships between tables are well-defined.
        3. SQL databases use structured query language (SQL) for defining and manipulating the data.
        4. SQL databases are vertically scalable, meaning they can handle increased load by increasing the resources (CPU, RAM) of a single server.
        5. SQL databases are a good fit for complex query-intensive environments and support powerful queries.
    - NoSQL
        1. NoSQL databases are primarily non-relational or distributed databases that can take various forms such as document-based, key-value pairs, graph databases, or wide-column stores.
        2. NoSQL databases have a dynamic schema, meaning they do not have strict schema definitions and can handle unstructured data.
        3. NoSQL databases have different query languages specific to each database type, such as UnQL (Unstructured Query Language).
        4. NoSQL databases are horizontally scalable, meaning they can handle increased load by adding more database servers to the pool of resources.
        5. NoSQL databases are not as suitable for complex queries compared to SQL databases, as they lack standard interfaces for performing complex queries.
 	 	 
2. What kind of data is a good fit for an SQL database?
    - Structured data with well-defined relationships between entities is a good fit for an SQL database. 
3. Give a real world example.
    - An example of data that is a good fit for an SQL database is an e-commerce application that needs to store information about customers, orders, products, and inventory. The structured nature of the data and the relationships between entities can be easily represented using tables in an SQL database.
4. What kind of data is a good fit a NoSQL database?
    - Unstructured or semi-structured data that can vary in its schema or does not fit well into a tabular structure.
5. Give a real world example.
    - A real-world example of data that is a good fit for a NoSQL database is a social media platform that needs to store user profiles, posts, comments, and relationships between users. The flexibility of NoSQL databases allows for easy storage and retrieval of varying and evolving data structures.
6. Which type of database is best for hierarchical data storage?
    - NoSQL databases, particularly graph databases, are well-suited for hierarchical data storage. 
7. Which type of database is best for scalability?
    - NoSQL databases are typically better suited for scalability, particularly horizontal scalability

## sql vs nosql (Video)

1. What does SQL stand for?
    - Structured Query Language

2. What is a relational database?
    - A type of database that organizes data into tables with predefined relationships between them. It consists of a collection of related tables, each having a unique identifier (primary key), and the relationships between tables are defined using foreign keys.

3. What type of structure does a relational database work with?
    - structured or tabular data models

4. What is a ‘schema’?
    -  The logical structure or blueprint that defines the organization of data in the database. It defines the tables, fields, relationships, constraints, and other properties of the database.

5. What is a NoSQL database?
    -"Not only SQL," is a type of database that provides a flexible and scalable approach to storing and retrieving data. NoSQL databases do not rely on a fixed schema and allow for unstructured or semi-structured data storage.

6. How does it work?
    - NoSQL databases use various data models to store and retrieve data, such as key-value pairs, column-oriented, document-oriented, or graph databases.

7. What is inside of a MongoDB database?
    - Data is organized into collections, which are similar to tables in a relational database. Each collection contains multiple documents, and each document is a set of key-value pairs. Documents in MongoDB are stored in a binary format called BSON (Binary JSON), which allows for efficient storage and retrieval.

8. Which is more flexible - SQL or MongoDB? and why.
    - MongoDB is generally considered more flexible than SQL (relational databases) because it allows for dynamic and schema-less data modeling.
    
9. What is the disadvantage of a NoSQL database?
    - One disadvantage of NoSQL databases is the potential loss of data consistency.


    