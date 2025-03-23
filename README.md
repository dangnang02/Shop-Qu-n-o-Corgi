<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop Quần Áo Corgi</title>
    <link rel="stylesheet" href="style.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #FFF5E1;
            text-align: center;
        }
        header {
            background-color: #FFD700;
            padding: 15px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }
        nav ul {
            list-style: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 15px;
        }
        nav ul li a {
            text-decoration: none;
            font-size: 18px;
            font-weight: bold;
            color: #8B4513;
        }
        #banner img {
            width: 80%;
            border-radius: 15px;
            margin: 20px 0;
        }
        .product {
            display: inline-block;
            background: white;
            padding: 15px;
            margin: 10px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .product:hover {
            transform: scale(1.05);
        }
        button {
            background-color: #FFD700;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }
        button:hover {
            background-color: #FFA500;
        }
    </style>
</head>
<body>
    <header>
        <h1>Shop Quần Áo Corgi</h1>
        <nav>
            <ul>
                <li><a href="#">Trang chủ</a></li>
                <li><a href="#">Sản phẩm</a></li>
                <li><a href="#">Giỏ hàng</a></li>
                <li><a href="#">Liên hệ</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="banner">
        <img src="C:\Users\Dang Nang\Downloads\corgi-e1586511152955.jpg"alt="Banner cửa hàng">
        <h2>Chào mừng đến với shop quần áo Corgi!</h2>
    </section>
    
    <section id="products">
        <h2>Sản phẩm nổi bật</h2>
        <div class="product">
            <img src="C:\Users\Dang Nang\Downloads\corgi.webp" alt="Áo T-Shirt Corgi">
            <h3>Áo T-Shirt Corgi</h3>
            <p>Màu sắc: Trắng, Đen, Xám</p>
            <p>Kích thước: S, M, L, XL</p>
            <p>Chất liệu: Cotton 100%</p>
            <p>Giá: 200.000đ</p>
            <button onclick="addToCart('Áo T-Shirt Corgi', 200000)">Thêm vào giỏ</button>
        </div>
        <div class="product">
            <img src="C:\Users\Dang Nang\Downloads\corgi sat.webp" alt="Áo T-Shirt Corgi Shark ">
            <h3>Áo T-Shirt Corgi Shark</h3>
            <p>Màu sắc: Đen, Xám</p>
            <p>Kích thước: M, L, XL</p>
            <p>Chất liệu: Nỉ bông</p>
            <p>Giá: 350.000đ</p>
            <button onclick="addToCart('Áo T-Shirt Corgi Shark', 350000)">Thêm vào giỏ</button>
        </div>
    </section>
    
    <section id="cart">
        <h2>Giỏ hàng</h2>
        <ul id="cart-items"></ul>
        <p id="total-price">Tổng tiền: 0đ</p>
        <button onclick="checkout()">Thanh toán</button>
    </section>
    
    <footer>
        <p>&copy; 2025 Shop Quần Áo Corgi. All rights reserved.</p>
    </footer>
    
    <script>
        let cart = [];
        function addToCart(name, price) {
            cart.push({ name, price });
            updateCart();
        }
        function updateCart() {
            let cartItems = document.getElementById("cart-items");
            let totalPrice = document.getElementById("total-price");
            cartItems.innerHTML = "";
            let total = 0;
            cart.forEach(item => {
                let li = document.createElement("li");
                li.textContent = `${item.name} - ${item.price}đ`;
                cartItems.appendChild(li);
                total += item.price;
            });
            totalPrice.textContent = `Tổng tiền: ${total}đ`;
        }
        function checkout() {
            alert("Có tiền đầu mà thanh toán!");
        }
    </script>
</body>
</html>
