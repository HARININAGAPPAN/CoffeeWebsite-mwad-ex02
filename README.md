# Ex02 – Commercial Website

## Date:
02-11-2026

## AIM

To design and develop a commercial website using HTML and CSS Flexbox with a professional layout, navigation bar, menu section, about section, and contact details.

## ALGORITHM

### STEP 1
Create an HTML file (`index.html`).

### STEP 2
Create a CSS file (`style.css`).

### STEP 3
Include a navigation bar with links to different sections of the website.

### STEP 4
Create a homepage with the website name, heading, description, and Explore Menu button.

### STEP 5
Add an About Us section to provide information about the coffee shop.

### STEP 6
Create a menu section displaying different coffee varieties and their prices.

### STEP 7
Add a Contact Us section with email, phone number, and location details.

### STEP 8
Define global styles for fonts, colors, margins, and padding.

### STEP 9
Style the header, navigation bar, homepage, and content sections using CSS.

### STEP 10
Use CSS Flexbox to arrange the menu cards and navigation links.

### STEP 11
Add hover effects, transitions, background images, and shadows to improve the website appearance.

### STEP 12
Use media queries to make the website responsive on different screen sizes.

### STEP 13
Add a footer with copyright information.

### STEP 14
Open the HTML file in a browser and check the website layout and functionality.

### STEP 15
Upload the project files to GitHub and deploy the website using GitHub Pages.

## PROGRAM
index
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bean Bliss - Coffee Shop</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header>
        <nav>
            <h2 class="logo">☕ Bean Bliss</h2>

            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Start Your Day With Fresh Coffee</h1>
            <p>Experience the perfect blend of taste, aroma and happiness.</p>
            <a href="#menu" class="btn">Explore Menu</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <h2>About Us</h2>
        <p>
            Welcome to Bean Bliss! We serve freshly brewed coffee
            made from carefully selected coffee beans.
            Our goal is to make every coffee moment special.
        </p>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="menu">
        <h2>Our Special Menu</h2>

        <div class="menu-container">

            <div class="menu-card">
                <h3>☕ Cappuccino</h3>
                <p>Rich espresso with steamed milk.</p>
                <h4>₹120</h4>
            </div>

            <div class="menu-card">
                <h3>☕ Latte</h3>
                <p>Smooth coffee with creamy milk.</p>
                <h4>₹150</h4>
            </div>

            <div class="menu-card">
                <h3>☕ Espresso</h3>
                <p>Strong and freshly brewed coffee.</p>
                <h4>₹100</h4>
            </div>

        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <p>Email: beanbliss@gmail.com</p>
        <p>Phone: +91 98765 43210</p>
        <p>Location: Chennai, India</p>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2026 Bean Bliss Coffee Shop. All Rights Reserved.</p>
    </footer>

</body>
</html>
```
css
```

/* General Styling */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background-color: #fffaf3;
    color: #333;
}

/* Navigation Bar */
header {
    background-color: #3e2723;
    padding: 20px 8%;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    color: #fff;
    font-size: 26px;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 30px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    font-size: 16px;
}

nav ul li a:hover {
    color: #ffcc80;
}

/* Home Section */
.hero {
    height: 500px;
    background: linear-gradient(
        rgba(0, 0, 0, 0.55),
        rgba(0, 0, 0, 0.55)
    ),
    url("https://images.unsplash.com/photo-1445116572660-236099ec97a0")
    center/cover no-repeat;

    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
}

.hero-content h1 {
    font-size: 45px;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 18px;
    margin-bottom: 30px;
}

.btn {
    background-color: #ff9800;
    color: white;
    padding: 13px 28px;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
}

.btn:hover {
    background-color: #e68900;
}

/* About Section */
.about {
    padding: 70px 15%;
    text-align: center;
}

.about h2,
.menu h2,
.contact h2 {
    font-size: 32px;
    color: #5d4037;
    margin-bottom: 25px;
}

.about p {
    font-size: 18px;
    line-height: 1.8;
}

/* Menu Section */
.menu {
    padding: 60px 8%;
    text-align: center;
    background-color: #f5e6d3;
}

.menu-container {
    display: flex;
    justify-content: center;
    gap: 25px;
    flex-wrap: wrap;
}

.menu-card {
    background-color: white;
    padding: 35px 25px;
    width: 260px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    transition: transform 0.3s;
}

.menu-card:hover {
    transform: translateY(-10px);
}

.menu-card h3 {
    color: #6d4c41;
    margin-bottom: 15px;
}

.menu-card p {
    margin-bottom: 15px;
    line-height: 1.5;
}

.menu-card h4 {
    color: #e67e22;
    font-size: 22px;
}

/* Contact Section */
.contact {
    padding: 60px 20px;
    text-align: center;
}

.contact p {
    margin: 12px;
    font-size: 17px;
}

/* Footer */
footer {
    background-color: #3e2723;
    color: white;
    text-align: center;
    padding: 20px;
}

/* Responsive Design */
@media (max-width: 600px) {

    nav {
        flex-direction: column;
        gap: 20px;
    }

    nav ul {
        gap: 15px;
        flex-wrap: wrap;
        justify-content: center;
    }

    .hero-content h1 {
        font-size: 30px;
    }

    .hero-content p {
        font-size: 16px;
    }

    .about {
        padding: 50px 8%;
    }
}
```


## OUTPUT

![alt text](image.png)

## RESULT

Thus, a commercial website was successfully designed and developed using HTML and CSS Flexbox with navigation links, homepage, about section, menu cards, contact details, and footer.