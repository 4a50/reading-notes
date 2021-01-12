# Notes for Read 11 - EJS

## EJS (Embedded Javascript Templates)

-Used to insert vairable and perfrom functions into HTML code.

+ `NPM i ejs`

```let template = ejs.compile(str, options);
template(data);
// => Rendered HTML string
 
ejs.render(str, data, options);
// => Rendered HTML string
 
ejs.renderFile(filename, data, options, function(err, str){
    // str => Rendered HTML string
});
```

Can perform *IF ELSE* statements

Can Map over objects to display their *properties*

## Google Books API

`https://www.googleapis.com/books/v1/volumes?q=search+terms`

`q` - Search for volumes that contain this text string. There are special keywords you can specify in the search terms to search in particular fields, such as:
`intitle`: Returns results where the text following this keyword is found in the title.
`inauthor`: Returns results where the text following this keyword is found in the author.
`inpublisher`: Returns results where the text following this keyword is found in the publisher.
`subject`: Returns results where the text following this keyword is listed in the category list of the volume.
`isbn`: Returns results where the text following this keyword is the ISBN number.
`lccn`: Returns results where the text following this keyword is the Library of Congress Control Number.
`oclc`: Returns results where the text following this keyword is the Online Computer Library Center number.

Example GET Request for *Flowers for Algernon* by Daniel Keyes 

`https://www.googleapis.com/books/v1/volumes?q=flowers+inauthor:keyes&key=yourAPIKey`

[&lt;--&#91;BACK&#93;](/README.md)
