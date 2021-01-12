# Notes for Read 05 - CSS: HTML Images, CSS Color & Text

## From HTML and CSS textbook

### Chapter 5: Images

All images should have their own folder.  normally an `/img` or `/images`

HTML syntax for an image:

`<img src="img/happyPic" alt="A picture of a happy person">`

You can add a `height=` and `width=` in the tag, but it is more common to use **CSS**

Placing an image in HTML matters:

+ Before a `<p>` tag the `<p>` will display on the next line
+ *inside* a `<p>` tag, the `<p>` first row aligns with the bottom of the image.
+ *In the middle* of a `<p>` the image will appear  in the middle.

3 rules for creating images:

+ Save the image in the correct format
+ Save the images in the size you intend to use them
+ Measure images in pixels.

Image formats:

+ **jpg** is good for images with many colors
+ **gif** and **png** good for images with few colors and large areas of the same color

Animated GIFs use more memory and tend to load slower.  Use sparingly.

*gif* is good to use when the transparency part of the image is in straight lines
*png* is good when the transparency area is more rounded or diagonal

### Chapter 11: Color

rgba color adds a fourth value for opacity.  ***NOTE*** only the most recent browsers support this.

hsl, hsla = hue, saturation, lightness, alpha

hue represented as degrees (color wheel)
saturation (how much grey) represented as a percentage
lightness (how much white or black) represented as a percentage

+ Differ from the **brightness** in that brightness only adds black, and lightness add black or white

alpha (transparency) represented as a percentage
add color backup for older browsers prior to normal lines.

### Chapter 12: Text

Different categories of typeface:

+ *Serif* - Good for long passages.  Easier to read
+ *Sans-serif* - Straight ends to letters.  Can be clearer to read by lower resolution monitors
+ *Monospace* - Good for code, it lines up well with structure.

Units of type size:

12 px scale

        px      %     ems 
  
+ h1    24px    200   1.5em
+ h2    18px    150   1.3em
+ h3    14px    117   1.17em
+ body  12px    75    100%
+ p                   0.75em

16px scale

+ h1    32px    200   2em
+ h2    24px    150   1.5em
+ h3    18px    133   1.125em
+ body  16px    100   100
+ p                   1em

```
@font-face {
font-family: 'emulogic';
src: url('font/emulogic.eot');
}
```

Font formats should be included in code in the following order

+ eot
+ woff
+ ttf/otf
+ svg

`font-weight:`

+ bold
+ normal

`font-style:`

+ normal
+ italic
+ oblique

`text-transform`

+ uppercase
+ lowercase
+ capitalize

`text-decoration`

+ none
+ underline
+ overline
+ line-through
+ blink

Leading (ledding) - the vertical distance between lines

`line-height:`

uses **em** unit

Letter and word spacing (kerning)

`letter-spacing:` - spacing between *letters*

`word-spacing:` - spacing between *words*

`text-align:` - control the alignment of text

+ left
+ right
+ justify
+ center

`vertical-align`

+ baseline
+ sub
+ super
+ top
+ text-top
+ middle
+ bottom
+ text-bottom

`text-indent` - Allows you to indent the first line of text within an element.

`text-shadow: 1px 2px 0px #000000;` - used to create a drop shadow (dark copy of the word, just behind and offset.)

1px = how far left or right
2px = distance to the top or bottom
0px = (optional) amount of *blur* to add
#000000 = color of the shadow

`first-letter:` or `first-line` - Specify different values.  These are *pseudo-elements*.  Technically they are **not** properties

styling links `:link` or `:visited` - pseudo-classes to handle what visited and non-visited links look like.

```a:link{
  color: indianred;
  font-size: 10px;  
}
```

Responding to Users

+ `:hover` - What is applied when the mouse is hovering over the element
+ `:active` - applies when an element is being activated by a user.  **Example**: When a button is being clicked.
+ `:focus` - When an element has focus.  When an element can be interacted with

[&lt;--&#91;BACK&#93;](README.md)