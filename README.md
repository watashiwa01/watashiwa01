<div align="center">

<!-- ============ MEGA ANIMATED HERO — pure inline SVG, no external image proxy ============ -->
<svg width="100%" height="340" viewBox="0 0 1000 340" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bgShift" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#05010a">
        <animate attributeName="stop-color" values="#05010a;#1a0025;#001a12;#05010a" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="50%" stop-color="#12002a">
        <animate attributeName="stop-color" values="#12002a;#00120e;#1a0025;#12002a" dur="8s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" stop-color="#000">
        <animate attributeName="stop-color" values="#000;#0a0014;#000;#000" dur="8s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>
    <linearGradient id="scan" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00ff9c" stop-opacity="0"/>
      <stop offset="50%" stop-color="#00ff9c" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#00ff9c" stop-opacity="0"/>
    </linearGradient>
    <filter id="glow" x="-60%" y="-60%" width="220%" height="220%">
      <feGaussianBlur stdDeviation="4" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
  </defs>

  <rect width="1000" height="340" rx="16" fill="url(#bgShift)"/>
  <rect x="2" y="2" width="996" height="336" rx="14" fill="none" stroke="#00ff9c" stroke-width="1.6">
    <animate attributeName="opacity" values="0.2;0.9;0.2" dur="2.4s" repeatCount="indefinite"/>
    <animate attributeName="stroke" values="#00ff9c;#ff3fa4;#7d7dff;#00ff9c" dur="6s" repeatCount="indefinite"/>
  </rect>

  <!-- scan sweep -->
  <rect x="-220" y="0" width="220" height="340" fill="url(#scan)">
    <animateTransform attributeName="transform" type="translate" values="-220 0; 1000 0; -220 0" dur="5s" repeatCount="indefinite"/>
  </rect>

  <!-- floating particles (EXP orbs rising) -->
  <g fill="#00ff9c">
    <circle r="2.4" opacity="0.8"><animateMotion path="M60,330 C40,220 90,120 55,10" dur="6s" repeatCount="indefinite"/><animate attributeName="opacity" values="0;0.9;0" dur="6s" repeatCount="indefinite"/></circle>
    <circle r="2" fill="#ff3fa4" opacity="0.8"><animateMotion path="M200,330 C220,240 170,140 210,10" dur="7s" repeatCount="indefinite"/><animate attributeName="opacity" values="0;0.9;0" dur="7s" repeatCount="indefinite"/></circle>
    <circle r="2.6" fill="#7d7dff" opacity="0.8"><animateMotion path="M820,330 C800,230 850,130 810,10" dur="5.5s" repeatCount="indefinite"/><animate attributeName="opacity" values="0;0.9;0" dur="5.5s" repeatCount="indefinite"/></circle>
    <circle r="2" opacity="0.8"><animateMotion path="M940,330 C920,220 960,120 930,10" dur="6.5s" repeatCount="indefinite"/><animate attributeName="opacity" values="0;0.9;0" dur="6.5s" repeatCount="indefinite"/></circle>
    <circle r="2.2" fill="#ffd166" opacity="0.8"><animateMotion path="M470,330 C500,230 440,130 480,10" dur="7.5s" repeatCount="indefinite"/><animate attributeName="opacity" values="0;0.9;0" dur="7.5s" repeatCount="indefinite"/></circle>
  </g>

  <!-- HUD corner brackets, pulsing -->
  <g stroke="#00ff9c" stroke-width="2" fill="none">
    <path d="M24 24 L24 50 M24 24 L50 24"><animate attributeName="stroke-opacity" values="0.4;1;0.4" dur="1.8s" repeatCount="indefinite"/></path>
    <path d="M976 24 L976 50 M976 24 L950 24"><animate attributeName="stroke-opacity" values="0.4;1;0.4" dur="1.8s" repeatCount="indefinite"/></path>
    <path d="M24 316 L24 290 M24 316 L50 316"><animate attributeName="stroke-opacity" values="0.4;1;0.4" dur="1.8s" repeatCount="indefinite"/></path>
    <path d="M976 316 L976 290 M976 316 L950 316"><animate attributeName="stroke-opacity" values="0.4;1;0.4" dur="1.8s" repeatCount="indefinite"/></path>
  </g>

  <text x="500" y="72" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="13" fill="#00ff9c" letter-spacing="5" opacity="0.85">
    ARCHIVE // ANOMALOUS HUNTER FILE
    <animate attributeName="opacity" values="0.5;1;0.5" dur="2.4s" repeatCount="indefinite"/>
  </text>

  <!-- GLITCH TITLE: three offset colored layers flicker in and out -->
  <g font-family="Share Tech Mono, monospace" font-size="64" font-weight="700" text-anchor="middle" letter-spacing="4">
    <text x="503" y="150" fill="#ff3fa4" opacity="0.7">
      MR. FOOL
      <animate attributeName="x" values="503;497;505;500;503" dur="2.6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0;0.7;0;0.5;0" dur="2.6s" repeatCount="indefinite"/>
    </text>
    <text x="497" y="150" fill="#7d7dff" opacity="0.7">
      MR. FOOL
      <animate attributeName="x" values="497;503;495;500;497" dur="3.1s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values="0.5;0;0.6;0;0.5" dur="3.1s" repeatCount="indefinite"/>
    </text>
    <text x="500" y="150" fill="#eafff0" filter="url(#glow)">MR. FOOL</text>
  </g>

  <text x="500" y="188" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="14" fill="#8affc1" letter-spacing="2">
    THE ONE WHO PLAYS DUMB WHILE THE SYSTEM LEVELS UP
  </text>

  <!-- EXP ring, spinning + filling -->
  <g transform="translate(500,246)">
    <circle r="26" fill="none" stroke="#123" stroke-width="6"/>
    <circle r="26" fill="none" stroke="#00ff9c" stroke-width="6" stroke-linecap="round"
            stroke-dasharray="163" stroke-dashoffset="163" transform="rotate(-90)">
      <animate attributeName="stroke-dashoffset" values="163;20;163" dur="4s" repeatCount="indefinite"/>
      <animate attributeName="stroke" values="#00ff9c;#ff3fa4;#7d7dff;#00ff9c" dur="4s" repeatCount="indefinite"/>
    </circle>
    <text x="0" y="6" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="12" fill="#eafff0">EXP</text>
  </g>

  <!-- terminal line with blinking cursor -->
  <text x="500" y="312" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="14" fill="#00ff9c">
    <tspan fill="#7d7dff">mr.fool</tspan><tspan fill="#5f5f5f">@</tspan><tspan fill="#ff3fa4">unknown-rank</tspan><tspan fill="#5f5f5f">:~$ </tspan><tspan fill="#eafff0">whoami --classified</tspan>
    <tspan fill="#00ff9c">▌<animate attributeName="opacity" values="1;0;1" dur="0.9s" repeatCount="indefinite"/></tspan>
  </text>
