<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">

  <title>Клеточная лаборатория</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #10131a;
      color: white;
      text-align: center;
    }

    header {
      padding: 25px 15px;
      background: #171c27;
      border-bottom: 1px solid #303747;
    }

    h1 {
      margin: 0;
      font-size: 32px;
    }

    .version {
      margin-top: 8px;
      color: #8f9bad;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 10px;
      padding: 15px;
      flex-wrap: wrap;
    }

    button {
      border: 0;
      border-radius: 12px;
      padding: 12px 20px;
      background: #2979ff;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background: #1565d8;
    }

    .page {
      display: none;
      padding: 25px 15px;
    }

    .page.active {
      display: block;
    }

    .welcome {
      margin: 30px auto;
      max-width: 700px;
      padding: 30px;
      background: #171c27;
      border-radius: 20px;
    }

    .game {
      width: 100%;
      min-height: 500px;
      background: #05070b;
      border-radius: 15px;
      overflow: hidden;
    }

    .update {
      max-width: 700px;
      margin: 15px auto;
      padding: 20px;
      background: #171c27;
      border-radius: 15px;
      text-align: left;
    }

    footer {
      margin-top: 50px;
      padding: 20px;
      color: #777;
    }
  </style>
</head>

<body>

  <header>
    <h1>Клеточная лаборатория</h1>
    <div class="version">Версия 0.1</div>
  </header>

  <nav>
    <button onclick="showPage('home')">🏠 Главная</button>
    <button onclick="showPage('game')">🎮 Играть</button>
    <button onclick="showPage('updates')">🆕 Обновления</button>
  </nav>

  <!-- ГЛАВНАЯ -->
  <section id="home" class="page active">
    <div class="welcome">
      <h2>Добро пожаловать!</h2>

      <p>
        Добро пожаловать в «Клеточную лабораторию»!
      </p>

      <button onclick="showPage('game')">
        🎮 Играть
      </button>
    </div>
  </section>

  <!-- ИГРА -->
  <section id="game" class="page">

    <h2>🎮 Игра</h2>

    <div class="game">

      <!-- СЮДА ВСТАВЬ КОД ИГРЫ -->

    </div>

  </section>

  <!-- ОБНОВЛЕНИЯ -->
  <section id="updates" class="page">

    <h2>🆕 Обновления</h2>

    <div class="update">
      <h3>Версия 0.1</h3>
      <p>🎉 Первый запуск сайта!</p>
      <p>Добавлена первая версия «Клеточной лаборатории».</p>
    </div>

  </section>

  <footer>
    © 2026 Клеточная лаборатория
  </footer>

  <script>
    function showPage(page) {

      document.querySelectorAll('.page').forEach(function(element) {
        element.classList.remove('active');
      });

      document.getElementById(page).classList.add('active');

      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    }
  </script>

</body>
</html>