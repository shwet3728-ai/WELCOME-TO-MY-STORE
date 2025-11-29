<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Leather Journals Store</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: #f7f4ef;
      color: #333;
      line-height: 1.5;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* Header & Navbar */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: #2f2a24;
      color: #f7f4ef;
      padding: 0.8rem 1.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 1.3rem;
      font-weight: bold;
      letter-spacing: 1px;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1rem;
      font-size: 0.95rem;
    }

    nav li {
      cursor: pointer;
      padding: 0.3rem 0.6rem;
      border-radius: 4px;
    }

    nav li:hover {
      background: #403730;
    }

    /* Hero Section */
    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 2rem;
      padding: 3rem 1.5rem;
      max-width: 1100px;
      margin: 0 auto;
      align-items: center;
    }

    .hero-text h1 {
      font-size: 2.4rem;
      margin-bottom: 0.8rem;
      color: #2b2420;
    }

    .hero-text p {
      margin-bottom: 1.2rem;
      font-size: 1rem;
    }

    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 1.5rem;
    }

    .badge {
      font-size: 0.8rem;
      padding: 0.3rem 0.7rem;
      background: #e1d2b8;
      border-radius: 999px;
    }

    .hero-buttons {
      display: flex;
      gap: 0.8rem;
      flex-wrap: wrap;
    }

    .btn {
      border: none;
      cursor: pointer;
      padding: 0.7rem 1.4rem;
      font-size: 0.9rem;
      border-radius: 999px;
      font-weight: 600;
      transition: transform 0.1s ease, box-shadow 0.1s ease, background 0.2s ease;
    }

    .btn-primary {
      background: #c48a3a;
      color: #fff;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.18);
    }

    .btn-primary:hover {
      background: #af7a33;
      transform: translateY(-1px);
    }

    .btn-outline {
      background: transparent;
      color: #2f2a24;
      border: 1px solid #bda78a;
    }

    .btn-outline:hover {
      background: #e5dac8;
    }

    .hero-image {
      background: #e3d4c0;
      border-radius: 1rem;
      padding: 1rem;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      min-height: 260px;
    }

    .hero-image-inner {
      background: #2f2a24;
      border-radius: 0.8rem;
      padding: 1rem;
      color: #f7f4ef;
      width: 100%;
      max-width: 320px;
      text-align: center;
    }

    .hero-image-inner h2 {
      margin-bottom: 0.6rem;
      font-size: 1.2rem;
    }

    .hero-image-inner p {
      font-size: 0.85rem;
      margin-bottom: 0.8rem;
    }

    .hero-stack {
      display: flex;
      justify-content: center;
      gap: 0.5rem;
    }

    .hero-stack-card {
      width: 70px;
      height: 110px;
      border-radius: 8px;
      background: linear-gradient(135deg, #c0873a, #5c3b24);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.35);
    }

    /* Products Section */
    .section {
      padding: 2.5rem 1.5rem;
      max-width: 1100px;
      margin: 0 auto;
    }

    .section-title {
      font-size: 1.8rem;
      margin-bottom: 1rem;
      color: #2b2420;
    }

    .section-subtitle {
      margin-bottom: 1.8rem;
      font-size: 0.95rem;
      color: #5a5045;
    }

    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 1.5rem;
    }

    .product-card {
      background: #ffffff;
      border-radius: 1rem;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
      display: flex;
      flex-direction: column;
    }

    .product-image-wrapper {
      width: 100%;
      aspect-ratio: 4 / 3;
      overflow: hidden;
      background: #e2d6c3;
    }

    .product-image-wrapper img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .product-body {
      padding: 0.9rem 1rem 1rem;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
    }

    .product-title {
      font-size: 1rem;
      font-weight: 600;
      margin-bottom: 0.3rem;
      color: #322822;
    }

    .product-caption {
      font-size: 0.83rem;
      color: #776b5c;
      margin-bottom: 0.5rem;
    }

    .price-row {
      display: flex;
      align-items: baseline;
      gap: 0.4rem;
      margin-bottom: 0.4rem;
    }

    .current-price {
      font-size: 1.05rem;
      font-weight: 700;
      color: #c05d2b;
    }

    .original-price {
      font-size: 0.85rem;
      text-decoration: line-through;
      color: #8a7b6b;
    }

    .discount-tag {
      font-size: 0.75rem;
      background: #e8f5e9;
      color: #2e7d32;
      padding: 0.15rem 0.4rem;
      border-radius: 999px;
    }

    .product-meta {
      font-size: 0.8rem;
      color: #7a6c5f;
      margin-bottom: 0.8rem;
    }

    .product-actions {
      margin-top: auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 0.5rem;
      flex-wrap: wrap;
    }

    .product-actions small {
      font-size: 0.75rem;
      color: #6b5d51;
    }

    /* About & Contact */
    .about-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 1.5rem;
      align-items: start;
    }

    .about-card {
      background: #fff;
      padding: 1.2rem;
      border-radius: 1rem;
      box-shadow: 0 3px 10px rgba(0, 0, 0, 0.06);
      font-size: 0.9rem;
      color: #4c4237;
    }

    .about-card h3 {
      margin-bottom: 0.6rem;
      font-size: 1.1rem;
      color: #2b2420;
    }

    .about-list {
      padding-left: 1.2rem;
      margin-top: 0.3rem;
    }

    .about-list li {
      margin-bottom: 0.3rem;
    }

    .contact-card {
      background: #fff;
      padding: 1.2rem;
      border-radius: 1rem;
      box-shadow: 0 3px 10px rgba(0, 0, 0, 0.06);
      font-size: 0.9rem;
    }

    .contact-card label {
      display: block;
      margin-bottom: 0.3rem;
      font-size: 0.85rem;
      color: #4c4237;
    }

    .contact-card input,
    .contact-card textarea {
      width: 100%;
      padding: 0.5rem 0.6rem;
      border-radius: 0.5rem;
      border: 1px solid #cab9a3;
      margin-bottom: 0.6rem;
      font-size: 0.85rem;
      background: #fdfaf6;
    }

    .contact-card textarea {
      min-height: 90px;
      resize: vertical;
    }

    .contact-note {
      font-size: 0.78rem;
      color: #7a6c5f;
      margin-top: 0.5rem;
    }

    .contact-note a {
      text-decoration: underline;
    }

    /* Cart Button & Panel */
    .cart-floating-btn {
      position: fixed;
      right: 1.2rem;
      bottom: 1.2rem;
      z-index: 120;
      background: #2f2a24;
      color: #f7f4ef;
      padding: 0.7rem 1.4rem;
      border-radius: 999px;
      border: none;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.9rem;
      box-shadow: 0 5px 16px rgba(0, 0, 0, 0.3);
    }

    .cart-count {
      background: #c48a3a;
      padding: 0.1rem 0.55rem;
      border-radius: 999px;
      font-size: 0.75rem;
      font-weight: 600;
    }

    .cart-panel-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0, 0, 0, 0.45);
      display: none;
      align-items: center;
      justify-content: flex-end;
      z-index: 130;
    }

    .cart-panel {
      width: 100%;
      max-width: 360px;
      background: #f7f4ef;
      height: 100%;
      padding: 1.2rem;
      display: flex;
      flex-direction: column;
    }

    .cart-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.8rem;
    }

    .cart-header h3 {
      font-size: 1.2rem;
      color: #2b2420;
    }

    .cart-close-btn {
      border: none;
      background: transparent;
      font-size: 1.3rem;
      cursor: pointer;
      line-height: 1;
    }

    .cart-items {
      flex-grow: 1;
      overflow-y: auto;
      padding-right: 0.4rem;
      font-size: 0.85rem;
    }

    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      padding: 0.5rem 0;
      border-bottom: 1px solid #ddcdb8;
      gap: 0.5rem;
    }

    .cart-item-title {
      flex: 1;
    }

    .cart-item-remove {
      border: none;
      background: transparent;
      font-size: 0.8rem;
      cursor: pointer;
      color: #c62828;
    }

    .cart-footer {
      border-top: 1px solid #ddcdb8;
      padding-top: 0.8rem;
      font-size: 0.9rem;
    }

    .cart-total-row {
      display: flex;
      justify-content: space-between;
      margin-bottom: 0.7rem;
      font-weight: 600;
    }

    .cart-footer small {
      display: block;
      margin-bottom: 0.6rem;
      color: #6b5d51;
      font-size: 0.78rem;
    }

    footer {
      text-align: center;
      padding: 1rem;
      font-size: 0.8rem;
      color: #7a6c5f;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .hero {
        grid-template-columns: 1fr;
        padding-top: 1.8rem;
      }

      .about-grid {
        grid-template-columns: 1fr;
      }

      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.4rem;
      }

      nav ul {
        gap: 0.6rem;
        font-size: 0.85rem;
      }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="logo">Leather Journal Studio</div>
    <nav>
      <ul>
        <li onclick="scrollToSection('hero')">Home</li>
        <li onclick="scrollToSection('products')">Products</li>
        <li onclick="scrollToSection('about')">About</li>
        <li onclick="scrollToSection('contact')">Contact</li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero" id="hero">
    <div class="hero-text">
      <h1>Handcrafted Leather Journals for Your Best Ideas</h1>
      <p>
        Premium leather, handmade paper, vintage locks and embossed designs – crafted for writers,
        artists, dreamers and gift-givers.
      </p>
      <div class="hero-badges">
        <span class="badge">Handmade in India</span>
        <span class="badge">Custom Name Personalisation</span>
        <span class="badge">Gift-Ready Packaging</span>
      </div>
      <div class="hero-buttons">
        <button class="btn btn-primary" onclick="scrollToSection('products')">Shop Journals</button>
        <button class="btn btn-outline" onclick="scrollToSection('contact')">Bulk / Custom Orders</button>
      </div>
    </div>
    
    <div class="hero-image-inner">
      <h2>Vintage Leather Collection</h2>
      <p>Deckle handmade paper · Key locks · Stone embossed designs.</p>
      <div class="hero-stack"></div>
    </div>
  </section>

  <!-- Products -->
  <section class="section" id="products">
    <h2 class="section-title">Featured Leather Journals</h2>
    <p class="section-subtitle">
      All journals are made with genuine leather and premium plain / deckle handmade paper.
      Choose your favourite design and we’ll personalise it with your name or initials.
    </p>

    <div class="products-grid">
      <!-- 1 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Leaf+Embossed+Journal" alt="Leaf Embossed Leather Cover Journal With Plain Paper">
        </div>
        <div class="product-body">
          <h3 class="product-title">Leaf Embossed Leather Cover Journal</h3>
          <p class="product-caption">Leaf embossed design · Plain paper · Perfect everyday diary.</p>
          <div class="price-row">
            <span class="current-price">₹899</span>
            <span class="original-price">₹1,299</span>
            <span class="discount-tag">30% off</span>
          </div>
          <p class="product-meta">Size: A5 · 200 pages · Plain paper</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Leaf Embossed Leather Cover Journal With Plain Paper"
                    data-price="899">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 2 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Leather+Journal+Diary" alt="Leather Journal Diary">
        </div>
        <div class="product-body">
          <h3 class="product-title">Classic Leather Journal Diary</h3>
          <p class="product-caption">Minimal design · Soft brown leather cover.</p>
          <div class="price-row">
            <span class="current-price">₹799</span>
            <span class="original-price">₹1,099</span>
            <span class="discount-tag">27% off</span>
          </div>
          <p class="product-meta">Size: A5 · 180 pages · Ruled / plain.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Leather Journal Diary"
                    data-price="799">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 3 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Handmade+Leather+Diary" alt="Handmade Leather Diary">
        </div>
        <div class="product-body">
          <h3 class="product-title">Handmade Leather Diary</h3>
          <p class="product-caption">Hand-stitched spine and soft-touch leather.</p>
          <div class="price-row">
            <span class="current-price">₹749</span>
            <span class="original-price">₹1,049</span>
            <span class="discount-tag">29% off</span>
          </div>
          <p class="product-meta">Size: A5 · 160 pages · Plain paper.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Handmade Leather Diary"
                    data-price="749">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 4 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Handmade+Leather+Journal+Diary" alt="Handmade Leather Journal Diary">
        </div>
        <div class="product-body">
          <h3 class="product-title">Handmade Leather Journal Diary</h3>
          <p class="product-caption">Perfect combo of journal + diary in one piece.</p>
          <div class="price-row">
            <span class="current-price">₹849</span>
            <span class="original-price">₹1,199</span>
            <span class="discount-tag">29% off</span>
          </div>
          <p class="product-meta">Size: A5 · 200 pages · Ruled.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Handmade Leather Journal Diary"
                    data-price="849">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 5 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Deckle+Paper+Vintage+Key+Lock" alt="Personalized Leather Journal Dairy With Deckle Paper and Vintage Key Lock">
        </div>
        <div class="product-body">
          <h3 class="product-title">Personalized Deckle Paper Vintage Lock Journal</h3>
          <p class="product-caption">Vintage key lock · Deckle handmade paper.</p>
          <div class="price-row">
            <span class="current-price">₹1,399</span>
            <span class="original-price">₹1,899</span>
            <span class="discount-tag">26% off</span>
          </div>
          <p class="product-meta">Size: A5 · 220 deckle pages · Name embossing.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Personalized Leather Journal Dairy With Deckle Paper and Vintage Key Lock"
                    data-price="1399">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 6 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Moon+Stone+Embossed" alt="Moon With Stone Embossed Leather Cover Journal Diary With Handmade Paper">
        </div>
        <div class="product-body">
          <h3 class="product-title">Moon & Stone Embossed Leather Journal</h3>
          <p class="product-caption">Moon phase embossing with centre stone.</p>
          <div class="price-row">
            <span class="current-price">₹1,299</span>
            <span class="original-price">₹1,799</span>
            <span class="discount-tag">28% off</span>
          </div>
          <p class="product-meta">Size: A5 · 200 handmade pages · Plain.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Moon With Stone Embossed Leather Cover Journal Diary With Handmade Paper"
                    data-price="1299">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 7 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Deckle+Paper+Lock" alt="Personalised Leather Journal Diary With Deckle Handmade Paper and Lock">
        </div>
        <div class="product-body">
          <h3 class="product-title">Personalised Deckle Paper Journal with Lock</h3>
          <p class="product-caption">Deckle handmade paper · Secure vintage lock.</p>
          <div class="price-row">
            <span class="current-price">₹1,349</span>
            <span class="original-price">₹1,849</span>
            <span class="discount-tag">27% off</span>
          </div>
          <p class="product-meta">Size: A5 · 220 pages.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Personalised Leather Journal Diary With Deckle Handmade Paper and Lock"
                    data-price="1349">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 8 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Brown+Leather+Handmade+Paper" alt="Personalised Brown Leather Diary Journal With Handmade Paper">
        </div>
        <div class="product-body">
          <h3 class="product-title">Personalised Brown Leather Diary</h3>
          <p class="product-caption">Rich brown leather · Handmade paper inside.</p>
          <div class="price-row">
            <span class="current-price">₹999</span>
            <span class="original-price">₹1,399</span>
            <span class="discount-tag">29% off</span>
          </div>
          <p class="product-meta">Size: A5 · 200 pages · Plain.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Personalised Brown Leather Diary Journal With Handmade Paper"
                    data-price="999">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 9 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=A5+Brown+Leather+Notebook" alt="A5 Brown Leather Leather Journal Diary Notebook With Handmade Paper">
        </div>
        <div class="product-body">
          <h3 class="product-title">A5 Brown Leather Journal Notebook</h3>
          <p class="product-caption">Compact A5 notebook with handmade paper.</p>
          <div class="price-row">
            <span class="current-price">₹899</span>
            <span class="original-price">₹1,249</span>
            <span class="discount-tag">28% off</span>
          </div>
          <p class="product-meta">Size: A5 · 180 pages.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="A5 Brown Leather Leather Journal Diary Notebook With Handmade Paper"
                    data-price="899">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 10 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Vintage+Tan+Deckle+Lock" alt="Vintage Tan Brown Leather Journal Dairy With Handmade Deckle Paper and Lock">
        </div>
        <div class="product-body">
          <h3 class="product-title">Vintage Tan Brown Deckle Journal</h3>
          <p class="product-caption">Vintage tan shade · Deckle paper · Lock closure.</p>
          <div class="price-row">
            <span class="current-price">₹1,449</span>
            <span class="original-price">₹1,999</span>
            <span class="discount-tag">28% off</span>
          </div>
          <p class="product-meta">Size: A5 · 220 deckle pages.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Vintage Tan Brown Leather Journal Dairy With Handmade Deckle Paper and Lock"
                    data-price="1449">
              Add to Cart
            </button>
          </div>
        </div>
      </div>

      <!-- 11 -->
      <div class="product-card">
        <div class="product-image-wrapper">
          <img src="https://via.placeholder.com/600x450?text=Handmade+Paper+Leather+Journal" alt="Handmade Paper Leather Diaries Journal With Vintage Deckle Paper">
        </div>
        <div class="product-body">
          <h3 class="product-title">Handmade Paper Leather Diaries Journal</h3>
          <p class="product-caption">Full vintage deckle handmade paper block.</p>
          <div class="price-row">
            <span class="current-price">₹1,249</span>
            <span class="original-price">₹1,749</span>
            <span class="discount-tag">29% off</span>
          </div>
          <p class="product-meta">Size: A5 · 210 deckle pages.</p>
          <div class="product-actions">
            <button class="btn btn-primary add-to-cart"
                    data-name="Handmade Paper Leather Diaries Journal With Vintage Deckle Paper"
                    data-price="1249">
              Add to Cart
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- About & Contact -->
  <section class="section" id="about">
    <h2 class="section-title">About the Brand</h2>
    <div class="about-grid">
      <div class="about-card">
        <h3>Why Our Journals?</h3>
        <p>
          Every journal is made in small batches using full-grain leather and high GSM handmade paper.
          We focus on quality, personalisation and thoughtful packaging so that each piece feels special.
        </p>
        <ul class="about-list">
          <li>100% genuine leather covers.</li>
          <li>Handmade / deckle paper – perfect for writing, sketching & gifts.</li>
          <li>Custom name / initials embossing available on most products.</li>
          <li>Ideal for journaling, travel notes, scrapbooking and gifting.</li>
        </ul>
      </div>
      <div class="contact-card" id="contact">
        <h3>Order / Bulk Enquiry</h3>
        <form onsubmit="handleEnquiry(event)">
          <label for="name">Your Name</label>
          <input type="text" id="name" placeholder="Enter your name" required>

          <label for="email">Email / WhatsApp</label>
          <input type="text" id="email" placeholder="Your email or WhatsApp number" required>

          <label for="message">Which journal are you interested in?</label>
          <textarea id="message" placeholder="Mention product name(s), quantity, customisation etc." required></textarea>

          <button type="submit" class="btn btn-primary" style="width: 100%; margin-top: 0.3rem;">
            Send Enquiry on WhatsApp
          </button>
        </form>
        <p class="contact-note">
          You can also reach us directly on WhatsApp:
          <strong>
            <a href="https://wa.me/919431505374" target="_blank">+91-9431505374</a>
          </strong>
        </p>
      </div>
    </div>
  </section>

  <footer>
    © <span id="year"></span> Leather Journal Studio · All rights reserved.
  </footer>

  <!-- Floating Cart Button -->
  <button class="cart-floating-btn" id="cartFloatingBtn">
    🛒 Cart
    <span class="cart-count" id="cartCount">0</span>
  </button>

  <!-- Cart Panel -->
  <div class="cart-panel-overlay" id="cartOverlay">
    <div class="cart-panel">
      <div class="cart-header">
        <h3>Your Cart</h3>
        <button class="cart-close-btn" id="cartCloseBtn">&times;</button>
      </div>
      <div class="cart-items" id="cartItems">
        <p style="font-size: 0.85rem; color:#7a6c5f;">Your cart is empty.</p>
      </div>
      <div class="cart-footer">
        <div class="cart-total-row">
          <span>Total</span>
          <span id="cartTotal">₹0</span>
        </div>
        <small>
          Click below to pay securely via UPI (PhonePe / GPay / Paytm / BHIM).
        </small>
        <button class="btn btn-primary" style="width: 100%;" onclick="checkoutUPI()">
          Pay Now with UPI
        </button>
      </div>
    </div>
  </div>

  <script>
    // Smooth scroll for sections
    function scrollToSection(id) {
      const el = document.getElementById(id);
      if (el) {
        el.scrollIntoView({ behavior: 'smooth' });
      }
    }

    // Year in footer
    document.getElementById('year').textContent = new Date().getFullYear();

    // Simple cart logic (front-end only)
    const cart = [];
    const cartCountEl = document.getElementById('cartCount');
    const cartTotalEl = document.getElementById('cartTotal');
    const cartItemsEl = document.getElementById('cartItems');
    const cartOverlay = document.getElementById('cartOverlay');
    const cartFloatingBtn = document.getElementById('cartFloatingBtn');
    const cartCloseBtn = document.getElementById('cartCloseBtn');

    function renderCart() {
      cartItemsEl.innerHTML = '';
      if (cart.length === 0) {
        cartItemsEl.innerHTML = '<p style="font-size:0.85rem;color:#7a6c5f;">Your cart is empty.</p>';
      } else {
        cart.forEach((item, index) => {
          const div = document.createElement('div');
          div.className = 'cart-item';
          div.innerHTML = `
            <div class="cart-item-title">${item.name}</div>
            <div>₹${item.price}</div>
            <button class="cart-item-remove" data-index="${index}">Remove</button>
          `;
          cartItemsEl.appendChild(div);
        });
      }

      const total = cart.reduce((sum, item) => sum + item.price, 0);
      cartTotalEl.textContent = '₹' + total;
      cartCountEl.textContent = cart.length;

      // Attach remove handlers
      document.querySelectorAll('.cart-item-remove').forEach(btn => {
        btn.addEventListener('click', function () {
          const i = parseInt(this.getAttribute('data-index'), 10);
          cart.splice(i, 1);
          renderCart();
        });
      });
    }

    function openCart() {
      cartOverlay.style.display = 'flex';
    }

    function closeCart() {
      cartOverlay.style.display = 'none';
    }

    cartFloatingBtn.addEventListener('click', openCart);
    cartCloseBtn.addEventListener('click', closeCart);
    cartOverlay.addEventListener('click', function (e) {
      if (e.target === cartOverlay) closeCart();
    });

    // Add to cart buttons
    document.querySelectorAll('.add-to-cart').forEach(btn => {
      btn.addEventListener('click', function () {
        const name = this.getAttribute('data-name');
        const price = parseInt(this.getAttribute('data-price'), 10);
        cart.push({ name, price });
        renderCart();
        openCart();
      });
    });

    // Enquiry form -> WhatsApp redirect (still WhatsApp, only for enquiry)
    function handleEnquiry(e) {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();

      if (!name || !email || !message) return;

      const text =
        `Hello, my name is ${name}.` +
        `%0AContact: ${email}` +
        `%0AI'm interested in the following journals:` +
        `%0A${message}`;

      const waUrl = `https://wa.me/919431505374?text=${text}`;
      window.open(waUrl, '_blank');

      e.target.reset();
    }

    /***********************
     *  UPI PAYMENT CONFIG *
     ***********************/
    const PAYMENT_CONFIG = {
      upiId: "9431505374-2@axl",          // 🔴 your UPI ID
      name: "Leather Journal Studio"      // name shown in UPI apps
    };

    function isMobile() {
      return /Android|iPhone|iPad|iPod/i.test(navigator.userAgent);
    }

    function buildUpiUrl(amount, customerName) {
      const params = new URLSearchParams({
        pa: PAYMENT_CONFIG.upiId,
        pn: PAYMENT_CONFIG.name,
        am: amount.toString(),
        cu: "INR",
        tn: `Leather journals order - ${customerName || "Customer"}`
      });
      return "upi://pay?" + params.toString();
    }

    function checkoutUPI() {
      if (cart.length === 0) {
        alert('Your cart is empty. Please add at least one journal first.');
        return;
      }

      const total = cart.reduce((sum, item) => sum + item.price, 0);

      // Ask for name (optional, for UPI note)
      const customerName = prompt("Enter your name for the payment (optional):", "") || "Customer";

      if (!isMobile()) {
        const upiUrl = buildUpiUrl(total, customerName);
        alert("UPI payment works best on a mobile phone with a UPI app.\n\nCopy this UPI link and open it on your mobile:\n\n" + upiUrl);
        return;
      }

      const upiUrl = buildUpiUrl(total, customerName);
      window.location.href = upiUrl;
    }
  </script>
</body>
</html>
