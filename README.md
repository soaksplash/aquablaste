<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop Pistolets à Eau - Aqua Blaster</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 20px; background-color: #f4f4f4; }
        .container { max-width: 900px; margin: auto; background: white; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); }
        .logo { width: 200px; margin-bottom: 20px; }
        .product { display: inline-block; width: 30%; margin: 15px; padding: 15px; background: #fff; border-radius: 8px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1); }
        .product img { width: 100%; border-radius: 8px; }
        .btn { background-color: #007BFF; color: white; padding: 10px 15px; text-decoration: none; display: inline-block; margin-top: 10px; border-radius: 5px; cursor: pointer; }
        .btn:hover { background-color: #0056b3; }
        #cart { margin-top: 30px; padding: 20px; background: white; border-radius: 10px; }
    </style>
</head>
<body>
    <div class="container">
        <img src="DALL·E 2025-02-18 16.53.15 - A dynamic and eye-catching logo for a TikTok account selling powerful water guns. The design should feature a sleek, modern water gun with vibrant blu.webp" alt="Aqua Blaster Logo" class="logo">
        <h1>💦 Boutique de Pistolets à Eau - Aqua Blaster 💦</h1>
        
        <div class="product">
            <img src="S23184c72fedc4aadbd3b2ada2d3fbea48.jpg_220x220q75.jpg_.avif" alt="Pistolet 1">
            <h3>Pistolet à Eau - Modèle 1</h3>
            <p>Puissant et amusant pour l'été !</p>
            <p><b>Prix : 10,00€</b></p>
            <button class="btn" onclick="addToCart('Pistolet à Eau - Modèle 1', 10.00)">Ajouter au panier</button>
        </div>
        
        <div class="product">
            <img src="S0faefe044071410fbee460cb6942427ff.jpg_220x220q75.jpg_.avif" alt="Pistolet 2">
            <h3>Pistolet à Eau - Modèle 2</h3>
            <p>Super portée et design ergonomique.</p>
            <p><b>Prix : 10,00€</b></p>
            <button class="btn" onclick="addToCart('Pistolet à Eau - Modèle 2', 10.00)">Ajouter au panier</button>
        </div>
        
        <div class="product">
            <img src="S9315b4a0271d430a9eeb0818a1e107dbi.jpg_220x220q75.jpg_.avif" alt="Pistolet 3">
            <h3>Pistolet à Eau - Modèle 3</h3>
            <p>Idéal pour les batailles en plein air.</p>
            <p><b>Prix : 10,00€</b></p>
            <button class="btn" onclick="addToCart('Pistolet à Eau - Modèle 3', 10.00)">Ajouter au panier</button>
        </div>
        
        <div id="cart">
            <h2>🛒 Votre Panier</h2>
            <ul id="cart-items"></ul>
            <h3>Total : <span id="total">0</span>€ (+1€ livraison partout en France)</h3>
            <button class="btn" onclick="checkout()">Commander</button>
        </div>
    </div>
    
    <script>
        let cart = [];
        function addToCart(product, price) {
            cart.push({ name: product, price: price });
            updateCart();
        }
        function updateCart() {
            let cartList = document.getElementById("cart-items");
            cartList.innerHTML = "";
            let total = 1; // Ajout de la livraison
            cart.forEach(item => {
                let li = document.createElement("li");
                li.textContent = `${item.name} - ${item.price}€`;
                cartList.appendChild(li);
                total += item.price;
            });
            document.getElementById("total").textContent = total.toFixed(2);
        }
        function checkout() {
            alert("Merci pour votre commande ! 🚀 Livraison partout en France à 1€");
            cart = [];
            updateCart();
        }
    </script>
</body>
</html>
