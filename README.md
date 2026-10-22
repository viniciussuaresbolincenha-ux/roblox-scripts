<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Lumex Forge | Scripts para Roblox Studio</title>
<meta name="description" content="Scripts prontos para Roblox Studio: roleplay, Exército RP, pets, anime RPG, tiro, terror e mais. Pacotes com desconto, Pix ou Robux.">
<meta name="theme-color" content="#0a0a0b">
<meta property="og:type" content="website">
<meta property="og:title" content="Lumex Forge | Scripts para Roblox Studio">
<meta property="og:description" content="Sistemas prontos para o seu jogo no Roblox Studio, com pacotes e desconto. Pague com Pix ou Robux.">
<meta name="twitter:card" content="summary">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22%3E%3Ctext y=%22.9em%22 font-size=%2290%22%3E💎%3C/text%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;900&family=Playfair+Display:wght@600;700;800&display=swap" rel="stylesheet">
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
.topbar{background:var(--tint);border-bottom:1px solid var(--line);font-size:13px;color:var(--mut);padding:8px 0}
.topbar .wrap{display:flex;gap:6px 18px;justify-content:center;flex-wrap:wrap;align-items:center}
.topbar a{color:var(--gold2);font-weight:600}
.topbar a:hover{text-decoration:underline}
.hero .hero-contact{margin:40px auto 0;padding-top:28px;border-top:1px solid var(--line);max-width:560px}
.hero .hero-contact p{margin:0 0 16px;font-size:14px;max-width:none}
.hero-contact .btn{margin:0 5px 10px}
.box input{width:100%;background:var(--bg);border:1px solid var(--line);border-radius:10px;padding:12px;color:var(--txt);font:inherit;margin-bottom:8px}
.box input:focus{outline:none;border-color:var(--gold)}
.err{color:#ff7a7a;font-size:13px;min-height:18px;margin:2px 0 6px}
.vpill{display:inline-block;background:hsl(var(--h) 55% 20%);border:1px solid hsl(var(--h) 70% 52%);color:hsl(var(--h) 90% 84%);border-radius:99px;padding:3px 10px;font-size:12px;font-weight:700;white-space:nowrap}
.vtag{position:fixed;left:12px;bottom:12px;z-index:30;background:var(--card);border:1px solid var(--line);border-radius:99px;padding:6px 12px;display:flex;gap:8px;align-items:center}
.vtag small{color:var(--mut);font-size:11px}
.note{font-size:12px;color:var(--mut);margin:6px 0 12px}
.admlink{color:var(--mut);font-size:12px;cursor:pointer;display:inline-block;margin-top:10px}
.admlink:hover{color:var(--gold2)}
.adm{position:fixed;inset:0;background:var(--bg);z-index:100;display:none;overflow:auto;padding:16px}
.adm.open{display:block}
.adm-top{display:flex;gap:10px;align-items:center;flex-wrap:wrap;margin-bottom:16px}
.adm-top b{font-size:18px}
.admmodo{font-size:12px;color:var(--mut)}
.grow{flex:1}
.adm-login{display:flex;justify-content:center;margin-top:50px}
.adm-login .box{max-width:380px;width:100%}
.adm-tabs{display:flex;gap:8px;margin-bottom:14px}
.adm-tabs .chip b{margin-left:6px;background:var(--gold);color:#111;border-radius:99px;padding:1px 8px;font-size:11px}
.kan{display:grid;grid-auto-flow:column;grid-auto-columns:minmax(290px,1fr);gap:14px;overflow-x:auto;padding-bottom:14px;align-items:start}
.col{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:12px}
.col h4{font-size:13px;margin-bottom:10px;display:flex;justify-content:space-between}
.col h4 span{color:var(--mut)}
.vazio{color:var(--mut);font-size:12px;text-align:center;padding:14px}
.oc{background:var(--bg);border:1px solid var(--line);border-radius:12px;padding:12px;margin-bottom:10px;font-size:13px}
.oc.new{border-color:var(--gold);animation:pulseb 2s ease-in-out infinite}
@keyframes pulseb{0%,100%{box-shadow:0 0 0 0 transparent}50%{box-shadow:0 0 14px color-mix(in srgb,var(--gold) 45%,transparent)}}
.ocTop{display:flex;justify-content:space-between;align-items:center;margin-bottom:8px}
.ocTop small,.vrow small{color:var(--mut)}
.ocMeta,.ocCont{color:var(--mut);margin-top:4px}
.ocCont a{color:var(--gold2);margin-left:6px}
.oc details{margin-top:10px}
.oc summary{cursor:pointer;color:var(--gold2);font-weight:600}
.oc textarea{width:100%;background:var(--card);border:1px solid var(--line);border-radius:8px;color:var(--txt);font:12px/1.45 Inter,sans-serif;padding:8px;margin-top:8px;resize:vertical}
.ocBtns{display:flex;flex-wrap:wrap;gap:6px;margin-top:10px}
.ocBtns button{background:var(--card);border:1px solid var(--line);color:var(--txt);border-radius:8px;padding:8px 10px;font:600 12px Inter,sans-serif;cursor:pointer}
.ocBtns button:hover{border-color:var(--gold)}
.ocBtns .bad:hover{border-color:#ff5a5a;color:#ff9a9a}
.vrow{display:flex;gap:12px;align-items:center;flex-wrap:wrap;padding:10px 0;border-bottom:1px solid var(--line);font-size:13px}
.comp{color:var(--gold2)}
.toast{position:fixed;right:16px;top:16px;z-index:200;background:var(--card);border:1px solid var(--gold);border-radius:12px;padding:14px 18px;max-width:320px;box-shadow:0 10px 30px rgba(0,0,0,.6);font-size:14px}
.box{max-height:92vh;overflow:auto}
#mQr{background:#fff;padding:10px;border-radius:12px;display:table;margin:0 auto 12px}
#mQr:empty{display:none}
#mPixCod{width:100%;background:var(--bg);border:1px solid var(--line);border-radius:10px;color:var(--mut);font:11px/1.4 monospace;padding:8px;margin-bottom:10px;resize:none}
.vtag{font:inherit;color:inherit;cursor:pointer}
.vtag:hover{border-color:var(--gold)}
.bot{position:fixed;left:12px;bottom:64px;z-index:40;width:340px;max-width:calc(100vw - 24px);max-height:72vh;background:var(--card);border:1px solid var(--tint2);border-radius:16px;box-shadow:0 20px 50px rgba(0,0,0,.6);display:none;flex-direction:column;overflow:hidden}
.bot.open{display:flex}
.bot-h{display:flex;justify-content:space-between;align-items:center;padding:12px 14px;background:var(--tint);border-bottom:1px solid var(--line);font-size:14px}
.bot-h button{background:none;border:0;color:var(--mut);cursor:pointer;font-size:16px}
.bot-b{padding:14px;overflow:auto;flex:1;display:flex;flex-direction:column;gap:8px;min-height:120px}
.bm{max-width:88%;padding:9px 12px;border-radius:12px;font-size:13px;line-height:1.5}
.bm.bot{background:var(--bg);border:1px solid var(--line);align-self:flex-start}
.bm.eu{background:var(--gold);color:#111;align-self:flex-end;font-weight:600}
.bot-f{padding:10px;border-top:1px solid var(--line);display:flex;flex-wrap:wrap;gap:6px;max-height:34vh;overflow:auto}
.bot-f button{background:var(--bg);border:1px solid var(--line);color:var(--txt);border-radius:99px;padding:8px 12px;font:600 12px Inter,sans-serif;cursor:pointer}
.bot-f button:hover{border-color:var(--gold);color:var(--gold2)}
.bot-f input{flex:1;min-width:0;background:var(--bg);border:1px solid var(--line);border-radius:10px;padding:9px 11px;color:var(--txt);font:13px Inter,sans-serif}
.bot-f input:focus{outline:none;border-color:var(--gold)}
.onl{display:flex;flex-wrap:wrap;gap:8px 14px;align-items:center;margin-bottom:16px}
.onl small{color:var(--mut);margin-left:-6px}
.intgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(290px,1fr));gap:14px}
@media(max-width:760px){.vtag .vt-s{display:none}.kan{grid-auto-columns:88%}}
.cb{position:relative;background:linear-gradient(160deg,var(--tint),var(--card));border-color:var(--tint2)}
.cb.top{border-color:var(--gold)}
.cb .off{position:absolute;top:16px;right:16px;background:var(--gold);color:#111;font-weight:900;font-size:13px;border-radius:8px;padding:4px 10px}
.cb .de{color:var(--mut);text-decoration:line-through;font-size:13px}
.cb .eco{color:var(--gold2);font-size:13px;font-weight:600;margin-bottom:12px}
.trust{padding:26px 0;border-top:1px solid var(--line);border-bottom:1px solid var(--line)}
.tr{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:18px}
.tr b{display:block;font-size:14px;margin-bottom:2px}
.tr span{color:var(--mut);font-size:13px}
.free{display:none;align-items:center;justify-content:space-between;gap:14px;flex-wrap:wrap;background:linear-gradient(135deg,var(--tint),var(--card));border:1px solid var(--gold);border-radius:14px;padding:16px 20px;margin-bottom:26px}
.tools select{background:var(--card);border:1px solid var(--line);border-radius:10px;padding:12px;color:var(--txt);font:inherit;cursor:pointer}
.cbtns{display:flex;gap:8px}
.card .cbtns .btn{flex:1;width:auto;padding:12px 8px}
.demo{display:inline-block;font-size:13px;color:var(--gold2);font-weight:600;margin-bottom:12px}
.cupom{display:flex;gap:8px;align-items:center;margin-top:6px}
.cupom input{margin:0}
.cartbtn{position:fixed;right:14px;bottom:14px;z-index:44;display:none;align-items:center;gap:8px;background:var(--gold);color:#111;border:0;border-radius:99px;padding:12px 18px;font:800 14px Inter,sans-serif;cursor:pointer;box-shadow:0 8px 24px rgba(0,0,0,.5)}
.cart{position:fixed;top:0;right:0;bottom:0;width:360px;max-width:100vw;background:var(--card);border-left:1px solid var(--line);z-index:46;display:flex;flex-direction:column;transform:translateX(100%);transition:transform .25s}
.cart.open{transform:none}
.cart-h{display:flex;justify-content:space-between;align-items:center;padding:16px;border-bottom:1px solid var(--line)}
.cart-h button{background:none;border:0;color:var(--mut);font-size:18px;cursor:pointer}
.cart-b{flex:1;overflow:auto;padding:8px 16px}
.cart-f{padding:16px;border-top:1px solid var(--line)}
.ci{display:flex;gap:10px;align-items:center;padding:10px 0;border-bottom:1px solid var(--line);font-size:13px}
.ci span{flex:1}
.ci button{background:none;border:0;color:var(--mut);cursor:pointer}
.crow{display:flex;justify-content:space-between;font-size:14px;margin-bottom:6px}
.crow.eco{color:var(--gold2)}
.crow.tot{font-size:17px;margin:10px 0 14px}
.nudge{background:var(--tint);border:1px solid var(--tint2);border-radius:10px;padding:10px 12px;font-size:13px;margin-bottom:12px}
:focus-visible{outline:2px solid var(--gold2);outline-offset:2px}
.card{position:relative}
.more{text-align:center;margin-top:22px}
.soon{opacity:.88}
.soonTag{position:absolute;top:14px;right:14px;background:var(--tint2);border:1px solid var(--gold);color:var(--gold2);font-size:11px;font-weight:700;border-radius:8px;padding:3px 9px}
.priv{max-width:640px;margin:12px auto 0;text-align:left;font-size:12px}
.priv summary{cursor:pointer;color:var(--mut);text-align:center}
.priv p{margin-top:8px}
.cfg{display:flex;gap:12px;align-items:flex-start;padding:12px 0;border-bottom:1px solid var(--line);font-size:14px}
.cfg small{display:block;color:var(--mut);font-size:12px;margin-top:2px}
.steps{margin:0 0 12px 18px;font-size:13px;color:var(--mut)}
.steps li{margin-bottom:4px}
.stars{color:var(--gold2);letter-spacing:2px;margin-bottom:8px}
.ver{font-size:12px;color:var(--gold2)}
.fontes{margin:0 0 0 18px;font-size:13px;color:var(--mut)}
.fontes li{margin-bottom:8px}
.fontes a{color:var(--gold2)}
.about{background:linear-gradient(160deg,var(--tint),var(--card));border:1px solid var(--tint2);border-radius:20px;padding:34px 24px;text-align:center}
.about p{max-width:640px;margin:10px auto 18px;color:var(--mut)}
.nums{display:flex;gap:30px;justify-content:center;flex-wrap:wrap;margin:18px 0 22px}
.nums b{display:block;font-size:26px;color:var(--gold2)}
.nums small{color:var(--mut)}
.about .btn{margin:4px}
.ex{border-color:var(--tint2)}
.ex .btn{width:100%;margin-top:auto}
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

/* ===== LUXO ===== */
:root{--serif:"Playfair Display",Georgia,"Times New Roman",serif;--ouro:linear-gradient(135deg,#7d5f1a 0%,var(--gold) 32%,var(--gold2) 52%,var(--gold) 72%,#7d5f1a 100%)}
*{scrollbar-color:var(--tint2) var(--bg)}
::selection{background:var(--gold);color:#111}
body{background:radial-gradient(1100px 520px at 50% -160px,color-mix(in srgb,var(--gold) 10%,transparent),transparent 70%),var(--bg)}
h1,h2,h3,.logo,.price b,.stats b,.nums b{font-family:var(--serif)}
h2{font-size:clamp(28px,4vw,40px);font-weight:700}
h2::after{content:"";display:block;width:64px;height:2px;margin:14px 0 8px;background:var(--ouro);border-radius:2px}
.cta h2::after,.about h2::after{margin-left:auto;margin-right:auto}
nav{background:rgba(8,8,9,.72);backdrop-filter:blur(18px) saturate(1.4);border-bottom:1px solid color-mix(in srgb,var(--gold) 20%,transparent)}
.logo{font-size:21px;letter-spacing:.3em;font-weight:700}
.topbar{background:linear-gradient(90deg,transparent,color-mix(in srgb,var(--gold) 11%,transparent),transparent)}
.hero h1{font-weight:800}
.hero h1 em{background:var(--ouro);background-size:220% auto;-webkit-background-clip:text;background-clip:text;color:transparent;animation:brilho 7s linear infinite}
@keyframes brilho{to{background-position:220% center}}
.badge{letter-spacing:.22em;font-size:11px;background:color-mix(in srgb,var(--gold) 9%,transparent)}
.stats b{font-size:32px}
.btn.gold{background:var(--ouro);background-size:200% auto;font-weight:700;letter-spacing:.02em;box-shadow:0 8px 22px -8px color-mix(in srgb,var(--gold) 60%,transparent),inset 0 1px 0 rgba(255,255,255,.4);transition:background-position .4s,transform .2s,box-shadow .3s}
.btn.gold:hover{background-position:right center}
.card{background:linear-gradient(160deg,color-mix(in srgb,var(--gold) 5%,#17171b),#0f0f12);border:1px solid color-mix(in srgb,var(--gold) 16%,var(--line));box-shadow:0 1px 0 rgba(255,255,255,.04) inset,0 18px 40px -26px #000;transition:transform .35s cubic-bezier(.2,.7,.2,1),border-color .35s,box-shadow .35s;animation:subir .55s cubic-bezier(.2,.7,.2,1) both}
.card:nth-child(2){animation-delay:.05s}.card:nth-child(3){animation-delay:.1s}.card:nth-child(4){animation-delay:.15s}.card:nth-child(5){animation-delay:.2s}.card:nth-child(n+6){animation-delay:.25s}
@keyframes subir{from{opacity:0;transform:translateY(22px)}}
@media(hover:hover){.card:hover{transform:translateY(-6px);border-color:var(--gold);box-shadow:0 26px 54px -24px color-mix(in srgb,var(--gold) 50%,transparent),0 1px 0 rgba(255,255,255,.06) inset}}
.card.cb{background:linear-gradient(160deg,color-mix(in srgb,var(--gold) 15%,#17140a),#0e0d0a)}
.card.cb.top{box-shadow:0 0 0 1px var(--gold),0 28px 60px -26px color-mix(in srgb,var(--gold) 60%,transparent)}
.cb .off{top:0;right:0;border-radius:0 16px 0 14px;padding:8px 14px;background:var(--ouro)}
.ico{border:1px solid color-mix(in srgb,var(--gold) 45%,transparent);box-shadow:0 0 24px -6px color-mix(in srgb,var(--gold) 55%,transparent)}
.price b{font-size:26px}
.box{border:1px solid color-mix(in srgb,var(--gold) 30%,var(--line));box-shadow:0 30px 80px -20px #000,0 0 70px -34px var(--gold)}
.about{box-shadow:0 30px 70px -40px color-mix(in srgb,var(--gold) 50%,transparent)}
footer{border-top:1px solid color-mix(in srgb,var(--gold) 22%,var(--line));background:linear-gradient(180deg,transparent,rgba(0,0,0,.45))}
/* Revelar ao rolar (só se o JS carregou) */
.js .rv{opacity:0;transform:translateY(18px);transition:opacity .7s ease,transform .7s cubic-bezier(.2,.7,.2,1)}
.js .rv.in{opacity:1;transform:none}
/* Desempenho: só desenha seções quando se aproximam da tela */
section:not(.trust):not(#combos),footer{content-visibility:auto;contain-intrinsic-size:auto 720px}
.card,.chip,.btn{contain:layout style}
@media(max-width:760px){nav{backdrop-filter:none;background:rgba(8,8,9,.95)}.stats b{font-size:26px}}
@media(prefers-reduced-motion:reduce){*,*::before,*::after{animation-duration:.01ms!important;animation-iteration-count:1!important;transition-duration:.01ms!important;scroll-behavior:auto!important}.js .rv{opacity:1;transform:none}}

/* ===== BLACK EDITION ===== */
.blk{text-align:center;background:radial-gradient(800px 300px at 50% 0,color-mix(in srgb,var(--gold) 15%,transparent),transparent 70%),linear-gradient(180deg,#0c0b08,#060606);border:1px solid color-mix(in srgb,var(--gold) 38%,var(--line));border-radius:24px;padding:46px 22px;box-shadow:0 40px 90px -50px color-mix(in srgb,var(--gold) 65%,transparent)}
.blk .badge{margin-bottom:16px}
.blk h2::after{margin-left:auto;margin-right:auto}
.blk .sub{max-width:620px;margin:0 auto}
.plans{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,260px),1fr));gap:18px;margin-top:30px;text-align:left}
.plan{background:linear-gradient(160deg,#15120a,#090908);border:1px solid color-mix(in srgb,var(--gold) 26%,var(--line));border-radius:18px;padding:26px;display:flex;flex-direction:column}
.plan.top{border-color:var(--gold);box-shadow:0 0 0 1px var(--gold),0 30px 60px -30px color-mix(in srgb,var(--gold) 60%,transparent)}
.plan h3{font-size:24px}
.pico{font-size:26px;margin-bottom:8px}
.pp{color:var(--gold2);font-family:var(--serif);font-size:22px;margin:6px 0 14px}
.plan ul{list-style:none;margin:0 0 20px;padding:0;flex:1}
.plan li{font-size:14px;color:var(--mut);padding:9px 0 9px 22px;border-top:1px solid var(--line);position:relative}
.plan li::before{content:"✦";position:absolute;left:0;top:12px;color:var(--gold2);font-size:11px}
.plan .btn{width:100%}
.hero .micro{font-size:13px;color:var(--mut);margin:18px auto 0;max-width:none}
</style>
</head>
<body>

<div class="topbar"><div class="wrap">
  <span>📩 Contato:</span>
  <a id="ftTiktok" href="#" target="_blank" rel="noopener">TikTok @vinlumexz00</a>
  <a id="ftRoblox" href="#" target="_blank" rel="noopener">Roblox eyeywtwywywy</a>
</div></div>

<nav><div class="wrap">
  <a class="logo" href="#">LUMEX <span>FORGE</span></a>
  <ul id="menu"><li><a href="#black">Black Edition</a></li><li><a href="#combos">Combos</a></li><li><a href="#loja">Loja</a></li><li><a href="#eb">Exército RP</a></li><li><a href="#como">Como funciona</a></li><li><a href="#faq">Dúvidas</a></li><li><a href="#contato">Contato</a></li></ul>
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
  <h1>Sistemas prontos para o seu jogo no Roblox, <em>sem semanas de programação</em></h1>
  <p>Roleplay, Exército RP, pets, tiro, terror e mais. Scripts em Luau com guia de instalação e suporte, para você colocar no Roblox Studio e publicar.</p>
  <a class="btn gold" href="#loja">Ver os scripts</a>
  <a class="btn line" href="#combos">Pacotes com desconto</a>
  <p class="micro">Pix ou Robux · Guia de instalação · Suporte pelo TikTok e Roblox</p>
  <div class="stats">
    <div><b id="nProd">0</b><small>scripts</small></div>
    <div><b>Luau</b><small>código limpo</small></div>
    <div><b>Robux + R$</b><small>formas de pagar</small></div>
  </div>
  <div class="hero-contact">
    <p>Fale com a gente e tire suas dúvidas</p>
    <a class="btn gold" id="heroTiktok" href="#" target="_blank" rel="noopener">TikTok @vinlumexz00</a>
    <a class="btn line" id="heroRoblox" href="#" target="_blank" rel="noopener">Roblox eyeywtwywywy</a>
  </div>
</div></header>

<section id="black"><div class="wrap"><div class="blk" id="blkBox"></div></div></section>

<section class="trust"><div class="wrap"><div class="tr">
  <div><b>💳 Pix ou Robux</b><span>Pague do jeito que preferir</span></div>
  <div><b>📦 Guia de instalação</b><span>Cada script vem com passo a passo</span></div>
  <div><b>🧑‍💻 Suporte</b><span>Dúvidas de instalação pelo TikTok ou Roblox</span></div>
  <div><b>🔓 Código aberto</b><span>Você edita e personaliza no seu jogo</span></div>
</div></div></section>

<section id="combos"><div class="wrap">
  <div class="free" id="freeBox"><span>🎁 Ganhe grátis: <b id="freeNome"></b></span><button class="btn gold" id="freeBtn">Quero o meu</button></div>
  <h2>Pacotes com desconto</h2>
  <p class="sub">Leve o pacote completo e pague bem menos do que comprando script por script.</p>
  <div class="grid" id="comboGrid"></div>
</div></section>

<section id="loja"><div class="wrap">
  <h2>Loja de scripts</h2>
  <p class="sub">Sistemas no estilo dos jogos mais jogados do Roblox: pets, anime RPG, obby, tiro, terror, tycoon, roleplay e mais.</p>
  <div class="tools">
    <input id="busca" type="search" placeholder="Pesquisar script...">
    <select id="ordem" aria-label="Ordenar"><option value="">Ordenar</option><option value="menor">Menor preço</option><option value="maior">Maior preço</option><option value="az">A–Z</option></select>
    <div class="chips" id="chips"></div>
  </div>
  <div class="grid" id="grid"></div>
  <div class="more" id="maisWrap"></div>
</div></section>

<section id="eb"><div class="wrap">
  <h2>Pacote Exército Brasileiro RP</h2>
  <p class="sub">Hierarquia completa para jogos de rotina militar. Nomes, cargos e salários são editáveis.</p>
  <div class="ranks" id="ranks"></div>
  <button class="btn gold" id="verEB">Ver scripts do Exército RP</button>
</div></section>

<section id="sobre"><div class="wrap"><div class="about" id="sobreBox"></div></div></section>

<section id="garantia"><div class="wrap">
  <h2>Compra com certeza</h2>
  <p class="sub">Você sabe o que recebe, quando recebe e o que fazer se algo não funcionar.</p>
  <div class="grid" id="garGrid"></div>
</div></section>

<section id="exclusivo"><div class="wrap">
  <h2>Seja exclusivo</h2>
  <p class="sub">Para quem quer um jogo que ninguém mais tem.</p>
  <div class="grid" id="exGrid"></div>
</div></section>

<section id="depo" style="display:none"><div class="wrap">
  <h2>Quem já comprou</h2>
  <p class="sub" id="depoSub">Depoimentos de clientes.</p>
  <div class="grid" id="depoGrid"></div>
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
  <details><summary>Como funcionam o carrinho e o cupom?</summary><p>No carrinho, quanto mais scripts você levar, maior o desconto. O cupom é digitado na hora de pagar, e vale sempre o maior desconto (os dois não somam).</p></details>
  <details><summary>Posso pedir um script sob medida?</summary><p>Pode. Clique na sua etiqueta no canto da tela, escolha “Script sob medida” e descreva a ideia. O criador responde com valor e prazo.</p></details>
  <details><summary>O que significa “Em breve”?</summary><p>É um script que ainda está sendo finalizado. Clique em “Avise-me quando sair” e deixe seu contato para ser avisado.</p></details>
  <details><summary>Preciso saber programar?</summary><p>Para instalar, não: o guia mostra o passo a passo. Para personalizar além do básico, ajuda conhecer um pouco de Luau, ou você pode pedir a personalização.</p></details>
  <details><summary>Vai funcionar no meu jogo?</summary><p>Os scripts são feitos para o Roblox Studio. Se tiver dúvida sobre o tipo do seu jogo, clique na etiqueta no canto da tela e pergunte antes de comprar.</p></details>
  <details><summary>Quanto tempo leva para receber?</summary><p>Depois que o pagamento é confirmado, você recebe o script e o guia pelo contato que informou. O prazo está na seção “Compra com certeza”.</p></details>
  <details id="faqGar"><summary>Como funciona a garantia?</summary><p id="faqGarT"></p></details>
</div></section>

<section id="contato"><div class="wrap">
  <div class="cta">
    <h2>Precisa de um script sob medida?</h2>
    <p class="sub">Descreva a ideia do seu jogo e receba um orçamento.</p>
    <a class="btn gold" id="lnkTiktok" href="#" target="_blank" rel="noopener">Chamar no TikTok</a>
    <a class="btn line" id="lnkRoblox" href="#" target="_blank" rel="noopener">Perfil no Roblox</a>
  </div>
</div></section>

<footer><div class="wrap">© <span id="ano"></span> Lumex Forge<br> Roblox e Roblox Studio são marcas da Roblox Corporation. Este site não é afiliado à Roblox nem ao Exército Brasileiro, e nenhum brasão ou insígnia oficial é incluído.<details class="priv"><summary>Privacidade</summary><p>Este site guarda no seu navegador uma etiqueta aleatória (para identificar a sua visita), o seu carrinho e a cor escolhida. O contato que você informa em um pedido ou no assistente é usado apenas para atender esse pedido. Para receber os pedidos usamos serviços de terceiros (Google Firebase e Web3Forms).</p></details><a href="#painel" id="abrirPainel" class="admlink">🔐 Painel do criador</a></div></footer>

<button class="cartbtn" id="cartBtn">🛒 <span id="cartN">0</span></button>
<div class="cart" id="cart">
  <div class="cart-h"><b>🛒 Seu carrinho</b><button id="cartX" aria-label="Fechar">✕</button></div>
  <div class="cart-b" id="cartList"></div>
  <div class="cart-f" id="cartF"></div>
</div>

<button class="vtag" id="vtag" title="Clique para falar com o assistente"></button>

<div class="bot" id="bot">
  <div class="bot-h"><b>🤖 Assistente da Lumex Forge</b><button id="botX" aria-label="Fechar">✕</button></div>
  <div class="bot-b" id="botB"></div>
  <div class="bot-f" id="botF"></div>
</div>

<div class="adm" id="adm">
  <div class="adm-top">
    <b>🛡️ Painel do Criador</b>
    <span class="admmodo" id="admModo"></span><span class="admmodo" id="admOnline"></span>
    <span class="grow"></span>
    <button class="chip" id="admNotif">🔔 Ativar avisos</button>
    <button class="chip" id="admFechar">Fechar</button>
    <button class="chip" id="admSair">Sair</button>
  </div>
  <div class="adm-login" id="admLogin"><div class="box">
    <h3>Entrar no painel</h3>
    <p id="admAviso"></p>
    <input id="admEmail" type="email" placeholder="E-mail" autocomplete="username">
    <input id="admSenha" type="password" placeholder="Senha" autocomplete="current-password">
    <div class="err" id="admErro"></div>
    <button class="btn gold" id="admEntrar" style="width:100%">Entrar</button>
  </div></div>
  <div id="admMain" style="display:none">
    <div class="adm-tabs">
      <button class="chip on" data-tab="ped">Pedidos <b id="cNovos">0</b></button>
      <button class="chip" data-tab="vis">Visitantes</button>
      <button class="chip" data-tab="int">Interesses <b id="cInt">0</b></button>
      <button class="chip" data-tab="cfg">Configuração</button>
    </div>
    <div id="tabPed"><div class="kan" id="kan"></div></div>
    <div id="tabVis" style="display:none"><div id="onlineBox"></div><div id="visList"></div></div>
    <div id="tabInt" style="display:none"><div id="intList" class="intgrid"></div></div>
    <div id="tabCfg" style="display:none"><div id="cfgList"></div></div>
  </div>
</div>

<div class="modal" id="modal" role="dialog" aria-modal="true" aria-label="Finalizar compra"><div class="box">
  <h3 id="mNome"></h3>
  <div id="mStep1"><p>Escolha como deseja pagar:</p>
  <button class="opt" id="mRbx"><span>Comprar com Robux<small>Pagamento pelo Roblox</small></span><em id="mRbxP"></em></button>
  <button class="opt" id="mPix"><span>Pagar com Pix<small>Pagamento na hora, sem taxas extras</small></span><em id="mPixP"></em></button>
  <p class="note">Preço final: sem cadastro e sem taxas extras.</p>
  <p class="note" id="mGar"></p>
  <div class="cupom"><input id="mCupom" placeholder="Tem um cupom? Digite aqui" maxlength="30"><button class="chip" id="mCupomOk">Aplicar</button></div>
  <div class="note" id="mCupomMsg"></div>
  </div>
  <div id="mStep2" style="display:none">
    <p>Para onde enviamos o script? Informe seu contato:</p>
    <input id="mContato" type="text" maxlength="80" placeholder="@seutiktok, usuário do Roblox ou WhatsApp">
    <div class="err" id="mErro"></div>
    <p class="note">Seu contato é usado só para te enviar o pedido.</p>
    <button class="btn gold" id="mOk" style="width:100%">Confirmar pedido</button>
  </div>
  <div id="mStep3" style="display:none">
    <p>✅ Pedido enviado! Em instantes o criador vai te chamar pelo contato informado.</p>
    <p>Sua etiqueta neste pedido: <span id="mTagOk"></span></p>
    <div class="err" id="mAviso"></div>
    <p class="note" id="mNota"></p>
    <div id="mPixBox" style="display:none">
      <p class="note">💸 Pague <b id="mPixVal"></b> via Pix:</p>
      <ol class="steps"><li>Abra o app do seu banco e vá em <b>Pix</b></li><li>Escolha <b>Pagar com QR Code</b> ou <b>Pix Copia e Cola</b></li><li>Confira o recebedor<b id="mTitular"></b> e o valor antes de confirmar</li><li>Envie o comprovante pelo TikTok ou Roblox</li></ol>
      <div id="mQr"></div>
      <textarea id="mPixCod" readonly rows="3"></textarea>
      <button class="btn gold" id="mPixCopy" style="width:100%;margin-bottom:8px">Copiar Pix copia e cola</button>
      <p class="note">Chave Pix: <span id="mPixKey"></span></p>
    </div>
    <button class="btn line" id="mFim" style="width:100%">Fechar</button>
  </div>
  <button class="close" id="mClose">Cancelar</button>
</div></div>

<script>
/* ===== CONFIGURAÇÃO: edite aqui ===== */
const CONFIG = {
  tiktok: "https://www.tiktok.com/@vinlumexz00",
  roblox: "https://www.roblox.com/search/users?keyword=eyeywtwywywy",
  moeda: "R$",
  pix: "+5541997381026",      // SUA CHAVE PIX (de preferência uma chave aleatória). Gera QR Code e copia-e-cola
  pixNome: "LUMEX FORGE",    // nome do recebedor (sem acentos, até 25 letras)
  pixCidade: "PARANAGUA",    // sua cidade (sem acentos, até 15 letras)
  pinLocal: "1234",          // PIN do painel no MODO TESTE (troque!)
  adminEmail: "encomuevade@gmail.com",  // e-mail do criador: já vem preenchido no login do painel
  emailKey: "COLE-SUA-CHAVE-WEB3FORMS", // chave grátis do web3forms.com (envia pedidos e interesses para o seu Gmail)
  cupons: {                             // "CÓDIGO": % (para tudo) ou { produtos: %, pacotes: % }. Vale o MAIOR desconto, não soma
    "TIKTOK10": 10,
    "NOVALumexforge": { produtos: 20, pacotes: 30 },
    "Vinlumexz300": { produtos: 20, pacotes: 30 },
    "LANÇAMENTO": { produtos: 10, pacotes: 30 }
  },
  descontoVolume: [[5, 15], [3, 10], [2, 5]], // carrinho: [mínimo de scripts, % de desconto]
  precoFator: 1,                        // preço dos scripts AVULSOS: 1 = normal (0.8 = 20% mais baixo)
  precoFatorPacote: 0.7,                // preço dos PACOTES: 0.7 = 30% mais baixo (além do desconto de cada pacote). 1 = sem redução extra
  garantiaDias: 7,                      // dias de garantia (0 = esconde). 7 dias é o mínimo legal em compra online (art. 49 do CDC)
  garantiaTexto: "Se o script não funcionar como descrito, corrigimos sem custo ou devolvemos o valor pago no Pix.",
  entregaPrazo: "em até 24 horas após a confirmação do pagamento",   // vazio = esconde
  autoridade: {                         // bloco "Quem faz os scripts" (apague o texto para esconder)
    titulo: "Quem faz os scripts",
    texto: "A Lumex Forge cria scripts em Luau para Roblox Studio. Cada script é testado no Studio antes da entrega e vem com guia de instalação e suporte para colocar no seu jogo.",
    numeros: []                         // só com números REAIS. Ex: [["+15","jogos atendidos"],["3 anos","com Roblox Studio"]]
  },
  black: {                              // Black Edition: atendimento premium. ativo:false esconde. Preço "Sob consulta" ou ex: "A partir de R$ 997"
    ativo: true,
    titulo: "Black Edition",
    sub: "Para criadores que levam o jogo a sério: exclusividade, atendimento direto e o script feito do seu jeito.",
    planos: [
      { nome: "Signature", icone: "💎", preco: "Sob consulta", itens: ["Licença exclusiva de 1 script: não é vendido para mais ninguém", "Personalização para o visual do seu jogo", "Atendimento prioritário", "Guia de instalação e suporte estendido"] },
      { nome: "Studio", icone: "🏛️", preco: "Sob consulta", destaque: true, itens: ["Pacote completo de um gênero, em licença exclusiva", "Integração entre os sistemas", "Reunião de briefing sobre o seu projeto", "Suporte estendido por 30 dias"] },
      { nome: "Concierge", icone: "👑", preco: "Sob consulta", itens: ["Projeto sob medida, do zero", "Acompanhamento direto do criador", "Confidencialidade sobre o seu projeto", "Prioridade na fila de entrega"] }
    ]
  },
  destaques: ["Menu Principal ALPHA", "Sistema de Inventário", "Chat RP"],   // "Comece por aqui": aparecem primeiro na loja (troque pelos seus preferidos)
  prontos: [],                          // nomes dos scripts que você JÁ TEM PRONTOS. Vazio = tudo à venda. Preenchido = só estes; o resto vira "Em breve"
  scriptGratis: "",                     // nome de um script GRÁTIS para atrair clientes (vazio = não aparece)
  depoimentos: [],                      // só quando tiver REAIS (e com permissão): [{nome:"João", texto:"Funcionou!", nota:5, verificado:true}]
  pixTitular: "",                       // nome que aparece no app do banco ao pagar o Pix (ajuda o cliente a conferir)
  firebase: {                // cole aqui os dados do seu projeto Firebase (veja o guia)
    apiKey: "", authDomain: "", projectId: "", appId: ""
  }
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
/* Preços: CONFIG.precoFator reduz (ou aumenta) todos de uma vez; sempre termina em ,90 e nunca fica abaixo de R$ 9,90 */
(() => {
  const f = CONFIG.precoFator || 1; if (f === 1) return;
  PRODUTOS.forEach(p => { const v = Math.round(p.brl * f); p.brl = Math.max(9.9, Math.round((v - 0.1) * 10) / 10); p.rbx = Math.round(p.brl * 10); });
})();

const $ = s => document.querySelector(s);
const fmt = v => CONFIG.moeda + " " + v.toFixed(2).replace(".", ",");
const cats = ["Todos", ...new Set(PRODUTOS.map(p => p.cat))];
let catAtual = "Todos", atual = null;

function abrir(link){
  if(link && link.startsWith("http")) window.open(link, "_blank", "noopener");
  else alert("Link ainda não configurado. Edite os links no começo do script em index.html.");
}

/* Demonstrações em vídeo (opcional): "Nome do script": "link do vídeo no TikTok" */
const DEMOS = {
  // "Sistema de Inventário": "https://www.tiktok.com/@vinlumexz00/video/0000000000",
};
let mostrar = 24;
const pronto = p => !(CONFIG.prontos || []).length || CONFIG.prontos.includes(p.nome);
function render(){
  const q = $("#busca").value.trim().toLowerCase();
  const lista = PRODUTOS.filter(p =>
    (catAtual === "Todos" || p.cat === catAtual) &&
    (p.nome + p.desc + p.tags.join(" ")).toLowerCase().includes(q));
  const o = $("#ordem").value;
  if (o === "menor") lista.sort((a, b) => a.brl - b.brl);
  else if (o === "maior") lista.sort((a, b) => b.brl - a.brl);
  else if (o === "az") lista.sort((a, b) => a.nome.localeCompare(b.nome, "pt-BR"));
  const dest = CONFIG.destaques || [];
  if (!q && catAtual === "Todos" && !o && dest.length) lista.sort((a, b) => (dest.includes(b.nome) ? 1 : 0) - (dest.includes(a.nome) ? 1 : 0));
  const vis = lista.slice(0, mostrar);
  $("#grid").innerHTML = vis.length ? vis.map(p => {
    const i = PRODUTOS.indexOf(p), ok = pronto(p);
    return `
    <article class="card ${ok ? "" : "soon"}">
      ${ok ? (dest.includes(p.nome) ? '<span class="soonTag">★ Comece por aqui</span>' : "") : '<span class="soonTag">Em breve</span>'}
      <div class="ico">${p.ico}</div>
      <h3>${p.nome}</h3>
      <p>${p.desc}</p>
      <div class="tags">${p.tags.map(t => `<span>${t}</span>`).join("")}</div>
      ${(DEMOS[p.nome] || "").startsWith("http") ? `<a class="demo" href="${DEMOS[p.nome]}" target="_blank" rel="noopener">▶ Ver demonstração</a>` : ""}
      <div class="price"><b>${fmt(p.brl)}</b><i>ou ${p.rbx} R$ Robux</i></div>
      ${ok ? `<div class="cbtns"><button class="btn gold" data-i="${i}">Comprar</button><button class="btn line" data-add="${i}">＋ Carrinho</button></div>`
           : `<button class="btn line" style="width:100%" data-avise="${i}">🔔 Avise-me quando sair</button>`}
    </article>`;
  }).join("") : `<div class="empty">Nenhum script encontrado.</div>`;
  $("#maisWrap").innerHTML = lista.length > mostrar ? `<button class="btn line" id="maisBtn">Ver mais (${lista.length - mostrar})</button>` : "";
}

function chips(){
  $("#chips").innerHTML = cats.map(c => `<button class="chip ${c===catAtual?"on":""}" data-c="${c}">${c}</button>`).join("");
}

$("#chips").addEventListener("click", e => {
  const c = e.target.dataset.c; if(!c) return;
  catAtual = c; mostrar = 24; chips(); render();
});
let _bt; $("#busca").addEventListener("input", () => { clearTimeout(_bt); _bt = setTimeout(() => { mostrar = 24; render(); }, 120); });
$("#ordem").addEventListener("change", () => { mostrar = 24; render(); });
$("#maisWrap").addEventListener("click", e => { if (e.target.id === "maisBtn") { mostrar += 24; render(); } });

/* ---- Compra unificada: produto, pacote ou carrinho, com cupom (vale o MAIOR desconto) ---- */
let baseCompra = null, CUPOM = null;
const precoDe = (b, off) => ({ brl: Math.round(b.somaBrl * (1 - off / 100) * 10) / 10, rbx: Math.round(b.somaRbx * (1 - off / 100)) });
const normCupom = t => String(t).normalize("NFD").replace(/[\u0300-\u036f]/g, "").replace(/\s+/g, "").toUpperCase();
function acharCupom(txt) {
  const k = normCupom(txt); if (!k) return null;
  for (const [cod, v] of Object.entries(CONFIG.cupons || {})) {
    if (normCupom(cod) === k) return { codigo: cod, produtos: typeof v === "number" ? v : (v.produtos || 0), pacotes: typeof v === "number" ? v : (v.pacotes || 0) };
  }
  return null;
}
function aplicarPrecos() {
  const b = baseCompra, base = b.offBase || 0;
  const cOff = CUPOM ? (b.tipo === "pacote" ? CUPOM.pacotes : CUPOM.produtos) : 0;
  const off = Math.max(base, cOff), usouCupom = cOff > base, pr = precoDe(b, off);
  atual = { nome: b.nome + (usouCupom ? " [cupom " + CUPOM.codigo + " -" + cOff + "%]" : ""), cat: b.cat, brl: pr.brl, rbx: pr.rbx, linkRobux: b.linkRobux, linkPay: b.linkPay };
  $("#mNome").textContent = b.nome;
  $("#mRbxP").textContent = pr.rbx + " Robux";
  $("#mPixP").textContent = fmt(pr.brl);
  $("#mCupomMsg").textContent = !CUPOM ? "" : usouCupom ? "✅ Cupom aplicado: -" + cOff + "% neste item" : "O desconto deste item já é maior que o do cupom.";
}
function abrirCompra(b) {
  baseCompra = b; CUPOM = null; $("#mCupom").value = "";
  aplicarPrecos(); mostrarPasso(1); $("#modal").classList.add("open");
}
$("#mCupomOk").onclick = () => {
  const txt = $("#mCupom").value;
  CUPOM = acharCupom(txt);
  aplicarPrecos();
  if (!CUPOM) $("#mCupomMsg").textContent = txt.trim() ? "Cupom inválido." : "Digite o código do cupom.";
};

/* ---- Carrinho com desconto por quantidade ---- */
let CARRINHO = [];
try { CARRINHO = JSON.parse(localStorage.getItem("carrinho") || "[]").filter(n => PRODUTOS.some(p => p.nome === n && pronto(p))); } catch (e) {}
const salvarCarrinho = () => { try { localStorage.setItem("carrinho", JSON.stringify(CARRINHO)); } catch (e) {} };
const offVolume = n => { for (const [m, d] of CONFIG.descontoVolume) if (n >= m) return d; return 0; };
const abrirCarrinho = () => $("#cart").classList.add("open");
const fecharCarrinho = () => $("#cart").classList.remove("open");
function itensCarrinho() { return CARRINHO.map((n, k) => ({ p: PRODUTOS.find(x => x.nome === n), k })).filter(x => x.p); }
function renderCarrinho() {
  const it = itensCarrinho(), n = it.length, soma = it.reduce((a, x) => a + x.p.brl, 0), off = offVolume(n);
  const tot = Math.round(soma * (1 - off / 100) * 10) / 10;
  const prox = CONFIG.descontoVolume.slice().reverse().find(([m]) => m > n);
  $("#cartN").textContent = n; $("#cartBtn").style.display = n ? "flex" : "none";
  $("#cartList").innerHTML = n ? it.map(x => `<div class="ci"><span>${x.p.ico} ${x.p.nome}</span><b>${fmt(x.p.brl)}</b><button data-rm="${x.k}" aria-label="Remover">✕</button></div>`).join("")
    : '<p class="note">Seu carrinho está vazio. Clique em “＋ Carrinho” nos scripts que quiser.</p>';
  $("#cartF").innerHTML = n ? `${prox ? `<div class="nudge">🔥 Adicione mais ${prox[0] - n} script(s) e ganhe ${prox[1]}% de desconto!</div>` : ""}
    <div class="crow"><span>Subtotal</span><span>${fmt(soma)}</span></div>
    ${off ? `<div class="crow eco"><span>Desconto por ${n} scripts</span><span>-${off}%</span></div>` : ""}
    <div class="crow tot"><span>Total</span><b>${fmt(tot)}</b></div>
    <button class="btn gold" id="cartGo" style="width:100%">Finalizar compra</button>` : "";
}
function addCarrinho(i) {
  const nome = PRODUTOS[i].nome;
  if (!CARRINHO.includes(nome)) { CARRINHO.push(nome); salvarCarrinho(); renderCarrinho(); }
  abrirCarrinho();
}
$("#cartBtn").onclick = abrirCarrinho;
$("#cartX").onclick = fecharCarrinho;
$("#cartList").addEventListener("click", e => {
  const k = e.target.dataset.rm; if (k === undefined) return;
  CARRINHO.splice(+k, 1); salvarCarrinho(); renderCarrinho();
});
$("#cartF").addEventListener("click", e => {
  if (e.target.id !== "cartGo") return;
  const it = itensCarrinho(); if (!it.length) return;
  fecharCarrinho();
  abrirCompra({
    nome: ("Carrinho (" + it.length + " scripts): " + it.map(x => x.p.nome).join("; ")).slice(0, 280), cat: "Carrinho",
    somaBrl: it.reduce((a, x) => a + x.p.brl, 0), somaRbx: it.reduce((a, x) => a + x.p.rbx, 0),
    offBase: offVolume(it.length), linkRobux: "#", linkPay: "#"
  });
});
renderCarrinho();

$("#grid").addEventListener("click", e => {
  const i = e.target.dataset.i, a = e.target.dataset.add;
  if (a !== undefined) return addCarrinho(+a);
  const av = e.target.dataset.avise;
  if (av !== undefined) return avisarMe(PRODUTOS[av].nome);
  if (i === undefined) return;
  const p = PRODUTOS[i];
  abrirCompra({ nome: p.nome, cat: p.cat, somaBrl: p.brl, somaRbx: p.rbx, offBase: 0, linkRobux: p.linkRobux, linkPay: p.linkPay });
});
$("#mClose").onclick = () => $("#modal").classList.remove("open");
$("#modal").addEventListener("click", e => { if(e.target.id === "modal") $("#modal").classList.remove("open"); });

/* Pacotes com desconto: o preço é calculado somando os scripts do grupo e aplicando o desconto (off) */
const COMBOS = [
  {titulo:"Pacote Exército RP Completo", grupo:"Militar EB", ico:"🎖️", off:25, top:true, desc:"Patentes, comando, fichas, cursos, rádio, arsenal e mais."},
  {titulo:"Pacote Cidade Roleplay", grupo:"Roleplay", ico:"🏙️", off:25, top:true, desc:"Documentos, celular, banco, empregos, casas, polícia e hospital."},
  {titulo:"Pacote Simulador de Pets", grupo:"Pets & Simulador", ico:"🐾", off:25, desc:"Ovos, trocas, rebirth, mundos, batalhas e conquistas."},
  {titulo:"Pacote Anime RPG", grupo:"Anime RPG", ico:"⚔️", off:25, desc:"Poderes, níveis, missões, chefes, combate e classes."},
  {titulo:"Pacote Arena PvP", grupo:"PvP & Tiro", ico:"🎯", off:25, desc:"Armas, partidas, loadouts, battle royale e polícia e ladrão."},
  {titulo:"Pacote Terror e Sobrevivência", grupo:"Terror & Sobrevivência", ico:"👹", off:20, desc:"Portas, monstro com IA, cutscenes, craft e fogueira."},
  {titulo:"Pacote Veículos", grupo:"Veículos", ico:"🚗", off:20, desc:"Carros, garagem, combustível, concessionária, barcos e aeronaves."},
  {titulo:"Pacote Minigames", grupo:"Minigames", ico:"🎲", off:20, desc:"Assassino e xerife, pique-esconde, votação, lobby e espectador."}
];
COMBOS.forEach(c => {
  const it = PRODUTOS.filter(p => p.cat === c.grupo);
  c.n = it.length;
  c.ok = it.length > 0 && it.every(pronto);
  const fp = CONFIG.precoFatorPacote || 1;
  c.soma = it.reduce((a, p) => a + p.brl, 0);          // valor normal comprando os scripts separados (preço "de")
  c.somaR = it.reduce((a, p) => a + p.rbx, 0);
  c.somaCalc = c.soma * fp; c.somaRCalc = c.somaR * fp;  // base do preço do pacote
  c.brl = Math.round(c.somaCalc * (1 - c.off / 100) * 10) / 10;
  c.rbx = Math.round(c.somaRCalc * (1 - c.off / 100));
  c.eco = c.soma - c.brl;
  c.offReal = c.soma ? Math.round((1 - c.brl / c.soma) * 100) : 0;   // desconto real em relação a comprar separado
  c.nome = c.titulo + " (" + c.n + " scripts)";
  c.cat = "Combo"; c.linkRobux = "#"; c.linkPay = "#";   // cole aqui os links de pagamento do pacote
});
$("#comboGrid").innerHTML = COMBOS.map((c, i) => `
  <article class="card cb ${c.top ? "top" : ""}">
    <span class="off">-${c.offReal}%</span>
    <div class="ico">${c.ico}</div>
    <h3>${c.titulo}</h3>
    <p>${c.desc} Inclui ${c.n} scripts.</p>
    <div class="price"><div><span class="de">${fmt(c.soma)}</span><br><b>${fmt(c.brl)}</b></div><i>ou ${c.rbx} R$ Robux</i></div>
    <div class="eco">Você economiza ${fmt(c.eco)}</div>
    ${c.ok ? `<button class="btn gold" data-k="${i}">Quero o pacote</button>` : `<button class="btn line" data-av="${i}">🔔 Avise-me quando sair</button>`}
  </article>`).join("");
$("#comboGrid").addEventListener("click", e => {
  const av = e.target.dataset.av;
  if (av !== undefined) return avisarMe(COMBOS[av].nome);
  const k = e.target.dataset.k; if (k === undefined) return;
  const c = COMBOS[k];
  abrirCompra({ nome: c.nome, cat: c.cat, somaBrl: c.somaCalc, somaRbx: c.somaRCalc, offBase: c.off, tipo: "pacote", linkRobux: c.linkRobux, linkPay: c.linkPay });
});

/* Garantia, entrega, suporte, exclusividade e autoridade (os textos ficam em CONFIG) */
(() => {
  const g = [];
  if (CONFIG.garantiaDias) g.push(["🛡️", "Garantia de " + CONFIG.garantiaDias + " dias", CONFIG.garantiaTexto]);
  if (CONFIG.entregaPrazo) g.push(["📦", "Entrega " + CONFIG.entregaPrazo, "Você recebe o script e o guia de instalação pelo contato que informou."]);
  g.push(["🧑‍💻", "Suporte de instalação", "Travou ao colocar o script no seu jogo? Chame no TikTok ou no Roblox."]);
  g.push(["🔒", "Pagamento conferido", "No Pix, o app do seu banco mostra o recebedor e o valor antes de você confirmar."]);
  $("#garGrid").innerHTML = g.map(([i, t, d]) => `<div class="card"><div class="ico">${i}</div><h3>${t}</h3><p>${d}</p></div>`).join("");
  $("#mGar").textContent = CONFIG.garantiaDias ? "🛡️ Garantia de " + CONFIG.garantiaDias + " dias nesta compra." : "";
  if (CONFIG.garantiaDias) $("#faqGarT").textContent = CONFIG.garantiaTexto; else $("#faqGar").style.display = "none";

  const EX = [
    ["💎", "Licença exclusiva", "Um script só para o seu jogo: não é vendido para mais ninguém. Preço sob consulta."],
    ["🛠️", "Personalização", "Ajustamos o script ao visual e às regras do seu jogo."],
    ["⚡", "Acesso antecipado", "Receba os novos scripts antes de eles chegarem à loja."]
  ];
  $("#exGrid").innerHTML = EX.map(([i, t, d], k) => `<div class="card ex"><div class="ico">${i}</div><h3>${t}</h3><p>${d}</p><button class="btn gold" data-ex="${k}">Quero saber mais</button></div>`).join("");
  $("#exGrid").addEventListener("click", e => { const k = e.target.dataset.ex; if (k !== undefined) pedirExtra(EX[k][1], EX[k][2]); });

  const A = CONFIG.autoridade;
  if (A && A.texto) {
    $("#sobreBox").innerHTML = `<h2>${A.titulo || "Sobre o criador"}</h2><p>${A.texto}</p>` +
      (A.numeros && A.numeros.length ? `<div class="nums">${A.numeros.map(([n, l]) => `<div><b>${n}</b><small>${l}</small></div>`).join("")}</div>` : "") +
      `<a class="btn gold" href="${CONFIG.tiktok}" target="_blank" rel="noopener">Ver meu trabalho no TikTok</a><a class="btn line" href="${CONFIG.roblox}" target="_blank" rel="noopener">Perfil no Roblox</a>`;
  } else $("#sobre").style.display = "none";
})();

/* Black Edition */
(() => {
  const B = CONFIG.black;
  if (!B || !B.ativo || !(B.planos || []).length) { $("#black").style.display = "none"; return; }
  $("#blkBox").innerHTML = `<span class="badge">${String(B.titulo).toUpperCase()}</span><h2>Exclusividade para poucos</h2><p class="sub">${B.sub}</p>
    <div class="plans">${B.planos.map((p, i) => `<div class="plan ${p.destaque ? "top" : ""}"><div class="pico">${p.icone}</div><h3>${p.nome}</h3><div class="pp">${p.preco}</div>
      <ul>${p.itens.map(x => `<li>${x}</li>`).join("")}</ul><button class="btn ${p.destaque ? "gold" : "line"}" data-bk="${i}">Solicitar proposta privada</button></div>`).join("")}</div>`;
  $("#blkBox").addEventListener("click", e => { const k = e.target.dataset.bk; if (k !== undefined) pedirExtra("Black Edition: " + B.planos[k].nome, "Proposta privada para o plano " + B.planos[k].nome); });
})();

/* Script grátis (aparece só se CONFIG.scriptGratis estiver preenchido) */
if (CONFIG.scriptGratis) { $("#freeNome").textContent = CONFIG.scriptGratis; $("#freeBox").style.display = "flex"; }
/* Depoimentos (aparecem só se CONFIG.depoimentos tiver itens) */
if (CONFIG.depoimentos && CONFIG.depoimentos.length) {
  const t2 = x => String(x).replace(/[&<>"]/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" }[c]));
  const notas = CONFIG.depoimentos.map(d => +d.nota).filter(n => n >= 1 && n <= 5);
  const estrelas = n => (n >= 1 && n <= 5) ? `<div class="stars">${"★".repeat(n)}${"☆".repeat(5 - n)}</div>` : "";
  $("#depoGrid").innerHTML = CONFIG.depoimentos.map(d => `<div class="card">${estrelas(+d.nota)}<p>“${t2(d.texto)}”</p><b>— ${t2(d.nome)}</b>${d.verificado ? ' <span class="ver">✔ Compra verificada</span>' : ""}</div>`).join("");
  if (notas.length >= 5) $("#depoSub").textContent = "Nota média " + (notas.reduce((a, n) => a + n, 0) / notas.length).toFixed(1).replace(".", ",") + " de 5, em " + notas.length + " avaliações de clientes.";
  $("#depo").style.display = "block";
}

$("#nProd").textContent = PRODUTOS.length;
$("#lnkTiktok").href = CONFIG.tiktok;
$("#ftTiktok").href = CONFIG.tiktok;
$("#lnkRoblox").href = CONFIG.roblox;
$("#ftRoblox").href = CONFIG.roblox;
$("#heroTiktok").href = CONFIG.tiktok;
$("#heroRoblox").href = CONFIG.roblox;
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
$("#verEB").onclick=()=>{catAtual="Militar EB";mostrar=24;chips();render();location.hash="#loja";};

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
  let t=0, c1="#fff", c2="#fff", nq=0;
  function draw(){
    const dpr=window.devicePixelRatio||1, w=cv.clientWidth||190;
    if(cv.width!==Math.round(w*dpr)){cv.width=cv.height=Math.round(w*dpr);}
    ctx.setTransform(dpr,0,0,dpr,0,0); ctx.clearRect(0,0,w,w);
    if(nq++%30===0){const cs=getComputedStyle(document.documentElement);c1=cs.getPropertyValue("--gold2").trim();c2=cs.getPropertyValue("--gold").trim();}
    const cy=Math.cos(t), sy=Math.sin(t), cx=Math.cos(.45), sx=Math.sin(.45);
    const Q=V.map(([x,y,z])=>{
      const X=x*cy+z*sy; let Z=-x*sy+z*cy;
      const Y=y*cx-Z*sx; Z=y*sx+Z*cx;
      const f=3.6/(3.6+Z);
      return [w/2+X*f*w*.31, w/2-Y*f*w*.31, Z];
    });
    ctx.lineWidth=1.7; ctx.lineCap="round"; ctx.shadowColor=c2; ctx.shadowBlur=6;
    for(const [a,b] of E){
      const A=Q[a], B=Q[b], z=(A[2]+B[2])/2;
      ctx.globalAlpha=Math.max(.2,Math.min(1,.65-z*.4));
      ctx.strokeStyle=z>0?c2:c1;
      ctx.beginPath(); ctx.moveTo(A[0],A[1]); ctx.lineTo(B[0],B[1]); ctx.stroke();
    }
    ctx.globalAlpha=1;
  }
  if(window.matchMedia("(prefers-reduced-motion: reduce)").matches){ draw(); }
  else{
    let visivel = true;
    if ("IntersectionObserver" in window) new IntersectionObserver(es => { visivel = es[0].isIntersecting; }).observe(cv);
    (function loop(){ if (visivel && !document.hidden) { t+=.016; draw(); } requestAnimationFrame(loop); })();
  }
})();

/* Menu do celular */
$("#burger").onclick = () => $("#menu").classList.toggle("open");
$("#menu").addEventListener("click", e => { if(e.target.tagName === "A") $("#menu").classList.remove("open"); });
chips(); render();
</script>
<script>
/* ===== Pedidos, etiqueta de visitante e painel do criador ===== */
const TIT = document.title;
const lsGet = (k, d) => { try { const v = JSON.parse(localStorage.getItem(k)); return v === null ? d : v; } catch (e) { return d; } };
const lsSet = (k, v) => { try { localStorage.setItem(k, JSON.stringify(v)); } catch (e) {} };
const esc = t => String(t == null ? "" : t).replace(/[&<>"']/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;", "'": "&#39;" }[c]));

/* Mensagens prontas (edite o texto à vontade). Campos: {contato} {produto} {valor} {tag} {link} {pix} {loja} */
const MSG = {
  Robux: "Olá {contato}! 👋 Aqui é da {loja}.\nRecebi o seu pedido ({tag}): *{produto}* por {valor}.\n\nPara pagar com Robux, compre este Game Pass:\n{link}\n\nAssim que o pagamento cair, eu te envio o script e o guia de instalação. Qualquer dúvida é só me chamar! 🚀",
  Dinheiro: "Olá {contato}! 👋 Aqui é da {loja}.\nRecebi o seu pedido ({tag}): *{produto}* por {valor}.\n\nPara pagar, use o Pix:\n{pix}{linkpay}\n\nDepois me mande o comprovante por aqui que eu te envio o script e o guia de instalação. Qualquer dúvida é só me chamar! 🚀"
};
function montarMsg(o) {
  const campos = {
    contato: o.contato, produto: o.produto, valor: o.valor, tag: o.tag,
    link: o.link || "(vou te enviar o link)", pix: CONFIG.pix, loja: "Lumex Forge",
    linkpay: o.link ? "\nOu pague pelo link: " + o.link : ""
  };
  return (MSG[o.pagamento] || MSG.Dinheiro).replace(/\{(\w+)\}/g, (_, k) => campos[k] == null ? "" : campos[k]);
}

/* ---------- Etiqueta do visitante ---------- */
/* A etiqueta é sorteada pelo sistema (ninguém escolhe). 30 bichos x 30 estilos x 900 números = 810.000 combinações */
const ETQ_BICHO = [["🦊","Raposa"],["🐺","Lobo"],["🦅","Águia"],["🐉","Dragão"],["🦁","Leão"],["🐯","Tigre"],["🦈","Tubarão"],["🐼","Panda"],["🦉","Coruja"],["🐙","Polvo"],["🦄","Unicórnio"],["🐧","Pinguim"],["🦋","Borboleta"],["🐢","Tartaruga"],["🦖","Dinossauro"],["🐸","Sapo"],["🐬","Golfinho"],["🦂","Escorpião"],["🐻","Urso"],["🦜","Papagaio"],["🦇","Morcego"],["🐍","Serpente"],["🦦","Lontra"],["🦔","Ouriço"],["🐘","Elefante"],["🦒","Girafa"],["🦩","Flamingo"],["🐊","Jacaré"],["🦥","Preguiça"],["🐝","Abelha"]];
const ETQ_ESTILO = ["Neon","Turbo","Astral","Pixel","Laser","Veloz","Feroz","Audaz","Ágil","Radiante","Brilhante","Cometa","Trovão","Fantasma","Ninja","Vulcão","Rubi","Safira","Eclipse","Aurora","Foguete","Relâmpago","Diamante","Magma","Cristal","Samurai","Hacker","Mestre","Turbina","Pirata"];
const sorteio = n => { try { const a = new Uint32Array(1); crypto.getRandomValues(a); return a[0] % n; } catch (e) { return Math.floor(Math.random() * n); } };
function sortearEtiqueta() {
  const [e, b] = ETQ_BICHO[sorteio(ETQ_BICHO.length)];
  return e + " " + b + " " + ETQ_ESTILO[sorteio(ETQ_ESTILO.length)] + " #" + (100 + sorteio(900));
}
let VTAG = lsGet("vtag", null);
if (VTAG && /^V-/.test(VTAG)) VTAG = null;   // formato antigo: será sorteada de novo
const matiz = t => { let h = 0; for (const c of String(t)) h = (h * 31 + c.charCodeAt(0)) % 360; return h; };
const pill = t => `<span class="vpill" style="--h:${matiz(t)}">${esc(t)}</span>`;
function desenharTag() {
  $("#vtag").innerHTML = (VTAG ? pill(VTAG) : '<span class="vpill" style="--h:200">🎲 sorteando…</span>') + '<span>💬</span><small class="vt-s">fale com a gente</small>';
}
desenharTag();

/* ---------- Banco de dados: Firebase (online) ou local (teste) ---------- */
const FB = CONFIG.firebase || {};
const DB = { mode: "local", refresh: {} };
const carregar = src => new Promise((ok, er) => { const s = document.createElement("script"); s.src = src; s.onload = ok; s.onerror = er; document.head.appendChild(s); });
DB.pronto = (async () => {
  if (!FB.apiKey) return;
  try {
    const b = "https://www.gstatic.com/firebasejs/10.12.2/firebase-";
    await carregar(b + "app-compat.js"); await carregar(b + "auth-compat.js"); await carregar(b + "firestore-compat.js");
    firebase.initializeApp(FB);
    DB.mode = "firebase"; DB.auth = firebase.auth(); DB.fs = firebase.firestore();
  } catch (e) { console.warn("Firebase não carregou; usando modo local.", e); }
})();
DB.add = async (col, o) => {
  await DB.pronto;
  o.t = Date.now();
  if (DB.mode === "firebase") { await DB.fs.collection(col).add(o); return; }
  const a = lsGet(col, []); o.id = o.t + Math.random().toString(36).slice(2, 5); a.push(o); lsSet(col, a);
  if (DB.refresh[col]) DB.refresh[col]();
};
DB.up = async (col, id, patch) => {
  await DB.pronto;
  if (DB.mode === "firebase") { await DB.fs.collection(col).doc(id).update(patch); return; }
  lsSet(col, lsGet(col, []).map(x => x.id === id ? { ...x, ...patch } : x));
  if (DB.refresh[col]) DB.refresh[col]();
};
DB.on = async (col, cb) => {
  await DB.pronto;
  if (DB.mode === "firebase") {
    return DB.fs.collection(col).orderBy("t", "desc").limit(300).onSnapshot(
      q => cb(q.docs.map(d => ({ id: d.id, ...d.data() }))),
      er => toast("⚠️ Sem acesso a " + col + " (" + er.code + "). Confira as regras do Firestore e o e-mail do criador.")
    );
  }
  const ler = () => cb(lsGet(col, []).slice().sort((a, b) => b.t - a.t));
  DB.refresh[col] = ler;
  window.addEventListener("storage", e => { if (e.key === col) ler(); });
  ler();
  return () => {};
};

/* Envio para o seu Gmail (via Web3Forms, plano grátis: 250 envios por mês) */
async function enviarEmail(assunto, campos) {
  const k = CONFIG.emailKey;
  if (!k || /COLE/i.test(k)) return false;
  try {
    const r = await fetch("https://api.web3forms.com/submit", {
      method: "POST", headers: { "Content-Type": "application/json", Accept: "application/json" },
      body: JSON.stringify({ access_key: k, subject: assunto, from_name: "Lumex Forge (site)", botcheck: "", ...campos })
    });
    const j = await r.json(); return !!j.success;
  } catch (e) { return false; }
}

/* Etiqueta ÚNICA: no modo online cada etiqueta é reservada no banco; se já existir, sorteia outra */
const slug = t => String(t).normalize("NFD").replace(/[\u0300-\u036f]/g, "").toLowerCase().replace(/[^a-z0-9]+/g, "-").replace(/^-+|-+$/g, "");
const DISP = /Mobi|Android/i.test(navigator.userAgent) ? "📱 Celular" : "💻 Computador";
async function garantirEtiqueta() {
  await DB.pronto;
  if (VTAG && (DB.mode !== "firebase" || lsGet("vtagOk", false))) return;
  if (DB.mode !== "firebase") { VTAG = sortearEtiqueta(); lsSet("vtag", VTAG); return; }
  for (let i = 0; i < 25; i++) {
    const t = sortearEtiqueta();
    try {
      await DB.fs.collection("etiquetas").doc(slug(t)).set({ tag: t, t: Date.now() });   // falha se já existir
      VTAG = t; lsSet("vtag", t); lsSet("vtagOk", true); return;
    } catch (e) { /* já em uso: tenta outra */ }
  }
  VTAG = sortearEtiqueta() + "-" + (1000 + sorteio(9000));   // plano B (só se o banco estiver sem acesso)
  lsSet("vtag", VTAG); lsSet("vtagOk", true);
}
/* Presença: a cada 45 s marca "estou online" (o painel mostra quem está ativo) */
function batimento(fim) {
  if (DB.mode !== "firebase" || !VTAG || (document.hidden && !fim)) return;
  DB.fs.collection("online").doc(slug(VTAG)).set({ tag: VTAG, t: fim ? 0 : Date.now(), disp: DISP }).catch(() => {});
}
const prontaTag = (async () => {
  try { await garantirEtiqueta(); } catch (e) { console.warn("Etiqueta", e); }
  desenharTag();
  let j = false;
  try { j = sessionStorage.getItem("vis"); sessionStorage.setItem("vis", "1"); } catch (e) {}
  if (!j) DB.add("visitas", { tag: VTAG, disp: DISP }).catch(() => {});
  batimento(); setInterval(batimento, 45000);
})();
document.addEventListener("visibilitychange", () => { if (!document.hidden) batimento(); });
addEventListener("pagehide", () => batimento(true));

/* ---------- Pedido do cliente (janela de compra em 3 passos) ---------- */
let formaSel = "";
function mostrarPasso(n) {
  ["1", "2", "3"].forEach(i => { $("#mStep" + i).style.display = i == n ? "block" : "none"; });
  if (n == 2) setTimeout(() => $("#mContato").focus(), 50);
}
function criarPedido(forma, contato) {
  const prod = atual, link = forma === "Robux" ? prod.linkRobux : prod.linkPay, ok = (link || "").startsWith("http");
  const envio = prontaTag.then(async () => {
    const ped = {
      tag: VTAG, produto: prod.nome, cat: prod.cat, pagamento: forma,
      valor: forma === "Robux" ? prod.rbx + " Robux" : fmt(prod.brl),
      contato: contato.slice(0, 80), link: ok ? link : "", status: "novo"
    };
    const mail = enviarEmail("🛒 Novo pedido: " + prod.nome, { etiqueta: VTAG, produto: prod.nome, pagamento: forma, valor: ped.valor, contato: ped.contato, aparelho: DISP, mensagem_pronta: montarMsg(ped) });
    const salvo = DB.add("pedidos", ped).then(() => DB.mode === "firebase").catch(e => { console.warn("Pedido não enviado", e); return false; });
    const [m, sv] = await Promise.all([mail, salvo]);
    return m || sv;
  });
  if (ok) window.open(link, "_blank", "noopener");
  return envio;
}
$("#mRbx").onclick = () => { formaSel = "Robux"; $("#mOk").textContent = "Continuar para o pagamento"; mostrarPasso(2); };
$("#mPix").onclick = () => { formaSel = "Dinheiro"; $("#mOk").textContent = "Gerar meu Pix"; mostrarPasso(2); };
$("#mOk").onclick = () => {
  const c = $("#mContato").value.trim();
  if (c.length < 3) { $("#mErro").textContent = "Informe seu TikTok, Roblox ou WhatsApp para eu te chamar."; $("#mContato").focus(); return; }
  $("#mErro").textContent = "";
  const envio = criarPedido(formaSel, c);
  $("#mAviso").textContent = "";
  if (atual.cat === "Carrinho") { CARRINHO = []; salvarCarrinho(); renderCarrinho(); }
  $("#mNota").textContent = formaSel === "Robux" && !(atual.linkRobux || "").startsWith("http") ? "Você vai receber o link de pagamento em Robux pelo contato que informou."
    : formaSel === "Dinheiro" && !pixOk() ? "Você vai receber os dados do Pix pelo contato que informou." : "";
  envio.then(ok => { if (!ok) $("#mAviso").textContent = "⚠️ Não consegui registrar o pedido automaticamente. Chame o criador no TikTok @" + CONFIG.tiktok.split("@").pop() + " com seu contato."; });
  $("#mTagOk").innerHTML = pill(VTAG);
  mostrarPix();
  $("#mContato").value = "";
  mostrarPasso(3);
};
$("#mFim").onclick = () => $("#modal").classList.remove("open");

/* ---------- Pix: QR Code e copia-e-cola ---------- */
function pixPayload(chave, valor, nome, cidade, txid) {
  const f = (id, v) => id + String(v.length).padStart(2, "0") + v;
  const limpa = t => String(t).normalize("NFD").replace(/[\u0300-\u036f]/g, "").replace(/[^A-Za-z0-9 ]/g, "").toUpperCase();
  const conta = f("00", "br.gov.bcb.pix") + f("01", chave);
  const tx = String(txid || "***").replace(/[^A-Za-z0-9*]/g, "").slice(0, 25) || "***";
  const p = f("00", "01") + f("01", "11") + f("26", conta) + f("52", "0000") + f("53", "986") +
    (valor > 0 ? f("54", Number(valor).toFixed(2)) : "") + f("58", "BR") +
    f("59", limpa(nome).slice(0, 25) || "LOJA") + f("60", limpa(cidade).slice(0, 15) || "BRASIL") +
    f("62", f("05", tx)) + "6304";
  let crc = 0xFFFF;
  for (let i = 0; i < p.length; i++) {
    crc ^= p.charCodeAt(i) << 8;
    for (let j = 0; j < 8; j++) crc = (crc & 0x8000) ? ((crc << 1) ^ 0x1021) : (crc << 1);
    crc &= 0xFFFF;
  }
  return p + crc.toString(16).toUpperCase().padStart(4, "0");
}
const pixOk = () => CONFIG.pix && !/SUA-CHAVE/i.test(CONFIG.pix);
async function mostrarPix() {
  $("#mPixBox").style.display = "none"; $("#mQr").innerHTML = "";
  if (formaSel !== "Dinheiro" || !pixOk()) return;
  const cod = pixPayload(CONFIG.pix.trim(), atual.brl, CONFIG.pixNome || "LUMEX FORGE", CONFIG.pixCidade || "SUA CIDADE", "***");
  if (/SUA CIDADE/i.test(CONFIG.pixCidade || "SUA CIDADE")) console.warn("Pix: troque CONFIG.pixCidade pela sua cidade real.");
  $("#mPixVal").textContent = fmt(atual.brl);
  $("#mPixCod").value = cod;
  $("#mPixKey").textContent = CONFIG.pix;
  $("#mTitular").textContent = CONFIG.pixTitular ? " (" + CONFIG.pixTitular + ")" : "";
  $("#mPixBox").style.display = "block";
  try {
    if (!window.QRCode) await carregar("https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js");
    new QRCode($("#mQr"), { text: cod, width: 176, height: 176, correctLevel: QRCode.CorrectLevel.M });
  } catch (e) { /* sem QR: o copia-e-cola continua funcionando */ }
}
$("#mPixCopy").onclick = async () => {
  const t = $("#mPixCod").value;
  try { await navigator.clipboard.writeText(t); } catch (e) { $("#mPixCod").select(); document.execCommand("copy"); }
  $("#mPixCopy").textContent = "✔ Código copiado!";
  setTimeout(() => { $("#mPixCopy").textContent = "Copiar Pix copia e cola"; }, 1800);
};

/* ---------- Assistente (bot) que abre ao clicar na etiqueta ---------- */
const MSGINT = "Olá {contato}! 👋 Aqui é da {loja}.\nVi que você ({tag}) tem interesse em: {tipo} — {detalhe}.\n\nPosso te ajudar agora! Me conta o que você precisa que eu te passo valores, prazo e como funciona a entrega. 🚀";
const MSGAVAL = "Oi {contato}! 😊 Obrigado pela compra de {produto}. Quando testar no seu jogo, pode me contar em uma frase o que achou e dar uma nota de 1 a 5? Isso ajuda muito a loja e outros criadores a escolherem. Posso publicar o seu depoimento no site (com seu nome ou só as iniciais)?";
const montarAval = o => MSGAVAL.replace(/\{(\w+)\}/g, (_, k) => ({ contato: o.contato, produto: o.produto }[k] || ""));
const montarMsgInt = o => MSGINT.replace(/\{(\w+)\}/g, (_, k) => ({ contato: o.contato, tag: o.tag, tipo: o.tipo, detalhe: o.detalhe, loja: "Lumex Forge" }[k] || ""));
const TIPOS = [...(CONFIG.scriptGratis ? [["gratis", "🎁 Ganhar grátis: " + CONFIG.scriptGratis]] : []), ["pacote", "🎁 Pacotes com desconto"], ["avulso", "🧩 Script avulso"], ["medida", "🛠️ Script sob medida"], ["duvida", "💬 Tirar dúvida"], ["outro", "✨ Outro assunto"]];
let botDados = {}, botIniciado = false;
function botMsg(h, de) {
  const d = document.createElement("div"); d.className = "bm " + (de || "bot"); d.innerHTML = h;
  $("#botB").appendChild(d); $("#botB").scrollTop = 1e6;
}
function botOpcoes(l) { $("#botF").innerHTML = l.map(([k, t]) => `<button data-o="${esc(k)}">${esc(t)}</button>`).join(""); }
function botTexto(ph, obrig, cb) {
  $("#botF").innerHTML = `<input id="botIn" maxlength="300" placeholder="${esc(ph)}"><button id="botOk">Enviar</button>`;
  const ir = () => {
    const v = $("#botIn").value.trim();
    if (obrig && v.length < 3) { $("#botIn").focus(); return; }
    botMsg(esc(v) || "(pular)", "eu"); cb(v);
  };
  $("#botOk").onclick = ir;
  $("#botIn").addEventListener("keydown", e => { if (e.key === "Enter") ir(); });
  setTimeout(() => $("#botIn").focus(), 50);
}
function botInicio() {
  botDados = {};
  botMsg("Oi! 👋 Sou o assistente da Lumex Forge. Sua etiqueta é " + pill(VTAG || "…") + ".<br>O que você procura?");
  botOpcoes(TIPOS);
}
function botContato() {
  botMsg("Qual é o seu contato para o criador te chamar? (@TikTok, usuário do Roblox ou WhatsApp)");
  botTexto("Seu contato", true, v => { botDados.contato = v; botEnviar(); });
}
async function botEnviar() {
  $("#botF").innerHTML = ""; botMsg("Enviando…");
  await prontaTag;
  const o = { tag: VTAG, tipo: botDados.tipo, detalhe: (botDados.detalhe || "").slice(0, 300), contato: botDados.contato.slice(0, 80) };
  const salvo = DB.add("interesses", { ...o }).then(() => DB.mode === "firebase").catch(e => { console.warn("Interesse não salvo", e); return false; });
  const mail = enviarEmail("💬 Novo interesse: " + o.tipo + " (" + o.tag + ")", { etiqueta: o.tag, interesse: o.tipo, detalhe: o.detalhe, contato: o.contato, aparelho: DISP, mensagem_pronta: montarMsgInt(o) });
  const [m, sv] = await Promise.all([mail, salvo]);
  botMsg(m || sv ? "✅ Pronto! Seu pedido foi enviado. O criador vai te chamar pelo contato informado em breve."
                 : "⚠️ Não consegui enviar agora. Chame o criador direto no TikTok @" + CONFIG.tiktok.split("@").pop() + ".");
  botOpcoes([["novo", "Fazer outro pedido"]]);
}
$("#botF").addEventListener("click", e => {
  const k = e.target.dataset.o; if (k === undefined) return;
  if (k === "novo") return botInicio();
  if (k.startsWith("c:") || k.startsWith("g:")) {
    botMsg(esc(k.slice(2)), "eu"); botDados.detalhe = k.slice(2);
    if (k[0] === "g") {
      botMsg("Quer citar algum script em especial? (opcional)");
      botTexto("Ex: sistema de patentes (ou deixe em branco)", false, v => { if (v) botDados.detalhe += " — " + v; botContato(); });
    } else botContato();
    return;
  }
  if (k === "gratis") { botMsg(esc("🎁 Quero o script grátis"), "eu"); botDados.tipo = "Script grátis"; botDados.detalhe = CONFIG.scriptGratis; return botContato(); }
  const t = TIPOS.find(x => x[0] === k); if (!t) return;
  botMsg(esc(t[1]), "eu"); botDados.tipo = t[1].replace(/^\S+\s/, "");
  if (k === "pacote") { botMsg("Qual pacote te interessa?"); botOpcoes([...COMBOS.map(c => ["c:" + c.titulo, c.titulo]), ["c:Quero ver todos", "Quero ver todos"]]); }
  else if (k === "avulso") { botMsg("De que tipo de script?"); botOpcoes(cats.filter(c => c !== "Todos").map(c => ["g:" + c, c])); }
  else botTexto(k === "medida" ? "Descreva o script que você quer" : "Escreva em poucas palavras", true, v => { botDados.detalhe = v; botContato(); });
});
$("#vtag").onclick = () => {
  $("#bot").classList.toggle("open");
  if (!botIniciado) { botIniciado = true; botInicio(); }
};
$("#botX").onclick = () => $("#bot").classList.remove("open");
if ("IntersectionObserver" in window) {
  document.documentElement.classList.add("js");
  const io = new IntersectionObserver(es => es.forEach(e => { if (e.isIntersecting) { e.target.classList.add("in"); io.unobserve(e.target); } }), { rootMargin: "0px 0px -8% 0px" });
  document.querySelectorAll("section h2, section .sub, .tr > div, .about, .step, .faq details, .cta").forEach(el => { el.classList.add("rv"); io.observe(el); });
}
$("#freeBtn").onclick = () => { if (!$("#bot").classList.contains("open")) $("#vtag").click(); };
/* "Avise-me quando sair": registra o interesse num script que ainda não está pronto (mostra a demanda real) */
function pedirExtra(tipo, detalhe) {
  if (!$("#bot").classList.contains("open")) $("#vtag").click();
  botMsg("Quero saber mais sobre: <b>" + esc(tipo) + "</b>", "eu");
  botDados = { tipo, detalhe };
  botContato();
}
function avisarMe(nome) {
  if (!$("#bot").classList.contains("open")) $("#vtag").click();
  botMsg("🔔 Quero ser avisado quando <b>" + esc(nome) + "</b> sair", "eu");
  botDados = { tipo: "Avise-me quando sair", detalhe: nome };
  botContato();
}
document.addEventListener("keydown", e => {
  if (e.key === "Escape") { $("#modal").classList.remove("open"); fecharCarrinho(); $("#bot").classList.remove("open"); }
});

/* ---------- Painel do criador ---------- */
let PEDIDOS = [], VISITAS = [], conhecidos = null, ligado = false, unsubs = [];
const COLS = [["novo", "🆕 Novos"], ["atendendo", "💬 Atendendo"], ["pago", "💰 Pagos"], ["entregue", "📦 Entregues"], ["cancelado", "✖ Cancelados"]];
const PROX = { novo: ["atendendo", "▶️ Iniciar atendimento"], atendendo: ["pago", "✅ Marcar como pago"], pago: ["entregue", "📦 Marcar entregue"] };
const hora = t => new Date(t).toLocaleString("pt-BR", { day: "2-digit", month: "2-digit", hour: "2-digit", minute: "2-digit" });

function toast(t) {
  const d = document.createElement("div");
  d.className = "toast"; d.textContent = t;
  d.style.top = (16 + document.querySelectorAll(".toast").length * 76) + "px";
  document.body.appendChild(d); setTimeout(() => d.remove(), 9000);
}
function bip() {
  try {
    const a = new (window.AudioContext || window.webkitAudioContext)(), o = a.createOscillator(), g = a.createGain();
    o.connect(g); g.connect(a.destination); o.frequency.value = 880; g.gain.setValueAtTime(.15, a.currentTime);
    o.start(); o.stop(a.currentTime + .3);
  } catch (e) {}
}
function avisar(o) {
  toast("🔔 Novo pedido! " + o.tag + " quer " + o.produto + " (" + o.pagamento + ")");
  bip();
  try { if (Notification.permission === "granted") new Notification("Novo pedido na Lumex Forge", { body: o.tag + " · " + o.produto + " · " + o.valor }); } catch (e) {}
}
function card(o, st) {
  const p = PROX[st], c = o.contato || "";
  const tk = c[0] === "@" ? ` <a href="https://www.tiktok.com/@${encodeURIComponent(c.slice(1))}" target="_blank" rel="noopener">abrir TikTok</a>` : "";
  return `<div class="oc ${st === "novo" ? "new" : ""}" data-id="${esc(o.id)}">
    <div class="ocTop">${pill(o.tag || "?")}<small>${hora(o.t)}</small></div>
    <b>${esc(o.produto)}</b>
    <div class="ocMeta">${o.pagamento === "Robux" ? "🟣 Robux" : "💵 Dinheiro"} · ${esc(o.valor)}</div>
    <div class="ocCont">👤 ${esc(c)}${tk}</div>
    <details ${st === "novo" ? "open" : ""}><summary>Mensagem pronta</summary><textarea readonly rows="8">${esc(montarMsg(o))}</textarea></details>
    <div class="ocBtns"><button data-a="copy">📋 Copiar mensagem</button>${p ? `<button data-a="st" data-s="${p[0]}">${p[1]}</button>` : ""}${st === "entregue" ? '<button data-a="aval">⭐ Pedir avaliação</button>' : ""}${st === "cancelado" ? '<button data-a="st" data-s="novo">↩ Reabrir</button>' : st !== "entregue" ? '<button class="bad" data-a="st" data-s="cancelado">✖ Cancelar</button>' : ""}</div>
  </div>`;
}
function renderKan() {
  const n = PEDIDOS.filter(o => (o.status || "novo") === "novo").length;
  $("#cNovos").textContent = n;
  document.title = (n ? "🔔 (" + n + ") " : "") + TIT;
  $("#kan").innerHTML = COLS.map(([st, tt]) => {
    const l = PEDIDOS.filter(o => (o.status || "novo") === st);
    return `<div class="col"><h4>${tt}<span>${l.length}</span></h4>${l.map(o => card(o, st)).join("") || '<div class="vazio">vazio</div>'}</div>`;
  }).join("");
}
function renderVis() {
  $("#visList").innerHTML = `<p class="sub">${VISITAS.length} visitas registradas (as últimas 150 aparecem aqui)</p>` +
    VISITAS.slice(0, 150).map(v => {
      const n = PEDIDOS.filter(o => o.tag === v.tag).length;
      return `<div class="vrow">${pill(v.tag)}<span>${esc(v.disp || "")}</span><small>${hora(v.t)}</small>${n ? `<b class="comp">🛒 ${n} pedido(s)</b>` : ""}</div>`;
    }).join("");
}
function aoReceberPedidos(lista) {
  PEDIDOS = lista;
  const novos = conhecidos ? lista.filter(o => !conhecidos.has(o.id)) : [];
  conhecidos = new Set(lista.map(o => o.id));
  renderKan(); renderVis();
  novos.forEach(avisar);
}
let INTERESSES = [], ONLINE = [], conhecidosInt = null;
function cardInt(o) {
  const st = o.status || "novo";
  return `<div class="oc ${st === "novo" ? "new" : ""}" data-id="${esc(o.id)}">
    <div class="ocTop">${pill(o.tag || "?")}<small>${hora(o.t)}</small></div>
    <b>${esc(o.tipo)}</b>
    <div class="ocMeta">${esc(o.detalhe)}</div>
    <div class="ocCont">👤 ${esc(o.contato)}</div>
    <details ${st === "novo" ? "open" : ""}><summary>Mensagem pronta</summary><textarea readonly rows="6">${esc(montarMsgInt(o))}</textarea></details>
    <div class="ocBtns"><button data-a="copy">📋 Copiar mensagem</button><button data-a="int" data-s="${st === "novo" ? "respondido" : "novo"}">${st === "novo" ? "✔ Marcar respondido" : "↩ Reabrir"}</button></div></div>`;
}
function renderInt() {
  $("#cInt").textContent = INTERESSES.filter(o => (o.status || "novo") === "novo").length;
  $("#intList").innerHTML = INTERESSES.map(cardInt).join("") || '<div class="vazio">Nenhum interesse ainda</div>';
}
function aoReceberInteresses(l) {
  INTERESSES = l;
  const novos = conhecidosInt ? l.filter(o => !conhecidosInt.has(o.id)) : [];
  conhecidosInt = new Set(l.map(o => o.id));
  renderInt();
  novos.forEach(o => { toast("💬 Novo interesse! " + o.tag + " quer " + o.tipo); bip(); });
}
function renderOnline() {
  const on = ONLINE.filter(v => v.t > Date.now() - 100000), fb = DB.mode === "firebase";
  $("#admOnline").textContent = fb ? "🟢 " + on.length + " online" : "";
  $("#onlineBox").innerHTML = fb
    ? `<p class="sub">🟢 ${on.length} pessoa(s) online agora</p><div class="onl">${on.map(v => pill(v.tag) + "<small>" + esc(v.disp || "") + "</small>").join("") || "<small>ninguém no momento</small>"}</div>`
    : '<p class="sub">A lista de quem está online em tempo real funciona no modo Firebase.</p>';
}
setInterval(() => { if (ligado) renderOnline(); }, 15000);
$("#intList").addEventListener("click", async e => {
  const b = e.target.closest("button[data-a]"); if (!b) return;
  const c = b.closest(".oc");
  if (b.dataset.a === "copy") {
    const ta = c.querySelector("textarea");
    try { await navigator.clipboard.writeText(ta.value); } catch (_) { ta.select(); document.execCommand("copy"); }
    b.textContent = "✔ Copiado!"; setTimeout(() => { b.textContent = "📋 Copiar mensagem"; }, 1500);
  } else DB.up("interesses", c.dataset.id, { status: b.dataset.s }).catch(er => toast("Erro ao atualizar: " + er.message));
});
async function iniciarPainel() {
  $("#admLogin").style.display = "none"; $("#admMain").style.display = "block";
  if (ligado) return;
  ligado = true;
  unsubs.push(await DB.on("pedidos", aoReceberPedidos));
  unsubs.push(await DB.on("visitas", l => { VISITAS = l; renderVis(); }));
  unsubs.push(await DB.on("interesses", aoReceberInteresses));
  unsubs.push(await DB.on("online", l => { ONLINE = l; renderOnline(); }));
}
function pararPainel() {
  ligado = false; conhecidos = null; conhecidosInt = null; PEDIDOS = []; VISITAS = []; INTERESSES = []; ONLINE = [];
  unsubs.forEach(f => { try { f(); } catch (e) {} }); unsubs = [];
  document.title = TIT;
  $("#admLogin").style.display = "flex"; $("#admMain").style.display = "none";
}
const BASE_ESTUDOS = `<h4 style="margin:22px 0 8px">Por que o site foi montado assim</h4>
<p class="note">Resumo de estudos usados. São estudos de varejo online em geral: os números não se repetem igual numa loja de scripts, então meça os seus resultados.</p>
<ul class="fontes">
<li><b>Abandono de carrinho (Baymard Institute):</b> checkout simples, preço final claro e sem cadastro obrigatório. <a href="https://baymard.com/lists/cart-abandonment-rate" target="_blank" rel="noopener">baymard.com</a></li>
<li><b>Avaliações (Northwestern, Spiegel Research Center):</b> poucas avaliações reais já aumentam a compra; compra verificada ajuda. <a href="https://spiegel.medill.northwestern.edu/How-Online-Reviews-Influence-Sales" target="_blank" rel="noopener">spiegel.medill.northwestern.edu</a></li>
<li><b>Velocidade no celular (Google e Deloitte):</b> décimos de segundo mudam a conversão. <a href="https://web.dev/case-studies/milliseconds-make-millions" target="_blank" rel="noopener">web.dev</a></li>
<li><b>Pix x cartão (Visa Conecta, 2026):</b> o pagamento é onde mais se abandona; Pix precisa de passos claros e conferência do recebedor. <a href="https://www.band.com.br/economia/noticias/pix-rivaliza-com-cartao-de-credito-em-preferencia-no-e-commerce-diz-estudo-202602261303" target="_blank" rel="noopener">band.com.br</a></li>
<li><b>Pacotes e descontos:</b> descontos muito altos corroem a margem; confira o desconto real de cada pacote e ajuste em CONFIG.precoFatorPacote.</li>
</ul>`;
function renderCfg() {
  const fb = DB.mode === "firebase", todos = [...PRODUTOS, ...COMBOS];
  const nRbx = todos.filter(p => (p.linkRobux || "").startsWith("http")).length, nDemo = Object.keys(DEMOS).length;
  const itens = [
    [pixOk(), "Chave Pix", "Preencha CONFIG.pix para o QR Code e o copia e cola aparecerem."],
    [pixOk() && !/SUA CIDADE/i.test(CONFIG.pixCidade || ""), "Cidade do Pix", "Troque CONFIG.pixCidade pela sua cidade, sem acento."],
    [!/COLE/i.test(CONFIG.emailKey || "COLE"), "E-mail no Gmail (Web3Forms)", "Cole a chave em CONFIG.emailKey para receber pedidos e interesses por e-mail."],
    [fb, "Firebase (pedidos de qualquer pessoa, etiqueta única e quem está online)", "Preencha CONFIG.firebase e cole as regras do Firestore. Sem isso o painel funciona só neste navegador."],
    [nRbx > 0, "Links de pagamento em Robux (Game Pass): " + nRbx + " de " + todos.length, "Sem o link, o cliente que paga em Robux recebe o link por mensagem sua."],
    [nDemo > 0, "Demonstrações em vídeo: " + nDemo, "Cole links do TikTok em DEMOS para aparecer ▶ Ver demonstração no card."],
    [(CONFIG.prontos || []).length > 0, "Lista de scripts prontos (CONFIG.prontos)", "Sem ela, TODOS os scripts aparecem à venda. Liste só os que você já tem prontos; os outros viram “Em breve”."],
    [fb || CONFIG.pinLocal !== "1234", "PIN do modo teste", "Troque CONFIG.pinLocal (o padrão 1234 é público)."]
  ];
  const ok = itens.filter(x => x[0]).length;
  $("#cfgList").innerHTML = `<p class="sub">${ok} de ${itens.length} itens prontos</p>` +
    itens.map(([v, t, d]) => `<div class="cfg"><span>${v ? "✅" : "⚠️"}</span><div><b>${esc(t)}</b>${v ? "" : "<small>" + esc(d) + "</small>"}</div></div>`).join("") + BASE_ESTUDOS;
}
async function abrirPainel() {
  $("#adm").classList.add("open"); document.body.style.overflow = "hidden";
  await DB.pronto;
  const fb = DB.mode === "firebase";
  $("#admModo").textContent = fb ? "🟢 Online" : "🟡 Modo teste (só neste navegador)";
  $("#admEmail").style.display = fb ? "block" : "none";
  if (fb && CONFIG.adminEmail && !$("#admEmail").value) { $("#admEmail").value = CONFIG.adminEmail; setTimeout(() => $("#admSenha").focus(), 50); }
  $("#admSenha").placeholder = fb ? "Senha" : "PIN";
  renderCfg();
  $("#admAviso").textContent = fb ? "Entre com o e-mail e a senha do criador." : "Modo teste: configure o Firebase para receber pedidos de qualquer pessoa. Digite o PIN definido em CONFIG.pinLocal.";
}
DB.pronto.then(() => { if (DB.mode === "firebase") DB.auth.onAuthStateChanged(u => u ? iniciarPainel() : pararPainel()); });

$("#abrirPainel").onclick = e => { e.preventDefault(); abrirPainel(); };
if (location.hash === "#painel") abrirPainel();
$("#admFechar").onclick = () => { $("#adm").classList.remove("open"); document.body.style.overflow = ""; };
$("#admSair").onclick = async () => {
  await DB.pronto;
  if (DB.mode === "firebase") await DB.auth.signOut(); else pararPainel();
  $("#admFechar").click();
};
$("#admEntrar").onclick = async () => {
  $("#admErro").textContent = "";
  try {
    await DB.pronto;
    if (DB.mode === "firebase") await DB.auth.signInWithEmailAndPassword($("#admEmail").value.trim(), $("#admSenha").value);
    else if ($("#admSenha").value === CONFIG.pinLocal) iniciarPainel();
    else throw new Error("PIN incorreto");
  } catch (e) { $("#admErro").textContent = "Não foi possível entrar: " + (e.message || "erro"); }
};
$("#admSenha").addEventListener("keydown", e => { if (e.key === "Enter") $("#admEntrar").click(); });
$("#admNotif").onclick = async () => {
  try { const r = await Notification.requestPermission(); toast(r === "granted" ? "🔔 Avisos do navegador ativados" : "Avisos bloqueados no navegador"); }
  catch (e) { toast("Este navegador não permite avisos"); }
  bip();
};
document.querySelectorAll(".adm-tabs .chip").forEach(b => b.onclick = () => {
  document.querySelectorAll(".adm-tabs .chip").forEach(x => x.classList.toggle("on", x === b));
  [["ped", "tabPed"], ["vis", "tabVis"], ["int", "tabInt"], ["cfg", "tabCfg"]].forEach(([k, id]) => { $("#" + id).style.display = b.dataset.tab === k ? "block" : "none"; });
});
$("#kan").addEventListener("click", async e => {
  const b = e.target.closest("button[data-a]"); if (!b) return;
  const c = b.closest(".oc");
  if (b.dataset.a === "copy") {
    const ta = c.querySelector("textarea");
    try { await navigator.clipboard.writeText(ta.value); } catch (_) { ta.select(); document.execCommand("copy"); }
    b.textContent = "✔ Copiado!"; setTimeout(() => { b.textContent = "📋 Copiar mensagem"; }, 1500);
  } else if (b.dataset.a === "aval") {
    const o = PEDIDOS.find(x => x.id === c.dataset.id); if (!o) return;
    try { await navigator.clipboard.writeText(montarAval(o)); b.textContent = "✔ Mensagem copiada!"; } catch (_) { b.textContent = "Não consegui copiar"; }
    setTimeout(() => { b.textContent = "⭐ Pedir avaliação"; }, 1800);
  } else DB.up("pedidos", c.dataset.id, { status: b.dataset.s }).catch(er => toast("Erro ao atualizar: " + er.message));
});
</script>
</body>
</html>
