<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>MARIA IZABELLA</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --black: #111111;
      --white: #fffdfb;
      --cream: #f5eee7;
      --pink: #ead1d5;
      --gold: #b6945f;
      --gray: #77716e;
      --border: #d8ccc2;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--white);
      color: var(--black);
      font-family: 'Montserrat', sans-serif;
      line-height: 1.6;
    }

    /* Шапка */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(255, 253, 251, 0.96);
      border-bottom: 1px solid var(--border);
      z-index: 1000;
    }

    .header-inner {
      max-width: 1200px;
      margin: 0 auto;
      min-height: 80px;
      padding: 15px 25px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      color: var(--black);
      text-decoration: none;
      font-family: 'Playfair Display', serif;
      font-size: 24px;
      font-weight: 700;
      letter-spacing: 5px;
      white-space: nowrap;
    }

    nav ul {
      display: flex;
      gap: 22px;
      list-style: none;
      flex-wrap: wrap;
      justify-content: center;
    }

    nav a {
      color: var(--black);
      text-decoration: none;
      font-size: 12px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: color 0.3s ease;
    }

    nav a:hover {
      color: var(--gold);
    }

    /* Общие стили */

    section {
      max-width: 1200px;
      min-height: 90vh;
      margin: 0 auto;
      padding: 140px 25px 90px;
    }

    .section-label {
      margin-bottom: 12px;
      color: var(--gold);
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 3px;
    }

    .section-title {
      margin-bottom: 18px;
      font-family: 'Playfair Display', serif;
      font-size: clamp(42px, 7vw, 90px);
      font-weight: 500;
      line-height: 1;
    }

    .section-subtitle {
      max-width: 600px;
      margin-bottom: 45px;
      color: var(--gray);
      font-size: 15px;
    }

    .line {
      width: 100%;
      height: 1px;
      margin: 30px 0;
      background: var(--border);
    }

    /* Главный экран */

    #home {
      max-width: none;
      padding: 150px 6vw 90px;
      background:
        linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.38)),
        url("фото/заствака.jpg")
        center/cover;
      color: white;
      display: flex;
      align-items: flex-end;
    }

    .hero-content {
      max-width: 850px;
    }

    .hero-label {
      margin-bottom: 25px;
      color: #f3d69d;
      font-size: 13px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 4px;
    }

    .hero-title {
      margin-bottom: 20px;
      font-family: 'Playfair Display', serif;
      font-size: clamp(62px, 12vw, 170px);
      font-weight: 500;
      line-height: 0.9;
      letter-spacing: -5px;
    }

    .hero-text {
      max-width: 580px;
      margin-bottom: 35px;
      font-size: 16px;
    }

    .hero-button,
    .dark-button {
      display: inline-block;
      padding: 14px 24px;
      border: 1px solid white;
      color: white;
      text-decoration: none;
      font-size: 12px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      transition: 0.3s ease;
    }

    .hero-button:hover {
      background: white;
      color: var(--black);
    }

    /* Фотография */

    .photo-section {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .main-photo {
      width: 100%;
      height: 580px;
      object-fit: cover;
      filter: grayscale(15%);
    }

    .article-text {
      color: var(--gray);
      font-size: 16px;
    }

    .article-text p {
      margin-bottom: 20px;
    }

    .quote {
      margin: 30px 0;
      padding-left: 22px;
      border-left: 3px solid var(--gold);
      color: var(--black);
      font-family: 'Playfair Display', serif;
      font-size: 27px;
      font-style: italic;
      line-height: 1.25;
    }

    /* Факты */

    .facts-section {
      background: var(--cream);
    }

    .facts-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .fact-card {
      min-height: 210px;
      padding: 28px;
      border: 1px solid var(--border);
      background: rgba(255, 255, 255, 0.45);
    }

    .fact-number {
      margin-bottom: 45px;
      color: var(--gold);
      font-family: 'Playfair Display', serif;
      font-size: 34px;
    }

    .fact-card h3 {
      margin-bottom: 10px;
      font-family: 'Playfair Display', serif;
      font-size: 25px;
      font-weight: 500;
    }

    .fact-card p {
      color: var(--gray);
      font-size: 14px;
    }

    /* Воспоминания */

    .memories-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 20px;
    }

    .memories-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    .memory-button {
      min-height: 180px;
      padding: 20px;
      border: 1px solid var(--border);
      background: var(--white);
      text-align: left;
      cursor: pointer;
      transition: 0.3s ease;
    }

    .memory-button:hover {
      background: var(--pink);
      transform: translateY(-5px);
    }

    .memory-number {
      display: block;
      margin-bottom: 55px;
      color: var(--gold);
      font-family: 'Playfair Display', serif;
      font-size: 25px;
    }

    .memory-button strong {
      display: block;
      font-family: 'Playfair Display', serif;
      font-size: 20px;
      font-weight: 500;
    }

    .memory-card {
      display: none;
      margin-top: 22px;
      padding: 28px;
      border: 1px solid var(--border);
      background: var(--cream);
      animation: showCard 0.35s ease;
    }

    .memory-card.active {
      display: block;
    }

    @keyframes showCard {
      from {
        opacity: 0;
        transform: translateY(10px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .memory-card h3 {
      margin-bottom: 10px;
      font-family: 'Playfair Display', serif;
      font-size: 30px;
      font-weight: 500;
    }

    .memory-card p {
      max-width: 750px;
      color: var(--gray);
    }

    /* Поздравление */

    #final {
      max-width: none;
      background: var(--black);
      color: white;
      text-align: center;
    }

    .final-content {
      max-width: 850px;
      margin: 0 auto;
    }

    .final-title {
      margin-bottom: 30px;
      font-family: 'Playfair Display', serif;
      font-size: clamp(48px, 8vw, 100px);
      font-weight: 500;
      line-height: 1;
    }

    .final-text {
      margin-bottom: 25px;
      color: #dddddd;
      font-size: 17px;
    }

    .signature {
      margin-top: 35px;
      color: #f3d69d;
      font-family: 'Playfair Display', serif;
      font-size: 32px;
      font-style: italic;
    }

    footer {
      padding: 25px;
      background: var(--black);
      border-top: 1px solid #333;
      color: #999;
      text-align: center;
      font-size: 12px;
    }

    /* Адаптация для телефона */

    @media (max-width: 800px) {
      .header-inner {
        min-height: auto;
        flex-direction: column;
      }

      nav ul {
        gap: 10px;
      }

      nav a {
        font-size: 10px;
      }

      section {
        padding: 120px 18px 65px;
      }

      .photo-section {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .main-photo {
        height: 400px;
      }

      .facts-grid {
        grid-template-columns: 1fr;
      }

      .memories-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .memories-header {
        display: block;
      }

      .hero-title {
        letter-spacing: -2px;
      }
    }

    @media (max-width: 480px) {
      .memories-grid {
        grid-template-columns: 1fr 1fr;
      }

      .memory-button {
        min-height: 145px;
        padding: 14px;
      }

      .memory-number {
        margin-bottom: 35px;
      }

      .memory-button strong {
        font-size: 17px;
      }
    }
  </style>
</head>

<body>

  <!-- ШАПКА С 4 ССЫЛКАМИ -->
  <header>
    <div class="header-inner">
      <a href="#home" class="logo">MARIA IZABELLA</a>

      <nav>
        <ul>
          <li><a href="#about">О ней</a></li>
          <li><a href="#facts">Факты</a></li>
          <li><a href="#memories">Воспоминания</a></li>
          <li><a href="#final">Поздравление</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- ГЛАВНАЯ -->
  <section id="home">
    <div class="hero-content">
      <div class="hero-label">Special birthday issue · 2026</div>

      <h1 class="hero-title">MARIA</h1>

      <p class="hero-text">
        «Мария Музалевская — та самая, рядом с которой даже обычные дни становятся особенными. В ней столько света, стиля и внутренней силы, что хочется ловить каждый момент и проживать его ярче. Она не просто следует трендам — она доказывает, что быть собой это и есть тренд»
      </p>

      <a href="#about" class="hero-button">Читать выпуск</a>
    </div>
  </section>

  <!-- О НЕЙ -->
  <section id="about" class="photo-section">
    <div>
      <!-- Здесь можно заменить ссылку на фотографию подруги -->
      <img
        class="main-photo"
        src="фото/очки.jpg"
        alt="Фотография"
      >
    </div>

    <div>
      <div class="section-label">Cover story</div>

      <h2 class="section-title">Главная героиня</h2>

      <div class="article-text">
        <p>
          Маша — человек с потрясающей внутренней эстетикой и невероятной харизмой. Она умеет находить красоту в самых простых вещах: в закатном солнце, вкусе любимого кофе или случайных моментах. С ней всегда тепло, легко и по-настоящему уютно, а её улыбка способна осветить даже самый серый и пасмурный день.
        </p>

        <div class="quote">
          «Дружба с ней — это когда одно слово заменяет часовой разговор».
        </div>

        <p>
          С ней невозможно соскучиться: прогулки превращаются в фотосессии, а любые разговоры затягиваются допоздна. Этот спецвыпуск — напоминание о том, насколько она крутая, уникальная и любимая!
        </p>
      </div>
    </div>
  </section>

  <!-- ФАКТЫ О НЕЙ -->
  <section id="facts" class="facts-section">
    <div class="section-label">Personal file</div>

    <h2 class="section-title">Факты о ней</h2>

    <p class="section-subtitle">
      Маленькие детали, из которых складывается её большая и прекрасная история.
    </p>

    <div class="facts-grid">
      <div class="fact-card">
        <div class="fact-number">01</div>
        <h3>Её талант</h3>
        <p>Маша потрясающе танцует! Когда она в движении, кажется, что музыка буквально оживает вместе с ней. Для неё танец — это не просто хобби, а способ выразить свои эмоции, показать свою невероятную грацию, пластику и свободу. Она способна зажечь своей энергией любой танцпол!</p>
        <img
        class="main-photo"
        src="фото/танцы.jpg"
        alt="Фотография">
      </div>

      <div class="fact-card">
        <div class="fact-number">02</div>
        <h3>Её стиль</h3>
        <p>Утончённый, эстетичный и всегда безупречный. Маша умеет круто сочетать элегантные вещи с расслабленным оверсайзом, дополняя образы красивыми деталями. Её стиль — это отражение её характера: лёгкий, уверенный и запоминающийся с первого взгляда.</p>
        <img
        class="main-photo"
        src="фото/океан.jpg"
        alt="Фотография">
      </div>

      <div class="fact-card">
        <div class="fact-number">03</div>
        <h3>Её мечта</h3>
        <p>
          Её главная цель — успешно сдать экзамены и сделать первый серьезный шаг на пути к медицине. Это не просто оценка в аттестате, это билет в профессию.
          Маша понимает, что за этим стоит большой труд, но её упорство и светлая голова обязательно помогут ей справиться.</p>
          <img
        class="main-photo"
        src="фото/зима.jpg"
        alt="Фотография">
      </div>
    </div>
  </section>

  <!-- ВОСПОМИНАНИЯ -->
  <section id="memories">
    <div class="memories-header">
      <div>
        <div class="section-label">The archive</div>
        <h2 class="section-title">Воспоминания</h2>
      </div>

      <p class="section-subtitle">
        Нажми на любое маленькое окошко, чтобы открыть воспоминание.
      </p>
    </div>

    <div class="line"></div>

    <div class="memories-grid">
      <button class="memory-button" onclick="openMemory('memory1')">
        <span class="memory-number">01</span>
        <strong>Все началось с...</strong>
      </button>

      <button class="memory-button" onclick="openMemory('memory2')">
        <span class="memory-number">02</span>
        <strong>Наши маленькие традиции</strong>
      </button>

      <button class="memory-button" onclick="openMemory('memory3')">
        <span class="memory-number">03</span>
        <strong>Ты всегда рядом</strong>
      </button>

      <button class="memory-button" onclick="openMemory('memory4')">
        <span class="memory-number">04</span>
        <strong>Спасибо за все</strong>
      </button>
    </div>

    <div id="memory1" class="memory-card">
      <h3>Все началось с...</h3>
      <p>
        «Все началось с обычных тренировок на танцах. Нам было всего по четыре года, мы были совсем крохами, но судьба уже тогда свела нас вместе. Мы сразу нашли друг в друге что-то родное и с тех самых пор идём по жизни рука об руку.»
      </p>
      <img
        class="main-photo"
        src="фото/детство.jpg"
        alt="Фотография">
    </div>

    <div id="memory2" class="memory-card">
      <h3>Наши маленькие традиции</h3>
      <p>
        «Наши часовые разговоры по телефону — это святое. Мы можем болтать обо всём на свете, но самые важные моменты — это разговоры по душам. Мы делимся друг с другом проблемами, переживаниями и секретами, и после каждого такого разговора становится легче.» 
      </p>
      <img
        class="main-photo"
        src="фото/разговоры.jpg"
        alt="Фотография">
    </div>

    <div id="memory3" class="memory-card">
      <h3>Ты всегда рядом</h3>
      <p>
        «Ты — тот человек, на которого можно положиться в любой ситуации. Если мне захочется просто пойти погулять, ты всегда составишь компанию. А если нужно что-то сделать или оплатить — ты без лишних слов придёшь на помощь. С тобой никогда не бывает одиноко.»
      </p>
      <img class="main-photo"
        src="фото/доверие.jpg" width="500" height="800"
        alt="Фотография">
    </div>

    <div id="memory4" class="memory-card">
      <h3>Спасибо за всё</h3>
      <p>
        «Спасибо тебе за то, что ты есть. За твою поддержку, за твоё терпение и за то, что ты всегда выслушаешь. Ты — не просто подруга, ты — родной человек. Я очень ценю всё, что ты для меня делаешь, и очень рада, что мы прошли этот путь вместе.»
      </p>
      <img
        class="main-photo"
        src="фото/прогулка.jpg"
        alt="Фотография">
    </div>
  </section>

  <!-- ФИНАЛЬНОЕ ПОЗДРАВЛЕНИЕ -->
  <section id="final">
    <div class="final-content">
      <div class="section-label">Final page</div>

      <h2 class="final-title">С днём рождения!</h2>

      <p class="final-text">
      С днём рождения, моя родная! Ты — тот человек, с которым я могу быть собой на 100%. Желаю тебе, чтобы твоя жизнь была такой же яркой, как твоя улыбка, а каждый день приносил только радость. Пусть все твои самые смелые желания обязательно сбудутся!
      </p>

      <p class="final-text">
        Спасибо тебе за то, что ты всегда рядом: и в горе, и в радости. За нашу дружбу, за смех до слёз и за все наши безумные идеи. Пусть этот год будет самым счастливым и щедрым на события. Я тебя очень люблю!
      </p>

      <div class="signature">
        С любовью, Катя ❤️
      </div>
    </div>
  </section>

  <footer>
    MARIA IZABELLA · Made with love
  </footer>

  <script>
    function openMemory(id) {
      const cards = document.querySelectorAll('.memory-card');

      cards.forEach(function(card) {
        card.classList.remove('active');
      });

      const selectedCard = document.getElementById(id);
      selectedCard.classList.add('active');

      selectedCard.scrollIntoView({
        behavior: 'smooth',
        block: 'center'
      });
    }
  </script>

</body>
</html>
