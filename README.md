# WDE04 CSS Box Model and Display Properties

**Description:**
In this assignment, we will explore the CSS box model together, which defines how the different parts of a box—content, padding, border, and margin—interact with each other and with surrounding elements. You’ll learn how to manipulate these properties to create diverse layouts and how various display properties (block, inline, inline-block) affect the flow and positioning of elements on a webpage. By the end of this exercise, you should feel confident working with the CSS box model and understand how display properties influence the overall structure of a webpage.

##
What we will be building together
![Screenshot of the finished webpage](./assets/images/example.png)
##

## Project Structure

```plaintext
project-folder/
├── index.html
└── styles.css
```

1. **Create the Project Folder and Files**
   - Create a folder named `TheBoxModel` to store all your project files.
   - Inside the `TheBoxModel` folder, create a file named `index.html`. This will be your main HTML file.
   - Also, in the `BasicCSS` folder, create another file named `styles.css`. This file will contain the CSS used to style your HTML content.

### Step-by-Step Breakdown of the HTML File
   Now that you have your files set up, start by adding content to the `index.html` file.

1. **HTML Boilerplate**
Start with the basic HTML5 boilerplate to set up the foundation of your document:

\`\`\`html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Display Types Showcase</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

<!-- Display code goes here  -->

</body>
</html>
\`\`\`

#### Explanation:
- \`<!DOCTYPE html>\` declares the document as an HTML5 document.
- \`<html lang="en">\` specifies the language of the document as English.
- The \`<head>\` section includes metadata such as character encoding (\`<meta charset="UTF-8">\`) and the viewport settings for responsiveness (\`<meta name="viewport" content="width=device-width, initial-scale=1.0">\`).
- The \`<title>\` tag sets the title of the webpage, which appears in the browser tab.
- The \`<link rel="stylesheet" href="styles.css">\` tag links the external CSS file to style the HTML content.
- The \`<body>\` tag contains all the content of the webpage that will be displayed in the browser.
- The \`</body>\` and \`</html>\` tags close the body content and the HTML document, respectively.

2. **Adding Content to the Body**

Next, add the main content inside the \`<body>\` tag:

\`\`\`html
<body>
  <h1 class="page-title">CSS Display Types Showcase</h1>
  <div class="container">
    <div class="card block-card">
      <p>I am a <strong>block</strong> element. I take up less width but still start on a new line.</p>
    </div>

    <div class="inline-container">
      <span class="card inline-card">I am an <strong>inline</strong> element.</span>
      <span class="card inline-card">Another <strong>inline</strong> element.</span>
    </div>

    <div class="inline-block-container">
      <div class="card inline-block-card">I am an <strong>inline-block</strong> element. I respect width and height properties.</div>
      <div class="card inline-block-card">Another <strong>inline-block</strong> element beside me.</div>
    </div>
  </div>
\`\`\`

#### Explanation:
- The content is wrapped inside the \`<body>\` tag.
- \`<h1 class="page-title">\` is the main heading of the page. The class \`page-title\` can be used to style the heading in CSS.
- \`<div class="container">\` groups the content and helps with layout styling.
- \`<div class="card block-card">\` represents a block element with a specific class \`block-card\`.
- \`<span class="card inline-card">\` represents inline elements with the class \`inline-card\`.
- \`<div class="inline-block-container">\` groups inline-block elements, allowing them to be styled and aligned together.
- \`<div class="card inline-block-card">\` represents inline-block elements with the class \`inline-block-card\`.

3. **Adding the Footer**

Finally, include a footer to summarize the differences between display types:

\`\`\`html
<footer class="footer">
  <p class="footer-title">Summary of Differences:</p>
  <p><strong>Block:</strong> Takes up the full width of its container and forces a line break. Examples: div, p, section.</p>
  <p><strong>Inline:</strong> Takes up only as much space as its content needs and stays inline. Examples: span, a, em.</p>
  <p><strong>Inline-Block:</strong> Behaves like an inline element but allows width and height to be set. Examples: img, button, input.</p>
</footer>
\`\`\`

### Explanation:
- \`<footer>\` contains the footer content, typically placed at the bottom of the webpage.
- \`<p class="footer-title">\` is the title of the footer content, which can be styled separately.
- Each \`<p>\` tag provides a summary of the different display types, including examples of HTML elements that use these display properties.

##

By following these steps, you've successfully built a simple HTML document that explains and demonstrates the differences between block, inline, and inline-block elements. 


### Now lets add CSS code to style your page
Open the `styles.css` file in the `TheBoxModel` folder and add the following code to style your webpage:


1. **CSS Reset**
Before diving into the box model, it's important to start with a CSS reset. This ensures consistent styling across different browsers by removing default margins, padding, and other styles.

```css
/* CSS Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

### Explanation:
- `* { ... }`: The asterisk `*` is a universal selector that targets all elements on the page.
- `margin: 0; padding: 0;`: This resets the default margin and padding applied by browsers to most elements.
- `box-sizing: border-box;`: This ensures that padding and border widths are included within the element's specified width and height, making the box model easier to work with.

2. **Styling the Body**
Next, let's apply some basic styling to the body element to set the font, background color, and layout.

```css
/* Body Styling */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f4f4f4;
    color: #333;
    padding: 20px;
}
```

### Explanation:
- `font-family: Arial, sans-serif;`: Sets the font to Arial, with a fallback to sans-serif.
- `line-height: 1.6;`: Adjusts the spacing between lines of text for better readability.
- `background-color: #f4f4f4;`: Sets a light gray background color.
- `color: #333;`: Changes the text color to a dark gray for better contrast.
- `padding: 20px;`: Adds padding inside the body to prevent the content from touching the edges of the browser window.

