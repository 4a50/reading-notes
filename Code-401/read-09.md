# Notes for Read 09 - LINQ

## LINQ
[Microsoft Docs - Linq](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/)

LINQ (Language Integrated Query) 
Useful for interfacing with a variety of other object
SQL and XML notably

## Introduction to LINQ Queries
[Microsoft Docs - Intro to LINQ](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)

There are three parts to a query operation

1. Get the Data Source
2. Create the Query
3. Execute the Query.

a source can be pretty much any collection of data.  int[] string[] List, etc

the query is made as an IEnnumerable&lt;int&gt; Doesnt have to executed right away.

Execute, is normally in the form of a ***foreach*** loop to get the data.

## Basic LINQ Query Operations
[Microsoft Docs - Basic LINQ Query Operations](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/basic-linq-query-operations)

Example of a query
```
var queryPowerUpItems = from item in powerUps
                           where item.Mushrooms == "Mega"
                           select item;
```

You can 
+ Order
+ Filter
+ Group
+ Join
+ Select

## Writing Queries in C#

Performed the walk-through in Visual Studio.

## C# In A Nutshell - LINQ



[&lt;--&#91;BACK&#93;](/README.md)