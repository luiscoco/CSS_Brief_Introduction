# CSS: brief introduction

https://www.w3schools.com/css/css_examples.asp

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







