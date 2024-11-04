Please create an index.html file and a style.css file after opening a codespace enviroment. Link your stylesheet using the instructions below then use the table below to make each reference

---

To link a CSS stylesheet to an HTML file, follow these steps:

1. **Create the CSS File**:
   - Write your CSS code in a file with the extension `.css` (e.g., `styles.css`).

2. **Link the CSS File in HTML**:
   - In your HTML document, add a `<link>` tag inside the `<head>` section to connect your CSS file.
   - The `<link>` tag should look like this:

     ```html
     <link rel="stylesheet" href="styles.css">
     ```

   - Here’s what each part of this line means:
     - `rel="stylesheet"` tells the browser that this link is for a stylesheet.
     - `href="styles.css"` provides the path to your CSS file. Replace `"styles.css"` with the correct path if your CSS file is in a different folder (e.g., `"css/styles.css"` if it’s inside a folder named `css`).

3. **Example HTML Structure**:

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>My Web Page</title>
     <link rel="stylesheet" href="styles.css">
   </head>
   <body>
     <h1>Welcome to My Web Page</h1>
     <p>This page is styled using an external CSS file.</p>
   </body>
   </html>
   ```
---
4. **Check the Link**:
   - After linking, check your HTML file in a browser to make sure the CSS styles are applied correctly. If they’re not showing, double-check the `href` path to ensure it matches the location of your CSS file.
---

**Preview**

Go to terminal below and exexute the following commands

. npm i -g http-server 
. http-server

---

This approach keeps your CSS code separate from HTML, which is best practice for organizing and maintaining your code.
Here's a table that outlines how to create **classes**, **IDs**, and **elements** in HTML, along with how to reference each in CSS.

| **Selector Type** | **HTML Code Example** | **CSS Code Example** | **Description** |
|-------------------|-----------------------|-----------------------|-----------------|
| **Element Selector** | ```<p>This is a paragraph.</p>``` | ```p { color: blue; }``` | Styles all `<p>` elements. |
| **Class Selector** | ```<div class="container">Content here</div>``` | ```.container { background-color: lightgray; }``` | Styles any element with the class `container`. |
| **ID Selector** | ```<h1 id="main-title">Welcome</h1>``` | ```#main-title { font-size: 2em; }``` | Styles the element with the unique ID `main-title`. |
| **Multiple Classes** | ```<p class="text highlight">Important text</p>``` | ```.text { font-size: 1em; } .highlight { color: red; }``` | Applies multiple classes `text` and `highlight` for combined styling. |
| **Descendant Selector** | ```<div class="container"><p>Text inside container</p></div>``` | ```.container p { color: green; }``` | Styles `<p>` elements that are inside `.container` elements only. |
| **Child Selector** | ```<ul class="menu"><li>Item 1</li></ul>``` | ```.menu > li { color: purple; }``` | Styles `<li>` elements that are direct children of `.menu`. |
| **Adjacent Sibling Selector** | ```<h2>Heading</h2><p>Paragraph after heading</p>``` | ```h2 + p { margin-top: 10px; }``` | Styles `<p>` elements that immediately follow an `<h2>`. |
| **General Sibling Selector** | ```<h2>Heading</h2><p>Paragraph 1</p><p>Paragraph 2</p>``` | ```h2 ~ p { color: gray; }``` | Styles all `<p>` elements that are siblings after an `<h2>`. |
| **Pseudo-Class Selector** | ```<a href="#">Link</a>``` | ```a:hover { color: orange; }``` | Styles links (`<a>`) when hovered over. |
| **Attribute Selector** | ```<input type="text" placeholder="Enter name">``` | ```input[type="text"] { border: 1px solid blue; }``` | Styles `<input>` elements with the `type="text"` attribute. |

---

### How to Use These in HTML and CSS

- **HTML**: Place the HTML code in your `.html` file within the `<body>` tags where you want the content to appear.
- **CSS**: Place the CSS code in your `.css` file or within `<style>` tags in the HTML `<head>`. Link the CSS file to the HTML file using `<link rel="stylesheet" href="styles.css">`.

