# Notes for Read 12 - EF Core and APIs

## Dependency Injection

[MS Docs - Dependency Injection](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection?view=aspnetcore-5.0)

To use a dependency, it is preferred that you create an Interface, and then use the interface in your class.
That way you won't be using a concrete class.  And it doesn't modify the controller.

.AddScoped Method registeres the action with a lifetime of a single request.

## Repository Design Pattern
[MS Docs](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design#the-repository-pattern)

Repositories are classes the encapsulate the logic needed to access data sources

 a repository allows you to populate data in memory that comes from the database in the form of the domain entities

 1 aggregate per repository.

## Repository Design Pattern

[medium.com](https://medium.com/@pererikbergman/repository-design-pattern-e28c0f3e4a30)

Repository pattern has two purposes

+ abstraction of the data layer
+ centralize the domain objects

Keep things small simple and consistent

If you generalize, the interface become more flexible to use.

## S O L I D
[Telerik.com](https://www.telerik.com/blogs/30-days-of-tdd-day-five-make-your-code-solid)

[Why SOLID matters](https://www.telerik.com/blogs/why-solid-matters)

[SOLID principle in pictures](https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898)

***S***ingle Responsibility Principle.

One method == One reason to change.

***O***pen/Close Principle

Method/Class should be open for extention, closed for modification

***L***iskov Substitution Principle

An Object in an application should be able to be replaced with a type derived from it withough breaking the application.  Should be able to use type &lt;Animal> and also use &lt;Dog> and &lt;CAT> that derive from it.

***I***nterface Segregation Principle

People should not be forced to rely on *interfaces* they do not use.  

***D***edendency Inversion Principle

Code should depend on *Abstractions* not concrete implementations.



[&lt;--&#91;BACK&#93;](/README.md)