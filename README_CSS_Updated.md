
# CSS Breakdown

## 1. **CSS Reset**
```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #e0f7fa;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100vh;
}
```
**Explanation:**
- Resets default margins and padding for consistency.
- Sets the default font and background color.
- Utilizes `display: flex` to align content centrally with a column direction.

## 2. **Page Title Styling**
```css
.page-title {
    color: #00796b;
    margin: 20px 0;
    font-size: 1.4em;
    text-align: center;
}
```
**Explanation:**
- Styles the main page title with specific color, margin, and font size.
- Centers the text using `text-align: center`.

## 3. **Container Styling**
```css
.container {
    width: 80%;
    max-width: 1100px;
    padding: 40px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    text-align: center;
    margin-bottom: 20px;
}
```
**Explanation:**
- Defines the container's dimensions and adds padding.
- Sets a white background and adds a subtle shadow for a lifted effect.
- Rounds the corners using `border-radius`.

## Now let's take a look at the progress of our webpage unstyled.

<img src="./assets/images/example2.png" alt="Screenshot of the finished index.html" width="300" height="300" style="border: 2px solid black;">

