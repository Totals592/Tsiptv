<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Deals</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        header {
            background-color: #333;
            color: white;
            padding: 1rem 0;
            text-align: center;
        }

        nav ul {
            list-style: none;
            padding: 0;
            text-align: center;
            background-color: #444;
        }

        nav ul li {
            display: inline;
            margin: 0 1rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            padding: 0.5rem 1rem;
            display: inline-block;
        }

        nav ul li a:hover {
            background-color: #555;
        }

        .container {
            width: 80%;
            margin: 2rem auto;
            overflow: hidden;
        }

        .product {
            width: 30%;
            float: left;
            margin: 1rem;
            border: 1px solid #ddd;
            padding: 1rem;
            text-align: center;
        }

        .product img {
            max-width: 100%;
            height: auto;
        }

        .product h3 {
            margin-top: 0.5rem;
        }

        .product .price {
            font-weight: bold;
            color: #007bff;
        }

        .product button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            cursor: pointer;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem 0;
            clear: both;
        }
    </style>
</head>
<body>
    <header>
        <h1>Digital Deals</h1>
    </header>

    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">IPTV</a></li>
            <li><a href="#">Gift Cards</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <div class="container">
        <div class="product">
            <img src="placeholder-iptv.jpg" alt="IPTV Subscription">
            <h3>IPTV Subscription - 1 Month</h3>
            <p class="price">$19.99</p>
            <button>Add to Cart</button>
        </div>

        <div class="product">
            <img src="placeholder-iptv.jpg" alt="IPTV Subscription">
            <h3>IPTV Subscription - 3 Months</h3>
            <p class="price">$49.99</p>
            <button>Add to Cart</button>
        </div>

        <div class="product">
            <img src="placeholder-giftcard.jpg" alt="Digital Gift Card">
            <h3>$25 Digital Gift Card</h3>
            <p class="price">$25.00</p>
            <button>Add to Cart</button>
        </div>
        <div class="product">
            <img src="placeholder-giftcard.jpg" alt="Digital Gift Card">
            <h3>$50 Digital Gift Card</h3>
            <p class="price">$50.00</p>
            <button>Add to Cart</button>
        </div>
        <div class="product">
            <img src="placeholder-giftcard.jpg" alt="Digital Gift Card">
            <h3>$100 Digital Gift Card</h3>
            <p class="price">$100.00</p>
            <button>Add to Cart</button>
        </div>

    </div>

    <footer>
        <p>&copy; 2024 Digital Deals. All rights reserved.</p>
    </footer>
    <script>
    //basic cart functionality example.
    const cart = [];
    document.querySelectorAll('.product button').forEach(button => {
        button.addEventListener('click', function(event){
            const productDiv = event.target.parentElement;
            const productName = productDiv.querySelector('h3').textContent;
            const productPrice = productDiv.querySelector('.price').textContent;
            cart.push({name: productName, price: productPrice});
            console.log(cart); //for testing, shows cart in console.
            alert(`${productName} added to cart!`);
        });
    });

    </script>
</body>
</html>
