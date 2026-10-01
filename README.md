```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ROBLOX SCRIPTS</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

:root{
    --cor:#8b5cf6;
    --cor2:#6d28d9;
    --fundo:#050505;
    --card:#0b0b0b;
    --borda:#222;
    --texto:#fff;
    --cinza:#888;
}

html{
    scroll-behavior:smooth;
}

body{
    background:var(--fundo);
    color:var(--texto);
    font-family:Arial,Helvetica,sans-serif;
    transition:.3s;
}

a{
    text-decoration:none;
    color:inherit;
}

/* =========================
   MENU
========================= */

header{
    height:75px;
    padding:0 7%;

    display:flex;
    align-items:center;
    justify-content:space-between;

    background:rgba(5,5,5,.95);
    border-bottom:1px solid var(--borda);

    position:sticky;
    top:0;
    z-index:100;
    backdrop-filter:blur(15px);
}

.logo{
    font-size:20px;
    font-weight:900;
}

.logo span{
    color:var(--cor);
}

.menu{
    display:flex;
    align-items:center;
    gap:12px;
}

.nav-button,
.appearance-button{
    border:1px solid var(--borda);
    background:#0b0b0b;
    color:white;

    padding:11px 17px;

    font-size:11px;
    font-weight:bold;

    cursor:pointer;
    transition:.2s;
}

.nav-button:hover,
.appearance-button:hover{
    border-color:var(--cor);
    color:var(--cor);
}

/* =========================
   PAINEL DE APARÊNCIA
========================= */

.appearance-panel{
    position:fixed;

    top:85px;
    right:25px;

    width:270px;

    padding:22px;

    background:#0b0b0b;
    border:1px solid #292929;

    border-radius:12px;

    z-index:200;

    box-shadow:0 20px 60px rgba(0,0,0,.6);

    display:none;
}

.appearance-panel.active{
    display:block;
}

.appearance-panel h3{
    font-size:18px;
    margin-bottom:6px;
}

.appearance-panel p{
    color:#777;
    font-size:12px;
    margin-bottom:20px;
}

.colors{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:10px;
}

.color{
    height:45px;
    border-radius:8px;
    border:2px solid transparent;
    cursor:pointer;
    transition:.2s;
}

.color:hover{
    transform:scale(1.06);
    border-color:white;
}

.roxo{background:#8b5cf6;}
.branco{background:#f5f5f5;}
.azulescuro{background:#2563eb;}
.vermelho{background:#ef4444;}
.azul{background:#008cff;}
.ciano{background:#06d6d6;}
.verde{background:#22c55e;}
.laranja{background:#f97316;}

/* =========================
   HERO
========================= */

.hero{
    min-height:650px;

    padding:100px 7%;

    display:flex;
    align-items:center;

    position:relative;
    overflow:hidden;

    border-bottom:1px solid var(--borda);
}

.hero-content{
    max-width:760px;
    position:relative;
    z-index:2;
}

.tag{
    color:var(--cor);
    font-size:11px;
    font-weight:bold;
    letter-spacing:2px;
    margin-bottom:22px;
}

.hero h1{
    font-size:clamp(50px,8vw,95px);
    line-height:.94;
    letter-spacing:-5px;
    margin-bottom:28px;
}

.hero h1 span{
    color:var(--cor);
}

.hero p{
    max-width:620px;

    color:var(--cinza);

    font-size:17px;

    margin-bottom:35px;
}

.hero-buttons{
    display:flex;
    gap:12px;
    flex-wrap:wrap;
}

.primary-button{
    background:var(--cor);
    color:white;

    padding:15px 25px;

    font-size:12px;
    font-weight:bold;

    transition:.2s;
}

.primary-button:hover{
    background:var(--cor2);
}

.secondary-button{
    border:1px solid var(--borda);

    padding:15px 25px;

    font-size:12px;
    font-weight:bold;

    transition:.2s;
}

.secondary-button:hover{
    border-color:var(--cor);
    color:var(--cor);
}

.orb{
    position:absolute;

    right:-150px;
    top:50px;

    width:550px;
    height:550px;

    border-radius:50%;

    background:
    radial-gradient(
        circle,
        var(--cor) 0%,
        #111 30%,
        transparent 70%
    );

    opacity:.22;
}

/* =========================
   SEÇÕES
========================= */

section{
    padding:100px 7%;
    border-bottom:1px solid var(--borda);
}

.section-title{
    display:flex;
    align-items:center;
    gap:20px;

    margin-bottom:40px;
}

.section-title span{
    color:var(--cor);
    font-weight:bold;
}

.section-title h2{
    font-size:38px;
    letter-spacing:-2px;
}

/* =========================
   COMO FUNCIONA
========================= */

.steps{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.card{
    background:var(--card);

    border:1px solid var(--borda);

    padding:30px;

    min-height:240px;

    transition:.25s;
}

.card:hover{
    transform:translateY(-5px);
    border-color:var(--cor);
}

.number{
    color:var(--cor);

    font-size:12px;
    font-weight:bold;

    margin-bottom:40px;
}

.card h3{
    font-size:21px;
    margin-bottom:12px;
}

.card p{
    color:var(--cinza);
    font-size:14px;
}

/* =========================
   PRODUTOS
========================= */

.products-section{
    background:#070707;
}

.products{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.product{
    position:relative;

    background:var(--card);

    border:1px solid var(--borda);

    padding:30px;

    min-height:360px;

    transition:.25s;
}

.product:hover{
    transform:translateY(-5px);
    border-color:var(--cor);
}

.product.featured{
    border-color:var(--cor);
}

.featured-label{
    position:absolute;

    right:0;
    top:0;

    padding:7px 12px;

    background:var(--cor);
    color:white;

    font-size:9px;
    font-weight:bold;
}

.product-icon{
    width:50px;
    height:50px;

    display:grid;
    place-items:center;

    border:1px solid var(--borda);

    color:var(--cor);

    font-weight:bold;

    margin-bottom:28px;
}

.product-top{
    display:flex;
    justify-content:space-between;

    margin-bottom:10px;
}

.status{
    color:var(--cor);

    font-size:9px;
    font-weight:bold;
    letter-spacing:1px;
}

.price{
    font-weight:bold;
}

.product h3{
    font-size:25px;
    margin-bottom:12px;
}

.product p{
    color:var(--cinza);
    font-size:14px;
}

.buy-button{
    position:absolute;

    left:30px;
    right:30px;
    bottom:28px;

    padding:12px;

    text-align:center;

    border:1px solid var(--borda);

    font-size:10px;
    font-weight:bold;
    letter-spacing:1px;

    transition:.2s;
}

.buy-button:hover{
    background:var(--cor);
    border-color:var(--cor);
}

.note{
    color:#555;
    font-size:11px;
    margin-top:20px;
}

/* =========================
   INFORMAÇÕES
========================= */

.info-section{
    padding:60px 7%;

    display:grid;
    grid-template-columns:1fr 1fr;
    gap:18px;
}

.info-box{
    background:#090909;

    border:1px solid var(--borda);

    padding:28px;

    display:flex;
    gap:20px;
}

.info-icon{
    color:var(--cor);
    font-weight:bold;
}

.info-box h3{
    margin-bottom:7px;
}

.info-box p{
    color:var(--cinza);
    font-size:13px;
}

/* =========================
   CONTATO
========================= */

.contact{
    padding:110px 7%;

    display:flex;
    justify-content:space-between;
    align-items:center;

    gap:40px;

    background:#0b0b0b;
}

.contact h2{
    font-size:clamp(35px,5vw,65px);

    line-height:1;

    letter-spacing:-3px;

    margin-bottom:18px;
}

.contact p{
    color:var(--cinza);
}

.tiktok-button{
    white-space:nowrap;

    background:var(--cor);
    color:white;

    padding:18px 25px;

    font-size:11px;
    font-weight:bold;
    letter-spacing:1px;

    transition:.2s;
}

.tiktok-button:hover{
    background:var(--cor2);
}

.tiktok-button span{
    margin-left:15px;
}

/* =========================
   FOOTER
========================= */

footer{
    padding:30px 7%;

    display:flex;
    justify-content:space-between;

    color:#555;

    font-size:11px;
}

/* =========================
   CELULAR
========================= */

@media(max-width:800px){

    header{
        padding:0 5%;
    }

    .nav-button{
        display:none;
    }

    .hero{
        padding:90px 5%;
        min-height:580px;
    }

    .hero h1{
        letter-spacing:-3px;
    }

    section{
        padding:80px 5%;
    }

    .steps,
    .products,
    .info-section{
        grid-template-columns:1fr;
    }

    .contact,
    footer{
        flex-direction:column;
        align-items:flex-start;
    }

    .appearance-panel{
        right:15px;
        left:15px;
        width:auto;
    }
}

</style>
</head>


<body>


<!-- =========================
     MENU
========================= -->

<header>

    <div class="logo">
        ROBLOX<span> SCRIPTS</span>
    </div>

    <div class="menu">

        <button
            class="appearance-button"
            onclick="abrirAparencia()"
        >
            🎨 EDITAR APARÊNCIA
        </button>

        <a
            href="#produtos"
            class="nav-button"
        >
            VER SCRIPTS
        </a>

    </div>

</header>


<!-- =========================
     PAINEL DE CORES
========================= -->

<div
    id="appearancePanel"
    class="appearance-panel"
>

    <h3>
        Editar aparência
    </h3>

    <p>
        Escolha a cor principal do site.
    </p>

    <div class="colors">

        <div
            class="color roxo"
            onclick="mudarCor('#8b5cf6','#6d28d9')"
            title="Roxo"
        ></div>

        <div
            class="color branco"
            onclick="mudarCor('#ffffff','#cccccc')"
            title="Branco"
        ></div>

        <div
            class="color azulescuro"
            onclick="mudarCor('#2563eb','#1d4ed8')"
            title="Azul escuro"
        ></div>

        <div
            class="color vermelho"
            onclick="mudarCor('#ef4444','#b91c1c')"
            title="Vermelho"
        ></div>

        <div
            class="color azul"
            onclick="mudarCor('#008cff','#0066cc')"
            title="Azul"
        ></div>

        <div
            class="color ciano"
            onclick="mudarCor('#06d6d6','#0891b2')"
            title="Ciano"
        ></div>

        <div
            class="color verde"
            onclick="mudarCor('#22c55e','#15803d')"
            title="Verde"
        ></div>

        <div
            class="color laranja"
            onclick="mudarCor('#f97316','#c2410c')"
            title="Laranja"
        ></div>

    </div>

</div>


<!-- =========================
     HERO
========================= -->

<section class="hero">

    <div class="hero-content">

        <div class="tag">
            ⚡ SCRIPTS PARA ROBLOX STUDIO
        </div>

        <h1>
            Scripts para deixar<br>
            <span>seu jogo melhor.</span>
        </h1>

        <p>
            Encontre scripts para utilizar nos
            seus projetos do Roblox Studio,
            com explicações simples de instalação
            e utilização.
        </p>

        <div class="hero-buttons">

            <a
                href="#produtos"
                class="primary-button"
            >
                VER PRODUTOS
            </a>

            <a
                href="#como-funciona"
                class="secondary-button"
            >
                COMO FUNCIONA
            </a>

        </div>

    </div>

    <div class="orb"></div>

</section>


<!-- =========================
     COMO FUNCIONA
========================= -->

<section id="como-funciona">

    <div class="section-title">

        <span>01</span>

        <h2>
            Como funciona?
        </h2>

    </div>


    <div class="steps">

        <div class="card">

            <div class="number">
                01
            </div>

            <h3>
                Escolha seu script
            </h3>

            <p>
                Veja os scripts disponíveis na
                loja e escolha o que combina
                com o seu projeto no Roblox.
            </p>

        </div>


        <div class="card">

            <div class="number">
                02
            </div>

            <h3>
                Entre em contato
            </h3>

            <p>
                Clique no botão de contato e
                fale comigo pelo TikTok para
                saber como adquirir o script.
            </p>

        </div>


        <div class="card">

            <div class="number">
                03
            </div>

            <h3>
                Use no Roblox Studio
            </h3>

            <p>
                Depois de receber o produto,
                abra o Roblox Studio e siga
                as instruções fornecidas.
            </p>

        </div>

    </div>

</section>


<!-- =========================
     PRODUTOS
========================= -->

<section
    id="produtos"
    class="products-section"
>

    <div class="section-title">

        <span>02</span>

        <h2>
            Scripts disponíveis
        </h2>

    </div>


    <div class="products">


        <!-- PRODUTO 1 -->

        <div class="product">

            <div class="product-icon">
                &lt;/&gt;
            </div>

            <div class="product-top">

                <span class="status">
                    DISPONÍVEL
                </span>

                <span class="price">
                    R$ 10,00
                </span>

            </div>

            <h3>
                Script Básico
            </h3>

            <p>
                Um script para projetos
                iniciais no Roblox Studio.
            </p>

            <a
                href="#contato"
                class="buy-button"
            >
                COMPRAR / SABER MAIS
            </a>

        </div>


        <!-- PRODUTO 2 -->

        <div class="product featured">

            <div class="featured-label">
                DESTAQUE
            </div>

            <div class="product-icon">
                ⚙
            </div>

            <div class="product-top">

                <span class="status">
                    DISPONÍVEL
                </span>

                <span class="price">
                    R$ 20,00
                </span>

            </div>

            <h3>
                Script Premium
            </h3>

            <p>
                Uma opção mais completa
                para adicionar sistemas
                ao seu jogo.
            </p>

            <a
                href="#contato"
                class="buy-button"
            >
                COMPRAR / SABER MAIS
            </a>

        </div>


        <!-- PRODUTO 3 -->

        <div class="product">

            <div class="product-icon">
                ✦
            </div>

            <div class="product-top">

                <span class="status">
                    DISPONÍVEL
                </span>

                <span class="price">
                    R$ 30,00
                </span>

            </div>

            <h3>
                Script Pro
            </h3>

            <p>
                Para projetos que precisam
                de recursos mais avançados.
            </p>

            <a
                href="#contato"
                class="buy-button"
            >
                COMPRAR / SABER MAIS
            </a>

        </div>

    </div>


    <p class="note">
        * Edite os nomes, preços e descrições
        para colocar seus scripts reais.
    </p>

</section>


<!-- =========================
     INFORMAÇÕES
========================= -->

<section class="info-section">

    <div class="info-box">

        <div class="info-icon">
            ROBLOX
        </div>

        <div>

            <h3>
                Feito para Roblox Studio
            </h3>

            <p>
                Os scripts são destinados a
                projetos desenvolvidos no
                Roblox Studio. Leia as
                instruções antes de instalar.
            </p>

        </div>

    </div>


    <div class="info-box">

        <div class="info-icon">
            ✓
        </div>

        <div>

            <h3>
                Suporte
            </h3>

            <p>
                Ficou com alguma dúvida?
                Entre em contato pelo TikTok
                para conversar sobre os produtos.
            </p>

        </div>

    </div>

</section>


<!-- =========================
     CONTATO
========================= -->

<section
    id="contato"
    class="contact"
>

    <div>

        <div class="tag">
            CONTATO
        </div>

        <h2>
            Quer comprar ou<br>
            tirar uma dúvida?
        </h2>

        <p>
            Entre em contato pelo TikTok
            para saber mais sobre os scripts.
        </p>

    </div>


    <!-- SEU TIKTOK -->

    <a
        href="https://www.tiktok.com/@Vinlumezx00"
        target="_blank"
        rel="noopener noreferrer"
        class="tiktok-button"
    >

        ENTRAR EM CONTATO TIKTOK

        <span>
            ↗
        </span>

    </a>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <div>
        ROBLOX SCRIPTS
    </div>

    <p>
        © 2026 — Loja independente de scripts para Roblox Studio.
    </p>

</footer>


<!-- =========================
     JAVASCRIPT
========================= -->

<script>

function abrirAparencia(){

    const painel =
        document.getElementById("appearancePanel");

    painel.classList.toggle("active");

}


function mudarCor(cor, cor2){

    document.documentElement.style
        .setProperty("--cor", cor);

    document.documentElement.style
        .setProperty("--cor2", cor2);

    localStorage.setItem(
        "corPrincipal",
        cor
    );

    localStorage.setItem(
        "corSecundaria",
        cor2
    );

}


/* CARREGAR A COR SALVA */

const corSalva =
    localStorage.getItem("corPrincipal");

const corSecundaria =
    localStorage.getItem("corSecundaria");

if(corSalva){

    document.documentElement.style
        .setProperty("--cor", corSalva);

}

if(corSecundaria){

    document.documentElement.style
        .setProperty("--cor2", corSecundaria);

}


/* FECHAR PAINEL AO CLICAR FORA */

document.addEventListener(
    "click",
    function(event){

        const painel =
            document.getElementById(
                "appearancePanel"
            );

        const botao =
            document.querySelector(
                ".appearance-button"
            );

        if(
            painel.classList.contains("active") &&
            !painel.contains(event.target) &&
            !botao.contains(event.target)
        ){

            painel.classList.remove("active");

        }

    }
);

</script>

</body>
</html>
```
