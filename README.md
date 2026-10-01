<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#08080b">

<title>VinlumeXz00 | Roblox Scripts</title>

<style>
:root{
  --primary:#8b5cf6;
  --primary2:#6d28d9;
  --bg:#050507;
  --bg2:#09090d;
  --card:#101014;
  --card2:#15151b;
  --text:#fff;
  --muted:#a1a1aa;
  --border:rgba(255,255,255,.09);
  --success:#22c55e;
  --danger:#ef4444;
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  scroll-behavior:smooth;
}

html{
  background:var(--bg);
}

body{
  font-family:Inter,Arial,Helvetica,sans-serif;
  background:
    radial-gradient(circle at 50% -10%,rgba(139,92,246,.18),transparent 35%),
    var(--bg);
  color:var(--text);
  min-height:100vh;
  overflow-x:hidden;
}

body::before{
  content:"";
  position:fixed;
  inset:0;
  pointer-events:none;
  background-image:
    linear-gradient(rgba(255,255,255,.018) 1px,transparent 1px),
    linear-gradient(90deg,rgba(255,255,255,.018) 1px,transparent 1px);
  background-size:55px 55px;
  mask-image:linear-gradient(to bottom,#000,transparent 85%);
}

a{
  color:inherit;
  text-decoration:none;
}

button{
  font:inherit;
}

/* ================= NAVBAR ================= */

.navbar{
  position:fixed;
  top:14px;
  left:50%;
  transform:translateX(-50%);
  width:min(1180px,calc(100% - 28px));
  height:64px;
  padding:0 18px;

  display:flex;
  align-items:center;
  justify-content:space-between;

  background:rgba(10,10,14,.78);
  border:1px solid var(--border);
  border-radius:18px;

  backdrop-filter:blur(18px);
  -webkit-backdrop-filter:blur(18px);

  z-index:1000;
  box-shadow:0 15px 50px rgba(0,0,0,.3);
}

.logo{
  display:flex;
  align-items:center;
  gap:10px;
  font-weight:900;
  letter-spacing:.5px;
}

.logo-icon{
  width:35px;
  height:35px;
  display:grid;
  place-items:center;
  border-radius:10px;
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  box-shadow:0 0 25px rgba(139,92,246,.35);
}

.logo span{
  color:var(--primary);
}

.nav-links{
  display:flex;
  gap:25px;
}

.nav-links a{
  color:#b9b9c2;
  font-size:14px;
  transition:.2s;
}

.nav-links a:hover{
  color:white;
}

.nav-actions{
  display:flex;
  align-items:center;
  gap:8px;
}

.icon-button{
  width:40px;
  height:40px;
  border:1px solid var(--border);
  background:#111116;
  color:white;
  border-radius:11px;
  cursor:pointer;
  transition:.2s;
}

.icon-button:hover{
  border-color:var(--primary);
  transform:translateY(-2px);
}

/* ================= HERO ================= */

.hero{
  min-height:850px;
  padding:170px 20px 100px;

  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;

  position:relative;
}

.hero-glow{
  position:absolute;
  width:600px;
  height:600px;
  border-radius:50%;
  background:var(--primary);
  opacity:.09;
  filter:blur(100px);
  pointer-events:none;
}

.hero-content{
  max-width:900px;
  position:relative;
  z-index:1;
}

.badge{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding:8px 13px;
  border:1px solid rgba(139,92,246,.25);
  background:rgba(139,92,246,.08);
  border-radius:999px;
  color:#c4b5fd;
  font-size:13px;
  margin-bottom:25px;
}

.badge-dot{
  width:7px;
  height:7px;
  background:#22c55e;
  border-radius:50%;
  box-shadow:0 0 12px #22c55e;
}

.hero h1{
  font-size:clamp(48px,8vw,92px);
  line-height:.98;
  letter-spacing:-4px;
  font-weight:950;
}

.hero h1 span{
  background:linear-gradient(90deg,var(--primary),#c4b5fd,var(--primary));
  background-size:200%;
  -webkit-background-clip:text;
  color:transparent;
  animation:gradient 4s linear infinite;
}

@keyframes gradient{
  to{background-position:200%}
}

.hero p{
  max-width:670px;
  margin:27px auto 35px;
  color:var(--muted);
  font-size:18px;
  line-height:1.8;
}

.hero-buttons{
  display:flex;
  justify-content:center;
  gap:12px;
  flex-wrap:wrap;
}

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:9px;
  min-height:48px;
  padding:0 21px;
  border-radius:12px;
  font-weight:800;
  border:1px solid var(--border);
  transition:.25s;
  cursor:pointer;
}

.btn:hover{
  transform:translateY(-3px);
}

.btn-primary{
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  border-color:transparent;
  box-shadow:0 10px 35px rgba(139,92,246,.22);
}

.btn-secondary{
  background:#111116;
}

.btn-secondary:hover{
  border-color:var(--primary);
}

.hero-stats{
  display:flex;
  justify-content:center;
  gap:40px;
  margin-top:65px;
  color:var(--muted);
}

.stat strong{
  display:block;
  color:white;
  font-size:21px;
}

.stat span{
  font-size:12px;
}

/* ================= GLOBAL ================= */

.section{
  padding:105px 20px;
  position:relative;
}

.container{
  width:min(1120px,100%);
  margin:auto;
}

.section-heading{
  text-align:center;
  margin-bottom:50px;
}

.section-heading .mini{
  color:var(--primary);
  text-transform:uppercase;
  font-size:12px;
  font-weight:900;
  letter-spacing:2px;
}

.section-heading h2{
  font-size:clamp(32px,5vw,48px);
  margin:9px 0;
  letter-spacing:-1.5px;
}

.section-heading p{
  color:var(--muted);
}

/* ================= HOW ================= */

.steps{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
}

.step{
  background:linear-gradient(145deg,var(--card),#0b0b0e);
  border:1px solid var(--border);
  border-radius:20px;
  padding:30px;
  transition:.3s;
}

.step:hover{
  transform:translateY(-7px);
  border-color:rgba(139,92,246,.4);
}

.step-number{
  width:45px;
  height:45px;
  display:grid;
  place-items:center;
  background:rgba(139,92,246,.13);
  color:#c4b5fd;
  border:1px solid rgba(139,92,246,.25);
  border-radius:13px;
  font-weight:900;
  margin-bottom:22px;
}

.step h3{
  font-size:20px;
  margin-bottom:9px;
}

.step p{
  color:var(--muted);
  font-size:14px;
}

/* ================= PRODUCTS ================= */

.products{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
}

.product{
  position:relative;
  background:linear-gradient(145deg,#111116,#0b0b0f);
  border:1px solid var(--border);
  border-radius:22px;
  padding:28px;
  transition:.3s;
  overflow:hidden;
}

.product::before{
  content:"";
  position:absolute;
  width:180px;
  height:180px;
  background:var(--primary);
  opacity:.06;
  filter:blur(50px);
  top:-80px;
  right:-60px;
}

.product:hover{
  transform:translateY(-8px);
  border-color:rgba(139,92,246,.5);
  box-shadow:0 25px 70px rgba(0,0,0,.3);
}

.product.popular{
  border-color:rgba(139,92,246,.5);
}

.popular-label{
  position:absolute;
  top:15px;
  right:15px;
  background:var(--primary);
  padding:6px 10px;
  border-radius:7px;
  font-size:10px;
  font-weight:900;
}

.product-tag{
  display:inline-block;
  padding:5px 9px;
  background:rgba(255,255,255,.05);
  border-radius:7px;
  color:#a1a1aa;
  font-size:10px;
  font-weight:900;
  letter-spacing:1px;
}

.product h3{
  font-size:24px;
  margin:18px 0 10px;
}

.product-description{
  color:var(--muted);
  min-height:67px;
  font-size:14px;
}

.product-price{
  margin-top:25px;
  font-size:30px;
  font-weight:950;
}

.product-price small{
  color:#22c55e;
  font-size:13px;
  margin-left:5px;
}

.buy{
  width:100%;
  margin-top:20px;
}

.buy.disabled{
  opacity:.55;
  cursor:not-allowed;
}

.buy.disabled:hover{
  transform:none;
}

/* ================= STUDIO ================= */

.studio{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:20px;
  align-items:stretch;
}

.studio-main,
.profile-card{
  border:1px solid var(--border);
  border-radius:22px;
  background:linear-gradient(145deg,var(--card),#0a0a0d);
  padding:35px;
}

.studio-main h3{
  font-size:30px;
  margin-bottom:13px;
}

.studio-main p{
  color:var(--muted);
  line-height:1.8;
  margin-bottom:25px;
}

.features{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
}

.feature{
  padding:13px;
  background:#0b0b0f;
  border:1px solid var(--border);
  border-radius:11px;
  font-size:13px;
}

/* ================= PROFILE ================= */

.profile-card{
  display:flex;
  flex-direction:column;
  justify-content:center;
}

.profile-top{
  display:flex;
  align-items:center;
  gap:17px;
}

.avatar{
  width:65px;
  height:65px;
  display:grid;
  place-items:center;
  border-radius:18px;
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  font-size:25px;
  font-weight:900;
}

.profile-info h3{
  font-size:21px;
}

.profile-info p{
  color:var(--muted);
  font-size:13px;
}

.profile-status{
  margin-top:25px;
  padding:13px;
  background:rgba(34,197,94,.07);
  border:1px solid rgba(34,197,94,.15);
  color:#86efac;
  border-radius:11px;
  font-size:13px;
}

/* ================= CONTACT ================= */

.contact-box{
  text-align:center;
  padding:75px 20px;
  border-radius:25px;
  border:1px solid var(--border);
  background:
    radial-gradient(circle at center,rgba(139,92,246,.13),transparent 60%),
    #0b0b0f;
}

.contact-box h2{
  font-size:clamp(34px,5vw,52px);
  margin-bottom:10px;
}

.contact-box p{
  color:var(--muted);
  margin-bottom:28px;
}

.contact-buttons{
  display:flex;
  justify-content:center;
  gap:10px;
  flex-wrap:wrap;
}

/* ================= APPEARANCE ================= */

.appearance-panel{
  position:fixed;
  top:88px;
  right:18px;
  width:290px;
  padding:22px;
  background:rgba(12,12,16,.96);
  border:1px solid var(--border);
  border-radius:20px;
  backdrop-filter:blur(20px);
  z-index:2000;
  box-shadow:0 25px 80px rgba(0,0,0,.55);
  transform:translateY(-15px) scale(.97);
  opacity:0;
  pointer-events:none;
  transition:.2s;
}

.appearance-panel.active{
  transform:none;
  opacity:1;
  pointer-events:auto;
}

.appearance-panel h3{
  margin-bottom:4px;
}

.appearance-panel p{
  color:var(--muted);
  font-size:12px;
  margin-bottom:18px;
}

.colors{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:10px;
}

.color{
  height:48px;
  border-radius:12px;
  border:2px solid transparent;
  cursor:pointer;
  transition:.2s;
}

.color:hover{
  transform:scale(1.08);
  border-color:white;
}

/* ================= TOAST ================= */

.toast{
  position:fixed;
  bottom:25px;
  left:50%;
  transform:translate(-50%,20px);
  background:#17171d;
  border:1px solid var(--border);
  padding:13px 18px;
  border-radius:12px;
  font-size:13px;
  opacity:0;
  pointer-events:none;
  transition:.3s;
  z-index:3000;
}

.toast.show{
  opacity:1;
  transform:translate(-50%,0);
}

/* ================= FOOTER ================= */

footer{
  padding:35px 20px;
  border-top:1px solid var(--border);
  text-align:center;
  color:#71717a;
  font-size:13px;
}

footer strong{
  color:var(--primary);
}

/* ================= MOBILE ================= */

@media(max-width:850px){

  .nav-links{
    display:none;
  }

  .hero{
    min-height:760px;
  }

  .hero h1{
    letter-spacing:-2px;
  }

  .hero-stats{
    gap:20px;
  }

  .steps,
  .products,
  .studio{
    grid-template-columns:1fr;
  }
}

@media(max-width:500px){

  .navbar{
    height:58px;
  }

  .logo{
    font-size:14px;
  }

  .logo-icon{
    width:31px;
    height:31px;
  }

  .hero{
    padding-top:130px;
  }

  .hero p{
    font-size:15px;
  }

  .hero-stats{
    flex-direction:column;
    gap:15px;
  }

  .features{
    grid-template-columns:1fr;
  }

  .product,
  .step,
  .studio-main,
  .profile-card{
    padding:24px;
  }

  .appearance-panel{
    left:15px;
    right:15px;
    width:auto;
  }
}
</style>
</head>

<body>

<!-- NAVBAR -->

<nav class="navbar">

  <a href="#inicio" class="logo">
    <div class="logo-icon">R</div>
    ROBLOX <span>SCRIPTS</span>
  </a>

  <div class="nav-links">
    <a href="#inicio">Início</a>
    <a href="#como-funciona">Como funciona</a>
    <a href="#scripts">Scripts</a>
    <a href="#studio">Studio</a>
    <a href="#contato">Contato</a>
  </div>

  <div class="nav-actions">
    <button class="icon-button" onclick="toggleAppearance()" title="Editar aparência">
      🎨
    </button>
  </div>

</nav>


<!-- APPEARANCE -->

<div class="appearance-panel" id="appearancePanel">

  <h3>Editar aparência</h3>

  <p>Escolha a cor principal do site.</p>

  <div class="colors">

    <button class="color" style="background:#8b5cf6"
      onclick="changeColor('#8b5cf6','#6d28d9')"></button>

    <button class="color" style="background:#ffffff"
      onclick="changeColor('#ffffff','#cccccc')"></button>

    <button class="color" style="background:#2563eb"
      onclick="changeColor('#2563eb','#1d4ed8')"></button>

    <button class="color" style="background:#ef4444"
      onclick="changeColor('#ef4444','#b91c1c')"></button>

    <button class="color" style="background:#008cff"
      onclick="changeColor('#008cff','#0066cc')"></button>

    <button class="color" style="background:#06d6d6"
      onclick="changeColor('#06d6d6','#0891b2')"></button>

    <button class="color" style="background:#22c55e"
      onclick="changeColor('#22c55e','#15803d')"></button>

    <button class="color" style="background:#f97316"
      onclick="changeColor('#f97316','#c2410c')"></button>

  </div>

</div>


<!-- HERO -->

<section class="hero" id="inicio">

  <div class="hero-glow"></div>

  <div class="hero-content">

    <div class="badge">
      <span class="badge-dot"></span>
      Scripts para Roblox
    </div>

    <h1>
      Construa.
      <span>Crie.</span>
      Evolua.
    </h1>

    <p>
      Scripts para Roblox Studio feitos para ajudar
      você a criar experiências melhores, de forma simples
      e organizada.
    </p>

    <div class="hero-buttons">

      <a href="#scripts" class="btn btn-primary">
        🛒 Ver scripts
      </a>

      <a href="#contato" class="btn btn-secondary">
        💬 Falar comigo
      </a>

    </div>

    <div class="hero-stats">

      <div class="stat">
        <strong>ROBLOX</strong>
        <span>Studio</span>
      </div>

      <div class="stat">
        <strong>ROBUX</strong>
        <span>Compra</span>
      </div>

      <div class="stat">
        <strong>100%</strong>
        <span>Online</span>
      </div>

    </div>

  </div>

</section>


<!-- COMO FUNCIONA -->

<section class="section" id="como-funciona">

  <div class="container">

    <div class="section-heading">
      <div class="mini">Processo</div>
      <h2>Como funciona?</h2>
      <p>Comprar um script é simples.</p>
    </div>

    <div class="steps">

      <div class="step">

        <div class="step-number">01</div>

        <h3>Escolha seu script</h3>

        <p>
          Veja os scripts disponíveis e escolha
          aquele que deseja utilizar.
        </p>

      </div>

      <div class="step">

        <div class="step-number">02</div>

        <h3>Compre com Robux</h3>

        <p>
          Clique no botão de compra e acesse
          o Game Pass correspondente.
        </p>

      </div>

      <div class="step">

        <div class="step-number">03</div>

        <h3>Entre em contato</h3>

        <p>
          Depois da compra, entre em contato
          para receber as informações necessárias.
        </p>

      </div>

    </div>

  </div>

</section>


<!-- PRODUTOS -->

<section class="section" id="scripts">

  <div class="container">

    <div class="section-heading">

      <div class="mini">Loja</div>

      <h2>Scripts disponíveis</h2>

      <p>
        Escolha uma opção abaixo.
      </p>

    </div>


    <div class="products">


      <!-- PRODUTO 1 -->

      <div class="product">

        <span class="product-tag">
          BÁSICO
        </span>

        <h3>Script Básico</h3>

        <p class="product-description">
          Uma opção simples para projetos
          e experiências no Roblox Studio.
        </p>

        <div class="product-price">
          100 <small>R$</small>
        </div>

        <a
          href="COLE_SEU_LINK_DO_GAMEPASS_1"
          target="_blank"
          class="btn btn-primary buy"
          onclick="buyProduct(event,'Script Básico')">

          💰 Comprar com Robux

        </a>

      </div>


      <!-- PRODUTO 2 -->

      <div class="product popular">

        <div class="popular-label">
          POPULAR
        </div>

        <span class="product-tag">
          PREMIUM
        </span>

        <h3>Script Premium</h3>

        <p class="product-description">
          Uma opção mais completa para
          projetos que precisam de mais recursos.
        </p>

        <div class="product-price">
          200 <small>R$</small>
        </div>

        <a
          href="COLE_SEU_LINK_DO_GAMEPASS_2"
          target="_blank"
          class="btn btn-primary buy"
          onclick="buyProduct(event,'Script Premium')">

          💰 Comprar com Robux

        </a>

      </div>


      <!-- PRODUTO 3 -->

      <div class="product">

        <span class="product-tag">
          PRO
        </span>

        <h3>Script Pro</h3>

        <p class="product-description">
          Para projetos maiores que precisam
          de uma solução mais avançada.
        </p>

        <div class="product-price">
          300 <small>R$</small>
        </div>

        <a
          href="COLE_SEU_LINK_DO_GAMEPASS_3"
          target="_blank"
          class="btn btn-primary buy"
          onclick="buyProduct(event,'Script Pro')">

          💰 Comprar com Robux

        </a>

      </div>

    </div>

  </div>

</section>


<!-- ROBLOX STUDIO -->

<section class="section" id="studio">

  <div class="container">

    <div class="section-heading">

      <div class="mini">Desenvolvimento</div>

      <h2>Roblox Studio</h2>

      <p>
        O lugar onde seus projetos ganham vida.
      </p>

    </div>


    <div class="studio">

      <div class="studio-main">

        <h3>🎮 Crie no Roblox Studio</h3>

        <p>
          O Roblox Studio permite criar mapas,
          sistemas, interfaces, scripts e
          experiências completas para Roblox.
        </p>

        <div class="features">

          <div class="feature">⚙️ Sistemas</div>
          <div class="feature">🧩 Scripts</div>
          <div class="feature">🌎 Mapas</div>
          <div class="feature">🎨 Interfaces</div>

        </div>

        <br>

        <a
          href="https://create.roblox.com/"
          target="_blank"
          class="btn btn-primary">

          Abrir Roblox Studio

        </a>

      </div>


      <!-- PERFIL -->

      <div class="profile-card">

        <div class="profile-top">

          <div class="avatar">
            V
          </div>

          <div class="profile-info">

            <h3>
              Vinlumexz00
            </h3>

            <p>
              Conta Roblox
            </p>

          </div>

        </div>


        <div class="profile-status">

          ● Usuário informado pelo proprietário do site

        </div>

        <br>

        <a
          href="https://www.roblox.com/search/users?keyword=Vinlumexz00"
          target="_blank"
          class="btn btn-secondary">

          🔎 Ver no Roblox

        </a>

      </div>

    </div>

  </div>

</section>


<!-- CONTATO -->

<section class="section" id="contato">

  <div class="container">

    <div class="contact-box">

      <div class="section-heading" style="margin-bottom:25px">

        <div class="mini">Contato</div>

        <h2>Vamos conversar?</h2>

        <p>
          Entre em contato pelas minhas redes.
        </p>

      </div>


      <div class="contact-buttons">

        <a
          href="https://www.tiktok.com/@Vinlumezx00"
          target="_blank"
          class="btn btn-primary">

          🎵 TikTok @Vinlumezx00

        </a>

        <a
          href="https://www.roblox.com/search/users?keyword=Vinlumexz00"
          target="_blank"
          class="btn btn-secondary">

          🎮 Roblox Vinlumexz00

        </a>

      </div>

    </div>

  </div>

</section>


<!-- FOOTER -->

<footer>

  © 2026
  <strong>Roblox Scripts</strong>
  • Desenvolvido para Roblox Studio

</footer>


<!-- TOAST -->

<div class="toast" id="toast"></div>


<script>

/* ================= APARÊNCIA ================= */

const root = document.documentElement;

function toggleAppearance(){

  document
    .getElementById("appearancePanel")
    .classList.toggle("active");

}


function changeColor(primary,primary2){

  root.style.setProperty("--primary",primary);
  root.style.setProperty("--primary2",primary2);

  localStorage.setItem("sitePrimary",primary);
  localStorage.setItem("sitePrimary2",primary2);

  showToast("Aparência atualizada!");

}


/* ================= CARREGAR COR ================= */

const savedPrimary =
  localStorage.getItem("sitePrimary");

const savedPrimary2 =
  localStorage.getItem("sitePrimary2");

if(savedPrimary && savedPrimary2){

  root.style.setProperty(
    "--primary",
    savedPrimary
  );

  root.style.setProperty(
    "--primary2",
    savedPrimary2
  );

}


/* ================= TOAST ================= */

let toastTimer;

function showToast(message){

  const toast =
    document.getElementById("toast");

  toast.textContent = message;

  toast.classList.add("show");

  clearTimeout(toastTimer);

  toastTimer = setTimeout(()=>{

    toast.classList.remove("show");

  },2500);

}


/* ================= COMPRA ================= */

function buyProduct(event,name){

  const link =
    event.currentTarget.getAttribute("href");

  if(
    !link ||
    link.startsWith("COLE_")
  ){

    event.preventDefault();

    showToast(
      "O link deste Game Pass ainda não foi configurado."
    );

    return;
  }

  showToast(
    "Abrindo compra de " + name + "..."
  );

}


/* ================= FECHAR PAINEL ================= */

document.addEventListener("click",function(event){

  const panel =
    document.getElementById("appearancePanel");

  const button =
    document.querySelector(".icon-button");

  if(
    panel.classList.contains("active") &&
    !panel.contains(event.target) &&
    !button.contains(event.target)
  ){

    panel.classList.remove("active");

  }

});

</script>

</body>
</html>
