# class 3

## Readings: Data Modeling & NoSQL Database


## Name 3 advantages to Test Driven Development


1. Better program design and higher code quality
2. Detailed project documentation

3. TDD reduces the time required for project development
It’s widely known that applications created with Test Driven Development take longer than ones created without TDD. Some sources mention the difference of about 30 percent.

## n what case would you need to use beforeEach() or afterEach() in a test suite?


**beforeEach()** Using these two functionalities, we can execute some pieces of code before and after execution of each spec.

 This functionality is very useful for running the common code in the application.

**afterEach()** is run after each test in a descriptive and used to clean up stuff like a close opened file.

## What is one downside of Test Driven Development?

- Big time investment. For the simple case you lose about 20% of the actual implementation, but for complicated cases you lose much more.

- Additional Complexity. For complex cases your test cases are harder to calculate, I'd suggest in cases like that to try and use automatic reference code that will run in parallel in the debug version / test run, instead of the unit test of simplest cases.

- Design Impacts. Sometimes the design is not clear at the start and evolves as you go along - this will force you to redo your test which will generate a big time lose. I would suggest postponing unit tests in this case until you have some grasp of the design in mind.

# Which 3 things had you heard about previously and now have better clarity on?

1. functional programming 
2.  pure function
3. class

# Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

1. immutable state
2. higher-order function
3. Test Driven Development (TDD)

# What are you most excited about trying to implement or see how it works?

unit test

# SQL vs NoSQL Database Differences

1-SQL vs NoSQL: High-Level Differences
- SQL databases are primarily called as Relational Databases (RDBMS); whereas NoSQL database are primarily called as non-relational or distributed database.

- SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.

- SQL databases have predefined schema whereas NoSQL databases have dynamic schema for unstructured data.

- SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware. NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.

## SQL Database Examples

1. MySQL Community Edition

MySQL database is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js. The following are some of MySQL benefits and strengths:

- Replication: By replicating MySQL database across multiple nodes the work load can be reduced heavily increasing the scalability and availability of business application
Sharding: MySQL sharding os useful when there is large no of write operations in a high traffic website. By sharding MySQL servers, the application is partitioned into multiple servers dividing the database into small chunks. As low cost servers can be deployed for this purpose, this is cost effective.

- Memcached as a NoSQL API to MySQL: Memcached can be used to increase the performance of the data retrieval operations giving an advantage of NoSQL api to MySQL server.

- Maturity: This database has been around for a long time and tremendous community input and testing has gone into this database making it very stable.


- Wide range of Platforms and Languages: MySql is available for all major platforms like Linux, Windows, Mac, BSD and Solaris. It also has connectors to languages like Node.js, Ruby, C#, C++, C, Java, Perl, PHP and Python.

Cost effectiveness: It is open source and free.

2. MS-SQL Server Express Edition
It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft. The following are some of MS-SQL benefits and strengths:

- Integrated Development Environment: Microsoft visual studio, Sql Server Management Studio and Visual Developer tools provide a very helpful way for development and increase the developers productivity.

3. Oracle Express Edition
It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment. The following are some of Oracle benefits and strengths:

- Easy to Upgrade: Can be easily upgraded to newer version, or to an enterprise edition.

## NoSQL Database Examples

1. MongoDB

Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks. The following are some of MongoDB benefits and strengths:

- Speed: For simple queries, it gives good performance, as all the related data are in single document which eliminates the join operations.

## NOSQL DATA MODELING TECHNIQUES


NoSQL databases are often compared by various non-functional criteria, such as scalability, performance, and consistency.

 This aspect of NoSQL is well-studied both in practice and theory because specific non-functional properties are often the main justification for NoSQL usage and fundamental results on

 distributed systems like the CAP theorem apply well to NoSQL systems.  At the same time, NoSQL data modeling is not so well studied and lacks the systematic theory found in relational databases.
 
  In this article I provide a short comparison of NoSQL system families from the data modeling point of view and digest several common modeling techniques.

## General Notes on NoSQL Data Modeling

The rest of this article describes concrete data modeling techniques and patterns. As a preface, I would like to provide a few general notes on NoSQL data modeling:

- NoSQL data modeling often starts from the application-specific queries as opposed to relational modeling:

Relational modeling is typically driven by the structure of available data. The main design theme is  **“What answers do I have?**” 
- NoSQL data modeling is typically driven by application-specific access patterns, i.e. the types of queries to be supported.

 The main design theme is **“What questions do I have?”**

 ## Conceptual Techniques

 This section is devoted to the basic principles of NoSQL data modeling.

- Denormalization

**Denormalization** can be defined as the copying of the same data into multiple documents or tables in order to simplify/optimize query processing or to fit the user’s data into a particular data model.

 Most techniques described in this article leverage denormalization in one or another form.

In general, denormalization is helpful for the following trade-offs:

Query data volume or IO per query VS total data volume. 

Using denormalization one can group all data that is needed to process a query in one place. This often means that for different query flows the same data will be accessed in different combinations. Hence we need to duplicate data, which increases total data volume.

Processing complexity VS total data volume. Modeling-time normalization and consequent query-time joins obviously increase complexity of the query processor, especially in distributed 


**Aggregates**

All major genres of NoSQL provide soft schema capabilities in one way or another:

Key-Value Stores and Graph Databases typically do not place constraints on values, so values can be comprised of arbitrary format. 

It is also possible to vary a number of records for one business entity by using composite keys. For example, a user account can be modeled as a set of entries with composite keys like UserID_name, UserID_email, UserID_messages and so on. If a user has no email or messages then a corresponding entry is not recorded.

BigTable models support soft schema via a variable set of columns within a column family and a variable number of versions for one cell.

**Application Side Joins**

Joins are rarely supported in NoSQL solutions. As a consequence of the “question-oriented” NoSQL nature, joins are often handled at design time as opposed to relational models where joins are handled at query execution time. Query time joins almost always mean a performance penalty, 

but in many cases one can avoid joins using Denormalization and Aggregates, i.e. embedding nested entities. Of course, in many cases joins are inevitable and should be handled by an application. The major use cases are:

Many to many relationships are often modeled by links and require joins.

## General Modeling Techniques

** Atomic Aggregates**
Many, although not all, NoSQL solutions have limited transaction support. In some cases one can achieve transactional behavior using distributed locks or application-managed MVCC, but it is common to model data using an Aggregates technique to guarantee some of the ACID properties.

** Nested Documents Flattening**: 
 
 Numbered Field Names
Search Engines typically work with flat documents, i.e. each document is a flat list of fields and values.

 The goal of data modeling is to map business entities to plain documents and this can be challenging if the entities have a complex internal structure. One typical challenge mapping documents with a hierarchical structure, i.e. documents with nested documents inside.

 ![](https://highlyscalable.files.wordpress.com/2012/02/nested-documents-1.png)