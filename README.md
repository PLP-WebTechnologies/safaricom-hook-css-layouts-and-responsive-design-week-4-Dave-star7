# Assignment: Responsive Web Design

## Objective:
Create a responsive webpage using modern CSS techniques, specifically Flexbox, Grid, and Media Queries. The goal is to ensure the webpage adapts gracefully to various screen sizes.

## Assignment Tasks

### Designing a Responsive Layout
a. Create a webpage with the following sections:

Header (including a logo and navigation links).
Main content area (with two columns: one for text content and the other for an image).
Footer (with links to social media and a copyright notice).
b. Use Flexbox to style the navigation menu in the header.
c. Use CSS Grid to structure the main content area.

### Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically.
Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns.
Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.

### Bonus

Add animations or transitions when resizing the screen.



<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Web Design</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Header Section -->
  <header>
    <div class="logo">My Logo</div>
    <nav class="nav-menu">
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Main Content Section -->
  <main>
    <div class="text-content">
      <h1>Welcome to Responsive Web Design</h1>
      <p>This is a demonstration of a responsive webpage using Flexbox, Grid, and Media Queries.</p>
    </div>
    <div class="image-content">
      <img src="https://via.placeholder.com/500x300" alt="Sample Image">
    </div>
  </main>

  <!-- Footer Section -->
  <footer>
    <div class="footer-links">
      <a href="#facebook">Facebook</a>
      <a href="#twitter">Twitter</a>
      <a href="#instagram">Instagram</a>
    </div>
    <p>&copy; 2024 My Responsive Page</p>
  </footer>
</body>
</html>


/* General Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body Styling */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #333;
  margin: 0;
  padding: 0;
}

/* Header Section */
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #007bff;
  color: #fff;
}

header .logo {
  font-size: 1.5rem;
  font-weight: bold;
}

header .nav-menu {
  display: flex;
  gap: 20px;
}

header .nav-menu a {
  color: #fff;
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s ease;
}

header .nav-menu a:hover {
  color: #ddd;
}

/* Main Content Section */
main {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  padding: 20px;
}

main .text-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

main .text-content h1 {
  font-size: 2rem;
  margin-bottom: 10px;
}

main .text-content p {
  font-size: 1rem;
}

main .image-content img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

/* Footer Section */
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
  background-color: #333;
  color: #fff;
}

footer .footer-links {
  display: flex;
  gap: 20px;
  margin-bottom: 10px;
}

footer .footer-links a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s ease;
}

footer .footer-links a:hover {
  color: #007bff;
}

/* Media Queries */
@media screen and (max-width: 600px) {
  header {
    flex-direction: column;
    text-align: center;
  }

  .nav-menu {
    flex-direction: column;
    gap: 10px;
  }

  main {
    grid-template-columns: 1fr;
  }
}

@media screen and (min-width: 601px) and (max-width: 1024px) {
  main {
    grid-template-columns: 1fr;
  }
}

@media screen and (min-width: 1024px) {
  main {
    grid-template-columns: 1fr 1fr;
  }
}

/* Bonus: Animations */
header, main, footer {
  transition: all 0.5s ease-in-out;
}

