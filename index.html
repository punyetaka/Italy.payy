<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>BancaSecure — Bonifico in Entrata</title>
<meta name="description" content="Ricevi il tuo bonifico SEPA in entrata in modo sicuro e professionale." />
<script src="https://cdn.tailwindcss.com"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0b1220;
    --card:#121b2e;
    --card-2:#0f1729;
    --border:#1f2a44;
    --muted:#8a95ad;
    --text:#e9eef8;
    --primary:#0a84ff;
    --primary-2:#3aa0ff;
    --green:#16c47f;
    --amber:#f5b400;
    --red:#ef4444;
    --gold:#c9a24a;
  }
  html,body{background:var(--bg);color:var(--text);font-family:'Inter',system-ui,sans-serif;}
  .mono{font-family:'JetBrains Mono',monospace;}
  .card{background:var(--card);border:1px solid var(--border);border-radius:18px;}
  .card-2{background:var(--card-2);border:1px solid var(--border);border-radius:14px;}
  .btn-primary{background:linear-gradient(135deg,var(--primary),var(--primary-2));color:#fff;font-weight:700;}
  .btn-primary:active{transform:scale(.98);}
  .chip{font-size:10px;letter-spacing:.14em;text-transform:uppercase;color:var(--muted);}
  .divider{height:1px;background:var(--border);}
  .fade-in{animation:fi .35s ease;}
  @keyframes fi{from{opacity:0;transform:translateY(6px);}to{opacity:1;transform:none;}}
  .stamp{
    color:#f5b400;border:3px solid #f5b400;padding:6px 14px;border-radius:6px;
    font-weight:800;letter-spacing:.18em;transform:rotate(-8deg);
    text-transform:uppercase;font-size:14px;opacity:.95;
    box-shadow:inset 0 0 0 2px rgba(245,180,0,.15);
  }
  .it-flag{display:inline-flex;border-radius:3px;overflow:hidden;width:18px;height:12px;border:1px solid rgba(255,255,255,.15);}
  .it-flag i{flex:1;}
  .it-flag .g{background:#008C45;}
  .it-flag .w{background:#F4F5F0;}
  .it-flag .r{background:#CD212A;}
  input{background:transparent;outline:none;}
  .modal-bg{background:rgba(2,6,20,.7);backdrop-filter:blur(6px);}
  .progress-track{background:#1c2742;border-radius:999px;height:6px;overflow:hidden;}
  .progress-fill{height:100%;background:linear-gradient(90deg,var(--primary),var(--primary-2));transition:width .15s linear;}
</style>
</head>
<body class="min-h-screen">
<div id="app" class="mx-auto max-w-md min-h-screen relative"></div>

<script>
const FEE = 50;
const AMOUNT = 1000;
const SUPPORT_URL = "https://t.me/customer_assist01";
const TXN_ID = "BNK-" + Math.random().toString(36).slice(2,8).toUpperCase() + "-" + Date.now().toString().slice(-5);
const REF = "SEPA-" + Math.random().toString(36).slice(2,10).toUpperCase();
const NOW = new Date();
const fmtDate = (d)=> d.toLocaleString("it-IT",{day:"2-digit",month:"2-digit",year:"numeric",hour:"2-digit",minute:"2-digit"});
const eur = (n)=> "€" + n.toLocaleString("it-IT",{minimumFractionDigits:2,maximumFractionDigits:2});

let state = { screen:"home", iban:"", holder:"" };
const app = document.getElementById("app");

function render(){
  app.innerHTML = "";
  if(state.screen==="home") app.appendChild(HomeScreen());
  if(state.screen==="iban") app.appendChild(IbanScreen());
  if(state.screen==="loading") app.appendChild(LoadingScreen());
  if(state.screen==="receipt") app.appendChild(ReceiptScreen());
}

function Header(title, back){
  const h = document.createElement("header");
  h.className="flex items-center justify-between px-5 pt-6 pb-3";
  h.innerHTML = `
    <div class="flex items-center gap-2">
      ${back?`<button id="back" class="w-9 h-9 rounded-full card-2 flex items-center justify-center">‹</button>`:`
      <div class="w-9 h-9 rounded-full flex items-center justify-center" style="background:linear-gradient(135deg,#0a84ff,#3aa0ff);font-weight:800">B</div>`}
      <div>
        <p class="text-[10px] text-[color:var(--muted)] tracking-widest uppercase">${title||"BancaSecure"}</p>
        <p class="text-sm font-bold flex items-center gap-1">Bonifico SEPA <span class="it-flag"><i class="g"></i><i class="w"></i><i class="r"></i></span></p>
      </div>
    </div>
    <button class="w-9 h-9 rounded-full card-2 flex items-center justify-center text-[color:var(--muted)]">⚙</button>
  `;
  if(back){ setTimeout(()=>document.getElementById("back").onclick=back,0); }
  return h;
}

function HomeScreen(){
  const w = document.createElement("div");
  w.className="fade-in";
  w.appendChild(Header());
  const inner = document.createElement("div");
  inner.className="px-5 pb-8";
  inner.innerHTML = `
    <div class="card-2 p-3 mb-4 flex items-center gap-3">
      <div class="w-2 h-2 rounded-full" style="background:var(--green);box-shadow:0 0 12px var(--green)"></div>
      <p class="text-xs text-[color:var(--muted)]">Notifica in tempo reale · ${fmtDate(NOW)}</p>
    </div>
    <div class="card p-6 mb-4" style="background:linear-gradient(160deg,#0f2240,#0b1220);">
      <p class="chip mb-2">Bonifico in entrata</p>
      <div class="flex items-baseline gap-2">
        <span class="text-3xl text-[color:var(--muted)]">€</span>
        <span class="text-5xl font-extrabold tracking-tight">1.000<span class="text-2xl text-[color:var(--muted)]">,00</span></span>
      </div>
      <p class="text-xs text-[color:var(--muted)] mt-1">EUR · SEPA Instant Credit Transfer</p>
      <div class="divider my-5"></div>
      <div class="space-y-3 text-sm">
        <div class="flex justify-between"><span class="text-[color:var(--muted)]">Mittente</span><span class="font-semibold">— — —</span></div>
        <div class="flex justify-between"><span class="text-[color:var(--muted)]">Causale</span><span class="font-semibold">Pagamento privato</span></div>
        <div class="flex justify-between"><span class="text-[color:var(--muted)]">Riferimento</span><span class="mono text-xs">${REF}</span></div>
        <div class="flex justify-between"><span class="text-[color:var(--muted)]">Data valuta</span><span class="font-semibold">${fmtDate(NOW)}</span></div>
      </div>
    </div>
    <div class="card-2 p-4 mb-5 flex gap-3">
      <div class="w-8 h-8 rounded-full flex items-center justify-center" style="background:rgba(10,132,255,.15);color:var(--primary-2)">🛡</div>
      <div class="text-xs leading-relaxed">
        <p class="font-bold mb-1">Operazione verificata</p>
        <p class="text-[color:var(--muted)]">Il bonifico è stato firmato digitalmente secondo lo standard SEPA SCT Inst. Accetta per accreditare i fondi sul tuo IBAN.</p>
      </div>
    </div>
    <button id="accept" class="btn-primary w-full h-14 rounded-full text-base">Accetta €1.000,00</button>
    <button id="reject" class="w-full h-12 mt-2 rounded-full text-sm text-[color:var(--muted)]">Rifiuta</button>
    <p class="text-[10px] text-[color:var(--muted)] text-center mt-5">BancaSecure S.p.A. · Vigilata da Banca d'Italia · IBAN protetto</p>
  `;
  w.appendChild(inner);
  setTimeout(()=>{
    document.getElementById("accept").onclick=()=>{state.screen="iban";render();};
    document.getElementById("reject").onclick=()=>alert("Operazione annullata.");
  },0);
  return w;
}

function IbanScreen(){
  const w=document.createElement("div");
  w.className="fade-in";
  w.appendChild(Header("Accredito",()=>{state.screen="home";render();}));
  const inner=document.createElement("div");
  inner.className="px-5 pb-8";
  inner.innerHTML=`
    <div class="mb-5">
      <p class="chip mb-1">Passo 1 di 2</p>
      <h1 class="text-2xl font-extrabold leading-tight">Dove vuoi ricevere<br/>i tuoi €1.000,00?</h1>
      <p class="text-sm text-[color:var(--muted)] mt-2">Inserisci l'IBAN del conto su cui vuoi accreditare il bonifico in entrata.</p>
    </div>
    <div class="card p-4 mb-3">
      <label class="chip">IBAN beneficiario</label>
      <input id="iban" maxlength="34" placeholder="IT00 X000 0000 0000 0000 0000 000"
        class="mono w-full text-base font-semibold tracking-wider mt-1 placeholder:text-[color:var(--muted)] placeholder:font-normal" value="${state.iban}"/>
      <p id="ibanHint" class="text-[11px] text-[color:var(--muted)] mt-2">Formato italiano: IT + 2 cifre di controllo + 23 caratteri</p>
    </div>
    <div class="card p-4 mb-5">
      <label class="chip">Nome e cognome intestatario</label>
      <input id="holder" placeholder="Mario Rossi"
        class="w-full text-base font-semibold mt-1 placeholder:text-[color:var(--muted)] placeholder:font-normal" value="${state.holder}"/>
    </div>
    <div class="card-2 p-3 mb-5 flex gap-2 text-[11px] text-[color:var(--muted)]">
      <span>🔒</span>
      <span>I tuoi dati sono cifrati end-to-end e usati esclusivamente per l'accredito SEPA. Non condividere mai le tue credenziali.</span>
    </div>
    <button id="confirm" class="btn-primary w-full h-14 rounded-full">Conferma accredito</button>
  `;
  w.appendChild(inner);
  setTimeout(()=>{
    const ibanEl=document.getElementById("iban");
    const holderEl=document.getElementById("holder");
    ibanEl.addEventListener("input",e=>{
      let v=e.target.value.toUpperCase().replace(/[^A-Z0-9]/g,"");
      v=v.match(/.{1,4}/g)?.join(" ")||"";
      e.target.value=v; state.iban=v;
    });
    holderEl.addEventListener("input",e=>state.holder=e.target.value);
    document.getElementById("confirm").onclick=()=>{
      const raw=state.iban.replace(/\s/g,"");
      if(raw.length<15){document.getElementById("ibanHint").textContent="IBAN non valido. Verifica e riprova.";document.getElementById("ibanHint").style.color="var(--red)";return;}
      if(state.holder.trim().length<3){alert("Inserisci nome e cognome dell'intestatario.");return;}
      state.screen="loading";render();
    };
  },0);
  return w;
}

function LoadingScreen(){
  const w=document.createElement("div");
  w.className="fade-in min-h-screen flex flex-col";
  w.innerHTML=`
    <div class="flex-1 flex flex-col items-center justify-center px-6 text-center">
      <div class="relative w-32 h-32 mb-6">
        <svg viewBox="0 0 100 100" class="w-full h-full -rotate-90">
          <circle cx="50" cy="50" r="44" fill="none" stroke="#1c2742" stroke-width="6"/>
          <circle id="ring" cx="50" cy="50" r="44" fill="none" stroke="url(#g)" stroke-width="6" stroke-linecap="round"
            stroke-dasharray="276.46" stroke-dashoffset="276.46" style="transition:stroke-dashoffset .15s linear"/>
          <defs><linearGradient id="g" x1="0" x2="1"><stop offset="0" stop-color="#0a84ff"/><stop offset="1" stop-color="#3aa0ff"/></linearGradient></defs>
        </svg>
        <div class="absolute inset-0 flex items-center justify-center">
          <span id="pct" class="text-2xl font-extrabold mono">0%</span>
        </div>
      </div>
      <h2 class="text-lg font-bold mb-1">Elaborazione in corso</h2>
      <p id="stage" class="text-sm text-[color:var(--muted)] min-h-[40px]">Connessione sicura al circuito SEPA…</p>
      <div class="w-full max-w-xs mt-4 progress-track"><div id="bar" class="progress-fill" style="width:0%"></div></div>
      <p class="text-[10px] text-[color:var(--muted)] mt-6">Non chiudere questa pagina</p>
    </div>
  `;
  setTimeout(()=>{
    const stages=[
      "Connessione sicura al circuito SEPA…",
      "Verifica IBAN beneficiario…",
      "Controllo antifrode AML/KYC…",
      "Autorizzazione Banca d'Italia…",
      "Inoltro fondi al conto destinatario…",
      "Finalizzazione bonifico…"
    ];
    const start=Date.now();
    const ring=document.getElementById("ring");
    const pct=document.getElementById("pct");
    const bar=document.getElementById("bar");
    const stageEl=document.getElementById("stage");
    const id=setInterval(()=>{
      const e=Date.now()-start;
      const p=Math.min(100,(e/12000)*100);
      pct.textContent=Math.floor(p)+"%";
      ring.setAttribute("stroke-dashoffset", 276.46*(1-p/100));
      bar.style.width=p+"%";
      stageEl.textContent=stages[Math.min(stages.length-1,Math.floor(p/100*stages.length))];
      if(e>=12000){clearInterval(id);state.screen="receipt";render();}
    },80);
  },0);
  return w;
}

function ReceiptScreen(){
  const w=document.createElement("div");
  w.className="fade-in";
  w.appendChild(Header("Ricevuta",()=>{state.screen="home";render();}));
  const inner=document.createElement("div");
  inner.className="px-5 pb-8";
  inner.innerHTML=`
    <div class="card p-6 relative overflow-hidden">
      <div class="absolute top-5 right-5"><div class="stamp">In Sospeso</div></div>
      <div class="flex items-center gap-2 mb-1">
        <span class="it-flag"><i class="g"></i><i class="w"></i><i class="r"></i></span>
        <p class="chip">Ricevuta SEPA</p>
      </div>
      <h2 class="text-xl font-extrabold">BancaSecure S.p.A.</h2>
      <p class="text-[11px] text-[color:var(--muted)]">Sede legale: Via Veneto 89, 00187 Roma · ABI 03069</p>
      <div class="divider my-4"></div>
      <p class="chip">Importo bonifico</p>
      <p class="text-4xl font-extrabold">${eur(AMOUNT)}<span class="text-base text-[color:var(--muted)] ml-1">EUR</span></p>
      <div class="grid grid-cols-2 gap-3 mt-5 text-sm">
        <div><p class="chip">Beneficiario</p><p class="font-semibold">${state.holder||"—"}</p></div>
        <div><p class="chip">Mittente</p><p class="font-semibold">— — —</p></div>
        <div class="col-span-2"><p class="chip">IBAN destinatario</p><p class="mono text-sm font-semibold break-all">${state.iban||"—"}</p></div>
        <div><p class="chip">ID transazione</p><p class="mono text-xs">${TXN_ID}</p></div>
        <div><p class="chip">Riferimento SEPA</p><p class="mono text-xs">${REF}</p></div>
        <div><p class="chip">Data operazione</p><p class="text-xs font-semibold">${fmtDate(NOW)}</p></div>
        <div><p class="chip">Canale</p><p class="text-xs font-semibold">SEPA SCT Inst</p></div>
      </div>
      <div class="divider my-4"></div>
      <div class="flex justify-between text-sm">
        <span class="text-[color:var(--muted)]">Stato</span>
        <span class="font-bold" style="color:var(--amber)">● PENDING — In attesa di conferma</span>
      </div>
    </div>
    <div class="card-2 p-4 mt-4 border" style="border-color:rgba(245,180,0,.35);background:rgba(245,180,0,.06)">
      <p class="font-bold text-sm mb-1" style="color:var(--amber)">⚠ Conferma finale richiesta</p>
      <p class="text-xs text-[color:var(--muted)] leading-relaxed">
        Il tuo bonifico di <span class="font-semibold text-[color:var(--text)]">€1.000,00</span> è stato instradato correttamente al tuo IBAN, ma risulta <span class="font-semibold text-[color:var(--text)]">PENDING</span> presso la stanza di compensazione.
        Per sbloccare l'accredito è necessario versare una commissione di conferma SEPA pari a
        <span class="font-bold" style="color:var(--text)"> ${eur(FEE)}</span>.
      </p>
      <div class="mt-3 grid grid-cols-2 gap-2 text-[11px]">
        <div class="card-2 p-2"><p class="chip">Commissione</p><p class="font-bold">${eur(FEE)}</p></div>
        <div class="card-2 p-2"><p class="chip">Tempo rilascio</p><p class="font-bold">2–5 minuti</p></div>
      </div>
    </div>
    <button id="pay" class="btn-primary w-full h-14 rounded-full mt-4">Paga ${eur(FEE)} e sblocca</button>
    <button id="support" class="w-full h-12 mt-2 rounded-full card-2 font-semibold text-sm flex items-center justify-center gap-2">
      💬 Contatta supporto BancaSecure
    </button>
    <p class="text-[10px] text-[color:var(--muted)] text-center mt-5 leading-relaxed">
      Documento generato automaticamente. Conserva la ricevuta come prova dell'operazione.<br/>
      BancaSecure S.p.A. · IVASS A000123 · Capitale sociale €120.000.000 i.v.
    </p>
  `;
  w.appendChild(inner);
  setTimeout(()=>{
    document.getElementById("support").onclick=()=>openSupport();
    document.getElementById("pay").onclick=()=>openSupport();
  },0);
  return w;
}

function openSupport(){
  const m=document.createElement("div");
  m.className="fixed inset-0 modal-bg flex items-end sm:items-center justify-center z-50 p-4";
  m.innerHTML=`
    <div class="card w-full max-w-sm p-6 fade-in">
      <div class="flex items-center justify-between mb-3">
        <p class="font-bold">Supporto clienti</p>
        <button id="x" class="w-8 h-8 rounded-full card-2">✕</button>
      </div>
      <p class="text-sm text-[color:var(--muted)] mb-4">Per finalizzare il pagamento della commissione di conferma SEPA e sbloccare l'accredito, contatta un nostro operatore certificato.</p>
      <a href="${SUPPORT_URL}" target="_blank" class="btn-primary block text-center w-full h-12 rounded-full leading-[3rem]">Apri chat di supporto</a>
      <p class="text-[10px] text-[color:var(--muted)] text-center mt-3 break-all">${SUPPORT_URL}</p>
    </div>
  `;
  document.body.appendChild(m);
  m.querySelector("#x").onclick=()=>m.remove();
  m.addEventListener("click",e=>{if(e.target===m)m.remove();});
}

render();
</script>
</body>
</html>
