<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Tug‘ilgan kuningiz muborak, Dadajon! 🎂</title>
<style>
:root{--gold:#ffd86b;--gold2:#ffb52e;--pink:#ff5fa2;--violet:#7b4dff;--bg1:#1a0b3d;--bg2:#4a1670;--bg3:#8a1f6b;--ink:#fff}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
html,body{height:100%}
body{font-family:"Segoe UI",system-ui,-apple-system,Roboto,sans-serif;color:var(--ink);overflow-x:hidden;
 background:radial-gradient(circle at 20% 10%,var(--bg3),transparent 50%),radial-gradient(circle at 85% 80%,#2b3cc4,transparent 55%),linear-gradient(160deg,var(--bg1),var(--bg2));
 background-attachment:fixed;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
#fx{position:fixed;inset:0;width:100%;height:100%;pointer-events:none;z-index:50}
.screen{position:fixed;inset:0;overflow-y:auto;overflow-x:hidden;display:flex;flex-direction:column;align-items:center;transition:opacity .8s,transform .8s}
.screen.hide{opacity:0;transform:scale(1.05);pointer-events:none}
#intro{justify-content:center;text-align:center;padding:20px}
#main{padding:30px 16px 90px;opacity:0;pointer-events:none}
#main.show{opacity:1;pointer-events:auto}
.hint{margin-top:2.2em;font-size:1.05rem;color:var(--gold);letter-spacing:.05em;animation:pulse 1.6s infinite}
@keyframes pulse{50%{opacity:.4;transform:scale(.96)}}
.glow-bg{position:absolute;width:60vmin;height:60vmin;border-radius:50%;background:radial-gradient(circle,rgba(255,216,107,.45),transparent 65%);animation:breathe 4s ease-in-out infinite;z-index:0}
@keyframes breathe{50%{transform:scale(1.25);opacity:.6}}

/* GIFT */
.gift{position:relative;width:10em;height:10.5em;cursor:pointer;z-index:2;font-size:var(--fs,18px);animation:bounce 2s ease-in-out infinite;transform-origin:50% 100%}
@keyframes bounce{0%,100%{transform:translateY(0) rotate(0)}15%{transform:translateY(-.8em) rotate(-3deg)}30%{transform:translateY(0) rotate(3deg)}45%{transform:translateY(-.4em) rotate(-2deg)}60%{transform:translateY(0) rotate(0)}}
.gift.opened,.gift.opening{animation:none}
.gift .base,.gift .lid{position:absolute;border-radius:.4em;background:linear-gradient(135deg,var(--pink),#c22a86);box-shadow:0 0 1.5em rgba(255,95,162,.55),inset 0 -.5em 0 rgba(0,0,0,.15)}
.gift .base{left:.6em;bottom:0;width:8.8em;height:6.6em}
.gift .lid{left:0;top:1.9em;width:10em;height:2.2em;transform-origin:0 100%;transition:transform .9s cubic-bezier(.3,1.6,.5,1);z-index:3;background:linear-gradient(135deg,#ff7ab5,#d4339a)}
.gift .rib{position:absolute;left:50%;width:1.7em;margin-left:-.85em;background:linear-gradient(90deg,var(--gold2),var(--gold),var(--gold2))}
.gift .base .rib{top:0;bottom:0}
.gift .lid .rib{top:0;bottom:0}
.gift .bow{position:absolute;left:50%;top:-1.2em;width:1px;height:1px}
.gift .bow i{position:absolute;width:2.2em;height:1.7em;border:.5em solid var(--gold);border-radius:50% 50% 50% 0;top:-.6em}
.gift .bow i:first-child{left:-2.1em;transform:rotate(-20deg)}
.gift .bow i:last-child{left:-.1em;transform:scaleX(-1) rotate(-20deg)}
.gift .bow b{position:absolute;left:-.5em;top:-.1em;width:1em;height:1em;border-radius:50%;background:var(--gold2)}
.gift.opened .lid,.gift.opening .lid{transform:translate(-1.5em,-3.5em) rotate(-40deg)}
.gift .inner{position:absolute;left:1em;top:3.6em;width:8em;height:3em;background:radial-gradient(ellipse,#fff7c2,var(--gold) 50%,transparent 75%);opacity:0;filter:blur(.3em);transition:opacity .5s}
.gift.opened .inner,.gift.opening .inner{opacity:1}
.gift:hover{filter:brightness(1.12)}
.gift:active{transform:scale(.95)}
.g2 .base,.g2 .lid{background:linear-gradient(135deg,#5b8bff,#3a3fd6);box-shadow:0 0 1.5em rgba(91,139,255,.6),inset 0 -.5em 0 rgba(0,0,0,.15)}
.g2 .lid{background:linear-gradient(135deg,#7aa2ff,#4d52e6)}
.g3 .base,.g3 .lid{background:linear-gradient(135deg,#27d6a0,#0f9a8a);box-shadow:0 0 1.5em rgba(39,214,160,.55),inset 0 -.5em 0 rgba(0,0,0,.15)}
.g3 .lid{background:linear-gradient(135deg,#4ee8b7,#14ad98)}

/* MESSAGES */
.greet{position:relative;z-index:2;margin-top:1.2em;max-width:620px;font-size:clamp(1.5rem,5.5vw,2.4rem);font-weight:800;line-height:1.3;opacity:0;transform:translateY(30px) scale(.9);
 background:linear-gradient(90deg,#fff,var(--gold),#fff);background-size:200%;-webkit-background-clip:text;background-clip:text;color:transparent;filter:drop-shadow(0 0 12px rgba(255,216,107,.5))}
.greet.in{animation:rise 1s forwards,shine 3s linear infinite}
@keyframes rise{to{opacity:1;transform:none}}
@keyframes shine{to{background-position:200%}}
.btn{margin-top:1.6em;padding:.9em 2.2em;border:0;border-radius:999px;font-size:1.1rem;font-weight:700;color:#3a1a00;cursor:pointer;
 background:linear-gradient(135deg,var(--gold),var(--gold2));box-shadow:0 0 25px rgba(255,200,70,.6);transition:transform .25s,box-shadow .25s;opacity:0;pointer-events:none;position:relative;z-index:2}
.btn.in{animation:rise .8s .6s forwards;pointer-events:auto}
.btn:hover{transform:scale(1.08) translateY(-2px);box-shadow:0 0 40px rgba(255,200,70,.95)}

/* MAIN */
h1{font-size:clamp(1.9rem,7vw,3.6rem);text-align:center;line-height:1.2;font-weight:900;max-width:900px;position:relative;z-index:2;
 background:linear-gradient(90deg,#fff3b8,var(--gold2),#fff3b8,var(--pink));background-size:300%;-webkit-background-clip:text;background-clip:text;color:transparent;animation:shine 6s linear infinite;filter:drop-shadow(0 0 16px rgba(255,190,60,.55))}
.sub{margin-top:.6em;color:var(--gold);letter-spacing:.2em;font-size:.85rem;text-transform:uppercase;z-index:2;text-align:center}
.cakewrap{position:relative;z-index:2;margin:34px 0 8px;display:flex;flex-direction:column;align-items:center;cursor:pointer}
.candles{display:flex;gap:14px;margin-bottom:-2px}
.candle{width:9px;height:34px;background:repeating-linear-gradient(45deg,#fff,#fff 5px,#ff8ab8 5px,#ff8ab8 10px);border-radius:3px;position:relative}
.flame{position:absolute;left:50%;top:-20px;width:12px;height:20px;margin-left:-6px;border-radius:50% 50% 50% 50%/65% 65% 35% 35%;
 background:radial-gradient(circle at 50% 70%,#fff,var(--gold) 50%,#ff7a18);box-shadow:0 0 18px 6px rgba(255,190,60,.7);animation:flick .3s infinite alternate;transition:opacity .5s}
@keyframes flick{from{transform:scale(1,1) rotate(-3deg)}to{transform:scale(.88,1.12) rotate(3deg)}}
.out .flame{opacity:0}
.tier{border-radius:14px 14px 6px 6px;position:relative}
.t1{width:120px;height:50px;background:linear-gradient(#ff9ec8,#e8478f)}
.t2{width:170px;height:58px;background:linear-gradient(#ffe0a3,#f5a742)}
.t3{width:220px;height:66px;background:linear-gradient(#b99bff,#7b4dff)}
.tier:before{content:"";position:absolute;left:0;right:0;top:0;height:14px;border-radius:14px 14px 40% 40%;background:#fff;opacity:.92}
.plate{width:260px;height:10px;border-radius:50%;background:var(--gold);box-shadow:0 0 25px var(--gold2)}
.wish{margin-top:12px;color:#ffd0e4;font-size:1rem;text-shadow:0 0 12px var(--pink)}
.card{position:relative;z-index:2;max-width:640px;width:100%;margin:26px auto 0;padding:30px 26px;border-radius:24px;
 background:linear-gradient(145deg,rgba(255,255,255,.16),rgba(255,255,255,.05));backdrop-filter:blur(12px);-webkit-backdrop-filter:blur(12px);
 border:1px solid rgba(255,216,107,.55);box-shadow:0 0 40px rgba(255,190,60,.25),0 20px 50px rgba(0,0,0,.35);transition:transform .4s}
.card:hover{transform:translateY(-6px) rotate(-.5deg)}
.card h2{color:var(--gold);font-size:1.5rem;margin-bottom:.6em}
.card p{line-height:1.75;font-size:1.05rem;margin-bottom:.8em;color:#fff4fb}
.card .sign{text-align:right;color:var(--gold);font-weight:700;font-size:1.15rem}
.gifts-title{position:relative;z-index:2;margin:40px 0 4px;font-size:1.3rem;color:var(--gold);text-align:center}
.row{position:relative;z-index:2;display:flex;justify-content:center;gap:clamp(4px,3vw,34px);width:100%;max-width:700px;margin-top:70px}
.slot{flex:1;display:flex;justify-content:center}
.row .gift{--fs:min(13px,2.8vw);animation-delay:var(--d)}
.reveal{position:relative;z-index:3;min-height:150px;width:min(92%,440px);margin-top:26px;display:flex;align-items:center;justify-content:center;text-align:center;
 padding:20px;border-radius:22px;font-size:1.35rem;font-weight:700;line-height:1.5;color:#fff;opacity:0;transform:scale(.3);
 background:linear-gradient(135deg,rgba(255,216,107,.3),rgba(255,95,162,.3));border:2px solid var(--gold);box-shadow:0 0 45px rgba(255,200,70,.65)}
.reveal.pop{animation:pop .9s cubic-bezier(.2,1.5,.4,1) forwards}
.reveal small{display:block;color:var(--gold);font-size:1rem;margin-bottom:.3em}
@keyframes pop{0%{opacity:0;transform:scale(.2) translateY(-90px)}100%{opacity:1;transform:none}}
.balloon{position:fixed;bottom:-140px;width:56px;height:70px;border-radius:50% 50% 48% 48%;z-index:1;opacity:.85;animation:float linear infinite}
.balloon:after{content:"";position:absolute;left:50%;top:100%;width:1px;height:60px;background:rgba(255,255,255,.5)}
@keyframes float{to{transform:translateY(-125vh) translateX(40px) rotate(8deg)}}
#music{position:fixed;right:14px;top:calc(14px + env(safe-area-inset-top,0px));z-index:60;width:48px;height:48px;border-radius:50%;border:1px solid var(--gold);
 background:rgba(30,10,60,.7);color:var(--gold);font-size:1.3rem;cursor:pointer;box-shadow:0 0 18px rgba(255,200,70,.5);transition:transform .25s}
#music:hover{transform:scale(1.12) rotate(10deg)}
#music.on{animation:pulse 1.5s infinite}
</style>
</head>
<body>
<canvas id="fx"></canvas>
<button id="music" title="Musiqa">🎵</button>

<!-- 1. KIRISH -->
<section id="intro" class="screen">
  <div class="glow-bg"></div>
  <div class="gift" id="bigGift" style="--fs:clamp(14px,4.5vw,24px)">
    <div class="base"><span class="rib"></span></div>
    <div class="inner"></div>
    <div class="lid"><span class="rib"></span><span class="bow"><i></i><i></i><b></b></span></div>
  </div>
  <p class="hint" id="hint">✨ Sovg‘ani bosing ✨</p>
  <div class="greet" id="greet">Salom dadajon! Sizni tug‘ilgan kuningiz bilan tabriklayman! 🎉🎂</div>
  <button class="btn" id="next">Keyingi →</button>
</section>

<!-- 2. ASOSIY -->
<section id="main" class="screen">
  <h1>🎉 Tug‘ilgan kuningiz muborak, Dadajon! 🎂</h1>
  <div class="sub">eng aziz insonimga</div>

  <div class="cakewrap" id="cake">
    <div class="candles"><div class="candle"><span class="flame"></span></div><div class="candle"><span class="flame" style="animation-delay:.1s"></span></div><div class="candle"><span class="flame" style="animation-delay:.2s"></span></div></div>
    <div class="tier t1"></div><div class="tier t2"></div><div class="tier t3"></div><div class="plate"></div>
    <div class="wish">Tilak tilang, Dadajon ❤️ <span style="opacity:.6">(tortni bosing)</span></div>
  </div>

  <article class="card">
    <h2>Aziz Dadajonim, 💌</h2>
    <p>Bugun dunyodagi eng mehribon, eng kuchli va eng g‘amxo‘r insonning tug‘ilgan kuni. Siz bizning tayanchimiz, ishonchimiz va g‘ururimizsiz.</p>
    <p>Sizga mustahkam sog‘liq, oilangizga xotirjamlik, uyingizga baraka, dilingizga cheksiz quvonch tilayman. Har bir kuningiz kulgu va mehr bilan to‘lsin, orzularingiz birma-bir ushalsin.</p>
    <p>Sizni juda yaxshi ko‘raman, dada! Doimo bizga omon bo‘ling. 🎂❤️</p>
    <div class="sign">Farzandingiz ❤️</div>
  </article>

  <h3 class="gifts-title">🎁 Sovg‘alarni oching 🎁</h3>
  <div class="row" id="row"></div>
  <div class="reveal" id="reveal"></div>
</section>

<script>
/* ---------- Zarrachalar (konfetti, yulduz, yurak) ---------- */
const cv=document.getElementById('fx'),cx=cv.getContext('2d');let W,H,P=[];
const COL=['#ffd86b','#ff5fa2','#7b4dff','#4ee8b7','#5b8bff','#fff','#ffb52e'];
function size(){const d=devicePixelRatio||1;W=innerWidth;H=innerHeight;cv.width=W*d;cv.height=H*d;cx.setTransform(d,0,0,d,0,0)}
addEventListener('resize',size);size();
const rnd=(a,b)=>a+Math.random()*(b-a);
function add(x,y,type,burst){
  const a=rnd(0,6.283),s=burst?rnd(3,11):rnd(.3,1.2);
  P.push({x,y,vx:burst?Math.cos(a)*s:rnd(-.4,.4),vy:burst?Math.sin(a)*s-3:s,t:type,c:COL[(Math.random()*COL.length)|0],
   r:rnd(5,13),rot:rnd(0,6),vr:rnd(-.2,.2),life:burst?rnd(70,140):9999,g:burst?.18:.01,ph:rnd(0,6)});
}
function burst(x,y,n=70){for(let i=0;i<n;i++)add(x,y,['c','c','s','h'][(Math.random()*4)|0],true)}
function ambient(){
  if(P.length<110&&Math.random()<.35)add(rnd(0,W),-10,['c','s','h','s'][(Math.random()*4)|0],false);
  if(Math.random()<.15)twinkle();
}
function twinkle(){P.push({x:rnd(0,W),y:rnd(0,H),vx:0,vy:0,t:'t',c:'#fff',r:rnd(2,5),rot:0,vr:0,life:60,g:0,ph:0,max:60})}
function loop(){
  cx.clearRect(0,0,W,H);ambient();
  for(let i=P.length-1;i>=0;i--){
    const p=P[i];p.x+=p.vx+Math.sin(p.ph+=.03)*.4;p.y+=p.vy;p.vy+=p.g;if(p.g>.1)p.vx*=.985;p.rot+=p.vr;p.life--;
    if(p.life<=0||p.y>H+20){P.splice(i,1);continue}
    cx.save();cx.translate(p.x,p.y);cx.rotate(p.rot);cx.fillStyle=p.c;
    cx.globalAlpha=p.t==='t'?Math.sin(p.life/p.max*Math.PI):Math.min(1,p.life/30);
    if(p.t==='c'){cx.fillRect(-p.r/2,-p.r/4,p.r,p.r/2)}
    else{cx.shadowColor=p.c;cx.shadowBlur=10;cx.font=(p.t==='t'?p.r*3:p.r*1.8)+'px serif';cx.textAlign='center';cx.textBaseline='middle';
      cx.fillStyle=p.t==='h'?'#ff5fa2':p.c;cx.fillText(p.t==='h'?'♥':'✦',0,0)}
    cx.restore();
  }
  requestAnimationFrame(loop);
}
loop();

/* ---------- Kirish: katta sovg‘a ---------- */
const $=id=>document.getElementById(id);
const big=$('bigGift');let introDone=false;
function center(el){const r=el.getBoundingClientRect();return[r.left+r.width/2,r.top+r.height/3]}
// quti atrofidan doimiy yaltirash
setInterval(()=>{if(introDone)return;const[x,y]=center(big);for(let i=0;i<2;i++){const a=rnd(0,6.28),d=rnd(60,130);
  P.push({x:x+Math.cos(a)*d,y:y+Math.sin(a)*d+30,vx:Math.cos(a)*.3,vy:-rnd(.3,1),t:Math.random()<.5?'s':'t',c:'#ffd86b',r:rnd(3,7),rot:0,vr:.05,life:70,max:70,g:0,ph:rnd(0,6)})}},120);
big.onclick=()=>{
  if(introDone)return;introDone=true;big.classList.add('opening');$('hint').style.display='none';
  const[x,y]=center(big);burst(x,y,130);setTimeout(()=>burst(x,y,80),400);
  setTimeout(()=>{big.classList.add('opened');$('greet').classList.add('in');$('next').classList.add('in');startMusic(true)},500);
};
$('next').onclick=()=>{
  $('intro').classList.add('hide');$('main').classList.add('show');$('main').scrollTop=0;
  burst(W/2,H/3,160);setTimeout(()=>burst(W*.2,H/2,70),300);setTimeout(()=>burst(W*.8,H/2,70),500);
  makeBalloons();
};

/* ---------- Havo sharlari ---------- */
let ballDone=false;
function makeBalloons(){
  if(ballDone)return;ballDone=true;
  for(let i=0;i<9;i++){const b=document.createElement('div');b.className='balloon';const c=COL[i%6];
    b.style.cssText=`left:${5+i*11}%;background:radial-gradient(circle at 30% 30%,#fff8,${c});animation-duration:${rnd(11,20)}s;animation-delay:${rnd(0,10)}s;box-shadow:0 0 18px ${c}88`;
    $('main').appendChild(b)}
}

/* ---------- Tort ---------- */
$('cake').onclick=e=>{
  const c=$('cake');c.classList.toggle('out');const r=c.getBoundingClientRect();
  burst(r.left+r.width/2,r.top+20,c.classList.contains('out')?110:40);
};

/* ---------- 3 ta sovg‘a qutisi ---------- */
const POOL=[
 "Dada, tug‘ilgan kuningiz bilan!","Yoshingiz 100 ga yetsin!","Hech qachon qarimang!",
 "Sog‘-salomat yuring, dadajon!","Doim kulib yuring! 😊","Siz bizning faxrimizsiz! 🏆","Sizni juda yaxshi ko‘ramiz! ❤️"
];
let msgs=[POOL[0],POOL[1],POOL[2]];
const row=$('row'),rev=$('reveal');
const boxes=[1,2,3].map((n,i)=>{
  const s=document.createElement('div');s.className='slot';
  s.innerHTML=`<div class="gift g${n}" style="--d:${i*.25}s"><div class="base"><span class="rib"></span></div><div class="inner"></div><div class="lid"><span class="rib"></span><span class="bow"><i></i><i></i><b></b></span></div></div>`;
  row.appendChild(s);const g=s.firstChild;g.onclick=()=>openBox(i,g);return g});
let closeT;
function shuffle(){ // 3 ta tasodifiy yozuv
  msgs=[...POOL].sort(()=>Math.random()-.5).slice(0,3);
}
function openBox(i,g){
  clearTimeout(closeT);
  boxes.forEach(b=>b.classList.remove('opened'));
  g.classList.remove('opened');void g.offsetWidth;   // animatsiyani qayta ishga tushirish
  g.classList.add('opened');
  const r=g.getBoundingClientRect();burst(r.left+r.width/2,r.top+r.height/3,90);
  setTimeout(()=>burst(r.left+r.width/2,r.top,40),250);
  rev.classList.remove('pop');void rev.offsetWidth;
  rev.style.transformOrigin=(r.left+r.width/2-rev.getBoundingClientRect().left)+'px 0';
  rev.innerHTML=`<div><small>Sovg‘a 🎁</small>${msgs[i]}</div>`;
  rev.classList.add('pop');
  shuffle(); // keyingi bosishda boshqa tabrik chiqadi
  closeT=setTimeout(()=>g.classList.remove('opened'),4500);
}

/* ---------- Musiqa (Web Audio, tashqi fayl kerak emas) ---------- */
let ac,playing=false,step=0,timer;
const NOTES=[261.6,329.6,392,523.3,392,329.6,293.7,349.2,440,587.3,440,349.2,246.9,293.7,392,493.9,392,293.7,261.6,329.6,392,659.3,523.3,392];
function tone(f,t,d,v){const o=ac.createOscillator(),g=ac.createGain();o.type='sine';o.frequency.value=f;
  g.gain.setValueAtTime(0,t);g.gain.linearRampToValueAtTime(v,t+.05);g.gain.exponentialRampToValueAtTime(.0001,t+d);
  o.connect(g).connect(ac.destination);o.start(t);o.stop(t+d)}
function tick(){const t=ac.currentTime+.05,f=NOTES[step%NOTES.length];tone(f,t,1.2,.09);tone(f/2,t,1.6,.05);
  if(step%4===0)tone(f*1.5,t+.1,1,.03);step++}
function startMusic(auto){
  if(playing)return;try{ac=ac||new (window.AudioContext||window.webkitAudioContext)();ac.resume();}catch(e){return}
  playing=true;timer=setInterval(tick,520);$('music').classList.add('on');$('music').textContent='⏸';
}
function stopMusic(){playing=false;clearInterval(timer);$('music').classList.remove('on');$('music').textContent='🎵'}
$('music').onclick=()=>playing?stopMusic():startMusic();
</script>
</body>
</html>
