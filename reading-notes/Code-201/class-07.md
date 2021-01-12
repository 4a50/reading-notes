# Notes for Read 07 - Object-Oriented Programming and HTML Tables

## Web Reading

Building a prototype will allow multiple *objects* to access the same code comprising of the function.

## From HTML and CSS textbook

### Chapter 6: Tables (pp.126-145)

`<table>` used to create the structure of a table

`<tr>` and `<td>` are Row Start/Table Cell

`<th>` is the table heading

*scope* to indicate whether the *heading* is for a *row* or *column*

Row (Cell, Cell, Cell, Cell, Cell)
Row (Cell, Cell, Cell, Cell, Cell)

```<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr
   <tr>
    <th scope="row">Ticket Sold</th>
    <td>122</td>
    <td>343</td>
</table>
```

Can *span* across rows

`<td rowspan="2">Big Item</td>`

Elements that help separate out the main content, first and last rows.  All of which may be styled differently.

```<thead>
<tbody>
<tfoot>
```

## Javascript/jQuery

### Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

To build a constructor of an object to create many other objects

```function ShipMembers(name, species, title, onBoard){
  this.name = name;
  this.species = species;
  this.title = title;
  this.onBoard = onBoard;

  this.checkIfOnBoard = function(){
    return this.onBoard;
  }
}
var starFoxOne = new ShipMembers('Peppy Hare', 'Hare', 'Mechanic', true);
var pilotName = document.getElementById('pilot-name');
pilotName.textContent = starFoxOne.name;
```

Three groups of built-in object models:

+ Browser Object Model
+ DOM
+ Global Javascript Objects

With the browser object model you can obtain information regarding browser window or tab.
(See page 124) for a list of commands.  A few are listed below

+ `window.location` - Current URL of window object
+ `window.alert()` - Generates a dialog box
+ `window.screen` - reference to a screen object

With the DOM you can access information about the page:
(See page 126) for a list of properties and methods.  A few are listed below

+ `document.title` - title of the current document
+ `document.URL` - url of the current page
+ `document.domain` - domain of the current document

Global javascript objects.  A few are listed for reference and context

+ `.length`
+ `toLowerCase()`
+ `charAt(12)`

Global object related to Date and Time
(See page 137) for list.  Few listed for reference

+ getDate();
+ getHours();
+ toDateString();

[&lt;--&#91;BACK&#93;](README.md)
