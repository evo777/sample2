# Responsive vs. Adaptive Design

## Why they are similar and easy to confuse

Responsive and adaptive design patterns are both answers to the fact that users will be accessing our sites from different devices with different characteristics. Responsive and adaptive design both allow us to create a good experience for our users regardless of how they reach our site.

## Why they are different

The difference between the two is primarily that responsive design is a continuous process and adaptive is a discrete process. A responsive site adjusts fluidly to varying screen sizes, whereas an adaptive site will respond at discrete points. Good design will often make use of both to achieve a good UX.

### Responsive Design
An example of responsive behavior can be seen in the following.

```html
<div class="container">
    <!-- site contents -->
</div>
```

```css
.container {
    width: 90%
}
```

In the above case, the site contents will dynamically adjust width with respect the the screen width.

### Adaptive Design

The following shows is an example of adaptive design. In this case, the div is only shown for large screens and is hidden for smaller screens.

```html
<div class="decorative">
```

```css
@media screen and (max-width: 700px) {
    .decorative {
         display: none;
    }
}
```

The practice of using a totally separate mobile and desktop site is also an example of adaptive design.
