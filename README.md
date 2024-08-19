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

2. **Create the HTML File**  
   Now that you have your files set up, start by adding content to the `index.html` file.

   ### HTML Boilerplate
   First, set up the basic structure of an HTML document. This is known as the boilerplate:

   ```html
   <!DOCTYPE html>
   <html lang="en">

   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>My Day as a Web Developer</title>
     <!-- link your CSS here  -->
   </head>

   <body>

    <!-- content code goes here  -->

   </body>

   </html>
   ```

   ### Explanation:
   - The `<!DOCTYPE html>` declaration defines the document type as HTML5.
   - The `<html lang="en">` tag specifies the language of the document.
   - The `<head>` section includes metadata like character encoding and viewport settings for responsiveness.
   - The `<title>` tag sets the title of the webpage, which appears in the browser tab.

3. **Linking the CSS File**
   After setting up the HTML boilerplate, the next step is to link your CSS file to the HTML document. This allows you to apply styling to the HTML elements.

   You should add the following `<link>` code **under the `<title>` tag but inside the `<head>` section only** of your HTML document:

   ```html
   <link rel="stylesheet" href="styles.css">
   ```

   ### Explanation:
   - The `<link rel="stylesheet" href="styles.css">` tag connects the HTML file to the CSS file.
   - The `rel="stylesheet"` attribute tells the browser that the linked file is a stylesheet.
   - The `href="styles.css"` attribute specifies the path to the CSS file. Since the `styles.css` file is located in the same folder (`BasicCSS`) as the `index.html` file, the path is simply `"styles.css"`.
   - **Important**: Ensure this `<link>` code is placed under the `<title>` tag and within the `<head>` section of your HTML document. This allows the browser to correctly identify and apply the CSS before rendering the body content.


4.  **Add Content to the Body**

Now that you've set up the basic structure, it's time to add the content that will be displayed on the webpage. This content will go between the opening `<body>` and closing `</body>` tags in your HTML file.

Here’s the code you'll be adding:

```html
<header>
    <h1>Welcome to My Webpage</h1>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
</nav>

<div class="container">
    <aside class="sidebar">
        <h2>Sidebar</h2>
        <p>This is the sidebar content.</p>
    </aside>

    <main class="main-content">
        <h2>Main Content</h2>
        <p>This is the main content area.</p>
    </main>
</div>

<footer>
    <p>&copy; 2024 My Webpage</p>
</footer>
```

### Explanation:

- **Placement:** All of this code will be placed inside the `<body>` tags. This is where the visible content of your webpage is defined.
  
- **Structure:**
  - The `<header>` section defines the title of your webpage.
  - The `<nav>` section creates navigation links for different sections of the page.
  - The `<div class="container">` groups the sidebar (`<aside>`) and the main content area (`<main>`).
  - The `<footer>` contains the copyright information.

### Reminder:

- Everything you add in this step should go between the open `<body>` and close `</body>` tags in your HTML file. The content you create here will be what users see when they visit your webpage.

By completing this step, you will have added all the primary content that will be displayed on your webpage.

5. **Test the HTML Structure**
   Before adding any CSS, open your `index.html` file in a browser to see how it looks. It should display plain text without any styling as seen below...

##
  <img src="./assets/images/example2.png" alt="Example of unstyled HTML" width="275" height="220">

##

## Now lets add CSS code to style your page
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


🌟 **Awesome work! You have successfully built a webpage layout using the CSS box model and display properties.** 🌟

##

### Conclusion
In this assignment, you learned how to effectively use the CSS box model to control the spacing and layout of elements on a webpage. You also explored how different display properties, such as block and inline-block, influence the positioning of elements. By creating a basic webpage structure with a header, navigation, content area, sidebar, and footer, you gained practical experience in applying these concepts to build a responsive and well-organized webpage layout. Understanding these fundamental principles will be crucial as you continue to design and develop more complex web pages. Rember to use your AI assistant to ask questions and troubleshoot issues.

--
© All rights reserved to ThriveDX



