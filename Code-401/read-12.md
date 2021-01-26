# Notes for Read 12 - EF Core and APIs

## EF Core Getting Started
[Microsoft Docs - EF Core - Getting Started](https://docs.microsoft.com/en-us/aspnet/core/data/ef-mvc/intro?view=aspnetcore-5.0)

**-Reviewed the tutorial-**

Every Entity is a class.

EF works best when Async.
Don't run operations in parallel.  use Await to keep each action in sync.

## Entity Framework Core

[Microsoft Docs - Entity Framework Core](https://docs.microsoft.com/en-us/ef/core/)

A *Model* consists of *Entity Classes* <--Class

Three ways to develop a model in EF

+ Generate from exsisting database
+ Hand Code a Model to match a database
+ Once model is created, use *EF Migrations*

Use *LINQ* <-- should be *LIQ* (I want it to anyway)

***CRUD*** Data using instances of *Entity* class

## Data Seeding

[Microsoft Docs - Data Seeding](https://docs.microsoft.com/en-us/ef/core/modeling/data-seeding)

How to seed data code example from MSDocs

```
modelBuilder.Entity<Blog>().HasData(
  new Blog {BlogId = 1, Url = "http://sample.com"}
  );
```

Create a new *object*

## Razor Pages with Entity Frameword

[Microsoft Docs - Razor Pages](https://docs.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-2.1&tabs=visual-studio)

+ Create a Model (Models Folder)
+ Create Entity Classes

Scaffolding a *Model* = produces pages for **CRUD**

## Enable User Secrets

[CodeFellows - Enabling user secrets](https://codefellows.github.io/code-401-dotnet-guide/resources/user-secrets.html)

Allows for certain data to remain locally and not be distributed.

This allows for setting of environment variables.  API Keys, UserName, Pwords, etc

## Intro to APIs

[Youtube - Intro to APIs](https://youtu.be/aIkpVzqLuhA)

--Viewed--

[&lt;--&#91;BACK&#93;](/README.md)