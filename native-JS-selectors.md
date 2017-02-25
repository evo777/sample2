Like CSS, JavaScript also has the ability to access DOM elements based on their selectors. This functionality is similar to CSS. In general, the methods for accessing and manipulating elements are on the `document` interface.

###Selecting by Tag
To select multiple elements by their tag name (`<div></div>`, `<span></span>`, ect.), use the `document.getElementsByTagName` method. This will return a HTMLCollection, which is a array-like object containing live (or automatically updating) DOM elements.
```
var allSpanElements = document.getElementsByTagName('span');
```

###Selecting by Class
To select multiple elements by their class name (`<div class="example"></div>`), use the `document.getElementsByClassName` method. This will return a HTMLCollection, which is a array-like object containing live (or automatically updating) DOM elements.
```
var allSpanElements = document.getElementsByClassName('content');

// You can also filter by elements that have multiple classes

var onlySpansWithTheseClasses = document.getElementsByClassName('content red');
// This will only return elements that have both the 'content' and 'red' classes
```

**Note:** this method can be called on other DOM elements as well. For instance: 

```
var insideClasses = document.getElementById('content').getElementsByClassName('red');
```

###Selecting by ID

> **Note:** this is the only JavaScript selector that does _not_ return a collection.

To select a single element by its class name (`<div id="myId"></div>`), use the `document.getElementById` method. This will return a live (or automatically updating) DOM element.
```
var myIdElement = document.getElementById('myId');
```
