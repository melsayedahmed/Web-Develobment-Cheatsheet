 # ********************* CSS Cheatsheet *********************

## CSS Selectors

### 1. Element Selector
The element selector targets all instances of a specified HTML element.

```css
/* Example: Change color of all links and center all headings */
a {
  color: red;
}

h1 {
  text-align: center;
}
```

### 2. Class Selector
The class selector targets elements with a specified class name. Use a period `.` followed by the class name.

```css
/* Targets all elements with the class "spacious" */
.spacious {
  margin: 20px;
}

/* Targets all <li> elements with the class "spacious" */
li.spacious {
  margin: 20px;
}

/* Targets <li> elements with both "spacious" and "elegant" classes */
li.spacious.elegant {
  margin: 20px;
}

/* Targets all <li> elements and all elements with the class "spacious" */
li, .spacious {
  margin: 20px;
}
```

### 3. ID Selector
The ID selector targets an element with a specific ID attribute. Use a `#` followed by the ID name.

```css
/* Example: Adds a red border to the element with ID "demo" */
#demo {
  border: red 2px solid;
}
```

### 4. Pseudo-classes selector

```css
/* Any button over which the user's pointer is hovering */
button:hover {
  color: blue;
}

/* Applied when the user has already visited the link */
a:visited {
  color: red;
}
```

---
---
---

## Colors

### 1. Color property

```css
p {
  color: #00ff00;
}
```

### 2. Background

```css
.header {
  background: green;
}
/* You can also use an image as a background. */
```

### 3. Native colors

```css
h1 {
  color: blueviolet;
}
/* Note: We generally only use black or white. Other colors such as red, blue, green are only good for testing purposes. You should use Hexadecimal values instead. */
```

### 4. Hexadecimal colors
```css
h1 {
  color: #885df1;
}
/* Use a color picker to find the color you need.

Note: #000000 is black, #ffffff is white. #ffffff is the same as #fff, #FFFFFF or #fff or white. */

```

### 5. RGB colors

```css
/* without transparency */
p {
  color: rgb(135, 93, 241);
}

/* with transparency */
h1 {
  color: rgba(135, 93, 241, 0.5);
}

/* The RGB color model defines a given color according to its red, green, and blue components. An optional alpha component represents the color's transparency. The first 3 values should be between 0 and 255 and the fourth between 0 and 1. 0 being completely transparent. */
```

### 6. Gradient

```css
.footer {
  background: linear-gradient(#e66465, #9198e5);
}

/* Multi-position color stop: A gradient tilted 45 degrees, with a red bottom-left half and a blue top-right half, with a hard line where the gradient changes from red to blue linear-gradient(45deg, red 0 50%, blue 50% 100%); */
```

### 7. CSS Background Size

```css
body {
  background-size: cover;
}

img { 
  background-size: 50%;
}
```

### 8. CSS Background Image

```css
body {
        background-image: url("https://i.notretemps.com/1400x787/smart/2022/06/13/albi.jpeg");
        background-repeat: no-repeat;
        background-size: cover;
        background-color: black;
}
```

---
---
---

## Box

### 1. Border

```css
.header {
  border: 1px solid #885df1;
}
/* First value is the thickness, second one the style (none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset), and third one is the color. */
```

### 2. Margin

```css
/* Margin around the element */
.box-1 {
  margin: 10px;
}

/* Margin left only */
.box-2 {
  margin-left: 10px;
}

/* 10px margin on top and bottom, 5px on the sides */
.box-3 {
  margin: 10px 5px;
}

/* 20px margin top, 15px margin right, 10px margin bottom and 5px margin left */
.box-4 {
  margin: 20px 15px 10px 5px;
}

/* Space outside an element. */
```


### 3. Padding

```css
/* padding around the element */
.box-1 {
  padding: 10px;
}

/* padding left only */
.box-2 {
  padding-left: 10px;
}

/* 10px padding on top and bottom, 5px on the sides */
.box-3 {
  padding: 10px 5px;
}

/* 20px padding top, 15px padding right, 10px padding bottom and 5px padding left */
.box-4 {
  padding: 20px 15px 10px 5px;
}

/* Space inside an element. */
```

### 4. Width

```css
.box-1 {
  width: 100%;
}

.box-2 {
  max-width: 100px;
}

.box-3 {
  min-width: 200px;
}
```

### 5. Height

```css
.box-1 {
  height: 100%;
}

.box-2 {
  max-height: 100px;
}

.box-3 {
  min-height: 200px;
}
```

### 6. Radius

```css
/* Light rounded corner all around the element */
.box-1 {
  border-radius: 20px;
}


/* Rounded corner top left and right only */
.box-2 {
  border-radius: 50% 50% 0 0;
}

/* The border-radius CSS property rounds the corners of an element's outer border edge. */
```

