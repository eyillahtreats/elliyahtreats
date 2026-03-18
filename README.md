<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>EYILLA'S TASTY TREATS · BITING INTO BLISS</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts: Cinematic Clash Display + Space Grotesk -->
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&family=Syne:wght@800;900&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* RADICAL COLOR SYSTEM — deep, warm, luxurious */
    :root {
      --obsidian: #1a0f0a;
      --cocoa: #2c1810;
      --ember: #d45f2e;
      --gold-fusion: #c88c4b;
      --cream-silk: #fae1c3;
      --caramel-satin: #b4824a;
      --rosewood: #592f1c;
      --chocolate-velvet: #3f2317;
      --liquid-amber: #e98a3e;
    }

    body {
      background: var(--obsidian);
      font-family: 'Space Grotesk', sans-serif;
      color: var(--cream-silk);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow-x: hidden;
    }

    /* LIQUID BACKGROUND — abstract shapes that move */
    .liquid-bg {
      position: fixed;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: 0;
      filter: blur(80px);
      opacity: 0.6;
    }

    .liquid-bg span {
      position: absolute;
      width: 50vmax;
      height: 50vmax;
      border-radius: 50%;
      background: radial-gradient(circle at 30% 30%, var(--ember), var(--rosewood));
      animation: liquid-morph 18s infinite alternate ease-in-out;
    }

    .liquid-bg span:nth-child(1) {
      top: -20vh;
      right: -10vw;
      background: radial-gradient(circle, #c06534, #4e2b19);
      animation-duration: 24s;
    }
    .liquid-bg span:nth-child(2) {
      bottom: -30vh;
      left: -20vw;
      width: 80vmax;
      height: 80vmax;
      background: radial-gradient(circle, #b4642e, #2e1b12);
      animation-duration: 32s;
      animation-direction: reverse;
    }

    @keyframes liquid-morph {
      0% { transform: translate(0, 0) scale(1) rotate(0deg); border-radius: 60% 40% 30% 70%; }
      100% { transform: translate(8%, -5%) scale(1.2) rotate(8deg); border-radius: 30% 70% 60% 40%; }
    }

    /* MAIN SCULPTURAL CONTAINER — broken grid, asymmetric */
    .dimensional-grid {
      max-width: 480px;
      width: 100%;
      margin: 0.8rem;
      position: relative;
      z-index: 10;
      display: flex;
      flex-direction: column;
      gap: 1.2rem;
      padding: 1rem 0;
    }

    /* HYBRID CARD SYSTEM — deconstructed layout */
    .hero-panel {
      background: rgba(44, 24, 16, 0.7);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      border: 1px solid rgba(212, 95, 46, 0.25);
      border-radius: 3rem 3rem 3rem 0.5rem;
      padding: 2rem 1.8rem;
      box-shadow: 0 30px 40px -20px #140b07, inset 0 1px 2px rgba(255,215,160,0.15);
      transform: rotate(-0.3deg);
      transition: transform 0.3s;
    }

    .hero-panel:hover {
      transform: rotate(0deg) scale(1.01);
    }

    .hero-clash {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: flex-start;
    }

    .hero-clash h1 {
      font-family: 'Syne', sans-serif;
      font-size: 3.5rem;
      font-weight: 900;
      line-height: 0.85;
      text-transform: uppercase;
      background: linear-gradient(130deg, #fccf9c, #eb9f60, #f7b475);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      max-width: 70%;
      letter-spacing: -2px;
      filter: drop-shadow(0 0 18px #c06028);
    }

    .slogan-mask {
      background: var(--chocolate-velvet);
      padding: 0.8rem 1.8rem;
      border-radius: 100px;
      font-size: 1.4rem;
      font-weight: 700;
      border: 2px solid var(--liquid-amber);
      transform: rotate(2deg) translateX(-10px);
      color: #fadbb8;
      text-transform: uppercase;
      letter-spacing: 2px;
      box-shadow: 0 10px 0 #341e14;
      align-self: flex-end;
    }

    /* SCULPTURAL PRODUCT GRID — broken into shards */
    .product-shards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 0.9rem;
      margin: 0.5rem 0 1rem;
    }

    .shard-item {
      background: rgba(69, 37, 24, 0.7);
      backdrop-filter: blur(8px);
      border: 1px solid #b7653066;
      border-radius: 2rem 0.5rem 2rem 0.5rem;
      padding: 1.2rem 0.4rem;
      text-align: center;
      font-weight: 700;
      font-size: 0.85rem;
      color: #ffe4cb;
      box-shadow: 8px 8px 0 #2f1b12;
      transition: 0.15s;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.4rem;
      backdrop-filter: blur(12px);
    }

    .shard-item i {
      font-size: 2.2rem;
      color: var(--liquid-amber);
      filter: drop-shadow(2px 4px 4px #251106);
    }

    .shard-item:nth-child(2) { border-radius: 0.5rem 2rem 0.5rem 2rem; background: #4a2d1dcc; }
    .shard-item:nth-child(5) { border-radius: 2rem 0.5rem 2rem 0.5rem; }
    .shard-item:nth-child(7) { border-radius: 0.5rem 2rem 0.5rem 2rem; }
    .shard-item:active { transform: scale(0.92); box-shadow: 2px 2px 0 #311d13; }

    /* INFO PANEL — brutalist map integration */
    .brutal-card {
      background: #2f1b10e0;
      backdrop-filter: blur(15px);
      border: 1px solid #b3713e;
      border-radius: 0.8rem 3rem 0.8rem 3rem;
      padding: 1.8rem 1.2rem;
      box-shadow: 20px 20px 0 #0d0704;
    }

    .contact-block {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }

    .wa-phone-group {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .phone-slab {
      background: #20120b;
      border-radius: 2rem 0.5rem 2rem 0.5rem;
      padding: 1rem 1.5rem;
      flex: 1;
      min-width: 130px;
      border-left: 6px solid var(--ember);
      font-weight: 700;
      font-size: 1.2rem;
      display: flex;
      align-items: center;
      gap: 12px;
      color: #fac89d;
    }

    .phone-slab i {
      font-size: 1.8rem;
    }

    .map-dystopian {
      border-radius: 1rem 3rem 1rem 3rem;
      overflow: hidden;
      height: 190px;
      border: 3px solid #a65323;
      box-shadow: 12px 12px 0 #341e12;
      margin: 1.8rem 0 1rem;
    }

    .map-dystopian iframe {
      width: 100%;
      height: 100%;
      filter: grayscale(0.7) sepia(0.5) hue-rotate(320deg);
    }

    .address-chaos {
      font-size: 1.1rem;
      background: #4e311f;
      padding: 1rem 1.8rem;
      border-radius: 3rem 0.5rem 3rem 0.5rem;
      display: inline-block;
      font-weight: 600;
      border: 1px dashed #e29f60;
      letter-spacing: 0px;
    }

    /* ORDER FORM — deconstructed brutalist */
    .order-abyss {
      background: #23160ed9;
      backdrop-filter: blur(25px);
      border-radius: 3rem 0.3rem 3rem 0.3rem;
      padding: 2.2rem 1.5rem;
      border: 2px solid #b55d2b;
      box-shadow: -15px 20px 0 #2b180f, inset 0 0 30px #3c2316;
    }

    .order-abyss h2 {
      font-size: 2.8rem;
      font-weight: 900;
      font-family: 'Syne', sans-serif;
      color: #fbca98;
      text-transform: uppercase;
      line-height: 1;
      margin-bottom: 2rem;
      word-break: break-word;
    }

    .input-gruv {
      margin-bottom: 1.8rem;
    }

    .input-gruv label {
      display: flex;
      align-items: center;
      gap: 8px;
      font-weight: 500;
      font-size: 1.2rem;
      margin-bottom: 6px;
      color: #edb581;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .input-gruv input, .input-gruv select, .input-gruv textarea {
      width: 100%;
      background: #312016;
      border: 2px solid #9f6137;
      border-radius: 2rem 0.3rem 2rem 0.3rem;
      padding: 1.2rem 1.5rem;
      font-size: 1.1rem;
      color: #ffe9d7;
      outline: none;
      transition: 0.2s;
    }

    .input-gruv input:focus, .input-gruv select:focus, .input-gruv textarea:focus {
      border-color: #f5984a;
      box-shadow: 0 0 0 4px #ac592e6b;
      background: #3f281b;
    }

    .order-trigger {
      background: #d4662b;
      border: none;
      padding: 1.6rem;
      width: 100%;
      border-radius: 3rem 0.5rem 3rem 0.5rem;
      font-size: 2.2rem;
      font-weight: 900;
      font-family: 'Syne', sans-serif;
      color: #1f110a;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 18px;
      box-shadow: 0 15px 0 #733e1f;
      transition: 0.1s;
      margin-top: 1.2rem;
      text-transform: uppercase;
    }

    .order-trigger:active {
      transform: translateY(8px);
      box-shadow: 0 7px 0 #733e1f;
    }

    /* special footer */
    .signature-offset {
      display: flex;
      justify-content: space-between;
      font-size: 0.9rem;
      color: #cfa977;
      background: #1e130d;
      border-radius: 0.5rem 2rem 0.5rem 2rem;
      padding: 1rem 1.5rem;
      border: 1px solid #825d3e;
      margin-bottom: 0.5rem;
    }

    /* loader cinematic */
    #deep-loader {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #0e0804;
      z-index: 9999;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: 1s;
    }

    .loader-content {
      text-align: center;
      animation: glitch 1.5s infinite;
    }

    @keyframes glitch {
      0% { transform: skew(0deg, 0deg); opacity: 1; }
      5% { transform: skew(5deg, -2deg); opacity: 0.8; text-shadow: 3px 0 red; }
      10% { transform: skew(-5deg, 2deg); text-shadow: -3px 0 blue; }
      15% { transform: skew(0deg); }
    }

    .loader-content i {
      font-size: 5rem;
      color: var(--liquid-amber);
      filter: drop-shadow(0 0 25px #f28b3c);
    }

    .loader-content h2 {
      font-size: 4rem;
      font-family: 'Syne', sans-serif;
      color: #fcc694;
      line-height: 0.9;
    }
  </style>
</head>
<body>
  <!-- DEEP LOADER (disappears after 2s) -->
  <div id="deep-loader">
    <div class="loader-content">
      <i class="fas fa-crown"></i>
      <h2>EYILLA'S</h2>
      <div style="color:#c3824a;">BITE INTO BLISS</div>
    </div>
  </div>

  <!-- LIQUID LIVING BACKGROUND -->
  <div class="liquid-bg">
    <span></span>
    <span></span>
  </div>

  <!-- MAIN ASYMMETRIC GRID -->
  <div class="dimensional-grid">

    <!-- HERO AREA: broken hierarchy -->
    <div class="hero-panel">
      <div class="hero-clash">
        <h1>EYILLA'S<br>TASTY<br>TREATS</h1>
        <div class="slogan-mask">#BITEINTOBLISS</div>
      </div>
    </div>

    <!-- PRODUCT SHARDS: edgy fragments -->
    <div class="product-shards">
      <div class="shard-item"><i class="fas fa-milk"></i> MILKSHAKES</div>
      <div class="shard-item"><i class="fas fa-ice-cream"></i> FROSTY ICE</div>
      <div class="shard-item"><i class="fas fa-wine-glass"></i> JUICES</div>
      <div class="shard-item"><i class="fas fa-drumstick-bite"></i> SMALL CHOPS</div>
      <div class="shard-item"><i class="fas fa-cake"></i> BIRTHDAY</div>
      <div class="shard-item"><i class="fas fa-ring"></i> WEDDING</div>
      <div class="shard-item"><i class="fas fa-cupcake"></i> BENTO CUP</div>
      <div class="shard-item"><i class="fas fa-bread-slice"></i> PASTRIES</div>
      <div class="shard-item"><i class="fas fa-candy-cane"></i> EXTRA</div>
    </div>

    <!-- CONTACT + MAP: brutalist block -->
    <div class="brutal-card">
      <div class="contact-block">
        <div class="wa-phone-group">
          <div class="phone-slab"><i class="fab fa-whatsapp"></i> <a href="https://wa.me/233599838472?text=EYILLA!%20I%20need%20the%20deep%20treats%20🔥" style="color:#fac89d; text-decoration:none;">0599838472</a></div>
          <div class="phone-slab"><i class="fas fa-phone"></i> <a href="tel:+233272406561" style="color:#fac89d; text-decoration:none;">0272406561</a></div>
        </div>

        <!-- MAP with attitude -->
        <div class="map-dystopian">
          <iframe src="https://www.openstreetmap.org/export/embed.html?bbox=-0.4582%2C5.5345%2C-0.4325%2C5.5500&layer=mapnik&marker=5.5425%2C-0.4453" loading="lazy"></iframe>
        </div>
        <div class="address-chaos">
          <i class="fas fa-location-dot" style="color:#f28237;"></i> KASOA WALENTU, 2ND STREET BEHIND CHURCH OF PENTECOST
        </div>
      </div>
    </div>

    <!-- ORDER FORM — deep, dark, interactive -->
    <div class="order-abyss" id="order-section">
      <h2>ORDER<br>PORTAL</h2>
      <form id="waFormDeep" onsubmit="return sendDeepOrder(event)">
        <div class="input-gruv">
          <label><i class="fas fa-user"></i> YOUR IDENTITY</label>
          <input type="text" id="deepName" placeholder="e.g. Ama" required>
        </div>
        <div class="input-gruv">
          <label><i class="fas fa-cake"></i> CRAVING</label>
          <select id="deepCategory" required>
            <option value="" disabled selected>— SELECT TREAT —</option>
            <option>MILKSHAKE</option>
            <option>FROSTY ICE</option>
            <option>JUICE/DRINK</option>
            <option>SMALL CHOPS</option>
            <option>BIRTHDAY CAKE</option>
            <option>WEDDING CAKE</option>
            <option>BENTO/CUPCAKE</option>
            <option>PASTRIES</option>
          </select>
        </div>
        <div class="input-gruv">
          <label><i class="fas fa-pen"></i> DETAILS / FLAVOUR</label>
          <textarea id="deepDetails" rows="2" placeholder="e.g. 2 chocolate shakes, red velvet bento" required></textarea>
        </div>
        <div class="input-gruv">
          <label><i class="fas fa-location-dot"></i> DELIVERY ZONE</label>
          <input type="text" id="deepLocation" value="Kasoa Walentu" required>
        </div>
        <div class="input-gruv">
          <label><i class="fas fa-coins"></i> BUDGET (GHS)</label>
          <input type="text" id="deepBudget" placeholder="e.g. 250" required>
        </div>
        <button type="submit" class="order-trigger"><i class="fab fa-whatsapp"></i> I'M READY</button>
        <p style="margin-top: 1.5rem; font-size: 0.9rem; color: #ad7d56; text-align: center;">⇾ you'll continue on WhatsApp with order pre-filled</p>
      </form>
    </div>

    <!-- footer with brutal touch -->
    <div class="signature-offset">
      <span>© EYILLA'S DEEP TREATS</span>
      <span>📍 WALENTU 2ND ST</span>
    </div>
  </div>

  <script>
    // kill loader after 2 sec
    window.addEventListener('load', function() {
      setTimeout(() => {
        document.getElementById('deep-loader').style.opacity = '0';
        setTimeout(() => {
          document.getElementById('deep-loader').style.display = 'none';
        }, 1000);
      }, 1800);
    });

    // whatsapp redirect with raw edge
    function sendDeepOrder(e) {
      e.preventDefault();

      const name = document.getElementById('deepName').value.trim();
      const category = document.getElementById('deepCategory').value;
      const details = document.getElementById('deepDetails').value.trim();
      const location = document.getElementById('deepLocation').value.trim();
      const budget = document.getElementById('deepBudget').value.trim();

      if (!name || !category || !details || !location || !budget) {
        alert("🔥 fill every field — Eyilla demands perfection.");
        return false;
      }

      const waNumber = '233599838472';
      const message = 
        `🔴 *EYILLA'S DEEP ORDER* 🔴%0a` +
        `⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯%0a` +
        `👤 *NAME:* ${name}%0a` +
        `🍫 *TREAT:* ${category}%0a` +
        `📦 *DETAILS:* ${details}%0a` +
        `📍 *WHERE:* ${location}%0a` +
        `💰 *BUDGET:* GHS ${budget}%0a` +
        `⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯⎯%0a` +
        `_BITE INTO BLISS_ 🍪`;

      window.open(`https://wa.me/${waNumber}?text=${message}`, '_blank');
      return false;
    }

    // dynamic shard haptics
    document.querySelectorAll('.shard-item').forEach(el => {
      el.addEventListener('click', function() { this.style.backgroundColor = '#623b26'; setTimeout(()=> this.style.backgroundColor = '', 100); });
    });
  </script>
</body>
</html>
