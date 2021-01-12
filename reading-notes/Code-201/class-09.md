# Notes for Read 09 - Forms and Events

## From HTML and CSS textbook

### Chapter 9: “Forms” (p.144-175)

Forms controls

+ Adding Text - User inputs
+ Making Choices - Radio buttons and check boxes
+ Submitting Forms - clicking buttons to submit data

Form structure:

```<form action="https://www.google.com" method=get>
<p>From Controls appear here
<input type = "password" name="password" maxlength="30" />
</p>
</form>
```

an *action* is required
*method*  = **Get** or **post**

input types:

+ text input
+ password inputs
+ text areas
+ radio buttons
+ checkboxes
+ dropdown select
+ multiple select box
+ file input box
+ submit button
+ image button - use an image for a submit button
+ button and hidden controls

### Chapter 14: “Lists, Tables & Forms” (pp.330-357)

bullet point styles

+ `list-style-type: lower-roman`
+ `list-style-image: url();`
+ `list-style-position: inside` Where to place the markers

Table properties

+ width
+ padding
+ text-transform
+ letter-spacing, font-size
+ border-top, border-bottom
+ text-align
+ background-color
+ :hover

border empty cells `empty-cells: show`

+ show
+ hide
+ inherit

gaps between cells

+ collapse
+ separate

## Javascript and JQuery

### Chapter 6: Events

Events *fire* or are *raised*

Events *trigger* scripts

How events trigger code

+ select element node
+ indicate which event the selected node will trigger the response.
+ state the code you want to run when the event occurs

DOM event handler

`element.ONevent = functionsName;  **NOTE**: No parentheses`

Event Listeners
`element.addEventListener('event', functionName, \[,Boolean\]);`

[&lt;--&#91;BACK&#93;](README.md)
