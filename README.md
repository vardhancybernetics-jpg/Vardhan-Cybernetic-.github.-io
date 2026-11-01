
<!DOCTYPE html>
<html>
<head>
<title>Vardhan Cybernetics</title>
<style>
body {
  margin: 0;
  font-family: Arial;
  background: #07111f;
  color: white;
}
header {
  background: #102944;
  padding: 25px;
  text-align: center;
}
h1 {color: #00eaff;}
nav {
  background: #183653;
  padding: 15px;
  text-align: center;
}
nav a {
  color: white;
  margin: 10px;
  text-decoration: none;
}
.hero {
  padding: 70px 15px;
  text-align: center;
}
h2 {color: #00eaff;}
.products {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(180px,1fr));
  gap: 15px;
  padding: 20px;
}
.card {
  background: #142944;
  padding: 15px;
  text-align: center;
  border-radius: 12px;
}
.card img {
  width: 100%;
  height: 150px;
  object-fit: contain;
  background: white;
}
button {
  background: #00eaff;
  border: none;
  padding: 12px;
  border-radius: 7px;
}
footer {
  background: #102944;
  text-align: center;
  padding: 20px;
}
</style>
</head>

<body>

<header>
<h1>VARDHAN CYBERNETICS</h1>
<p>Robotics | Electronics | Innovation</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#inventions">Inventions</a>
<a href="#shop">Shop</a>
<a href="#contact">Contact</a>
</nav>

<div class="hero" id="home">
<h2>WELCOME TO THE FUTURE</h2>
<p>Discover Amazing Robotics and Electronics.</p>
</div>

<section id="inventions">
<h2 align="center">🚀 Vardhan Inventions</h2>
<div class="products">
<div class="card">
<img src="images/invention1.jpg">
<h3>My Invention 1</h3>
</div>
<div class="card">
<img src="images/invention2.jpg">
<h3>My Invention 2</h3>
</div>
</div>
</section>

<section id="shop">
<h2 align="center">🛒 Electronics Store</h2>
<div class="products" id="products"></div>
</section>

<section id="contact">
<h2 align="center">Contact Us</h2>
<p align="center">Vardhan Cybernetics</p>
</section>

<footer>
© 2026 Vardhan Cybernetics
</footer>

<script>
let items = [
["Arduino UNO",450],
["ESP32",350],
["Servo Motor",150],
["DC Motor",80],
["Ultrasonic Sensor",100],
["Breadboard",90],
["LED",50],
["Jumper Wires",60],
["Battery",200],
["Robotics Kit",999]
];

let html = "";

items.forEach((item,i) => {
html += `
<div class="card">
<img src="https://placehold.co/250x150?text=${encodeURIComponent(item[0])}">
<h3>${item[0]}</h3>
<p>₹${item[1]}</p>
<button onclick="alert('Added ${item[0]} to cart')">
Add to Cart
</button>
</div>`;
});

document.getElementById("products").innerHTML = html;
</script>

</body>
</html>
