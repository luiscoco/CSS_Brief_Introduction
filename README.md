# CSS: brief introduction

https://www.w3schools.com/css/css_examples.asp

https://frontendinterviewquestions.medium.com/top-30-css-interview-questions-and-answers-b2ab81bcbd38

CSS, or Cascading Style Sheets, is a stylesheet language used to describe the presentation of a document written in HTML or XML (including XML dialects such as SVG or XHTML)

CSS defines how elements should be rendered on screen, on paper, in speech, or on other media

CSS is used to control the layout of web pages with styles and design elements such as colors, fonts, and spacing

It allows you to apply styles to HTML elements selectively, using selectors based on element types, class names, ID, or attributes

## Example of CSS

Here's a basic example of CSS where we style a simple HTML document to change the color and font size of a paragraph:

**HTML File (index.html)**

```html
<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p class="content">This is a sample paragraph to demonstrate CSS styling.</p>
</body>
</html>
```

**CSS File (style.css)**

```css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
}

h1 {
    color: navy;
}

.content {
    color: #555;
    font-size: 16px;
}
```

## How to Use CSS in VSCode

Visual Studio Code (VSCode) is a popular editor for web development that supports HTML, CSS, JavaScript, and many other languages. Here’s how you can start using CSS in VSCode:

**Open VSCode**: Start by opening Visual Studio Code

**Create a New Project**: Go to File -> New File or open an existing project with HTML files

**Add a CSS File**: You can create a new CSS file by going to File -> New File and saving it with a .css extension

**Link CSS to HTML**: Ensure your HTML file links to the CSS file using the <link> tag in the <head> section

**Write Your CSS**: Use the CSS file to define styles for HTML elements

**Preview Your Page**: You can preview your web page by opening the HTML file in a web browser or using a live server extension in VSCode

VSCode also provides helpful features like syntax highlighting, code completion, and linting for CSS, making it easier to write and debug your stylesheets

Additionally, the VSCode marketplace offers extensions like Live Server that can help you see changes in real time as you develop your web pages

I'll provide you with a few more CSS samples that demonstrate different aspects of styling, such as layout, responsiveness, and interactive elements. These examples will help you see the variety of ways CSS can be used to enhance the presentation of web pages.

## CSS for Layout: Flexbox

Flexbox is a CSS layout module that makes it easy to design flexible responsive layout structure without using float or positioning

**CSS (style.css)**

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Full height of the viewport */
}

.box {
    width: 100px;
    height: 100px;
    margin: 10px;
    background-color: teal;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
}
```

**HTML (index.html)**

```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
</div>
```

## CSS for Responsiveness: Media Queries

Media queries are useful for making designs responsive across different screen sizes.

**CSS (style.css)**

```css
body {
    background-color: lightblue;
}

.content {
    padding: 20px;
    margin: 20px;
    background-color: white;
}

@media (max-width: 600px) {
    .content {
        background-color: lightgreen;
    }
}
```

**HTML (index.html)**

```html
<div class="content">
    Resize the browser window to see the background color change.
</div>
```

## CSS for Interactive Elements: Hover Effects

CSS can be used to create interactive effects such as changes on hover.

**CSS (style.css)**

```css
.button {
    background-color: navy;
    color: white;
    padding: 10px 20px;
    text-align: center;
    display: inline-block;
    transition: background-color 0.3s;
}

.button:hover {
    background-color: coral;
}
```

**HTML (index.html)**

```html
<a href="#" class="button">Hover Over Me!</a>
```

These examples should give you a good starting point for exploring different CSS properties and techniques

You can use them directly in a project or modify them according to your needs

Each example demonstrates a fundamental aspect of CSS that can be expanded upon or combined with other CSS features to create rich, interactive web experiences

Let’s dive into some more advanced CSS samples that demonstrate animations, grid layouts, and advanced selectors. These examples will help you utilize CSS to create more sophisticated and interactive web designs.

## CSS Animations: Keyframes

CSS animations are powerful for creating smooth, animated changes to the properties of HTML elements

Here's an example of using keyframes to animate an element continuously:

**CSS (style.css)**

```css
@keyframes spin {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}

