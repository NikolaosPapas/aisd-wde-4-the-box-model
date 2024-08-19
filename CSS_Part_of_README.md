
## Now let's add CSS code to style your page
Open the `styles.css` file in the `TheBoxModel` folder and add the following code to style your webpage:

### 1. CSS Reset
Before diving into the box model, it's important to start with a CSS reset. This ensures consistent styling across different browsers by removing default margins, padding, and other styles.

```css
/* CSS Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

#### Explanation:
- `* { ... }`: The asterisk `*` is a universal selector that targets all elements on the page.
- `margin: 0; padding: 0;`: This resets the default margin and padding applied by browsers to most elements.
- `box-sizing: border-box;`: This ensures that padding and border widths are included within the element's specified width and height, making the box model easier to work with.

### 2. Styling the Body
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

#### Explanation:
- `font-family: Arial, sans-serif;`: Sets the font to Arial, with a fallback to sans-serif.
- `line-height: 1.6;`: Adjusts the spacing between lines of text for better readability.
- `background-color: #f4f4f4;`: Sets a light gray background color.
- `color: #333;`: Changes the text color to a dark gray for better contrast.
- `padding: 20px;`: Adds padding inside the body to prevent the content from touching the edges of the browser window.

### 3. Styling the Header
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

#### Explanation:
- `background-color: #35424a;`: Gives the header a dark slate color.
- `color: #ffffff;`: Changes the text color to white for contrast against the dark background.
- `padding: 20px 0;`: Adds vertical padding to the header, with no horizontal padding.
- `text-align: center;`: Centers the text within the header.
- `margin-bottom: 20px;`: Adds space below the header, separating it from the content that follows.

### 4. Styling the Navigation
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

#### Explanation:
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

### 5. Styling the Main Content and Sidebar
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

#### Explanation:
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

### 6. Styling the Footer
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
