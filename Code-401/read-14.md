# Notes for Read 14 - Routing and Navigation Properties

## Routing within MVC

[MS-Docs - Routing within MVC](https://docs.microsoft.com/en-us/aspnet/mvc/overview/older-versions-1/controllers-and-routing/asp-net-mvc-routing-overview-cs)

With MVC Web App, the routing table is created in the Global.asax.

When a url in entered: /Home/Index/4

controller = Home
action = Index
id = 4

You can make calls to routes with controller or index or id.

## Routing within ASP.NET Core

app.use uses middleware to perform it routing.

ASP.Net uses an **endpoint** concept.  
They represent parts of functionality that are distinct from each other

Use endpoints.MapGet -> to establish a route.  This will allow
different functionality to be performed based on the HTTP route.

ASP.NET will perform URL matching.

You can template routes.

```
products/{id}
```

route template matching examples:

Template: hello  URLMatching: /hello

{controller=Home}/{action}/{id?}  Maps to the **Home** controller and **index** method.  Ignores **id**

You can use REGEX to get more complex matching

Create custom constraints IConstraints interface.

For good error information:
set appsetting.Development.json set: Logging:LogLevel:Microsoft --> Debug.





[&lt;--&#91;BACK&#93;](/README.md)