### 7. Box shadow

```css
.box {
  box-shadow: 10px 5px 5px red;
}

/* the third value is the blur radius and the last value is the shadow color.*/
```


### 8. Transform

```css
/* Function values */
transform: rotate(0.5);
transform: rotateX(10deg);
transform: rotateY(10deg);
transform: rotateZ(10deg);
transform: translate(12px, 50%);
transform: translate3d(12px, 50%, 3em);
transform: translateX(2em);
transform: translateY(3in);
transform: translateZ(2px);
transform: scale(2, 0.5);
transform: skew(30deg, 20deg);;

/* Multiple function values */
transform: translateX(10px) rotate(10deg) translateY(5px);
transform: perspective(500px) translate(10px, 0, 20px) rotateY(3deg);
```

---
---
---

## Text

### 1. Text align

```css
h1 {
  text-align: center;
}
/* text-align: left | right | center | justify | initial | inherit; */
```

### 2. Text align

```css
h1 {
  text-decoration: underline;
}
/* none: no line is drawn, and any existing decoration is removed. underline: draws a 1px line across the text at its baseline. line-through: draws a 1px line across the text at its “middle” point. overline: draws a 1px line across the text, directly above its “top” point. inherit: inherits the decoration of the parent. */
```

### 3. Text transform

```css
h1 {
  text-transform: uppercase;
}
/* Note: text-transform: none | capitalize | uppercase | lowercase | initial | inherit; */
```

### 4. Line height

```css
h1 {
  line-height: 28px;
}

p {
  font-size: 14px;
  line-height: 1.5;
}
/* Note: We generally use a multiplier such as 1.5 which making the line height 1.5 times higher than the font size */
```

### 5. Font style

```css
h1 {
  font-style: italic;
}
/* Note: font-style: normal | italic | oblique | initial | inherit; */
```

### 6. Font weight

```css
h1 {
  font-weight: normal;
}

p {
  font-weight: 700;
}

a {
  font-weight: 100;
}
/* Note: font-weight: normal | bold | bolder | lighter | number | initial | inherit; It can also be a value between 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 where 100 is thin and 900 is extra bold */
```

### 7. Font size

```css
body {
  font-size: 18px;
}
```

### 8. Font family

```css
body {
  font-family: Georgia, serif;
}
```

---
---
---

## List

### 1. List style

```css
/* Remove the list bullets point and default spacing */
ul {
  list-style: none;
  padding: 0;
  margin: 0;
}


/* Horizontal list */
li.students {
  display: inline;
}
```

---
---
---

## Layout

### 1. Display

```css
img {
  display: block;
}

.heading {
  display: inline;
}

/* Note: Each element is by default inline or block element. A block element creates an invisible line before and after. An inline element doesn't. */
```

### 2. Position

```css
.heading {
  position: relative;
  top: -10px;
  left: 20px;
}

/* Note: Position can be static | relative | fixed | absolute | sticky. By default, elements are static. */
```


### 3. Center element

```css
img {
  display: block;
  margin: 0 auto;
}
```

### 4. Flexbox

```css
.container {
   display: flex;
   flex-direction: row | row-reverse | column | column-reverse; /* optional */
   justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right; /* optional */
   flex-direction: row | column; /* optional */
}

/* Align elements within the container horizontally */
```

### 5. Responsive image

```css
img {
  max-width: 100%;
  height: auto;
}
```

### 6. Grids

```css
.image-gallery {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: repeat(2, 2fr 1fr);
  gap: 20px;
}

.image-gallery img {
  width: 100%;
}
```

---
---
---

## Mouse

### 1. Cursor

```css
button:hover {
  cursor: pointer;
}

/* auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | zoom-in | zoom-out | grab | grabbing

Note: Pointer is the most common one. */
```

---
---
---

## Advanced CSS

### 1. CSS Variables

```css
:root {
  --main-branding-color: #885df1;
}

h1 {
  color: var(--main-branding-color);
}

/* Note: Useful to store font families, colors or sizes. */
```

### 2. Media queries

```css
@media (max-width: 900px) {
  h1 {
    font-size: 18px;
    text-align: center;
  }

  .footer {
    display: none;
  }
}

@media (min-width: 900px) {
  h1 {
    color: red;
  }
}

/* Media queries are useful when you want to apply CSS to specific resolution breakpoints to make your website more responsive. */
```


---
---
---

## Animations

### 1. Transitions

```css
a {
  transition: all 200ms ease;
  opacity: 1;
  color: blue;
}

a:hover {
  opacity: 0.7;
  color: red;
}
```

---
---
---