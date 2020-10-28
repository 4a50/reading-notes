# Notes for Read 03 - HTML Lists. CSS Boxes, JS Control Flow

## From HTML and CSS textbook

### Chapter 3: Lists

3 Types of Lists in HTML

+ ordered `<ol>`
  Will display the list items with sequential numbering
+ unordered `<ul>`
  Will display list items without sequential marking
+ definitions `<dl>`, `<dt>` and `<dd>`
  `<dl>` Will display an Definition List
  Will display the term `<dt>` and `<dd>` the definition of that term.

Example Code below

```<h3>Stuff</h3>
<ul>
  <li>Parts of Stuff</li>
  <li>Other Parts of Stuff</li>
</ul>
<h3>Bake a cake</h3>
<ol>
  <li>Mix the batter</li>
  <li>Shove in an oven</li>
</ol>
<dl>
  <dt>Tween</dt>
  <dd>A young person that is older than 10, but younger than 13 years of age.</dd>
```

**NOTE**: You can *NEST* lists/

### Chapter 13: Boxes

Box Dimensions:
You can specify a width or height.  Units are **px**, **%**, and **em**

```div{
  height: 100px;
  width: 200px;
}
```

You can limit the width with **max-width** and **min-width**

```div{
  max-width: 1000px;
  max-height: 1000px;
  min-width: 1000px;
  min-height: 1000px;  
}
```

Can handle how the browser deal with content that is larger than it's container.
Utilizing *overflow* with the values of **hidden** and **scroll**

```p.one{
  overflow: hidden;
}
p.two{
  overflow: scroll;
}
```

![Borders, Margins, and Padding](/img/MBP.png)

**NOTE**: *Screenshot from Chrome Web Browser*

Adjust the *border* width `border-width: 2px;`

+ Specify with the following: **border-xxx-width**.  xxx = top, right, bottom, or left.
+ Can also specify unique edges all at once: `border-width: 2px, 3px, 10px, 4px;` **NOTE**: %s not allowed

Border Styles - 'border-style: dashed'

+ solid
+ dotted
+ double
+ groove
+ ridge
+ inset
+ outset
+ hidden/none+
**NOTE**: You can specify as side: `border-xxx-style` xxx = directions

Border Coloring: `border-color: indianred;`.  
**NOTE**: You can specify as side: `border-xxx-color` xxx = directions

Border Shorthand: `border: 3px, dotted, red`.  Should in the following specific order: Size, style, color

Padding is defined `padding: 10px;`.  
**NOTE**: You can specify as side: `padding-xxx` xxx = directions

Margins are handled in the same manner as Padding

To center boxes set the ***Margins** to **Auto**

```p.example{
  margin: 5px, Auto, 5px, Auto
}
```

**REMEMBER** top, right, bottom, left

**Display** will reverse the function or a **block** or **inline** element

+ **inline-block** will allow a block level element to flow like and *inline* element, but retain the *block* properties.
+ **none** will hide the block

Utilizing **visibility** will hide the element, but retain the space where it should be.

## From Javascript and JQuery textbook

### Chapter 4: Decisions and Loops

Switch Statements:

>"Well, it's kinda like an if-else but not really.  It's dumb." - Anonymous

Wonder who said that?

```{
switch(elevatorFloor) {
    case 1:
      msgRead = 'Floor 1'
      break;
    case 2:
      msgRead = 'Floor 2'
      break;
    default:
      msgRead = 'No Floor.  You are in the twilight zone.';
      break;
}
```

Javascript will try to use a given value rather than display an error.  It can *implicitly* convert data types.  This is ***type coercion***

Data Types:

+ string
+ bool
+ number
+ null - empty value
+ undefined - declared but not defined

List of **Falsy Values**

+ *false* bool
+ number zero
+ Empty String
+ 10/'score' - NaN(Not a Number)
+ `var warpSpeed;` a declared value

List of **Truthy Values**

+ *true* bool
+ number one
+ strings with content
+ `10/2` number calculations
+ `'true'` as a string
+ `'0'` as a string
+ 'false' as a string

#### USE STRICT EQUALITY OPERATORS

``` (4 == '4') = true
(4 === '4') = false
```

*strict equality* operators will only compare same data types.  If they are different, then **FALSE**!!!

When comparing using || logical operators.  It will stop at the first *true* value.  Either assign the value, or execute the code in the condition.

```var redShirt = '';
var blueShirt = 'Crusher';
awayTeamLeader = (redShirt || blueShirt || 'No one will go');
```

awayTeamLeader = 'Crusher'

Loop Counters:

```for (var i = 0; i < 10; i++){
  setWarpSpeed = i;
}
```

setWarpSpeed will iterate 10 time. 0 - 9.

Common Keywords: *break* and *continue*

Delta between *do..While*  and *while*

+ **while** loop condition is evaluated *first* prior to executing the code
+ **do..while** loop condition is evaluated *after* the code has run.

[&lt;--&#91;BACK&#93;](README.md)
