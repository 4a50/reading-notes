# Notes for the Pre-work for Code 201 - Introductory HTML and JavaScript

## From HTML and CSS textbook

### Introduction

This book is broken down into three parts:

+ HTML
+ CSS
+ JavaScript

### Chapter 1: Structure

How the a user accesses a webpage (basic):
User-&gt;isp(internet provider)-&gt;Server-&gt;Data Back to User.

Building webpage is like building a house.

+ HTML is equivalent to the framing of the house
+ CSS is the paint
+ Javascript is the plumbing, electricity and utilities.

HTML uses a series of "Tags" to identify the elements.  Tags, for the most part need to be "opened" and then "closed"

+ `<p>` = "open" paragraph tag
+ `</p>;` ="closed" paragraph tag

An element is broken down into a tag, attribute, and value
`<p lang="en-us" >`

`<p` and `>` = tag
`lang=` = attribute
`"en-us"` = value

HTML file is typically laid out in the following manner:
```<HTML>```

```<HEAD>```

```Content about the page, the user does not see goes here```

```</HEAD>```

```<BODY>```

```Content the User Sees goes here```

```</BODY>```

```<HTML>```

### Chapter 8: Extra Markup

When commenting code use the following notation:
```<!-- This is a comment that the users will NOT see -->```

The attribute `ID="Unique-Name` gives a tag an identifier for use in CSS and Javascript

**NOTE:** Two ID attributes *CANNOT* have the SAME value

Attribute `class="A-Class-Name"` gives a tag an identifier that can be used on MULTIPLE tags

Element Types:

+ Block Elements = Elements that start a NEW LINE or Window within the page.
    Examples: `<h1>, <p>, <ul>, and <li>`
+ Inline Elements = Elements that continue on the same line.
    Examples: `<a>, <b>, <em>, and <img>`

Grouping Elements:

+ `<div>` Used to group elements together

+ `<span>` grouping elements inline
    Mostly used to control the appearance through CSS

+ `<iframe>` Utilize a sub-window
    Example: A google map, embed within the page.

+ `<meta>` Information about your page for the search engine to use.

Special Characters:  Characters reserved for use in HTML
    Example: &lt;, &gt;, &amp;, or &copy;
    These are preceded by an &amp;, followed by either the entity name or ASCII code, ended with a ;.
    `&lt;` or `&#60;` will output &lt;

### Chapter 17: HTML 5 Layout

HTML5 is the most current version of HTML.  It add new elements to help with webpage design.

New Elements:

+ `<header>` and `<footer>`
+ `<nav>` = Navigation Block
+ `<article>` = A container for any section that could be standalone or syndicated
+ `<aside>`
    +When used inside an `<article>` = container information related but not critical to the overall article
    +When used outside of an `<article>` = container for content related to the whole page.
+ `<section>` groups related content together
+ `<hgroups>` groups `<h1>` - `<h6>` to be formatted as a single unit
+ `<figures>` references from main flow of page
+ `<div>` used to group together related elements
+ `<a>` can group whole blocks into hyperlinks
    Example:
        ```<a href="intro.html">```
        ```<article>```
        ```<figure>```
        ```<img scr="coolPic.png" />```
        ```</figure>```
        ```</article>```
        ```</a>```

**Note** Javascript is required to help older browsers that cannot use HTML5

### Chapter 18: Process and Design

Some things to consider before designing your website:

+ Who are you designing your site for?
    To assist with this step create several "people" that may use your site.

+ Why would someone visit?
    Perhaps to buy a product or get information
+ What are you trying to achieve?
+ What information do visitors need?
    Are they familiar with your product or service?
    What is *special* about you?
+ How often will people be expected to visit?
    Will be key in determining how often you need to update your site.

Start website design:

+ Build a *site map* to lay out the information needed.
+ Build a *wireframe* to lay out how the site will be structured
+ Organize and prioritize the design of the site
    How to effectively communicate your message to the user
        Some elements to consider:
            Visual Hierarchy: Draw attention to what you want them to see
            Grouping: Easier for the user to parse the information
            Similarity: Associate style with content type
            Navigation: Ease of which to make your way around the site.

**CODING IS THE *LAST* THING YOU DO WHEN DESIGNING A SITE**

## From Javascript and JQuery Textbook

### Intro

javascript make webpages more interactive

+ Access content
+ Modify content
+ Program rules
+ React to events

Examples:

+ slide shows
+ forms
+ reload part of a page
+ filter data

### Chapter 1

A *script* is a series of instructions

To write a script:

+ Define a goal.
+ Design the script.
+ Code each step.
    **CODING IS THE LAST STEP!**

Events - computer has marked that something has occurred.  Used to trigger some kind of functionality.

Scripts - A series of instructions for the computer to execute

Method - How programmers interact with objects

+ Tell you something about an object
+ Change one or more of the object's values

EVENTS -&gt; Call Method -&gt; changes value or returns object property

Web browsers are programs built using objects.

+ Window Object - The window
+ Document Object - The HTML Code
    Page Received as Code
    Creates a model of the page in memory
    Uses a rendering engine to display the page in screen

HTML -&gt; CSS -&gt; javascript = content -&gt; presentation -&gt; behavior (interactivity)

Linking to a javascript file:

```<script src="/app.js"></script>```

How objects are called in javascript:

```document.write("Good Day");```

```document``` = object

```.``` = member operator

```write("Good Day")``` = method

```;``` = line terminator

**NOTE**: `"Good Day"` is a parameter used by the method

javascript file is run where it is found.  Scripts are mostly called at the end of the ```<body>``` container.

[&lt;--&#91;BACK&#93;](README.md)
