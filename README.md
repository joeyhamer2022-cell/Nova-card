# Nova-card
Visa card
<!doctype html>
<html lang="nl">
<head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#f8f9ff"><title>Nova — Kaart demo</title>
<style>
:root{--blue:#1912ed;--ink:#151620;--muted:#737d90;--line:#e7e9f2;--bg:#f8f9ff}
*{box-sizing:border-box}body{margin:0;background:var(--bg);color:var(--ink);font-family:Inter,system-ui,-apple-system,"Segoe UI",sans-serif}
button,input{font:inherit}button,a{cursor:pointer}a{text-decoration:none;color:inherit}
header{height:78px;background:#fff;border-bottom:1px solid var(--line);display:flex;align-items:center;justify-content:space-between;padding:0 clamp(18px,5vw,56px);position:sticky;top:0;z-index:4}
.brand{display:flex;align-items:center;gap:10px;color:var(--blue);font-size:29px;font-weight:850;letter-spacing:-1.4px}
.mark{width:31px;height:37px;background:linear-gradient(135deg,#15d9b0,#1764ff 55%,#3210dc);clip-path:polygon(50% 0,100% 15%,100% 70%,50% 100%,0 70%,0 15%)}
.header-actions{display:flex;gap:10px;align-items:center}.btn{border:0;border-radius:999px;padding:14px 23px;background:var(--blue);color:white;font-weight:700;box-shadow:0 8px 20px #1912ed20}.btn.secondary{background:white;color:var(--blue);border:1.5px solid var(--blue);box-shadow:none}.btn:hover{transform:translateY(-1px)}
main{max-width:1100px;margin:auto;padding:55px 24px 75px}.hero{text-align:center}.eyebrow{color:var(--blue);font-size:13px;font-weight:800;letter-spacing:1.5px;text-transform:uppercase}
h1{font-size:clamp(43px,7vw,76px);line-height:1;letter-spacing:-3.7px;margin:17px auto 30px;max-width:780px}h1 span{color:var(--blue)}
.banner{display:flex;align-items:center;justify-content:space-between;gap:25px;text-align:left;padding:25px 35px;border-radius:28px;color:white;background:radial-gradient(circle at 10% 100%,#a21ad1,transparent 36%),linear-gradient(110deg,#2414c9,#1266ee 58%,#00b978);min-height:160px}
.card{width:230px;height:135px;flex:none;border-radius:16px;background:linear-gradient(140deg,#282d38,#080a10);padding:17px;color:white;display:flex;flex-direction:column;justify-content:space-between;transform:rotate(-6deg);box-shadow:0 17px 28px #080a1245;border:1px solid #ffffff30}
.cardname{font-size:12px;font-weight:850;letter-spacing:.6px}.chip{height:23px;width:30px;border-radius:5px;background:linear-gradient(135deg,#eee9d6,#aaa89c);border:1px solid #fff8}.cardfoot{display:flex;justify-content:space-between;font-size:11px;font-weight:800}
.banner h2{font-size:23px;margin:0 0 8px}.banner p{margin:0;color:#e3eaff;line-height:1.5}
.payments{text-align:center;margin:36px 0 12px;color:var(--muted);font-weight:650}.logos{display:flex;justify-content:center;gap:13px}.logos span{background:white;border:1px solid var(--line);border-radius:20px;width:62px;height:62px;display:grid;place-items:center;font-size:27px;font-weight:850}
.preview{display:flex;align-items:flex-end;justify-content:center;gap:0;min-height:400px;margin:42px auto 0}
.phone{width:225px;height:390px;background:#fff;border:8px solid #181b24;border-radius:36px;padding:17px 13px;box-shadow:0 22px 45px #12172a25;transform:translateX(30px);text-align:left}
.phone:before{content:"";display:block;width:75px;height:17px;border-radius:20px;background:#151820;margin:-10px auto 19px}
.appbrand{font-weight:850;color:var(--blue);margin-bottom:23px}.muted{font-size:10px;color:var(--muted)}.balance{font-size:25px;font-weight:850;margin:4px 0 16px}
.phone .card{width:100%;height:112px;transform:none;padding:13px;border-radius:12px}.phone .cardfoot{font-size:10px}
.activity{font-size:10px;color:var(--muted);margin-top:20px;font-weight:700}.tx{padding:12px 0;border-bottom:1px solid var(--line);display:flex;justify-content:space-between;font-size:10px}
.boxcard{width:250px;height:160px;margin:0 0 22px -42px;border-radius:17px;padding:20px;background:linear-gradient(140deg,#292d37,#080a10);color:#fff;transform:rotate(-8deg);box-shadow:0 20px 35px #12172a30}
.boxcard .cardname{margin-top:20px}.boxcard small{display:block;color:#aeb8c9;margin-top:32px;font-size:9px}
.auth-wrap{max-width:470px;margin:22px auto 0;background:white;border:1px solid var(--line);border-radius:26px;padding:30px;box-shadow:0 18px 50px #1d24500b}
.auth-wrap h2{font-size:28px;margin:0 0 8px;letter-spacing:-1px}.sub{color:var(--muted);font-size:14px;margin:0 0 23px;line-height:1.5}
.tabs{display:flex;background:#f1f2fa;padding:5px;border-radius:999px;margin-bottom:22px}.tabs button{flex:1;border:0;background:transparent;padding:11px;border-radius:999px;color:#626b7d;font-weight:700}.tabs button.active{background:white;color:var(--blue);box-shadow:0 2px 8px #10142a12}
label{display:block;font-size:13px;font-weight:700;margin:14px 0 7px}input{width:100%;border:1px solid #dfe2ed;border-radius:12px;padding:13px 14px;outline:none;background:#fff}input:focus{border-color:var(--blue);box-shadow:0 0 0 3px #1912ed14}
.full{width:100%;margin-top:20px}.notice{font-size:11px;line-height:1.5;color:#8a91a1;margin:14px 0 0}
.dashboard{max-width:850px;margin:25px auto 0}.dashhead{display:flex;align-items:center;justify-content:space-between;gap:15px;margin-bottom:22px}.dashhead h2{margin:0;font-size:30px;letter-spacing:-1px}.dashgrid{display:grid;grid-template-columns:1.2fr .8fr;gap:17px}.panel{background:#fff;border:1px solid var(--line);border-radius:22px;padding:22px;text-align:left}.panel h3{margin:0 0 15px;font-size:16px}.demo-balance{font-size:34px;font-weight:850;letter-spacing:-1px;margin:5px 0 18px}.dashcard{height:170px;border-radius:17px;background:linear-gradient(130deg,#252b39,#080a11);color:#fff;padding:20px;display:flex;flex-direction:column;justify-content:space-between}.status{display:inline-block;border-radius:99px;background:#e8f8ef;color:#138347;padding:6px 10px;font-size:11px;font-weight:800}
.hidden{display:none!important}footer{text-align:center;background:#fff;border-top:1px solid var(--line);padding:22px;color:#8991a1;font-size:12px}
@media(max-width:650px){header{height:70px}.brand{font-size:25px}.header-actions .secondary{display:none}main{padding:45px 17px 55px}h1{letter-spacing:-2.4px}.banner{padding:18px;min-height:130px;gap:15px;border-radius:22px}.banner .card{width:132px;height:87px;padding:10px;border-radius:11px}.banner .cardname{font-size:9px}.banner .chip{width:22px;height:16px}.banner .cardfoot{font-size:8px}.banner h2{font-size:17px}.banner p{font-size:11px}.preview{min-height:350px}.phone{width:205px;height:360px;transform:translateX(19px)}.boxcard{width:205px;height:135px;margin-left:-48px;padding:16px}.boxcard .cardname{margin-top:13px}.boxcard small{margin-top:24px}.dashgrid{grid-template-columns:1fr}.auth-wrap{padding:24px 20px}}
</style>
</head>
<body>
<header><a class="brand" href="#" onclick="showPage('home');return false"><span class="mark"></span>nova</a><div class="header-actions"><button class="btn secondary" onclick="showPage('login')">Inloggen</button><button class="btn" onclick="showPage('register')">Account maken</button></div></header>
<main>
<section id="home">
 <div class="hero"><div class="eyebrow">Een frisse digitale kaartdemo</div><h1>Jouw kaart.<br>Jouw stijl.<br><span>Jouw overzicht.</span></h1></div>
 <section class="banner"><div class="card"><div class="cardname">✦ NOVA</div><div class="chip"></div><div class="cardfoot"><span>•••• ••••</span><span>DEMO</span></div></div><div><h2>Alles overzichtelijk op één plek</h2><p>Een modern kaartconcept met een eenvoudige demo-app.</p></div></section>
 <div class="payments">Een helder ontwerp op elk scherm</div><div class="logos"><span>◉</span><span>●</span><span style="color:#4285f4">G</span></div>
 <section class="preview"><div class="boxcard"><div class="cardname">✦ NOVA</div><div class="chip"></div><small>JOUW KAART. JOUW OVERZICHT.</small></div><div class="phone"><div class="appbrand">✦ NOVA</div><div class="muted">Demo saldo</div><div class="balance">€ 2.450,00</div><div class="card"><div class="cardname">✦ NOVA</div><div class="chip"></div><div class="cardfoot"><span>•••• 4821</span><span>DEMO</span></div></div><div class="activity">RECENTE ACTIVITEIT</div><div class="tx"><span>Online aankoop</span><b>− € 24,50</b></div><div class="tx"><span>Abonnement</span><b>− € 8,99</b></div></div></section>
 <div style="text-align:center;margin-top:10px"><button class="btn" onclick="showPage('register')">Bekijk de demo</button></div>
</section>

<section id="login" class="hidden">
 <div class="auth-wrap"><div class="eyebrow">Welkom terug</div><h2>Log in bij Nova</h2><p class="sub">Dit is een lokale demo. Je gegevens worden niet verstuurd of opgeslagen.</p>
 <div class="tabs"><button class="active" onclick="showPage('login')">Inloggen</button><button onclick="showPage('register')">Registreren</button></div>
 <form onsubmit="event.preventDefault();showPage('dashboard')"><label for="loginmail">E-mailadres (demo)</label><input id="loginmail" type="email" placeholder="naam@voorbeeld.nl" required><label for="loginpass">Demo-wachtwoord</label><input id="loginpass" type="password" placeholder="Vul iets in voor de demo" required><button class="btn full" type="submit">Inloggen in demo</button></form>
 <p class="notice">Gebruik geen echt wachtwoord of echte bankgegevens. Deze knop opent alleen het voorbeeld-dashboard.</p></div>
</section>

<section id="register" class="hidden">
 <div class="auth-wrap"><div class="eyebrow">Start met Nova</div><h2>Maak een demo-account</h2><p class="sub">Vul testgegevens in om het voorbeeld-dashboard te bekijken.</p>
 <div class="tabs"><button onclick="showPage('login')">Inloggen</button><button class="active" onclick="showPage('register')">Registreren</button></div>
 <form onsubmit="event.preventDefault();showPage('dashboard')"><label for="fullname">Naam</label><input id="fullname" placeholder="Jouw naam" required><label for="regmail">E-mailadres (demo)</label><input id="regmail" type="email" placeholder="naam@voorbeeld.nl" required><label for="regpass">Demo-wachtwoord</label><input id="regpass" type="password" placeholder="Kies iets voor deze demo" required><button class="btn full" type="submit">Account bekijken</button></form>
 <p class="notice">Dit formulier maakt geen echt account aan. Er worden geen gegevens opgeslagen of doorgestuurd.</p></div>
</section>

<section id="dashboard" class="hidden dashboard">
 <div class="dashhead"><div><div class="eyebrow">Nova demo-app</div><h2>Jouw dashboard</h2></div><button class="btn secondary" onclick="showPage('home')">Uitloggen</button></div>
 <div class="dashgrid"><div class="panel"><h3>Demo saldo</h3><div class="demo-balance">€ 2.450,00</div><span class="status">● Voorbeeldaccount</span><p class="sub" style="margin:18px 0 0">Dit bedrag is fictief en heeft geen echte geldwaarde.</p></div>
 <div class="panel"><h3>Jouw demo-kaart</h3><div class="dashcard"><div class="cardname">✦ NOVA</div><div class="chip"></div><div class="cardfoot"><span>•••• 4821</span><span>DEMO</span></div></div></div>
 <div class="panel"><h3>Recente activiteit</h3><div class="tx"><span>Online aankoop</span><b>− € 24,50</b></div><div class="tx"><span>Abonnement</span><b>− € 8,99</b></div><div class="tx"><span>Terugbetaling</span><b>+ € 12,00</b></div></div>
 <div class="panel"><h3>Snelle acties</h3><button class="btn secondary" style="width:100%;margin:4px 0 10px" onclick="alert('Dit is alleen een visuele demo.')">Kaart bekijken</button><button class="btn secondary" style="width:100%" onclick="alert('Er wordt geen betaling uitgevoerd.')">Betaling simuleren</button></div></div>
</section>
</main>
<footer>© 2026 Nova — fictieve website-demo. Geen bank, betaalkaart of financiële dienst.</footer>
<script>
function showPage(page){
  ['home','login','register','dashboard'].forEach(id=>document.getElementById(id).classList.toggle('hidden',id!==page));
  window.scrollTo({top:0,behavior:'smooth'});
}
</script>
</body></html>
