# Data Modeling

## Lesson 1 - Introduction to Data Modeling
### Introduction to the Course
- Database: a structured, electronic repository, where data can be stored, updated or deleted.  
- Database Management System: a software to access databases for users and applications.
### What is Data Modeling?
- Data Modeling: an abstraction that organizes elements of data and how they relate to each other.
- Strong relation to business, as we try to model data based upon business logic.
- Starting with concept, going to logic and ending up with physical data modeling.
- DDL: data definition language.
### Why Data Modeling is Important?
- Only well-thought out and well-structured data can be used for later purposes.
- Flexibility is important, as data structures might change over time.
### Who does this type of work?
- Anyone who is involved in the process of working with data.
### Introduction to Relational Databases
- Organizes data into one or more tables of columns and rows with a unique key. identifying each row.
- Invented by IBM (E. Codd, 1970).
- SQL (Structured Query Language): language to process relational databases.
### When to use a relational database?
- SQL is easy to use.
- You can join tables.
- You can aggregate.
- Useful for small data.
- Query flexibility.
- You can index columns for speeding up queries.
- ACID transactions.
### ACID transactions
- Guarantees validity even in the event of errors.
- Multiple steps/ operations = one transaction.
- Atomicity: the whole transaction is processed, or nothing is processed.
- Consistency: only transactions that follow constraints and rules are written into the database.
- Isolation: transactions are processed independently - order does not matter.
- Durability: completed transactions are saved to the database, even in cases of system failure (once it is committed).
### When not to Use a Relational Database?
- When you have large amounts of data.
- When your data is very heterogeneous.
- When you need high throughput or fast reads.
- When you need a flexible schema.
- When you need high availability.
    - Relational databases always have a single points of failure.
- When you need to scale horizontally (when you want to add more nodes to increase performance)
  - Relational databases can only scale vertically.
### What is PostgreSQL?
- Open-source, object-relational database system, built upon SQL.
### Demos: Creating a Table with PostgreSQL.
- They use psycopg2.
- You need to commit after every transaction.
- You can also set autocommit to True.
### NoSQL Databases
- NoSQL = Not Only SQL.
- Has a simpler design.
- Has simpler horizontal scaling.
- Common types: Apache Cassandra, MongoDB, DynamoDB, Apache HBase, Neo4J.
- Apache Cassandra terms:
 - Keyspace: collection of tables.
 - Partition: collection of rows. How the data is distributed.  

### What is Apache Cassandra?
- Scalability.
- High availability.
