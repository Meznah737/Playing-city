# Playing-city
Playing
<!DOCTYPE html><html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>play23y - عالم الألعاب</title>
  <style>
    body {
      margin: 0;
      font-family: 'Tahoma', sans-serif;
      background: #fef6e4;
      color: #333;
    }
    header {
      background-color: #ff9b85;
      padding: 1rem;
      text-align: center;
      color: white;
      font-size: 2rem;
      font-weight: bold;
    }
    nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      background-color: #ffc8dd;
    }
    nav a {
      padding: 1rem;
      color: #333;
      text-decoration: none;
      font-weight: bold;
    }
    nav a:hover {
      color: #ff5c8a;
    }
    .search-bar {
      display: flex;
      justify-content: center;
      margin: 1rem auto;
    }
    .search-bar input {
      width: 60%;
      padding: 0.5rem;
      border-radius: 2rem;
      border: 2px solid #ff9b85;
      font-size: 1rem;
      text-align: right;
    }
    .game-section {
      padding: 2rem;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1.5rem;
    }
    .game-card {
      background: #fff0f5;
      border-radius: 1rem;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      padding: 1rem;
      text-align: center;
      transition: transform 0.2s ease;
    }
    .game-card:hover {
      transform: scale(1.05);
    }
    .game-card img {
      width: 100%;
      border-radius: 1rem;
    }
    .game-card a {
      display: inline-block;
      margin-top: 0.5rem;
      padding: 0.5rem 1rem;
      background-color: #ff9b85;
      color: white;
      border-radius: 1rem;
      text-decoration: none;
      font-weight: bold;
    }
    .game-card a:hover {
      background-color: #ff5c8a;
    }
    footer {
      background-color: #cdb4db;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header>play23y - عالم الألعاب</header>
  <nav>
    <a href="#education">تعليمية</a>
    <a href="#cooking">طبخ</a>
    <a href="#drawing">رسم</a>
    <a href="#simulation">محاكاة</a>
    <a href="#racing">سباقات</a>
    <a href="#fun">ترفيه</a>
  </nav>  <div class="search-bar">
    <input type="text" id="searchInput" placeholder="ابحث عن لعبة..." onkeyup="searchGames()">
  </div>  <section id="education" class="game-section">
    <div class="game-card">
      <img src="images/math-game.jpg" alt="لعبة الأرقام">
      <h3>لعبة الأرقام</h3>
      <a href="games/math.html">العب الآن</a>
    </div>
    <div class="game-card">
      <img src="images/letters-game.jpg" alt="لعبة الحروف">
      <h3>لعبة الحروف</h3>
      <a href="games/letters.html">العب الآن</a>
    </div>
  </section>  <section id="cooking" class="game-section">
    <div class="game-card">
      <img src="images/cake.jpg" alt="طبخ الكيك">
      <h3>طبخ الكيك</h3>
      <a href="games/cake.html">العب الآن</a>
    </div>
    <div class="game-card">
      <img src="images/pizza.jpg" alt="طبخ البيتزا">
      <h3>طبخ البيتزا</h3>
      <a href="games/pizza.html">العب الآن</a>
    </div>
  </section>  <section id="drawing" class="game-section">
    <div class="game-card">
      <img src="images/draw1.jpg" alt="ارسم وتعلم">
      <h3>ارسم وتعلم</h3>
      <a href="games/draw1.html">العب الآن</a>
    </div>
  </section>  <!-- يمكنك تكرار الباقي بنفس الشكل للفئات الأخرى -->  <footer>
    &copy; 2025 play23y - جميع الحقوق محفوظة
  </footer>  <script>
    function searchGames() {
      const input = document.getElementById('searchInput').value.toLowerCase();
      const cards = document.querySelectorAll('.game-card');

      cards.forEach(card => {
        const title = card.querySelector('h3').innerText.toLowerCase();
        if (title.includes(input)) {
          card.style.display = '';
        } else {
          card.style.display = 'none';
        }
      });
    }
  </script></body>
</html>
