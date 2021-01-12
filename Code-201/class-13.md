# Notes for Read 13 - Local Storage

[“The Past, Present, and Future of Local Storage for Web Applications”](http://diveinto.html5doctor.com/storage.html)

To check if a browser supports local storage

```function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
```

Or you can use [modernizr](http://diveinto.html5doctor.com/detect.html#modernizr)

```f (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```

**setters** and **getters**

```var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
```var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
```

check to see if someting has changed in storage

```if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};
```

Interesting to note, that normally there is only 5 megabytes of persistent storage.  But with *sql* you can conceivable have unlimited amounts of data.  Tempting thought.

## Added from in class code

```function localStore() {
  //converting to JSON
  var stringifyAllProducts = JSON.stringify(allProducts);
  // console.log(stringifyAllProducts);
  //put JSON into local storage
  localStorage.setItem('allProducts', stringifyAllProducts);
  //retrieve the item
  var fromLocalStorage = localStorage.getItem('allProducts');
  // console.log('retrieved: ' + fromLocalStorage);
  //translate back to javascript (parse JSON to JS)
  var parsedFromLocaleStorage = JSON.parse(fromLocalStorage);
  // console.log('parsed allProducts: ', parsedFromLocaleStorage);
  // When parsed loose connection to the constructor. They are all object literals
  // If you need to re-establish to constructor: loop over all the object literals and create new object instances
  return parsedFromLocaleStorage;
}
```

[&lt;--&#91;BACK&#93;](README.md)
