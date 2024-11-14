# ********************* HTML Cheatsheet *********************

## General


### 1. Page structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SheCodes</title>
</head>
<body>
  
</body>
</html>
```


### 2. Comment

```html
<!-- this is a comment -->
```

---
---
---

## Text Tags


### 1. Headings

```html
<h1>
  SheCodes
</h1>
<h2>
  SheCodes
</h2>
<h3>
  SheCodes
</h3>
<h4>
  SheCodes
</h4>
<h5>
  SheCodes
</h5>
<h6>
  SheCodes
</h6>

<!-- // Note: Only h1, h2, h3, h4, h5, and h6 exist, you should only have one h1 on your page. -->
```


### 2. Paragraph

```html
<p>
  SheCodes teaches busy women how to code.
</p>
```


### 3. Unordered Lists

```html
<ul>
  <li>
    SheCodes Basics
  </li>
  <li>
    SheCodes Plus
  </li>
  <li>
    SheCodes Responsive
  </li>
  <li>
    SheCodes React
  </li>
</ul>
<!-- // Note: <ul> can only have <li> as direct descendants. -->
```


### 4. Ordered List

```html
<ol>
  <li>
    SheCodes Basics
  </li>
  <li>
    SheCodes Plus
  </li>
  <li>
    SheCodes Responsive
  </li>
  <li>
    SheCodes React
  </li>
</ol>
<!-- // Adds numbers in front of each list item. -->
<!-- // Note: We rarely use this one as it's hard to style. -->
```

### 5. Nested lists

```html
<ul>
  <li>SheCodes Basics</li>
  <li>SheCodes Plus</li>
  <li>
    <strong>SheCodes Pro</strong>
    <br />
    <ul>
      <li>SheCodes Basics</li>
      <li>SheCodes Plus</li>
      <li>SheCodes Responsive</li>
      <li>SheCodes React</li>
    </ul>
  </li>
</ul>
```

### 6. Link

```html
<a href="https://www.shecodes.io/">SheCodes</a>
<a href="https://www.shecodes.io/" target="_blank">SheCodes</a>
<a href="https://www.shecodes.io/" target="_blank" title="SheCodes Website">SheCodes</a>

<!-- // Adds a link to the page. -->
<!-- // Note: target="_blank" opens the link in a new window. -->
```

### 7. Mailto link

```html
<a href="mailto:team@shecodes.io">Send us an email</a>
```

### 8. Anchor link

```html
<a href="#important">
  Jump to the heading below
</a>

<div id="important">
  This is a note
</div>
<!-- // Link to a section on the same page -->
```

---
---
---


## Separators

### 1. Line Break

```html
SheCodes offers coding workshops <br />
to busy women <br />
Sign up today
<!-- // Note: Inline element -->
```


### 2. Horizontal Rule

```html
SheCodes offers coding workshops
<hr />
to busy women
<hr />
Sign up today
<!-- // Note: Inline element -->
```

---
---
---


## Attributes

### 1. Classes


```html
<a href="https://www.shecodes.io/" class="website-url">SheCodes</a>
<div class="header important">SheCodes Workshops</div>
<!-- // Classes are generally used to select elements from CSS. Name your classes using clear English words. If you want a class name to include multiple words, separate each word with a hyphen - . If you want to use multiple class names, use a space in between. Class names should be lower cased. -->
```


### 2. Ids

```html
<a href="https://www.shecodes.io/" id="website-link">SheCodes</a>
<!-- // Ids are generally used to select elements from JavaScript and can only be used once. Name your ids using clear English words. If you want an id name to include multiple words, separate each word with a hyphen -. If you want to use multiple id names, use a space in between. Id names should be lowercased. -->
```

---
---
---


## Containers

### 1. Div


```html
<div>SheCodes</div>
<div class="coding-workshop">SheCodes</div>
```


### 2. Span

```html
<span>SheCodes</span>
<span class="best-workshop">SheCodes</span>
```


### 3. Header

```html
<header class="page-header">
    <h1>SheCodes Workshops</h1>
</header>
```


### 4. Footer

```html
 <footer>
        <p>© SheCodes</p>
    </footer>
```

### 5. Section

```html
<section class="workshop-information">
    <h2>SheCodes Pro</h2>
    <p>SheCodes Pro includes everything you need to become a professional developer...</p>
