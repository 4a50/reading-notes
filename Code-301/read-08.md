# Notes for Read 08 - SQL

SQL - **S**tructured **Q**uery **L**anguage

**Relational Database** -a collection of related (two-dimensional) tables.

```
SELECT column
FROM myTable
WHERE conditionals
```

+ `=` 	Case sensitive exact string comparison (notice the single equals)	
    + col_name = "abc"
+ `!= or <>`	Case sensitive exact string inequality comparison	    
  + col_name != "abcd"
+ `LIKE`	Case insensitive exact string comparison
  + col_name LIKE "ABC"
+ `NOT LIKE`	Case insensitive exact string inequality comparison	col_name 
  + NOT LIKE "ABCD"
+ `%`	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	
  + col_name LIKE "%AT%" (matches "AT", "ATTIC", "CAT" or even "BATS")
+ `_`	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE)
  + col_name LIKE "AN_"  (matches "AND", but not "AN")
+ `IN (…)`  String exists in a list
  + col_name IN ("A", "B", "C")
+ `NOT IN (…)` String does not exist in a list
  + col_name NOT IN ("D", "E", "F")

+ `ORDER BY` Order the results by a given column
  + ORDER BY Title ASC
```
 
```
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;
```

```
INSERT INTO mytable
VALUES (value_or_expr, another_value_or_expr, …),
       (value_or_expr_2, another_value_or_expr_2, …),
       …;

```

Create a Table
```CREATE TABLE movies (
  id INTEGER PRIMARY KEY,
  title TEXT,
  director TEXT,
  year INTEGER,
  length_minutes INTEGER
);
```

`DROP TABLE IF EXISTS mytable;`

[&lt;--&#91;BACK&#93;](/README.md)
