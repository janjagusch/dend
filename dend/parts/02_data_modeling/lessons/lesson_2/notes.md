## Lesson 2 - Relational Data Models

### Databases
- Database: a set of related data and the way it is organized.  
- Database Management System: a software that gives users and applications access to the database.  

### Importance of Relational Databases
- E. Codd, 1970, 12 rules for relational systems:
- Standardization of data models: allow for querying it with SQL.
- Flexibility: when it comes to adding, altering or removing data.  
- Data integrity: ACID.
- SQL.  
- Simplicity.  
- Intuition.  

### OLAP vs. OLTP  
- Online Analytical Processing: allows for analytics and ad-hoc queries. Mostly read queries. Large aggregations.
- OLTP: less complex queries in large volumes. Read, insert, update and delete queries. Little aggregations.  

### Structuring the Database: Normalization
- Normalization: reduce data redundancy, increase data integrity. Enforce constraints, have one source of truth.
- Denormalization: must be done if you do read-heavy workloads to increase performance.  

### Objectives of Normal Form
- Free database from redundant insertions, updates & deletions. Only do it in one place.
- Reduce need to refactor the database over time.  
- Make sense to users.  
- Make database neutral to queries.  

### Normal Forms
- 1NF:
  - Atomic values: each cell contains unique and single values. No sets, collections or lists.  
  - Add columns without altering tables.  
  - Separate different relations into different tables.
  - Keep relationships together with foreign keys.  
- 2NF:
  - Have reached 1NF.
  - All columns in the table must rely on the primary key.
- 3NF:  
  - Have reached 2NF.
  - No transitive dependencies.  
- Goes up to 6NF...  

### Fact and Dimension Tables
- Together they create an organized data model.  
- Fact tables:
  - Measurement, metrics of business processes.
  - Example, how much does a customer spend?
  - They normally store numbers.
- Dimension tables:
  - Categorizes facts in order to enable users to answer business questions.
  - Answering the when, where, what questions.
- Popular schemas: star schema, snowflake schema.

### Star Schemas
- Simplest style of data mart schemas.
- One or more fact tables referencing any number of dimension tables.

### Benefits of Star Schemas
- Benefits:
  - Denormalized
  - Simplifies queries.
  - Fast aggregations.
- Drawbacks:
 - Data integrity.
 - Decrease query flexibility.
 - Many to many  

### Snowflake Schemas
- More complex than star schema.
- Allows for many-to-many relationships.
- More normalized than star schema.

### Data Definitions and Constraints
- NOT NULL: value cannot be empty (useful for composite key).  
- UNIQUE: needs to be unique.
- PRIMARY KEY: not null and unique.  

### Upsert
- Inserting a new row in an existing table or updating row.
- ON CONFLICT
