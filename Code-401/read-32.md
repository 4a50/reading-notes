# Notes for Read 32 - Component Pages

##  Intro to Components
[Microsoft Docs - Components](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/view-components?view=aspnetcore-2.1)

Don't use model binding, they just use the data provided to them.

Can be used in Razor Pages

View Component Class can be defined in three ways
+ Deriving ViewComponent
+ Decorating the class with `[ViewComponent]`
+ Create a class where the name end with **ViewComponent**

uses `<IViewComponentResult>`

Where the site will look for Components:
+ /Views/{Controller Name}/Components/{View Component Name}/{View Name}
+ /Views/Shared/Components/{View Component Name}/{View Name}
+ /Pages/Shared/Components/{View Component Name}/{View Name}

Calling the View Component in Razor Page `@await Component.InvokeAsync("PriorityList", new { maxPriority = 2, isDone = false })`

## View Components

[Marius Schulz - View Components](https://mariusschulz.com/blog/view-components-in-asp-net-core-mvc)

Example Decoration

```
[ViewComponent(Name="Navigation")]
public class NavigationViewComponents : ViewComponent
{

}
```

Render code: `@Component.Invoke("Navigation")`

Example ForEach in the page using the Component Page

`<a href="@navigationItem.TargetUrl">@navigationItem.Name</a>`



[&lt;--&#91;BACK&#93;](/README.md)
