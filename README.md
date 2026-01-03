<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Only For You ❤️</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      min-height: 100vh;
      overflow-x: hidden;
      color: #333;
    }
    .container {
      max-width: 900px;
      margin: auto;
      padding: 40px 20px 90px;
      text-align: center;
    }
    h1 {
      font-size: 2.8rem;
      margin-bottom: 10px;
    }
    .subtitle {
      font-size: 1.2rem;
      opacity: 0.95;
      margin-bottom: 30px;
    }
    .card {
      background: rgba(255,255,255,0.95);
      border-radius: 22px;
      padding: 28px;
      margin: 22px 0;
      box-shadow: 0 20px 40px rgba(0,0,0,0.18);
      animation: float 6s ease-in-out infinite;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    .photos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 15px;
      margin-top: 15px;
    }
    .photo {
      border-radius: 16px;
      height: 170px;
      overflow: hidden;
    }
    .photo img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .btn {
      margin-top: 22px;
      background: #ff4d6d;
      color: #fff;
      border: none;
      padding: 15px 30px;
      font-size: 1.1rem;
      border-radius: 999px;
      cursor: pointer;
      box-shadow: 0 10px 25px rgba(255,77,109,0.45);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }
    .btn:hover {
      transform: translateY(-2px) scale(1.04);
      box-shadow: 0 14px 30px rgba(255,77,109,0.6);
    }
    .hidden { display: none; }
    .love-text {
      font-size: 1.2rem;
      line-height: 1.8;
    }
    footer {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      text-align: center;
      padding: 10px;
      font-size: 0.9rem;
      background: rgba(255,255,255,0.65);
      backdrop-filter: blur(6px);
    }
    .heart {
      position: fixed;
      bottom: -20px;
      font-size: 22px;
      animation: rise 6s linear infinite;
      opacity: 0.85;
    }
    @keyframes rise {
      from { transform: translateY(0) scale(1); opacity: 1; }
      to { transform: translateY(-120vh) scale(1.9); opacity: 0; }
    }
  </style>
</head>
<body>  <!-- Background Music -->  <audio id="bgMusic" loop>
    <!-- Replace love-song.mp3 with your romantic song -->
    <source src="love-song.mp3" type="audio/mpeg">
  </audio>  <div class="container">
    <h1>Hey ❤️ (Shabana)</h1>
    <div class="subtitle">This little website is made only for you</div><div class="card">
  <h2>Our Beautiful Moments ✨</h2>
  <p>Ye photos sirf yaadein nahi hain… ye meri duniya hain 💖</p>
  <div class="photos">
    <div class="photo"><img src="photo1.jpg" alt="Memory 1"></div>
    <div class="photo"><img src="photo2.jpg" alt="Memory 2"></div>
    <div class="photo"><img src="photo3.jpg" alt="Memory 3"></div>
    <div class="photo"><img src="photo4.jpg" alt="Memory 4"></div>
  </div>
</div>

<div class="card">
  <h2>From My Heart 💌</h2>
  <p class="love-text">
    Tum meri life ka wo hissa ho jiske bina sab adhoora lagta hai.
    When I am with you, even silence feels beautiful.
    Tumhari smile meri strength hai aur tumhara saath meri peace. ❤️
  </p>

  <button class="btn" onclick="startLove()">Tap to Feel My Love 🎶💖</button>

  <div id="surprise" class="hidden">
    <p class="love-text" style="margin-top:18px;">
      Chahe life kitni bhi difficult ho jaaye,
      <br><strong>I promise — I will always choose you.</strong>
      <br>Tum meri aadat nahi, meri zarurat ho 🌸
    </p>
  </div>
</div>

  </div>  <footer>
    Made with endless love ❤️
  </footer>  <script>
    function startLove() {
      document.getElementById('surprise').classList.remove('hidden');
      document.getElementById('bgMusic').play();
      spawnHearts();
    }

    function spawnHearts() {
      for (let i = 0; i < 30; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.innerText = '❤️';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = 4 + Math.random() * 3 + 's';
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 7000);
      }
    }
  </script></body>
</html>