</section>
```

---
---
---


## Media Tags

### 1. Image

```html
<img src="https://s3.amazonaws.com/shecodesio-production/uploads/files/000/083/182/original/cat.png?1685030491" />
<img src="https://s3.amazonaws.com/shecodesio-production/uploads/files/000/083/182/original/cat.png?1685030491" alt="Image description" />
<img src="https://s3.amazonaws.com/shecodesio-production/uploads/files/000/083/182/original/cat.png?1685030491" alt="Image description" width="400" />
```


### 2. Video

```html
<video src="https://video-url"></video>
<video src="https://video-url" controls></video>
```


### 3. Audio

```html
<audio controls src="https://url-to-audio-file.mp3"></audio>
```

---
---
---

## Form Tags

### 1. Form

```html
<form action="/submit">
    <label for="name">Enter your name: </label>
    <input type="text" placeholder="Your name" name="name" id="name" required />
    <label for="email">Enter your email: </label>
    <input type="email" placeholder="Your email" name="email" id="email" required />
    <input type="submit" value="Subscribe!" />
</form>
```


### 2. Inputs

```html
<label for="name">Name (4 to 8 characters):</label>
<input type="text" id="name" />
```


### 3. Button

```html
<button class="signup-button">
  Sign up now
</button>
```

### 4. Radio inputs

```html
<label>What pets do you have?</label>
<input type="radio" name="pet" id="cats" value="cats" checked />
<label for="cats">Cats</label>
<input type="radio" name="pet" id="dogs" value="dogs" />
<label for="dogs">Dogs</label>
<input type="radio" name="pet" id="frogs" value="frogs" />
<label for="frogs">Frogs</label>
```

### 5. Checkbox inputs

```html
<label>What pets do you have?</label>
      <div>
        <input type="checkbox" name="pets" id="cats" value="cats" />
        <label for="cats">Cats</label>
      </div>
      <div>
        <input type="checkbox" name="pets" id="dogs" value="dogs" />
        <label for="dogs">Dogs</label>
      </div>
      <div>
        <input type="checkbox" name="pets" id="frogs" value="frogs" />
        <label for="frogs">Frogs</label>
      </div>
```

### 6. Select element

```html
 <label for="countries">Which country would you like to travel to?</label>
    <select id="countries">
      <option value="">Select a country</option>
      <option value="france">France</option>
      <option value="italy">Italy</option>
      <option value="usa">USA</option>
      <option value="brazil">Brazil</option>
      <option value="japan">Japan</option>
    </select>
```

---
---
---

## Styling tags

### 1. Strong

```html
<strong>SheCodes Workshops</strong>
<!-- Makes the content bold. -->

<!-- Note: Inline element -->
```


### 2. Small

```html
<small>SheCodes Workshops</small>
<!-- Makes the text within it one font size smaller.
Note: Inline element -->
```


### 3. Em

```html
<em>SheCodes Workshops</em>
<!-- Makes the text italic.
Note: Inline element -->
```

---
---
---


## CSS in HTML

### 1. Internal CSS

```html
<head>
  <style>
    body {
      background: #f8f5ff;
    }

    h1 {
      color: purple;
      text-align: center;
    }
  </style>
</head>

<!-- Add a style element inside your <head> to include CSS in your HTML file. You should ideally have a maximum of 1 style element on your page. You don't need a style element if you're using external CSS. -->
```


### 2. External CSS

```html
<head>
    <link rel="stylesheet" href="style.css" />
</head>
<!-- Link to an external CSS file, add multiple link tags to link to multiple CSS files.
Note: Link is a self-closing tag -->
```

---
---
---


## JavaScript in HTML

### 1. Internal JavaScript

```html
<body>
  <h1>
    SheCodes
  </h1>
  <script>
    alert("Hello SheCodes");
  </script>
</body>
<!-- Add your script tag to the bottom of your body. Anything inside script is JavaScript. -->
```


### 2. External JavaScript

```html
<body>
  <h1>
    SheCodes
  </h1>
  <script src="app.js"></script>
</body>
<!-- Link to your external JavaScript file at the bottom of your body. The script element doesn't include any content but needs to be closed. It is not a self-closing tag. -->
```

---
---
---

## SEO

### 1. Title element

```html
<title>The title of your website - Brand</title>
<!-- Determine the document's title that will be shown in a browser’s title bar or a page's tab More info -->
```


### 2. Meta description

```html

<head>  
  <meta name="description"  content="This is an example of a meta description. This will often show up in search results." />
</head>
```

---
---
---

## Table

### 1. Table structure

```html
   <table>
      <thead>
        <tr>
          <th>First name</th>
          <th>Last name</th>
          <th>Nationality</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Matt</td>
          <td>Delac</td>
          <td>French</td>
        </tr>
        <tr>
          <td>Amanda</td>
          <td>Smith</td>
          <td>American</td>
        </tr>
      </tbody>
    </table>
```

---
---
---