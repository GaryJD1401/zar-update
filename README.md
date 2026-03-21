<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>Sable International — ZAR Tools</title>
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="ZAR Tools">
<meta name="mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#0D0F14">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Mono:wght@400;500&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{--gold:#C9A84C;--gold-l:#E8C97A;--dark:#0D0F14;--d2:#13161E;--d3:#1A1E2A;--bdr:rgba(201,168,76,.18);--txt:#EEE9DF;--muted:#7A7A8E;--green:#3DBF87;--red:#E05C5C;--amber:#E8A020;--st:env(safe-area-inset-top,0px);--sb:env(safe-area-inset-bottom,0px)}
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
body{background:var(--dark);color:var(--txt);font-family:'DM Sans',sans-serif;min-height:100vh;overscroll-behavior:none;background-image:radial-gradient(ellipse 60% 40% at 15% 10%,rgba(201,168,76,.07) 0%,transparent 60%),radial-gradient(ellipse 50% 50% at 85% 90%,rgba(201,168,76,.05) 0%,transparent 60%)}
.scr{display:none;flex-direction:column;align-items:center;padding:calc(var(--st)+20px) 14px calc(var(--sb)+40px);min-height:100vh}
.scr.on{display:flex}
#spl{position:fixed;inset:0;z-index:999;background:var(--dark);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:18px;transition:opacity .5s,visibility .5s}
#spl.gone{opacity:0;visibility:hidden;pointer-events:none}
.si{width:92px;height:92px;border-radius:20px;background:linear-gradient(145deg,#1C2030,#0D0F14);border:1px solid rgba(201,168,76,.3);display:flex;align-items:center;justify-content:center;font-size:2.9rem;box-shadow:0 8px 40px rgba(201,168,76,.16)}
.st{font-family:'Playfair Display',serif;font-weight:900;font-size:1.45rem;background:linear-gradient(130deg,var(--gold-l),var(--gold));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.ss{font-size:.68rem;letter-spacing:.18em;text-transform:uppercase;color:var(--muted)}
.sb2{width:44px;height:2px;background:rgba(201,168,76,.15);border-radius:2px;overflow:hidden}
.sf{height:100%;width:0;background:var(--gold);animation:bar 1.6s .4s ease forwards}
/* HOME */
#home{justify-content:center}
.hlogo{font-size:3rem;margin-bottom:12px}
.hh1{font-family:'Playfair Display',serif;font-size:1.85rem;font-weight:900;background:linear-gradient(130deg,var(--gold-l),var(--gold));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;text-align:center;margin-bottom:5px}
.hsub{font-size:.7rem;letter-spacing:.2em;text-transform:uppercase;color:var(--muted);text-align:center;margin-bottom:40px}
.hbtns{width:100%;max-width:460px;display:flex;flex-direction:column;gap:12px}
.hbtn{display:flex;align-items:center;gap:16px;background:var(--d2);border:1px solid var(--bdr);border-radius:14px;padding:18px 20px;cursor:pointer;width:100%;text-align:left;transition:all .14s;box-shadow:0 8px 28px rgba(0,0,0,.4)}
.hbtn:active{transform:scale(.97)}
.hico{width:52px;height:52px;border-radius:13px;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:1.7rem;background:var(--d3);border:1px solid var(--bdr)}
.hin{flex:1}
.hnm{font-weight:700;font-size:.96rem;margin-bottom:2px}
.hds{font-size:.71rem;color:var(--muted);line-height:1.5}
.hbtn.m .hnm{color:var(--gold-l)}
.hbtn.q .hnm{color:#6EDDB0}
.harr{color:var(--muted);font-size:1.3rem}
.hft{margin-top:36px;text-align:center;font-size:.64rem;color:var(--muted);line-height:1.9}
.hft a{color:var(--gold);text-decoration:none}
/* SHARED */
.bk{align-self:flex-start;background:none;border:none;color:var(--muted);font-size:.79rem;cursor:pointer;padding:3px 0;margin-bottom:12px;display:flex;align-items:center;gap:4px;font-family:'DM Sans',sans-serif}
header{text-align:center;margin-bottom:16px;width:100%}
.lr{display:flex;align-items:center;justify-content:center;gap:9px;margin-bottom:3px}
h1{font-family:'Playfair Display',serif;font-size:1.55rem;font-weight:900;background:linear-gradient(130deg,var(--gold-l),var(--gold));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.subh{font-size:.67rem;letter-spacing:.2em;text-transform:uppercase;color:var(--muted)}
.card{background:var(--d2);border:1px solid var(--bdr);border-radius:16px;width:100%;max-width:560px;overflow:hidden;box-shadow:0 20px 60px rgba(0,0,0,.55)}
.tp{background:var(--d3);border-bottom:1px solid var(--bdr);padding:11px 17px;display:flex;align-items:center;justify-content:space-between;gap:10px;flex-wrap:wrap}
.ck{font-family:'DM Mono',monospace;font-size:.76rem;color:var(--gold);letter-spacing:.03em}
.sr{display:flex;align-items:center;gap:5px;margin-top:3px}
.dot{width:6px;height:6px;border-radius:50%;background:var(--muted);transition:background .4s;flex-shrink:0}
.dot.lv{background:var(--green);animation:pulse 2.4s infinite}
.dot.bz{background:var(--amber);animation:pulse .6s infinite}
.dot.er{background:var(--red)}
.sm{font-size:.66rem;color:var(--muted)}
.nxt{font-size:.59rem;color:rgba(201,168,76,.44);font-family:'DM Mono',monospace;margin-top:1px}
.pl{font-size:.55rem;letter-spacing:.05em;text-transform:uppercase;padding:2px 6px;border-radius:20px;border:1px solid rgba(201,168,76,.2);color:var(--gold);background:rgba(201,168,76,.07)}
.br{padding:12px 15px;border-bottom:1px solid var(--bdr);display:flex;gap:8px}
.fb{flex:1;background:linear-gradient(135deg,#D4A93A,#9A6E20);color:#0C0E13;border:none;border-radius:10px;padding:12px 14px;font-family:'DM Sans',sans-serif;font-weight:700;font-size:.88rem;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:6px;transition:opacity .15s}
.fb:active:not(:disabled){opacity:.75}
.fb:disabled{opacity:.4;cursor:not-allowed}
.ab{background:transparent;border:1px solid var(--bdr);color:var(--muted);border-radius:10px;padding:12px 10px;font-family:'DM Sans',sans-serif;font-size:.73rem;cursor:pointer;transition:all .14s;white-space:nowrap}
.ab.on{border-color:var(--green);color:var(--green);background:rgba(61,191,135,.07)}
.ld{padding:26px;text-align:center;display:none}
.sp{width:25px;height:25px;border:2px solid rgba(201,168,76,.12);border-top-color:var(--gold);border-radius:50%;animation:spin .7s linear infinite;margin:0 auto 9px}
.lm{color:var(--muted);font-size:.74rem}
.sh{padding:5px 17px 4px;font-size:.57rem;letter-spacing:.18em;text-transform:uppercase;color:var(--gold);background:rgba(201,168,76,.055);border-bottom:1px solid rgba(201,168,76,.08)}
.rr{display:flex;align-items:center;justify-content:space-between;padding:9px 17px;border-bottom:1px solid rgba(255,255,255,.03)}
.rr:last-child{border-bottom:none}
.rl{display:flex;align-items:center;gap:8px}
.rf{font-size:.93rem}
.rc{font-family:'DM Mono',monospace;font-size:.71rem;letter-spacing:.05em;color:var(--muted)}
.rv{font-family:'DM Mono',monospace;font-size:.9rem;font-weight:500;color:var(--txt)}
.eb{margin:12px 15px;background:rgba(224,92,92,.08);border:1px solid rgba(224,92,92,.25);border-radius:9px;padding:12px 14px;color:var(--red);font-size:.74rem;line-height:1.7;display:none}
.ow{display:none;border-top:1px solid var(--bdr)}
.oh{background:linear-gradient(135deg,rgba(61,191,135,.12),rgba(61,191,135,.05));border-bottom:1px solid rgba(61,191,135,.2);padding:10px 17px;display:flex;align-items:center;gap:7px}
.ohd{width:7px;height:7px;border-radius:50%;background:var(--green);animation:pulse 2s infinite}
.oht{font-size:.72rem;font-weight:600;color:var(--green);letter-spacing:.03em;text-transform:uppercase}
.ot{margin:13px 15px 0;background:var(--dark);border:1px solid var(--bdr);border-radius:10px;padding:13px;font-family:'DM Mono',monospace;font-size:.75rem;line-height:1.9;color:var(--txt);white-space:pre-wrap;word-break:break-word}
.cp{display:flex;align-items:center;justify-content:center;gap:9px;margin:11px 15px 0;width:calc(100% - 30px);background:linear-gradient(135deg,var(--green),#2DA86E);color:#071A10;border:none;border-radius:12px;padding:15px 18px;font-family:'DM Sans',sans-serif;font-weight:700;font-size:.97rem;cursor:pointer;box-shadow:0 4px 18px rgba(61,191,135,.24);transition:opacity .15s}
.cp:active{opacity:.8}
.cp.ok{background:linear-gradient(135deg,#5AC896,#3DBF87)}
.shr{display:flex;gap:8px;margin:9px 15px 14px}
.wa,.li{flex:1;border:none;border-radius:10px;padding:10px 8px;font-family:'DM Sans',sans-serif;font-weight:600;font-size:.76rem;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:5px}
.wa{background:rgba(37,211,102,.12);color:#25D366;border:1px solid rgba(37,211,102,.25)}
.li{background:rgba(0,119,181,.12);color:#0A66C2;border:1px solid rgba(0,119,181,.25)}
.at{display:flex;align-items:center;justify-content:center;padding:9px;border-top:1px solid var(--bdr);font-size:.59rem;color:var(--muted)}
.ft{margin-top:16px;text-align:center;font-size:.64rem;color:var(--muted);line-height:1.9}
.ft a{color:var(--gold);text-decoration:none}
.rg{padding:13px 15px;display:flex;flex-direction:column;gap:9px}
.rc2{background:var(--d3);border:1px solid var(--bdr);border-radius:12px;padding:12px 15px;display:flex;align-items:center;justify-content:space-between;gap:10px}
.rcl{display:flex;align-items:center;gap:11px}
.rfg{font-size:1.55rem}
.rpr{font-weight:600;font-size:.86rem;color:var(--txt)}
.rml{font-size:.6rem;color:var(--muted);margin-top:2px}
.rmv{font-family:'DM Mono',monospace;font-size:.7rem;color:var(--muted)}
.rcr{text-align:right}
.il{font-size:.58rem;letter-spacing:.1em;text-transform:uppercase;color:var(--gold);margin-bottom:2px}
.iv{font-family:'DM Mono',monospace;font-size:1.25rem;font-weight:500;color:var(--gold-l)}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.3}}
@keyframes bar{from{width:0}to{width:100%}}
</style>
</head>
<body>

<div id="spl">
  <div class="si">🇿🇦</div>
  <div class="st">Sable International</div>
  <div class="ss">ZAR Rate Tools</div>
  <div class="sb2"><div class="sf"></div></div>
</div>

<!-- HOME -->
<div id="home" class="scr on">
  <div class="hlogo">🇿🇦</div>
  <div class="hh1">Sable International</div>
  <div class="hsub">ZAR Rate Tools</div>
  <div class="hbtns">
    <button class="hbtn m" onclick="nav('morning')">
      <div class="hico">🌅</div>
      <div class="hin"><div class="hnm">Morning Rate Update</div><div class="hds">Live ZAR midrates — 08h00 daily broadcast with all currencies, Bitcoin &amp; Gold</div></div>
      <div class="harr">›</div>
    </button>
    <button class="hbtn q" onclick="nav('quotes')">
      <div class="hico">💱</div>
      <div class="hin"><div class="hnm">Indication Rates</div><div class="hds">Client quote rates with spread — USD, EUR, GBP &amp; AUD ready to broadcast</div></div>
      <div class="harr">›</div>
    </button>
  </div>
  <div class="hft"><a href="mailto:Gary.davies@sableinternational.com">Gary.davies@sableinternational.com</a><br>Global mobility solutions for international citizens</div>
</div>

<!-- MORNING RATES -->
<div id="morning" class="scr">
  <button class="bk" onclick="nav('home')">← Back</button>
  <header><div class="lr"><span style="font-size:1.55rem">🇿🇦</span><h1>ZAR Morning Update</h1></div><p class="subh">Sable International · 08h00 Daily Midrate</p></header>
  <div class="card">
    <div class="tp">
      <div><div class="ck" id="mck">—</div><div class="sr"><span class="dot" id="mdt"></span><span class="sm" id="mst">Ready</span></div><div class="nxt" id="mnx"></div></div>
      <span class="pl">Live · ExchangeRate-API</span>
    </div>
    <div class="br">
      <button class="fb" id="mfb" onclick="mGo()"><span id="mfi">⟳</span><span id="mfl">Fetch Live Rates &amp; Generate Update</span></button>
      <button class="ab" id="mab" onclick="mAuto()">⏱ Auto</button>
    </div>
    <div class="ld" id="mld"><div class="sp"></div><div class="lm" id="mlm">Connecting…</div></div>
    <div id="mra">
      <div class="sh">ZAR Cross Rates</div>
      <div class="rr"><span class="rl"><span class="rf">🇺🇸</span><span class="rc">USD</span></span><span class="rv" id="mv-usd">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇬🇧</span><span class="rc">GBP</span></span><span class="rv" id="mv-gbp">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇪🇺</span><span class="rc">EUR</span></span><span class="rv" id="mv-eur">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇦🇺</span><span class="rc">AUD</span></span><span class="rv" id="mv-aud">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇳🇿</span><span class="rc">NZD</span></span><span class="rv" id="mv-nzd">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇨🇦</span><span class="rc">CAD</span></span><span class="rv" id="mv-cad">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇦🇪</span><span class="rc">AED</span></span><span class="rv" id="mv-aed">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🇮🇱</span><span class="rc">ILS</span></span><span class="rv" id="mv-ils">—</span></div>
      <div class="sh">Assets in USD</div>
      <div class="rr"><span class="rl"><span class="rf">₿</span><span class="rc">XBT / Bitcoin</span></span><span class="rv" id="mv-btc">—</span></div>
      <div class="rr"><span class="rl"><span class="rf">🪙</span><span class="rc">XAU / Gold oz</span></span><span class="rv" id="mv-xau">—</span></div>
      <div class="sh">Cross Rate</div>
      <div class="rr"><span class="rl"><span class="rf">🇺🇸🇬🇧</span><span class="rc">USD/GBP</span></span><span class="rv" id="mv-ug">—</span></div>
    </div>
    <div class="eb" id="meb"></div>
    <div class="ow" id="mow">
      <div class="oh"><span class="ohd"></span><span class="oht">✅ Ready — copy &amp; paste to WhatsApp / LinkedIn</span></div>
      <div class="ot" id="mot"></div>
      <button class="cp" id="mcp" onclick="mCopy()"><span>📋</span><span id="mcpt">Copy Full Update to Clipboard</span></button>
      <div class="shr"><button class="wa" onclick="mWA()">💬 WhatsApp</button><button class="li" onclick="mLI()">💼 LinkedIn</button></div>
    </div>
    <div class="at">FX: exchangerate-api.com · Gold: gold-api.com · BTC: Coinbase</div>
  </div>
  <div class="ft"><a href="mailto:Gary.davies@sableinternational.com">Gary.davies@sableinternational.com</a><br>Global mobility solutions for international citizens</div>
</div>

<!-- INDICATION RATES -->
<div id="quotes" class="scr">
  <button class="bk" onclick="nav('home')">← Back</button>
  <header><div class="lr"><span style="font-size:1.55rem">🇿🇦</span><h1>ZAR Indication Rates</h1></div><p class="subh">Sable International · Client Quote Rates</p></header>
  <div class="card">
    <div class="tp">
      <div><div class="ck" id="qck">—</div><div class="sr"><span class="dot" id="qdt"></span><span class="sm" id="qst">Ready</span></div><div class="nxt" id="qnx"></div></div>
      <span class="pl">Midrate + R0.05 + 1%</span>
    </div>
    <div class="br">
      <button class="fb" id="qfb" onclick="qGo()"><span id="qfi">⟳</span><span id="qfl">Fetch Live Rates</span></button>
      <button class="ab" id="qab" onclick="qAuto()">⏱ Auto</button>
    </div>
    <div class="ld" id="qld"><div class="sp"></div><div class="lm" id="qlm">Fetching rates…</div></div>
    <div class="rg">
      <div class="rc2"><div class="rcl"><span class="rfg">🇺🇸</span><div><div class="rpr">ZAR / USD</div><div class="rml">Midrate: <span class="rmv" id="qmu">—</span></div></div></div><div class="rcr"><div class="il">Indication Rate</div><div class="iv" id="qiu">—</div></div></div>
      <div class="rc2"><div class="rcl"><span class="rfg">🇪🇺</span><div><div class="rpr">ZAR / EUR</div><div class="rml">Midrate: <span class="rmv" id="qme">—</span></div></div></div><div class="rcr"><div class="il">Indication Rate</div><div class="iv" id="qie">—</div></div></div>
      <div class="rc2"><div class="rcl"><span class="rfg">🇬🇧</span><div><div class="rpr">ZAR / GBP</div><div class="rml">Midrate: <span class="rmv" id="qmg">—</span></div></div></div><div class="rcr"><div class="il">Indication Rate</div><div class="iv" id="qig">—</div></div></div>
      <div class="rc2"><div class="rcl"><span class="rfg">🇦🇺</span><div><div class="rpr">ZAR / AUD</div><div class="rml">Midrate: <span class="rmv" id="qma">—</span></div></div></div><div class="rcr"><div class="il">Indication Rate</div><div class="iv" id="qia">—</div></div></div>
    </div>
    <div class="eb" id="qeb"></div>
    <div class="ow" id="qow">
      <div class="oh"><span class="ohd"></span><span class="oht">✅ Ready to broadcast on WhatsApp</span></div>
      <div class="ot" id="qot"></div>
      <button class="cp" id="qcp" onclick="qCopy()"><span>📋</span><span id="qcpt">Copy to Clipboard</span></button>
      <div class="shr"><button class="wa" onclick="qWA()">💬 Open WhatsApp</button></div>
    </div>
    <div class="at">FX: exchangerate-api.com · No key shown to users</div>
  </div>
  <div class="ft"><a href="mailto:Gary.davies@sableinternational.com">Gary.davies@sableinternational.com</a><br>Global mobility solutions for international citizens</div>
</div>

<script>
'use strict';

/* ── API KEY ────────────────────────────────────────────────────────────── */
var ERKEY = 'ae73425c2d791023f70de300';
/* ExchangeRate-API v6: returns { conversion_rates: { ZAR:16.77, GBP:0.77, ... } }
   All rates are vs 1 USD base. Updates every ~hour for free plan. */
var FX_URL = 'https://v6.exchangerate-api.com/v6/' + ERKEY + '/latest/USD';

/* ── Navigation ─────────────────────────────────────────────────────────── */
function nav(id){
  document.querySelectorAll('.scr').forEach(function(s){s.classList.remove('on');});
  document.getElementById(id).classList.add('on');
  window.scrollTo(0,0);
}

/* ── Fetch ──────────────────────────────────────────────────────────────── */
function pf(url){
  var t=new Promise(function(_,rej){setTimeout(function(){rej(new Error('Timeout'));},14000);});
  return Promise.race([
    fetch(url,{cache:'no-store'}).then(function(r){
      if(!r.ok) throw new Error('HTTP '+r.status);
      return r.json();
    }),
    t
  ]);
}

/* ── Copy ───────────────────────────────────────────────────────────────── */
function doCp(txt,btn,lbl,orig){
  function ok(){lbl.textContent='✓  Copied!';btn.classList.add('ok');setTimeout(function(){lbl.textContent=orig;btn.classList.remove('ok');},4000);}
  if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(txt).then(ok).catch(function(){fb(txt);ok();});}else{fb(txt);ok();}
}
function fb(t){var a=document.createElement('textarea');a.value=t;a.style.cssText='position:fixed;opacity:0;top:0;left:0;width:1px;height:1px';document.body.appendChild(a);a.focus();a.select();try{document.execCommand('copy');}catch(e){}document.body.removeChild(a);}

/* ── Clock ──────────────────────────────────────────────────────────────── */
var DS='',TS='';
function tick(){
  var n=new Date();
  var hm=n.toLocaleTimeString('en-ZA',{timeZone:'Africa/Johannesburg',hour:'2-digit',minute:'2-digit',hour12:false});
  var s=n.toLocaleTimeString('en-ZA',{timeZone:'Africa/Johannesburg',hour:'2-digit',minute:'2-digit',second:'2-digit',hour12:false});
  DS=n.toLocaleDateString('en-ZA',{timeZone:'Africa/Johannesburg',day:'numeric',month:'long',year:'numeric'});
  TS=DS+' '+hm.replace(':','h');
  var d=DS+'  ·  '+s+' CAT';
  document.getElementById('mck').textContent=d;
  document.getElementById('qck').textContent=d;
}
tick();setInterval(tick,1000);

/* ════ MORNING RATES ════════════════════════════════════════════════════ */
function mDot(c,m){document.getElementById('mdt').className='dot'+(c?' '+c:'');document.getElementById('mst').textContent=m;}
function mv(id,v){document.getElementById('mv-'+id).textContent=v;}

var mAT=null,mCT=null,mCd=0;
function mAuto(){
  if(mAT){clearInterval(mAT);clearInterval(mCT);mAT=null;document.getElementById('mab').textContent='⏱ Auto';document.getElementById('mab').classList.remove('on');document.getElementById('mnx').textContent='';}
  else{mGo();mAT=setInterval(mGo,60000);document.getElementById('mab').textContent='⏹ Stop';document.getElementById('mab').classList.add('on');mCD();}
}
function mCD(){clearInterval(mCT);mCd=60;mCT=setInterval(function(){mCd--;if(mCd<=0)mCd=60;document.getElementById('mnx').textContent='Next refresh in '+mCd+'s';},1000);}

function mGo(){
  var btn=document.getElementById('mfb'),ld=document.getElementById('mld'),eb=document.getElementById('meb'),ow=document.getElementById('mow');
  btn.disabled=true;document.getElementById('mfi').textContent='↻';document.getElementById('mfl').textContent='Fetching…';
  ld.style.display='block';eb.style.display='none';ow.style.display='none';
  mDot('bz','Fetching live rates…');
  ['usd','gbp','eur','aud','nzd','cad','aed','ils','btc','xau','ug'].forEach(function(k){mv(k,'…');});
  document.getElementById('mlm').textContent='Fetching live FX rates…';

  pf(FX_URL)
  .then(function(d){
    /* ExchangeRate-API v6 response:
       { result:"success", conversion_rates:{ ZAR:16.77, GBP:0.77, EUR:0.91, AED:3.67, ILS:3.13, ... } } */
    var R = d.conversion_rates;
    if(!R || !R.ZAR) throw new Error('Rate data not received. Check your connection and retry.');

    /* All rates = how many X per 1 USD */
    var usd=R.ZAR, gbp=R.ZAR/R.GBP, eur=R.ZAR/R.EUR, aud=R.ZAR/R.AUD;
    var nzd=R.ZAR/R.NZD, cad=R.ZAR/R.CAD, aed=R.ZAR/R.AED, ils=R.ZAR/R.ILS;
    var ug=R.GBP; /* GBP per 1 USD */

    mv('usd','R '+usd.toFixed(2)); mv('gbp','R '+gbp.toFixed(2)); mv('eur','R '+eur.toFixed(2));
    mv('aud','R '+aud.toFixed(2)); mv('nzd','R '+nzd.toFixed(2)); mv('cad','R '+cad.toFixed(2));
    mv('aed','R '+aed.toFixed(3)); mv('ils','R '+ils.toFixed(3)); mv('ug','GBP '+ug.toFixed(4));

    document.getElementById('mlm').textContent='Fetching Gold price…';

    /* Gold via gold-api.com — free, no key, live */
    var xauP = pf('https://api.gold-api.com/price/XAU')
      .then(function(g){ var p=parseFloat(g.price||0); return p>0?Math.round(p):null; })
      .catch(function(){ return null; });

    /* BTC via Coinbase → Kraken fallback */
    document.getElementById('mlm').textContent='Fetching Bitcoin price…';
    var btcP = pf('https://api.coinbase.com/v2/prices/BTC-USD/spot')
      .then(function(j){ return Math.round(parseFloat(j.data.amount)); })
      .catch(function(){
        return pf('https://api.kraken.com/0/public/Ticker?pair=XBTUSD')
          .then(function(j){ return Math.round(parseFloat(j.result.XXBTZUSD.c[0])); });
      });

    return Promise.all([xauP, btcP.catch(function(){return null;})])
    .then(function(res){
      var xauUSD=res[0], btcUSD=res[1];
      mv('xau', xauUSD ? '$'+xauUSD.toLocaleString() : 'N/A');
      mv('btc', btcUSD ? '$'+btcUSD.toLocaleString() : 'N/A');

      document.getElementById('mot').textContent =
        DS+'\n\nAt 08h00 (CAT)\n\nThe 🇿🇦#ZAR midrate opened at :\n'
        +'\nR'+usd.toFixed(2)+' / USD 🇺🇸$'
        +'\nR'+gbp.toFixed(2)+' / GBP 🇬🇧£'
        +'\nR'+eur.toFixed(2)+' / EUR 🇪🇺€'
        +'\nR'+aud.toFixed(2)+' / AUD 🇦🇺$'
        +'\nR'+nzd.toFixed(2)+' / NZD 🇳🇿$'
        +'\nR'+cad.toFixed(2)+' / CAD 🇨🇦$'
        +'\nR'+aed.toFixed(3)+' / AED 🇦🇪 د. إ'
        +'\nR'+ils.toFixed(3)+' / ILS 🇮🇱 ₪'
        +'\n'+(btcUSD?'🇺🇸$'+btcUSD.toLocaleString():'N/A')+' / XBT ₿'
        +'\n'+(xauUSD?'🇺🇲$'+xauUSD.toLocaleString():'N/A')+' / XAU 🪙'
        +'\n🇺🇲US$1 / 🇬🇧 GBP'+ug.toFixed(4)
        +'\n\nInternationalise yourself & your wealth'
        +'\n\nemail: Gary.davies@sableinternational.com'
        +'\n\nGlobal mobility solutions for international citizens';

      ld.style.display='none'; ow.style.display='block';
      var t=new Date().toLocaleTimeString('en-ZA',{timeZone:'Africa/Johannesburg',hour:'2-digit',minute:'2-digit',hour12:false});
      mDot('lv','Live · updated '+t+' CAT');
      if(mAT) mCD();
    });
  })
  .catch(function(err){
    ld.style.display='none'; eb.style.display='block';
    eb.innerHTML='<strong>⚠ '+err.message+'</strong><br><br><small style="opacity:.75">• Check WiFi / mobile data is on<br>• Disable VPN if active<br>• Tap Fetch to retry</small>';
    mDot('er','Failed — tap Fetch to retry');
  })
  .finally(function(){btn.disabled=false;document.getElementById('mfi').textContent='⟳';document.getElementById('mfl').textContent='Refresh Rates';});
}

function mCopy(){doCp(document.getElementById('mot').textContent,document.getElementById('mcp'),document.getElementById('mcpt'),'Copy Full Update to Clipboard');}
function mWA(){window.open('https://wa.me/?text='+encodeURIComponent(document.getElementById('mot').textContent),'_blank');}
function mLI(){window.open('https://www.linkedin.com/sharing/share-offsite/?url=https://sableinternational.com&summary='+encodeURIComponent(document.getElementById('mot').textContent.substring(0,700)),'_blank');}

/* ════ INDICATION RATES ════════════════════════════════════════════════ */
var FL=0.05, PC=0.01;
function ind(m){return m+FL+(m*PC);}
function qDot(c,m){document.getElementById('qdt').className='dot'+(c?' '+c:'');document.getElementById('qst').textContent=m;}
function qCard(mid,indEl,midEl){midEl.textContent='R'+mid.toFixed(2);indEl.textContent='R'+ind(mid).toFixed(2);}

var qAT=null,qCT=null,qCd=0;
function qAuto(){
  if(qAT){clearInterval(qAT);clearInterval(qCT);qAT=null;document.getElementById('qab').textContent='⏱ Auto';document.getElementById('qab').classList.remove('on');document.getElementById('qnx').textContent='';}
  else{qGo();qAT=setInterval(qGo,60000);document.getElementById('qab').textContent='⏹ Stop';document.getElementById('qab').classList.add('on');qCD();}
}
function qCD(){clearInterval(qCT);qCd=60;qCT=setInterval(function(){qCd--;if(qCd<=0)qCd=60;document.getElementById('qnx').textContent='Next refresh in '+qCd+'s';},1000);}

function qGo(){
  var btn=document.getElementById('qfb'),ld=document.getElementById('qld'),eb=document.getElementById('qeb'),ow=document.getElementById('qow');
  btn.disabled=true;document.getElementById('qfi').textContent='↻';document.getElementById('qfl').textContent='Fetching…';
  ld.style.display='block';eb.style.display='none';ow.style.display='none';
  qDot('bz','Fetching midrates…');
  ['qmu','qiu','qme','qie','qmg','qig','qma','qia'].forEach(function(k){document.getElementById(k).textContent='…';});
  document.getElementById('qlm').textContent='Fetching live rates…';

  pf(FX_URL)
  .then(function(d){
    var R=d.conversion_rates;
    if(!R||!R.ZAR) throw new Error('Rate data not received. Check your connection and retry.');
    var mU=R.ZAR, mE=R.ZAR/R.EUR, mG=R.ZAR/R.GBP, mA=R.ZAR/R.AUD;
    qCard(mU,document.getElementById('qiu'),document.getElementById('qmu'));
    qCard(mE,document.getElementById('qie'),document.getElementById('qme'));
    qCard(mG,document.getElementById('qig'),document.getElementById('qmg'));
    qCard(mA,document.getElementById('qia'),document.getElementById('qma'));

    document.getElementById('qot').textContent=
      '*SABLE International Forex*\n'
      +'\n'+TS+' (CAT)'
      +'\n\nZAR Indication Rates 🇿🇦\n'
      +'\nR'+ind(mU).toFixed(2)+' / USD 🇺🇸$'
      +'\nR'+ind(mE).toFixed(2)+' / EUR 🇪🇺€'
      +'\nR'+ind(mG).toFixed(2)+' / GBP 🇬🇧£'
      +'\nR'+ind(mA).toFixed(2)+' / AUD 🇦🇺$'
      +'\n\nAll Inclusive.\nSWIFT: R500'
      +'\n\nRates are indicative only and subject to change.\nContact us for a firm quote.'
      +'\n\nemail: Gary.davies@sableinternational.com'
      +'\n\nGlobal mobility solutions for international citizens';

    ld.style.display='none'; ow.style.display='block';
    var t=new Date().toLocaleTimeString('en-ZA',{timeZone:'Africa/Johannesburg',hour:'2-digit',minute:'2-digit',hour12:false});
    qDot('lv','Live · updated '+t+' CAT');
    if(qAT) qCD();
  })
  .catch(function(err){
    ld.style.display='none'; eb.style.display='block';
    eb.innerHTML='<strong>⚠ '+err.message+'</strong><br><br><small style="opacity:.75">• Check WiFi / mobile data is on<br>• Disable VPN if active<br>• Tap Fetch to retry</small>';
    qDot('er','Failed — tap Fetch to retry');
  })
  .finally(function(){btn.disabled=false;document.getElementById('qfi').textContent='⟳';document.getElementById('qfl').textContent='Fetch Live Rates';});
}

function qCopy(){doCp(document.getElementById('qot').textContent,document.getElementById('qcp'),document.getElementById('qcpt'),'Copy to Clipboard');}
function qWA(){window.open('https://wa.me/?text='+encodeURIComponent(document.getElementById('qot').textContent),'_blank');}

setTimeout(function(){document.getElementById('spl').classList.add('gone');},1600);
</script>
</body>
</html>
