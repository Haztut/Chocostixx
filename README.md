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

    .about-row {
        display: flex;
        justify-content: center;
        align-items: flex-start;
        gap: 40px;
        margin-top: 30px;
        flex-wrap: wrap;
    }

    .about-box {
        width: 350px;
        min-height: 200px;
        border: 2px solid #6b3e18;
        border-radius: 10px;
        padding: 15px;
        background: #fff5eb;
        text-align: left;
    }

    .about-img {
        width: 320px;
        height: auto;
        border-radius: 10px;
        box-shadow: 0 4px 10px rgba(0,0,0,0.15);
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
    Get your fix with Chocostixx!  
    <br>
    <img class="logo" src="CHOCOSTIXX TITLE.png" alt="Chocostixx Logo">
</header>

<nav>
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('shop')">Shop</button>
    <button onclick="showSection('cart')">Trolley</button>

    <!-- NEW BUTTON -->
    <button onclick="showSection('about')">About Us</button>
</nav>

<!-- HOME -->
<div id="home" class="section" style="display:block;">
    <h1 style="color:#6b3e18;">Welcome to Chocostixx.co.uk!</h1>
    <p style="font-size:20px;">The official home of the world’s first twist up chocolate treat! Any queries or business interests: Email-harrytutton1@gmail.com</p>
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

<!-- ABOUT US -->
<div id="about" class="section">

    <h1 style="color:#6b3e18;">About Us</h1>

    <div class="about-row">

        <!-- LEFT BOX TEXT -->
        <div class="about-box">
            <!-- 🔶 TYPE YOUR FIRST ABOUT TEXT HERE (LINE TO EDIT) -->
            Inspired on a bleak November Monday, Founder and CEO of Chocostixx.co.uk -Harry Tutton- sat and thought, how could he revolutionise the chocolate industry? How could he build a snack to eat now, to eat later, to be fun and flavourful, to combine food and design into one lip-smacking treat... And Chocostixx was born.
        </div>

        <!-- RIGHT IMAGE -->
        <!-- 🔶 REPLACE THE FILENAME BELOW WITH YOUR PNG NAME -->
        <div>
            <img class="about-img" src="Founder image.png" alt="Founder Image">
            <p style="margin-top:5px; font-weight:bold; color:#4a2b12;">
                Founder and CEO: Harry Tutton
            </p>
        </div>

    </div>

    <div class="about-row">

        <!-- LEFT IMAGE -->
        <!-- 🔶 REPLACE THIS FILENAME WITH YOUR PNG NAME -->
        <div>
            <img class="about-img" src="Chocotube.png" alt="Design Image">
            <p style="margin-top:5px; font-weight:bold; color:#4a2b12;">
                The Design
            </p>
        </div>

        <!-- RIGHT BOX TEXT -->
        <div class="about-box">
            <!-- 🔶 TYPE YOUR SECOND ABOUT TEXT HERE (LINE TO EDIT) -->
            He got to work and in 4 days, a website was built, a prototype created, market research collected that allowed him to understand what the people wanted. Witnessing the impact of litter in the local area, he implemented a policy, instead of the stixx tube being thrown away after the customer enjoys the snack, it would be returned for sterilisation and the customer would be paid back 50p allowing further chocostixx to be created keeping the small business thriving.
        </div>

    </div>
</div>

<!-- CART -->
<div id="cart" class="section">
    <h2 style="color:#6b3e18;">Your Trolley</h2>
    <div id="cartItems"></div>
    <h3 id="total" style="margin-top:20px;"></h3>

    <button id="payButton" onclick="startWonderfulPayment()">Pay Now</button>
</div>

<script>
let cart = [];

function showSection(id) {
    document.querySelectorAll('.section').forEach(sec => sec.style.display = 'none');
    document.getElementById(id).style.display = 'block';
}

function addToCart(name, price) {
    cart.push({name, price});
    alert(name + " added to trolley!");
    updateCart();
}

function updateCart() {
    let cartDiv = document.getElementById("cartItems");
    let totalDiv = document.getElementById("total");
    let payBtn = document.getElementById("payButton");

    cartDiv.innerHTML = "";
    let total = 0;

    cart.forEach(item => {
        cartDiv.innerHTML += `<div class="cart-item">${item.name} – £${item.price.toFixed(2)}</div>`;
        total += item.price;
    });

    totalDiv.innerHTML = "Total: £" + total.toFixed(2);

    if (cart.length > 0) payBtn.style.display = "inline-block";
    else payBtn.style.display = "none";
}

function startWonderfulPayment() {
    let total = cart.reduce((sum, item) => sum + item.price, 0);

    let url = `https://checkout.wonderful.co/pay?
        merchantId=Chocostixx&
        amount=${total.toFixed(2)}&
        currency=GBP&
        reference=ChocostixxOrder`;

    url = url.replace(/\s+/g, ''); 
    window.location.href = url;
}
</script>

</body>
</html>
