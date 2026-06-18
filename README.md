<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Shubham Kumar Pandey — AI Security Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
<style>
  /* ── TOKENS ─────────────────────────────────────────────────── */
  :root {
    --bg:        #080b0f;
    --surface:   #0d1117;
    --surface2:  #111820;
    --border:    #1e2d3d;
    --green:     #00ff88;
    --green-dim: #00ff8840;
    --green-glow:#00ff8815;
    --cyan:      #00d4ff;
    --red:       #ff4b4b;
    --text:      #c9d1d9;
    --muted:     #586069;
    --white:     #f0f6fc;
    --mono:      'JetBrains Mono', monospace;
    --sans:      'Space Grotesk', sans-serif;
  }

  /* ── RESET ──────────────────────────────────────────────────── */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }
  a { color: inherit; text-decoration: none; }

  /* ── SCANLINE OVERLAY ───────────────────────────────────────── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,255,136,0.015) 2px,
      rgba(0,255,136,0.015) 4px
    );
    pointer-events: none;
    z-index: 9999;
  }

  /* ── NOISE TEXTURE ──────────────────────────────────────────── */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.03'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9998;
    opacity: 0.4;
  }

  /* ── LAYOUT ─────────────────────────────────────────────────── */
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 24px;
  }

  section { padding: 80px 0; }

  /* ── NAV ─────────────────────────────────────────────────────── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 16px 24px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(8,11,15,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--green);
    letter-spacing: 0.05em;
  }

  .nav-logo span { color: var(--muted); }

  .nav-links {
    display: flex;
    gap: 28px;
    list-style: none;
  }

  .nav-links a {
    font-family: var(--mono);
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 0.08em;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--green); }

  /* ── HERO ─────────────────────────────────────────────────────── */
  #hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding-top: 80px;
    position: relative;
  }

  .hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
    width: 100%;
  }

  .hero-left {}

  .hero-tag {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--green);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .hero-tag::before {
    content: '';
    width: 24px;
    height: 1px;
    background: var(--green);
  }

  h1 {
    font-family: var(--sans);
    font-size: clamp(36px, 5vw, 52px);
    font-weight: 700;
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 8px;
  }

  .hero-subtitle {
    font-family: var(--mono);
    font-size: 15px;
    color: var(--green);
    margin-bottom: 20px;
  }

  .hero-desc {
    font-size: 15px;
    color: var(--muted);
    line-height: 1.7;
    margin-bottom: 36px;
    max-width: 420px;
  }

  .hero-cta {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }

  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 11px 22px;
    background: var(--green);
    color: #000;
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.08em;
    border: none;
    cursor: pointer;
    transition: all 0.2s;
    clip-path: polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 8px 100%, 0 calc(100% - 8px));
  }

  .btn-primary:hover {
    background: #00ffaa;
    transform: translateY(-1px);
    box-shadow: 0 4px 20px var(--green-dim);
  }

  .btn-ghost {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 11px 22px;
    border: 1px solid var(--border);
    color: var(--text);
    font-family: var(--mono);
    font-size: 12px;
    letter-spacing: 0.08em;
    cursor: pointer;
    transition: all 0.2s;
    background: transparent;
  }

  .btn-ghost:hover {
    border-color: var(--green);
    color: var(--green);
  }

  /* ── TERMINAL ─────────────────────────────────────────────────── */
  .terminal {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    overflow: hidden;
    font-family: var(--mono);
    box-shadow: 0 0 60px rgba(0,255,136,0.06), 0 20px 60px rgba(0,0,0,0.5);
  }

  .terminal-bar {
    background: var(--surface2);
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 8px;
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-red    { background: #ff5f57; }
  .dot-yellow { background: #febc2e; }
  .dot-green  { background: #28c840; }

  .terminal-title {
    margin-left: 8px;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  .terminal-body {
    padding: 20px;
    font-size: 12.5px;
    line-height: 1.9;
  }

  .t-prompt { color: var(--green); }
  .t-cmd    { color: var(--white); }
  .t-key    { color: var(--cyan); }
  .t-val    { color: #e3b341; }
  .t-str    { color: #a5d6ff; }
  .t-comment{ color: var(--muted); }
  .t-output { color: var(--text); }
  .t-cursor {
    display: inline-block;
    width: 8px; height: 14px;
    background: var(--green);
    vertical-align: text-bottom;
    animation: blink 1.2s step-end infinite;
  }

  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* ── SECTION HEADER ──────────────────────────────────────────── */
  .section-header {
    margin-bottom: 48px;
  }

  .section-label {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--green);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .section-title {
    font-size: 28px;
    font-weight: 700;
    color: var(--white);
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
    max-width: 300px;
  }

  /* ── ABOUT ───────────────────────────────────────────────────── */
  #about { border-top: 1px solid var(--border); }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
    align-items: start;
  }

  .about-text p {
    color: var(--text);
    font-size: 15px;
    line-height: 1.75;
    margin-bottom: 16px;
  }

  .about-text p:last-child { margin-bottom: 0; }

  .about-text strong { color: var(--white); }

  .stat-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 20px;
    transition: border-color 0.2s;
  }

  .stat-card:hover { border-color: var(--green); }

  .stat-num {
    font-family: var(--mono);
    font-size: 28px;
    font-weight: 700;
    color: var(--green);
    line-height: 1;
    margin-bottom: 4px;
  }

  .stat-label {
    font-size: 12px;
    color: var(--muted);
  }

  /* ── SKILLS ──────────────────────────────────────────────────── */
  #skills { border-top: 1px solid var(--border); }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
  }

  .skill-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 24px;
    transition: all 0.2s;
    position: relative;
    overflow: hidden;
  }

  .skill-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 0;
    background: var(--green);
    transition: height 0.3s ease;
  }

  .skill-card:hover { border-color: var(--border); transform: translateY(-2px); }
  .skill-card:hover::before { height: 100%; }

  .skill-icon {
    font-size: 22px;
    margin-bottom: 12px;
  }

  .skill-name {
    font-family: var(--mono);
    font-size: 13px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 8px;
    letter-spacing: 0.05em;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .tag {
    font-family: var(--mono);
    font-size: 10px;
    padding: 3px 8px;
    border: 1px solid var(--border);
    color: var(--muted);
    letter-spacing: 0.06em;
  }

  /* ── PROGRESS BARS ───────────────────────────────────────────── */
  .progress-section {
    margin-top: 40px;
  }

  .progress-title {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--green);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 20px;
  }

  .progress-item {
    margin-bottom: 16px;
  }

  .progress-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 6px;
  }

  .progress-name {
    font-family: var(--mono);
    font-size: 12px;
    color: var(--text);
  }

  .progress-pct {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
  }

  .progress-track {
    height: 3px;
    background: var(--border);
    position: relative;
    overflow: hidden;
  }

  .progress-fill {
    height: 100%;
    background: var(--green);
    position: relative;
    transition: width 1.5s cubic-bezier(0.4,0,0.2,1);
    width: 0;
  }

  .progress-fill.loaded { width: var(--w); }

  .progress-fill::after {
    content: '';
    position: absolute;
    right: 0; top: 0; bottom: 0;
    width: 20px;
    background: linear-gradient(to right, transparent, rgba(0,255,136,0.6));
  }

  /* ── PROJECTS ────────────────────────────────────────────────── */
  #projects { border-top: 1px solid var(--border); }

  .projects-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 16px;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 28px 32px;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 16px;
    align-items: start;
    transition: all 0.2s;
    cursor: default;
    position: relative;
  }

  .project-card:hover {
    border-color: var(--green);
    background: var(--surface2);
    transform: translateX(4px);
  }

  .project-num {
    font-family: var(--mono);
    font-size: 10px;
    color: var(--green);
    letter-spacing: 0.1em;
    margin-bottom: 8px;
  }

  .project-name {
    font-size: 17px;
    font-weight: 600;
    color: var(--white);
    margin-bottom: 8px;
  }

  .project-desc {
    font-size: 14px;
    color: var(--muted);
    line-height: 1.6;
    margin-bottom: 16px;
  }

  .project-stack {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
  }

  .stack-tag {
    font-family: var(--mono);
    font-size: 10px;
    padding: 3px 10px;
    background: var(--green-glow);
    border: 1px solid var(--green-dim);
    color: var(--green);
    letter-spacing: 0.06em;
  }

  .project-arrow {
    font-size: 20px;
    color: var(--border);
    transition: color 0.2s;
    align-self: center;
  }

  .project-card:hover .project-arrow { color: var(--green); }

  /* ── CERTS ───────────────────────────────────────────────────── */
  #certs { border-top: 1px solid var(--border); }

  .cert-list {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .cert-item {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 18px 20px;
    background: var(--surface);
    border: 1px solid var(--border);
    transition: border-color 0.2s;
  }

  .cert-item:hover { border-color: var(--green); }

  .cert-check {
    font-family: var(--mono);
    font-size: 13px;
    color: var(--green);
    margin-top: 1px;
    flex-shrink: 0;
  }

  .cert-name {
    font-size: 13px;
    color: var(--text);
    line-height: 1.4;
  }

  /* ── CONTACT ─────────────────────────────────────────────────── */
  #contact { border-top: 1px solid var(--border); }

  .contact-inner {
    text-align: center;
    max-width: 560px;
    margin: 0 auto;
  }

  .contact-inner h2 {
    font-size: 36px;
    font-weight: 700;
    color: var(--white);
    margin-bottom: 12px;
  }

  .contact-inner p {
    color: var(--muted);
    font-size: 15px;
    margin-bottom: 36px;
    line-height: 1.7;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 16px;
    flex-wrap: wrap;
  }

  .contact-link {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border: 1px solid var(--border);
    font-family: var(--mono);
    font-size: 12px;
    color: var(--text);
    letter-spacing: 0.06em;
    transition: all 0.2s;
  }

  .contact-link:hover {
    border-color: var(--green);
    color: var(--green);
    background: var(--green-glow);
  }

  .contact-link svg {
    width: 14px; height: 14px;
    fill: currentColor;
  }

  /* ── FOOTER ──────────────────────────────────────────────────── */
  footer {
    border-top: 1px solid var(--border);
    padding: 24px 0;
  }

  .footer-inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-copy {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
  }

  .footer-copy span { color: var(--green); }

  .footer-status {
    display: flex;
    align-items: center;
    gap: 8px;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--muted);
  }

  .status-dot {
    width: 6px; height: 6px;
    background: var(--green);
    border-radius: 50%;
    animation: pulse 2s ease-in-out infinite;
  }

  @keyframes pulse {
    0%,100% { box-shadow: 0 0 0 0 rgba(0,255,136,0.4); }
    50%      { box-shadow: 0 0 0 5px rgba(0,255,136,0); }
  }

  /* ── AMBIENT GLOW ────────────────────────────────────────────── */
  .glow-orb {
    position: fixed;
    border-radius: 50%;
    pointer-events: none;
    filter: blur(80px);
    z-index: 0;
  }

  .glow-1 {
    width: 400px; height: 400px;
    background: rgba(0,255,136,0.04);
    top: -100px; right: -100px;
  }

  .glow-2 {
    width: 300px; height: 300px;
    background: rgba(0,212,255,0.03);
    bottom: 200px; left: -80px;
  }

  /* ── SCROLL REVEAL ───────────────────────────────────────────── */
  .reveal {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }

  .reveal.visible {
    opacity: 1;
    transform: none;
  }

  /* ── RESPONSIVE ──────────────────────────────────────────────── */
  @media (max-width: 720px) {
    .hero-grid    { grid-template-columns: 1fr; gap: 40px; }
    .about-grid   { grid-template-columns: 1fr; }
    .skills-grid  { grid-template-columns: 1fr; }
    .cert-list    { grid-template-columns: 1fr; }
    .stat-grid    { grid-template-columns: 1fr 1fr; }
    .project-card { grid-template-columns: 1fr; }
    .nav-links    { display: none; }
    h1            { font-size: 32px; }
    section       { padding: 60px 0; }
  }

  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after { animation: none !important; transition: none !important; }
  }
