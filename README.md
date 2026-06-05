<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Varun Solanki — Shadow Architect</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Orbitron:wght@400;700;900&family=Rajdhani:wght@400;600;700&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{--green:#00ff41;--blue:#0088ff;--purple:#a040ff;--gold:#ffd700;--red:#ff0080}
body{background:#000;font-family:'Rajdhani',sans-serif;color:var(--green);min-height:100vh;overflow-x:hidden}
canvas#bg{position:fixed;top:0;left:0;width:100%;height:100%;z-index:0;pointer-events:none}
.page{position:relative;z-index:2;max-width:820px;margin:0 auto;padding:40px 20px 60px}

.hero{text-align:center;padding:40px 0 30px}
.sys-tag{font-family:'Share Tech Mono',monospace;font-size:11px;color:var(--green);letter-spacing:4px;opacity:.7;margin-bottom:14px;animation:fadeUp 1s ease}
.glitch{font-family:'Orbitron',sans-serif;font-size:clamp(32px,8vw,64px);font-weight:900;color:#fff;position:relative;display:inline-block}
.glitch::before{content:attr(data-text);position:absolute;top:0;left:0;width:100%;color:var(--green);clip-path:polygon(0 0,100% 0,100% 35%,0 35%);animation:g1 5s infinite}
.glitch::after{content:attr(data-text);position:absolute;top:0;left:0;width:100%;color:var(--red);clip-path:polygon(0 65%,100% 65%,100% 100%,0 100%);animation:g2 5s infinite}
@keyframes g1{0%,88%,100%{transform:none}89%{transform:translateX(-5px)}91%{transform:translateX(5px)}93%{transform:none}}
@keyframes g2{0%,88%,100%{transform:none}90%{transform:translateX(5px)}92%{transform:translateX(-5px)}94%{transform:none}}
.sub{font-family:'Share Tech Mono',monospace;font-size:13px;letter-spacing:3px;margin:12px 0 18px;color:rgba(0,255,65,0.8)}
.rank-badge{display:inline-block;border:1px solid var(--red);color:var(--red);font-family:'Orbitron',sans-serif;font-size:11px;padding:7px 22px;letter-spacing:3px;animation:rpulse 2s infinite}
@keyframes rpulse{0%,100%{box-shadow:0 0 8px var(--red)}50%{box-shadow:0 0 24px var(--red),0 0 48px rgba(255,0,128,0.2)}}
@keyframes fadeUp{from{opacity:0;transform:translateY(-12px)}to{opacity:1;transform:translateY(0)}}

.scan{width:100%;height:2px;background:linear-gradient(90deg,transparent,var(--green),transparent);margin:28px 0;animation:scanAnim 3s infinite}
@keyframes scanAnim{0%,100%{opacity:.3}50%{opacity:1}}

.hcard{border:1px solid var(--green);background:rgba(0,20,0,0.88);position:relative;overflow:hidden;margin-bottom:28px;animation:slideUp .8s ease .2s both}
.hcard::before{content:'';position:absolute;inset:-2px;background:conic-gradient(var(--green),transparent,var(--green),transparent);z-index:-1;animation:spin 5s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes slideUp{from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:translateY(0)}}
.hcard-hdr{background:rgba(0,255,65,.07);border-bottom:1px solid rgba(0,255,65,.25);padding:10px 18px;display:flex;justify-content:space-between;align-items:center}
.hcard-t{font-family:'Orbitron',sans-serif;font-size:12px;letter-spacing:3px}
.hcard-id{font-family:'Share Tech Mono',monospace;font-size:10px;opacity:.5}
.hcard-body{padding:20px;display:grid;grid-template-columns:1fr 1fr;gap:20px}
@media(max-width:560px){.hcard-body{grid-template-columns:1fr}}
.info-pair{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:14px}
.ip-k{font-family:'Share Tech Mono',monospace;font-size:9px;color:rgba(0,255,65,.5)}
.ip-v{font-size:13px;font-weight:600;color:#fff;margin-top:2px}
.stat-r{display:flex;align-items:center;gap:10px;margin-bottom:8px}
.stat-lbl{font-family:'Share Tech Mono',monospace;font-size:10px;min-width:34px;opacity:.7}
.bar-bg{flex:1;height:5px;background:rgba(0,255,65,.1);border:1px solid rgba(0,255,65,.15);overflow:hidden}
.bar-f{height:100%;width:0;background:linear-gradient(90deg,#003300,var(--green));transition:width 1.5s ease;position:relative}
.bar-f::after{content:'';position:absolute;right:0;top:0;width:2px;height:100%;background:#fff;box-shadow:0 0 5px var(--green)}
.stat-v{font-family:'Share Tech Mono',monospace;font-size:10px;min-width:28px;text-align:right}
.skill-sec{border:1px solid rgba(0,255,65,.18);background:rgba(0,18,0,.5);padding:12px}
.skill-lbl{font-family:'Share Tech Mono',monospace;font-size:9px;opacity:.5;margin-bottom:10px}
.card-title{grid-column:1/-1;text-align:center;font-family:'Orbitron',sans-serif;font-size:10px;color:var(--gold);letter-spacing:2px;padding-top:12px;border-top:1px solid rgba(0,255,65,.15)}

.sec{margin-bottom:28px}
.sec-h{font-family:'Orbitron',sans-serif;font-size:11px;letter-spacing:3px;border-left:3px solid var(--green);padding-left:10px;margin-bottom:16px}

.dom-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
@media(max-width:480px){.dom-grid{grid-template-columns:1fr}}
.dom{border:1px solid rgba(0,255,65,.25);background:rgba(0,10,0,.8);padding:18px 12px;text-align:center;cursor:pointer;transition:all .35s;position:relative;overflow:hidden}
.dom:hover{transform:translateY(-4px);border-color:var(--green);background:rgba(0,40,0,.9)}
.dom::before{content:'';position:absolute;inset:0;background:radial-gradient(circle,rgba(0,255,65,.07),transparent);opacity:0;transition:.3s}
.dom:hover::before{opacity:1}
.dom-ico{font-size:28px;margin-bottom:10px;display:block}
.dom-n{font-family:'Orbitron',sans-serif;font-size:10px;letter-spacing:2px;margin-bottom:6px}
.dom-s{font-family:'Share Tech Mono',monospace;font-size:9px;line-height:1.7;opacity:.55}

.tech{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
@media(max-width:480px){.tech{grid-template-columns:repeat(3,1fr)}}
.tp{border:1px solid rgba(0,255,65,.22);background:rgba(0,12,0,.7);padding:9px 6px;text-align:center;font-family:'Share Tech Mono',monospace;font-size:10px;letter-spacing:1px;transition:all .3s;cursor:default}
.tp:hover{background:rgba(0,255,65,.08);border-color:var(--green);color:#fff}
.tp.hl{border-color:var(--gold);color:var(--gold)}

.quest{display:flex;align-items:flex-start;gap:10px;padding:11px 14px;border:1px solid rgba(0,255,65,.14);background:rgba(0,8,0,.6);margin-bottom:7px;transition:all .3s}
.quest:hover{border-color:rgba(0,255,65,.45);background:rgba(0,28,0,.8)}
.qst{font-family:'Share Tech Mono',monospace;font-size:9px;padding:3px 8px;white-space:nowrap;font-weight:bold;letter-spacing:1px}
.qa{border:1px solid var(--green);color:var(--green);background:rgba(0,255,65,.08);animation:qblink 2s infinite}
.ql{border:1px solid rgba(100,100,100,.4);color:rgba(120,120,120,.55)}
@keyframes qblink{0%,100%{opacity:1}50%{opacity:.5}}
.qt{font-size:14px;color:rgba(200,255,200,.9);line-height:1.4}

.aw-wrap{padding:4px 0}
.aw{display:flex;align-items:center;gap:14px;padding:10px 12px;position:relative}
.aw-line-v{position:absolute;left:18px;top:0;bottom:0;width:1px;background:rgba(0,255,65,.2)}
.aw-d{width:16px;height:16px;border-radius:50%;border:2px solid rgba(0,255,65,.35);background:#000;z-index:1;flex-shrink:0}
.aw-d.done{border-color:var(--green);background:var(--green);box-shadow:0 0 10px var(--green)}
.aw-d.cur{border-color:var(--gold);background:rgba(255,215,0,.15);animation:curPulse 1.5s infinite}
@keyframes curPulse{0%,100%{box-shadow:0 0 6px var(--gold)}50%{box-shadow:0 0 20px var(--gold),0 0 40px rgba(255,215,0,.25)}}
.aw-rk{font-family:'Orbitron',sans-serif;font-size:9px;letter-spacing:2px;min-width:100px}
.aw-rk.done{color:var(--green)}
.aw-rk.cur{color:var(--gold)}
.aw-rk.lk{color:rgba(90,90,90,.5)}
.aw-dc{font-family:'Share Tech Mono',monospace;font-size:10px}
.aw-dc.done{color:rgba(0,255,65,.75)}
.aw-dc.cur{color:var(--gold)}
.aw-dc.lk{color:rgba(90,90,90,.4)}

.term{border:1px solid rgba(0,255,65,.28);background:rgba(0,7,0,.95);padding:20px;font-family:'Share Tech Mono',monospace;font-size:12px;line-height:2}
.tp2{color:rgba(0,255,65,.5)}
.tc{color:var(--green)}
.to{color:rgba(160,255,160,.8);padding-left:16px;line-height:1.9;display:block}
.tcur{display:inline-block;width:8px;height:13px;background:var(--green);vertical-align:middle;animation:cblink 1s infinite}
@keyframes cblink{0%,49%{opacity:1}50%,100%{opacity:0}}

footer{text-align:center;padding:32px 0 20px;border-top:1px solid rgba(0,255,65,.18)}
.fq{font-family:'Orbitron',sans-serif;font-size:11px;color:rgba(0,255,65,.7);letter-spacing:2px;line-height:2.2}
.badges{display:flex;justify-content:center;gap:12px;flex-wrap:wrap;margin-top:18px}
.bdg{border:1px solid rgba(0,255,65,.3);padding:7px 16px;font-family:'Share Tech Mono',monospace;font-size:10px;letter-spacing:1px;transition:.3s;cursor:pointer;color:var(--green)}
.bdg:hover{background:rgba(0,255,65,.08);border-color:var(--green)}
</style>
</head>
<body>

<canvas id="bg"></canvas>

<div class="page">

  <!-- HERO -->
  <div class="hero">
    <div class="sys-tag">[ HUNTER SYSTEM &middot; NEURAL INTERFACE ACTIVE ]</div>
    <div class="glitch" data-text="VARUN SOLANKI">VARUN SOLANKI</div>
    <div class="sub">AI SYSTEMS &middot; CYBERSECURITY &middot; BLOCKCHAIN</div>
    <div class="rank-badge">&#9672; S-CLASS ASCENDING &#9672;</div>
  </div>

  <div class="scan"></div>

  <!-- HUNTER CARD -->
  <div class="hcard">
    <div class="hcard-hdr">
      <span class="hcard-t">&#9672; HUNTER PROFILE</span>
      <span class="hcard-id">ID: SHADOW-0001 &middot; STATUS: ACTIVE</span>
    </div>
    <div class="hcard-body">
      <div>
        <div class="info-pair">
          <div><div class="ip-k">CLASS</div><div class="ip-v">Shadow Architect</div></div>
          <div><div class="ip-k">RANK</div><div class="ip-v" style="color:var(--gold)">S-Class &#8593;</div></div>
          <div><div class="ip-k">DEGREE</div><div class="ip-v">B.Tech AIML</div></div>
          <div><div class="ip-k">GUILD</div><div class="ip-v">Solo</div></div>
        </div>
        <div class="stat-r"><span class="stat-lbl">INT</span><div class="bar-bg"><div class="bar-f" data-w="92"></div></div><span class="stat-v">92</span></div>
        <div class="stat-r"><span class="stat-lbl">STR</span><div class="bar-bg"><div class="bar-f" data-w="80"></div></div><span class="stat-v">80</span></div>
        <div class="stat-r"><span class="stat-lbl">DEF</span><div class="bar-bg"><div class="bar-f" data-w="85"></div></div><span class="stat-v">85</span></div>
        <div class="stat-r"><span class="stat-lbl">AGI</span><div class="bar-bg"><div class="bar-f" data-w="72"></div></div><span class="stat-v">72</span></div>
        <div class="stat-r"><span class="stat-lbl">LCK</span><div class="bar-bg"><div class="bar-f" data-w="100" style="background:linear-gradient(90deg,#402000,var(--gold))"></div></div><span class="stat-v" style="color:var(--gold)">&#8734;</span></div>
      </div>
      <div>
        <div class="skill-sec">
          <div class="skill-lbl">DOMAIN SKILL UNLOCK %</div>
          <div class="stat-r"><span class="stat-lbl" style="font-size:9px;min-width:42px">AI/ML</span><div class="bar-bg"><div class="bar-f" data-w="88"></div></div><span class="stat-v">88%</span></div>
          <div class="stat-r"><span class="stat-lbl" style="font-size:9px;min-width:42px">CYBER</span><div class="bar-bg"><div class="bar-f" data-w="75" style="background:linear-gradient(90deg,#000040,var(--blue))"></div></div><span class="stat-v" style="color:var(--blue)">75%</span></div>
          <div class="stat-r"><span class="stat-lbl" style="font-size:9px;min-width:42px">CHAIN</span><div class="bar-bg"><div class="bar-f" data-w="68" style="background:linear-gradient(90deg,#200040,var(--purple))"></div></div><span class="stat-v" style="color:var(--purple)">68%</span></div>
        </div>
        <div style="margin-top:12px;border:1px solid rgba(0,255,65,.15);padding:10px;text-align:center">
          <div style="font-family:'Share Tech Mono',monospace;font-size:9px;color:rgba(0,255,65,.5)">STATUS: TRAINING ARC ACTIVE</div>
          <div style="font-family:'Share Tech Mono',monospace;font-size:10px;color:var(--gold);margin-top:5px">&#9650; EXP GAINED DAILY</div>
        </div>
      </div>
      <div class="card-title">&#10022; "THE ONE WHO BUILDS IN SILENCE" &#10022;</div>
    </div>
  </div>

  <!-- THREE DOMAINS -->
  <div class="sec">
    <div class="sec-h">THREE-DOMAIN PROTOCOL</div>
    <div class="dom-grid">
      <div class="dom">
        <span class="dom-ico">&#129504;</span>
        <div class="dom-n">AI / ML</div>
        <div class="dom-s">Neural networks<br>LLM design &amp; APIs<br>Intelligent systems</div>
      </div>
      <div class="dom" style="border-color:rgba(0,100,255,.28)">
        <span class="dom-ico">&#128274;</span>
        <div class="dom-n" style="color:var(--blue)">CYBERSECURITY</div>
        <div class="dom-s" style="color:rgba(100,160,255,.55)">Offensive theory<br>Defense architecture<br>Secure engineering</div>
      </div>
      <div class="dom" style="border-color:rgba(150,0,255,.28)">
        <span class="dom-ico">&#9935;</span>
        <div class="dom-n" style="color:var(--purple)">BLOCKCHAIN</div>
        <div class="dom-s" style="color:rgba(160,100,255,.55)">Smart contracts<br>DeFi security<br>Web3 + AI agents</div>
      </div>
    </div>
  </div>

  <!-- TECH ARSENAL -->
  <div class="sec">
    <div class="sec-h">TECH ARSENAL</div>
    <div class="tech">
      <div class="tp hl">PYTHON</div>
      <div class="tp hl">PyTorch</div>
      <div class="tp">LINUX</div>
      <div class="tp">GIT</div>
      <div class="tp">FLASK</div>
      <div class="tp">DJANGO</div>
      <div class="tp">JAVA</div>
      <div class="tp">C</div>
      <div class="tp hl">LLM APIs</div>
      <div class="tp">DOCKER</div>
      <div class="tp">HTML/CSS</div>
      <div class="tp" style="border-color:rgba(150,0,255,.4);color:var(--purple)">SOLIDITY</div>
    </div>
  </div>

  <!-- QUESTS -->
  <div class="sec">
    <div class="sec-h">ACTIVE QUESTS</div>
    <div class="quest"><span class="qst qa">ACTIVE</span><div class="qt">Build AI-powered voice + text assistant beyond demo level</div></div>
    <div class="quest"><span class="qst qa">ACTIVE</span><div class="qt">Master cybersecurity exploit patterns to engineer defense</div></div>
    <div class="quest"><span class="qst qa">ACTIVE</span><div class="qt">Study smart contract vulnerabilities + DeFi attack vectors</div></div>
    <div class="quest"><span class="qst qa">ACTIVE</span><div class="qt">Build strong ML foundations through real deployable systems</div></div>
    <div class="quest"><span class="qst ql">LOCKED</span><div class="qt" style="color:rgba(100,100,100,.6)">Autonomous AI agent operating on-chain &mdash; S-rank required</div></div>
    <div class="quest"><span class="qst ql">LOCKED</span><div class="qt" style="color:rgba(100,100,100,.6)">Redefine human&ndash;computer interaction &mdash; final dungeon</div></div>
  </div>

  <!-- AWAKENING -->
  <div class="sec">
    <div class="sec-h">AWAKENING STAGES</div>
    <div class="aw-wrap">
      <div class="aw"><div class="aw-line-v"></div><div class="aw-d done"></div><span class="aw-rk done">E-RANK</span><span class="aw-dc done">Learned Python &middot; First ML model &#10003;</span></div>
      <div class="aw"><div class="aw-line-v"></div><div class="aw-d done"></div><span class="aw-rk done">D-RANK</span><span class="aw-dc done">Built first full-stack AI app &#10003;</span></div>
      <div class="aw"><div class="aw-line-v"></div><div class="aw-d done"></div><span class="aw-rk done">C-RANK</span><span class="aw-dc done">Entered cybersec + blockchain &#10003;</span></div>
      <div class="aw"><div class="aw-line-v"></div><div class="aw-d cur"></div><span class="aw-rk cur">B &#8594; A RANK</span><span class="aw-dc cur">&#9889; Designing intelligent systems &mdash; NOW</span></div>
      <div class="aw"><div class="aw-line-v"></div><div class="aw-d"></div><span class="aw-rk lk">S-RANK</span><span class="aw-dc lk">Autonomous AI at production scale</span></div>
      <div class="aw"><div class="aw-d"></div><span class="aw-rk lk">SHADOW MONARCH</span><span class="aw-dc lk">Redefine HCI &mdash; final form</span></div>
    </div>
  </div>

  <!-- TERMINAL -->
  <div class="sec">
    <div class="sec-h">SYSTEM MANIFESTO</div>
    <div class="term">
      <div><span class="tp2">root@varun:~$ </span><span class="tc">cat /etc/manifesto</span></div>
      <span class="to">» I don't chase trends. I study foundations.</span>
      <span class="to">» Cybersec: think like the attacker to architect defense.</span>
      <span class="to">» Blockchain: trustless systems are the future of trust.</span>
      <span class="to">» AI: the most powerful amplifier ever created.</span>
      <span class="to">» Three domains. One mind. Unfair advantage.</span>
      <br>
      <div><span class="tp2">root@varun:~$ </span><span class="tc">ping future.io</span></div>
      <span class="to">PONG &middot; 64 bytes from destiny &middot; ttl=&#8734; ms=0</span>
      <br>
      <div><span class="tp2">root@varun:~$ </span><span class="tcur"></span></div>
    </div>
  </div>

  <!-- FOOTER -->
  <footer>
    <div class="fq">
      "THE STRONGEST HUNTERS DON'T ANNOUNCE THEIR POWER LEVEL."<br>
      <span style="font-size:9px;letter-spacing:1px;opacity:.5">&mdash; BUILDING QUIETLY. ASCENDING DAILY. &mdash;</span>
    </div>
    <div class="badges">
      <div class="bdg">AI / ML</div>
      <div class="bdg" style="color:var(--blue);border-color:rgba(0,136,255,.3)">CYBERSECURITY</div>
      <div class="bdg" style="color:var(--purple);border-color:rgba(160,64,255,.3)">BLOCKCHAIN</div>
      <div class="bdg" style="color:var(--gold);border-color:rgba(255,215,0,.3)">github: watashiwa01</div>
    </div>
  </footer>

</div>

<script>
var cv = document.getElementById('bg');
var cx = cv.getContext('2d');
function rsz() { cv.width = window.innerWidth; cv.height = window.innerHeight; }
rsz();
var chars = '01アイウカキクケコサシ{}[]<>//\\ABCDEF';
var cols, drops;
function init() {
  cols = Math.floor(cv.width / 16);
  drops = [];
  for (var i = 0; i < cols; i++) { drops[i] = Math.random() * -60; }
}
init();
function draw() {
  cx.fillStyle = 'rgba(0,0,0,0.06)';
  cx.fillRect(0, 0, cv.width, cv.height);
  cx.font = '12px "Share Tech Mono", monospace';
  for (var i = 0; i < drops.length; i++) {
    var c = chars[Math.floor(Math.random() * chars.length)];
    var b = Math.random();
    cx.fillStyle = b > 0.97 ? '#ffffff' : b > 0.9 ? 'rgba(0,255,65,0.7)' : 'rgba(0,255,65,0.12)';
    cx.fillText(c, i * 16, drops[i] * 16);
    if (drops[i] * 16 > cv.height && Math.random() > 0.975) drops[i] = 0;
    drops[i] += 0.35;
  }
}
setInterval(draw, 50);
window.addEventListener('resize', function() { rsz(); init(); });
window.addEventListener('load', function() {
  var bars = document.querySelectorAll('.bar-f');
  for (var i = 0; i < bars.length; i++) {
    (function(b) {
      setTimeout(function() { b.style.width = b.getAttribute('data-w') + '%'; }, 400);
    })(bars[i]);
  }
});
</script>
</body>
</html>
