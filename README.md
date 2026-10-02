<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Scripts para Roblox Studio</title>
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
  botaoFixo: "Pedir meu script",

  // topo
  tituloInicio: "Seu jogo no Roblox com ",
  tituloDestaque: "scripts que o jogador nota",
  descricao: "Painel ADM, patentes, portões, spawn por base, painel de festa e mais. Eu faço o script sob medida, você cola no Roblox Studio e ele funciona.",
  botaoPedido: "Montar meu pedido",
  frasesegura: "Site seguro: não baixa arquivos e não pede senha.",

  // faixa de vantagens (use só o que é verdade)
  vantagens: [
    ["Sob medida","feito para o seu jogo"],
    ["Mobile e PC","funciona nos dois"],
    ["Ajuste incluso","se não funcionar, eu arrumo"],
    ["Passo a passo","eu mostro onde colar"]
  ],

  // demonstração do painel ADM
  demoTitulo: "Teste um painel ADM agora",
  demoTexto: "Isto é uma demonstração. Toque nos botões e veja como o painel responde dentro do jogo.",
  jogadores: ["Jogador_01","Jogador_02","Jogador_03"],
  acoes: ["Expulsar","Voar","Velocidade"],
  interruptores: [["Chat liberado",true],["Portões abertos",false],["Modo noite",false]],

  // scripts à venda
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

  // sem script x com script
  compTitulo: "A diferença no seu jogo",
  semScript: ["Você configura tudo na mão","Qualquer pessoa entra em qualquer lugar","Sem controle de quem manda no jogo","Menus simples e sem identidade"],
  comScript: ["Tudo pronto e funcionando","Portões só para quem tem permissão","Painel ADM para controlar o servidor","Interface bonita e com a sua cor"],

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

  // depoimentos: coloque só os de clientes reais. Formato ["Nome","O que disse"]. Vazio = seção escondida
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
header{padding:70px 0 40px;position:relative}
header::before{content:"";position:absolute;left:50%;top:-120px;width:680px;height:480px;max-width:140vw;transform:translateX(-50%);background:radial-gradient(closest-side,var(--ac),transparent);opacity:.2;pointer-events:none;animation:glow 5s ease-in-out infinite alternate}
@keyframes glow{from{opacity:.12}to{opacity:.28}}
header>*{position:relative}
h1{font-size:clamp(2.2rem,8vw,4.2rem);line-height:1.02;letter-spacing:-.035em;max-width:14ch}
h1 span{color:var(--ac)}
.lead{color:var(--mu);max-width:50ch;margin:18px 0 26px;font-size:1.08rem}
.row{display:flex;flex-wrap:wrap;gap:10px}
.btn{display:inline-block;padding:14px 20px;border-radius:10px;font-weight:700;font-size:.95rem;font-family:inherit;text-decoration:none;border:2px solid var(--ac);cursor:pointer}
.pri{background:var(--ac);color:var(--on)}
.big{padding:16px 24px;font-size:1.02rem;animation:pulso 2.4s ease-in-out infinite}
@keyframes pulso{0%,100%{box-shadow:0 0 0 0 transparent}50%{box-shadow:0 0 0 8px color-mix(in srgb,var(--ac) 25%,transparent)}}
.sec{background:transparent;color:var(--tx)}
.sec:hover{background:var(--ac);color:var(--on)}
section{padding:46px 0;border-top:1px solid var(--line)}
h2{font-size:1.75rem;letter-spacing:-.02em;margin-bottom:6px}
.sub{color:var(--mu);margin-bottom:22px;max-width:56ch}
.ok{color:var(--mu);font-size:.85rem;margin-top:14px}
.vant{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:1px;background:var(--line);border:1px solid var(--line);border-radius:12px;overflow:hidden;margin:6px 0 10px}
.vant div{background:var(--card);padding:16px}
.vant b{display:block;color:var(--ac)}
.vant span{color:var(--mu);font-size:.88rem}
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
.sm:hover{border-color:var(--ac);color:var(--ac)}
.tg{display:flex;justify-content:space-between;align-items:center;padding:11px 0;border-bottom:1px solid var(--line)}
.sw{width:46px;height:26px;border-radius:99px;background:#2a2a2a;border:0;position:relative;cursor:pointer}
.sw::after{content:"";position:absolute;top:3px;left:3px;width:20px;height:20px;border-radius:50%;background:#fff;transition:transform .15s}
.sw[aria-pressed=true]{background:var(--ac)}
.sw[aria-pressed=true]::after{transform:translateX(20px)}
.log{background:#050505;border-top:1px solid var(--line);padding:12px 16px;font-size:.85rem;color:var(--mu);min-height:84px}
.log p+p{margin-top:2px}.log em{color:var(--ac);font-style:normal}
.grid{display:grid;gap:12px;grid-template-columns:repeat(auto-fit,minmax(250px,1fr))}
.c{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:18px}
.c h3{font-size:1.05rem;margin-bottom:4px}
.c p{color:var(--mu);font-size:.93rem}
.vs{display:grid;gap:12px;grid-template-columns:repeat(auto-fit,minmax(260px,1fr))}
.vs .c ul{list-style:none;padding:0;display:grid;gap:8px;margin-top:10px}
.vs .c li{display:flex;gap:10px;font-size:.95rem}
.vs .nao{opacity:.75}.vs .nao li::before{content:"✕";color:#ef4444;font-weight:700}
.vs .sim{border-color:var(--ac)}.vs .sim li::before{content:"✓";color:var(--ac);font-weight:700}
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
.cp{display:flex;align-items:center;gap:10px;color:var(--mu);font-size:.9rem}
.cp input{width:52px;height:38px;border:0;background:none;padding:0;cursor:pointer}
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
</div>

<script>
(function(){
var C=CONFIG;
var TK="https://www.tiktok.com/@"+encodeURIComponent(C.tiktokUser);
var RB=C.robloxLink||("https://www.roblox.com/search/users?keyword="+encodeURIComponent(C.robloxUser));
var app=document.getElementById('app');

function el(tag,cls,txt,par){var e=document.createElement(tag);if(cls)e.className=cls;if(txt!=null)e.textContent=txt;if(par)par.appendChild(e);return e}
function link(txt,href,cls,par){var a=el('a','btn '+cls,txt,par);a.href=href;a.target='_blank';a.rel='noopener';return a}
function sec(id,titulo,texto,cls){var s=el('section',cls||'',null,app);s.id=id;el('h2','',titulo,s);if(texto)el('p','sub',texto,s);return s}
function cards(par,lista){var g=el('div','grid',null,par);lista.forEach(function(x){var c=el('div','c',null,g);el('h3','',x[0],c);el('p','',x[1],c)})}

// topo
var h=el('header','',null,app);
var h1=el('h1','',C.tituloInicio,h);el('span','',C.tituloDestaque,h1);
el('p','lead',C.descricao,h);
var r=el('div','row',null,h);
var bp=el('a','btn pri big',C.botaoPedido,r);bp.href='#pedido';
link(C.botaoTiktok,TK,'sec',r);
link('Roblox: '+C.robloxUser,RB,'sec',r);
el('p','ok',C.frasesegura,h);

// vantagens
var v=el('div','vant',null,app);
C.vantagens.forEach(function(x){var d=el('div','',null,v);el('b','',x[0],d);el('span','',x[1],d)});

// demo
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

// scripts
cards(sec('scripts',C.scriptsTitulo,C.scriptsTexto),C.scripts);

// sem x com
var s5=sec('comp',C.compTitulo);var vs=el('div','vs',null,s5);
[['Sem script',C.semScript,'nao'],['Com o meu script',C.comScript,'sim']].forEach(function(x){
  var c=el('div','c '+x[2],null,vs);el('h3','',x[0],c);var u=el('ul','',null,c);x[1].forEach(function(t){el('li','',t,u)})});

// pedido
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

// venda
var s2=sec('como',C.vendaTitulo,C.vendaTexto);var ol=el('ol','st',null,s2);
C.passos.forEach(function(x){var li=el('li','',null,ol);var dv=el('div','',null,li);el('b','',x[0],dv);el('span','',x[1],dv)});

// segurança
cards(sec('seguranca',C.segTitulo,C.segTexto),C.seguranca);

// depoimentos reais
if(C.depoimentos&&C.depoimentos.length){cards(sec('dep',C.depTitulo),C.depoimentos.map(function(x){return [x[0],'“'+x[1]+'”']}))}

// faq
var s7=sec('faq',C.faqTitulo);
C.faq.forEach(function(x){var dt=el('details','',null,s7);el('summary','',x[0],dt);el('p','',x[1],dt)});

// final
var s4=el('section','cta',null,app);el('h2','',C.ctaTitulo,s4);
var r4=el('div','row',null,s4);link(C.botaoTiktok,TK,'pri big',r4);link('Roblox: '+C.robloxUser,RB,'sec',r4);
var tx=el('p','sub','TikTok: @'+C.tiktokUser,s4);tx.style.margin='18px auto 0';

document.getElementById('rod').textContent=C.rodape;
document.title=C.tituloInicio+C.tituloDestaque;

// botão fixo
var fx=document.getElementById('fx');fx.textContent=C.botaoFixo;
function topo(){var y=window.scrollY||document.documentElement.scrollTop;var pe=document.getElementById('pedido').getBoundingClientRect();
  fx.classList.toggle('on',y>500&&!(pe.top<window.innerHeight&&pe.bottom>0))}
window.addEventListener('scroll',topo,{passive:true});topo();

// aparência
var root=document.documentElement,sws=document.getElementById('sws'),cc=document.getElementById('cc'),ed=document.getElementById('ed'),pn=document.getElementById('pn');
ed.textContent=C.botaoAparencia;
function aplicar(c){
  root.style.setProperty('--ac',c);
  var R=parseInt(c.substr(1,2),16),G=parseInt(c.substr(3,2),16),B=parseInt(c.substr(5,2),16);
  root.style.setProperty('--on',(R*299+G*587+B*114)/1000>150?'#000':'#fff');
  cc.value=c;
  sws.querySelectorAll('.dot').forEach(function(x){x.setAttribute('aria-pressed',x.dataset.c===c)});
  try{localStorage.setItem('cor',c)}catch(e){}
}
C.cores.forEach(function(x){var b=el('button','dot',null,sws);b.style.background=x[1];b.dataset.c=x[1];b.title=x[0];b.setAttribute('aria-label',x[0]);b.setAttribute('aria-pressed','false');b.onclick=function(){aplicar(x[1])}});
cc.oninput=function(){aplicar(cc.value)};
ed.onclick=function(){var o=pn.classList.toggle('on');ed.setAttribute('aria-expanded',o)};
var salva=null;try{salva=localStorage.getItem('cor')}catch(e){}
aplicar(/^#[0-9a-f]{6}$/i.test(salva||'')?salva:C.corInicial);

// links externos com aviso
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
