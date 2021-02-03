# Notes for Read 18 - Authentication

## Introduction to Identity on ASP.NET Core

[MS Docs](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity?view=aspnetcore-2.1&tabs=visual-studio)

Add service to `service.Configure{service}` methods

`app.UseAuthentication();` 

On a PostAsync method you can Login and Logout

## Authorization Demystified

Key componenets
+ Ident
+ Verbs
+ Auth Handlers
+ middleware

Claim is a *single fact* about a user, such as a Name or DOB

*Ident* form of proving who you are.

*principal* is the actual user

Utilized in Razor Pages.  Should take a look at those.

 
[&lt;--&#91;BACK&#93;](/README.md)