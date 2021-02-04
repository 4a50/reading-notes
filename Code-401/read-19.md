# Notes for Read 19 - Claims and JWT tokens

## Claims Base Authorization

[MS DOCS](https://docs.microsoft.com/en-us/aspnet/core/security/authorization/claims?view=aspnetcore-2.1)

Checks the value of a claim and grants access based upon the value.

Adding a claim:

```services.AddAuthorization``` in the *ConfigureServices* method

Then need to apply the attribute.

Can add multiple policies under one Controller action.

## Intro to Claims

[Andrew Lock](https://andrewlock.net/introduction-to-authentication-with-asp-net-core/)

Claims based Authentication.

A claim is about *who* or *what* the property is.

You *Claim* a FirstName

The *Value* could be 'Mario'

You can have multiple Identities toes to claims. Person -> Passport and driver's license.


## IWT Authentication

[CodeBurst](https://codeburst.io/jwt-to-authenticate-servers-apis-c6e179aa8c4e)

JWT = JSON Web Token

It's a way to ENCODE a JSON object

Parts
+ Header - Gives the way to verify the token
+ Payload - the stuff (Claims)
+ Signature - Encrypts the Data and provides a unique signature




 
[&lt;--&#91;BACK&#93;](/README.md)