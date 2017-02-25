In CSS, selectors are the keywords used to assign styling properties to DOM elements. While there are a variety of selectors, they all take the same basic syntax: 

```
div {
  color: blue;
}
```

In this example, `div` is the _selector_ and the keyword `color` is the _property_ we are applying to it.

###Tag Selectors

_Tag Selectors_ are selectors that apply to an entire HTML tag. Please note that you may sometimes hear these referred to as _type selectors_, as per CSS specifications. For this example, every `p` tag in the document would have a green background:

```
p {
  background-color: green;
}
```

###Class Selectors

> **Note:** classes are preferred over ids for styling elements. Refer to the Hack Reactor official style guide for more information.

_Class Selectors_ are used to provide styling properties to multiple elements within a document. Classes can be used with other classes, and do not need to be unique. This means that multiple elements can reuse the same styles, enabling DRY practices. 

**style.css**
```
.example1 {
  color: white;
}

.example2 {
  background: blue;
}
```

**index.html**
```
...
<div class="example1 example2">
A div with multiple classes
</div>

<div class="example1 example2">
Notice how this element also uses the same classes. This is a great feature!
</div>
```

Take careful note of the syntax used to apply multiple classes to the same element. 

###id Selectors

Unlike class selectors, _id selectors_ **must** be unique within a document. While the `id` HTML attribute is commonly used for DOM manipulation and insertion, it is discouraged for styling purposes. 

**style.css**
```
#uniqueItem {
  color: red;
}

#warningBox {
  border: 1px solid red;
}
```

**index.html**
```
...
<div id="uniqueItem">
Warning: please don't use ids for styling
</div>
```

Notice how ids and classes are both used on the same element.