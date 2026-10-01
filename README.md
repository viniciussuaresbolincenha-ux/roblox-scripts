<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Roblox Scripts</title>

  <style>
    :root {
      --primary: #8b5cf6;
      --primary-dark: #6d28d9;
      --bg: #050505;
      --card: #101010;
      --card-hover: #171717;
      --text: #ffffff;
      --muted: #a1a1aa;
      --border: #252525;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    a {
      color: inherit;
    }

    /* NAVBAR */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      height: 70px;

      display: flex;
      align-items: center;
      justify-content: space-between;

      padding: 0 7%;

      background: rgba(5, 5, 5, 0.92);
      backdrop-filter: blur(12px);

      border-bottom: 1px solid var(--border);

      z-index: 1000;
    }

    .logo {
      font-size: 21px;
      font-weight: 900;
      letter-spacing: 1px;
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 25px;
    }

    .nav-links a {
      text-decoration: none;
      color: #ddd;
      font-size: 14px;
      transition: 0.2s;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    .appearance-button {
      border: none;
      cursor: pointer;

      background: var(--primary);
      color: white;

      padding: 10px 15px;
      border-radius: 9px;

      font-weight: bold;

      transition: 0.2s;
    }

    .appearance-button:hover {
      background: var(--primary-dark);
      transform: translateY(-2px);
    }

    /* HERO */

    .hero {
      min-height: 100vh;

      display: flex;
      align-items: center;
      justify-content: center;

      text-align: center;

      padding: 120px 20px 70px;

      background:
        radial-gradient(
          circle at center,
          rgba(139, 92, 246, 0.16),
          transparent 45%
        );
    }

    .hero-content {
      max-width: 850px;
    }

    .hero h1 {
      font-size: clamp(42px, 7vw, 82px);
      font-weight: 900;
      line-height: 1.05;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: var(--primary);
    }

    .hero p {
      color: var(--muted);
      font-size: 18px;
      max-width: 650px;
      margin: 0 auto 35px;
    }

    .hero-buttons {
      display: flex;
      justify-content: center;
      gap: 14px;
      flex-wrap: wrap;
    }

    .button {
      display: inline-block;
      padding: 14px 22px;

      border-radius: 10px;

      text-decoration: none;
      font-weight: bold;

      transition: 0.2s;
    }

    .button-primary {
      background: var(--primary);
      color: white;
    }

    .button-primary:hover {
      background: var(--primary-dark);
      transform: translateY(-2px);
    }

    .button-secondary {
      border: 1px solid var(--border);
      background: #101010;
      color: white;
    }

    .button-secondary:hover {
      border-color: var(--primary);
      transform: translateY(-2px);
    }

    /* SECTIONS */

    .section {
      padding: 100px 7%;
    }

    .container {
      max-width: 1150px;
      margin: auto;
    }

    .section-title {
      text-align: center;
      font-size: 38px;
      margin-bottom: 12px;
    }

    .section-subtitle {
      text-align: center;
      color: var(--muted);
      margin-bottom: 55px;
    }

    /* STEPS */

    .steps {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .step {
      background: var(--card);
      border: 1px solid var(--border);

      border-radius: 16px;

      padding: 30px;

      transition: 0.25s;
    }

    .step:hover {
      transform: translateY(-5px);
      background: var(--card-hover);
      border-color: var(--primary);
    }

    .step-number {
      width: 45px;
      height: 45px;

      display: flex;
      align-items: center;
      justify-content: center;

      border-radius: 12px;

      background: var(--primary);

      font-weight: 900;

      margin-bottom: 20px;
    }

    .step h3 {
      margin-bottom: 10px;
    }

    .step p {
      color: var(--muted);
    }

    /* PRODUCTS */

    .products {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .product-card {
      position: relative;

      background: var(--card);

      border: 1px solid var(--border);

      border-radius: 18px;

      padding: 30px;

      transition: 0.25s;
    }

    .product-card:hover {
      transform: translateY(-6px);
      background: var(--card-hover);
      border-color: var(--primary);
    }

    .product-tag {
      display: inline-block;

      font-size: 11px;
      font-weight: bold;

      padding: 5px 9px;

      border-radius: 6px;

      background: rgba(139, 92, 246, 0.15);
      color: var(--primary);

      margin-bottom: 15px;
    }

    .product-card h3 {
      font-size: 23px;
      margin-bottom: 12px;
    }

    .product-card p {
      color: var(--muted);
      min-height: 70px;
      margin-bottom: 18px;
    }

    .price {
      font-size: 26px;
      font-weight: 900;
      margin-bottom: 15px;
    }

    .robux {
      color: #22c55e;
    }

    .buy-button {
      display: block;

      width: 100%;

      margin-top: 18px;

      padding: 13px 18px;

      border-radius: 10px;

      background: var(--primary);

      color: white;

      text-align: center;

      text-decoration: none;

      font-weight: 700;

      transition: 0.2s;
    }

    .buy-button:hover {
      transform: translateY(-2px);
      filter: brightness(1.15);
    }

    /* ROBLOX STUDIO */

    .studio-box {
      background: var(--card);

      border: 1px solid var(--border);

      border-radius: 20px;

      padding: 40px;

      text-align: center;
    }

    .studio-box h3 {
      font-size: 30px;
      margin-bottom: 15px;
    }

    .studio-box p {
      max-width: 750px;
      margin: auto;

      color: var(--muted);

      margin-bottom: 25px;
    }

    /* CONTACT */

    .contact-box {
      text-align: center;

      background:
        radial-gradient(
          circle at center,
          rgba(139, 92, 246, 0.15),
          transparent 60%
        );

      border: 1px solid var(--border);

      border-radius: 20px;

      padding: 60px 20px;
    }

    .contact-box h2 {
      font-size: 40px;
      margin-bottom: 12px;
    }

    .contact-box p {
      color: var(--muted);
      margin-bottom: 30px;
    }

    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 12px;
      flex-wrap: wrap;
    }

    /* APPEARANCE PANEL */

    .appearance-panel {
      position: fixed;

      top: 80px;
      right: 20px;

      width: 260px;

      background: #0d0d0d;

      border: 1px solid var(--border);

      border-radius: 15px;

      padding: 20px;

      z-index: 2000;

      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);

      display: none;
    }

    .appearance-panel.active {
      display: block;
    }

    .appearance-panel h3 {
      margin-bottom: 15px;
    }

    .colors {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
    }

    .color {
      width: 42px;
      height: 42px;

      border-radius: 10px;

      border: 2px solid #333;

      cursor: pointer;

      transition: 0.2s;
    }

    .color:hover {
      transform: scale(1.1);
      border-color: white;
    }

    /* FOOTER */

    footer {
      border-top: 1px solid var(--border);

      padding: 30px 20px;

      text-align: center;

      color: #71717a;

      font-size: 14px;
    }

    footer span {
      color: var(--primary);
    }

    /* MOBILE */

    @media (max-width: 800px) {

      nav {
        padding: 0 20px;
      }

      .nav-links {
        display: none;
      }

      .steps,
      .products {
        grid-template-columns: 1fr;
      }

      .section {
        padding: 80px 20px;
      }

      .hero {
        padding-left: 20px;
        padding-right: 20px;
      }

      .studio-box {
        padding: 30px 20px;
      }

      .appearance-panel {
        right: 10px;
        left: 10px;
        width: auto;
      }
    }
  </style>
</head>

<body>

  <!-- NAVBAR -->

  <nav>

    <div class="logo">
      ROBLOX SCRIPTS
    </div>

    <div class="nav-links">

      <a href="#inicio">Início</a>

      <a href="#como-funciona">Como funciona</a>

      <a href="#scripts">Scripts</a>

      <a href="#studio">Roblox Studio</a>

      <a href="#contato">Contato</a>

    </div>

    <button
      class="appearance-button"
      onclick="toggleAppearance()">

      🎨 Aparência

    </button>

  </nav>


  <!-- APPEARANCE -->

  <div
    class="appearance-panel"
    id="appearancePanel">

    <h3>Editar aparência</h3>

    <div class="colors">

      <button
        class="color"
        style="background:#8b5cf6"
        onclick="changeColor('#8b5cf6','#6d28d9')">
      </button>

      <button
        class="color"
        style="background:#ffffff"
        onclick="changeColor('#ffffff','#cccccc')">
      </button>

      <button
        class="color"
        style="background:#2563eb"
        onclick="changeColor('#2563eb','#1d4ed8')">
      </button>

      <button
        class="color"
        style="background:#ef4444"
        onclick="changeColor('#ef4444','#b91c1c')">
      </button>

      <button
        class="color"
        style="background:#008cff"
        onclick="changeColor('#008cff','#0066cc')">
      </button>

      <button
        class="color"
        style="background:#06d6d6"
        onclick="changeColor('#06d6d6','#0891b2')">
      </button>

      <button
        class="color"
        style="background:#22c55e"
        onclick="changeColor('#22c55e','#15803d')">
      </button>

      <button
        class="color"
        style="background:#f97316"
        onclick="changeColor('#f97316','#c2410c')">
      </button>

    </div>

  </div>


  <!-- HERO -->

  <section
    class="hero"
    id="inicio">

    <div class="hero-content">

      <h1>
        Scripts para
        <span>Roblox</span>
      </h1>

      <p>
        Encontre scripts para seus projetos no Roblox Studio
        e compre de forma simples utilizando Robux.
      </p>

      <div class="hero-buttons">

        <a
          href="#scripts"
          class="button button-primary">

          🛒 Ver scripts

        </a>

        <a
          href="#contato"
          class="button button-secondary">

          💬 Contato

        </a>

      </div>

    </div>

  </section>


  <!-- COMO FUNCIONA -->

  <section
    class="section"
    id="como-funciona">

    <div class="container">

      <h2 class="section-title">
        Como funciona?
      </h2>

      <p class="section-subtitle">
        Comprar um script é simples.
      </p>


      <div class="steps">

        <div class="step">

          <div class="step-number">
            1
          </div>

          <h3>
            Escolha o script
          </h3>

          <p>
            Escolha o script que você deseja
            para seu projeto.
          </p>

        </div>


        <div class="step">

          <div class="step-number">
            2
          </div>

          <h3>
            Pague com Robux
          </h3>

          <p>
            Clique no botão de compra e
            acesse o Game Pass correspondente.
          </p>

        </div>


        <div class="step">

          <div class="step-number">
            3
          </div>

          <h3>
            Receba o script
          </h3>

          <p>
            Depois da compra, entre em contato
            para receber as informações do script.
          </p>

        </div>

      </div>

    </div>

  </section>


  <!-- SCRIPTS -->

  <section
    class="section"
    id="scripts">

    <div class="container">

      <h2 class="section-title">
        Scripts disponíveis
      </h2>

      <p class="section-subtitle">
        Escolha seu script e compre com Robux.
      </p>


      <div class="products">


        <!-- SCRIPT 1 -->

        <div class="product-card">

          <span class="product-tag">
            BÁSICO
          </span>

          <h3>
            Script Básico
          </h3>

          <p>
            Script simples para começar
            seu projeto no Roblox Studio.
          </p>

          <div class="price">
            <span class="robux">
              100 R$
            </span>
          </div>

          <a
            href="COLE_AQUI_O_LINK_DO_GAMEPASS_1"
            target="_blank"
            class="buy-button">

            💰 Comprar com Robux

          </a>

        </div>


        <!-- SCRIPT 2 -->

        <div class="product-card">

          <span class="product-tag">
            PREMIUM
          </span>

          <h3>
            Script Premium
          </h3>

          <p>
            Uma opção mais completa
            para seus projetos.
          </p>

          <div class="price">
            <span class="robux">
              200 R$
            </span>
          </div>

          <a
            href="COLE_AQUI_O_LINK_DO_GAMEPASS_2"
            target="_blank"
            class="buy-button">

            💰 Comprar com Robux

          </a>

        </div>


        <!-- SCRIPT 3 -->

        <div class="product-card">

          <span class="product-tag">
            PRO
          </span>

          <h3>
            Script Pro
          </h3>

          <p>
            Script avançado para
            projetos maiores.
          </p>

          <div class="price">
            <span class="robux">
              300 R$
            </span>
          </div>

          <a
            href="COLE_AQUI_O_LINK_DO_GAMEPASS_3"
            target="_blank"
            class="buy-button">

            💰 Comprar com Robux

          </a>

        </div>


      </div>

    </div>

  </section>


  <!-- ROBLOX STUDIO -->

  <section
    class="section"
    id="studio">

    <div class="container">

      <div class="studio-box">

        <h3>
          🎮 Roblox Studio
        </h3>

        <p>
          O Roblox Studio é a ferramenta utilizada
          para criar experiências no Roblox.
          Você pode construir mapas, criar sistemas,
          adicionar scripts e muito mais.
        </p>

        <a
          href="https://create.roblox.com/"
          target="_blank"
          class="button button-primary">

          Abrir Roblox Studio

        </a>

      </div>

    </div>

  </section>


  <!-- CONTATO -->

  <section
    class="section"
    id="contato">

    <div class="container">

      <div class="contact-box">

        <h2>
          Entre em contato
        </h2>

        <p>
          Precisa de ajuda ou quer falar comigo?
        </p>


        <div class="contact-buttons">

          <a
            href="https://www.tiktok.com/@Vinlumezx00"
            target="_blank"
            class="button button-primary">

            🎵 TikTok
            @Vinlumezx00

          </a>


          <a
            href="https://www.roblox.com/search/users?keyword=Vinlumexz00"
            target="_blank"
            class="button button-secondary">

            🎮 Roblox
            Vinlumexz00

          </a>

        </div>

      </div>

    </div>

  </section>


  <!-- FOOTER -->

  <footer>

    © 2026
    <span>
      Roblox Scripts
    </span>

    — Todos os direitos reservados.

  </footer>


  <!-- JAVASCRIPT -->

  <script>

    const root =
      document.documentElement;


    function toggleAppearance() {

      const panel =
        document.getElementById(
          "appearancePanel"
        );

      panel.classList.toggle(
        "active"
      );

    }


    function changeColor(
      primary,
      dark
    ) {

      root.style.setProperty(
        "--primary",
        primary
      );

      root.style.setProperty(
        "--primary-dark",
        dark
      );


      localStorage.setItem(
        "primaryColor",
        primary
      );

      localStorage.setItem(
        "darkColor",
        dark
      );

    }


    const savedPrimary =
      localStorage.getItem(
        "primaryColor"
      );

    const savedDark =
      localStorage.getItem(
        "darkColor"
      );


    if (
      savedPrimary &&
      savedDark
    ) {

      root.style.setProperty(
        "--primary",
        savedPrimary
      );

      root.style.setProperty(
        "--primary-dark",
        savedDark
      );

    }

  </script>

</body>
</html>
