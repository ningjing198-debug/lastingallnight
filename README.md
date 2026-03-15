<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>365 shop Inc - Brooklyn Adult Store</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background-color: #111;
      color: #fff;
    }

    /* 顶部 */
    header {
      background: #000;
      padding: 20px;
      text-align: center;
      border-bottom: 2px solid #ff4081;
    }

    .logo {
      width: 200px;
    }

    /* 轮播图 */
    .slider {
      width: 100%;
      height: 420px;
      background: #1a1a1a;
      position: relative;
      overflow: hidden;
      margin-bottom: 30px;
    }

    .slide {
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 30px;
      background: linear-gradient(45deg, #111, #333);
      position: absolute;
      animation: slide 12s infinite;
      opacity: 0;
    }

    .slide:nth-child(1) { animation-delay: 0s; }
    .slide:nth-child(2) { animation-delay: 4s; }
    .slide:nth-child(3) { animation-delay: 8s; }

    @keyframes slide {
      0% { opacity: 0; }
      20% { opacity: 1; }
      40% { opacity: 1; }
      60% { opacity: 0; }
      100% { opacity: 0; }
    }

    /* 店铺信息 */
    .store-info {
      background: #1a1a1a;
      padding: 25px;
      margin: 20px;
      border-radius: 12px;
      border: 1px solid #333;
    }

    .store-info p {
      margin: 8px 0;
      font-size: 16px;
      color: #eee;
    }

    /* 购物车 */
    .cart-bar {
      background: #1a1a1a;
      padding: 15px 25px;
      margin: 20px;
      border-radius: 12px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border: 1px solid #444;
    }

    .cart-count {
      background: #ff4081;
      padding: 5px 12px;
      border-radius: 50px;
      font-weight: bold;
    }

    /* 商品网格 */
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 22px;
      padding: 20px;
    }

    .product-card {
      background: #1a1a1a;
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid #333;
      transition: 0.3s;
    }

    .product-card:hover {
      transform: translateY(-6px);
      border-color: #ff4081;
    }

    .product-img {
      width: 100%;
      height: 230px;
      background: #222;
      object-fit: cover;
    }

    .product-info {
      padding: 18px;
    }

    .product-name {
      font-size: 18px;
      font-weight: bold;
      margin-bottom: 8px;
      color: #fff;
    }

    .product-desc {
      font-size: 14px;
      color: #aaa;
      margin-bottom: 12px;
      height: 40px;
      overflow: hidden;
    }

    .product-price {
      font-size: 21px;
      color: #ff4081;
      font-weight: bold;
      margin-bottom: 14px;
    }

    .add-cart {
      background: #ff4081;
      color: white;
      border: none;
      padding: 11px;
      width: 100%;
      border-radius: 8px;
      cursor: pointer;
      font-size: 15px;
      font-weight: bold;
    }

    .add-cart:hover {
      background: #ff5993;
    }

    .section-title {
      font-size: 26px;
      margin: 40px 20px 15px;
      color: #fff;
    }

    /* 底部 */
    footer {
      background: #000;
      color: white;
      text-align: center;
      padding: 40px 20px;
      margin-top: 50px;
      border-top: 2px solid #ff4081;
    }
  </style>
</head>

