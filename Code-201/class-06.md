# Notes for Read 06 - Object Literals and the DOM

## Javascript/jQuery

### Lecture

String literals:

`var string = \`The product of ${a} and ${b} is ${product}\``

### Chapter 3: Object Literals

Defining an object with key value pairs

```var starFox{//These are key:value pairs
  name: 'Fox McCloud',//These are properties
  species: 'Fox',
  title: 'Team Leader',
  onBoard: true,
  checkIfOnBoard: function() {//this is a Method
    return this.onBoard;
  }
};
//to Run the method
starFox.checkIfOnBoard
```

Accessing HTML page elements and inserting data.  **NOTE**: html code not included

```var displName = document.getElementById('pilot-name');
displName.textContent = starFox.name;
var displPosit = document.getElementById('team-status');
displPosit.textContent = starFox.title
var isOnBoardShip = document.getElementById('is-onboard');
isOnBoardShip.textContent = starFox.onBoard;
```

## Chapter 5: DOM (Document Object Model)

At the top of any *DOM TREE* it is assigned the **document** node.

Below the *document* node are all the child nodes:

+ **element** node - html, h1-6, body, div, etc
+ **attribute** nodes - Don't have children, are *part* of the element node.  *div=* or *class=*
+ **text nodes** the annotated text

### Selecting what you need

Selecting an *individual* element

+ *getElementById()*
+ *querySelector()*

Selecting a *group* of elements

+ *getElementsByClassName()*
+ *getElementsByTagName()*
+ *querySelectorAll()*

Moving between element nodes

+ *parentNode*
+ *previousSibling* / *nextSibling*
+ *firstChild* / *lastChild*

#### Working withing those elements

Access or update text nodes

+ *nodeValue*

Work with HTML content

+ *innerHtml*
+ *text-content*
+ \[create a new node \] *createElement()* - DOM Manipulation
+ \[create a new node \] *createTextNode()* - DOM Manipulation
+ \[create a new node \] *appendChild()*/*removeChild* - DOM Manipulation

Access of update attribute values

+ *hasAttribute()*
+ *getAttribute()*
+ *setAttribute()*

A *NodeList* is similar to an *array* in that they are a collection of nodes indexed at 0.  These are regarded as *collections* and not arrays

**static node lists** will not be updated as the document is updated.  It's a single snapshot
**live node lists** will update as the document is updated.

*getElementsBy* returns *live* node lists
*querySelector* returns *static* node lists

you can utlize brackets to search for the *id* attribute, regardless of what it's value it.  

```querySelectorAll('li[id]')```

two methods when selecting elements from a nodelist.

+ item() - ```var firstItem = elements.item(0)```
+ array syntax - ```var firstItem = elements[0]``` **preferred method**

Utilizing *querySelector* or *querySelectorAll* can use CSS selectors.

```var foo = document.querySelect('li.hot');
foo.className = 'cool';
```

```var foo = document.querySelectAll('li.hot');
foo[1].className = 'cool';
```

Most browsers (except Internet Explorer) treat whitespace between elements as a *text-node*.  
2 ways to deal with it:

+ Could strip the whitespace out of the HTML
+ utilize javascript library: JQuery

Inline elements are treated as *sibling* nodes to regular text.  And the inline elements text is a *child* of the inline element.

```<li id="one"><em>fresh</em> figs</li>```

**li** = parent.  **em** and the text **figs** = *siblings*.  **fresh** = child of em, and grandchild to li.

update text with either

+ text-content
+ innerText

Avoid using innerText:

+ browser compatibility
+ obeys CSS
+ performance

Adding elements using DOM manipulation

+ `createElement()`
+ `createTextNode()`
+ `appendChild()`

```var newElem = document.createElement('li');
// console.log('newElem' + newElem);
var newText = document.createTextNode('Lara Croft');
// console.log('newText: ' + newText);
newElem.appendChild(newText);
// console.log('updated newElem: ' + newElem);
var position = document.getElementsByTagName('ul');
// console.log('position: ' + position);
position.appendChild(newElem, 1);
```

Remove elements using DOM manipulation

+ store the elements to be removed in a *var*
+ store the *parent* parent of the element in a *var*
+ remove the element from it's *containing* element.  `removeChild()`

```var removeElem = document.getElementsByTagName('li')[0];
console.log(removeElem);

var containerElem = removeElem.parentNode; //Parent of removeElem
console.log(containerElem);

containerElem.removeChild(removeElem);
```

Attribute Nodes

`document.getElementById('one').getAttribute('class');`

Methods:

+ getAttribute()
+ hasAttribute()
+ setAttribute()
+ removeAttribute()

Properties:

+ className
+ id

[&lt;--&#91;BACK&#93;](README.md)
