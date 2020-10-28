# Class 5: HTML Structures

## Chapter 10 and 11: CSS color

referencing the stylesheet, what each of the components mean.
```<link href="css/style.css" type="text/css" rel="stylesheet" />```

href = path to the CSS file
type = what type of file is being referenced
rel = relationship between HTML and the file being referenced

class selector : ```p.note {}```  this will target all elements &lt;p&gt; with the class name **note**

childs and decendants:  
+**child** is an element directly below it's **parent**
    +```li>a {}``` targets &lt;a&gt; elements that are children of &lt;li&gt;
+**decendant** an element nested in the parent, does **not** have to be a child.
    +```p a {}``` targets all elements &lt;a&gt; that are nested/decended within &lt;p&gt;

rgba color add a fourth value for opacity.  ***NOTE*** only the most recent browsers support this.

hsl, hsla = hue, saturation, lightness, alpha

hue represented as degrees (color wheel)
saturation (how much grey) represented as a percentage
lightness (how much white or black) represented as a percentage
    + Differ from **brightness** in that brightness only adds black, and lightness add black or white
alpha (transparancy) represented as a percentage

add color backup for older browsers prior to normal lines.

[<--BACK](README.md)