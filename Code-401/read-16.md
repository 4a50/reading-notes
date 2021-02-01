# Notes for Read 16 - Refactoring with DTO
# Data Transfer Objects

## Create DTOs 
[Microsoft Docs - Create DTOs](https://docs.microsoft.com/en-us/aspnet/web-api/overview/data/using-web-api-with-entity-framework/part-5)

A DTO is an object that defines how the data will be sent.

+ Can reduce payload size
+ Decouple Service Layer from Database layer.
+ Avoid "over-posting vulnerabilities"

Build the Object from the database before you send it out, that will not directly connect the Db

## How to Use DTOs
[Infoworld - How To Use DTOs](https://www.infoworld.com/article/3562271/how-to-use-data-transfer-objects-in-aspnet-core-31.html)

Biggest plus: Decouple clients from internal structures

DTOs should be *immutable* meaning once created they cannot be changed

They should not contain any logic.  Just data containers.


[&lt;--&#91;BACK&#93;](/README.md)