<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Feyza'ya Özür ve Sürpriz</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Arial', sans-serif;
      background: #0a0a0a;
      overflow: hidden;
      position: relative;
    }
    .container {
      text-align: center;
      background: rgba(255, 255, 255, 0.85);
      padding: 40px;
      border-radius: 25px;
      box-shadow: 0 6px 30px rgba(0,0,0,0.5);
      z-index: 3;
      position: relative;
      animation: fadeIn 2s ease-in-out;
    }
    h1 {
      color: #e91e63;
      font-size: 2.8em;
      text-shadow: 0 0 15px rgba(233,30,99,0.6);
      animation: heartbeat 2s infinite;
    }
    p {
      font-size: 1.3em;
      color: #333;
    }
    button {
      background: linear-gradient(135deg, #e91e63, #f06292);
      color: white;
      border: none;
      padding: 12px 25px;
      font-size: 1.1em;
      border-radius: 12px;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    button:hover {
      transform: scale(1.1);
      box-shadow: 0 0 20px rgba(233,30,99,0.6);
    }

    /* Yağmur damlaları */
    .raindrop {
      position: absolute;
      width: 2px;
      height: 15px;
      background: rgba(255,255,255,0.6);
      top: -20px;
      animation: fall linear infinite;
      z-index: 2;
    }

    @keyframes fall {
      to { transform: translateY(110vh); }
    }

    /* Pencere efekti */
    .window {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(200, 200, 255, 0.05);
      backdrop-filter: blur(2px);
      z-index: 1;
    }

    /* Kalp arka plan */
    .heart-bg {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 320px;
      height: 300px;
      background: radial-gradient(circle at 30% 30%, rgba(255,0,100,0.5), transparent 70%),
                  radial-gradient(circle at 70% 30%, rgba(255,0,150,0.5), transparent 70%),
                  radial-gradient(circle at 50% 70%, rgba(255,0,80,0.5), transparent 70%);
      clip-path: polygon(50% 0%, 100% 35%, 80% 100%, 50% 80%, 20% 100%, 0% 35%);
      animation: pulse 4s infinite;
      filter: blur(10px);
      z-index: 0;
    }

    @keyframes pulse {
      0%, 100% { transform: translate(-50%, -50%) scale(1); opacity: 0.3; }
      50% { transform: translate(-50%, -50%) scale(1.2); opacity: 0.7; }
    }

    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      25% { transform: scale(1.1); }
      50% { transform: scale(0.95); }
      75% { transform: scale(1.05); }
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Konfeti */
    .confetti {
      position: fixed;
      width: 10px;
      height: 10px;
      background-color: red;
      animation: fall 3s linear infinite;
      z-index: 999;
    }
    @keyframes fallConfetti {
      from { transform: translateY(-10vh) rotate(0deg); }
      to { transform: translateY(100vh) rotate(720deg); }
    }
  </style>
</head>
<body>
  <div class="heart-bg"></div>
  <div class="window"></div>
  <div class="container">
    <h1>Sevgili Feyza ❤️</h1>
    <p>Sana yaptığım şey seni üzdüyse çok özür dilerim. Böyle olacağını tahmin etmemiştim.</p>
    <p>Sen benim için çok özelsin 💕</p>
    <button onclick="showSurprise()">Sürprizi Gör 🎁</button>
    <div id="surprise" style="display:none; margin-top:25px; font-size:1.6em; color:#e91e63; font-weight:bold; text-shadow: 0 0 10px rgba(233,30,99,0.6);">
      💖 SANA HER ZAMAN SADIK VE SEVGİ DOLU OLACAĞIM 💖
    </div>
  </div>

  <script>
    function createRain() {
      for (let i = 0; i < 60; i++) {
        let drop = document.createElement('div');
        drop.classList.add('raindrop');
        drop.style.left = Math.random() * window.innerWidth + 'px';
        drop.style.animationDuration = (1 + Math.random() * 1.5) + 's';
        document.body.appendChild(drop);
        setTimeout(() => drop.remove(), 3000);
      }
    }
    setInterval(createRain, 500);

    function showSurprise() {
      document.getElementById('surprise').style.display = 'block';
      for (let i = 0; i < 120; i++) {
        let confetti = document.createElement('div');
        confetti.classList.add('confetti');
        confetti.style.left = Math.random() * window.innerWidth + 'px';
        confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 50%)`;
        confetti.style.animation = `fallConfetti ${(2 + Math.random() * 3)}s linear`;
        document.body.appendChild(confetti);
        setTimeout(() => confetti.remove(), 4000);
      }
    }
  </script>
</body>
</html>
