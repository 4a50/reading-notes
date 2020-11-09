# Notes for Read 05 - Heroku

+ Requires Git
+ NodeJS
+ NPM

Allows to deploy to an acutal server.

Basic JS for to test a server

```
var http = require("http");

http.createServer(function(request, response) {
  response.writeHead(200, {"Content-Type": "text/plain"});
  response.write("It's alive!");
  response.end();
}).listen(3000);
```



[&lt;--&#91;BACK&#93;](/README.md)
