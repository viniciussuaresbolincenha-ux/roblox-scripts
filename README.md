<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Lumex Forge | Scripts para Roblox Studio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;900&display=swap" rel="stylesheet">
<style>
:root{--bg:#0a0a0b;--card:#131316;--line:#26262c;--txt:#f2f2f3;--mut:#8b8b95;--gold:#d4af37;--gold2:#f5d77a;--tint:color-mix(in srgb,var(--gold) 12%,#0a0a0b);--tint2:color-mix(in srgb,var(--gold) 30%,#0a0a0b)}
[data-theme=azul]{--gold:#3b9eff;--gold2:#8ccbff}
[data-theme=roxo]{--gold:#9b6bff;--gold2:#c9b0ff}
[data-theme=verde]{--gold:#2fd18b;--gold2:#8cf0c3}
[data-theme=rosa]{--gold:#ff5fa2;--gold2:#ffa6cc}
[data-theme=vermelho]{--gold:#ff4d4d;--gold2:#ff9c9c}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--txt);font-family:Inter,system-ui,sans-serif;line-height:1.55}
a{color:inherit;text-decoration:none}
.wrap{max-width:1120px;margin:0 auto;padding:0 20px}
nav{position:sticky;top:0;z-index:20;background:rgba(10,10,11,.85);backdrop-filter:blur(12px);border-bottom:1px solid var(--line)}
nav .wrap{display:flex;align-items:center;justify-content:space-between;height:64px}
.logo{font-weight:900;letter-spacing:.18em;font-size:20px}
.logo span{color:var(--gold);margin-left:2px}
nav ul{display:flex;gap:24px;list-style:none;font-size:14px;color:var(--mut)}
nav ul a:hover{color:var(--txt)}
.hero{padding:96px 0 72px;text-align:center;background:radial-gradient(ellipse at top,var(--tint) 0,transparent 60%)}
.badge{display:inline-block;border:1px solid var(--gold);color:var(--gold2);border-radius:99px;padding:5px 14px;font-size:12px;letter-spacing:.1em;margin-bottom:22px}
.hero h1{font-size:clamp(36px,6vw,64px);font-weight:900;line-height:1.1;letter-spacing:-.02em}
.hero h1 em{font-style:normal;background:linear-gradient(90deg,var(--gold),var(--gold2));-webkit-background-clip:text;background-clip:text;color:transparent}
.hero p{max-width:560px;margin:20px auto 32px;color:var(--mut);font-size:17px}
.btn{display:inline-block;border:0;cursor:pointer;font:600 15px Inter,sans-serif;padding:13px 26px;border-radius:10px;transition:.18s}
.btn.gold{background:linear-gradient(90deg,var(--gold),var(--gold2));color:#111}
.btn.gold:hover{transform:translateY(-2px);box-shadow:0 8px 24px color-mix(in srgb,var(--gold) 35%,transparent)}
.btn.line{background:transparent;border:1px solid var(--line);color:var(--txt)}
.btn.line:hover{border-color:var(--gold);color:var(--gold2)}
.stats{display:flex;justify-content:center;gap:48px;margin-top:52px;flex-wrap:wrap}
.stats b{display:block;font-size:28px;color:var(--gold2)}
.stats small{color:var(--mut);font-size:13px}
section{padding:64px 0}
h2{font-size:30px;font-weight:700;margin-bottom:8px}
.sub{color:var(--mut);margin-bottom:28px}
.tools{display:flex;gap:12px;flex-wrap:wrap;align-items:center;margin-bottom:28px}
.tools input{flex:1;min-width:200px;background:var(--card);border:1px solid var(--line);border-radius:10px;padding:12px 16px;color:var(--txt);font:inherit}
.tools input:focus{outline:none;border-color:var(--gold)}
.chips{display:flex;gap:8px;flex-wrap:wrap}
.chip{background:var(--card);border:1px solid var(--line);color:var(--mut);border-radius:99px;padding:8px 16px;font:500 13px Inter,sans-serif;cursor:pointer;transition:.15s}
.chip:hover{color:var(--txt)}
.chip.on{background:var(--gold);border-color:var(--gold);color:#111;font-weight:700}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(min(100%,300px),1fr));gap:20px}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:22px;display:flex;flex-direction:column;transition:.2s}
.card:hover{border-color:var(--gold);transform:translateY(-4px)}
.ico{width:48px;height:48px;border-radius:12px;background:var(--tint);border:1px solid var(--tint2);display:grid;place-items:center;font-size:24px;margin-bottom:14px}
.card h3{font-size:18px;margin-bottom:6px}
.card p{color:var(--mut);font-size:14px;flex:1}
.tags{display:flex;gap:6px;flex-wrap:wrap;margin:14px 0}
.tags span{font-size:11px;color:var(--gold2);background:var(--tint);border-radius:6px;padding:3px 8px}
.price{display:flex;justify-content:space-between;align-items:baseline;margin-bottom:14px}
.price b{font-size:22px}
.price i{font-style:normal;color:var(--gold2);font-weight:600}
.card .btn{width:100%}
.empty{grid-column:1/-1;text-align:center;color:var(--mut);padding:40px}
.how{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:20px}
.step{border-left:2px solid var(--gold);padding:4px 0 4px 18px}
.step b{display:block;margin-bottom:4px}
.step span{color:var(--mut);font-size:14px}
.faq details{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:16px 20px;margin-bottom:10px}
.faq summary{cursor:pointer;font-weight:600}
.faq p{color:var(--mut);margin-top:10px;font-size:14px}
.cta{text-align:center;background:linear-gradient(135deg,var(--tint),#0f0f11);border:1px solid var(--tint2);border-radius:20px;padding:56px 24px}
footer{border-top:1px solid var(--line);padding:28px 0;text-align:center;color:var(--mut);font-size:13px}
.modal{position:fixed;inset:0;background:rgba(0,0,0,.7);backdrop-filter:blur(4px);display:none;place-items:center;z-index:50;padding:20px}
.modal.open{display:grid}
.box{background:var(--card);border:1px solid var(--line);border-radius:18px;padding:28px;max-width:420px;width:100%}
.box h3{font-size:20px;margin-bottom:4px}
.box p{color:var(--mut);font-size:14px;margin-bottom:20px}
.opt{display:flex;justify-content:space-between;align-items:center;width:100%;background:var(--bg);border:1px solid var(--line);color:var(--txt);border-radius:12px;padding:14px 16px;margin-bottom:10px;cursor:pointer;font:600 15px Inter,sans-serif;transition:.15s}
.opt:hover{border-color:var(--gold)}
.opt small{display:block;color:var(--mut);font-weight:400;font-size:12px}
.opt em{font-style:normal;color:var(--gold2)}
.close{background:none;border:0;color:var(--mut);cursor:pointer;width:100%;padding:8px;font:inherit}
.right{display:flex;align-items:center;gap:14px}
.themes{display:flex;gap:8px}
.dot{width:18px;height:18px;border-radius:50%;border:2px solid transparent;cursor:pointer;padding:0;transition:.15s}
.dot:hover{transform:scale(1.15)}
.dot.on{border-color:var(--txt)}
.burger{display:none;background:none;border:1px solid var(--line);color:var(--txt);border-radius:8px;width:40px;height:40px;font-size:20px;cursor:pointer}
.ranks{display:grid;gap:16px;grid-template-columns:repeat(auto-fit,minmax(min(100%,260px),1fr));margin-bottom:28px}
.rk{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:18px}
.rk h4{color:var(--gold2);font-size:14px;letter-spacing:.06em;margin-bottom:8px}
.rk li{list-style:none;font-size:14px;color:var(--mut);padding:6px 0;border-top:1px solid var(--line)}
.gem-wrap canvas{position:relative;width:100%;height:100%;display:block}
.pbtn{display:flex;align-items:center;gap:8px;background:var(--card);border:1px solid var(--line);color:var(--txt);border-radius:10px;padding:8px 12px;font:600 13px Inter,sans-serif;cursor:pointer;transition:.15s}
.pbtn:hover{border-color:var(--gold)}
.pbtn i{width:14px;height:14px;border-radius:50%;background:var(--gold);display:block}
.palette{position:relative}
.pbox{display:none;position:absolute;right:0;top:calc(100% + 12px);width:300px;background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px;box-shadow:0 20px 50px rgba(0,0,0,.6);z-index:60}
.pbox.open{display:block}
.pbox h5{font-size:13px;color:var(--mut);font-weight:600;margin-bottom:12px}
.sw{display:grid;grid-template-columns:repeat(6,1fr);gap:10px}
.sw button{aspect-ratio:1;border-radius:10px;border:2px solid transparent;cursor:pointer;transition:.12s}
.sw button:hover{transform:scale(1.1)}
.sw button.on{border-color:var(--txt);box-shadow:0 0 0 2px var(--card) inset}
.custom{display:flex;align-items:center;justify-content:space-between;margin-top:14px;padding-top:14px;border-top:1px solid var(--line);font-size:13px;color:var(--mut)}
.custom input{width:46px;height:32px;border:0;background:none;cursor:pointer}
/* Diamante 360 em loop */
.gem-wrap{position:relative;width:190px;height:190px;margin:0 auto 18px;perspective:700px;animation:float 3.5s ease-in-out infinite}
.glow{position:absolute;inset:-30px;border-radius:50%;background:radial-gradient(circle,color-mix(in srgb,var(--gold) 45%,transparent),transparent 65%);animation:pulse 3s ease-in-out infinite}
.gem{position:absolute;inset:0;transform-style:preserve-3d;animation:spin 5s linear infinite}
.gem svg{position:absolute;inset:0;width:100%;height:100%;overflow:visible}
.gem svg:nth-child(2){transform:rotateY(60deg)}
.gem svg:nth-child(3){transform:rotateY(120deg)}
.spark{position:absolute;color:var(--gold2);font-size:16px;animation:tw 2.4s ease-in-out infinite;opacity:0}
.spark:nth-of-type(1){top:-6px;left:4px}
.spark:nth-of-type(2){top:20px;right:-14px;animation-delay:.8s}
.spark:nth-of-type(3){bottom:6px;left:-12px;animation-delay:1.6s}
@keyframes spin{to{transform:rotateY(360deg)}}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}
@keyframes pulse{0%,100%{opacity:.5;transform:scale(.9)}50%{opacity:1;transform:scale(1.1)}}
@keyframes tw{0%,100%{opacity:0;transform:scale(.4)}50%{opacity:1;transform:scale(1)}}
@media(prefers-reduced-motion:reduce){.gem,.gem-wrap,.glow,.spark{animation:none}.spark{opacity:1}}
/* Celular */
@media(max-width:760px){
  .burger{display:block}
  nav ul{display:none;position:absolute;top:64px;left:0;right:0;flex-direction:column;gap:0;background:var(--bg);border-bottom:1px solid var(--line)}
  nav ul.open{display:flex}
  nav ul a{display:block;padding:16px 20px;border-top:1px solid var(--line)}
  .vbtn{display:none}
  .hero{padding:48px 0 44px}
  .hero p{font-size:15px}
  .hero .btn,.cta .btn{display:block;margin:10px auto 0;max-width:320px}
  .stats{gap:24px;margin-top:36px}
  section{padding:44px 0}
  h2{font-size:25px}
  .tools{flex-direction:column;align-items:stretch}
  .chips{overflow-x:auto;flex-wrap:nowrap;padding-bottom:4px}
  .chip{white-space:nowrap}
  .cta{padding:40px 18px}
  .modal.open{place-items:end center;padding:0}
  .box{border-radius:18px 18px 0 0;max-width:100%}
  .gem-wrap{width:150px;height:150px}
  .palette{position:static}
  .pbox{left:12px;right:12px;top:68px;width:auto}
}
@media(max-width:420px){.pbtn span{display:none}.themes{gap:6px}.dot{width:16px;height:16px}.logo{font-size:17px}.right{gap:10px}}
</style>
</head>
<body>

<nav><div class="wrap">
  <a class="logo" href="#">LUMEX <span>FORGE</span></a>
  <ul id="menu"><li><a href="#loja">Loja</a></li><li><a href="#eb">Exército RP</a></li><li><a href="#como">Como funciona</a></li><li><a href="#faq">Dúvidas</a></li><li><a href="#contato">Contato</a></li></ul>
  <div class="right">
    <div class="palette" id="palette">
      <button class="pbtn" id="pbtn" aria-haspopup="true" aria-label="Escolher cor do site"><i></i><span>Cores</span></button>
      <div class="pbox" id="pbox">
        <h5>🎨 Escolha a cor do site</h5>
        <div class="sw" id="sw"></div>
        <label class="custom">Cor personalizada<input type="color" id="pcustom" value="#d4af37"></label>
      </div>
    </div>
    <a class="btn gold vbtn" href="#loja" style="padding:9px 18px;font-size:14px">Ver scripts</a>
    <button class="burger" id="burger" aria-label="Abrir menu">☰</button>
  </div>
</div></nav>

<header class="hero"><div class="wrap">
  <div class="gem-wrap" aria-hidden="true">
    <div class="glow"></div>
    <canvas id="gem" aria-hidden="true"></canvas>
    <span class="spark">✦</span><span class="spark">✦</span><span class="spark">✦</span>
  </div>
  <span class="badge">SCRIPTS PARA ROBLOX STUDIO</span>
  <h1>Acelere o seu jogo com scripts <em>prontos e elegantes</em></h1>
  <p>Sistemas completos, organizados e fáceis de instalar para quem cria jogos no Roblox Studio. Pague com Robux ou com dinheiro.</p>
  <a class="btn gold" href="#loja">Explorar a loja</a>
  <a class="btn line" href="#como">Como funciona</a>
  <div class="stats">
    <div><b id="nProd">0</b><small>scripts</small></div>
    <div><b>Luau</b><small>código limpo</small></div>
    <div><b>Robux + R$</b><small>formas de pagar</small></div>
  </div>
</div></header>

<section id="loja"><div class="wrap">
  <h2>Loja de scripts</h2>
  <p class="sub">Sistemas no estilo dos jogos mais jogados do Roblox: pets, anime RPG, obby, tiro, terror, tycoon, roleplay e mais.</p>
  <div class="tools">
    <input id="busca" type="search" placeholder="Pesquisar script...">
    <div class="chips" id="chips"></div>
  </div>
  <div class="grid" id="grid"></div>
</div></section>

<section id="eb"><div class="wrap">
  <h2>Pacote Exército Brasileiro RP</h2>
  <p class="sub">Hierarquia completa para jogos de rotina militar. Nomes, cargos e salários são editáveis.</p>
  <div class="ranks" id="ranks"></div>
  <button class="btn gold" id="verEB">Ver scripts do Exército RP</button>
</div></section>

<section id="como"><div class="wrap">
  <h2>Como funciona</h2>
  <p class="sub">Do pagamento ao jogo em poucos minutos.</p>
  <div class="how">
    <div class="step"><b>1. Escolha</b><span>Veja a descrição e as opções de cada script.</span></div>
    <div class="step"><b>2. Pague</b><span>Robux pelo Roblox ou dinheiro por Pix, cartão e outros.</span></div>
    <div class="step"><b>3. Receba</b><span>Você recebe o arquivo e um guia de instalação.</span></div>
    <div class="step"><b>4. Use</b><span>Cole no Roblox Studio, personalize e publique.</span></div>
  </div>
</div></section>

<section id="faq"><div class="wrap faq">
  <h2>Dúvidas frequentes</h2>
  <p class="sub">Respostas rápidas antes de comprar.</p>
  <details><summary>Como recebo o script?</summary><p>Depois da confirmação do pagamento, o arquivo e o guia de instalação são enviados pelo contato informado na compra.</p></details>
  <details><summary>Posso usar em jogos comerciais?</summary><p>Sim. A licença permite usar no seu jogo. Revender ou redistribuir o código não é permitido.</p></details>
  <details><summary>Os scripts funcionam em qualquer jogo?</summary><p>Eles são feitos para o Roblox Studio e devem ser instalados no seu próprio jogo.</p></details>
  <details><summary>Tem suporte?</summary><p>Sim. Você pode tirar dúvidas de instalação pelo TikTok ou pelo Roblox.</p></details>
  <details><summary>Quais formas de pagamento?</summary><p>Robux (via Game Pass do Roblox) e dinheiro (Pix, cartão ou outros links configurados na loja).</p></details>
</div></section>

<section id="contato"><div class="wrap">
  <div class="cta">
    <h2>Precisa de um script sob medida?</h2>
    <p class="sub">Descreva a ideia do seu jogo e receba um orçamento.</p>
    <a class="btn gold" id="lnkTiktok" href="#" target="_blank" rel="noopener">Chamar no TikTok</a>
    <a class="btn line" id="lnkRoblox" href="#" target="_blank" rel="noopener">Perfil no Roblox</a>
  </div>
</div></section>

<footer><div class="wrap">© <span id="ano"></span> Lumex Forge · <a id="ftTiktok" href="#" target="_blank" rel="noopener" style="color:var(--gold2)">TikTok @vinlumexz00</a> · <a id="ftRoblox" href="#" target="_blank" rel="noopener" style="color:var(--gold2)">Roblox eyeywtwywywy</a><br> Roblox e Roblox Studio são marcas da Roblox Corporation. Este site não é afiliado à Roblox nem ao Exército Brasileiro, e nenhum brasão ou insígnia oficial é incluído.</div></footer>

<div class="modal" id="modal"><div class="box">
  <h3 id="mNome"></h3>
  <p>Escolha como deseja pagar:</p>
  <button class="opt" id="mRbx"><span>Comprar com Robux<small>Pagamento pelo Roblox</small></span><em id="mRbxP"></em></button>
  <button class="opt" id="mPix"><span>Pagar com dinheiro<small>Pix, cartão ou link de pagamento</small></span><em id="mPixP"></em></button>
  <button class="close" id="mClose">Cancelar</button>
</div></div>

<script>
/* ===== CONFIGURAÇÃO: edite aqui ===== */
const CONFIG = {
  tiktok: "https://www.tiktok.com/@vinlumexz00",
  roblox: "https://www.roblox.com/search/users?keyword=eyeywtwywywy",
  moeda: "R$"
};

/* Para cada produto: troque linkRobux pelo link do seu Game Pass
   e linkPay pelo link de pagamento (Pix, Mercado Pago, PayPal, Stripe...). */
const PRODUTOS = [
  {nome:"Sistema de Inventário",cat:"Sistemas",ico:"🎒",desc:"Inventário com slots, arrastar e soltar, empilhamento e salvamento automático.",tags:["DataStore","UI","Server"],brl:39.9,rbx:399,linkRobux:"#",linkPay:"#"},
  {nome:"Menu Principal ALPHA",cat:"Interface",ico:"🖤",desc:"Menu preto elegante com botões animados, abas e tela de carregamento.",tags:["UI","Tween","Mobile"],brl:24.9,rbx:249,linkRobux:"#",linkPay:"#"},
  {nome:"Economia e Moedas",cat:"Economia",ico:"💰",desc:"Sistema de moedas com salvamento seguro, recompensas diárias e placar.",tags:["DataStore","Leaderstats"],brl:29.9,rbx:299,linkRobux:"#",linkPay:"#"},
  {nome:"Loja Dentro do Jogo",cat:"Economia",ico:"🛒",desc:"Loja com itens, preços, compra com moedas e integração com Game Pass.",tags:["UI","MarketplaceService"],brl:44.9,rbx:449,linkRobux:"#",linkPay:"#"},
  {nome:"Sistema de Missões",cat:"Sistemas",ico:"📜",desc:"Missões diárias e de história com progresso, recompensas e interface pronta.",tags:["Quests","UI","DataStore"],brl:34.9,rbx:349,linkRobux:"#",linkPay:"#"},
  {nome:"Times e Aliados",cat:"Combate",ico:"🛡️",desc:"Times balanceados, cores por equipe e destaque de aliados com Highlight.",tags:["Teams","Highlight"],brl:19.9,rbx:199,linkRobux:"#",linkPay:"#"},
  {nome:"Armas Básicas",cat:"Combate",ico:"🔫",desc:"Base de armas com tiro, recarga, dano, efeitos e HUD de munição.",tags:["Tools","Raycast","FX"],brl:49.9,rbx:499,linkRobux:"#",linkPay:"#"},
  {nome:"Painel de Administração",cat:"Ferramentas",ico:"⚙️",desc:"Painel para o dono do jogo: comandos, kick, aviso global e logs.",tags:["Admin","UI","Remote"],brl:39.9,rbx:399,linkRobux:"#",linkPay:"#"},
  {nome:"Ciclo Dia e Noite",cat:"Ferramentas",ico:"🌙",desc:"Dia e noite suaves com iluminação, céu e velocidade configuráveis.",tags:["Lighting","Config"],brl:14.9,rbx:149,linkRobux:"#",linkPay:"#"},
  {nome:"Sistema de Pets",cat:"Sistemas",ico:"🐾",desc:"Pets que seguem o jogador, raridades, equipar e chocar ovos.",tags:["Pets","UI","DataStore"],brl:54.9,rbx:549,linkRobux:"#",linkPay:"#"}
];
/* Atalho: P(nome, categoria, ícone, descrição, "tag1,tag2", preço em R$) */
const P=(n,c,i,d,t,b)=>({nome:n,cat:c,ico:i,desc:d,tags:t.split(","),brl:b,rbx:Math.round(b*10),linkRobux:"#",linkPay:"#"});
PRODUTOS.push(
/* ---- Militar EB ---- */
P("Sistema de Patentes EB","Militar EB","🎖️","17 patentes do Soldado ao Marechal, com cargo, tag sobre a cabeça, salário e permissões por patente.","Patentes,DataStore,Tags",59.9),
P("Painel do Comando","Militar EB","🧭","Promover, rebaixar, expulsar e advertir militares, com confirmação e registro de tudo.","Admin,UI,Logs",49.9),
P("Ficha do Militar","Militar EB","📋","Registro de serviço com medalhas, cursos, horas e histórico de promoções.","Ficha,DataStore,UI",34.9),
P("Ponto de Serviço","Militar EB","⏱️","Entrar e sair de serviço, contagem de horas, ranking e controle de folga.","Horas,Ranking,UI",29.9),
P("Companhias e Batalhões","Militar EB","🏛️","Organizações militares com comandante, membros, convites e hierarquia própria.","Grupos,UI,Server",44.9),
P("Uniformes por Patente","Militar EB","👕","Uniforme, divisas personalizáveis e boina aplicados automaticamente conforme a patente.","Avatar,Roupas,Patentes",39.9),
P("Cursos e Formação","Militar EB","🎓","Escola de formação com aulas, provas e certificados que liberam novas patentes.","Cursos,Provas,UI",44.9),
P("Rádio Militar","Militar EB","📻","Canais por unidade e patente, alerta geral e modo silêncio.","Rádio,Chat,UI",24.9),
P("Formatura e Continência","Militar EB","🫡","Formação em fileiras, continência ao superior e comandos de ordem unida.","Animações,Comandos",34.9),
P("Arsenal e Cautela","Militar EB","🗄️","Retirada de armas por patente, cautela, devolução e histórico de quem pegou.","Tools,Permissões,Logs",39.9),
P("Controle de Acesso","Militar EB","🚧","Portões e áreas restritas liberados por patente, com cartão e alarme.","Portões,Permissões",27.9),
P("Disciplina e Punições","Militar EB","⚖️","Advertências, prisão disciplinar, cela com tempo e histórico do militar.","Punições,Cela,UI",32.9),
P("Operações e Missões","Militar EB","🎯","Comandante cria operações com equipes, objetivos, tempo e relatório final.","Missões,Equipes,UI",49.9),
P("Viaturas Militares","Militar EB","🚙","Garagem de viaturas liberadas por patente, com spawn, chave e devolução.","Veículos,Garagem",44.9),
/* ---- Roleplay ---- */
P("Nome RP e Documentos","Roleplay","🪪","Escolha de nome e sobrenome, RG, CNH e número do cidadão exibidos para outros jogadores.","Documentos,UI,DataStore",29.9),
P("Celular In-Game","Roleplay","📱","Celular com contatos, mensagens, câmera, banco e apps que você personaliza.","UI,Apps,Chat",59.9),
P("Banco e Caixa Eletrônico","Roleplay","🏦","Conta, saque, depósito, transferência entre jogadores e extrato.","Economia,UI,DataStore",39.9),
P("Sistema de Empregos","Roleplay","💼","Empregos com salário, uniforme, ferramentas e folha de pagamento automática.","Empregos,Economia",44.9),
P("Casas e Aluguel","Roleplay","🏠","Comprar, alugar e decorar casas, com chave, trancar porta e convidados.","Casas,Portas,DataStore",54.9),
P("Fome, Sede e Energia","Roleplay","🍔","Necessidades do personagem com barras, comidas, bebidas e descanso.","Status,UI,Itens",19.9),
P("Hospital e Socorro","Roleplay","🚑","Ferimentos, ambulância, reanimar jogador e atendimento médico.","Saúde,Veículos,UI",39.9),
P("Polícia e Prisão","Roleplay","🚓","Algemar, revistar, multar, prender e cela com tempo de pena.","Polícia,Cela,UI",49.9),
P("Chat RP","Roleplay","💬","Comandos /me, /do, /ooc e /anon com balões e cores por tipo de fala.","Chat,Comandos,UI",22.9),
P("Emotes e Animações","Roleplay","🕺","Menu radial com dezenas de animações e atalhos de teclado.","Animações,UI,Mobile",24.9),
P("Roupas e Avatar","Roleplay","🧥","Armário de roupas, salvar looks e trocar visual sem sair do jogo.","Avatar,UI,DataStore",34.9),
P("Mercado e Lojas","Roleplay","🏪","Lojas com caixa, estoque, preços editáveis e NPC vendedor.","Lojas,NPC,Economia",39.9),
P("Multas e Licenças","Roleplay","📑","Multas, licenças de porte e habilitação com validade e pagamento.","Documentos,Economia",29.9),
P("Cidade Dinâmica","Roleplay","🌆","Horários da cidade, semáforos, clima e eventos aleatórios.","Cidade,Lighting,Eventos",34.9),
P("Mapa e GPS","Roleplay","🗺️","Mapa da cidade com marcadores, rota até o destino e minimapa.","UI,Mapa,Mobile",27.9),
P("Eventos e Sorteios","Roleplay","🎁","Eventos agendados, contagem regressiva, sorteios e recompensas.","Eventos,UI",24.9),
/* ---- Veículos ---- */
P("Carros e Garagem","Veículos","🚗","Spawn de carros, cores, chave, trancar, buzina e garagem salva por jogador.","Veículos,Garagem,DataStore",64.9),
P("Combustível e Posto","Veículos","⛽","Tanque, consumo, posto de gasolina e pagamento no frentista.","Veículos,Economia",29.9),
P("Concessionária","Veículos","🏎️","Loja de veículos com test drive, cores e financiamento.","Loja,Veículos,UI",44.9),
P("Barcos e Aeronaves","Veículos","✈️","Barcos, helicópteros e aviões com controles simples e hangar.","Veículos,Física",49.9),
/* ---- Sistemas e ferramentas ---- */
P("Grupos e Clãs","Sistemas","👥","Criar clã, convidar, cargos, banco do clã e chat privado.","Clãs,UI,DataStore",44.9),
P("Tags e Cargos","Sistemas","🏷️","Tags coloridas acima da cabeça por cargo, grupo ou gamepass.","Tags,Grupos",17.9),
P("Tutorial Inicial","Interface","🧩","Tutorial guiado para novos jogadores, com passos, setas e recompensa.","UI,Onboarding",19.9),
P("Configurações do Jogador","Interface","🎚️","Menu de som, brilho, sensibilidade e teclas, com salvamento automático.","UI,DataStore",17.9),
P("Notificações","Interface","🔔","Avisos animados no canto da tela, com tipos, som e fila.","UI,Tween",14.9),
P("Ranking Global","Economia","🏆","Placar global de moedas, horas ou abates, atualizado em tempo real.","DataStore,OrderedDataStore",19.9),
P("Loja VIP e Game Pass","Economia","💎","Loja de Game Pass e Developer Products com entrega automática.","MarketplaceService,UI",29.9),
P("Anti-Exploit Básico","Ferramentas","🔒","Proteções de servidor contra abusos no SEU jogo: velocidade, teletransporte e remotes.","Segurança,Server",39.9)
);
PRODUTOS.push(
/* ---- Pets e Simulador ---- */
P("Ovos, Raridades e Mutações","Pets & Simulador","🥚","Chocar ovos com chances exibidas, raridades, mutações, equipar e evoluir pets.","Pets,Ovos,DataStore",59.9),
P("Trocas Seguras","Pets & Simulador","🤝","Troca entre jogadores com confirmação em duas etapas e proteção contra golpes.","Trocas,UI,Segurança",54.9),
P("Simulador de Cliques e Renascimento","Pets & Simulador","🖱️","Coletar, multiplicadores, renascer (rebirth) e áreas que abrem por nível.","Simulador,Rebirth",49.9),
P("Mochila e Venda de Recursos","Pets & Simulador","🎒","Capacidade de mochila, ponto de venda, upgrades e preço por recurso.","Simulador,Economia",34.9),
P("Mundos Desbloqueáveis","Pets & Simulador","🌍","Portais para novas áreas por custo ou nível, com tela de desbloqueio.","Mundos,UI",39.9),
P("Batalha de Pets","Pets & Simulador","⚔️","Duelo de pets por turnos com ataques, tipos e recompensas.","Pets,Batalha,UI",59.9),
P("Conquistas e Troféus","Pets & Simulador","🏅","Lista de conquistas com progresso, recompensa e vitrine de troféus.","Conquistas,UI,DataStore",29.9),
P("Recompensa Diária e Roleta","Pets & Simulador","🎡","Sequência de dias, roleta de prêmios com chances à mostra e cooldown.","Daily,Roleta,UI",34.9),
/* ---- Anime RPG ---- */
P("Habilidades e Poderes","Anime RPG","✨","Poderes com tecla, cooldown, energia, efeitos e evolução de nível.","Skills,Cooldown,FX",64.9),
P("Níveis, XP e Atributos","Anime RPG","📈","Subir de nível, distribuir pontos de força, vida e velocidade.","RPG,UI,DataStore",44.9),
P("NPCs, Diálogos e Missões","Anime RPG","🗣️","NPCs com diálogo, aceitar missão, objetivo e recompensa.","NPC,Missões,UI",49.9),
P("Chefes e Raids","Anime RPG","🐉","Chefes com fases, ataques, barra de vida e drops por dano.","Boss,IA,Drops",59.9),
P("Combate Corpo a Corpo","Anime RPG","🥋","Combos, bloqueio, esquiva, hitbox e animações de golpe.","Combate,Animações",54.9),
P("Classes e Estilos de Luta","Anime RPG","🧙","Escolha de classe com status e habilidades próprias.","Classes,RPG",49.9),
P("Equipamentos e Raridades","Anime RPG","🗡️","Espadas, armaduras e acessórios com status, raridade e melhoria.","Itens,Inventário",44.9),
/* ---- Obby e Parkour ---- */
P("Obby com Checkpoints","Obby & Parkour","🏁","Estágios, checkpoints salvos, pular fase e contador de mortes.","Obby,Checkpoint",29.9),
P("Torre Infinita","Obby & Parkour","🗼","Torre com seções aleatórias, cronômetro, altura e ranking.","Torre,Geração,Ranking",49.9),
P("Speedrun e Cronômetro","Obby & Parkour","⏲️","Tempo por fase, recorde pessoal e ranking dos mais rápidos.","Timer,Ranking",24.9),
P("Movimentos Extras","Obby & Parkour","🦘","Pulo duplo, dash, corrida e planar com energia.","Movimento,Mobile",29.9),
/* ---- PvP e Tiro ---- */
P("Armas Avançadas","PvP & Tiro","🎯","Recuo, mira, balas, recarga, headshot e skins de arma.","Armas,Raycast,FX",69.9),
P("Partidas e Lobby","PvP & Tiro","🎮","Lobby, times, rodadas, votação de mapa e fim de partida.","Partidas,Times,UI",64.9),
P("Kill Feed e Placar","PvP & Tiro","📊","Feed de abates, placar da partida, MVP e estatísticas.","UI,Placar",24.9),
P("Loadouts e Skins","PvP & Tiro","🧰","Montar kits de armas, equipar skins e salvar loadouts.","Loadout,UI,DataStore",39.9),
P("Zona que Fecha (Battle Royale)","PvP & Tiro","🪂","Queda de paraquedas, zona que encolhe, loot e último vivo.","BattleRoyale,Zona",79.9),
P("Polícia e Ladrão","PvP & Tiro","🚔","Assalto, fuga, prisão, resgate e recompensa por equipe.","Equipes,Prisão,Missões",59.9),
/* ---- Terror e Sobrevivência ---- */
P("Portas, Chaves e Salas","Terror & Sobrevivência","🚪","Corredor com salas numeradas, chaves, esconderijos e sustos.","Terror,Portas",49.9),
P("Monstro com IA","Terror & Sobrevivência","👹","Monstro que ouve, persegue e procura, com esconderijos e fuga.","IA,Pathfinding",54.9),
P("Capítulos e Cutscenes","Terror & Sobrevivência","🎬","Capítulos com cutscenes de câmera, falas e salvamento.","Cutscene,Câmera",44.9),
P("Sobrevivência: Fogueira e Craft","Terror & Sobrevivência","🔥","Coletar recursos, craftar, fogueira, vida, fome e construção.","Craft,Construção,Status",69.9),
/* ---- Tycoon ---- */
P("Tycoon Base","Tycoon","🏭","Botões de compra, droppers, esteira, renda e upgrades salvos.","Tycoon,Economia,DataStore",54.9),
P("Prestígio e Multiplicadores","Tycoon","♻️","Resetar progresso por bônus permanente e multiplicador de renda.","Prestígio,Economia",34.9),
/* ---- Minigames ---- */
P("Assassino e Xerife","Minigames","🔪","Papéis secretos, rodada, moedas, arma do xerife e tela final.","Rodadas,Papéis,UI",59.9),
P("Pique-Esconde","Minigames","🙈","Pegador, tempo de esconder, rodadas e pontuação.","Rodadas,Times",34.9),
P("Duelo de Reflexo com Bola","Minigames","⚽","Bola que mira nos jogadores, defesa na hora certa e eliminação.","Reflexo,Física,Partidas",39.9),
P("Votação de Mapas","Minigames","🗳️","Votação de mapa e modo antes da rodada, com contagem.","Votação,UI",24.9),
P("Sala de Espera e Contagem","Minigames","⏳","Lobby com contagem regressiva, mínimo de jogadores e teleporte.","Lobby,Timer",19.9),
P("Modo Espectador","Minigames","👁️","Assistir outros jogadores depois de ser eliminado.","Câmera,UI",19.9),
P("Passe de Batalha","Sistemas","🎟️","Temporadas com níveis grátis e premium, missões e recompensas.","Temporada,UI,DataStore",69.9),
P("Grupos de Jogadores (Party)","Sistemas","🎉","Criar grupo, convidar amigos e entrar juntos nas partidas.","Party,UI,Teleport",29.9)
);
/* ===================================== */

const $ = s => document.querySelector(s);
const fmt = v => CONFIG.moeda + " " + v.toFixed(2).replace(".", ",");
const cats = ["Todos", ...new Set(PRODUTOS.map(p => p.cat))];
let catAtual = "Todos", atual = null;

function abrir(link){
  if(link && link.startsWith("http")) window.open(link, "_blank", "noopener");
  else alert("Link ainda não configurado. Edite os links no começo do script em index.html.");
}

function render(){
  const q = $("#busca").value.trim().toLowerCase();
  const lista = PRODUTOS.filter(p =>
    (catAtual === "Todos" || p.cat === catAtual) &&
    (p.nome + p.desc + p.tags.join(" ")).toLowerCase().includes(q));
  $("#grid").innerHTML = lista.length ? lista.map(p => `
    <article class="card">
      <div class="ico">${p.ico}</div>
      <h3>${p.nome}</h3>
      <p>${p.desc}</p>
      <div class="tags">${p.tags.map(t => `<span>${t}</span>`).join("")}</div>
      <div class="price"><b>${fmt(p.brl)}</b><i>ou ${p.rbx} R$ Robux</i></div>
      <button class="btn gold" data-i="${PRODUTOS.indexOf(p)}">Comprar</button>
    </article>`).join("") : `<div class="empty">Nenhum script encontrado.</div>`;
}

function chips(){
  $("#chips").innerHTML = cats.map(c => `<button class="chip ${c===catAtual?"on":""}" data-c="${c}">${c}</button>`).join("");
}

$("#chips").addEventListener("click", e => {
  const c = e.target.dataset.c; if(!c) return;
  catAtual = c; chips(); render();
});
$("#busca").addEventListener("input", render);
$("#grid").addEventListener("click", e => {
  const i = e.target.dataset.i; if(i === undefined) return;
  atual = PRODUTOS[i];
  $("#mNome").textContent = atual.nome;
  $("#mRbxP").textContent = atual.rbx + " Robux";
  $("#mPixP").textContent = fmt(atual.brl);
  $("#modal").classList.add("open");
});
$("#mRbx").onclick = () => abrir(atual.linkRobux);
$("#mPix").onclick = () => abrir(atual.linkPay);
$("#mClose").onclick = () => $("#modal").classList.remove("open");
$("#modal").addEventListener("click", e => { if(e.target.id === "modal") $("#modal").classList.remove("open"); });

$("#nProd").textContent = PRODUTOS.length;
$("#lnkTiktok").href = CONFIG.tiktok;
$("#ftTiktok").href = CONFIG.tiktok;
$("#lnkRoblox").href = CONFIG.roblox;
$("#ftRoblox").href = CONFIG.roblox;
$("#ano").textContent = new Date().getFullYear();

/* Cores do site: caixinha de cores (lembra a escolha) */
const CORES=[["Dourado","#d4af37"],["Laranja","#ff9f1c"],["Coral","#ff7a59"],["Vermelho","#ff4d4d"],["Carmim","#e63946"],["Rosa","#ff5fa2"],
["Magenta","#ff77e9"],["Roxo","#9b6bff"],["Índigo","#6c5ce7"],["Azul","#3b9eff"],["Ciano","#00c2ff"],["Turquesa","#18d9c8"],
["Verde","#2fd18b"],["Lima","#8ee000"],["Amarelo","#f5e663"],["Bronze","#c9a27a"],["Prata","#b0b8c4"],["Branco","#ffffff"]];
const clarear=(h,p)=>{const n=parseInt(h.slice(1),16),m=v=>Math.round(v+(255-v)*p).toString(16).padStart(2,"0");return "#"+m(n>>16)+m(n>>8&255)+m(n&255);};
function aplicarCor(h){
  const r=document.documentElement.style;
  document.documentElement.removeAttribute("data-theme");
  if(h.toLowerCase()==="#d4af37"){r.removeProperty("--gold");r.removeProperty("--gold2");}
  else{r.setProperty("--gold",h);r.setProperty("--gold2",clarear(h,.45));}
  $("#pbtn i").style.background=h; $("#pcustom").value=h;
  document.querySelectorAll("#sw button").forEach(x=>x.classList.toggle("on",x.dataset.c.toLowerCase()===h.toLowerCase()));
  try{localStorage.setItem("cor",h);}catch(e){}
}
$("#sw").innerHTML=CORES.map(([n,c])=>`<button data-c="${c}" title="${n}" aria-label="${n}" style="background:${c}"></button>`).join("");
$("#sw").addEventListener("click",e=>{if(e.target.dataset.c)aplicarCor(e.target.dataset.c);});
$("#pcustom").addEventListener("input",e=>aplicarCor(e.target.value));
$("#pbtn").onclick=e=>{e.stopPropagation();$("#pbox").classList.toggle("open");};
document.addEventListener("click",e=>{if(!e.target.closest("#pbox"))$("#pbox").classList.remove("open");});
document.addEventListener("keydown",e=>{if(e.key==="Escape")$("#pbox").classList.remove("open");});
let corSalva="#d4af37";try{corSalva=localStorage.getItem("cor")||corSalva;}catch(e){}
aplicarCor(/^#[0-9a-f]{6}$/i.test(corSalva)?corSalva:"#d4af37");

/* Patentes (seção do Exército) */
const PATENTES={
  "Praças":["Soldado","Cabo","3º Sargento","2º Sargento","1º Sargento","Subtenente"],
  "Oficiais":["Aspirante a Oficial","2º Tenente","1º Tenente","Capitão","Major","Tenente-Coronel","Coronel"],
  "Oficiais-Generais":["General de Brigada","General de Divisão","General de Exército","Marechal"]
};
$("#ranks").innerHTML=Object.entries(PATENTES).map(([g,l])=>`<div class="rk"><h4>${g.toUpperCase()}</h4><ul>${l.map(n=>`<li>${n}</li>`).join("")}</ul></div>`).join("");
$("#verEB").onclick=()=>{catAtual="Militar EB";chips();render();location.hash="#loja";};

/* Diamante 3D feito de linhas */
(function(){
  const cv=$("#gem"),ctx=cv.getContext("2d");
  const V=[],E=[];
  const ring=(n,r,y,off)=>{const a=[];for(let k=0;k<n;k++){const t=off+k*2*Math.PI/n;V.push([r*Math.cos(t),y,r*Math.sin(t)]);a.push(V.length-1);}return a;};
  const tb=ring(8,.55,.55,0), gd=ring(8,1,.15,Math.PI/8), md=ring(8,.5,-.45,0);
  V.push([0,-1.15,0]); const cu=V.length-1;
  for(let k=0;k<8;k++){
    const n=(k+1)%8, pv=(k+7)%8;
    E.push([tb[k],tb[n]],[gd[k],gd[n]],[tb[k],gd[k]],[tb[k],gd[pv]],[gd[k],md[k]],[gd[k],md[n]],[md[k],cu]);
  }
  let t=0;
  function draw(){
    const dpr=window.devicePixelRatio||1, w=cv.clientWidth||190;
    if(cv.width!==Math.round(w*dpr)){cv.width=cv.height=Math.round(w*dpr);}
    ctx.setTransform(dpr,0,0,dpr,0,0); ctx.clearRect(0,0,w,w);
    const cs=getComputedStyle(document.documentElement);
    const c1=cs.getPropertyValue("--gold2").trim(), c2=cs.getPropertyValue("--gold").trim();
    const cy=Math.cos(t), sy=Math.sin(t), cx=Math.cos(.45), sx=Math.sin(.45);
    const Q=V.map(([x,y,z])=>{
      const X=x*cy+z*sy; let Z=-x*sy+z*cy;
      const Y=y*cx-Z*sx; Z=y*sx+Z*cx;
      const f=3.6/(3.6+Z);
      return [w/2+X*f*w*.31, w/2-Y*f*w*.31, Z];
    });
    ctx.lineWidth=1.7; ctx.lineCap="round"; ctx.shadowColor=c2; ctx.shadowBlur=10;
    for(const [a,b] of E){
      const A=Q[a], B=Q[b], z=(A[2]+B[2])/2;
      ctx.globalAlpha=Math.max(.2,Math.min(1,.65-z*.4));
      ctx.strokeStyle=z>0?c2:c1;
      ctx.beginPath(); ctx.moveTo(A[0],A[1]); ctx.lineTo(B[0],B[1]); ctx.stroke();
    }
    ctx.globalAlpha=1;
  }
  if(window.matchMedia("(prefers-reduced-motion: reduce)").matches){ draw(); }
  else{ (function loop(){ t+=.016; draw(); requestAnimationFrame(loop); })(); }
})();

/* Menu do celular */
$("#burger").onclick = () => $("#menu").classList.toggle("open");
$("#menu").addEventListener("click", e => { if(e.target.tagName === "A") $("#menu").classList.remove("open"); });
chips(); render();
</script>
</body>
</html>
