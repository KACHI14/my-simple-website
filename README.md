# My Simple Website

## Project Overview

This project is a simple static website built using **HTML and CSS**. The website includes:

- A **homepage** with a header, navigation menu, and a content section.
- A **background image slideshow** effect using CSS animations.
- A **fixed header and footer** for better layout consistency.

This project is intended for practice and to reinforce knowledge of HTML and CSS structuring.

## Technologies Used

- **HTML5**: For structuring the web page.
- **CSS3**: For styling, layout, and animations.

---

## File Structure

```
/my-website
│── index.html   # Main HTML file
│── style.css    # Stylesheet file
│── image/       # Folder for background images
│── README.md    # This documentation
```

---

## Code Explanation

### 1. HTML Structure (`index.html`)

#### **Header Section**

```html
<header>
  <h1>Welcome to My Website</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>
```

- The `<header>` contains the **website title** and a **navigation menu**.
- The `<nav>` holds an unordered list (`<ul>`) of navigation links.

#### **Main Section**

```html
<section>
  <h2>The Home Page</h2>
  <p>Am a web developer newbie currently done watching HTML and CSS Video tutorials on YouTube, so I am trying to get better at what I learned by practicing.</p>
</section>
```

- Contains the **main content** of the homepage.
- Includes an `<h2>` for the section title and a `<p>` paragraph for description.

#### **Footer**

```html
<footer>
  <p> &copy; 2025 My Website</p>
</footer>
```

- Displays a **copyright message** at the bottom of the page.

#### **Sliding Background**

```html
<div class="sliding-background"></div>
```

- This `<div>` is used for the **background image slideshow** animation.

---

### 2. CSS Styling (`style.css`)

#### **General Styling**

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
}
```

- Sets the **global font** and removes default margin and padding.
- Uses **flexbox** to center content vertically and horizontally.

#### **Header and Navigation**

```css
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  color: white;
  padding: 15px 0;
  text-align: center;
  z-index: 1000;
}
nav ul {
  list-style: none;
  padding: 0;
}
nav ul li {
  display: inline;
  margin: 0 70px;
}
nav ul li a {
  color: white;
  text-decoration: none;
}
```

- The header is **fixed** at the top of the page.
- The navigation links are **inline** and evenly spaced.

#### **Section and Footer**

```css
section, footer {
  padding: 20px;
  text-align: center;
  background: rgba(0, 0, 0, 0.2);
  border-radius: 10px;
}
```

- Adds **padding** for better spacing.
- Uses a **semi-transparent black background** to improve readability.
- Applies **border-radius** for rounded corners.

#### **Sliding Background Animation**

```css
@keyframes backgroundSlide {
  0% { background-image: url("image/my1.jpeg"); }
  20% { background-image: url("image/kyz.jpeg"); }
  39% { background-image: url("image/my2.jpeg"); }
  66% { background-image: url("image/my3.jpeg"); }
  100% { background-image: url("image/my4.jpeg"); }
}
```

- Defines a **keyframe animation** that changes the background image at different intervals.

```css
.sliding-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  animation: backgroundSlide 30s infinite;
  z-index: -1;
}
```

- **Positions the sliding background** behind other elements.
- Uses `animation: backgroundSlide 30s infinite;` to create a **looping slideshow** effect.

---

## Author

- **Developer:** KACHi
- Date: 30/1/2025