</style>
</head>
<body>

<!-- Ambient orbs -->
<div class="glow-orb glow-1"></div>
<div class="glow-orb glow-2"></div>

<!-- ── NAV ──────────────────────────────────────────────────────── -->
<nav>
  <div class="nav-logo"><span>~/</span>shubham<span>.dev</span></div>
  <ul class="nav-links">
    <li><a href="#about">about</a></li>
    <li><a href="#skills">skills</a></li>
    <li><a href="#projects">projects</a></li>
    <li><a href="#certs">certs</a></li>
    <li><a href="#contact">contact</a></li>
  </ul>
</nav>

<!-- ── HERO ─────────────────────────────────────────────────────── -->
<section id="hero">
  <div class="container">
    <div class="hero-grid">

      <div class="hero-left">
        <div class="hero-tag">AI × Security</div>
        <h1>Shubham Kumar Pandey</h1>
        <div class="hero-subtitle">> AI Security Engineer_</div>
        <p class="hero-desc">
          First-year at IIT Patna — BS AI & Cybersecurity.<br>
          Building at the intersection of <strong style="color:var(--white)">LLM Security</strong>,
          <strong style="color:var(--white)">Red Teaming</strong>, and
          <strong style="color:var(--white)">AI Agents</strong>.<br>
          Breaking things to understand them.
        </p>
        <div class="hero-cta">
          <a class="btn-primary" href="#projects">view work ↗</a>
          <a class="btn-ghost" href="mailto:shubhamkpandey009@gmail.com">get in touch</a>
        </div>
      </div>

      <div class="hero-right">
        <div class="terminal">
          <div class="terminal-bar">
            <div class="dot dot-red"></div>
            <div class="dot dot-yellow"></div>
            <div class="dot dot-green"></div>
            <span class="terminal-title">shubham@iit-patna ~ zsh</span>
          </div>
          <div class="terminal-body">
