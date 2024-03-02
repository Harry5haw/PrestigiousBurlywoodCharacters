## make the menu so that it is vertically stacked

## Updated HTML Structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harry Shaw Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="header">
        <h1>Harry Shaw</h1>
        <nav class="burger-menu">
            <ul>
                <li><a href="#about">About Me</a></li>
                <li><a href="#cv">My CV</a></li>
                <li><a href="#github">Github</a></li>
                <li><a href="#other-projects">Other Projects</a></li>
                <li><a href="#film-reviews">Film Reviews</a></li>
            </ul>
        </nav>
    </header>

    <main class="content">
        <section id="about">
            <h2>About Me</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </section>
        <section id="cv">
            <h2>My CV</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </section>
        <section id="github">
            <h2>Github</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </section>
        <section id="other-projects">
            <h2>Other Projects</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </section>
        <section id="film-reviews">
            <h2>Film Reviews</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </section>
    </main>

    <script src="script.js"></script>
</body>
</html>
```

## Updated CSS Styling:

```css
/* Basic Styles */
body {
    font-family: sans-serif;
    margin: 0;
    padding: 0;
}

.header, .content {
    display: grid;
    grid-template-columns: 1fr;
    justify-items: center;
    align-items: center;
    min-height: 100vh;
}

/* Header Styles */
.header {
    background-color: #eee;
    padding: 20px;
}

h1 {
    font-size: 2em;
    margin: 0;
}

/* Burger Menu Styles */
.burger-menu {
    list-style: none;
    padding: 0;
    margin: 0;
}

.burger-menu li {
    display: block; /* Change to block for vertical stacking */
    padding: 5px 10px;
    border-radius: 5px;
    background-color: purple;
    margin: 5px 0; /* Adjust margin for spacing */
    transition: background-color 0.2s ease;
}

.burger-menu li a {
    color: white;
    text-decoration: none;
    text-shadow: 1px 1px black;
}

.burger-menu li:hover {
    background-color: #9b00ff; /* Adjust hover color */
}

/* Content Styles */
.content {
    background-color: #f5f5f5;
}

section {
    padding: 20px;
    background-color: white;
    border-radius: 5px;
    margin-top: 20px;
}

h2 {
    margin-bottom: 10px;
}
```

These changes adjust the `display` property of the menu items in the CSS to `block` instead of `inline-block`, which will stack them vertically instead of horizontally. Additionally, the margin property of the list items is adjusted slightly to maintain proper spacing.

```
Sources:
1. https://medium.com/samsung-internet-dev/making-an-ar-game-with-aframe-529e03ae90cb