# CSS

## CSS Inheritance Templates

```
/* CSS body default */
body {
  font-family: "Courier New", Courier, monospace;
  font-size: 2em;
  color: #ffffff;
}
```

```
/* CSS box-sizing  */
html { box-sizing: border-box; }

*:not(img), *:before, *:after { box-sizing: inherit; }
```

## **Custom Properties**

```
/* Define variables for CSS colors */
:root {
  --darkBG: #1e1e2e;
  --darkFG: #ff5747;
}

body {
  background-color: var(--darkBG);
  color: var(--darkFG);
}
```

## **Responsive CSS / Mobile First Design**

### **View-port Meta Tag**

```
<!--Disabling Viewport Zomming-->
<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0, maximum-scale=1.0"
/>
```

### **CSS Tricks**

- By default CSS is responsive (width and height)
- Set values can take **responsive** nature away from CSS
- Elements are defaulted to a _width of 100% of parent element_
- Avoid assigning height if possible / rather set padding as relative unit `em`
- For larger screens use `max-width: 750px;` or `width: 80%` to avoid stretching

### **Relative Units**

- **`em`** Compounds on top of parent element's font-size
  - Use when dealing with margins and padding
  - **`em`** For margin/padding looks at the font-size of that element not
    the parent element
- **`rem`** Does not compound, looks at font-size in `::root` element
  - **`rem`** For `margin` or `padding` looks at the `font-size` in the `::root` element
- To have consistent spacing between elements, use `rem` over `em`
- **`em` and `rem`** are more effective when working with `media queries`

### **View-Port Units**

- **`vh`** Specifies the % of the view-port height `100vh` is `100%` of
  the view-port height
- **`vw`** Specifies the % of the view-port width `80vw` is `80%` of
  the view-port width
  - **`vh` and `vw`** can be very effective on titles `h tags` for responsive designs as the view-port changes so does title tags
- **`vmin`** Takes the smallest value out of the two units
  `(view-port height vs view-port width)`
- **`vmax`** Takes the largest value out of the two two units ``(view-port height vs view-port width)`
- **`vmin` and `vmax`** can benefit in the same way and can prevent
  bloating at certain device sizes

## **Media Queries**

### **Breakpoints**

- Work out breakpoints when the layout starts breaking
- Keep breakpoints to minimal

```
/* can set media types, if left blank, targets all media types */
min-width: 600px , 600px or bigger target
max-width: 200px, 200px or smaller target
/* Below selects screen sizes in-between the targets */
@media (min-width: 600px) and (max-width: 600px) {
}
/* Write css for mobile first, use media queries to size desktop sizes */
/* Order is important */
@media (min-width: 600px) {
  background-color: steelblue;
}
```

## **CSS One Liners**

```
/* Sets Text Vertical */
writing-mode: vertical-1r;

/* Flip an Image */
transform: scaleX(-1);
transform: scaleY(-1);

/* Smooth Scrolling */
scroll-behavior: smooth;

/* Scroll Snapping */
scroll-snap-type: x mandartory; /*On parent*/
scroll-snap-type: y mandartory; /*On parent*/
scroll-snap-type: x promimity;/*On parent*/
scroll-snap-align: center; /*On child */

/* Resize */
overflow: auto;
resize: both;

/* Truncate */
max-width: 20rem;
display: -webkit-box;
-webkit-line-clamp: 1; /* x of lines to show */
-webkit-box-orient: vertical;
overflow: hidden;

/* Text Gradients */
/* On h1 */
background: linear-graidient(to right, color1, color2, colorN)
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;

/* Pointer Events -- Stops from selecting items  */
pointer-events: none;
opacity: 0;
animation: fade 1s ease-in 1s;
```
