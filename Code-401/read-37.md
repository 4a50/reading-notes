# Notes for Read 37 - Xamarin Forms and Data Services

##  Local Storage Using Xamarin Forms
[CSharp Corner](https://www.c-sharpcorner.com/article/local-file-storage-using-xamarin-form/)

Xamarin recommends a third party storage PCLStorage Library
PCL Storage provides a consisten protable set of local file IO

Steps to get up and running:

+ Add NuGet package *PCLStorage*
+ Utilize the IFile interface to access local storage and do CRUD Actions


***Some Examples are provided***

## Local Databases

[Microsoft Docs](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/data/databases)

Install NuGet Package (sqlite-net-pcl)

Must configure app constants to initialize the connection

+ Create and instance of the database and use Database.CreateTableAsync to add a table

Can Copy the database to backup/update/etc..

[&lt;--&#91;BACK&#93;](/README.md)
