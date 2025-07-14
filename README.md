# Setelah reset, kita buat ulang file HTML ucapan ulang tahun dengan emoji 🎂 dan confetti 🎉

html_content = """
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>🎂 Selamat Ulang Tahun!</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffdee9, #b5fffc);
      overflow-x: hidden;
      text-align: center;
      color: #c2185b;
    }
    h1 {
      margin-top: 60px;
      font-size: 2.8em;
      animation: pop 1s ease;
    }
    @keyframes pop {
      0% { transform: scale(0.5); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }
    .cake {
      font-size: 5em;
      animation: bounce 1.5s infinite;
      margin: 20px 0;
    }
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }
    .note {
      background: #fff8fc;
      padding: 30px;
      margin: 30px auto;
      border-radius: 12px;
      max-width: 600px;
      box-shadow: 0 0 10px rgba(255, 192, 203, 0.4);
    }
    .confetti {
      position: fixed;
      top: -10px;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: pink;
      animation: fall 6s linear infinite;
      z-index: 100;
    }
    @keyframes fall {
      0% { transform: translateY(0); opacity: 1; }
      100% { transform: translateY(100vh); opacity: 0; }
    }
    footer {
      margin-top: 40px;
      font-size: 0.9em;
      color: #888;
    }
  </style>
</head>
<body>
  <h1>🎉 Selamat Ulang Tahun, Sulfiyatun! 🎉</h1>
  <div class="cake">🎂</div>
  <div class="note">
    <p>Hari ini bukan cuma tentang ulang tahunmu...</p>
    <p>...tapi tentang betapa berartinya kamu bagi orang-orang di sekitarmu ❤️</p>
    <p>Semoga harimu dipenuhi tawa, cinta, dan kue yang banyak 🍰</p>
    <p>Dan semoga semua mimpimu perlahan jadi nyata 💫</p>
    <p><strong>— Dari seseorang yang selalu doain bahagiamu 💖</strong></p>
  </div>

  <footer>Ditulis khusus buatmu... karena kamu spesial 🎁</footer>

  <script>
    for (let i = 0; i < 40; i++) {
      const confetti = document.createElement('div');
      confetti.className = 'confetti';
      confetti.style.left = Math.random() * 100 + "vw";
      confetti.style.backgroundColor = ['#ff5e8e', '#ffd700', '#87cefa'][Math.floor(Math.random()*3)];
      confetti.style.animationDelay = Math.random() * 5 + "s";
      document.body.appendChild(confetti);
    }
  </script>
</body>
</html>
"""

# Simpan sebagai file HTML
file_path = "/mnt/data/selamat-ulang-tahun.html"
with open(file_path, "w", encoding="utf-8") as f:
    f.write(html_content)

file_path
