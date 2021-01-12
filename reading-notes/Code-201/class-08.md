# Notes for Read 08 - Object-Oriented Programming and HTML Tables

## From HTML and CSS textbook

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

[&lt;--&#91;BACK&#93;](README.md)
