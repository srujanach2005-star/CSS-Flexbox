## 📅 Day 6: CSS Flexbox

## 🔹 1️⃣ What is Flexbox?
-Flexbox is a 1-dimensional layout system used to arrange items in:
-A row
-OR a column

# To activate Flexbox, use:
display: flex;

# 🔹 2️⃣ display: flex
# ✅ Step 1: Basic Example
HTML :
<div class="container">
  <div class="box">1</div>
  <div class="box">2</div>
  <div class="box">3</div>
</div>

CSS
.container {
  display: flex;
}

.box {
  width: 100px;
  height: 100px;
  background: lightblue;
  margin: 5px;
}

-👉 Now items automatically align in a row.

# 🔹 3️⃣ flex-direction

Controls the direction of items.

flex-direction: row;       
flex-direction: column;
flex-direction: row-reverse;
flex-direction: column-reverse;

# Example:
.container {
  display: flex;
  flex-direction: column;
}

-👉 Items will stack vertically.

# 🔹 4️⃣ justify-content

Controls alignment on the main axis (row direction by default).

justify-content: flex-start;
justify-content: center;
justify-content: flex-end;
justify-content: space-between;
justify-content: space-around;
justify-content: space-evenly;

## Example:
.container {
  display: flex;
  justify-content: center;
}

-👉 Items move to the center horizontally.

## 🔹 5️⃣ align-items

Controls alignment on the cross axis (vertical by default).

align-items: stretch;
align-items: center;
align-items: flex-start;
align-items: flex-end;

## Example:
.container {
  display: flex;
  height: 300px;
  align-items: center;
}

-👉 Items align vertically center.

# 🔹 6️⃣ gap

Adds space between flex items.

gap: 20px;

# Example:

.container {
  display: flex;
  gap: 15px;
}

-👉 Adds equal spacing between items.

## 🟢 PROJECT 1: Build a Navbar Using Flexbox
# HTML :
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Flexbox Layout</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- NAVBAR -->
    <nav class="navbar">
        <div class="logo">FlexBrand</div>

        <ul class="menu">
            <li><a href="#">Home</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Portfolio</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero">
        <h1>Flexbox Layout Example</h1>
        <p>Simple, clean and responsive design using Flexbox</p>
    </section>

    <!-- CARD SECTION -->
    <section class="cards">
        <div class="card">HTML</div>
        <div class="card">CSS</div>
        <div class="card">JavaScript</div>
        <div class="card">React</div>
        <div class="card">Node.js</div>
       
    </section>

</body>
</html>

## CSS:
/* ===== RESET ===== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', sans-serif;
    background: #f8f9fa;
    color: #333;
}

/* ===== NAVBAR ===== */

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 18px 60px;
    background: #111827;
}

.logo {
    font-size: 22px;
    font-weight: bold;
    color: white;
}

.menu {
    list-style: none;
    display: flex;
    gap: 30px;
}

.menu li a {
    text-decoration: none;
    color: white;
    font-weight: 500;
    transition: 0.3s ease;
}

.menu li a:hover {
    color: #3b82f6;
}

/* ===== HERO SECTION ===== */

.hero {
    height: 300px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 15px;
    text-align: center;
}

.hero h1 {
    font-size: 36px;
}

.hero p {
    color: #555;
}

/* ===== CARD SECTION ===== */

.cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 25px;
    padding: 40px 60px;
}

.card {
    width: 220px;
    height: 150px;
    background: white;
    border-radius: 12px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.08);

    display: flex;
    justify-content: center;
    align-items: center;

    font-size: 20px;
    font-weight: 600;

    transition: 0.3s ease;
}

.card:hover {
    transform: translateY(-8px);
    background: #3b82f6;
    color: white;
}

/* ===== RESPONSIVE ===== */

@media (max-width: 768px) {

    .navbar {
        flex-direction: column;
        gap: 15px;
    }

    .menu {
        flex-direction: column;
        align-items: center;
    }

    .hero h1 {
        font-size: 28px;
    }
}

## OUT PUT :
![Day-6 Output](day-6/img/day-6-output.png)
