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
  robloxLink: "",                         // se tiver o link do perfil, cole aqui. Vazio = busca pelo usuário
  botaoTiktok: "ENTRAR EM CONTATO TIKTOK",

  // aparência
  corInicial: "#8b5cf6",
  cores: [
    ["Roxo","#8b5cf6"],["Azul","#3b82f6"],["Amarelo","#facc15"],["Magenta","#ff00cc"],["Branco","#ffffff"],
    ["Vermelho","#ef4444"],["Laranja","#fb923c"],["Verde","#22c55e"],["Ciano","#06b6d4"],["Rosa","#f472b6"],
    ["Lima","#a3e635"],["Turquesa","#14b8a6"],["Dourado","#d4af37"],["Azul-marinho","#1e40af"],["Cinza","#9ca3af"]
  ],
  botaoAparencia: "Editar aparência",

  // topo
  tituloInicio: "Scripts prontos para o seu jogo no ",
  tituloDestaque: "Roblox Studio",
  descricao: "Painel ADM, sistema de patentes, portões, spawn por base, painel de festa e mais. Eu faço o script, você cola no seu jogo e ele funciona.",
  frasesegura: "Site seguro: não baixa arquivos e não pede senha.",

  // demonstração do painel ADM
  demoTitulo: "Teste um painel ADM",
  demoTexto: "Esta é uma demonstração. Clique nos botões para ver como o painel responde dentro do jogo.",
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

  // final
  ctaTitulo: "Quer um script para o seu jogo?",
  rodape: "Não tenho ligação com a Roblox Corporation. Roblox e Roblox Studio são marcas da Roblox Corporation."
};
</script>
<!-- ============ FIM DAS CONFIGURAÇÕES ============ -->

<style>
:root{--ac:#8b5cf6;--on:#fff;--bg:#000;--card:#0d0d0d;--line:#222;--tx:#f2f2f2;--mu:#9a9a9a}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--tx);font-family:"Space Grotesk",system-ui,sans-serif;line-height:1.55;padding-bottom:80px}
a{color:inherit}
.w{max-width:960px;margin:0 auto;padding:0 20px}
header{padding:64px 0 40px}
h1{font-size:clamp(2.1rem,7vw,3.8rem);line-height:1.05;letter-spacing:-.03em;max-width:15ch}
h1 span{color:var(--ac)}
.lead{color:var(--mu);max-width:52ch;margin:18px 0 26px;font-size:1.05rem}
.row{display:flex;flex-wrap:wrap;gap:10px}
.btn{display:inline-block;padding:14px 20px;border-radius:10px;font-weight:700;font-size:.95rem;font-family:inherit;text-decoration:none;border:2px solid var(--ac);cursor:pointer}
.pri{background:var(--ac);color:var(--on)}
.sec{background:transparent;color:var(--tx)}
.sec:hover{background:var(--ac);color:var(--on)}
section{padding:44px 0;border-top:1px solid var(--line)}
h2{font-size:1.7rem;letter-spacing:-.02em;margin-bottom:6px}
.sub{color:var(--mu);margin-bottom:22px;max-width:56ch}
.ok{color:var(--mu);font-size:.85rem;margin-top:12px}
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
ol.st{list-style:none;padding:0;counter-reset:s;display:grid;gap:12px}
ol.st li{counter-increment:s;display:flex;gap:14px;align-items:flex-start;background:var(--card);border:1px solid var(--line);border-radius:12px;padding:16px}
ol.st li::before{content:counter(s);flex:none;width:30px;height:30px;border-radius:50%;background:var(--ac);color:var(--on);display:grid;place-items:center;font-weight:700}
ol.st b{display:block}
ol.st span{color:var(--mu);font-size:.93rem}
.cta{text-align:center}
.cta h2{margin-bottom:16px}.cta .row{justify-content:center}
footer{color:var(--mu);text-align:center;font-size:.85rem;padding:30px 20px}
#ed{position:fixed;right:16px;bottom:16px;z-index:5}
#pn{position:fixed;right:16px;bottom:74px;width:min(320px,calc(100vw - 32px));background:#0b0b0b;border:1px solid #333;border-radius:14px;padding:16px;display:none;z-index:5;max-height:70vh;overflow:auto}
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
@media (prefers-reduced-motion:reduce){*{transition:none!important;scroll-behavior:auto!important}}
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

function el(tag,cls,txt,par){var e=document.createElement(tag);if(cls)e.className=cls;if(txt!=null)e.textContent=txt;if(par)par.appendChild(e);return e}
function link(txt,href,cls,par){var a=el('a','btn '+cls,txt,par);a.href=href;a.target='_blank';a.rel='noopener';return a}
function sec(id,titulo,texto,cls){var s=el('section',cls||'',null,app);s.id=id;el('h2','',titulo,s);if(texto)el('p','sub',texto,s);return s}

var app=document.getElementById('app');

// topo
var h=el('header','',null,app);
var h1=el('h1','',C.tituloInicio,h);el('span','',C.tituloDestaque,h1);
el('p','lead',C.descricao,h);
var r=el('div','row',null,h);
link(C.botaoTiktok,TK,'pri',r);
link('Perfil no Roblox: '+C.robloxUser,RB,'sec',r);
el('p','ok',C.frasesegura,h);

// demo
var d=sec('demo',C.demoTitulo,C.demoTexto);
var dm=el('div','demo',null,d);
var bar=el('div','bar',null,dm);bar.setAttribute('role','tablist');
el('b','','Painel ADM',bar);
var abas=['Jogadores','Servidor','Avisos'],panes=[];
var log=el('div','log',null,null);log.setAttribute('aria-live','polite');
function say(a,b){if(log.dataset.v!=='1'){log.innerHTML='';log.dataset.v='1'}
  var p=document.createElement('p');el('em','',a,p);p.appendChild(document.createTextNode(' '+b));log.insertBefore(p,log.firstChild);while(log.children.length>4)log.lastChild.remove()}
abas.forEach(function(n,i){
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
dm.appendChild(log);el('p','',null,log).textContent='Nenhuma ação ainda. Toque em um botão acima.';

// scripts
var s1=sec('scripts',C.scriptsTitulo,C.scriptsTexto);var g1=el('div','grid',null,s1);
C.scripts.forEach(function(x){var c=el('div','c',null,g1);el('h3','',x[0],c);el('p','',x[1],c)});

// venda
var s2=sec('como',C.vendaTitulo,C.vendaTexto);var ol=el('ol','st',null,s2);
C.passos.forEach(function(x){var li=el('li','',null,ol);var dv=el('div','',null,li);el('b','',x[0],dv);el('span','',x[1],dv)});

// segurança
var s3=sec('seguranca',C.segTitulo,C.segTexto);var g3=el('div','grid',null,s3);
C.seguranca.forEach(function(x){var c=el('div','c',null,g3);el('h3','',x[0],c);el('p','',x[1],c)});

// final
var s4=el('section','cta',null,app);el('h2','',C.ctaTitulo,s4);
var r4=el('div','row',null,s4);link(C.botaoTiktok,TK,'pri',r4);link('Roblox: '+C.robloxUser,RB,'sec',r4);
var tx=el('p','sub','TikTok: @'+C.tiktokUser,s4);tx.style.margin='18px auto 0';

document.getElementById('rod').textContent=C.rodape;
document.title=C.tituloInicio+C.tituloDestaque;

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
