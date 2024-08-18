
# WDE04 CSS Box Model and Display Properties

### Description
In this assignment, we will explore the CSS box model togethe. which defines how the different parts of a box (content, padding, border, and margin) interact with each other and with surrounding elements. You will learn how to manipulate these properties to create different layouts and how the display properties (`block`, `inline`, `inline-block`) affect the flow and positioning of elements on the page. By the end of this exercise, you should be comfortable working with the CSS box model and understand how display properties influence the structure of a webpage.

![Screenshot of the finished webpage](./assets/images/example.png)

## Project Description


## Project Structure

Below is an example of the project structure for this assignment:

```plaintext
project-folder/
├── index.html
└── styles.css
```

## Setup Steps

1. **Create a New Project Folder**:  
   Start by creating a new folder on your local machine for this project.

2. **Create Blank HTML and CSS Files**:  
   Inside your project folder, create two blank files: `index.html` and `styles.css`.

3. **Open the Project in Your Code Editor**:  
   Use a code editor like Visual Studio Code to open the project folder and start editing the files.

4. **Open index.html in the Browser**:  
   Launch the `index.html` file in your preferred web browser to see the initial layout.

## Instructions

You are now ready to begin coding your CSS Box Model and Display Properties!

### HTML Coding

Start by creating the basic HTML structure. Below is a sample code snippet:

\`\`\`html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Box Model</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>CSS Box Model and Display Properties</h1>
    </header>
    <main>
        <section class="box-model">
            <div class="box">Box 1</div>
            <div class="box">Box 2</div>
            <div class="box">Box 3</div>
        </section>
    </main>
</body>
</html>
\`\`\`

**Explanation:**  
This basic HTML code provides the skeleton of the webpage. It includes a `header` for the title and a `main` section containing a `section` with three `div` elements that will be styled using the CSS box model.

### CSS Coding

Next, let's style the elements using CSS. Below is a sample code snippet:

\`\`\`css
/* Basic CSS Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; /* Ensures padding and border are included in element's total width and height */
}

/* Style the header */
header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

/* Style the boxes */
.box-model {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
}

.box {
    background-color: #4CAF50;
    border: 5px solid #333;
    padding: 20px;
    margin: 10px;
    width: 150px;
    height: 150px;
    text-align: center;
    line-height: 110px; /* Centers the text vertically */
    color: #fff;
    font-weight: bold;
}
\`\`\`

**Explanation:**  
- **CSS Reset**: The `box-sizing: border-box;` ensures that padding and borders are included in the width and height of the elements, which helps maintain the layout consistency.
- **Header Styling**: The header is given a background color, text color, and padding to make it stand out.
- **Box Styling**: The `.box-model` section uses Flexbox to arrange the boxes evenly. Each `.box` has padding, margin, border, width, and height defined to showcase the box model properties.

## Testing the Project

After implementing the HTML and CSS code, test the project by:
1. Resizing the browser window to see how the boxes and other elements respond.
2. Experimenting with different values for `margin`, `padding`, `border`, and `display` properties to see their effects.
3. Trying out different display properties like `inline`, `block`, and `inline-block` on the boxes to observe changes in layout behavior.

## Conclusion

By completing this exercise, you should have a solid understanding of the CSS box model and how to apply it in web design. You have also learned about different display properties and their impact on element positioning and flow within a webpage.

---

© All rights reserved to ThriveDX
