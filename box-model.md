*TODO: what's the point of knowing this?*

## Background
* How CSS acts on an HTML element in the DOM
    * *TODO: This is a bit vague.  Probably good to use the word "layout" somewhere in the article.*
* Defined by W3C

From outside-in, the CSS box model is defined as: margin-border-padding-content. In CSS, the width and height of an element refer to the width and height of the content.

![box-model](https://upload.wikimedia.org/wikipedia/commons/7/7a/Boxmodell-detail.png)

The total height of an element is: `margin-top` + `border-top` + `padding-top` + `height` + `padding-bottom` + `border-bottom` + `margin-bottom`.

The total width of an element is: `margin-left` + `border-left` + `padding-left` + `width` + `padding-right` + `border-right` + `margin-right`.

## Gotchas
* Old versions of Internet Explorer include border, padding, and content in the calculation of the width of an element.