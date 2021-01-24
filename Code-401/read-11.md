# Notes for Read 11 - ERD (Entity Relationship Diagram)?

## Database Concepts
[Microsoft Docs - Data Models](https://docs.microsoft.com/en-us/aspnet/core/data/ef-mvc/complex-data-model?view=aspnetcore-2.0)

[TutorialsPoint - DBMS](https://www.tutorialspoint.com/dbms/dbms_overview.htm)

Database Schema:
**What is a Schema?**

+ A schema is how the database is represented.  Shows how it is organized.

**Why do we use them?**

A schema defines what all of the entities are and that their relationship is to one another.

**What do they look like?**

Look like a hierarchal cascade of interrelating data.  

There is a phycical side <- is the actual stroage of the data

And there is a logical side <- Defines all the constraints.


**What are the different types of Database Keys?**
+ Primary Key
+ Candidate Key
+ Super Key
+ Alternate key
+ Composite or Compound Key
+ Unique Key
+ Foreign Key

**What is a Primary Key?**

It is the key in the table that identifies it.  There is only one per table.  Must be unique

**What is a Foreign Key?**

This is a key that two databases can share to associate with each other

**What is a Composite Key?**

Combo of one or more columns that can uniquely identify records on that table

**How are they different?**

A foriegn key allows different table to share the relationships with each other.

**When do you use 1 over the others?**

Primary Key must be used, Identifies the table.

Foriegn Key where you need data from one table to reference data in another

Composite Key wher you want to identigy a collection of columns in a table

**What are Relationships in a relational database?**

Relationships are the way you can call diffent data from table and present them in a useful way.

**What is a 1:1 relationship?**

Both tables can only share one record per table together.

**What is a Many:Many relationship?**

You can relate as many records as you want in the other table.

**How about a 1: Many or a Many:1?**

A *1:Many* or *Many:1* allows on record to relate to any number of records in another table





[&lt;--&#91;BACK&#93;](/README.md)