These selectors help organize styling, target elements precisely, and enhance web page design!

---



### 1. HTML Document (index.html)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Selectors Practice</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header id="main-header">
    <h1>Welcome to CSS Selectors Practice</h1>
    <p class="subtitle">Learn how to use IDs, classes, and tags with CSS.</p>
  </header>

  <section class="content">
    <article id="intro">
      <h2>Introduction</h2>
      <p>This section introduces basic concepts for using CSS selectors to style HTML.</p>
    </article>

    <article id="examples">
      <h2>Examples</h2>
      <p class="highlight">Use different selectors to change the appearance of this text.</p>
      <p class="highlight">Try styling elements based on IDs, classes, and tags.</p>
    </article>

    <footer id="main-footer">
      <p>&copy; 2024 CSS Practice</p>
      <p class="footer-link">Learn more about CSS on <a href="https://www.w3schools.com/css/">W3Schools</a>.</p>
    </footer>
  </section>
</body>
</html>
```

### 2. CSS File (styles.css)

```css
/* Tag selector */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f5;
}

/* ID selectors */
#main-header {
  background-color: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

#intro {
  background-color: #e6f7ff;
  padding: 15px;
  border-left: 5px solid #0099cc;
}

#examples {
  background-color: #e6ffe6;
  padding: 15px;
  border-left: 5px solid #33cc33;
}

/* Class selectors */
.subtitle {
  font-size: 1.2em;
  color: #666;
}

.highlight {
  font-weight: bold;
  color: #005580;
}

/* Element selector */
footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px;
}

.footer-link {
  color: #ffa500;
  text-decoration: none;
}

/* Tag selector with class */
a:hover {
  color: #ff4500;
}
```

---


### CSS Challenges

1. **Customize Header and Footer Colors**  
   - Change the background color and text color of the `#main-header` and `#main-footer`. Choose colors that contrast well with each other and the body background.

2. **Add Borders and Padding**  
   - Add a border around each `article` section (`#intro` and `#examples`). Adjust the border thickness, style (solid, dotted, dashed), and color.
   - Add padding inside each section to ensure the text does not touch the borders.

3. **Modify Font Properties**  
   - Change the font size and style of the `h2` tags within each `article` section.
   - Set the font for `.subtitle` to a different font family from the rest of the page and adjust its size and color.

4. **Background Colors for Classes**  
   - Add a light background color to all paragraphs with the `.highlight` class.
   - Try using RGBA values (e.g., `rgba(0, 0, 0, 0.1)`) to make the background semi-transparent.

5. **Hover Effects on Links**  
   - Modify the link styling in the footer so that links have different colors on hover and active states.
   - Add an underline effect on hover to emphasize links in `.footer-link`.

6. **Experiment with Margins and Spacing**  
   - Adjust the `margin` around each `article` section to add space between them.
   - Center the entire `section` element on the page by adding `margin: auto` and setting a `max-width` (e.g., `600px`).

7. **Style Based on Hierarchy**  
   - Add styling to make only the first paragraph inside `#examples` bold.
   - Try selecting the `p` tags only within `#intro` and give them a distinct color or font style.

8. **Use `nth-child` Selectors**  
   - Style every second paragraph with the `.highlight` class in `#examples` using the `nth-child` selector.
   - Experiment with other `nth-child` patterns to alternate background colors between different elements.

9. **Text Alignment and Shadow Effects**  
   - Center-align the text in `#main-header` and add a subtle shadow effect.
   - Add a shadow to the text in each `h2` tag, making it stand out against the background.

10. **Transform and Transition Effects**  
    - Add a transition effect on the `.footer-link` so that the color changes smoothly when hovered.
    - Apply a slight rotation or scale effect on the `h1` title in `#main-header` when the user hovers over it to make it pop.

---

Each of these challenges will give you a chance to explore CSS styling techniques, work with various selectors, and learn more about styling for layout and interactivity! Let me know if you'd like examples of any of these.
