# Notes for Read 27 - Cookies

## HTTP Cookies
[Mozilla Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)

**Cookie** Small piece of data that a server sends to the user's browser.
Mostly used to tell is two request came from the same server

3 Main purposes:

+ Session Management - Logins, Shopping Carts, Game Score, etc
+ Personalization - preferences, themes, etc
+ Tracking - Recording and analyzing user behavior

Cookies should have lifetimes

You can restrict access with the `http-only` attribute

Cookies should use the `Same-Site` attribute to specify whether or not cookies may be sent by third parties

## HTTP Cookies Explained

Web Server sends a HTTP header `set-cookie`

Microsoft developed a `HTTP-only` cookie to prevent JS interference


 
[&lt;--&#91;BACK&#93;](/README.md)