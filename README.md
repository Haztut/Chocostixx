<html lang="en">
<head>
<meta charset="UTF-8">
<title>Get your fix with Chocostixx!</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
    body {
        margin: 0;
        font-family: Arial, sans-serif;
        background: #f7d7b5;
    }

    header {
        background: #6b3e18;
        padding: 20px;
        text-align: center;
        color: white;
        font-size: 28px;
        font-weight: bold;
        border-bottom: 6px solid #4a2b12;
    }

    .logo {
        width: 350px;
        margin-top: 10px;
    }

    nav {
        text-align: center;
        margin: 20px;
    }
    nav button {
        padding: 12px 25px;
        background: #6b3e18;
        color: white;
        border: none;
        border-radius: 10px;
        cursor: pointer;
        font-size: 18px;
    }
    nav button:hover {
        background: #4a2b12;
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
        margin-top: 20px;
    }

    .product {
        background: #fff;
        border-radius: 20px;
        padding: 20px;
        width: 280px;
        box-shadow: 0 6px 15px rgba(0,0,0,0.15);
    }

    .product img {
        width: 200px;
        height: auto;
    }

    .product-name {
        font-size: 22px;
        font-weight: bold;
        margin-top: 10px;
    }

    .title {
        font-size: 30px;
        font-weight: bold;
        color: #6b3e18;
        margin-bottom: 10px;
    }

    .price {
        font-size: 22px;
        font-weight: bold;
        color: #4a2b12;
    }

    .add-btn {
        margin-top: 10px;
        padding: 10px 20px;
        background: #6b3e18;
        color: white;
        border: none;
        border-radius: 10px;
        cursor: pointer;
    }

    .cart-item {
        font-size: 22px;
        margin: 10px 0;
    }

    #payButton {
        margin-top: 20px;
        padding: 15px 25px;
        background: #28a745;
        color: white;
        border: none;
        border-radius: 12px;
        cursor: pointer;
        font-size: 20px;
        display: none;
    }
</style>

</head>
<body>

<header>
    <span style="display:none;">Get your fix with Chocostixx!</span>
    <br>
    <img class="logo" src="CHOCOSTIXX TITLE.png" alt="Chocostixx Logo">
</header>

<nav>
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('shop')">Shop</button>
    <button onclick="showSection('cart')">Trolley</button>
</nav>

<!-- HOME -->
<div id="home" class="section" style="display:block;">
    <h1 style="color:#6b3e18;">Welcome to Chocostixx!</h1>
    <p style="font-size:20px;">The official home of the world’s most fun chocolate snack!</p>
</div>

<!-- SHOP -->
<div id="shop" class="section">
    <div class="title">Check out our range!</div>

    <div class="product-grid">

        <div class="product">
            <img src="CHOCOSTIXX ORIGINAL.png" alt="Original Chocostixx">
            <div class="product-name" style="color:#6b3e18;">Original</div>
            <div class="price">£2.99</div>
            <button class="add-btn" onclick="addToCart('Original Chocostixx', 2.99)">Add to Trolley</button>
        </div>

        <div class="product">
            <img src="CHOCOSTIXX RASPBERRY RIPPLE.png" alt="Raspberry Chocostixx">
            <div class="product-name" style="color:#ff4da6;">Raspberry Ripple</div>
            <div class="price">£3.49</div>
            <button class="add-btn" onclick="addToCart('Raspberry Chocostixx', 3.49)">Add to Trolley</button>
        </div>

        <div class="product">
            <img src="CHOCOSTIXX CARAMEL.png" alt="Caramel Chocostixx">
            <div class="product-name" style="color:#c88b3a;">Caramel</div>
            <div class="price">£3.49</div>
            <button class="add-btn" onclick="addToCart('Caramel Chocostixx', 3.49)">Add to Trolley</button>
        </div>

    </div>
</div>

<!-- CART -->
<div id="cart" class="section">
    <h2 style="color:#6b3e18;">Your Trolley</h2>
    <div id="cartItems"></div>
    <h3 id="total" style="margin-top:20px;"></h3>

    <!-- WONDERFUL PAY BUTTON -->
    <button id="payButton" onclick="startWonderfulPayment()">Pay Now</button>
</div>

<script>
let cart = [];

function showSection(id) {
    document.querySelectorAll('.section').forEach(sec => sec.style.display = 'none');
    document.getElementById(id).style.di
