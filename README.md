[index.html](https://github.com/user-attachments/files/24639070/index.html)
<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mines Hack</title>
  <style>
    body { background: #0d0d0d; color: white; font-family: Arial; margin: 0; padding: 0; }
    .top { display: flex; justify-content: center; gap: 30px; padding: 15px; background: #111; }
    .top-btn { background: #222; padding: 10px 25px; border-radius: 50px; font-size: 18px; }
    .header { text-align: center; padding: 20px; font-size: 28px; font-weight: bold; }
    .menu-icon { position: absolute; top: 20px; right: 20px; font-size: 30px; cursor: pointer; }
    .menu { display: none; position: absolute; top: 70px; right: 20px; background: #1a1a1a; border-radius: 10px; padding: 15px; box-shadow: 0 0 15px rgba(0,0,0,0.8); z-index: 10; }
    .menu button { display: block; width: 100%; padding: 12px; margin: 8px 0; background: #333; border: none; color: white; border-radius: 8px; cursor: pointer; }
    .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px; padding: 20px; }
    .card { background: #1a1a1a; border-radius: 20px; overflow: hidden; text-align: center; box-shadow: 0 5px 15px rgba(0,0,0,0.7); }
    .card img { width: 100%; }
    .open-btn { background: #00cc00; color: black; padding: 15px; font-weight: bold; border: none; width: 100%; font-size: 18px; cursor: pointer; }
    .bottom { background: #00cc00; color: black; text-align: center; padding: 25px; font-size: 32px; margin: 20px; border-radius: 20px; font-weight: bold; }
    #signalPopup { display: none; position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); background: rgba(0,0,0,0.9); padding: 30px; border-radius: 20px; text-align: center; z-index: 100; max-width: 90%; }
    #signalPopup button { margin-top: 15px; background: #00cc00; color: black; padding: 12px 30px; border: none; border-radius: 10px; font-size: 18px; cursor: pointer; }
  </style>
</head>
<body>
  <div class="top">
    <div class="top-btn">📱 Android</div>
    <div class="top-btn">🌍 Global</div>
  </div>

  <div class="menu-icon" onclick="toggleMenu()">☰</div>
  <div class="menu" id="menu">
    <button onclick="changeLang('tr')">🇹🇷 Türkçe</button>
    <button onclick="changeLang('en')">🇬🇧 English</button>
    <button onclick="getSignal()">📡 Sinyal Al</button>
  </div>

  <div class="header">🚀 Mines Hack</div>

  <div class="grid">
    <div class="card">
      <img src="https://i.imgur.com/YOUR_MINES_ICON.png" alt="MINES"> <!-- kendi ikon linkini koy -->
      <button class="open-btn" onclick="window.open('https://1win.com')">AÇ</button>
    </div>
    <div class="card">
      <img src="https://i.imgur.com/YOUR_MI_ICON.png" alt="Mi Mines">
      <button class="open-btn" onclick="window.open('https://1win.com')">AÇ</button>
    </div>
    <div class="card">
      <img src="https://i.imgur.com/YOUR_BOMBA_ICON.png" alt="BOMBA">
      <button class="open-btn" onclick="window.open('https://1win.com')">AÇ</button>
    </div>
    <div class="card">
      <img src="https://i.imgur.com/YOUR_MINES2_ICON.png" alt="MINES">
      <button class="open-btn" onclick="window.open('https://1win.com')">AÇ</button>
    </div>
  </div>

  <div class="bottom">1WIN</div>

  <!-- Sinyal Popup -->
  <div id="signalPopup">
    <h2 id="signalTitle">Yeni Sinyal!</h2>
    <p id="signalText">Tahmin: 🔵 Mavi • 4. sıra • 3.2x 🍀</p>
    <button onclick="closeSignal()">Kapat</button>
  </div>

  <script>
    function toggleMenu() {
      const menu = document.getElementById('menu');
      menu.style.display = menu.style.display === 'block' ? 'none' : 'block';
    }

    function changeLang(lang) {
      alert('Dil değiştirildi: ' + lang.toUpperCase() + ' (gerçek dil desteği için JS genişletebilirsin)');
      toggleMenu();
    }

    const signals = [
      '🔵 Mavi • 3. sıra • 2.5x – Kazanma yüksek!',
      '💣 Bomba • 8. sıra – Kaçın!',
      '🟢 Yeşil • 6. sıra • 4.1x',
      '🔴 Kırmızı • 10. sıra • 1.8x'
    ];

    function getSignal() {
      const random = signals[Math.floor(Math.random() * signals.length)];
      document.getElementById('signalText').innerText = random;
      document.getElementById('signalPopup').style.display = 'block';
      toggleMenu();
    }

    function closeSignal() {
      document.getElementById('signalPopup').style.display = 'none';
    }

    // Telegram Mini App entegrasyonu
    if (window.Telegram && window.Telegram.WebApp) {
      Telegram.WebApp.ready();
      Telegram.WebApp.expand();
      Telegram.WebApp.setBackgroundColor('#0d0d0d');
    }
  </script>
</body>
</html>
