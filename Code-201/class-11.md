# Notes for Read 11 - Audio, Video. and Images

## From HTML and CSS textbook

### Chapter 9: pages (201-206)

History of Flash.  No longer being supported ~January 2021

### Chapter 16: Images

Commonly used image sizes

+ small: 220 x 360
+ medium: 330 x 210
+ large: 620 x 400

Setting image size universally wrt size.  Make them a *class*

To align images create a class similar to:

```img.align-left{
  float:left;
  margin-right-10px

  img.align-right {
    float: right;
    margin-left: 10px
  }
}
```

Centering an image:

```img.align-center:{
  display: block;
  margin: 0px auto;}
```

background images: `background-image`

repeating background images:

`background-repeat: repeat;`

+ repeat
+ repeat-x
+ repeat-y
+ no-repeat

`background attachment:` - determines whether the image should move with the page or stay fixed in one spot

+ fixed
+ scroll

`background-position: 50% 26%`
Two positions entered: horiz and vert

Image rollovers and sprites

#### SEE PAGE 417 FOR SYNTAX

### Chapter 19: Practical Information

**SEO**: Search Engine Optimization

Where possible:

+ use keywords in the URL
+ use keywords in the heading
+ use keywords 2-3 times in text
+ use keywords as *link* names
+ keywords in image *alt-text*
+ Use keywords in the *meta* data in the *&lt;head&gt;*

Identify keywords and phrases:

+ Brainstorm
+ organize
+ research
+ compare
+ refine
+ map

Check out google analytics to learn about people visiting your site (pg 483-44)

[&lt;--&#91;BACK&#93;](README.md)
