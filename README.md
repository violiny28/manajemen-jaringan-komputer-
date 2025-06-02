<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Kelompok MJK</title>
  <link href="https://fonts.googleapis.com/css2?family=Baloo+2&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #89f7fe, #66a6ff);
      font-family: 'Baloo 2', cursive;
      color: #fff;
      text-align: center;
      overflow-x: hidden;
    }

    h1 {
      font-size: 3em;
      margin-top: 60px;
      animation: fadeDown 1s ease-out;
    }

    h2 {
      font-size: 2em;
      margin-bottom: 30px;
      animation: fadeDown 1.5s ease-out;
    }

    .anggota-container {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 30px;
      margin-top: 40px;
    }

    .anggota {
      background: #ffffff33;
      border-radius: 25px;
      padding: 20px;
      width: 220px;
      cursor: pointer;
      transition: transform 0.3s ease, background 0.3s ease;
      box-shadow: 0 12px 24px rgba(0, 0, 0, 0.2);
      animation: bounceIn 1.5s ease;
      position: relative;
    }

    .anggota:hover {
      transform: translateY(-10px) scale(1.05);
      background: #ffffff55;
    }

    .anggota strong {
      font-size: 1.4em;
      display: block;
      margin-bottom: 10px;
    }

    .nbi {
      font-size: 1.1em;
      color: #222;
      background: #fff;
      padding: 8px 12px;
      border-radius: 12px;
      display: none;
      margin-top: 10px;
      animation: fadeIn 0.5s ease-in-out forwards;
    }

    @keyframes fadeDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes bounceIn {
      0% {
        transform: scale(0.5);
        opacity: 0;
      }
      60% {
        transform: scale(1.2);
        opacity: 1;
      }
      100% {
        transform: scale(1);
      }
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(10px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <h1>Selamat Datang</h1>
  <h2>Manajemen Jaringan Komputer</h2>

  <div class="anggota-container">
    <div class="anggota" onclick="toggleNBI('nbi1')">
      <strong>Andi Pratama</strong>
      <div class="nbi" id="nbi1">1462300101</div>
    </div>
    <div class="anggota" onclick="toggleNBI('nbi2')">
      <strong>Budi Santoso</strong>
      <div class="nbi" id="nbi2">1462300102</div>
    </div>
    <div class="anggota" onclick="toggleNBI('nbi3')">
      <strong>Citra Lestari</strong>
      <div class="nbi" id="nbi3">1462300103</div>
    </div>
  </div>

  <script>
    function toggleNBI(id) {
      const el = document.getElementById(id);
      if (el.style.display === 'block') {
        el.style.display = 'none';
      } else {
        el.style.display = 'block';
        el.style.animation = 'fadeIn 0.5s ease-in-out';
      }
    }
  </script>

</body>
</html>
