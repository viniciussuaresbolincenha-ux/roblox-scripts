<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BOT LAB</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: Arial, Helvetica, sans-serif;
    background:
        radial-gradient(circle at top left, #172554, transparent 35%),
        radial-gradient(circle at bottom right, #312e81, transparent 35%),
        #050816;
    color: white;
}

header {
    padding: 30px;
    border-bottom: 1px solid #263252;
    background: rgba(5, 8, 22, .75);
    backdrop-filter: blur(12px);
}

.logo {
    font-size: 32px;
    font-weight: 900;
    letter-spacing: 3px;
}

.logo span {
    color: #38bdf8;
}

.subtitle {
    color: #94a3b8;
    margin-top: 8px;
}

.container {
    max-width: 1200px;
    margin: auto;
    padding: 25px;
}

.grid {
    display: grid;
    grid-template-columns: 350px 1fr;
    gap: 20px;
}

.card {
    background: rgba(15, 23, 42, .85);
    border: 1px solid #263252;
    border-radius: 18px;
    padding: 22px;
    box-shadow: 0 20px 50px rgba(0,0,0,.25);
}

h2 {
    margin-top: 0;
}

label {
    display: block;
    margin-top: 22px;
    color: #cbd5e1;
}

input[type="range"] {
    width: 100%;
    margin-top: 12px;
    accent-color: #38bdf8;
}

.value {
    float: right;
    color: #38bdf8;
    font-weight: bold;
}

button {
    width: 100%;
    margin-top: 18px;
    padding: 14px;
    border: 0;
    border-radius: 10px;
    background: #38bdf8;
    color: #03111c;
    font-weight: 900;
    cursor: pointer;
    transition: .2s;
}

button:hover {
    transform: translateY(-2px);
    filter: brightness(1.1);
}

button.stop {
    background: #334155;
    color: white;
}

.status {
    display: inline-block;
    padding: 7px 12px;
    border-radius: 20px;
    background: #334155;
    color: #cbd5e1;
    font-size: 12px;
    font-weight: bold;
}

.status.running {
    background: #064e3b;
    color: #6ee7b7;
}

.stats {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
}

.stat {
    padding: 18px;
    background: #080d1d;
    border: 1px solid #1e293b;
    border-radius: 13px;
}

.stat small {
    color: #64748b;
}

.stat strong {
    display: block;
    margin-top: 8px;
    font-size: 27px;
}

canvas {
    width: 100%;
    height: 280px;
    margin-top: 20px;
    background: #070b17;
    border-radius: 14px;
}

.bot-area {
    position: relative;
    height: 280px;
    overflow: hidden;
    margin-top: 20px;
    background: #070b17;
    border-radius: 14px;
    border: 1px solid #1e293b;
}

.bot {
    position: absolute;
    width: 9px;
    height: 9px;
    border-radius: 50%;
    background: #38bdf8;
    box-shadow: 0 0 12px #38bdf8;
}

.target {
    position: absolute;
    right: 25px;
    top: 50%;
    transform: translateY(-50%);
    width: 55px;
    height: 55px;
    border-radius: 50%;
    border: 2px solid #a78bfa;
    box-shadow: 0 0 30px #7c3aed;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 10px;
    color: #c4b5fd;
}

.log {
    height: 150px;
    overflow: auto;
    padding: 15px;
    background: #030712;
    border-radius: 10px;
    font-family: monospace;
    font-size: 12px;
    color: #86efac;
}

.warning {
    margin-top: 15px;
    padding: 12px;
    border-radius: 10px;
    background: #1e293b;
    color: #94a3b8;
    font-size: 12px;
    line-height: 1.5;
}

@media(max-width: 800px) {
    .grid {
        grid-template-columns: 1fr;
    }

    .stats {
        grid-template-columns: repeat(2, 1fr);
    }
}
</style>
</head>

<body>

<header>
    <div class="logo">BOT<span>LAB</span></div>
    <div class="subtitle">
        Simulador visual de bots • laboratório local
    </div>
</header>

<div class="container">

<div class="grid">

<!-- CONTROLES -->

<div class="card">

    <h2>Controle</h2>

    <div id="status" class="status">
        ● PARADO
    </div>

    <label>
        Quantidade de bots
        <span id="botValue" class="value">50</span>
    </label>

    <input
        id="botCount"
        type="range"
        min="1"
        max="250"
        value="50"
    >

    <label>
        Intensidade
        <span id="intensityValue" class="value">10</span>
    </label>

    <input
        id="intensity"
        type="range"
        min="1"
        max="50"
        value="10"
    >

    <button onclick="startSimulation()">
        ▶ INICIAR SIMULAÇÃO
    </button>

    <button class="stop" onclick="stopSimulation()">
        ■ PARAR
    </button>

    <div class="warning">
        ⚠️ Os bots deste projeto são apenas objetos virtuais
        executados pelo navegador. Nenhum tráfego é enviado
        para computadores, sites ou IPs externos.
    </div>

</div>

<!-- PAINEL -->

<div class="card">

    <h2>Telemetria</h2>

    <div class="stats">

        <div class="stat">
            <small>BOTS</small>
            <strong id="bots">0</strong>
        </div>

        <div class="stat">
            <small>REQUESTS</small>
            <strong id="requests">0</strong>
        </div>

        <div class="stat">
            <small>ACEITAS</small>
            <strong id="accepted">0</strong>
        </div>

        <div class="stat">
            <small>BLOQUEADAS</small>
            <strong id="blocked">0</strong>
        </div>

    </div>

    <canvas id="chart"></canvas>

</div>

</div>

<!-- VISUALIZAÇÃO -->

<div class="card">

    <h2>Mapa dos Bots</h2>

    <div id="botArea" class="bot-area">

        <div class="target">
            LAB
        </div>

    </div>

</div>

<!-- LOG -->

<div class="card">

    <h2>Eventos</h2>

    <div id="log" class="log">
        [SYSTEM] Bot Lab iniciado.
    </div>

</div>

</div>

<script>

let running = false;

let botCount = 50;
let intensity = 10;

let requests = 0;
let accepted = 0;
let blocked = 0;

let bots = [];

const botInput = document.getElementById("botCount");
const intensityInput = document.getElementById("intensity");

const botValue = document.getElementById("botValue");
const intensityValue = document.getElementById("intensityValue");

const botArea = document.getElementById("botArea");

const status = document.getElementById("status");

const canvas = document.getElementById("chart");
const ctx = canvas.getContext("2d");

const history = [];


/* CONTROLES */

botInput.addEventListener("input", () => {

    botCount = Number(botInput.value);

    botValue.textContent = botCount;

    createBots();

});


intensityInput.addEventListener("input", () => {

    intensity = Number(intensityInput.value);

    intensityValue.textContent = intensity;

});


/* CRIAR BOTS */

function createBots() {

    bots.forEach(bot => bot.remove());

    bots = [];

    for(let i = 0; i < botCount; i++) {

        const bot = document.createElement("div");

        bot.className = "bot";

        bot.style.left =
            Math.random() * 75 + "%";

        bot.style.top =
            Math.random() * 90 + "%";

        bot.dataset.x =
            parseFloat(bot.style.left);

        bot.dataset.y =
            parseFloat(bot.style.top);

        botArea.appendChild(bot);

        bots.push(bot);
    }
}


/* LOG */

function log(message) {

    const box = document.getElementById("log");

    const time =
        new Date().toLocaleTimeString();

    box.innerHTML =
        `[${time}] ${message}<br>` +
        box.innerHTML;

}


/* INICIAR */

function startSimulation() {

    if(running) return;

    running = true;

    status.textContent = "● RODANDO";

    status.classList.add("running");

    log(
        `Simulação iniciada com ${botCount} bots virtuais.`
    );

}


/* PARAR */

function stopSimulation() {

    running = false;

    status.textContent = "● PARADO";

    status.classList.remove("running");

    log("Simulação interrompida.");

}


/* SIMULAÇÃO */

function simulationLoop() {

    if(running) {

        const generated = intensity;

        requests += generated;

        const newBlocked =
            Math.floor(generated / 7);

        blocked += newBlocked;

        accepted +=
            generated - newBlocked;

        document.getElementById("bots").textContent =
            botCount;

        document.getElementById("requests").textContent =
            requests;

        document.getElementById("accepted").textContent =
            accepted;

        document.getElementById("blocked").textContent =
            blocked;

        history.push(
            requests === 0
            ? 0
            : (blocked / requests) * 100
        );

        if(history.length > 80) {
            history.shift();
        }

        moveBots();

        drawChart();

    }

    requestAnimationFrame(simulationLoop);
}


/* MOVIMENTO */

function moveBots() {

    bots.forEach(bot => {

        let x = Number(bot.dataset.x);
        let y = Number(bot.dataset.y);

        x += (80 - x) * 0.02;
        y += (50 - y) * 0.02;

        if(Math.abs(80 - x) < 1) {

            x = Math.random() * 75;
            y = Math.random() * 90;

        }

        bot.dataset.x = x;
        bot.dataset.y = y;

        bot.style.left = x + "%";
        bot.style.top = y + "%";

    });

}


/* GRÁFICO */

function drawChart() {

    const width =
        canvas.width =
        canvas.clientWidth * 2;

    const height =
        canvas.height =
        canvas.clientHeight * 2;

    ctx.clearRect(
        0,
        0,
        width,
        height
    );

    ctx.strokeStyle = "#1e293b";

    ctx.lineWidth = 2;

    for(let y = 40; y < height; y += 60) {

        ctx.beginPath();

        ctx.moveTo(0,y);

        ctx.lineTo(width,y);

        ctx.stroke();

    }

    if(history.length < 2)
        return;

    ctx.beginPath();

    ctx.strokeStyle = "#38bdf8";

    ctx.lineWidth = 5;

    history.forEach((value,index) => {

        const x =
            index /
            (history.length - 1) *
            width;

        const y =
            height -
            40 -
            (value / 100) *
            (height - 80);

        if(index === 0)
            ctx.moveTo(x,y);
        else
            ctx.lineTo(x,y);

    });

    ctx.stroke();

}


/* INICIALIZAÇÃO */

createBots();

simulationLoop();

</script>

</body>
</html>
