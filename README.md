# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <link rel="stylesheet" href="box.css">
</head>
<body>

    <header>
        <nav class="navbar">
            <div class="logo">MyLogo</div>
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
            <div class="menu-toggle">&#9776;</div>
        </nav>
    </header>

    <main class="container">
        <section class="box">Box 1</section>
        <section class="box">Box 2</section>
        <section class="box">Box 3</section>
        <section class="box">Box 4</section>
    </main>

    <footer>
        <p>Wakanda Transformer</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>



* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
}


.navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333;
    padding: 1rem;
    color: white;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 1rem;
}

.nav-links li a {
    color: white;
    text-decoration: none;
}

.menu-toggle {
    display: none;
    font-size: 1.5rem;
    cursor: pointer;
}


.container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
    padding: 2rem;
    width: 80%;
}

.box {
    background: #007bff;
    color: white;
    padding: 2rem;
    text-align: center;
    border-radius: 8px;
}


@media (max-width: 768px) {
    .container {
        grid-template-columns: 1fr;
    }

    .nav-links {
        display: none;
        flex-direction: column;
        background: #444;
        position: absolute;
        top: 60px;
        right: 10px;
        padding: 1rem;
        border-radius: 5px;
    }

    .nav-links li {
        margin-bottom: 10px;
    }

    .menu-toggle {
        display: block;
    }
}

