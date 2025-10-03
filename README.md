<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Task Management Tracker Surprice</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #f4f6f9; }
    header { background: #2c3e50; color: white; padding: 15px; text-align: center; font-size: 22px; }
    .sidebar {
      width: 220px; background: #34495e; position: fixed; top: 0; bottom: 0; left: 0; padding-top: 60px;
    }
    .sidebar a { display: block; color: white; padding: 12px; text-decoration: none; }
    .sidebar a:hover { background: #1abc9c; }
    .main { margin-left: 240px; padding: 20px; }
    .report-link { background: #ecf0f1; margin: 8px 0; padding: 10px; border-radius: 6px; }
    footer { margin-top: 30px; text-align: center; font-size: 12px; color: gray; }
    .topbar { display: flex; justify-content: space-between; align-items: center; }
    img.logo { height: 40px; margin: 10px; }
    .logo-section { margin: 20px 0; text-align:center; }
  </style>
</head>
<body>
  <header>📊 Task Management Tracker Operasional Surprice</header>

  <!-- DASHBOARD langsung tampil -->
  <div id="dashboard">
    <div class="sidebar">
      <a href="#" onclick="showReports('Gudang')">Gudang</a>
      <a href="#" onclick="showReports('cs')">Customer Service</a>
      <a href="#" onclick="showReports('marketing')">Marketing</a>
      <a href="#" onclick="showReports('driver')">Driver</a>
      <a href="#" onclick="showReports('finance')">Finance</a>
      <a href="#" onclick="secureOperasional()">Kepala Operasional</a>
      <a href="#" onclick="showReports('admin')">Admin</a>
      <a href="#" onclick="openChat()">💬 Chat</a>
    </div>

    <div class="main">
      <div id="motivasi"></div>
      <div class="topbar">
        <h2 id="welcome">Selamat Datang di Dashboard</h2>
      </div>

      <!-- Logo Marketplace -->
      <div class="logo-section">
        <h3>Marketplace</h3>
        <img src="https://upload.wikimedia.org/wikipedia/commons/1/1f/Shopee_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/08/TikTok_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/50/Lazada_%28Thailand%29_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/2/20/Blibli_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/9/9e/Tokopedia.svg" class="logo">
      </div>

      <!-- Logo Kurir -->
      <div class="logo-section">
        <h3>Partner Kurir</h3>
        <img src="https://upload.wikimedia.org/wikipedia/commons/1/1f/J%26T_Express_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/09/JNE_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d8/Ninja_Van_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/5c/Grab_logo.svg" class="logo">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Gojek_logo_2020.svg" class="logo">
        <img src="https://seeklogo.com/images/S/spx-express-logo-52DCBDF622-seeklogo.com.png" class="logo">
      </div>

      <h3 id="menu-title">Pilih Menu</h3>
      <div id="report-list"></div>
      <footer>© Sendi_Muchdianto</footer>
    </div>
  </div>

  <script>
    // langsung tampil motivasi saat halaman dibuka
    const motivasiList = [
      "💡 Tetap semangat tim! Fokus hari ini = hasil besar esok 🌟",
      "🚀 Kerja keras mengalahkan bakat ketika bakat tidak bekerja keras!",
      "🔥 Jangan menunda pekerjaan, sukses diraih bersama!",
      "🌱 Konsistensi kecil setiap hari membuahkan hasil besar!"
    ];
    function tampilkanMotivasi(){
      const rand = motivasiList[Math.floor(Math.random() * motivasiList.length)];
      document.getElementById("motivasi").innerHTML = `<marquee>${rand}</marquee>`;
    }
    tampilkanMotivasi();
  </script>
</body>
</html>
