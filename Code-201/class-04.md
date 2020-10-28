# Notes for Read 04 - HTML Links, CSS Layout, JS Functions

## From HTML and CSS textbook

### Chapter 4: Links

Linking is a way to navigator to other sites, pages, or areas of the current page.

uses the `<a>` tag.

```<a href="https:/www.imdb.com">IMDB</a>
```

+ `<a href="https://www.imdb.com">` is the Opening Link tag
+ **IMDB** is the text that will be displayed
+ `</a>` is the closing tag.

Ways to link

+ `<a href="https:/www.imdb.com">IMDB</a>` Link to a website
+ `<a href="page2.html">` links to a page on the site
+ `<a href="mailto:jp@jpsrgn.com>` starts up default email program
+ `<a href="https:/www.imdb.com" target="_blank">IMDB</a>`
+ `<a href="#list-of-stuff">List of Stuff</a>` links to an ID element

Relative URLs (other pages withing the same site)

+ `index.html` in the *root* folder
+ `img/happyPic.jpg` in the *child* folder img
+ `data/files/data.csv` in the *grandchild* folder of root
+ `../index.html` links to the *parent* of the current folder to find **index.html**
+ `../../index.html` links to the *grandparent* of the current folder

### Chapter 15: Layout

CSS **Position**:

+ *static* is the default.  Each block element sits on top of the other.
+ *relative* moves an element in relation to where it *would* have been in the normal flow.
+ *absolute* takes the box out of normal flow and no longer affects the position of other elements. **Position** in relation to the containing object.
+ *fixed* Positions the elements in relation to the **browser** window.  Will remain in place even when scrolling down.

CSS: **Z-Index**

+ Used to handle the  position of the elements over top of one each other.  Hence the "Z" in Z-index.

CSS: Floating elements.  The property that allows you to 'float' the element to the far left or right in the containing element.  All others elements will flow around it.

Can use the *clear* command to clear floats so the element does not touch the left or right hand sides of the box.

***Multi-Column*** with Floats:

HTML:

```<div class="column1">
  <h2></h2>
</div>
<div class="column2">
  <h2></h2>
</div>
```

CSS

```.column1{
  float: left;
  width: 620px;
  margin: 10px;
}
.column2{
  float: left;
  width: 300px;
  margin: 10px;
}
```

***Web Page Size*** is typically *960-1000px*

You can call other stylesheet within an *exsisting* style sheet.

```@import url("tables.css");
```

## Javascript & JQuery

### Chapter 3: Functions (Partial Chapter)

declaring a function:

#### Named Function

```function myFunc(a, b){
  return a + bl  
}
var foo = myFunc(12,2);
```

#### Function Expression

```var foo = function(a, b){
  return a + b;
};

var bar = foo(2,3);
```

Immediately invoked Function Expressions (IIFE)

```var area(function() {
  var width = 3;
  var height = 2;
  return width * height;
}());
```

``` greeting(response = 'Not a good Answer'){
  console.log(response);
}
```
*response* is setup as a default, will use the string if no *arguments* are presented when invoking the function.

Minimize the amount of global variables to reduce the risk of collisions when interfacing with other code.

[&lt;--&#91;BACK&#93;](README.md)
