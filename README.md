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








**Reminder:** Use your AI assistant to ask questions and troubleshoot issues.

🌟 **Awesome work! You have successfully built a webpage layout using the CSS box model and display properties.** 🌟
