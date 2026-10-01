<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ROBLOX SCRIPTS</title>

<style>
:root {
    --cor: #8b5cf6;
    --cor2: #6d28d9;
    --fundo: #050505;
    --card: #0c0c0c;
    --borda: #242424;
    --texto: #ffffff;
    --cinza: #999999;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background: var(--fundo);
    color: var(--texto);
}

header {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(5, 5, 5, 0.95);
    border-bottom: 1px solid var(--borda);
    backdrop-filter: blur(10px);
}

.navbar {
    max-width: 1200px;
    margin: auto;
    padding: 18px 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
}

.logo {
    font-size: 22px;
    font-weight: 900;
}

.logo span {
    color: var(--cor);
}

.nav-buttons {
    display: flex;
    gap: 10px;
    align-items: center;
}

button,
.button {
    border: none;
    cursor: pointer;
    text-decoration: none;
}

.appearance-button {
    background: #111;
    color: white;
    border: 1px solid var(--borda);
    padding: 11px 15px;
    border-radius: 8px;
    transition: 0.2s;
}

.appearance-button:hover {
    border-color: var(--cor);
    color: var(--cor);
}

.hero {
    min-height: 650px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 80px 20px;
    background:
        radial-gradient(circle at center, rgba(139,92,246,0.16), transparent 40%),
        var(--fundo);
}

.hero-content {
    max-width: 850px;
}

.tag {
    color: var(--cor);
    font-weight: bold;
    margin-bottom: 18px;
}

.hero h1 {
    font-size: clamp(42px, 8vw, 80px);
    line-height: 0.95;
    margin-bottom: 25px;
}

.hero h1 span {
    color: var(--cor);
}

.hero p {
    color: var(--cinza);
    font-size: 18px;
    line-height: 1.7;
    margin-bottom: 35px;
}

.main-button {
    display: inline-block;
    background: linear-gradient(135deg, var(--cor), var(--cor2));
    color: white;
    padding: 15px 25px;
    border-radius: 9px;
    font-weight: bold;
    box-shadow: 0 0 30px rgba(139,92,246,0.2);
    transition: 0.2s;
}

.main-button:hover {
    transform: translateY(-3px);
}

section {
    max-width: 1200px;
    margin: auto;
    padding: 80px 20px;
}

.section-title {
    text-align: center;
    margin-bottom: 45px;
}

.section-title h2 {
    font-size: 38px;
    margin-bottom: 12px;
}

.section-title p {
    color: var(--cinza);
}

.cards {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.card {
    background: var(--card);
    border: 1px solid var(--borda);
    border-radius: 14px;
    padding: 30px;
    transition: 0.25s;
}

.card:hover {
    transform: translateY(-5px);
    border-color: var(--cor);
}

.icon {
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(139,92,246,0.12);
    color: var(--cor);
    border-radius: 10px;
    font-size: 23px;
    margin-bottom: 20px;
}

.card h3 {
    margin-bottom: 12px;
}

.card p {
    color: var(--cinza);
    line-height: 1.6;
}

.products {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.product {
    background: var(--card);
    border: 1px solid var(--borda);
    border-radius: 14px;
    padding: 25px;
    position: relative;
}

.product.featured {
    border-color: var(--cor);
    box-shadow: 0 0 35px rgba(139,92,246,0.12);
}

.badge {
    position: absolute;
    right: 15px;
    top: 15px;
    background: var(--cor);
    color: white;
    padding: 6px 9px;
    border-radius: 5px;
    font-size: 11px;
    font-weight: bold;
}

.product h3 {
    font-size: 22px;
    margin-bottom: 12px;
}

.price {
    font-size: 30px;
    font-weight: bold;
    margin: 20px 0;
    color: var(--cor);
}

.product ul {
    list-style: none;
    margin-bottom: 25px;
}

.product li {
    color: var(--cinza);
    margin: 10px 0;
}

.product li::before {
    content: "✓";
    color: var(--cor);
    margin-right: 8px;
}

.product-button {
    display: block;
    text-align: center;
    padding: 12px;
    border-radius: 7px;
    border: 1px solid var(--cor);
    color: white;
    text-decoration: none;
    transition: 0.2s;
}

.product-button:hover {
    background: var(--cor);
}

.info-box {
    background: var(--card);
    border: 1px solid var(--borda);
    border-radius: 14px;
    padding: 35px;
    line-height: 1.8;
}

.info-box strong {
    color: var(--cor);
}

.contact {
    text-align: center;
}

.tiktok-button {
    display: inline-flex;
    gap: 15px;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--cor), var(--cor2));
    color: white;
    text-decoration: none;
    padding: 16px 25px;
    border-radius: 9px;
    font-weight: bold;
    margin-top: 20px;
    transition: 0.2s;
}

