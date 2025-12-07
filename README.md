# my-project
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dhatri Official</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: #fffaf6;
      color: #3b3b3b;
    }

    header {
      background: #fff;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: bold;
      color: #d4af37;
    }

    nav a {
      margin-left: 20px;
      text-decoration: none;
      color: #333;
      font-weight: 500;
    }

    section.hero {
      padding: 4rem 2rem;
      text-align: center;
      background: #fdf7f2;
    }

    .hero h1 {
      font-size: 2.2rem;
      margin-bottom: 1rem;
      color: #b48834;
    }

    section.products {
      padding: 3rem 2rem;
      background: #fffaf6;
    }

    .products h2 {
      text-align: center;
      font-size: 2rem;
      margin-bottom: 2rem;
      color: #b48834;
    }

    .product-gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
      gap: 2rem;
    }

    .product {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.08);
      padding: 1rem;
      text-align: center;
    }

    .product img {
      width: 100%;
      border-radius: 8px;
    }

    .product h4 {
      margin-top: 1rem;
      font-size: 1rem;
    }

    section.about,
    section.contact,
    section.instagram,
    section.youtube {
      padding: 3rem 2rem;
      text-align: center;
    }

    section h2 {
      font-size: 2rem;
      margin-bottom: 1rem;
      color: #b48834;
    }

    footer {
      background: #fff;
      text-align: center;
      padding: 1rem;
      color: #999;
    }

    form input, form textarea, form select {
      padding: 0.5rem;
      margin: 0.5rem 0;
      width: 80%;
      max-width: 400px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    form button {
      margin-top: 10px;
      padding: 0.7rem 1rem;
      background: #25D366;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      width: 80%;
      max-width: 400px;
    }

    form button:hover {
      background: #128C7E;
    }

    @media (max-width: 600px) {
      nav {
        display: none;
      }
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <div class="logo">DHATRI COLLECTIONS</div>
    <nav>
      <a href="#products">Our Collections</a>
      <a href="#contact">Get In Touch</a>
      <a href="#instagram">Instagram</a>
      <a href="#youtube">Youtube</a>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <h1>✨ Elegant Shine • Aesthetic Glow ✨</h1>
    <p>Minimal Designs • Trending Styles • Everyday Elegance</p>
  </section>

  <!-- Product Gallery -->
  <section class="products" id="products">
    <h2>OUR COLLECTIONS</h2>

    <div class="product-gallery">

      <div class="product">
        <img src="images/minimal-chains.jpg" alt="">
        <h4>MINIMAL EARRING & CHAINS</h4>
      </div>

      <div class="product">
        <img src="images/bracelets.jpg" alt="">
        <h4>BRACELETS</h4>
      </div>

      <div class="product">
        <img src="images/scurenchies-bows.jpg" alt="">
        <h4>SCRUNCHIES AND BOWS</h4>
      </div>

      <div class="product">
        <img src="images/necklaces.jpg" alt="">
        <h4>NECKLACES</h4>
      </div>

      <div class="product">
        <img src="images/CLIPS-COLLECTION.jpg" alt="">
        <h4>CLIPS COLLECTION</h4>
      </div>

    </div>
  </section>

  <!-- About Section -->
  <section class="about" id="about">
    <h2>ABOUT DHATRI COLLECTIONS 💍</h2>
    <p>
      Dhatri creates beautiful, minimal jewellery inspired by everyday elegance and timeless beauty.
    </p>
  </section>

  <!-- CONTACT + WHATSAPP ORDER -->
  <section class="contact" id="contact">
    <h2>Get In Touch 😍</h2>

    <p>📧 Email: dhatrioffical@gmail.com</p>
    <p>☎️ Phone: +91 7093504081</p>

    <form onsubmit="sendWhatsApp(event)">

      <input type="text" id="name" placeholder="Your Name" required><br>
      <input type="email" id="email" placeholder="Your Email" required><br>

      <label>Select Product</label><br>
      <select id="product" required>
        <option value="MINIMAL EARRING & CHAINS">MINIMAL EARRING & CHAINS</option>
        <option value="BRACELETS">BRACELETS</option>
        <option value="SCRUNCHIES AND BOWS">SCRUNCHIES AND BOWS</option>
        <option value="NECKLACES">NECKLACES</option>
        <option value="CLIPS COLLECTION">CLIPS COLLECTION</option>
      </select><br>

      <textarea id="message" placeholder="Your Message" required></textarea><br>

      <button type="submit">Order on WhatsApp</button>

    </form>
  </section>

  <!-- Instagram Section -->
  <section class="instagram" id="instagram">
    <h2>FOLLOW US ON INSTAGRAM</h2>
    <p>@dhatriofficial</p>
  </section>

  <!-- YouTube Section -->
  <section class="youtube" id="youtube">
    <h2>FOLLOW US ON YOUTUBE</h2>
    <p>@DHATRIOFFICAL2822</p>
  </section>

  <!-- Footer -->
  <footer>
    &copy; 2025 Dhatri Official. All Rights Reserved.
  </footer>


  <!-- WHATSAPP SCRIPT -->
  <script>
    function sendWhatsApp(event) {
      event.preventDefault();

      let name = document.getElementById("name").value;
      let email = document.getElementById("email").value;
      let product = document.getElementById("product").value;
      let message = document.getElementById("message").value;

      // CHANGE THIS NUMBER TO YOUR WHATSAPP NUMBER
      let phone = "919999999999";

      let text = `Hello, I want to order from Dhatri Collections:%0A
Name: ${name}%0A
Email: ${email}%0A
Product: ${product}%0A
Message: ${message}`;

      let url = `https://wa.me/${phone}?text=${text}`;

      window.open(url, "_blank");
    }
  </script>

</body>
</html>
