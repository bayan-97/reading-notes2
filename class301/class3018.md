# SQL

![](https://sqlbolt.com/cs/images/favicon.pngS)

**SQL, or Structured Query Language,** is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications.

**To retrieve data from a SQL database,** we need to write SELECT statements, which are often colloquially refered to as queries. A query in itself is just a statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned. It has a specific syntax though, which is what we are going to learn in the following exercises.

As we mentioned in the introduction, you can think of a table in SQL as a type of an entity (ie. Dogs), and each row in that table as a specific instance of that type (ie. A pug, a beagle, a different colored pug, etc). This means that the columns would then represent the common properties shared by all instances of that entity (ie. Color of fur, length of tail, etc).


``SELECT column, another_column, …``
``FROM mytable;``


The result of this query will be a two-dimensional set of rows and columns, effectively a copy of the table, but only with the columns that we requested.


Now we know how to select for specific columns of data from a table, but if you had a table with a hundred million rows of data, reading through all the rows would be inefficient and perhaps even impossible.

In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

``SELECT column, another_column, …``
``FROM mytable``
``WHERE condition``
    ``AND/OR another_condition``
   `` AND/OR …;``

   When writing WHERE clauses with columns containing text data, SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching. 

   ## Filtering and sorting Query results


   Even though the data in a database may be unique, the results of any particular query may not be – take our Movies table for example, many different movies can be released the same year. 
   
   In such cases, SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword.

   ``SELECT DISTINCT column, another_column, …``
``FROM mytable``
``WHERE condition(s);``
## Database normalization


**Database normalization** is useful because it minimizes duplicate data in any single table, and allows for data in the database to grow independently of each other (ie. Types of car engines can grow independent of each type 

of car). As a trade-off, queries get slightly more complex since they have to be able to find data from different parts of the database, and performance issues can arise when working with many large tables.

In order to answer questions about an entity that has data spanning multiple tables in a normalized database, we need to learn how to write a query that can combine all that data and pull out exactly the information we need.

### Multi-table queries with JOINs

Tables that share information about a single entity need to have a primary key that identifies that entity uniquely across the database. One common 

primary key type is an auto-incrementing integer (because they are space efficient), but it can also be a string, hashed value, so long as it is unique.

Using the JOIN clause in a query, we can combine row data across two separate tables using this unique key. The first of the joins that we will introduce is the INNER JOIN.

``SELECT column, another_table_column, …``
``FROM mytable``
``INNER JOIN another_table ``
    ``ON mytable.id = another_table.id``
``WHERE condition(s)``
``ORDER BY column, … ASC/DESC``
``LIMIT num_limit OFFSET num_offset;``


### OUTER JOINs
Depending on how you want to analyze the data, the INNER JOIN we used last lesson might not be sufficient because the resulting table only contains data that belongs in both of the tables.

If the two tables have asymmetric data, which can easily happen when data is entered in different stages, then we would have to use a LEFT JOIN, RIGHT JOIN or FULL JOIN instead to ensure that the data you need is not left out of the results.

``SELECT column, another_column, …``
``FROM mytable``
``INNER/LEFT/RIGHT/FULL JOIN another_table ``
    ``ON mytable.id = another_table.matching_id``
``WHERE condition(s)``
``ORDER BY column, … ASC/DESC``
``LIMIT num_limit OFFSET num_offset;``


