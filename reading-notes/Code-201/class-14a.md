# Notes for Read 14a - CSS Transforms, Transitions, and Animations

## 2d and 3d Transforms
[https://learn.shayhowe.com/advanced-html-css/css-transforms/](https://learn.shayhowe.com/advanced-html-css/css-transforms/)

```<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

```.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

use *scale* in similar fashion (units are percentage of 100.  60% = .6 200% = 2)

*translate* in px.  Can translate on x and y

*skew* rotate on the Z.  Units **deg**

2d cube demo:

```<div class="cube">
  <figure class="side top">1</figure>
  <figure class="side left">2</figure>
  <figure class="side right">3</figure>
</div>
```

```.cube {
  position: relative;
}
.side {
  height: 95px;
  position: absolute;
  width: 95px;
}
.top {
  background: #9acc53;
  transform: rotate(-45deg) skew(15deg, 15deg);
}
.left {
  background: #8ec63f;
  transform: rotate(15deg) skew(15deg, 15deg) translate(-50%, 100%);
}
.right {
  background: #80b239;
  transform: rotate(-15deg) skew(-15deg, -15deg) translate(50%, 100%);
}
```

## Transitions and animations

[https://learn.shayhowe.com/advanced-html-css/transitions-animations/](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)

psuedo-code ```element:hover```

box to circle hover transition

```.box {
    background: #2db34a;
    border-radius: 6px
    transition-property: background, border-radius;
    transition-duration: 1s;
    transition-timing-function: linear;
  }
  .box:hover {
    background: #ff7b29;
    border-radius: 50%;
  }
```

### All Tranistional Properties

+ background-color
+ background-position
+ border-color
+ border-width
+ border-spacing
+ bottom
+ clip
+ color
+ crop
+ font-size
+ font-weight
+ height
+ left
+ letter-spacing
+ line-height
+ margin
+ max-heigh
+ tmax-width
+ min-height
+ min-width
+ opacity
+ outline-color
+ outline-offset
+ outline-width
+ padding
+ right
+ text-indent
+ text-shadow
+ top
+ vertical-align
+ visibility
+ width
+ word-spacing

Quick Transitions that make an impact:
[http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

[&lt;--&#91;BACK&#93;](README.md)
