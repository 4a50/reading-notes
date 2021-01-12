# Notes for Read 01 - Responsive Web Design and Floats

## Websites

[Shay Howe's Intro to RWD](http://learn.shayhowe.com/advanced-html-css/responsive-web-design/)

[All About Floats](https://css-tricks.com/all-about-floats/)

### Shay Howe's Intro to RWD

**Responsive** generally means to react quickly and positively to any change

**Adaptive** means to be easily modified for a new purpose or situation

Responsive web design is broken down into three main components:

+ flexible layouts
  Use relative units *em* or *%*
+ media queries
 using the `@media` rule inside of an existing style sheet importing a new style sheet using the `@import` rule, or by *linking to a separate style sheet from within the HTML*
common `@media` types:
  all
  screen
  print
  tv
  braille

  Can use *logical operators*
  `only` is a new operator, and cannot be used using *HTML4 algorithm*

  `@media all and (min-device-aspect-ratio: 16/9)` can use for aspect ratios
  `@media all and (orientation: landscape)`
  `media only screen and (-webkit-min-device-pixel-ratio: 1.3), only screen   and (min-device-pixel-ratio: 1.3)`
  breakout of mobile first media queries example
  
  ```Default styles first then media queries
  @media screen and (min-width: 400px)  {...}
  @media screen and (min-width: 600px)  {...}
  @media screen and (min-width: 1000px) {...}
  @media screen and (min-width: 1400px) {...}
  ```

  Viewport Rule

    ```@viewport {
    width: device-width;
    zoom: 1;
    }
  ```

+ flexible media
    One quick way to make media scalable is by using the *max-width* property with a value of **100%**
    This ensures that as the viewport gets smaller any media will scale down according to its containers width.

    ```img, video, canvas {
    max-width: 100%;
    }
    ```

### All About Floats

Floats are helpful for layout for **smaller instances**

Using *clear* sister property to *float*
![float-not-cleared](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/unclearedfooter.png?resize=540%2C195)

![float-cleared](https://i2.wp.com/css-tricks.com/wp-content/csstricks-uploads/clearedfooter.png?resize=540%2C230)

*Images used from [CSS Tricks](https://css-tricks.com/all-about-floats/)

Some issues with floats

+ Pushdown - an element *inside* a floated item being *wider* than the float itself will push down

+ Double Margin Bug: With IE6 if you apply a *margin* in the same direction as the float it will **double** the margin

+ 3px jog - when text is up against a floated object it will kick away about *3px*

[&lt;--&#91;BACK&#93;](/README.md)
