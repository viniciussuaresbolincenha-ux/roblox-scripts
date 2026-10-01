<!DOCTYPE html>

<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#07070a">
<title>Roblox Scripts | Vinlumexz00</title>

<style>
:root{
  --primary:#8b5cf6;
  --primary2:#6d28d9;
  --bg:#050507;
  --card:#101014;
  --card2:#15151b;
  --text:#fff;
  --muted:#a1a1aa;
  --border:rgba(255,255,255,.09);
  --green:#22c55e;
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  scroll-behavior:smooth;
}

body{
  font-family:Arial,Helvetica,sans-serif;
  background:
    radial-gradient(circle at 50% -10%,rgba(139,92,246,.18),transparent 35%),
    var(--bg);
  color:var(--text);
  overflow-x:hidden;
}

body:before{
  content:"";
  position:fixed;
  inset:0;
  pointer-events:none;
  opacity:.35;
  background-image:
    linear-gradient(rgba(255,255,255,.015) 1px,transparent 1px),
    linear-gradient(90deg,rgba(255,255,255,.015) 1px,transparent 1px);
  background-size:55px 55px;
}

a{
  color:inherit;
  text-decoration:none;
}

button{
  font:inherit;
}

/* NAV */

.navbar{
  position:fixed;
  z-index:1000;
  top:14px;
  left:50%;
  transform:translateX(-50%);
  width:min(1180px,calc(100% - 28px));
  height:64px;
  padding:0 18px;

  display:flex;
  align-items:center;
  justify-content:space-between;

  background:rgba(10,10,14,.8);
  border:1px solid var(--border);
  border-radius:18px;
  backdrop-filter:blur(18px);

  box-shadow:0 15px 50px rgba(0,0,0,.35);
}

.logo{
  display:flex;
  align-items:center;
  gap:9px;
  font-weight:900;
}

.logo-icon{
  width:36px;
  height:36px;
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
  gap:24px;
}

.nav-links a{
  color:#b9b9c2;
  font-size:14px;
  transition:.2s;
}

.nav-links a:hover{
  color:#fff;
}

.icon-btn{
  width:40px;
  height:40px;
  border:1px solid var(--border);
  background:#111116;
  color:#fff;
  border-radius:11px;
  cursor:pointer;
}

/* HERO */

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
  opacity:.08;
  filter:blur(110px);
}

.hero-content{
  max-width:900px;
  position:relative;
}

.badge{
  display:inline-flex;
  gap:8px;
  align-items:center;
  padding:8px 13px;
  border:1px solid rgba(139,92,246,.25);
  background:rgba(139,92,246,.08);
  border-radius:999px;
  color:#c4b5fd;
  font-size:13px;
  margin-bottom:25px;
}

.dot{
  width:7px;
  height:7px;
  border-radius:50%;
  background:#22c55e;
  box-shadow:0 0 12px #22c55e;
}

.hero h1{
  font-size:clamp(48px,8vw,92px);
  line-height:.98;
  letter-spacing:-4px;
  font-weight:950;
}

.gradient{
  background:linear-gradient(90deg,var(--primary),#c4b5fd,var(--primary));
  background-size:200%;
  -webkit-background-clip:text;
  color:transparent;
}

.hero p{
  max-width:680px;
  margin:28px auto 35px;
  color:var(--muted);
  font-size:18px;
  line-height:1.8;
}

.buttons{
  display:flex;
  justify-content:center;
  gap:12px;
  flex-wrap:wrap;
}

.btn{
  min-height:48px;
  padding:0 21px;
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:8px;
  border-radius:12px;
  border:1px solid var(--border);
  font-weight:800;
  cursor:pointer;
  transition:.25s;
}

.btn:hover{
  transform:translateY(-3px);
}

.primary{
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  border-color:transparent;
  box-shadow:0 10px 35px rgba(139,92,246,.22);
}

.secondary{
  background:#111116;
}

.stats{
  display:flex;
  justify-content:center;
  gap:45px;
  margin-top:60px;
}

.stat strong{
  display:block;
  font-size:21px;
}

.stat span{
  color:var(--muted);
  font-size:12px;
}

/* GENERAL */

.section{
  padding:105px 20px;
}

.container{
  width:min(1120px,100%);
  margin:auto;
}

.heading{
  text-align:center;
  margin-bottom:50px;
}

.heading small{
  color:var(--primary);
  font-weight:900;
  letter-spacing:2px;
  text-transform:uppercase;
}

.heading h2{
  font-size:clamp(32px,5vw,48px);
  margin:8px 0;
}

.heading p{
  color:var(--muted);
}

/* CATEGORIES */

.categories{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:12px;
}

.category{
  padding:22px;
  background:var(--card);
  border:1px solid var(--border);
  border-radius:17px;
  transition:.25s;
}

.category:hover{
  transform:translateY(-5px);
  border-color:rgba(139,92,246,.4);
}

.category-icon{
  font-size:27px;
  margin-bottom:12px;
}

.category h3{
  font-size:16px;
}

.category p{
  margin-top:5px;
  color:var(--muted);
  font-size:12px;
}

/* PRODUCTS */

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
}

