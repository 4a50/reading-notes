# Notes for Read 02 - HTML Text, CSS Introduction, and Basic Javascript Instructions

## From HTML and CSS textbook

### Chapter 2: Text

There are six levels of headings.  Largest to smallest => &lt;h1&gt; - &lt;h6&gt;

`<p>` Is a paragraph.  Starts on a new line with spacing between it and other paragraphs

`<b>` bolds text.  `I am <b>groot</b>! => I am **groot**!

`<sup>`/`<sub>` superscript/subscripts

`<br />` inserts a line break
`<ht />` inserts a horizontal rule

*Semantic Markup* will not visually add anything to your code, but is useful for organization

Examples:

+ `<em>` emphasizes a word
+ `<strong>` indicate context has strong importance.
+ `<blockquote>` longer quotes that take up a whole paragraph
+ `<q>` used for shorter quotes.  IE Explorer does not put in quotations, so this is not as widely used.
+ `<abbr>` is used for abbreviations and acronyms.  Syntax is:
    `<abbr title="Super Mario Brothers">SMB</abbr>`
+ `<cite>` used for citing a piece of work.
    `<cite>A Tale of Two Cities</cite> by Charles Dickens`
+ `<dfn>` first time you explain some new terminology
    `<dfn></dfn>`
+ `<address>` contain contact details of the author

```<address>
    <p><a href="mailto:link@hyrule.gov">link@hyrule.gov</a></p>
    <p>123 Rainy Shrub Ln, Small Province, Hyrule 55544</p>
    </address>
```

+ `<ins>` and `<del>` are used to annotate inserted and deleted text to show changes
+ `<s>` indicated the data that is no longer required, but should not be removed from the page.

**NOTE:** Should not use to change the way the page looks, it's a way to describe the content of your webpage more accurately.

### Chapter 10: Introducing CSS

Linking to an external CSS:

`<link href="css/styles.css" type="text/css" rel="stylesheet" />`

`href` where the file is located
`type` type of document being linked to
`rel` Specifies the relationship between the HTML and the file it is linked to

**NOTE**: You can link multiple files.  Some link files for fonts and another for layout

CSS Rule Parts

``` p {
    font-family: Arial;}
```

`p` is the selector (HTML element)
`font-family: Arial;` is the declaration

The declaration is broken down into two parts

`font-family:` is the property
`Arial` is the value

Not commonly used but *internal CSS* allows for use in the HTML page

```<style type="text/css">
h1 {
    color: red;
}
</style>
```

CSS Selectors allow for targeting rule to specific elements in the HTML

Selectors:

+ Universal Selector
    Applies to ALL elements in the document
        `* {}`
+ Type Selector
    Matches element names
        `h1, h2, p {}`
+ Class Selector
    Matches an element whose class **id** attribute has a value that matches the one specified after the full-stop (.)
        `.note{}`
+ ID Selector
    Matches an element whose id attribute has a value that matches the one specified after the pound symbol
        `#introduction`
+ Child Selector
    Matches the element that is a direct **child** of another
        `li>a {}`
+ Descendant Selector
    Matches the element that is a descendant of of another specified element
        `p a {}` and `'` elements inside a `p` element.  Even if they are further nested 
+ Adjacent Sibling Selector
    Matches and element that is the next sibling of another
        `h1+p []` Targets the first `<p>` element after ANY `<h1>` element (but not other `<p>` elements)
+ General Sibling Selector
    Matches an element that is a sibling of another, although it doesn't have to be directly preceding the element.
        `h1~p {}` if you had two siblings of an `<h1>` element, this rule would apply to both.

***R-E-M-E-M-B-E-R*** CSS reads from top to bottom.  If two selectors conflict, the one farther down the page will take precedence

If you specify properties on an element.  It's properties are **inherited** by the child properties.

## From Javascript and JQuery textbook

### Chapter 2: Basic Javascript Instructions

A *script* is a series of instructions that a computer can follow

a *statement* is each set of instructions, that should end in a semi-colon

a *comment* is code that will not be run, but can be helpful for explaining your code.
```// This is a comment```

``` var = whatever
    */
    This is a multi-line
    comment
    */
```

Anatomy of declaring a variable: `var quantity;`
`var` = variable keyword
`quantity` = variable name

Anatomy of assigning a value: `quantity = 12;`
`quantity` = variable name
`=` is the assignment operator
`12`; variable value

Data Types

+ Number
+ String
+ Boolean

Some shorthand for assigning variables

+ Declare and assign at the same time `var isFull = false;`
+ Declare multiple variables at once `var isFull, speed, fluxReadout`
+ Declare and assign on the same line: `var crazyMeter = 100, speed = 88;`

6 Rules for assigning a variable:

+ Variable name must begin with a letter, _ , or $ it
+ Cannot use a - or an full-stop (.) in the variable name
+ Cannot use *keywords* or *reserved* words
+ Variable are case-sensitive
+ Use camelCase, no spaces allowed

Arrays in Javascript can be accessed and changes as required.
```var collectionStuff = ['one', 'two', 'three'];```
**NOTE**: Arrays are zero-indexed
**NOTE**: Can use multiple data-types
Above is an example of an *Array Literal*

`var collectionStuff = new Array('one', 'two', 'three');`
This is an example of an *Array Constructor*

### Chapter 4: Decisions and Loops *less Switch Statements*

Comparison Operators

+ `==` equal to (can mix data types.  `'3' == 3) *Not Commonly Used*
+ `===` strict equal to (must match data types)
+ `!=` *not* equal to
+ `!==` strict *not* equal to
+ `>` greater than
+ `>=` greater than or equal to
+ `<` less than
+ `<=` less than or equal to

Can compare multiple expressions keep each in their own parens
`(score1 + score2 ) > (highScore1 + highScore2);`

Can evaluate multple expressions using logical operators
`&&` and
`||` or
`!` not `!(2 < 1)` will evaluate to *true*

[&lt;--&#91;BACK&#93;](README.md)
