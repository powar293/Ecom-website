<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Leanine - Printed Shirt Store</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #f5f5f5;
    }

    header {
      background: #fff;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .logo {
      font-size: 1.8rem;
      font-weight: bold;
      color: #333;
    }

    .search-box {
      padding: 0.5rem;
      width: 200px;
    }

    .cart {
      font-size: 1.5rem;
      cursor: pointer;
    }

    .hero {
      background: url('https://images.pexels.com/photos/9821919/pexels-photo-9821919.jpeg?auto=compress&w=1200&h=800&fit=crop') no-repeat center center/cover;
      padding: 3rem 2rem;
      text-align: center;
      position: relative;
      min-height: 400px;
      color: #fff;
    }
    .hero h2, .hero h1, .hero button {
      position: relative;
      z-index: 2;
    }
    .hero::after {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.45);
      z-index: 1;
      border-radius: 0;
    }

    .hero h2 {
      font-size: 2rem;
      color: #555;
    }

    .hero h1 {
      font-size: 3rem;
      font-weight: bold;
      margin: 0.5rem 0;
    }

    .hero button {
      padding: 0.7rem 1.5rem;
      font-size: 1rem;
      background-color: #111;
      color: #fff;
      border: none;
      cursor: pointer;
    }

    .menu {
      background-color: #111;
      display: flex;
      justify-content: center;
      gap: 2rem;
      padding: 1rem 0;
    }

    .menu a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.3rem;
      font-size: 1rem;
    }
    .menu-img {
      width: 48px;
      height: 48px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid #fff;
      background: #eee;
      margin-bottom: 0.2rem;
      box-shadow: 0 2px 6px rgba(0,0,0,0.08);
      transition: transform 0.2s;
    }
    .menu a:hover .menu-img {
      transform: scale(1.08);
      border-color: #f39c12;
    }

    .products {
      padding: 2rem;
    }

    .products h3 {
      margin-bottom: 1rem;
      font-size: 1.5rem;
      color: #222;
    }

    .product-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 1.5rem;
    }

    @media (min-width: 992px) {
      .product-list {
        grid-template-columns: repeat(4, 1fr);
      }
    }

    .product-card {
      background-color: white;
      border: 1px solid #ddd;
      padding: 1rem;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.05);
    }

    .product-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 5px;
    }

    .product-card h4 {
      margin: 0.5rem 0;
      font-size: 1rem;
    }

    .product-card p {
      color: #555;
      margin-bottom: 0.3rem;
    }

    .product-card span {
      color: #f39c12;
      font-size: 0.9rem;
    }

    footer {
      background-color: #111;
      color: #fff;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
    }

    footer a {
      color: #fff;
      margin-right: 1rem;
      text-decoration: none;
    }

    .socials span {
      margin-left: 1rem;
      font-size: 1.2rem;
    }

    @media (max-width: 600px) {
      .menu {
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        overflow-x: auto !important;
        overflow-y: hidden;
        white-space: nowrap;
        gap: 1rem;
        padding: 0.5rem 0.5rem 0.5rem 0.5rem;
        scrollbar-width: thin;
        -webkit-overflow-scrolling: touch;
        width: 100vw;
        max-width: 100vw;
        box-sizing: border-box;
      }
      .menu a {
        min-width: 90px;
        flex: 0 0 auto;
        font-size: 0.9rem;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        padding: 0.2rem 0.2rem 0.2rem 0.2rem;
        background: transparent;
        z-index: 1;
      }
      .menu-img {
        width: 40px;
        height: 40px;
        display: block;
      }
      /* Hide scroll bar but keep scrollable */
      .menu::-webkit-scrollbar {
        display: none;
      }
      .menu::-webkit-scrollbar {
        height: 6px;
        background: #222;
      }
      .menu::-webkit-scrollbar-thumb {
        background: #444;
        border-radius: 4px;
      }
      .menu a {
        min-width: 80px;
        flex: 0 0 auto;
        font-size: 0.9rem;
      }
      .menu-img {
        width: 40px;
        height: 40px;
      }
      .search-box {
        width: 100px;
      }
      .product-list {
        grid-template-columns: repeat(2, 1fr);
      }
      html, body {
        max-width: 100vw;
        overflow-x: hidden;
      }
      header, .hero, .menu, .products, footer {
        max-width: 100vw;
        overflow-x: hidden;
      }
      .hero {
        background-size: cover;
      }
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">SLEANINE</div>
    <input type="text" class="search-box" placeholder="Search now...">
    <div class="cart">🛒</div>
  </header>

  <section class="hero">
    <h2>CURRENT SALE</h2>
    <h1>ORE WOW</h1>
    <button>KOW ATIONS</button>
  </section>

  <nav class="menu">
    <a href="#" id="newArrivalsBtn">
      <img src="https://images.unsplash.com/photo-1512436991641-6745cdb1723f?auto=format&fit=facearea&w=60&h=60&mask=circle" alt="New Arrivals" class="menu-img">
      <div>New Arrivals</div>
    </a>
    <a href="#" id="shirtsBtn">
      <img src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&fit=facearea&w=60&h=60&mask=circle" alt="Shirts" class="menu-img">
      <div>Shirts</div>
    </a>
    <a href="#" id="hoodiesBtn">
      <img src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=facearea&w=60&h=60&mask=circle" alt="Hoodies" class="menu-img">
      <div>Hoodies</div>
    </a>
    <a href="#" id="tshirtsBtn">
      <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=facearea&w=60&h=60&mask=circle" alt="T-Shirts" class="menu-img">
      <div>T-Shirts</div>
    </a>
    <a href="#" id="customBtn">
      <img src="https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=facearea&w=60&h=60&mask=circle" alt="Custom Prints" class="menu-img">
      <div>Custom Prints</div>
    </a>
  </nav>

  <section class="products">
    <h3>Top Products</h3>
    <div class="product-list" id="productList">
      <!-- JS will add products here -->
    </div>
  </section>

  <footer>
    <div>
      <a href="#" id="aboutUsLink">About Us</a>
      <a href="#" id="contactLink">Contact</a>
      <a href="#">FAQ</a>
    </div>
    <div class="socials">
      <a href="https://instagram.com" target="_blank" title="Instagram" style="margin-left:1rem;color:#fff;font-size:1.5rem;"><i class="bi bi-instagram"></i></a>
      <a href="https://youtube.com" target="_blank" title="YouTube" style="margin-left:1rem;color:#fff;font-size:1.5rem;"><i class="bi bi-youtube"></i></a>
      <a href="https://facebook.com" target="_blank" title="Facebook" style="margin-left:1rem;color:#fff;font-size:1.5rem;"><i class="bi bi-facebook"></i></a>
      <a href="https://twitter.com" target="_blank" title="Twitter" style="margin-left:1rem;color:#fff;font-size:1.5rem;"><i class="bi bi-twitter"></i></a>
    </div>
  </footer>

  <div id="footerModal" style="display:none;position:fixed;top:0;left:0;width:100vw;height:100vh;background:rgba(0,0,0,0.5);z-index:1000;justify-content:center;align-items:center;">
    <div style="background:#fff;padding:2rem 1.5rem;border-radius:10px;max-width:350px;text-align:center;position:relative;">
      <button id="closeModalBtn" style="position:absolute;top:10px;right:15px;font-size:1.2rem;background:none;border:none;cursor:pointer;">&times;</button>
      <div id="modalContent"></div>
    </div>
  </div>
    /* Modal styles */
    #footerModal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: rgba(0,0,0,0.5);
      z-index: 1000;
      justify-content: center;
      align-items: center;
    }
    #footerModal > div {
      background: #fff;
      padding: 2rem 1.5rem;
      border-radius: 10px;
      max-width: 350px;
      text-align: center;
      position: relative;
    }
    #closeModalBtn {
      position: absolute;
      top: 10px;
      right: 15px;
      font-size: 1.2rem;
      background: none;
      border: none;
      cursor: pointer;
    }

  <script>
    const allProducts = {
      "New Arrivals": Array.from({length: 10}, (_, i) => ({
        name: `New Arrival ${i+1}`,
        price: `$${(14.99 + i).toFixed(2)}`,
        image: `https://images.unsplash.com/photo-1512436991641-6745cdb1723f?auto=format&fit=crop&w=400&q=80&sig=${i}`,
        rating: 3 + (i % 3)
      })),
      "Shirts": [
        { name: "Classic White Shirt", price: "$15.99", image: "https://images.unsplash.com/photo-1512436991641-6745cdb1723f?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Blue Denim Shirt", price: "$16.99", image: "https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Striped Shirt", price: "$17.99", image: "https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Black Formal Shirt", price: "$18.99", image: "https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Red Casual Shirt", price: "$19.99", image: "https://images.unsplash.com/photo-1517263904808-5dc0d6e1b8d4?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Green Printed Shirt", price: "$20.99", image: "https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Grey Slim Shirt", price: "$21.99", image: "https://images.unsplash.com/photo-1518717758536-85ae29035b6d?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Yellow Summer Shirt", price: "$22.99", image: "https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Purple Trend Shirt", price: "$23.99", image: "https://images.unsplash.com/photo-1519864600265-abb23847ef2c?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Brown Check Shirt", price: "$24.99", image: "https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?auto=format&fit=crop&w=400&q=80", rating: 4 }
      ],
      "Hoodies": Array.from({length: 10}, (_, i) => ({
        name: `Hoodie ${i+1}`,
        price: `$${(19.99 + i).toFixed(2)}`,
        image: `https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=400&q=80&sig=${i}`,
        rating: 3 + (i % 3)
      })),
      "T-Shirts": [
        { name: "White Graphic Tee", price: "$12.99", image: "https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Black Basic Tee", price: "$13.99", image: "https://images.unsplash.com/photo-1518717758536-85ae29035b6d?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Red Print Tee", price: "$14.99", image: "https://images.unsplash.com/photo-1517263904808-5dc0d6e1b8d4?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Blue Sport Tee", price: "$15.99", image: "https://images.unsplash.com/photo-1519864600265-abb23847ef2c?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Green Summer Tee", price: "$16.99", image: "https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Yellow Fun Tee", price: "$17.99", image: "https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Grey Urban Tee", price: "$18.99", image: "https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Purple Trend Tee", price: "$19.99", image: "https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80", rating: 4 },
        { name: "Brown Classic Tee", price: "$20.99", image: "https://images.unsplash.com/photo-1512436991641-6745cdb1723f?auto=format&fit=crop&w=400&q=80", rating: 5 },
        { name: "Orange Print Tee", price: "$21.99", image: "https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80", rating: 4 }
      ],
      "Custom Prints": Array.from({length: 10}, (_, i) => ({
        name: `Custom Print ${i+1}`,
        price: `$${(21.99 + i).toFixed(2)}`,
        image: `https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80&sig=${i}`,
        rating: 3 + (i % 3)
      }))
    };

    function renderProducts(section) {
      const products = allProducts[section] || [];
      const productList = document.getElementById("productList");
      productList.innerHTML = "";
      products.forEach(p => {
        const card = document.createElement("div");
        card.className = "product-card";
        card.innerHTML = `
          <img src="${p.image}" alt="${p.name}">
          <h4>${p.name}</h4>
          <p>${p.price}</p>
          <span>${"★".repeat(p.rating)}${"☆".repeat(5 - p.rating)}</span>
        `;
        productList.appendChild(card);
      });
    }

    // Initial load
    renderProducts("New Arrivals");

    document.getElementById("newArrivalsBtn").onclick = () => renderProducts("New Arrivals");
    document.getElementById("shirtsBtn").onclick = () => renderProducts("Shirts");
    document.getElementById("hoodiesBtn").onclick = () => renderProducts("Hoodies");
    document.getElementById("tshirtsBtn").onclick = () => renderProducts("T-Shirts");
    document.getElementById("customBtn").onclick = () => renderProducts("Custom Prints");

    // Footer modal logic
    function showModal(content) {
      document.getElementById('modalContent').innerHTML = content;
      document.getElementById('footerModal').style.display = 'flex';
    }
    document.getElementById('aboutUsLink').onclick = function(e) {
      e.preventDefault();
      showModal('<h2>About Us</h2><p>LEANINE is your destination for premium printed shirts. We blend style, comfort, and quality to bring you the best in fashion. Our mission is to make you look and feel great every day!</p>');
    };
    document.getElementById('contactLink').onclick = function(e) {
      e.preventDefault();
      showModal('<h2>Contact Us</h2><p>📞 +91-9876543210<br>📩 info@leanine.com<br>📍 Kolhapur, India</p>');
    };
    document.getElementById('closeModalBtn').onclick = function() {
      document.getElementById('footerModal').style.display = 'none';
    };
  </script>

</body>
</html>
