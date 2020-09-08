# Database Normalization

**Database normalization**is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included.

 Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:

 - Identify salespeople in your organization

- List all customers your company calls upon to sell a product

- Identify which salespeople call on specific customers.

There are three normal forms most databases adhere to using. 

 As tables satisfy each successive database normalization form, they become less prone to database modification anomalies and more focused toward a sole purpose or topic.
 
  Before we move on be sure you understand the definition of a database table.

  # Reasons for Database Normalization

  There are three main reasons to normalize a database.  
  
  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 

  As we go through the various states of normalization we’ll discuss how each form addresses these issues, but to start, let’s look at some data which hasn’t been normalized and discuss some potential pitfalls. 

I think once you understand the issues, you better appreciate normalization. Consider the following table:

![](https://www.essentialsql.com/wp-content/uploads/2014/06/FirstNormalFormUnormalized-1.png?ezimgfmt=ng:webp/ngcb8)




The first thing to notice is this table serves many purposes including:

Identifying the organization’s salespeople
- Listing the sales offices and phone numbers
- Associating a salesperson with an sales office
- Showing each salesperson’s customers
- As a DBA this raises a red flag.  In general I like to see tables that have one purpose.  Having the table serve many purposes introduces many of the challenges; namely, data duplication, data update issues, and increased effort to query data.

## Data Duplication and Modification Anomalies

Anomalies
Notice that for each SalesPerson we have listed both the SalesOffice and OfficeNumber. There are duplicate salesperson data. Duplicated information presents two problems:

- It increases storage and decrease performance.
- It becomes more difficult to maintain data changes.

## Update Anomaly
In this case we have the same information in several rows. 
For instance if the office number changes, then there are multiple updates that need to be made.  
If we don’t update all rows, then inconsistencies appear.

## Deletion Anomaly

![](https://www.essentialsql.com/wp-content/uploads/2014/06/Intro-Deletion-Anomaly-e1425554658757.png?ezimgfmt=ng:webp/ngcb8)

Deletion of a row causes removal of more than one set of facts.  For instance, if John Hunt retires, then deleting that row cause us to lose information about the New York office.

### Definition of Database Normalization

There are several additional forms, such as BCNF, but I consider those advanced, and not too necessary to learn in the beginning.

The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form. Before we discuss the various forms and rules in detail, let’s summarize the various forms:

- First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.


- Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.


- Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key
If the rules don’t make too much sense, don’t worry. I’ve linked to article to help you understand them.



For now it’s important to understand there are three rules for database normalization that upon each other.  Some people make database normalization seem complicated.