</svg>

<br/>

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=15&pause=900&color=00FF9C&center=true&vCenter=true&width=860&lines=%5BBOOT%5D+identity+obfuscated+on+purpose...;%5BALIAS%5D+MR.+FOOL+%C2%B7+rank%3A+unlisted;%5BLOG%5D+plays+dumb+in+public%2C+levels+up+in+private;%5BPROTOCOL%5D+observe+%E2%80%BA+break+%E2%80%BA+rebuild+%E2%80%BA+ascend" alt="typing banner"/>

&nbsp;

[![Visits](https://komarev.com/ghpvc/?username=watashiwa01&style=for-the-badge&color=00ff9c&label=SYSTEM%20PINGS&labelColor=0a0a0a)](https://github.com/watashiwa01)
[![Status](https://img.shields.io/badge/STATUS-TRAINING%20ARC-00ff9c?style=for-the-badge&labelColor=0a0a0a)](#)
[![Rank](https://img.shields.io/badge/RANK-UNLISTED_%E2%80%94_S--CLASS_SUSPECTED-ff3fa4?style=for-the-badge&labelColor=0a0a0a)](#)

</div>

<br/>

## ⟢ Field Report

> Everyone underestimates the fool. That's the point. While the room laughs, the system quietly logs another level-up.

B.Tech AI/ML student operating across three fronts most people treat as separate careers: **build the intelligence, understand how it gets broken, design the trustless rails it eventually runs on.** No hype, no clout-farming — this profile is a training log, not a highlight reel.

<br/>

## ⟢ The Three Fronts

<div align="center">

<table>
<tr>
<td width="33%" align="center" valign="top">

### 🧠 AI / ML
<sub>neural networks · LLM tooling · applied systems</sub>

`88%` mastery

</td>
<td width="33%" align="center" valign="top">

### 🔓 Cybersecurity
<sub>offense theory · defense architecture</sub>

`75%` mastery

</td>
<td width="33%" align="center" valign="top">

### ⛓ Blockchain
<sub>smart contracts · DeFi attack surfaces</sub>

`68%` mastery

</td>
</tr>
</table>

*The edge isn't any one of these — it's the intersection.*

</div>

<br/>

## ⟢ Live Stat Panel — animated on load

<div align="center">

<svg width="720" height="150" viewBox="0 0 720 150" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bar1" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#00ff9c"/><stop offset="100%" stop-color="#00c2ff"/>
    </linearGradient>
    <linearGradient id="bar2" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#ff3fa4"/><stop offset="100%" stop-color="#7d7dff"/>
    </linearGradient>
    <linearGradient id="bar3" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#ffd166"/><stop offset="100%" stop-color="#00ff9c"/>
    </linearGradient>
  </defs>
  <style>text{font-family:'Share Tech Mono',monospace;fill:#cfffe0;font-size:13px;}</style>

  <text x="0" y="18">AI / ML</text>
  <rect x="0" y="26" width="560" height="14" rx="7" fill="#0d0d0d" stroke="#1e1e1e"/>
  <rect x="0" y="26" height="14" rx="7" fill="url(#bar1)">
    <animate attributeName="width" values="0;493;493;0" keyTimes="0;0.3;0.85;1" dur="5s" repeatCount="indefinite"/>
  </rect>
  <text x="575" y="38">88%</text>

  <text x="0" y="68">CYBERSECURITY</text>
  <rect x="0" y="76" width="560" height="14" rx="7" fill="#0d0d0d" stroke="#1e1e1e"/>
  <rect x="0" y="76" height="14" rx="7" fill="url(#bar2)">
    <animate attributeName="width" values="0;420;420;0" keyTimes="0;0.3;0.85;1" dur="5s" begin="0.3s" repeatCount="indefinite"/>
  </rect>
  <text x="575" y="88">75%</text>

  <text x="0" y="118">BLOCKCHAIN</text>
  <rect x="0" y="126" width="560" height="14" rx="7" fill="#0d0d0d" stroke="#1e1e1e"/>
  <rect x="0" y="126" height="14" rx="7" fill="url(#bar3)">
    <animate attributeName="width" values="0;381;381;0" keyTimes="0;0.3;0.85;1" dur="5s" begin="0.6s" repeatCount="indefinite"/>
  </rect>
  <text x="575" y="138">68%</text>
</svg>

</div>

<br/>

## ⟢ Arsenal

<div align="center">

**Core**

<img src="https://skillicons.dev/icons?i=python,java,c,linux,git,github,vscode&theme=dark&perline=7"/>

**Deploy**

<img src="https://skillicons.dev/icons?i=flask,django,html,css,docker&theme=dark&perline=7"/>

</div>

<div align="center">

| Weapon | Domain | Mastery |
|:--|:--|:--:|
| ![Python](https://img.shields.io/badge/Python-000?style=flat-square&logo=python&logoColor=00ff9c) | AI / ML | `██████████████` |
| ![PyTorch](https://img.shields.io/badge/PyTorch-000?style=flat-square&logo=pytorch&logoColor=00ff9c) | Deep Learning | `███████████░░░` |
| ![LLM APIs](https://img.shields.io/badge/LLM_APIs-000?style=flat-square&labelColor=000&color=00ff9c) | AI Systems | `██████████████` |
| ![Linux](https://img.shields.io/badge/Linux-000?style=flat-square&logo=linux&logoColor=00ff9c) | Systems | `███████████░░░` |
| ![Solidity](https://img.shields.io/badge/Solidity-000?style=flat-square&logo=solidity&logoColor=a97bff) | Blockchain | `█████████░░░░░` |

</div>

<br/>

## ⟢ Quest Log — Season 1: The Ascension Protocol

- [x] Learn Python → ship first ML model
- [x] Build first full-stack AI application
- [x] Break into cybersecurity + blockchain fundamentals
- [ ] Design and ship an intelligent, production-shaped system *(in progress)*
- [ ] Study smart-contract vulnerabilities & DeFi attack vectors *(in progress)*
- [ ] Ship an autonomous AI agent operating on-chain
- [ ] Redefine a slice of human–computer interaction

<br/>

## ⟢ System Manifesto

```bash
mr.fool@unknown-rank:~$ cat manifesto.txt

  I study foundations, not trends.
  In security, think like the attacker to build the defender.
  In blockchain, trustless systems are just trust — redesigned.
  In AI, the amplifier is only as good as the mind behind it.
  Let them think the fool. The system already knows the rank.

mr.fool@unknown-rank:~$ ping future.io
  64 bytes from destiny: ttl=∞ time=0ms
```

<br/>

## ⟢ Diagnostics

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=watashiwa01&show_icons=true&theme=chartreuse-dark&hide_border=true&bg_color=060606&title_color=00ff9c&icon_color=00ff9c&text_color=cfffe0" width="48%"/>
<img src="https://github-readme-streak-stats.herokuapp.com?user=watashiwa01&theme=chartreuse-dark&hide_border=true&background=060606&ring=00ff9c&fire=ff3fa4&currStreakLabel=00ff9c&sideLabels=cfffe0&dates=666666" width="48%"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=watashiwa01&layout=compact&theme=chartreuse-dark&hide_border=true&bg_color=060606&title_color=00ff9c&text_color=cfffe0" width="40%"/>

</div>

<br/>

## ⟢ Neural Trail

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/watashiwa01/watashiwa01/blob/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/watashiwa01/watashiwa01/blob/output/github-contribution-grid-snake.svg"/>
  <img alt="contribution snake" src="https://github.com/watashiwa01/watashiwa01/blob/output/github-contribution-grid-snake-dark.svg"/>
</picture>

</div>

<br/>

## ⟢ Signal

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-coming_soon-0a0a0a?style=for-the-badge&logo=linkedin&logoColor=00ff9c)](https://linkedin.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-building-0a0a0a?style=for-the-badge&logo=vercel&logoColor=00ff9c)](https://github.com/watashiwa01)
[![GitHub](https://img.shields.io/badge/GitHub-watashiwa01-0a0a0a?style=for-the-badge&logo=github&logoColor=00ff9c)](https://github.com/watashiwa01)

</div>

<br/>

<div align="center">

<sub>The strongest hunters don't announce their power level. They let you call them a fool first.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:1a0025,50:001a12,100:000000&section=footer"/>

</div>
