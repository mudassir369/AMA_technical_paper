# Core Concepts of HTML, CSS
## 1. How to Write Responsive CSS

Responsive CSS ensures that web pages adapt to different screen sizes (mobile, tablet, desktop).

### Media Queries

```bash
/* Default (Mobile First) */
.container {
  width: 100%;
}

/* Tablet */
@media (min-width: 768px) {
  .container {
    width: 80%;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .container {
    width: 60%;
  }
}
```
---
## 2. Justify Content in CSS

`justify-content` aligns items horizontally inside a flex container.

```bash
.container {
  display: flex;
  justify-content: center;
}
```
---
## 3. display: none vs visibility: hidden


| Property	        | Removes from layout? |	Visible?	| Takes Space? |
|-------------------|----------------------|----------------|--------------|
| `display: none`	    | Yes	               | No	            | No           |
| `visibility: hidden`| No	               | No	            | Yes          |

### Example:

```bash
.box1 { display: none; }
.box2 { visibility: hidden; }
```
---
## 4. How to See Commits in Git

Git tracks version history of your project.

- View All Commits
```bash
git log
```
---
## 5. Box Sizing in HTML

`box-sizing` defines how width and height are calculated.

- border-box

Width = content + padding + border

```bash
* {
  box-sizing: border-box;
}
```
---
## 6. Pseudo Class in HTML (CSS Pseudo-Classes)

Pseudo-classes define special states of elements.

### Examples:

```bash
a:hover {
  color: red;
}

input:focus {
  border: 2px solid blue;
}

li:first-child {
  color: green;
}
```

Common pseudo-classes:

- `:hover`

- `:focus`

- `:active`

- `:first-child`

- `:last-child`

- `:nth-child()`

---

## 7. Opacity in CSS

Controls transparency (0 to 1).

```bash
.box {
  opacity: 0.5;
}
```

- `1` Fully visible

- `0` Fully transparent

Note: Affects the entire element including children.

## 8. Class and ID Selector
- Class Selector (`.`)

```bash
<div class="box"></div>
```
```bash
.box {
  background: red;
}
```

Can be used multiple times.

- ID Selector (`#`)

```bash
<div id="main"></div>
```
```bash
#main {
  background: blue;
}
```

Must be unique.

## 9. Attributes of Flexbox

Flexbox is a layout model.

- Parent Properties

```bash
.container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  align-content: space-between;
}
```

- Child Properties

```bash
.item {
  order: 1;
  flex-grow: 1;
  flex-shrink: 1;
  flex-basis: 200px;
  align-self: center;
}
```
---

## 10. Semantic Tags in HTML

Semantic tags describe meaning.

### Examples:

```bash
<header></header>
<nav></nav>
<section></section>
<article></article>
<aside></aside>
<footer></footer>
```

Benefits:

- SEO friendly

- Accessible

- Better structure

---

## 11. Different Types of Lists in HTML

### 1. Ordered List
```bash
<ol>
  <li>Item 1</li>
</ol>
```

### 2. Unordered List
```bash
<ul>
  <li>Item 1</li>
</ul>
```

### 3. Description List
```bash
<dl>
  <dt>HTML</dt>
  <dd>Markup Language</dd>
</dl>
```
## 12. Label Tag in HTML

Used with form elements.

<label for="email">Email:</label>
<input type="email" id="email">

Benefits:

- Improves accessibility

- Clicking label focuses input

---
## 13. Tags Used in HTML (Common Tags)

```bash
<html>

<head>

<body>

<div>

<span>

<p>

<a>

<img>

<form>

<input>

<button>
```

---
## 14. Header and Footer
```bash
<header>
  <h1>Website Title</h1>
</header>

<footer>
  <p>© 2026 All rights reserved</p>
</footer>
```

- `<header>` Top section

- `<footer>` Bottom section

---
## 15. Block vs Inline Elements
### Block Elements

- Take full width

- Start on new line


#### Examples:
`<div>`, `<p>`, `<h1>`

### Inline Elements

- Take required width only

- Do not start new line

#### Examples:
`<span>`, `<a>`, `<strong>`

## 16. CSS Priority (Inline, Internal, External)
### 1. Inline CSS (Highest Priority)
```bash
<p style="color:red;">Hello</p>
```
### 2. Internal CSS
```bash
<style>
  p { color: blue; }
</style>
```

### 3. External CSS (Recommended)
```bash
<link rel="stylesheet" href="style.css">
```
- Priority Order:

```bash
Inline > Internal > External
```


