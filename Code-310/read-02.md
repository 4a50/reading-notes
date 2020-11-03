# Notes for Read 02 - jQuery, Events, and The DOM

## JQuery

`$('li.hot').addClass('complete');`

**('li.hot')**  --> JQuery Object
**addClass('complete')** --> Method

If jQuery has *multiple* selections and a method is called to *get* information only the *1st* object will be called.

JQuery does not store the objects it *sets* or *gets*, it just **references** it. (Just stores the address)

JQuery can **chain** methods together when *setting*.  Cannot **chain** when *retrieving* information/

To run the script *AFTER* the page is fully loaded.

``` 
$function(){
  //All code to be executed.
}
```

inserting elements:

**.before()** &lt;li&gt;**&#46;prepend()** item **.append()** &lt;/li&gt; **.after()**

### Setting CSS Properties

Get

```
var bgColor = $('li').css('background-color');
```
Set

```
$('li').css('background-color, #ffffff);
```

### Event Methods

```
$('li').on('click', function() {
  $(this).addClass('complete');
});
```

You can use the contextual *this* to refer to the object the event has occurred on.

[&lt;--&#91;BACK&#93;](/README.md)