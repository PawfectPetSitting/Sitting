<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pawfect Pet Sitting</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Pawfect Pet Sitting</h1>
        <p>Tail-Wagging Care for Your Furry Friends!</p>
        <nav>
            <ul>
                <li><a href="#services">Services</a></li>
                <li><a href="#custom-package">Build Your Package</a></li>
                <li><a href="#contact">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <section id="services">
        <h2>Our Services</h2>
        <ul>
            <li>Daily Visits - $25 per visit</li>
            <li>Overnight Stays - $50 per night</li>
            <li>Dog Walking - $15 per walk</li>
            <li>Special Needs Care - Custom pricing</li>
        </ul>
    </section>

    <section id="custom-package">
        <h2>Build Your Custom Package</h2>
        <form id="package-form">
            <label for="pet-type">Pet Type:</label>
            <select id="pet-type">
                <option>Dog</option>
                <option>Cat</option>
                <option>Other</option>
            </select>

            <label for="visits">Number of Visits:</label>
            <input type="number" id="visits" min="1" value="1">

            <label for="overnight">Overnight Stay:</label>
            <input type="checkbox" id="overnight">

            <label for="special-needs">Special Needs Care:</label>
            <input type="checkbox" id="special-needs">

            <h3 id="total-price">Total Price: $0</h3>
            <button type="submit">Submit Request</button>
        </form>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <p>Email: support@pawfectpets.com</p>
        <p>Phone: (555) 123-4567</p>
    </section>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f9f9f9;
}

header {
    background-color: #ffcc80;
    padding: 20px;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

section {
    padding: 20px;
    background: #fff;
    margin: 20px auto;
    width: 60%;
    border-radius: 10px;
}

button {
    background: #ff9800;
    padding: 10px;
    border: none;
    cursor: pointer;
}
document.getElementById("package-form").addEventListener("input", function() {
    let visits = parseInt(document.getElementById("visits").value) * 25;
    let overnight = document.getElementById("overnight").checked ? 50 : 0;
    let specialNeeds = document.getElementById("special-needs").checked ? 30 : 0;

    let totalPrice = visits + overnight + specialNeeds;
    document.getElementById("total-price").textContent = "Total Price: $" + totalPrice;
});
