# CSS

## Inheritance Shortcuts

```css
/* Use body tag to set styles for most tags -- Saves re-writing code. */
body {
  font-family: "Courier New", Courier, monospace;
  font-size: 2em;
  color: #ffffff;
}
```

```css
/* Box Model default behaviour is set to content-box -- Set to border-box */
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

```css
/* Inherit code -- saves re-writing code */
*,
*::before,
*::after {
  box-sizing: inherit;
}

html {
  box-sizing: border-box;
}
```

## **Responsive CSS / Mobile First Design**

### **Percentages and avoiding heights**

- By default CSS is responsive (width and height)
- Set values can take **responsive** away
- Elements are defaulted to a `width of 100% of parent element`
- Avoid giving height if possible / rather set padding as relative unit `em`

### **Relative Units**

- **`em`** Compounds on top of parent element's font-size
  - Use when dealing with margins and padding
  - **`em`** For margin/padding looks at the font-size of that element not the parent element
- **`rem`** Does not compound, looks at font-size in **`::root`** element
  - **`rem`** For margin/padding looks at the font-size in the **`::root`** element
- To have consistent spacing between elements, use **`rem`** over **`em`**
- **`em`** and **`rem`** are more effective when working with media queries

### **View-port Units**

- **`vh`** Specifies the % of the view-port height **`100vh`** is `100%` of the view-port height
- **`vw`** Specifies the % of the view-port width **`80vw`** is `80%` of the view-port width
  - **`vh`** and **`vw`** can be very effective on *titles (h tags)* for responsive designs (as view-port changes so does title tags)
- **`vmin`** Takes the smallest(smaller) value out of the two units (view-port height vs view-port width)
- **`vmax`** Takes the largest(taller) value out of the two two units (view-port height vs view-port width)
- **`vmin`** and **`vmax`** can benefit in the same way and can prevent bloating at certain device sizes

## **CSS Grid**

```css
.testimonial-grid {
  display: grid;
  gap: 1.5rem;
}

@media (min-width: 50em) {
  .grid-col-span-2 {
    grid-column: span 2;
  }
  .testimonial-grid {
    grid-template-columns: repeat(4, 1fr);
  }
  .testimonial:last-child {
    grid-column-start: 4;
    grid-row: 1/3;
  }
}
v

/* ZTM */
.container {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  grid-template-rows: 1fr;
}
```

## **Flex Box**

```css
.containers {
  display: flex;
  /* display: flex => flex container */
  flex-direction: row;
  /* By default set to flex-direction: row */
  /* This div becomes a row, all direct children of this row becomes columns */
  gap: 100px;
  /* Creates a space of 100px between each Flex-items */
  justify-content: flex-start;
  /* Justifies space between flex items */
  flex-wrap: wrap;
  /* By Default set to nowrap,switching to wrap, 
allows flex-items to no spill over */
  flex-flow: row wrap;
  /* Combines flex direction and wrap (shorthand) */
}
.flexbox-items {
  /* These are now flex items */
  /* Flex items by default try to shrink to the smallest size they can be */
  flex-grow: 1;
  /* When more than 250px, Grows to take all available space */
  flex-shrink: 1;
  /* When less than 250px, Shrinks to smallest size it can be */
  flex-basis: 250px
    /* If it has available space how muc room does it want to take up, 
I want to be 250px */ flex 1 1 250px;
  /* Shorthand for all three */
  order: 1;
  /* Controls the order, good for re-arranging items (mobile) */
}

.col + .col {
  /* Combinator > selecting adjustent sibling */
  margin-left: 30px;
}

.hero__img {
  align-self: flex-start;
  /* align vertically from the top */
}

.img {
  max-width: 100%;
  /* Images will never increase above original size, 
but will shrink to fit page */
}
```

## **Media Queries**

```css
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

### **Breakpoints**

- Work out breakpoints when the layout starts breaking
- Keep breakpoints to minimal

### **View-port meta tag**

```css
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<!-- Ensure your website is going to be responsive the way you want it to be. -->
```

### **Custom Properties**

```css
/* Have to defined inside selector */ /* If in root, they will be Global Properties */ /* --{name}: value */
:root {
  --dark: #00bd9d;
  --light: #88bd7d;
}

body {
  /*  */
  color: var(--dark);
}
```

## **CSS One Liners**

```css
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