.spinner {
    width: 100px;
    height: 100px;
    background-color: red;
    animation: spin 2s linear infinite;
}
```

**HTML (index.html)**

```html
<div class="spinner"></div>
```

## CSS Grid Layout: Responsive Gallery

CSS Grid is a powerful tool for creating complex and responsive layouts

Here’s an example of a responsive image gallery using CSS Grid:

**CSS (style.css)**

```css
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    grid-gap: 10px;
    padding: 10px;
}

.gallery img {
    width: 100%;
    height: auto;
    object-fit: cover; /* Ensures images cover the grid item */
}
```

**HTML (index.html)**

```html
<div class="gallery">
    <img src="image1.jpg" alt="Gallery Image 1">
    <img src="image2.jpg" alt="Gallery Image 2">
    <img src="image3.jpg" alt="Gallery Image 3">
    <img src="image4.jpg" alt="Gallery Image 4">
</div>
```

## Advanced Selectors: Styling Forms and Inputs

Using advanced CSS selectors, you can style different states of form elements, enhancing the user interface of forms:

**CSS (style.css)**

```css
input[type="text"],
input[type="email"],
textarea {
    width: 100%;
    padding: 8px;
    margin: 10px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box; /* Include padding and border in the element's width */
}

input[type="submit"] {
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

input[type="submit"]:hover {
    background-color: #45a049;
}

input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    border-color: #4A90E2;
    outline: none; /* Removes the default focus outline */
}
```

**HTML (index.html)**

```html
<form action="">
    <input type="text" placeholder="Your name..." name="name">
    <input type="email" placeholder="Your email..." name="email">
    <textarea placeholder="Enter message..."></textarea>
    <input type="submit" value="Submit">
</form>
```

These advanced examples showcase how CSS can be used to create dynamic, responsive, and visually appealing web designs

They provide a foundation for exploring more complex features and techniques in CSS to enhance your web development projects

# Advanced CSS

We'll explore CSS Variables, the clip-path property, and the filter property for creating more dynamic and stylistic web elements

## CSS Variables for Theme Customization

CSS Variables, also known as custom properties, allow you to define reusable values that can be applied throughout your stylesheet

This is extremely useful for themes or to adjust styles dynamically

**CSS (style.css)**

```css
:root {
    --primary-color: #4CAF50;
    --accent-color: #FFC107;
}

body {
    background-color: var(--primary-color);
    color: white;
    font-family: Arial, sans-serif;
}

.button {
    background-color: var(--accent-color);
    border: none;
    padding: 10px 20px;
    margin: 5px;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.button:hover {
    background-color: darken(var(--accent-color), 10%);
}
```

**HTML (index.html)**

```html
<button class="button">Click Me!</button>
```

## Using clip-path for Creative Shapes

The clip-path CSS property allows you to create complex shapes by clipping an element to a basic shape or an SVG path

This can be used for intriguing visual effects

**CSS (style.css)**

```css
.shape {
    width: 200px;
    height: 200px;
    background-color: var(--accent-color);
    clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
    transition: all 0.3s ease;
}

.shape:hover {
    background-color: var(--primary-color);
}
```

**HTML (index.html)**

```html
<div class="shape"></div>
```

## CSS Filters for Visual Effects

CSS filters can be applied to images and other elements to create various visual effects like blurring, brightness adjustment, and more

**CSS (style.css)**

```css
.image-effect {
    filter: grayscale(50%) blur(2px);
    transition: filter 0.3s ease;
}

.image-effect:hover {
    filter: grayscale(0%) blur(0);
}
```

**HTML (index.html)**

```html
<img src="photo.jpg" alt="Sample Image" class="image-effect">
```

## Advanced Hover Effects with Sibling Selectors

Using sibling selectors combined with pseudo-classes can create sophisticated hover effects.

**CSS (style.css)**

```css
.container {
    display: flex;
}

.item {
    flex: 1;
    background: lightblue;
    padding: 20px;
    margin: 10px;
    transition: transform 0.3s;
}

.item:hover + .item {
    transform: scale(1.1);
}
```

**HTML (index.html)**

```html
<div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
</div>
```

These examples illustrate some of the more sophisticated techniques available in CSS that can significantly enhance the interactivity and style of web pages

Each example demonstrates a feature that can be mixed, matched, or expanded upon to fit specific design needs and creative ideas