.tiktok-button:hover {
    transform: translateY(-3px);
}

footer {
    border-top: 1px solid var(--borda);
    text-align: center;
    padding: 30px 20px;
    color: var(--cinza);
}

/* PAINEL DE APARÊNCIA */

.appearance-panel {
    position: fixed;
    top: 75px;
    right: 20px;
    width: 280px;
    background: #0c0c0c;
    border: 1px solid var(--borda);
    border-radius: 14px;
    padding: 22px;
    z-index: 2000;
    box-shadow: 0 15px 50px rgba(0,0,0,0.5);

    opacity: 0;
    visibility: hidden;
    transform: translateY(-10px);
    transition: 0.2s;
}

.appearance-panel.active {
    opacity: 1;
    visibility: visible;
    transform: translateY(0);
}

.appearance-panel h3 {
    margin-bottom: 8px;
}

.appearance-panel p {
    color: var(--cinza);
    font-size: 14px;
    margin-bottom: 20px;
}

.colors {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
}

.color {
    height: 42px;
    border-radius: 8px;
    cursor: pointer;
    border: 2px solid #333;
    transition: 0.2s;
}

.color:hover {
    transform: scale(1.08);
    border-color: white;
}

.roxo { background: #8b5cf6; }
.branco { background: #ffffff; }
.azulescuro { background: #2563eb; }
.vermelho { background: #ef4444; }
.azul { background: #008cff; }
.ciano { background: #06d6d6; }
.verde { background: #22c55e; }
.laranja { background: #f97316; }

@media (max-width: 800px) {
    .cards,
    .products {
        grid-template-columns: 1fr;
    }

    .navbar {
        flex-direction: column;
    }

    .hero {
        min-height: 550px;
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

<header>
    <div class="navbar">

        <div class="logo">
            ROBLOX<span> SCRIPTS</span>
        </div>

        <div class="nav-buttons">
            <button class="appearance-button" onclick="abrirAparencia()">
                🎨 EDITAR APARÊNCIA
            </button>
        </div>

    </div>
</header>

<!-- PAINEL DE CORES -->

<div id="appearancePanel" class="appearance-panel">

    <h3>Editar aparência</h3>

    <p>
        Escolha a cor principal do site.
    </p>

    <div class="colors">

        <div class="color roxo"
             onclick="mudarCor('#8b5cf6','#6d28d9')"
             title="Roxo"></div>

        <div class="color branco"
             onclick="mudarCor('#ffffff','#cccccc')"
             title="Branco"></div>

        <div class="color azulescuro"
             onclick="mudarCor('#2563eb','#1d4ed8')"
             title="Azul escuro"></div>

        <div class="color vermelho"
             onclick="mudarCor('#ef4444','#b91c1c')"
             title="Vermelho"></div>

        <div class="color azul"
             onclick="mudarCor('#008cff','#0066cc')"
             title="Azul"></div>

        <div class="color ciano"
             onclick="mudarCor('#06d6d6','#0891b2')"
             title="Ciano"></div>

        <div class="color verde"
             onclick="mudarCor('#22c55e','#15803d')"
             title="Verde"></div>

        <div class="color laranja"
             onclick="mudarCor('#f97316','#c2410c')"
             title="Laranja"></div>

    </div>

</div>

<!-- HERO -->

<section class="hero">

    <div class="hero-content">

        <div class="tag">
            ⚡ SCRIPTS PARA ROBLOX STUDIO
        </div>

        <h1>
            Scripts para deixar<br>
            seu jogo <span>melhor.</span>
        </h1>

        <p>
            Encontre scripts para utilizar nos seus projetos
            do Roblox Studio, com explicações simples de
            instalação e utilização.
        </p>

        <a href="#scripts" class="main-button">
            VER SCRIPTS
        </a>

    </div>

</section>

<!-- COMO FUNCIONA -->

<section>

    <div class="section-title">

        <h2>Como funciona?</h2>

        <p>
            Comprar e utilizar seus scripts é simples.
        </p>

    </div>

    <div class="cards">

        <div class="card">

            <div class="icon">🛒</div>

            <h3>1. Escolha seu script</h3>

            <p>
                Veja os scripts disponíveis e escolha
                aquele que combina com seu projeto.
            </p>

        </div>

        <div class="card">

            <div class="icon">💬</div>

            <h3>2. Entre em contato</h3>

            <p>
                Entre em contato pelo TikTok para
                tirar dúvidas e combinar a compra.
            </p>

        </div>

        <div class="card">

            <div class="icon">🎮</div>

            <h3>3. Use no Roblox Studio</h3>

            <p>
                Depois da compra, utilize o script
                no seu projeto dentro do Roblox Studio.
            </p>

        </div>

    </div>

</section>

<!-- SCRIPTS -->

<section id="scripts">

    <div class="section-title">

        <h2>Scripts disponíveis</h2>

        <p>
            Escolha o script que deseja adquirir.
        </p>

    </div>

    <div class="products">

        <div class="product">

            <h3>Script Básico</h3>

            <p>
                Uma opção para projetos simples.
            </p>

            <div class="price">
                R$ 10,00
            </div>

            <ul>
                <li>Script para Roblox</li>
                <li>Instruções de instalação</li>
                <li>Suporte básico</li>
            </ul>

            <a href="#contato" class="product-button">
                TENHO INTERESSE
            </a>

        </div>

        <div class="product featured">

            <div class="badge">
                POPULAR
            </div>

            <h3>Script Premium</h3>

            <p>
                Mais recursos para seu projeto.
            </p>

            <div class="price">
                R$ 20,00
            </div>

            <ul>
                <li>Script para Roblox</li>
                <li>Mais recursos</li>
                <li>Instruções completas</li>
                <li>Suporte</li>
            </ul>

            <a href="#contato" class="product-button">
                TENHO INTERESSE
            </a>

        </div>

        <div class="product">

            <h3>Script Pro</h3>

            <p>
                Para projetos que precisam de mais recursos.
            </p>

            <div class="price">
                R$ 30,00
            </div>

            <ul>
                <li>Script avançado</li>
                <li>Instruções</li>
                <li>Suporte</li>
                <li>Atualizações</li>
            </ul>

            <a href="#contato" class="product-button">
                TENHO INTERESSE
            </a>

        </div>

    </div>

</section>

<!-- ROBLOX STUDIO -->

<section>

    <div class="section-title">

        <h2>Roblox Studio</h2>

        <p>
            Onde você pode utilizar seus scripts.
        </p>

    </div>

    <div class="info-box">

        <p>
            O <strong>Roblox Studio</strong> é a ferramenta
            utilizada para criar e editar experiências no Roblox.
        </p>

        <br>

        <p>
            Os scripts desta loja são destinados aos
            <strong>seus próprios projetos</strong>.
            Depois de adquirir um script, você poderá
            adicioná-lo ao seu jogo seguindo as instruções
            fornecidas.
        </p>

        <br>

        <p>
            Sempre teste os scripts no seu próprio projeto
            antes de publicar sua experiência.
        </p>

    </div>

</section>

<!-- CONTATO -->

<section id="contato" class="contact">

    <div class="section-title">

        <h2>Quer comprar um script?</h2>

        <p>
            Entre em contato pelo TikTok para saber mais.
        </p>

        <a
            href="https://www.tiktok.com/@Vinlumezx00"
            target="_blank"
            rel="noopener noreferrer"
            class="tiktok-button"
        >
            ENTRAR EM CONTATO TIKTOK
            <span>↗</span>
        </a>

    </div>

</section>

<footer>

    © 2026 Roblox Scripts — Todos os direitos reservados.

</footer>

<script>

function abrirAparencia() {

    const painel =
        document.getElementById("appearancePanel");

    painel.classList.toggle("active");
}


function mudarCor(cor, cor2) {

    document.documentElement
        .style.setProperty("--cor", cor);

    document.documentElement
        .style.setProperty("--cor2", cor2);

    localStorage.setItem(
        "corPrincipal",
        cor
    );

    localStorage.setItem(
        "corSecundaria",
        cor2
    );
}


// CARREGAR COR SALVA

const corSalva =
    localStorage.getItem("corPrincipal");

const corSecundaria =
    localStorage.getItem("corSecundaria");

if (corSalva) {

    document.documentElement
        .style.setProperty(
            "--cor",
            corSalva
        );
}

if (corSecundaria) {

    document.documentElement
        .style.setProperty(
            "--cor2",
            corSecundaria
        );
}


// FECHAR PAINEL AO CLICAR FORA

document.addEventListener(
    "click",
    function(event) {

        const painel =
            document.getElementById(
                "appearancePanel"
            );

        const botao =
            document.querySelector(
                ".appearance-button"
            );

        if (
            painel.classList.contains("active") &&
            !painel.contains(event.target) &&
            !botao.contains(event.target)
        ) {

            painel.classList.remove("active");

        }

    }
);

</script>

</body>
</html>