<span class="t-prompt">shubham@iit-patna</span><span class="t-cmd"> ~ </span><span class="t-prompt">$</span> <span class="t-cmd">python3 whoami.py</span><br>
<br>
<span class="t-key">class</span> <span class="t-val">Shubham</span><span class="t-cmd">:</span><br>
&nbsp;&nbsp;<span class="t-key">role</span>     <span class="t-cmd">=</span> <span class="t-str">"AI Security Engineer"</span><br>
&nbsp;&nbsp;<span class="t-key">college</span>  <span class="t-cmd">=</span> <span class="t-str">"IIT Patna"</span><br>
&nbsp;&nbsp;<span class="t-key">focus</span>    <span class="t-cmd">=</span> <span class="t-str">["LLM Security"</span><span class="t-cmd">,</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class="t-str">"Red Teaming"</span><span class="t-cmd">,</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class="t-str">"AI Agents"</span><span class="t-cmd">,</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class="t-str">"Cloud IAM"</span><span class="t-cmd">]</span><br>
&nbsp;&nbsp;<span class="t-key">status</span>   <span class="t-cmd">=</span> <span class="t-str">"building + breaking"</span><br>
<br>
<span class="t-comment"># Currently learning</span><br>
<span class="t-prompt">></span> <span class="t-cmd">LangChain · LangGraph · Multi-Agent</span><br>
<span class="t-prompt">></span> <span class="t-cmd">Prompt Injection · Jailbreak Research</span><br>
<span class="t-prompt">></span> <span class="t-cmd">AWS IAM · Cloud Attack Paths</span><br>
<br>
<span class="t-prompt">shubham@iit-patna</span><span class="t-cmd"> ~ </span><span class="t-prompt">$</span> <span class="t-cursor"></span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ── ABOUT ─────────────────────────────────────────────────────── -->
<section id="about">
  <div class="container">
    <div clas