.product:hover{
  transform:translateY(-7px);
  border-color:rgba(139,92,246,.5);
}

.popular{
  position:absolute;
  top:15px;
  right:15px;
  background:var(--primary);
  padding:5px 9px;
  border-radius:7px;
  font-size:10px;
  font-weight:900;
}

.tag{
  display:inline-block;
  padding:5px 9px;
  border-radius:7px;
  background:rgba(255,255,255,.05);
  color:#aaa;
  font-size:10px;
  font-weight:900;
}

.product h3{
  font-size:23px;
  margin:18px 0 10px;
}

.description{
  color:var(--muted);
  min-height:65px;
  font-size:14px;
}

.price{
  margin-top:22px;
  font-size:27px;
  font-weight:950;
}

.price small{
  color:#22c55e;
  font-size:12px;
}

.buy{
  width:100%;
  margin-top:12px;
}

.money{
  background:#15151a;
}

.robux{
  background:rgba(34,197,94,.1);
  border-color:rgba(34,197,94,.25);
  color:#86efac;
}

/* CUSTOM */

.custom-box{
  padding:50px 30px;
  text-align:center;
  background:
    radial-gradient(circle at center,rgba(139,92,246,.13),transparent 60%),
    var(--card);
  border:1px solid var(--border);
  border-radius:23px;
}

.custom-box h2{
  font-size:34px;
  margin-bottom:10px;
}

.custom-box p{
  color:var(--muted);
  max-width:650px;
  margin:0 auto 25px;
}

/* STUDIO */

.studio{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:18px;
}

.studio-card,
.profile{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:22px;
  padding:35px;
}

.studio-card h3{
  font-size:28px;
  margin-bottom:13px;
}

.studio-card p{
  color:var(--muted);
  line-height:1.8;
}

.features{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:10px;
  margin:25px 0;
}

.feature{
  padding:13px;
  border:1px solid var(--border);
  background:#0b0b0f;
  border-radius:11px;
  font-size:13px;
}

/* ROBLOX PROFILE */