3. **Styling the Header**
Now let's style the header to make it stand out.

```css
/* Header Styling */
header {
    background-color: #35424a;
    color: #ffffff;
    padding: 20px 0;
    text-align: center;
    margin-bottom: 20px;
}
```

### Explanation:
- `background-color: #35424a;`: Gives the header a dark slate color.
- `color: #ffffff;`: Changes the text color to white for contrast against the dark background.
- `padding: 20px 0;`: Adds vertical padding to the header, with no horizontal padding.
- `text-align: center;`: Centers the text within the header.
- `margin-bottom: 20px;`: Adds space below the header, separating it from the content that follows.

4. **Styling the Navigation**
Next, let's style the navigation links to give them a horizontal layout.

```css
/* Navigation Styling */
nav {
    text-align: center;
    margin-bottom: 20px;
}

nav a {
    color: #35424a;
    text-decoration: none;
    padding: 10px 20px;
    border-radius: 5px;
    background-color: #e2e2e2;
    margin: 0 5px;
    display: inline-block;
}

nav a:hover {
    background-color: #c1c1c1;
}
```

### Explanation:
- `text-align: center;`: Centers the navigation links within the navigation bar.
- `nav a { ... }`: Styles each navigation link:
  - `color: #35424a;`: Sets the link text color.
  - `text-decoration: none;`: Removes the default underline from the links.
  - `padding: 10px 20px;`: Adds padding inside each link, making them look like buttons.
  - `border-radius: 5px;`: Rounds the corners of the buttons.
  - `background-color: #e2e2e2;`: Sets a light gray background color for the buttons.
  - `margin: 0 5px;`: Adds space between each button.
  - `display: inline-block;`: Ensures the links behave like inline elements but respect the padding and margin.
- `nav a:hover { ... }`: Changes the background color of the buttons when hovered over.

5. **Styling the Main Content and Sidebar**
Now let's style the main content and sidebar to create a simple two-column layout.

```css
/* Layout Styling */
.container {
    display: flex;
    margin-bottom: 20px;
}

.sidebar {
    background-color: #e2e2e2;
    padding: 20px;
    flex: 1;
    margin-right: 20px;
}

.main-content {
    background-color: #ffffff;
    padding: 20px;
    flex: 2;
}
```

### Explanation:
- `.container { ... }`: Sets up a flexbox container for a two-column layout:
  - `display: flex;`: Enables flexbox, allowing children to align horizontally.
  - `margin-bottom: 20px;`: Adds space below the container.
- `.sidebar { ... }`: Styles the sidebar:
  - `background-color: #e2e2e2;`: Sets a light gray background.
  - `padding: 20px;`: Adds padding inside the sidebar.
  - `flex: 1;`: Allows the sidebar to take up one part of the space.
  - `margin-right: 20px;`: Adds space between the sidebar and the main content.
- `.main-content { ... }`: Styles the main content area:
  - `background-color: #ffffff;`: Sets a white background.
  - `padding: 20px;`: Adds padding inside the main content area.
  - `flex: 2;`: Allows the main content to take up twice the space of the sidebar.

6. **Styling the Footer**
Finally, let's style the footer to match the header.

```css
/* Footer Styling */
footer {
    background-color: #35424a;
    color: #ffffff;
    text-align: center;
    padding: 10px 0;
    margin-top: 20px;
}
```

#### Explanation:
- `background-color: #35424a;`: Matches the footer's background color with the header.
- `color: #ffffff;`: Changes the text color to white for contrast.
- `text-align: center;`: Centers the text within the footer.
- `padding: 10px 0;`: Adds vertical padding to the footer, with no horizontal padding.
- `margin-top: 20px;`: Adds space above the footer, separating it from the content above.



##

🌟 **Awesome work! You have successfully built a webpage layout using the CSS box model and display properties.** 🌟

### Conclusion
In this assignment, you learned how to effectively use the CSS box model to control the spacing and layout of elements on a webpage. You also explored how different display properties, such as block and inline-block, influence the positioning of elements. By creating a basic webpage structure with a header, navigation, content area, sidebar, and footer, you gained practical experience in applying these concepts to build a responsive and well-organized webpage layout. Understanding these fundamental principles will be crucial as you continue to design and develop more complex web pages. Rember to use your AI assistant to ask questions and troubleshoot issues.

---
© All rights reserved to ThriveDX



