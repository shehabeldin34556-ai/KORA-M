
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>KORA M</title>

  <style>
    * {
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      margin: 0;
      background: #0b0d10;
      color: white;
    }

    .app {
      max-width: 430px;
      margin: auto;
      min-height: 100vh;
      background: #11151a;
      padding-bottom: 75px;
    }

    header {
      padding: 25px 18px;
      background: #171b20;
      border-bottom: 1px solid #292f36;
    }

    .logo {
      font-size: 32px;
      font-weight: 900;
    }

    .logo span {
      color: #e31b23;
    }

    .subtitle {
      color: #9da4ad;
      margin-top: 5px;
      font-size: 13px;
    }

    main {
      padding: 16px;
    }

    .hero {
      background: #e31b23;
      border-radius: 18px;
      padding: 20px;
      margin-bottom: 16px;
    }

    .hero h2 {
      margin-top: 0;
    }

    .hero p {
      color: #ffe7e7;
    }

    .grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }

    .card {
      background: #1a2027;
      border: 1px solid #292f36;
      border-radius: 16px;
      padding: 17px;
      min-height: 125px;
      cursor: pointer;
    }

    .card:hover {
      transform: scale(1.02);
    }

    .icon {
      font-size: 28px;
    }

    .card h3 {
      margin: 8px 0 5px;
    }

    .card p {
      margin: 0;
      color: #9da4ad;
      font-size: 12px;
    }

    section {
      display: none;
    }

    section.active {
      display: block;
    }

    .list {
      background: #1a2027;
      border: 1px solid #292f36;
      border-radius: 15px;
      padding: 15px;
      margin: 10px 0;
    }

    .row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
    }

    .note {
      color: #9da4ad;
      font-size: 13px;
      line-height: 1.6;
    }

    button {
      border: 0;
      border-radius: 11px;
      padding: 11px 15px;
      background: #e31b23;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }

    button.secondary {
      background: #292f36;
    }

    .back {
      margin-bottom: 12px;
      background: #292f36;
    }

    .big-number {
      font-size: 45px;
      text-align: center;
      font-weight: bold;
    }

    nav {
      position: fixed;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: min(430px, 100%);
      background: #171b20;
      border-top: 1px solid #292f36;
      display: flex;
      justify-content: space-around;
      padding: 8px 3px;
      z-index: 10;
    }

    nav button {
      background: transparent;
      color: #b8bec6;
      padding: 7px;
      font-size: 11px;
    }

    .player {
      text-align: center;
      padding: 20px;
      background: #20262d;
      border-radius: 15px;
      margin: 12px 0;
    }

    .player-name {
      font-size: 23px;
      font-weight: bold;
    }

    .bid {
      font-size: 25px;
      margin: 12px;
    }
  </style>
</head>

<body>

<div class="app">

  <header>
    <div class="logo">KORA <span>M</span></div>
    <div class="subtitle">كرة القدم • أخبار • مباريات • ألعاب</div>
  </header>

  <main>

    <!-- الرئيسية -->
    <section id="home" class="active">

      <div class="hero">
        <h2>أهلاً بك في KORA M ⚽</h2>
        <p>
          كل أخبار كرة القدم وأهم المباريات وألعاب التحدي في مكان واحد.
        </p>
      </div>

      <div class="grid">

        <div class="card" onclick="show('games')">
          <div class="icon">🎮</div>
          <h3>الألعاب</h3>
          <p>العب وتحدى أصدقاءك</p>
        </div>

        <div class="card" onclick="show('matches')">
          <div class="icon">⚽</div>
          <h3>المباريات</h3>
          <p>مصر وإنجلترا والعالم</p>
        </div>

        <div class="card" onclick="show('news')">
          <div class="icon">📰</div>
          <h3>أهم الأخبار</h3>
          <p>آخر أخبار كرة القدم</p>
        </div>

        <div class="card" onclick="show('info')">
          <div class="icon">📚</div>
          <h3>معلومات</h3>
          <p>لاعبون وفرق وبطولات</p>
        </div>

      </div>

    </section>


    <!-- الألعاب -->
    <section id="games">

      <button class="back" onclick="show('home')">
        ← الرئيسية
      </button>

      <h2>🎮 الألعاب</h2>

      <div class="list">
        <div class="row">
          <b>🔨 المزاد</b>
          <button onclick="startAuction(11,250)">
            العب
          </button>
        </div>

        <p class="note">
          11 لاعب + مدرب • الميزانية 250 مليون يورو •
          20 ثانية لكل مزايدة
        </p>
      </div>


      <div class="list">
        <div class="row">
          <b>💎 المزاد الكبير</b>
          <button onclick="startAuction(18,1500)">
            العب
          </button>
        </div>

        <p class="note">
          18 لاعب + مدرب • الميزانية 1.5 مليار يورو
        </p>
      </div>


      <div class="list">
        <div class="row">
          <b>⏱️ التحدي الثلاثين</b>
          <button onclick="challenge30()">
            العب
          </button>
        </div>

        <p class="note">
          30 ثانية • من 2 إلى 6 لاعبين • إجابات صوتية في النسخة الكاملة
        </p>
      </div>


      <div class="list">
        <div class="row">
          <b>🧠 مين اللاعب؟</b>
          <button onclick="guessPlayer()">
            العب
          </button>
        </div>

        <p class="note">
          خمن اللاعب من خلال التلميحات
        </p>
      </div>

    </section>


    <!-- المباريات -->
    <section id="matches">

      <button class="back" onclick="show('home')">
        ← الرئيسية
      </button>

      <h2>⚽ المباريات</h2>

      <div class="list">
        <h3>🇪🇬 الدوري المصري</h3>
        <p class="note">
          المباريات والنتائج ستتصل لاحقًا بمصدر بيانات مباشر.
        </p>
      </div>

      <div class="list">
        <h3>🏴 الدوري الإنجليزي</h3>
        <p class="note">
          المباريات والنتائج ستتصل لاحقًا بمصدر بيانات مباشر.
        </p>
      </div>

    </section>


    <!-- الأخبار -->
    <section id="news">

      <button class="back" onclick="show('home')">
        ← الرئيسية
      </button>

      <h2>📰 أهم الأخبار</h2>

      <div class="list">
        <h3>🔥 أخبار كرة القدم</h3>
        <p class="note">
          في النسخة الحقيقية سيتم جلب الأخبار الجديدة تلقائيًا من مصدر موثوق.
        </p>
      </div>

      <div class="list">
        <h3>🔄 سوق الانتقالات</h3>
        <p class="note">
          أخبار انتقالات اللاعبين والصفقات.
        </p>
      </div>

    </section>


    <!-- المعلومات -->
    <section id="info">

      <button class="back" onclick="show('home')">
        ← الرئيسية
      </button>

      <h2>📚 معلومات كرة القدم</h2>

      <div class="list">
        <h3>👤 اللاعبون</h3>
        <p class="note">
          معلومات وإحصائيات اللاعبين.
        </p>
      </div>

      <div class="list">
        <h3>🏆 البطولات</h3>
        <p class="note">
          البطولات والنتائج والترتيب والهدافون.
        </p>
      </div>

    </section>


    <!-- الحساب -->
    <section id="profile">

      <button class="back" onclick="show('home')">
        ← الرئيسية
      </button>

      <h2>👤 حسابي</h2>

      <div class="list">
        <div class="row">
          <span>النقاط</span>
          <b id="points">0</b>
        </div>
      </div>

      <div class="list">
        <div class="row">
          <span>المستوى</span>
          <b>مبتدئ</b>
        </div>
      </div>

    </section>


    <!-- شاشة اللعبة -->
    <section id="game">

      <button class="back" onclick="show('games')">
        ← الألعاب
      </button>

      <div id="gameContent"></div>

    </section>

  </main>


  <!-- القائمة السفلية -->
  <nav>

    <button onclick="show('home')">
      🏠<br>الرئيسية
    </button>

    <button onclick="show('games')">
      🎮<br>الألعاب
    </button>

    <button onclick="show('matches')">
      ⚽<br>المباريات
    </button>

    <button onclick="show('news')">
      📰<br>الأخبار
    </button>

    <button onclick="show('profile')">
      👤<br>حسابي
    </button>

  </nav>

</div>


<script>

let points = 0;
let timer = null;


/* تغيير الشاشة */
function show(id) {

  document.querySelectorAll("section")
    .forEach(section => section.classList.remove("active"));

  document.getElementById(id)
    .classList.add("active");

  window.scrollTo(0,0);
}


/* إضافة نقاط */
function addPoints(value) {

  points += value;

  document.getElementById("points")
    .textContent = points;
}


/* لعبة المزاد */
function startAuction(players, budget) {

  show("game");

  document.getElementById("gameContent").innerHTML = `

    <h2>🔨 المزاد</h2>

    <p class="note">
      فريقك يحتاج إلى ${players} لاعب + مدرب.
    </p>

    <div class="list">

      <div class="player">

        <div class="player-name">
          لاعب معروض
        </div>

        <p>
          الميزانية: ${budget} مليون €
        </p>

        <div class="bid">
          أعلى مزايدة:
          <b id="currentBid">20</b>
          مليون €
        </div>

        <div>
          ⏱️
          <b id="auctionTimer">20</b>
          ثانية
        </div>

      </div>

      <button onclick="raiseBid()">
        ➕ زايد 5 مليون
      </button>

      <button class="secondary" onclick="skipPlayer()">
        تخطي
      </button>

    </div>

    <p class="note">
      النسخة القادمة ستربط المزاد بين هاتفين عن طريق السيرفر.
    </p>
  `;

  let seconds = 20;

  clearInterval(timer);

  timer = setInterval(() => {

    
