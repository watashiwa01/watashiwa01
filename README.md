<div align="center">

<!-- ================= CUSTOM ANIMATED HERO — inline SVG, real SMIL animation ================= -->
<svg width="100%" height="280" viewBox="0 0 1000 280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#02040a"/>
      <stop offset="55%" stop-color="#001a0f"/>
      <stop offset="100%" stop-color="#02040a"/>
    </linearGradient>
    <linearGradient id="scan" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00ff9c" stop-opacity="0"/>
      <stop offset="50%" stop-color="#00ff9c" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#00ff9c" stop-opacity="0"/>
    </linearGradient>
    <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feGaussianBlur stdDeviation="3.5" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <rect width="1000" height="280" rx="14" fill="url(#bg)"/>
  <rect x="2" y="2" width="996" height="276" rx="12" fill="none" stroke="#00ff9c" stroke-width="1.4" opacity="0.55">
    <animate attributeName="opacity" values="0.25;0.7;0.25" dur="3.2s" repeatCount="indefinite"/>
  </rect>

  <!-- moving scan sweep -->
  <rect x="-200" y="0" width="200" height="280" fill="url(#scan)">
    <animateTransform attributeName="transform" type="translate" values="-200 0; 1000 0; -200 0" dur="6s" repeatCount="indefinite"/>
  </rect>

  <!-- corner brackets, HUD style -->
  <g stroke="#00ff9c" stroke-width="2" opacity="0.9">
    <path d="M22 22 L22 46 M22 22 L46 22" fill="none"/>
    <path d="M978 22 L978 46 M978 22 L954 22" fill="none"/>
    <path d="M22 258 L22 234 M22 258 L46 258" fill="none"/>
    <path d="M978 258 L978 234 M978 258 L954 258" fill="none"/>
  </g>

  <text x="500" y="98" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="13" fill="#00ff9c" letter-spacing="4" opacity="0.8">
    ARCHIVE // HUNTER-CLASS DOSSIER
  </text>

  <text x="500" y="150" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="46" font-weight="700" fill="#eafff0" filter="url(#glow)" letter-spacing="3">
    VARUN SOLANKI
  </text>

  <text x="500" y="184" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="14" fill="#8affc1" letter-spacing="2">
    SHADOW ARCHITECT · AI/ML · CYBERSECURITY · BLOCKCHAIN
  </text>

  <!-- blinking terminal cursor line -->
  <text x="500" y="222" text-anchor="middle" font-family="Share Tech Mono, monospace" font-size="15" fill="#00ff9c">
    <tspan>root@varun</tspan><tspan fill="#5f5f5f">:</tspan><tspan fill="#7d7dff">~</tspan><tspan fill="#5f5f5f">$ </tspan><tspan fill="#eafff0">status --hunter</tspan>
    <tspan fill="#00ff9c">
      <animate attributeName="opacity" values="1;0;1" dur="1s" repeatCount="indefinite"/>
      ▌
    </tspan>
  </text>
</svg>

<br/>

<img src="https://readme-typing-svg.herokuapp.com?font=Share+Tech+Mono&size=15&pause=1000&color=00FF9C&center=true&vCenter=true&width=820&lines=%5BBOOT%5D+neural+interface+online...;%5BID%5D+SHADOW-0001+%C2%B7+rank+S+(ascending);%5BLOG%5D+building+in+silence%2C+shipping+in+public;%5BPROTOCOL%5D+observe+%E2%80%BA+break+%E2%80%BA+rebuild+%E2%80%BA+ascend" alt="typing banner"/>

&nbsp;

[![Visits](https://komarev.com/ghpvc/?username=watashiwa01&style=for-the-badge&color=00ff9c&label=SYSTEM%20PINGS&labelColor=0a0a0a)](https://github.com/watashiwa01)
[![Status](https://img.shields.io/badge/STATUS-TRAINING%20ARC-00ff9c?style=for-the-badge&labelColor=0a0a0a)](#)
[![Rank](https://img.shields.io/badge/RANK-S--CLASS-ff3fa4?style=for-the-badge&labelColor=0a0a0a)](#)

</div>

<br/>

## ⟢ Field Report

> Most people scroll past the dungeon door. I've been leveling inside it — quietly, one commit at a time.

I'm a B.Tech AI/ML student who treats three fields as one discipline: **build intelligent systems, understand how they break, and design the trustless rails they'll eventually run on.** No hype cycle, no follower farming — this profile is a training log, not a highlight reel.

<br/>

## ⟢ The Three Fronts

<div align="center">

<table>
<tr>
<td width="33%" align="center" valign="top">

### 🧠 AI / ML
<sub>neural networks · LLM tooling · applied systems</sub>

```
▰▰▰▰▰▰▰▰▰▰▰▰▰▱▱▱  88%
```

</td>
<td width="33%" align="center" valign="top">

### 🔓 Cybersecurity
<sub>offense theory · defense architecture</sub>

```
▰▰▰▰▰▰▰▰▰▰▰▱▱▱▱▱  75%
```

</td>
<td width="33%" align="center" valign="top">

### ⛓ Blockchain
<sub>smart contracts · DeFi attack surfaces</sub>

```
▰▰▰▰▰▰▰▰▰▱▱▱▱▱▱▱  68%
```

</td>
</tr>
</table>

*The edge isn't any one of these. It's operating at the intersection of all three.*

</div>

<br/>

## ⟢ Live Stat Panel

<!-- animated bars that actually fill in on load -->
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
  <style>
    text{font-family:'Share Tech Mono',monospace;fill:#cfffe0;font-size:13px;}
  </style>

  <text x="0" y="18">AI / ML</text>
  <rect x="0" y="26" width="560" height="14" rx="7" fill="#0d0d0d" stroke="#1e1e1e"/>
  <rect x="0" y="26" height="14" rx="7" fill="url(#bar1)">
    <animate attributeName="width" from="0" to="493" dur="1.6s" fill="freeze" begin="0.1s"/>
  </rect>
  <text x="575" y="38">88%</text>

  <text x="0" y="68">CYBERSECURITY</text>
  <rect x="0" y="76" width="560" height="14" rx="7" fill="#0d0d0d" stroke="#1e1e1e"/>
  <rect x="0" y="76" height="14" rx="7" fill="url(#bar2)">
    <animate attributeName="width" from="0" to="420" dur="1.6s" fill="freeze" begin="0.3s"/>
  </rect>
  <text x="575" y="88">75%</text>

  <text x="0" y="118">BLOCKCHAIN</text>
  <rect x="0" y="126" width="560" height="14" rx="7" fill="#0d0d0d" stroke="#1e1e1e"/>
  <rect x="0" y="126" height="14" rx="7" fill="url(#bar3)">
    <animate attributeName="width" from="0" to="381" dur="1.6s" fill="freeze" begin="0.5s"/>
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
root@varun:~$ cat manifesto.txt

  I study foundations, not trends.
  In security, think like the attacker to build the defender.
  In blockchain, trustless systems are just trust — redesigned.
  In AI, the amplifier is only as good as the mind behind it.

  Three domains. One operator. Compounding edge.

root@varun:~$ ping future.io
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

<sub>The strongest hunters don't announce their power level — they just keep clearing floors.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:001a0f,100:02040a&section=footer"/>

</div>
