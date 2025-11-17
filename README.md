<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Chocostixx</title>
<style>
 body {
   margin: 0;
   font-family: Arial, sans-serif;
   background: #fff7e6;
   color: #4b2e19;
 }
 header {
   text-align: center;
   padding: 40px 20px;
 }
 .logo {
   font-size: 64px;
   font-weight: bold;
   color: #ff66cc;
   text-shadow: 0 0 5px #ffccff;
   position: relative;
 }
 .logo span {
   position: relative;
   display: inline-block;
 }
 .choc-drip {
   position: absolute;
   bottom: -10px;
   left: 0;
   width: 100%;
   height: 20px;
   background: url('CHOCOSTIXX TITLE.png') repeat-x;
 }
 nav {
   text-align: center;
   margin-top: 20px;
 }
 nav button {
   background: #ff66cc;
   color: white;
   border: none;
   padding: 12px 24px;
   border-radius: 20px;
   font-size: 18px;
   cursor: pointer;
 }
 .section {
   display: none;
   padding: 20px;
   text-align: center;
 }
 .product-grid {
   display: flex;
   justify-content: center;
   gap: 30px;
   flex-wrap: wrap;
 }
 .product {
   background: white;
   padding: 20px;
   border-radius: 20px;
   width: 250px;
   box-shadow: 0 4px 8px rgba(0,0,0,0.1);
 }
 .product img {
   width: 100%;
   border-radius: 15px;
 }
 .product button {
   background: #ff66cc;
   color: white;
   border: none;
   padding: 10px 20px;
   border-radius: 20px;
   cursor: pointer;
 }
 #cart-list {
   max-width: 400px;
   margin: 0 auto;
   background: white;
   padding: 20px;
   border-radius: 20px;
   box-shadow: 0 4px 8px rgba(0,0,0,0.1);
 }
</style>
</head>
<body>
<header>
 <div class="logo">Chocostixx<span class="choc-drip"></span></div>
 <p style="font-size:20px; margin-top:10px;">Get your fix with Chocostixx!</p>
 <nav>
   <button onclick="showSection('home')">Home</button>
   <button onclick="showSection('shop')">Shop</button>
   <button onclick="showSection('cart')">🛒 Trolley</button>
 </nav>
</header>

<section id="home" class="section" style="display:block;">
 <h1>Welcome to Chocostixx!</h1>
 <p>A fun, colourful, chocolate snack that twists up just like a glue stick!</p>
</section>

<section id="shop" class="section">
 <h1 style="font-size:40px; color:#ff66cc; text-shadow:0 0 5px #ffccff;">Check out our range!</h1>
 <div class="product-grid">
   <div class="product">
     <img src="CHOCOSTIXX ORIGINAL.png" alt="Original Chocostixx">
     <h3>Original Chocostixx</h3>
     <p>Milk chocolate with a swirl of white chocolate.</p>
     <button onclick="addToCart('Original Chocostixx', 2.99)">Add to trolley (£2.99)</button>
   </div>
   <div class="product">
     <img src="CHOCOSTIXX RASPBERRY RIPPLE.png" alt="Raspberry Chocostixx">
     <h3>Raspberry Chocostixx</h3>
     <p>Milk chocolate with a pink raspberry swirl.</p>
     <button onclick="addToCart('Raspberry Chocostixx', 3.49)">Add to trolley (£3.49)</button>
   </div>
   <div class="product">
     <img src="CHOCOSTIXX CARAMEL.png" alt="Caramel Chocostixx">
     <h3>Caramel Chocostixx</h3>
     <p>Milk chocolate with a caramel ribbon swirl.</p>
     <button onclick="addToCart('Caramel Chocostixx', 3.29)">Add to trolley (£3.29)</button>
   </div>
 </div>
</section>

<section id="cart" class="section">
 <h1>Your Trolley</h1>
 <div id="cart-list"></div>
 <h2 id="total"></h2>
</section>

<script>
let cart = [];

function showSection(id) {
 document.querySelectorAll('.section').forEach(sec => sec.style.display = 'none');
 document.getElementById(id).style.display = 'block';
}

function addToCart(name, price) {
 cart.push({ name, price });
 updateCart();
 alert(name + ' added to trolley!');
}

function updateCart() {
 let cartList = document.getElementById('cart-list');
 let total = cart.reduce((sum, item) => sum + item.price, 0);
 cartList.innerHTML = cart.map(i => `<p>${i.name} - £${i.price.toFixed(2)}</p>`).join('');
 document.getElementById('total').innerText = 'Total: £' + total.toFixed(2);
}
</script>

</body>
</html>
