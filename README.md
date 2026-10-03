<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Scripts para Roblox Studio</title>
<meta name="description" content="Scripts sob medida para o seu jogo no Roblox Studio: painel ADM, patentes, portões, painel de festa e mais.">
<meta property="og:title" content="Scripts para Roblox Studio">
<meta property="og:description" content="Teste ao vivo um painel ADM, tags de patente e portões. Monte seu pedido em 20 segundos.">
<meta property="og:type" content="website">
<meta name="theme-color" content="#000000">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&display=swap" rel="stylesheet">

<!-- ============ CONFIGURAÇÕES: MUDE TUDO AQUI ============ -->
<script>
var CONFIG = {
  // contatos
  tiktokUser: "vinlumexz00",
  robloxUser: "eyeywtwywywy",
  robloxLink: "",                        // link do perfil do Roblox. Vazio = busca pelo usuário
  botaoTiktok: "ENTRAR EM CONTATO TIKTOK",

  // aparência
  corInicial: "#8b5cf6",
  cores: [
    ["Roxo","#8b5cf6"],["Azul","#3b82f6"],["Amarelo","#facc15"],["Magenta","#ff00cc"],["Branco","#ffffff"],
    ["Vermelho","#ef4444"],["Laranja","#fb923c"],["Verde","#22c55e"],["Ciano","#06b6d4"],["Rosa","#f472b6"],
    ["Lima","#a3e635"],["Turquesa","#14b8a6"],["Dourado","#d4af37"],["Azul-marinho","#1e40af"],["Cinza","#9ca3af"]
  ],
  botaoAparencia: "Editar aparência",
  botaoArcoiris: "Modo arco-íris",
  botaoFixo: "Pedir meu script",

  // topo
  tituloInicio: "Seu jogo no Roblox com ",
  palavras: ["scripts que o jogador nota","painel ADM de verdade","patentes e portões","festa com música e cor"],
  descricao: "Eu faço o script sob medida, você cola no Roblox Studio e ele funciona. Teste tudo aqui no site antes de pedir.",
  botaoPedido: "Montar meu pedido",
  frasesegura: "Site seguro: não baixa arquivos e não pede senha.",
  faixa: ["Painel ADM","Tags e patentes","Portões","Spawn por base","Painel de festa","Menus e lojas","Sob medida","Mobile e PC"],

  // compartilhar
  botaoCompartilhar: "Compartilhar o site",
  textoCompartilhar: "Olha esse site de scripts para Roblox Studio, dá para testar tudo ao vivo:",
  linkCopiado: "Link copiado! Cole onde quiser.",

  // janela de código (exemplo ilustrativo)
  codTitulo: "Exemplo de script: portão por patente",
  codTexto: "É esse tipo de código que eu entrego pronto. Você só cola no Roblox Studio.",
  codArquivo: "Portao (Script)",
  codigo: [
    "-- portão que só abre para quem tem a patente certa",
    "local portao = script.Parent",
    "local PATENTE_MINIMA = 3",
    "",
    "portao.Touched:Connect(function(hit)",
    "\tlocal jogador = game.Players:GetPlayerFromCharacter(hit.Parent)",
    "\tif jogador == nil then return end",
    "\tlocal patente = jogador:GetAttribute(\"Patente\") or 0",
    "\tif patente >= PATENTE_MINIMA then",
    "\t\tportao.CanCollide = false",
    "\t\ttask.wait(3)",
    "\t\tportao.CanCollide = true",
    "\tend",
    "end)"
  ],

  // demonstração do painel ADM
  demoTitulo: "Teste um painel ADM agora",
  demoTexto: "Isto é uma demonstração. Toque nos botões e veja como o painel responde dentro do jogo.",
  jogadores: ["Jogador_01","Jogador_02","Jogador_03"],
  acoes: ["Expulsar","Voar","Velocidade"],
  interruptores: [["Chat liberado",true],["Portões abertos",false],["Modo noite",false]],

  // teste ao vivo (tag + portão)
  labTitulo: "Veja no seu jogo, com o seu nome",
  labTexto: "Escreva seu nome, escolha uma patente e teste o portão. É assim que fica para o jogador.",
  labNomePadrao: "SeuNome",
  labPatentes: [["Soldado","#9ca3af"],["Cabo","#22c55e"],["Sargento","#3b82f6"],["Tenente","#facc15"],["Capitão","#fb923c"],["General","#ef4444"]],
  labPatenteMin: 2,

  // scripts à venda (mantenha "Tags e patentes" e "Portões e portas" na 2ª e 3ª posição)
  scriptsTitulo: "O que eu faço",
  scriptsTexto: "Peça o que o seu jogo precisa. Se não estiver na lista, eu crio sob medida.",
  scripts: [
    ["Painel ADM","Expulsar, banir, voar, velocidade, avisos e comandos de servidor."],
    ["Tags e patentes","Nome e patente acima da cabeça, por grupo ou por cargo."],
    ["Portões e portas","Abrem só para quem tem a patente ou o passe certo."],
    ["Spawn por base","Cada jogador renasce na sua própria base."],
    ["Painel de festa","Cores, volume, ID de música e aba só para ADM."],
    ["Menus e lojas","Loja com gamepass, menu de roupas e interface mobile."]
  ],

  // em breve (ainda NÃO está pronto: o visitante vota)
  breveTitulo: "Em breve: vote no próximo",
  breveTexto: "Estas ideias ainda não estão prontas. Toque em \"Quero\" nas que você compraria. Eu faço primeiro as mais pedidas.",
  breve: [
    ["Sistema de pets","Pet que segue o jogador e dá bônus."],
    ["Ranking e níveis","Ranking dos melhores e subida de nível."],
    ["Missões diárias","Tarefas todo dia com recompensa."],
    ["Menu de emotes","Danças e emotes em um menu bonito."],
    ["Sistema de clãs","Criar clã, convidar e ter tag própria."],
    ["Loja de skins","Roupas e efeitos comprados com moedas do jogo."],
    ["Anti-fly básico","Avisa quando alguém voa sem permissão."],
    ["Painel de eventos","Liga chuva, noite e eventos no servidor."]
  ],

  // monte seu pedido
  pedidoTitulo: "Monte seu pedido em 20 segundos",
  pedidoTexto: "Marque o que você quer. O site escreve a mensagem, você copia e cola no meu TikTok.",
  pedidoOutro: "Outro (explico no chat)",
  pedidoCampo: "Nome do seu jogo (opcional)",
  pedidoBotao: "Copiar mensagem e abrir TikTok",
  pedidoCopiado: "Mensagem copiada! Cole no chat do TikTok.",

  // como funciona a venda
  vendaTitulo: "Como funciona a venda",
  vendaTexto: "Tudo é feito no Roblox Studio, a ferramenta gratuita para criar jogos no Roblox.",
  passos: [
    ["Você me chama no TikTok","Conte qual jogo você tem e o que quer no script."],
    ["Combinamos o valor","Eu explico o que está incluso antes de você pagar."],
    ["Eu entrego o script","Você recebe os arquivos prontos: Script, LocalScript e ModuleScript."],
    ["Você cola no Roblox Studio","Eu mostro em qual lugar colocar cada um (ServerScriptService, StarterGui, etc.)."],
    ["Testamos juntos","Se algo não funcionar no seu jogo, eu ajusto."]
  ],

  // segurança
  segTitulo: "Site seguro",
  segTexto: "Eu quero que você se sinta tranquilo antes de falar comigo.",
  seguranca: [
    ["Não baixa nada","Os botões só abrem o meu TikTok e o meu perfil do Roblox. Nenhum arquivo é baixado."],
    ["Nunca peço sua senha","Para fazer o script eu não preciso da sua senha nem do cookie do Roblox. Se alguém pedir isso, é golpe."],
    ["Você confere antes","Antes de abrir qualquer link, o site mostra para onde você vai e você escolhe se quer continuar."]
  ],

  // depoimentos: só de clientes reais. Formato ["Nome","O que disse"]. Vazio = seção escondida
  depoimentos: [],
  depTitulo: "Quem já comprou",

  // perguntas frequentes
  faqTitulo: "Perguntas frequentes",
  faq: [
    ["Preciso saber programar?","Não. Eu mostro onde colar cada arquivo no Roblox Studio."],
    ["Funciona no celular?","Sim. Eu faço a interface pensando no mobile e no PC."],
    ["Quanto custa?","Depende do script. Me chama no TikTok com o seu pedido e eu falo o valor antes de você pagar."],
    ["E se der erro no meu jogo?","Me chama que eu ajusto o script para o seu jogo."]
  ],

  // final
  ctaTitulo: "Pronto para ter o script do seu jogo?",
  rodape: "Não tenho ligação com a Roblox Corporation. Roblox e Roblox Studio são marcas da Roblox Corporation."
};
</script>
<!-- ============ FIM DAS CONFIGURAÇÕES ============ -->

