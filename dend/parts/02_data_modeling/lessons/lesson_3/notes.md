# Lesson 3 - NoSQL Data Models

## Non-Relational Databases
- NoSQL = Not Only SQL = Non-Relational Databases
- High availability, large amounts of data, horizontal scalability, low latency, fast read and writes.
- Apache Cassandra: created by Facebook in 2010.

## Distributed Databases
- In order to have high availability, you need data redundancy.
- Distributed: a database made of many individual nodes/ systems/ machines.  
- Eventual consistency: data might not be updated in all locations.

## CAP Theorem
- Consistency: every read from the database gets the latest piece of data or an error.
- availability: every request is received and a response given - without a guarantee that the data is the latest update.
- Partition tolerance: the system continues to work regardless of losing network connectivity between nodes.
- NoSQL: Mostly AP, not C.

## Denormalization in Apache Cassandra
- Think about your queries first!
- There are no JOINS.
- Denormalization is a must.
- AP has been optimized for fast writes.
- One table per query.

## Cassandra Query Language: CQL
- Similar to SQL but
  - No JOINS
  - NO GROUP BYs

## Primary Key
- Primary Key = Partition Key + Clustering Columns
- The partition key will determine on which node the record is stored.

## Clustering Columns
- Determine the sort order within a partition.
- Needs to be in the same order in the SELECT statement.

## WHERE Clause
