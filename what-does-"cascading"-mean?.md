CSS is cascading because each CSS file or inline style progressively adds upon the next.  This is in contrast to a type of style which would wholly overwrite the next.  For example:

    <style>
      h1 {
        color: red
      }
    </style>
    <h1 style="font-size: 22em">This is a heading</h1>


If CSS were non-cascading, then the in-line style definition would take precedence and override the style defined in the tag, and as a result the h1 tag would be 22em, but not red.  Since CSS IS cascading, they are additive, with the most recent attribute in the cascade having priority if there is a conflict.  For the example, this results in the h1 text being BOTH red and 22em.

##What about conflicting styles?

Cascading does mean that the when two styles address the same property, the last ordered one will take precedence. For example:

```
.example1 {
  color: red;
}
    
.example2 {
  color: blue;
}
```

For the following HTML, what color would you expect the text to be?

```
<div class="example1 example2">What color am I?</div>
```

The text would be blue, because `.example2` comes after the styling of `.example1`.
