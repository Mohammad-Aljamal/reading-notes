# Class 03

## Data Modeling


### [nosql vs sql](thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

#### 1. What type of database is the best fit for the complex query intensive environment?
In a complex query-intensive environment, SQL databases are generally considered to be a better fit. SQL databases excel at handling structured data and complex queries that involve multiple tables and relationships. They have a well-defined schema and support powerful querying languages like SQL, which allows for efficient and optimized execution of complex queries.



#### 2. What type of database is the best fit for hierarchical data storage?
Graph databases are the best fit for hierarchical data storage among NoSQL databases. Graph databases are specifically designed to handle and represent complex hierarchical relationships efficiently. They store data in nodes and edges, making it easy to navigate and query hierarchical data structures. Graph databases excel at traversing and querying relationships, allowing for efficient retrieval and manipulation of hierarchical data. Therefore, if you are considering a NoSQL database for hierarchical data storage, a graph database is often the most suitable choice.


#### 3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend
Think of a SQL database like a traditional store with fixed sections and aisles. If more customers come in, you can add more checkout counters to handle the increased load. However, this might slow down the overall process because everyone has to go through the same checkout area.
On the other hand, a NoSQL database is like a modern store with multiple checkout counters scattered around. As the number of customers increases, you can add more checkout counters wherever it makes sense. This way, customers can go to any counter and get served quickly, without causing congestion.
In simpler terms, SQL databases scale vertically by adding more resources to a central server. It's like making the checkout area bigger. NoSQL databases, on the other hand, scale horizontally by adding more servers to share the load. It's like having more checkout counters distributed throughout the store.



### [sql modeling techniques](https://www.essentialsql.com/get-ready-to-learn-sql-7-simplified-data-modeling/)

#### 1. Among data tables, what is a one-to-many relationship and how do we “relate” them?
 One-to-many relationship is established between two tables when one record in the first table can have multiple related records in the second table. This relationship is commonly represented using a foreign key in the "many" side table that references the primary key in the "one" side table.


#### 2. Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.
create a conceptual model.



#### 3. Explain the difference between a primary and foreign key.
A primary key uniquely identifies each record in a table, while a foreign key establishes a relationship between tables by referencing the primary key of another table.



### [Video sql vs nosql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

#### 1. How do we treat keywords and parameters differently in SQL syntax?


#### 2. Define normalization within the context of schemas and data.
Normalization is the process of organizing data and designing database schemas in a way that minimizes redundancy and ensures data integrity. It involves applying a set of rules and guidelines to eliminate data anomalies and dependencies.
In the context of schemas and data, normalization aims to achieve the following goals Eliminate data redundancy, Reduce data update anomalies and Maintain data integrity



#### 3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
imagine that we have apples, oranges and bananas and we have three people (A),(B) and (C)

In one to one relation (A) just can take Apples and (B) just can take oranges and (C) he just can take bananas

In one to many
all of the three person can take appales but not all of them can take the other fruits

In many to many
all of the three person can take any type of this fruits