.profile-top{
  display:flex;
  align-items:center;
  gap:15px;
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

.profile h3{
  font-size:21px;
}

.profile-name{
  color:var(--muted);
  font-size:13px;
}

.status{
  margin:25px 0 15px;
  padding:14px;
  border-radius:11px;
  background:rgba(34,197,94,.07);
  border:1px solid rgba(34,197,94,.18);
  color:#86efac;
  font-size:13px;
}

.loading{
  color:#facc15;
}

.error{
  color:#fca5a5;
  background:rgba(239,68,68,.07);
  border-color:rgba(239,68,68,.2);
}

/* CONTACT */

.contact{
  text-align:center;
  padding:75px 20px;
  background:
    radial-gradient(circle at center,rgba(139,92,246,.13),transparent 60%),
    #0b0b0f;
  border:1px solid var(--border);
  border-radius:25px;
}

.contact h2{
  font-size:45px;
  margin-bottom:10px;
}

.contact p{
  color:var(--muted);
  margin-bottom:28px;
}

/* APPEARANCE */

.panel{
  position:fixed;
  top:88px;
  right:18px;
  width:290px;
  padding:22px;
  background:rgba(12,12,16,.97);
  border:1px solid var(--border);
  border-radius:20px;
  z-index:2000;
  box-shadow:0 25px 80px rgba(0,0,0,.55);
  opacity:0;
  transform:translateY(-10px) scale(.98);
  pointer-events:none;
  transition:.2s;
}

.panel.active{
  opacity:1;
  transform:none;
  pointer-events:auto;
}

.panel p{
  color:var(--muted);
  font-size:12px;
  margin:5px 0 18px;
}

.colors{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:10px;
}

.color{
  height:46px;
  border-radius:11px;
  border:2px solid transparent;
  cursor:pointer;
}

.color:hover{
  transform:scale(1.08);
  border-color:#fff;
}

/* TOAST */

.toast{
  position:fixed;
  bottom:25px;
  left:50%;
  transform:translate(-50%,20px);
  opacity:0;
  pointer-events:none;
  background:#17171d;
  border:1px solid var(--border);
  padding:13px 18px;
  border-radius:12px;
  z-index:3000;
  transition:.25s;
  font-size:13px;
}

.toast.show{
  opacity:1;
  transform:translate(-50%,0);
}

/* FOOTER */

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

/* MOBILE */

@media(max-width:850px){

  .nav-links{
    display:none;
  }

  .categories,
  .products,
  .studio{
    grid-template-columns:1fr;
  }

  .hero{
    min-height:760px;
  }
}

@media(max-width:600px){

  .stats{
    flex-direction:column;
    gap:15px;
  }

  .features{
    grid-template-columns:1fr;
  }

  .panel{
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
    <a href="#categorias">Categorias</a>
    <a href="#scripts">Scripts</a>
    <a href="#studio">Studio</a>
    <a href="#contato">Contato</a>
  </div>

  <button class="icon-btn" onclick="togglePanel()">
    🎨
  </button>

</nav>

<!-- APPEARANCE -->

<div class="panel" id="panel">

  <h3>Editar aparência</h3>

  <p>Escolha a cor principal do site.</p>

  <div class="colors">

```
<button class="color" style="background:#8b5cf6"
  onclick="setColor('#8b5cf6','#6d28d9')"></button>

<button class="color" style="background:#fff"
  onclick="setColor('#fff','#ccc')"></button>

<button class="color" style="background:#2563eb"
  onclick="setColor('#2563eb','#1d4ed8')"></button>

<button class="color" style="background:#ef4444"
  onclick="setColor('#ef4444','#b91c1c')"></button>

<button class="color" style="background:#008cff"
  onclick="setColor('#008cff','#0066cc')"></button>

<button class="color" style="background:#06d6d6"
  onclick="setColor('#06d6d6','#0891b2')"></button>

<button class="color" style="background:#22c55e"
  onclick="setColor('#22c55e','#15803d')"></button>

<button class="color" style="background:#f97316"
  onclick="setColor('#f97316','#c2410c')"></button>
```

  </div>

</div>

<!-- HERO -->

<section class="hero" id="inicio">

  <div class="hero-glow"></div>

  <div class="hero-content">

```
<div class="badge">
  <span class="dot"></span>
  Loja de scripts para Roblox
</div>

<h1>
  Seus scripts.
  <span class="gradient">Seu jogo.</span>
</h1>

<p>
  Scripts, sistemas, painéis e soluções para
  projetos no Roblox Studio. Com opções de
  pagamento em Robux ou dinheiro.
</p>

<div class="buttons">

  <a href="#scripts" class="btn primary">
    🛒 Ver scripts
  </a>

  <a href="#personalizado" class="btn secondary">
    🔧 Script personalizado
  </a>

</div>

<div class="stats">

  <div class="stat">
    <strong>ROBLOX</strong>
    <span>Studio</span>
  </div>

  <div class="stat">
    <strong>ROBUX</strong>
    <span>Pagamento</span>
  </div>

  <div class="stat">
    <strong>R$</strong>
    <span>Pagamento</span>
  </div>

</div>
```

  </div>

</section>

<!-- CATEGORIAS -->

<section class="section" id="categorias">

  <div class="container">

```
<div class="heading">

  <small>Serviços</small>

  <h2>O que eu faço</h2>

  <p>
    Diferentes tipos de sistemas e scripts
    para projetos Roblox.
  </p>

</div>

<div class="categories">

  <div class="category">
    <div class="category-icon">🛡️</div>
    <h3>Painéis Admin</h3>
    <p>Interfaces administrativas para seu jogo.</p>
  </div>

  <div class="category">
    <div class="category-icon">⚙️</div>
    <h3>Sistemas</h3>
    <p>Sistemas personalizados para experiências.</p>
  </div>

  <div class="category">
    <div class="category-icon">🎮</div>
    <h3>Gameplay</h3>
    <p>Mecânicas e recursos para jogos.</p>
  </div>

  <div class="category">
    <div class="category-icon">🖥️</div>
    <h3>GUIs</h3>
    <p>Interfaces modernas e personalizadas.</p>
  </div>

  <div class="category">
    <div class="category-icon">💰</div>
    <h3>Economia</h3>
    <p>Moedas, lojas e sistemas econômicos.</p>
  </div>

  <div class="category">
    <div class="category-icon">👤</div>
    <h3>Jogadores</h3>
    <p>Sistemas relacionados aos jogadores.</p>
  </div>

  <div class="category">
    <div class="category-icon">🔧</div>
    <h3>Personalizados</h3>
    <p>Projetos feitos conforme sua necessidade.</p>
  </div>

  <div class="category">
    <div class="category-icon">🧩</div>
    <h3>Outros</h3>
    <p>Outros tipos de scripts sob consulta.</p>
  </div>

</div>
```

  </div>

</section>

<!-- PRODUTOS -->

<section class="section" id="scripts">

  <div class="container">

```
<div class="heading">

  <small>Loja</small>

  <h2>Scripts disponíveis</h2>

  <p>
    Escolha o produto e selecione a forma de pagamento.
  </p>

</div>

<div class="products">


  <!-- ADMIN -->

  <div class="product">

    <span class="tag">ADMIN</span>

    <h3>Painel Admin</h3>

    <p class="description">
      Painel administrativo para controlar
      recursos do seu jogo.
    </p>

    <div class="price">
      R$ 20,00
    </div>

    <a
      href="COLE_AQUI_SEU_LINK_DE_PAGAMENTO_1"
      target="_blank"
      class="btn buy money"
      onclick="checkPayment(event)">
      💰 Comprar com dinheiro
    </a>

    <a
      href="COLE_AQUI_SEU_GAMEPASS_1"
      target="_blank"
      class="btn buy robux"
      onclick="checkPayment(event)">
      🟩 Comprar com Robux
    </a>

  </div>


  <!-- PREMIUM -->

  <div class="product">

    <div class="popular">POPULAR</div>

    <span class="tag">PREMIUM</span>

    <h3>Sistema Premium</h3>

    <p class="description">
      Sistema completo para adicionar
      funcionalidades ao seu projeto.
    </p>

    <div class="price">
      R$ 35,00
    </div>

    <a
      href="COLE_AQUI_SEU_LINK_DE_PAGAMENTO_2"
      target="_blank"
      class="btn buy money"
      onclick="checkPayment(event)">
      💰 Comprar com dinheiro
    </a>

    <a
      href="COLE_AQUI_SEU_GAMEPASS_2"
      target="_blank"
      class="btn buy robux"
      onclick="checkPayment(event)">
      🟩 Comprar com Robux
    </a>

  </div>


  <!-- PRO -->

  <div class="product">

    <span class="tag">PRO</span>

    <h3>Script Pro</h3>

    <p class="description">
      Solução mais avançada para projetos
      que precisam de recursos personalizados.
    </p>

    <div class="price">
      R$ 60,00
    </div>

    <a
      href="COLE_AQUI_SEU_LINK_DE_PAGAMENTO_3"
      target="_blank"
      class="btn buy money"
      onclick="checkPayment(event)">
      💰 Comprar com dinheiro
    </a>

    <a
      href="COLE_AQUI_SEU_GAMEPASS_3"
      target="_blank"
      class="btn buy robux"
      onclick="checkPayment(event)">
      🟩 Comprar com Robux
    </a>

  </div>

</div>
```

  </div>

</section>

<!-- PERSONALIZADO -->

<section class="section" id="personalizado">

  <div class="container">

```
<div class="custom-box">

  <h2>🔧 Precisa de algo personalizado?</h2>

  <p>
    Se você precisa de um painel, sistema, GUI,
    mecânica ou outro script específico, entre em
    contato para explicar o que deseja.
  </p>

  <a
    href="https://www.tiktok.com/@Vinlumezx00"
    target="_blank"
    class="btn primary">
    🎵 Solicitar pelo TikTok
  </a>

</div>
```

  </div>

</section>

<!-- STUDIO + ROBLOX -->

<section class="section" id="studio">

  <div class="container">

```
<div class="heading">

  <small>Desenvolvimento</small>

  <h2>Roblox Studio</h2>

  <p>
    Ferramentas e scripts para seus projetos.
  </p>

</div>


<div class="studio">

  <div class="studio-card">

    <h3>🎮 Crie seu jogo</h3>

    <p>
      Roblox Studio permite criar mapas,
      sistemas, interfaces, scripts e
      experiências completas.
    </p>

    <div class="features">

      <div class="feature">⚙️ Sistemas</div>
      <div class="feature">🧩 Scripts</div>
      <div class="feature">🌎 Mapas</div>
      <div class="feature">🎨 Interfaces</div>

    </div>

    <a
      href="https://create.roblox.com/"
      target="_blank"
      class="btn primary">
      Abrir Roblox Studio
    </a>

  </div>


  <!-- PERFIL -->

  <div class="profile">

    <div class="profile-top">

      <div class="avatar">
        V
      </div>

      <div>

        <h3 id="robloxName">
          eyeywtwywywy
        </h3>

        <div class="profile-name">
          Conta Roblox
        </div>

      </div>

    </div>

    <div class="status loading" id="robloxStatus">
      🔎 Localizando conta Roblox...
    </div>

    <a
      id="robloxProfile"
      href="https://www.roblox.com/search/users?keyword=eyeywtwywywy"
      target="_blank"
      class="btn secondary">
      🎮 Abrir perfil Roblox
    </a>

  </div>

</div>
```

  </div>

</section>

<!-- CONTATO -->

<section class="section" id="contato">

  <div class="container">

```
<div class="contact">

  <h2>Entre em contato</h2>

  <p>
    Fale comigo pelo TikTok ou veja minha conta Roblox.
  </p>

  <div class="buttons">

    <a
      href="https://www.tiktok.com/@Vinlumezx00"
      target="_blank"
      class="btn primary">
      🎵 TikTok @Vinlumezx00
    </a>

    <a
      id="contactRoblox"
      href="https://www.roblox.com/search/users?keyword=eyeywtwywywy"
      target="_blank"
      class="btn secondary">
      🎮 Roblox eyeywtwywywy
    </a>

  </div>

</div>
```

  </div>

</section>

<footer>

© 2026 <strong>Roblox Scripts</strong>
• Scripts, sistemas e soluções para Roblox Studio

</footer>

<div class="toast" id="toast"></div>

<script>

/* ================= APARÊNCIA ================= */

const root=document.documentElement;

function togglePanel(){

  document
    .getElementById("panel")
    .classList.toggle("active");

}

function setColor(primary,primary2){

  root.style.setProperty("--primary",primary);
  root.style.setProperty("--primary2",primary2);

  localStorage.setItem("primary",primary);
  localStorage.setItem("primary2",primary2);

  toast("Aparência atualizada!");

}

const savedPrimary=localStorage.getItem("primary");
const savedPrimary2=localStorage.getItem("primary2");

if(savedPrimary && savedPrimary2){

  root.style.setProperty("--primary",savedPrimary);
  root.style.setProperty("--primary2",savedPrimary2);

}


/* ================= TOAST ================= */

let toastTimer;

function toast(message){

  const box=document.getElementById("toast");

  box.textContent=message;
  box.classList.add("show");

  clearTimeout(toastTimer);

  toastTimer=setTimeout(()=>{
    box.classList.remove("show");
  },2500);

}


/* ================= PAGAMENTO ================= */

function checkPayment(event){

  const link=event.currentTarget.getAttribute("href");

  if(
    !link ||
    link.startsWith("COLE_AQUI")
  ){

    event.preventDefault();

    toast(
      "Esse link de pagamento ainda não foi configurado."
    );

  }

}


/* ================= ROBLOX ================= */

/*
  Nome da conta:
  eyeywtwywywy

  O Roblox possui um endpoint público que
  permite obter usuários por nome de usuário.
*/

async function findRobloxUser(){

  const username="eyeywtwywywy";

  const status=document.getElementById("robloxStatus");
  const name=document.getElementById("robloxName");
  const profile=document.getElementById("robloxProfile");
  const contact=document.getElementById("contactRoblox");

  try{

    const response=await fetch(
      "https://users.roblox.com/v1/usernames/users",
      {
        method:"POST",
        headers:{
          "Content-Type":"application/json"
        },
        body:JSON.stringify({
          usernames:[username],
          excludeBannedUsers:false
        })
      }
    );

    if(!response.ok){
      throw new Error("API");
    }

    const data=await response.json();

    if(data.data && data.data.length>0){

      const user=data.data[0];

      name.textContent=user.name;

      status.className="status";

      status.style.color="#86efac";

      status.textContent=
        "✓ Conta encontrada no Roblox";

      const url=
        "https://www.roblox.com/users/"
        + user.id
        + "/profile";

      profile.href=url;
      contact.href=url;

    }else{

      status.className="status error";

      status.textContent=
        "Não foi possível localizar esse nome.";

    }

  }catch(error){

    status.className="status error";

    status.textContent=
      "Não foi possível consultar o Roblox agora.";

  }

}

findRobloxUser();


/* ================= FECHAR PAINEL ================= */

document.addEventListener("click",(event)=>{

  const panel=document.getElementById("panel");
  const button=document.querySelector(".icon-btn");

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
