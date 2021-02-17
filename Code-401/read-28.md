# Notes for Read 28 - MVC Forms

## Views in ASP.NET Core MVC

[Microsoft Docs](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-2.2)

View discover happens in this order:

+ Views/[ControllerName]/[ViewName].cshtml
+ Views/Shared/[ViewName].cshtml

Can Pass weakly typed data also

Can Annotate `[ViewData]` to reference a property to save code
It will load the property into the `ViewData` Dictionary.

`@model` at the top not required if the model instance in passed in the `return View(<instance>);` 

## 4 Ways to Create Form in ASP.NET MVC

[CompleteCSharpTutorial](https://www.completecsharptutorial.com/asp-net-mvc5/4-ways-to-create-form-in-asp-net-mvc.php)

Can blend JQuery and AJAX into the page.

Using a strongly typed Form will allow Intellisense to assist 

 `@Html` is a helper able to use MVC data in the element


[&lt;--&#91;BACK&#93;](/README.md)