<style>
:root{--ac:#8b5cf6;--on:#fff;--bg:#000;--card:#0d0d0d;--line:#222;--tx:#f2f2f2;--mu:#a3a3a3}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--tx);font-family:"Space Grotesk",system-ui,sans-serif;line-height:1.55;padding-bottom:90px;overflow-x:hidden}
a{color:inherit}
.w{max-width:960px;margin:0 auto;padding:0 20px}
#prog{position:fixed;top:0;left:0;height:3px;width:0;background:var(--ac);z-index:20}
header{padding:70px 0 40px;position:relative}
header::before{content:"";position:absolute;left:50%;top:-120px;width:680px;height:480px;max-width:140vw;transform:translateX(-50%);background:radial-gradient(closest-side,var(--ac),transparent);opacity:.2;pointer-events:none;animation:glow 5s ease-in-out infinite alternate}
@keyframes glow{from{opacity:.12}to{opacity:.28}}
header>*:not(.fundo){position:relative;z-index:1}
.fundo{position:absolute;inset:0;width:100%;height:100%;pointer-events:none}
h1{font-size:clamp(2.2rem,8vw,4.2rem);line-height:1.02;letter-spacing:-.035em;max-width:16ch;min-height:3.1em}
h1 span{color:var(--ac)}
h1 span::after{content:"";display:inline-block;width:.07em;height:.9em;background:var(--ac);margin-left:.06em;vertical-align:-.08em;animation:pisca 1s steps(1) infinite}
@keyframes pisca{50%{opacity:0}}
.lead{color:var(--mu);max-width:50ch;margin:18px 0 26px;font-size:1.08rem}
.row{display:flex;flex-wrap:wrap;gap:10px}
.btn{display:inline-block;padding:14px 20px;border-radius:10px;font-weight:700;font-size:.95rem;font-family:inherit;text-decoration:none;border:2px solid var(--ac);cursor:pointer}
.pri{background:var(--ac);color:var(--on)}
.big{padding:16px 24px;font-size:1.02rem;animation:pulso 2.4s ease-in-out infinite}
@keyframes pulso{0%,100%{box-shadow:0 0 0 0 transparent}50%{box-shadow:0 0 0 8px color-mix(in srgb,var(--ac) 25%,transparent)}}
.sec{background:transparent;color:var(--tx)}
.sec:hover,.sec.on{background:var(--ac);color:var(--on)}
section{padding:46px 0;border-top:1px solid var(--line)}
h2{font-size:1.75rem;letter-spacing:-.02em;margin-bottom:6px}
.sub{color:var(--mu);margin-bottom:22px;max-width:56ch}
.ok{color:var(--mu);font-size:.85rem;margin-top:14px}
.faixa{overflow:hidden;border-block:1px solid var(--line);padding:14px 0;background:#050505}
.faixa div{display:flex;gap:42px;width:max-content;animation:rola 28s linear infinite}
.faixa span{white-space:nowrap;font-weight:700;color:var(--mu)}
.faixa span::before{content:"◆ ";color:var(--ac)}
@keyframes rola{to{transform:translateX(-50%)}}
.jan{background:#0a0a0a;border:1px solid var(--line);border-radius:14px;overflow:hidden}
.jb{display:flex;gap:7px;align-items:center;padding:10px 14px;border-bottom:1px solid var(--line);color:var(--mu);font-size:.85rem}
.jb i{width:11px;height:11px;border-radius:50%;background:#333}
.jb i:first-child{background:var(--ac)}
.jb b{margin-left:8px;font-weight:500}
pre{padding:16px;overflow-x:auto;font:.86rem/1.7 ui-monospace,Menlo,Consolas,monospace;color:#d6d6d6;tab-size:2;min-height:12.5em}
pre div{opacity:0;transform:translateY(4px);transition:.3s}
pre div.v{opacity:1;transform:none}
pre div:empty::after{content:" "}
.k{color:var(--ac)}.s{color:#86efac}.c0{color:#6b7280}.n{color:#fbbf24}
.demo{background:var(--card);border:1px solid var(--line);border-radius:14px;overflow:hidden}
.bar{display:flex;gap:6px;padding:10px 14px;border-bottom:1px solid var(--line);align-items:center;overflow-x:auto}
.bar b{margin-right:auto;color:var(--ac);white-space:nowrap}
.tab{background:none;border:0;color:var(--mu);padding:8px 12px;border-radius:8px;font:inherit;cursor:pointer;white-space:nowrap}
.tab[aria-selected=true]{background:var(--ac);color:var(--on)}
.pane{padding:16px;display:none}.pane.on{display:block}
.pl{display:flex;flex-wrap:wrap;gap:8px;align-items:center;padding:10px 0;border-bottom:1px solid var(--line)}
.pl:last-child{border:0}
.pl strong{flex:1;min-width:110px}
.sm{background:#161616;color:var(--tx);border:1px solid #333;border-radius:8px;padding:7px 11px;font:inherit;font-size:.85rem;cursor:pointer}
.sm:hover,.sm.on{border-color:var(--ac);color:var(--ac)}
.tg{display:flex;justify-content:space-between;align-items:center;padding:11px 0;border-bottom:1px solid var(--line)}
.sw{width:46px;height:26px;border-radius:99px;background:#2a2a2a;border:0;position:relative;cursor:pointer}
.sw::after{content:"";position:absolute;top:3px;left:3px;width:20px;height:20px;border-radius:50%;background:#fff;transition:transform .15s}
.sw[aria-pressed=true]{background:var(--ac)}
.sw[aria-pressed=true]::after{transform:translateX(20px)}
.log{background:#050505;border-top:1px solid var(--line);padding:12px 16px;font-size:.85rem;color:var(--mu);min-height:84px}
.log p+p{margin-top:2px}.log em{color:var(--ac);font-style:normal}
.lab{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:16px}
.lc{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:12px}
.lc input,.lc select{background:#111;color:var(--tx);border:1px solid #333;border-radius:10px;padding:11px 12px;font:inherit;flex:1;min-width:130px}
.cena{position:relative;height:230px;border-radius:12px;overflow:hidden;background:linear-gradient(#050505,#0d0d0d 70%,#161616 70%);border:1px solid var(--line)}
.bon{position:absolute;bottom:38px;left:8%;width:60px;display:flex;flex-direction:column;align-items:center;transition:left .9s ease}
.cena.perto .bon{left:calc(90% - 170px)}
.tag{white-space:nowrap;font-size:.78rem;font-weight:700;padding:3px 9px;border-radius:6px;background:#000;border:2px solid var(--ac);margin-bottom:6px}
.head{width:26px;height:26px;border-radius:6px;background:#d9d9d9}
.corpo{width:40px;height:44px;border-radius:6px;background:var(--ac);margin-top:2px}
.pernas{width:30px;height:26px;background:#333;border-radius:0 0 6px 6px}
.gate{position:absolute;right:10%;bottom:38px;width:96px;height:124px;border:2px solid #333;border-radius:6px;overflow:hidden;background:radial-gradient(var(--ac),#000)}
.gate i{position:absolute;top:0;bottom:0;width:50%;background:#1b1b1b;transition:transform .7s}
.gate i:first-child{left:0;border-right:1px solid #333}
.gate i:last-child{right:0}
.gate.open i:first-child{transform:translateX(-100%)}
.gate.open i:last-child{transform:translateX(100%)}
.st2{margin:10px 0 14px;min-height:1.4em;font-weight:700}
.st2.liberado{color:#22c55e}.st2.negado{color:#ef4444}
.grid{display:grid;gap:12px;grid-template-columns:repeat(auto-fit,minmax(250px,1fr))}
.c{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:18px}
.c h3{font-size:1.05rem;margin-bottom:4px}
.c p{color:var(--mu);font-size:.93rem}
.tagb{display:inline-block;font-size:.72rem;font-weight:700;padding:2px 8px;border-radius:99px;border:1px solid var(--ac);color:var(--ac);margin-bottom:8px}
.bv .sm{margin-top:12px}
.ped{background:var(--card);border:1px solid var(--ac);border-radius:14px;padding:20px}
.chk{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:14px}
.chk label{cursor:pointer}
.chk input{position:absolute;opacity:0}
.chk span{display:inline-block;padding:9px 14px;border-radius:99px;border:1px solid #333;background:#111;font-size:.92rem}
.chk input:checked+span{background:var(--ac);color:var(--on);border-color:var(--ac)}
.chk input:focus-visible+span{outline:3px solid #fff;outline-offset:2px}
.ped input[type=text],.ped textarea{width:100%;background:#111;color:var(--tx);border:1px solid #333;border-radius:10px;padding:12px;font:inherit;margin-bottom:12px}
.ped textarea{min-height:130px;resize:vertical}
.msg{margin-top:10px;color:var(--ac);font-size:.92rem;min-height:1.3em}
ol.st{list-style:none;padding:0;counter-reset:s;display:grid;gap:12px}
ol.st li{counter-increment:s;display:flex;gap:14px;align-items:flex-start;background:var(--card);border:1px solid var(--line);border-radius:12px;padding:16px}
ol.st li::before{content:counter(s);flex:none;width:30px;height:30px;border-radius:50%;background:var(--ac);color:var(--on);display:grid;place-items:center;font-weight:700}
ol.st b{display:block}
ol.st span{color:var(--mu);font-size:.93rem}
details{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:14px 16px;margin-bottom:10px}
summary{cursor:pointer;font-weight:700}
details p{color:var(--mu);margin-top:8px;font-size:.95rem}
.cta{text-align:center}
.cta h2{margin-bottom:16px}.cta .row{justify-content:center}
footer{color:var(--mu);text-align:center;font-size:.85rem;padding:30px 20px}
#ed{position:fixed;right:16px;bottom:16px;z-index:5}
#fx{position:fixed;left:16px;bottom:16px;z-index:5;display:none}
#fx.on{display:inline-block}
#pn{position:fixed;right:16px;bottom:74px;width:min(320px,calc(100vw - 32px));background:#0b0b0b;border:1px solid #333;border-radius:14px;padding:16px;display:none;z-index:6;max-height:70vh;overflow:auto}
#pn.on{display:block}
#pn h3{font-size:1rem;margin-bottom:10px}
.sws{display:grid;grid-template-columns:repeat(5,1fr);gap:10px;margin-bottom:14px}
.dot{aspect-ratio:1;border-radius:50%;border:2px solid #333;cursor:pointer;padding:0}
.dot[aria-pressed=true]{outline:3px solid #fff;outline-offset:2px}
.cp{display:flex;align-items:center;gap:10px;color:var(--mu);font-size:.9rem;margin-bottom:12px}
.cp input{width:52px;height:38px;border:0;background:none;padding:0;cursor:pointer}
#pn .btn{width:100%;text-align:center}
#md{position:fixed;inset:0;background:rgba(0,0,0,.85);display:none;place-items:center;z-index:9;padding:20px}
#md.on{display:grid}
#md .bx{background:#0b0b0b;border:1px solid #333;border-radius:14px;padding:22px;max-width:380px;width:100%}
#md h3{font-size:1.15rem;margin-bottom:6px}
#md p{color:var(--mu);font-size:.93rem}
#md .u{display:block;background:#161616;border:1px solid #2a2a2a;border-radius:8px;padding:10px;margin:14px 0;word-break:break-all;font-size:.9rem;color:var(--tx)}
#md .row{margin-top:16px}
:focus-visible{outline:3px solid #fff;outline-offset:2px}
@media (prefers-reduced-motion:reduce){*{transition:none!important;animation:none!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<div id="prog"></div>
<div class="w" id="app"></div>

<div id="md" role="dialog" aria-modal="true" aria-labelledby="mt">
  <div class="bx">
    <h3 id="mt">Link oficial do <span id="mn"></span> ✅</h3>
    <p>Pode entrar tranquilo. Este é o perfil de verdade do vendedor, não baixa nada e nunca pede sua senha.</p>
    <span class="u" id="mu"></span>
    <div class="row">
      <a class="btn pri" id="go" href="#" target="_blank" rel="noopener noreferrer">Abrir com segurança</a>
      <button class="btn sec" id="vl" type="button">Voltar</button>
    </div>
  </div>
</div>

<footer id="rod"></footer>
<a class="btn pri" id="fx" href="#pedido"></a>
<button class="btn pri" id="ed" aria-expanded="false" aria-controls="pn"></button>
<div id="pn" role="dialog" aria-label="Editar aparência">
  <h3>Cor do site</h3>
  <div class="sws" id="sws"></div>
  <label class="cp">Qualquer outra cor <input type="color" id="cc"></label>
  <button class="btn sec" id="rb" type="button" aria-pressed="false"></button>
</div>

<script>
(function(){
var C=CONFIG,ACC=C.corInicial,reduz=window.matchMedia('(prefers-reduced-motion: reduce)').matches;
var TK="https://www.tiktok.com/@"+encodeURIComponent(C.tiktokUser);
var RB=C.robloxLink||("https://www.roblox.com/search/users?keyword="+encodeURIComponent(C.robloxUser));
var app=document.getElementById('app');

function el(tag,cls,txt,par){var e=document.createElement(tag);if(cls)e.className=cls;if(txt!=null)e.textContent=txt;if(par)par.appendChild(e);return e}
function link(txt,href,cls,par){var a=el('a','btn '+cls,txt,par);a.href=href;a.target='_blank';a.rel='noopener';return a}
function sec(id,titulo,texto,cls){var s=el('section',cls||'',null,app);s.id=id;el('h2','',titulo,s);if(texto)el('p','sub',texto,s);return s}
function cards(par,lista,badge){var g=el('div','grid',null,par);lista.forEach(function(x){var c=el('div','c',null,g);if(badge)el('span','tagb',badge,c);el('h3','',x[0],c);el('p','',x[1],c)})}
function salvar(k,v){try{localStorage.setItem(k,v)}catch(e){}}
function ler(k){try{return localStorage.getItem(k)}catch(e){return null}}

// ===== topo =====
var h=el('header','',null,app);
var cv=el('canvas','fundo',null,h);cv.setAttribute('aria-hidden','true');
var h1=el('h1','',C.tituloInicio,h);var sp=el('span','',reduz?C.palavras[0]:'',h1);
el('p','lead',C.descricao,h);
var r=el('div','row',null,h);
el('a','btn pri big',C.botaoPedido,r).href='#pedido';
link(C.botaoTiktok,TK,'sec',r);
link('Roblox: '+C.robloxUser,RB,'sec',r);
var shb=el('button','btn sec',C.botaoCompartilhar,r);shb.type='button';
var shm=el('p','ok',C.frasesegura,h);shm.setAttribute('aria-live','polite');
function compartilhar(){
  var d={title:document.title,text:C.textoCompartilhar,url:location.href};
  if(navigator.share){navigator.share(d).catch(function(){})}
  else{try{navigator.clipboard.writeText(C.textoCompartilhar+' '+location.href);shm.textContent=C.linkCopiado}catch(e){}}
}
shb.onclick=compartilhar;

// digitando
if(!reduz){var pi=0,ci=0,del=false;(function digita(){
  var p=C.palavras[pi];ci+=del?-1:1;sp.textContent=p.slice(0,ci);var t=del?30:65;
  if(!del&&ci===p.length){del=true;t=1700}else if(del&&ci===0){del=false;pi=(pi+1)%C.palavras.length;t=300}
  setTimeout(digita,t)})()}

// partículas
if(!reduz){var cx=cv.getContext('2d'),ps=[],W=0,H=0;
  function ajusta(){W=cv.width=h.offsetWidth;H=cv.height=h.offsetHeight}
  ajusta();window.addEventListener('resize',ajusta);
  for(var i=0;i<38;i++)ps.push({x:Math.random()*W,y:Math.random()*H,vx:(Math.random()-.5)*.4,vy:(Math.random()-.5)*.4});
  (function anda(){
    cx.clearRect(0,0,W,H);cx.fillStyle=ACC;cx.strokeStyle=ACC;
    ps.forEach(function(p,i){
      p.x+=p.vx;p.y+=p.vy;if(p.x<0||p.x>W)p.vx*=-1;if(p.y<0||p.y>H)p.vy*=-1;
      cx.globalAlpha=.5;cx.beginPath();cx.arc(p.x,p.y,1.8,0,6.3);cx.fill();
      for(var j=i+1;j<ps.length;j++){var q=ps[j],dx=p.x-q.x,dy=p.y-q.y,dd=dx*dx+dy*dy;
        if(dd<14000){cx.globalAlpha=.16*(1-dd/14000);cx.beginPath();cx.moveTo(p.x,p.y);cx.lineTo(q.x,q.y);cx.stroke()}}
    });
    requestAnimationFrame(anda)})();
}

// faixa rolando
var fa=el('div','faixa',null,app),fi=el('div','',null,fa);fa.setAttribute('aria-hidden','true');
C.faixa.concat(C.faixa).forEach(function(t){el('span','',t,fi)});

// ===== janela de código =====
var sc=sec('codigo',C.codTitulo,C.codTexto),jn=el('div','jan',null,sc),jb=el('div','jb',null,jn);
el('i','',null,jb);el('i','',null,jb);el('i','',null,jb);el('b','',C.codArquivo,jb);
var pre=el('pre','',null,jn),lins=[];
function hl(t){return t.replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(
  /(--.*$)|("[^"]*")|\b(local|function|end|if|then|and|or|not|true|false|nil|return)\b|\b(\d+)\b/g,
  function(m,a,b,c,d){return a?'<span class="c0">'+a+'</span>':b?'<span class="s">'+b+'</span>':c?'<span class="k">'+c+'</span>':'<span class="n">'+d+'</span>'})}
C.codigo.forEach(function(l){var d=el('div','',null,pre);d.innerHTML=hl(l);lins.push(d)});
function mostra(){lins.forEach(function(d,i){setTimeout(function(){d.classList.add('v')},reduz?0:i*130)})}
if('IntersectionObserver' in window&&!reduz){var io=new IntersectionObserver(function(es){if(es[0].isIntersecting){mostra();io.disconnect()}},{threshold:.35});io.observe(jn)}else mostra();

// ===== demo painel ADM =====
var d=sec('demo',C.demoTitulo,C.demoTexto);
var dm=el('div','demo',null,d);
var bar=el('div','bar',null,dm);bar.setAttribute('role','tablist');
el('b','','Painel ADM',bar);
var panes=[];
var log=el('div','log',null,null);log.setAttribute('aria-live','polite');
function say(a,b){if(log.dataset.v!=='1'){log.innerHTML='';log.dataset.v='1'}
  var p=document.createElement('p');el('em','',a,p);p.appendChild(document.createTextNode(' '+b));log.insertBefore(p,log.firstChild);while(log.children.length>4)log.lastChild.remove()}
['Jogadores','Servidor','Avisos'].forEach(function(n,i){
  var t=el('button','tab',n,bar);t.setAttribute('role','tab');t.setAttribute('aria-selected',i===0);
  var p=el('div','pane'+(i===0?' on':''),null,dm);panes.push(p);
  t.onclick=function(){bar.querySelectorAll('.tab').forEach(function(x){x.setAttribute('aria-selected',x===t)});panes.forEach(function(q){q.classList.toggle('on',q===p)})}
});
C.jogadores.forEach(function(j){
  var l=el('div','pl',null,panes[0]);el('strong','',j,l);
  C.acoes.forEach(function(a){var b=el('button','sm',a,l);b.onclick=function(){say(a,'aplicado em '+j)}});
});
C.interruptores.forEach(function(s){
  var l=el('div','tg',null,panes[1]);el('span','',s[0],l);
  var b=el('button','sw',null,l);b.setAttribute('aria-pressed',s[1]);b.setAttribute('aria-label',s[0]);
  b.onclick=function(){var on=b.getAttribute('aria-pressed')!=='true';b.setAttribute('aria-pressed',on);say(s[0],on?'ligado':'desligado')}
});
[['Enviar aviso para todos','Enviar aviso','Aviso enviado em','todos'],['Reiniciar o servidor','Reiniciar','Reinício agendado em','servidor']].forEach(function(x){
  var l=el('div','pl',null,panes[2]);el('strong','',x[0],l);var b=el('button','sm',x[1],l);b.onclick=function(){say(x[1],x[2]+' '+x[3])}
});
dm.appendChild(log);el('p','','Nenhuma ação ainda. Toque em um botão acima.',log);

// ===== teste ao vivo =====
var s8=sec('lab',C.labTitulo,C.labTexto);
var lb=el('div','lab',null,s8),lc=el('div','lc',null,lb);
var ln=el('input','',null,lc);ln.type='text';ln.maxLength=14;ln.value=C.labNomePadrao;ln.setAttribute('aria-label','Seu nome');
var lp=el('select','',null,lc);lp.setAttribute('aria-label','Patente');
C.labPatentes.forEach(function(p,i){var o=el('option','',p[0],lp);o.value=i});
var lbt=el('button','btn sec','Aproximar do portão',lc);lbt.type='button';
var cena=el('div','cena',null,lb),bon=el('div','bon',null,cena),tg=el('div','tag',null,bon);
el('div','head',null,bon);el('div','corpo',null,bon);el('div','pernas',null,bon);
var gt=el('div','gate',null,cena);el('i','',null,gt);el('i','',null,gt);
var ls=el('p','st2',null,lb);ls.setAttribute('aria-live','polite');
var tmo;
function nomeLab(){return ln.value.trim()||C.labNomePadrao}
function patLab(){return C.labPatentes[+lp.value]}
function atualizarTag(){
  clearTimeout(tmo);var p=patLab();
  tg.textContent=nomeLab()+' | '+p[0];tg.style.borderColor=p[1];tg.style.color=p[1];
  cena.classList.remove('perto');gt.classList.remove('open');ls.textContent='';ls.className='st2';
}
ln.oninput=atualizarTag;lp.onchange=atualizarTag;atualizarTag();
lbt.onclick=function(){
  clearTimeout(tmo);cena.classList.add('perto');
  var ok=(+lp.value)>=C.labPatenteMin;
  tmo=setTimeout(function(){
    if(ok){gt.classList.add('open');ls.textContent='Acesso liberado para '+patLab()[0]+'.';ls.className='st2 liberado'}
    else{ls.textContent='Acesso negado. Precisa ser '+C.labPatentes[C.labPatenteMin][0]+' ou mais.';ls.className='st2 negado'}
    tmo=setTimeout(atualizarTag,3200);
  },900);
};
var lcta=el('a','btn pri big','Quero isso no meu jogo',lb);lcta.href='#pedido';
lcta.onclick=function(){
  [1,2].forEach(function(k){if(inputs[k])inputs[k].checked=true});
  montar();
  ta.value=ta.value.replace('\nPode me falar o valor?','\nQuero igual ao teste do site: tag "'+nomeLab()+' | '+patLab()[0]+'" e portão que só abre para '+C.labPatentes[C.labPatenteMin][0]+' ou mais.\n\nPode me falar o valor?');
};

// ===== catálogo =====
cards(sec('scripts',C.scriptsTitulo,C.scriptsTexto),C.scripts,'Pronto');

// ===== em breve + votos =====
var votos=[];try{votos=JSON.parse(ler('votos')||'[]')}catch(e){votos=[]}
var s9=sec('breve',C.breveTitulo,C.breveTexto),g9=el('div','grid',null,s9);
C.breve.forEach(function(x,i){
  var c=el('div','c bv',null,g9);el('span','tagb','Em breve',c);el('h3','',x[0],c);el('p','',x[1],c);
  var b=el('button','sm','Quero',c);b.type='button';b.setAttribute('aria-pressed',votos.indexOf(i)>-1);
  function pinta(){var on=votos.indexOf(i)>-1;b.classList.toggle('on',on);b.textContent=on?'Voto registrado ✓':'Quero';b.setAttribute('aria-pressed',on)}
  pinta();
  b.onclick=function(){var k=votos.indexOf(i);if(k>-1)votos.splice(k,1);else votos.push(i);salvar('votos',JSON.stringify(votos));pinta();montar()};
});

// ===== pedido =====
var s6=sec('pedido',C.pedidoTitulo,C.pedidoTexto);
var pd=el('div','ped',null,s6);
var ck=el('div','chk',null,pd);
var nomes=C.scripts.map(function(x){return x[0]}).concat([C.pedidoOutro]);
var inputs=nomes.map(function(n){var l=el('label','',null,ck);var i=el('input','',null,l);i.type='checkbox';i.value=n;el('span','',n,l);i.onchange=montar;return i});
var jg=el('input','',null,pd);jg.type='text';jg.placeholder=C.pedidoCampo;jg.setAttribute('aria-label',C.pedidoCampo);jg.oninput=montar;
var ta=el('textarea','',null,pd);ta.setAttribute('aria-label','Mensagem do pedido');
function montar(){
  var sel=inputs.filter(function(i){return i.checked}).map(function(i){return '- '+i.value});
  var t='Oi! Vi o seu site e quero fazer um pedido de script para Roblox Studio.\n';
  t+=sel.length?'\nQuero:\n'+sel.join('\n')+'\n':'\nQuero ver o que você tem para o meu jogo.\n';
  if(votos.length)t+='\nTambém quero quando ficar pronto:\n'+votos.map(function(i){return '- '+C.breve[i][0]}).join('\n')+'\n';
  if(jg.value.trim())t+='\nMeu jogo: '+jg.value.trim()+'\n';
  t+='\nPode me falar o valor?';
  ta.value=t;
}
montar();
var pb=link(C.pedidoBotao,TK,'pri big',pd);pb.style.marginTop='4px';
var ms=el('p','msg',null,pd);ms.setAttribute('aria-live','polite');
pb.addEventListener('click',function(){
  var t=ta.value,ok=false;
  try{navigator.clipboard.writeText(t);ok=true}catch(e){}
  if(!ok){try{ta.select();ok=document.execCommand('copy')}catch(e){}}
  ms.textContent=ok?C.pedidoCopiado:'';
});

// ===== venda, segurança, depoimentos, faq =====
var s2=sec('como',C.vendaTitulo,C.vendaTexto);var ol=el('ol','st',null,s2);
C.passos.forEach(function(x){var li=el('li','',null,ol);var dv=el('div','',null,li);el('b','',x[0],dv);el('span','',x[1],dv)});
cards(sec('seguranca',C.segTitulo,C.segTexto),C.seguranca);
if(C.depoimentos&&C.depoimentos.length){cards(sec('dep',C.depTitulo),C.depoimentos.map(function(x){return [x[0],'“'+x[1]+'”']}))}
var s7=sec('faq',C.faqTitulo);
C.faq.forEach(function(x){var dt=el('details','',null,s7);el('summary','',x[0],dt);el('p','',x[1],dt)});

// ===== final =====
var s4=el('section','cta',null,app);el('h2','',C.ctaTitulo,s4);
var r4=el('div','row',null,s4);link(C.botaoTiktok,TK,'pri big',r4);link('Roblox: '+C.robloxUser,RB,'sec',r4);
var sh2=el('button','btn sec',C.botaoCompartilhar,r4);sh2.type='button';sh2.onclick=compartilhar;
var tx=el('p','sub','TikTok: @'+C.tiktokUser,s4);tx.style.margin='18px auto 0';

document.getElementById('rod').textContent=C.rodape;
document.title=C.tituloInicio+C.palavras[0];

// ===== barra de progresso + botão fixo =====
var fx=document.getElementById('fx'),pg=document.getElementById('prog');fx.textContent=C.botaoFixo;
function rolou(){
  var y=window.scrollY||document.documentElement.scrollTop,t=document.documentElement.scrollHeight-window.innerHeight;
  pg.style.width=(t>0?y/t*100:0)+'%';
  var pe=document.getElementById('pedido').getBoundingClientRect();
  fx.classList.toggle('on',y>500&&!(pe.top<window.innerHeight&&pe.bottom>0));
}
window.addEventListener('scroll',rolou,{passive:true});rolou();

// ===== aparência =====
var root=document.documentElement,sws=document.getElementById('sws'),cc=document.getElementById('cc'),ed=document.getElementById('ed'),pn=document.getElementById('pn'),rb=document.getElementById('rb');
ed.textContent=C.botaoAparencia;rb.textContent=C.botaoArcoiris;
function aplicar(c,guarda){
  ACC=c;root.style.setProperty('--ac',c);
  var R=parseInt(c.substr(1,2),16),G=parseInt(c.substr(3,2),16),B=parseInt(c.substr(5,2),16);
  root.style.setProperty('--on',(R*299+G*587+B*114)/1000>150?'#000':'#fff');
  cc.value=c;
  sws.querySelectorAll('.dot').forEach(function(x){x.setAttribute('aria-pressed',x.dataset.c===c)});
  if(guarda!==false)salvar('cor',c);
}
C.cores.forEach(function(x){var b=el('button','dot',null,sws);b.style.background=x[1];b.dataset.c=x[1];b.title=x[0];b.setAttribute('aria-label',x[0]);b.setAttribute('aria-pressed','false');b.onclick=function(){parar();aplicar(x[1])}});
cc.oninput=function(){parar();aplicar(cc.value)};
ed.onclick=function(){var o=pn.classList.toggle('on');ed.setAttribute('aria-expanded',o)};
var salva=ler('cor');
aplicar(/^#[0-9a-f]{6}$/i.test(salva||'')?salva:C.corInicial);

// modo arco-íris
var arco=null,hue=0;
function hslHex(h,s,l){s/=100;l/=100;var k=function(n){return(n+h/30)%12},a=s*Math.min(l,1-l),f=function(n){var v=l-a*Math.max(-1,Math.min(k(n)-3,Math.min(9-k(n),1)));return Math.round(255*v).toString(16).padStart(2,'0')};return '#'+f(0)+f(8)+f(4)}
function parar(){if(arco){clearInterval(arco);arco=null;rb.classList.remove('on');rb.setAttribute('aria-pressed','false')}}
rb.onclick=function(){
  if(arco){parar();aplicar(ler('cor')||C.corInicial);return}
  rb.classList.add('on');rb.setAttribute('aria-pressed','true');
  arco=setInterval(function(){hue=(hue+3)%360;aplicar(hslHex(hue,90,60),false)},60);
};

// ===== links externos com aviso =====
var md=document.getElementById('md'),go=document.getElementById('go');
function fechar(){md.classList.remove('on')}
document.querySelectorAll('a[target=_blank]').forEach(function(a){
  if(a===go)return;
  a.addEventListener('click',function(e){
    e.preventDefault();
    var tik=a.href.indexOf('tiktok')>-1;
    document.getElementById('mn').textContent=tik?'TikTok':'Roblox';
    document.getElementById('mu').textContent=tik?'@'+C.tiktokUser+' no TikTok':C.robloxUser+' no Roblox';
    go.href=a.href;md.classList.add('on');go.focus();
  });
});
go.addEventListener('click',function(){setTimeout(fechar,200)});
document.getElementById('vl').onclick=fechar;
md.addEventListener('click',function(e){if(e.target===md)fechar()});
document.addEventListener('keydown',function(e){if(e.key==='Escape')fechar()});
})();
</script>
</body>
</html>
