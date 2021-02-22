# Notes for Read 31 - Razor Pages

## Intro To Razor Pages

[MS Docs](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/?view=aspnetcore-2.2&tabs=visual-studio)
[GunnarPeipan](https://gunnarpeipman.com/aspnet-core-razor-pages/)
[Razor vs MVC](https://jonhilton.net/razor-pages-or-mvc-a-quick-comparison/)



Designed to provide HTML for server side view data

Can directly access the model in the HTML page.

This is similar to MVC, but there are no areas required for controllers and models.

You can access methods and properties directly on the page using the `@` symbol.

Razor Pages are built into .NET framework

MVC uses the controller to call the logic and then send the data out.  Razor Pages the request goes to the page that was built to handle it 
and sends back the response from there.

Razor Pages vs MVC
+ Don't need make Models and Controllers as seperate pages
+ Razor is good for people beginning or transitions over from other languages.

[&lt;--&#91;BACK&#93;](/README.md)
