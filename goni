<!DOCTYPE html>
<html lang="sq">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dyqani Im Online</title>
    <style>
        body {
    font-family: Arial, sans-serif;
    background-color: #f9f9f9;
    margin: 0;
    padding: 0;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 10px 0;
    text-align: center;
}

.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 20px;
}

.product {
    background-color: white;
    margin: 10px;
    padding: 20px;
    border-radius: 8px;
    width: 200px;
    text-align: center;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.product img {
    max-width: 100%;
    border-radius: 8px;
}

.product h2 {
    font-size: 20px;
    color: #333;
}

.product p {
    color: #555;
}

.product .price {
    font-size: 18px;
    color: #4CAF50;
    margin: 10px 0;
}

.product button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.product button:hover {
    background-color: #45a049;
}

.cart {
    background-color: #fff;
    padding: 10px;
    position: fixed;
    top: 10%;
    right: 0;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 250px;
    box-sizing: border-box;
    display: none;
}

.cart h3 {
    margin-top: 0;
}

.cart-item {
    margin-bottom: 10px;
}

/* Media query for smaller screens (e.g., mobile) */
@media screen and (max-width: 768px) {
    .container {
        flex-direction: column; /* Items will stack vertically */
        align-items: center; /* Center the products */
    }

    .product {
        width: 90%; /* Make each product take more width on small screens */
        margin: 10px 0; /* Space between products */
    }

    .cart {
        width: 100%; /* Cart takes full width on mobile */
        right: 0; /* Cart appears at the top-right */
    }
}

    </style>
</head>
<body>
<header>
    <h1>Dyqani Im Online</h1>
</header>
<div class="container">
    <!-- Produkti 1 -->
    <div class="product" id="product1">
        <img src="https://via.placeholder.com/200" alt="Produkt 1">
        <h2>Produkt 1</h2>
        <p>Lorem ipsum dolor sit amet</p>
        <div class="price">$50</div>
        <button onclick="addToCart('Produkt 1', 50)">Shto në Shportë</button>
    </div>
    <!-- Produkti 2 -->
    <div class="product" id="product2">
        <img src="https://via.placeholder.com/200" alt="Produkt 2">
        <h2>Produkt 2</h2>
        <p>Lorem ipsum dolor sit amet</p>
        <div class="price">$30</div>
        <button onclick="addToCart('Produkt 2', 30)">Shto në Shportë</button>
    </div>
    <!-- Produkti 3 -->
    <div class="product" id="product3">
        <img src="https://via.placeholder.com/200" alt="Produkt 3">
        <h2>Produkt 3</h2>
        <p>Lorem ipsum dolor sit amet</p>
        <div class="price">$75</div>
        <button onclick="addToCart('Produkt 3', 75)">Shto në Shportë</button>
    </div>
     <!-- Produkt 4 -->
    <div class="product" id="product4">
        <img src="https://via.placeholder.com/200" alt="Produkt 4">
        <h2>Produkt 4</h2>
        <p>dardh</p>
        <div class="price">$5</div>
        <button onclick="addToCart('Produkt 4', 5)">Shto në Shportë</button>
    </div>
    <!-- Produkt 5 -->
    <div class="product" id="product5">
        <img src="https://via.placeholder.com/200" alt="Produkt 5">
        <h2>Produkt 5</h2>
        <p>modh</p>
        <div class="price">$3</div>
        <button onclick="addToCart('Produkt 5', 3)">Shto në Shportë</button>
    </div>
</div>
<!-- Shporta -->
<div class="cart" id="cart">
    <h3>Shporta Juaj</h3>
    <div id="cart-items"></div>
    <button onclick="checkout()">Paguaj</button>
</div>
<!-- Formë Pagesë -->
<div id="payment-form" style="display:none;">
    <h3>Formë Pagesë</h3>
    <form action="/submit-payment" method="POST">
        <label for="card">Numri i Kartës:</label><br>
        <input type="text" id="card" name="card" required><br><br>
        <label for="name">Emri dhe Mbiemri:</label><br>
        <input type="text" id="name" name="name" required><br><br>
        <input type="submit" value="Paguaj">
    </form>
</div>
<script>
    let cart = [];
    // Funksioni për shtimin e produktit në shportë
    function addToCart(productName, price) {
        cart.push({ productName, price });
        updateCart();
    }
    // Funksioni për përditësimin e shportës
    function updateCart() {
        let cartItems = document.getElementById('cart-items');
        cartItems.innerHTML = '';
        cart.forEach((item, index) => {
            const cartItem = document.createElement('div');
            cartItem.classList.add('cart-item');
            cartItem.innerHTML = `${item.productName} - $${item.price} 
                <button onclick="removeFromCart(${index})">Heq</button>`;
            cartItems.appendChild(cartItem);
        });
        // Shfaq shportën nëse ka produkte
        let cartContainer = document.getElementById('cart');
        cartContainer.style.display = cart.length > 0 ? 'block' : 'none';
    }
    // Funksioni për heqjen e produktit nga shporta
    function removeFromCart(index) {
        cart.splice(index, 1); // Heqim produktin nga shporta duke përdorur `splice()`
        updateCart(); // Përsëri përditësojmë shportën pas heqjes
    }
    // Funksioni për checkout
    function checkout() {
        document.getElementById('cart').style.display = 'none';
        document.getElementById('payment-form').style.display = 'block';
    }
</script>
</body>
</html>