<body>
  <header>
    <img src="https://romanticdepot.com/store/wp-content/uploads/2025/09/RD-Logo-2025.webp" alt="Logo" class="logo">
    <h2>365 shop Inc / Brooklyn Adult Sex Toy & Lingerie Store</h2>
  </header>

  <!-- 轮播图 -->
  <div class="slider">
    <div class="slide">24 Hours Open • Discreet Shipping</div>
    <div class="slide">Premium Toys & Luxury Lingerie</div>
    <div class="slide">Male Enhancement • Safe & Private</div>
  </div>

  <!-- 购物车 -->
  <div class="cart-bar">
    <div>🛒 Shopping Cart</div>
    <div>Total: <span id="total">$0</span></div>
    <div class="cart-count" id="count">0</div>
  </div>

  <!-- 店铺信息 -->
  <div class="store-info">
    <p><strong>About:</strong> Professional adult toys, lingeries and male enhancement products. Discreet packaging, safe & private shopping experience.</p>
    <p><strong>Address:</strong> 5704 8th Ave Ste 205, Brooklyn, NY 11220</p>
    <p><strong>Hours:</strong> 24 Hours / 7 Days</p>
    <p><strong>Contact:</strong> 1-800-462-7334</p>
  </div>

  <h3 class="section-title">All Products</h3>
  <div class="products" id="productList">

    <!-- 原有12个 -->
    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2025/05/Elite-3-in-1-G-Spot-Licking-Vibrator1-600x600.jpg.webp">
      <div class="product-info">
        <div class="product-name">Vibrator Pro Max</div>
        <div class="product-desc">Multi-speed silent vibrator, waterproof, medical grade material.</div>
        <div class="product-price">$79.00</div>
        <button class="add-cart" onclick="addCart(79)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/10/Supersonic-Vibrating-Finger-Rose-Vibrator-1.jpg">
      <div class="product-info">
        <div class="product-name">Finger Rose Vibrator</div>
        <div class="product-desc">Supersonic Advanced Silicone.</div>
        <div class="product-price">$59.00</div>
        <button class="add-cart" onclick="addCart(59)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/10/Supersonic-LCD-Display-Silicone-Wand-1-600x600.jpg">
      <div class="product-info">
        <div class="product-name">High-quality silicone rods</div>
        <div class="product-desc">Supersonic LCD screen.</div>
        <div class="product-price">$69.00</div>
        <button class="add-cart" onclick="addCart(69)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2025/04/Play-with-Me-Pink-Real-Feel-Sensation-Remote-Control-Thursting-Dildo1-3.jpg">
      <div class="product-info">
        <div class="product-name">Realistic remote-controlled vibrating dildo</div>
        <div class="product-desc">8-inch - Purple.</div>
        <div class="product-price">$67.00</div>
        <button class="add-cart" onclick="addCart(67)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2026/03/Zero-Tolereance-Riley-Reid-10-600x600.jpg">
      <div class="product-info">
        <div class="product-name">Zero Tolerance</div>
        <div class="product-desc">Large Body Stroker W/ Riley Reid Download Code.</div>
        <div class="product-price">$189.00</div>
        <button class="add-cart" onclick="addCart(189)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/10/Naughty-USA-Edible-Juicy-Strawberry-Elite-Lubrican-600x600.jpg">
      <div class="product-info">
        <div class="product-name">American Naughty Strawberry Lubricant – 1 4 oz</div>
        <div class="product-desc">Water-based, non-toxic, long lasting formula.</div>
        <div class="product-price">$59.00</div>
        <button class="add-cart" onclick="addCart(59)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/08/Elite-Torso-Realistic-Feel-with-XL-Breasts-Pussy-and-Asshole-600x600.jpg">
      <div class="product-info">
        <div class="product-name">Elite Torso Realistic Feel Torso Sex Doll with Lifelike Breasts</div>
        <div class="product-desc">Pussy & Asshole – Natural Vanilla.</div>
        <div class="product-price">$179.00</div>
        <button class="add-cart" onclick="addCart(179)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2025/03/Seduce-Me-Sapphire-The-Realistic-Doll1-600x600.jpg">
      <div class="product-info">
        <div class="product-name">Seduce Me Sapphire Realistic Sex Doll</div>
        <div class="product-desc">Realistic touch, smooth vaginal skin, a good companion that will always be with you..</div>
        <div class="product-price">$999.00</div>
        <button class="add-cart" onclick="addCart(999)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2025/03/Curvy-Kim-The-Realistic-Doll5-1.jpg">
      <div class="product-info">
        <div class="product-name">Bang Me Bianca</div>
        <div class="product-desc">Realistic Sex Doll.</div>
        <div class="product-price">$999.00</div>
        <button class="add-cart" onclick="addCart(999)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/08/Elite-Realistic-Feel-Gigantic-Ass-Pussy-5.JPG">
      <div class="product-info">
        <div class="product-name">Elite Snow Bunny Real Feel Life Size Big Booty</div>
        <div class="product-desc"> Natural Vanilla.</div>
        <div class="product-price">$219.00</div>
        <button class="add-cart" onclick="addCart(219)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/10/Elite-Feels-So-Real-Remote-Control-Thrusting-Dildo-Mocha-3.jpg">
      <div class="product-info">
        <div class="product-name">Elite Feels So Real</div>
        <div class="product-desc">Premium Silicone Remote Control 7.5″ Realistic Thrusting Dildo – Tan.</div>
        <div class="product-price">$89.00</div>
        <button class="add-cart" onclick="addCart(89)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/09/Ass-Relax-Premium-Anal-Desensitizing-Water-Based-Lubricant-4-25-oz-768x768.webp">
      <div class="product-info">
        <div class="product-name">Ass Relax </div>
        <div class="product-desc">Premium Anal Desensitizing Water-Based Lubricant 14.25oz.</div>
        <div class="product-price">$68.00</div>
        <button class="add-cart" onclick="addCart(68)">Add to Cart</button>
      </div>
    </div>

    <!-- 新增10个商品 -->
    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/11/4-Cuff-Expandable-Spreader-Bar-Set-3.jpg">
      <div class="product-info">
        <div class="product-name">4 Cuff Expandable Spreader Bar Set</div>
        <div class="product-desc">Dual stimulation,  waterproof design.</div>
        <div class="product-price">$70.00</div>
        <button class="add-cart" onclick="addCart(70)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/09/lux-fetish-quality-love-sex-swing-packaging-08_1000x1000-copy.jpg">
      <div class="product-info">
        <div class="product-name">Lux Fetish</div>
        <div class="product-desc">Stand-Up Sex Swing for Couples – Black.</div>
        <div class="product-price">$129.00</div>
        <button class="add-cart" onclick="addCart(129)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/11/water-based-mood-lube-personal-lubricant-32-oz-600x600.jpg.webp">
      <div class="product-info">
        <div class="product-name">Water-Based Mood Lube Personal Lubricant</div>
        <div class="product-desc">32 Oz.</div>
        <div class="product-price">$59.00</div>
        <button class="add-cart" onclick="addCart(59)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/10/Cloud-9-Novelties-Health-Wellness-Deluxe-Anal-Enema-Douche-With-Rechargeable-Sprinkler-Pump-Remote-Control.jpeg">
      <div class="product-info">
        <div class="product-name">Cloud 9 Novelties</div>
        <div class="product-desc">Health & Wellness Deluxe Anal Enema Douche With Rechargeable Sprinkler Pump & Remote Control.</div>
        <div class="product-price">$79.00</div>
        <button class="add-cart" onclick="addCart(79)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2026/03/Elite-App-Based-Silver-Heart-Shaped-LED-Butt-Plug-with-Remote-Control-Main-Pic-768x768.jpg.webp">
      <div class="product-info">
        <div class="product-name">Anal training device </div>
        <div class="product-desc">Elite App Based Silver Heart Shaped LED Butt Plug with Remote Control.</div>
        <div class="product-price">$49.00</div>
        <button class="add-cart" onclick="addCart(49)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2026/02/Fix-the-background-so-it-fills-the-entire-frame-11.jpg">
      <div class="product-info">
        <div class="Fleshlight Girls Riley Reid</div>
        <div class="product-desc">Mouth Stroker Masturbator Insomnia.</div>
        <div class="product-price">$89.00</div>
        <button class="add-cart" onclick="addCart(89)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2025/11/Elite-Realistic-Sucking-Lips-Caramel.jpg">
      <div class="product-info">
        <div class="product-name">Elite Realistic Sucking Lips Caramel</div>
        <div class="product-desc">Super realistic touch, a paradise for men who love oral sex..</div>
        <div class="product-price">$109.00</div>
        <button class="add-cart" onclick="addCart(109)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2025/01/BDMS-Kit.webp">
      <div class="product-info">
        <div class="product-name">BDSM Kit</div>
        <div class="product-desc">You deserve to keep your married life fresh and exciting..</div>
        <div class="product-price">$119.00</div>
        <button class="add-cart" onclick="addCart(119)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/08/Liquid-V-for-Men-1-oz-Bottle-600x600.jpg">
      <div class="product-info">
        <div class="product-name">Liquid V for Men Stimulating Gel</div>
        <div class="product-desc">5 oz Bottle.</div>
        <div class="product-price">$89.00</div>
        <button class="add-cart" onclick="addCart(89)">Add to Cart</button>
      </div>
    </div>

    <div class="product-card">
      <img class="product-img" src="https://romanticdepot.com/store/wp-content/uploads/2024/08/SPANISH-FLY-LIQUID-VIRGIN-CHERRY-600x600.jpg">
      <div class="product-info">
        <div class="product-name">Original Spanish Fly Liquid Elixir</div>
        <div class="product-desc">Cherry Flavor.</div>
        <div class="product-price">$49.00</div>
        <button class="add-cart" onclick="addCart(49)">Add to Cart</button>
      </div>
    </div>

  </div>

  <div class="store-info">
    <h3 style="margin-bottom:12px;">Delivery & Payment</h3>
    <p><strong>Delivery:</strong> Express Shipping | In-store Pickup | Local Delivery</p>
    <p><strong>Payment Address:</strong> TBBFsXpjB8MP38KXhU7D1RijTd8GsKfFyX</p>
    <p><strong>Service:</strong> 24H open, discreet package, privacy guaranteed.</p>
  </div>

  <footer>
    <p>365 shop Inc / Brooklyn Adult Sex Toy & Lingerie Store</p>
    <p>5704 8th Ave Ste 205, Brooklyn, NY 11220 | Tel: 1-800-462-7334</p>
    <p>© 2025 All Rights Reserved | 24 Hours Service</p>
  </footer>

  <!-- 购物车功能 -->
  <script>
    let total = 0;
    let count = 0;

    function addCart(price) {
      total += price;
      count += 1;
      document.getElementById("total").innerText = "$" + total;
      document.getElementById("count").innerText = count;
      alert("Added to cart successfully!");
    }
  </script>
</body>
</html>
