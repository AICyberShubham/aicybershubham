<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Shubham Kumar Pandey | AI &amp; Cybersecurity</title>
<meta name="description" content="First-year BS student in AI & Cybersecurity at IIT Patna. Building LLM agents, WebXR and IoT projects.">
<style>
:root{--bg:#070a14;--ink:#0a0e1a;--pan:#121829;--ln:#252d47;--tx:#e8ecf7;--t2:#b8c0d9;--mu:#8b94b0;--am:#ffb454;--te:#2dd4bf;--pe:#8b9cff;--on:#0a0e1a}
@media(prefers-color-scheme:light){:root{--bg:#eef1f8;--ink:#fff;--pan:#f3f5fb;--ln:#d9deee;--tx:#0f1530;--t2:#38405f;--mu:#5b6482;--am:#b45309;--te:#0f766e;--pe:#4f46e5;--on:#fff}}
*{box-sizing:border-box;margin:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--tx);font:16px/1.6 "Segoe UI",system-ui,-apple-system,Roboto,Helvetica,Arial,sans-serif}
a{color:inherit}
:focus-visible{outline:2px solid var(--am);outline-offset:3px}
.wrap{max-width:1040px;margin:0 auto;padding:0 24px}
nav{position:sticky;top:0;z-index:5;background:color-mix(in srgb,var(--bg) 85%,transparent);backdrop-filter:blur(10px);border-bottom:1px solid var(--ln)}
nav .wrap{display:flex;align-items:center;justify-content:space-between;height:56px}
nav ul{display:flex;gap:22px;list-style:none;padding:0;font-size:14px;color:var(--t2)}
nav a{text-decoration:none}nav a:hover{color:var(--am)}
.hero{display:grid;grid-template-columns:1.2fr .8fr;gap:32px;align-items:center;padding:72px 0 48px}
h1{font-size:clamp(36px,6vw,58px);line-height:1.05;letter-spacing:-.03em;font-weight:800}
.lead{margin-top:18px;font-size:19px;color:var(--t2);max-width:32em}
.roles{position:relative;height:1.8em;margin-top:20px;font:15px/1.8 ui-monospace,"JetBrains Mono",Consolas,monospace}
.roles::before{content:">";color:var(--am);margin-right:10px}
.roles span{position:absolute;left:22px;white-space:nowrap;opacity:0;animation:cyc 12s infinite}
.roles span:nth-child(2){animation-delay:3s}.roles span:nth-child(3){animation-delay:6s}.roles span:nth-child(4){animation-delay:9s}
.status{display:inline-flex;gap:8px;align-items:center;margin-top:20px;padding:6px 14px;border:1px solid color-mix(in srgb,var(--te) 50%,transparent);border-radius:99px;color:var(--te);font-size:14px;font-weight:600;background:color-mix(in srgb,var(--te) 10%,transparent)}
.status::before{content:"";width:8px;height:8px;border-radius:50%;background:var(--te);animation:pulse 2s infinite}
.cta{display:flex;flex-wrap:wrap;gap:10px;margin-top:26px}
.btn{padding:10px 18px;border:1px solid var(--ln);border-radius:12px;text-decoration:none;font-weight:600;font-size:15px;background:var(--ink)}
.btn:hover{border-color:var(--am)}
.btn.pri{background:var(--am);color:var(--on);border-color:var(--am)}
.radar{width:100%;max-width:380px;justify-self:center}
.radar text{font:11px ui-monospace,Consolas,monospace;fill:var(--mu)}
.sweep{transform-origin:160px 160px;animation:spin 7s linear infinite}
.blip{animation:ping 7s infinite;animation-delay:var(--d)}
section{padding:44px 0}
h2{font-size:28px;letter-spacing:-.02em}
.desc{color:var(--mu);margin:4px 0 22px}
.box{background:var(--ink);border:1px solid var(--ln);border-radius:16px}
.term header{display:flex;gap:7px;padding:14px 18px;background:var(--pan);border-bottom:1px solid var(--ln);border-radius:16px 16px 0 0}
.term header i{width:11px;height:11px;border-radius:50%}
pre{padding:20px 24px;font:14.5px/1.8 ui-monospace,"JetBrains Mono",Consolas,monospace;overflow-x:auto;color:var(--t2)}
.k{color:var(--am)}.c{color:var(--tx)}.m{color:var(--mu)}
.row{display:grid;grid-template-columns:200px 1fr;gap:12px;padding:16px 24px;border-top:1px solid var(--ln);align-items:center}
.row:first-child{border:0}
dt{font-weight:600;color:var(--t2);font-size:14px}
.tags{display:flex;flex-wrap:wrap;gap:8px;list-style:none;padding:0}
.tags li{padding:5px 12px;border:1px solid var(--ln);border-radius:8px;background:var(--pan);font-size:13.5px}
.tags li::before{content:"";display:inline-block;width:7px;height:7px;border-radius:50%;background:var(--c,var(--pe));margin-right:8px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:20px}
.card{position:relative;padding:24px;display:flex;flex-direction:column}
.card::before{content:"";position:absolute;top:0;left:24px;width:56px;height:3px;background:var(--c);border-radius:0 0 3px 3px}
.pill{align-self:flex-end;font-size:12px;font-weight:600;color:var(--c);border:1px solid color-mix(in srgb,var(--c) 50%,transparent);background:color-mix(in srgb,var(--c) 10%,transparent);padding:3px 12px;border-radius:99px}
h3{font-size:21px;margin-top:8px}
.sub{color:var(--mu);font-size:14px}
.d{color:var(--t2);font-size:14.5px;margin:12px 0 16px;flex:1}
.more{border-style:dashed;align-items:center;justify-content:center;text-align:center;text-decoration:none;gap:6px;min-height:200px}
.certs{list-style:none;padding:0}
.certs li{display:flex;gap:14px;align-items:center;padding:14px 24px;border-top:1px solid var(--ln)}
.certs li:first-child{border:0}
.ck{flex:none;width:26px;height:26px;border-radius:50%;display:grid;place-items:center;color:var(--te);border:1px solid color-mix(in srgb,var(--te) 50%,transparent);background:color-mix(in srgb,var(--te) 10%,transparent);font-size:13px}
small{display:block;color:var(--mu);font-size:13px}
footer{margin-top:24px;padding:40px 0 56px;border-top:1px solid var(--ln);text-align:center;color:var(--t2)}
footer b{display:block;font-size:18px;letter-spacing:.04em;color:var(--tx);margin-bottom:12px}
footer a{margin:0 10px;font-size:14px}
@keyframes cyc{0%{opacity:0;transform:translateY(8px)}4%,22%{opacity:1;transform:none}26%,100%{opacity:0;transform:translateY(-8px)}}
@keyframes spin{to{transform:rotate(360deg)}}
@keyframes ping{0%{opacity:1}45%,100%{opacity:.2}}
@keyframes pulse{50%{opacity:.3}}
@media(max-width:760px){.hero{grid-template-columns:1fr;padding-top:40px}.radar{max-width:260px;order:-1}.row{grid-template-columns:1fr;gap:8px}nav ul{display:none}}
@media(prefers-reduced-motion:reduce){*{animation:none!important}.roles span:first-child{opacity:1}}
</style>
</head>
<body>
<nav><div class="wrap"><b>Shubham Kumar Pandey</b>
<ul><li><a href="#about">About</a></li><li><a href="#stack">Tech stack</a></li><li><a href="#projects">Projects</a></li><li><a href="#certs">Certificates</a></li></ul></div></nav>

<main class="wrap">
<div class="hero">
  <div>
    <h1>Shubham Kumar Pandey</h1>
    <p class="lead">BS in AI &amp; Cybersecurity at IIT Patna, and B.Tech in Information Technology at REC Mirzapur.</p>
    <div class="roles" aria-label="Currently: building LLM agents, exploring AI security, making WebXR and IoT prototypes, learning ML and DSA">
      <span>building LLM agents with tool-calling</span><span>exploring AI &amp; agent security</span><span>making WebXR and IoT prototypes</span><span>learning ML, DSA and Java</span>
    </div>
    <div class="status">Open to a winter internship</div>
    <div class="cta">
      <a class="btn pri" href="https://shubhampandey.dev">Portfolio</a>
      <a class="btn" href="https://www.linkedin.com/in/shubham-kumar-pandey-iitp/">LinkedIn</a>
      <a class="btn" href="https://github.com/AICyberShubham">GitHub</a>
      <a class="btn" href="mailto:shubhamkpandey009@gmail.com">Email</a>
    </div>
  </div>
  <svg class="radar" viewBox="0 0 320 320" role="img" aria-label="Radar sweep with subfinder, nmap and httpx blips">
    <g fill="none" stroke="var(--ln)"><circle cx="160" cy="160" r="50"/><circle cx="160" cy="160" r="100"/><circle cx="160" cy="160" r="150"/><path d="M10 160H310M160 10V310" stroke-dasharray="2 6"/></g>
    <g class="sweep"><path d="M160 160L310 160A150 150 0 0 0 266 54Z" fill="var(--am)" opacity=".14"/><path d="M160 160H310" stroke="var(--am)" stroke-width="1.5"/></g>
    <g class="blip" style="--d:.3s"><circle cx="257" cy="186" r="9" fill="none" stroke="var(--am)" opacity=".4"/><circle cx="257" cy="186" r="3.5" fill="var(--am)"/><text x="271" y="190">subfinder</text></g>
    <g class="blip" style="--d:2.7s"><circle cx="103" cy="208" r="9" fill="none" stroke="var(--am)" opacity=".4"/><circle cx="103" cy="208" r="3.5" fill="var(--am)"/><text x="117" y="212">nmap</text></g>
    <g class="blip" style="--d:4.9s"><circle cx="119" cy="47" r="9" fill="none" stroke="var(--am)" opacity=".4"/><circle cx="119" cy="47" r="3.5" fill="var(--am)"/><text x="133" y="51">httpx</text></g>
    <circle cx="160" cy="160" r="3" fill="var(--tx)"/>
  </svg>
</div>

<section id="about">
  <h2>About</h2><p class="desc">Where I study and what I am working towards.</p>
  <div class="box term"><header><i style="background:#ff6b6b"></i><i style="background:var(--am)"></i><i style="background:var(--te)"></i></header>
<pre><span class="k">$</span> <span class="c">whoami</span>
  Shubham Kumar Pandey, first-year student in AI &amp; Cybersecurity
<span class="k">$</span> <span class="c">cat education.txt</span>
  BS in AI &amp; Cybersecurity       IIT Patna                  2026 - 2029
  B.Tech in Information Tech     Samrat Ashok REC, Mirzapur 2026 - 2030
<span class="k">$</span> <span class="c">cat focus.txt</span>
  LLM agents, tool-calling, RAG, MCP, AI and agent security
<span class="k">$</span> <span class="c">cat now.txt</span>
  <span class="m">learning</span>  Python, Machine Learning, DSA, Java
  <span class="m">building</span>  Rekonix, an AI agent that uses recon tools
<span class="k">$</span> <span class="c">cat looking_for.txt</span>
  On-campus winter internship or residential program at an IIT or NIT</pre></div>
</section>

<section id="stack">
  <h2>Tech stack</h2><p class="desc">Tools I use and what I am learning.</p>
  <dl class="box">
    <div class="row"><dt>Languages</dt><dd><ul class="tags"><li>Python</li><li>C</li><li>JavaScript</li><li>HTML5</li><li>CSS3</li></ul></dd></div>
    <div class="row"><dt>Backend and tools</dt><dd><ul class="tags"><li>FastAPI</li><li>Git</li><li>GitHub</li><li>Linux</li></ul></dd></div>
    <div class="row"><dt>AI and GenAI</dt><dd><ul class="tags" style="--c:var(--am)"><li>LLM APIs</li><li>LangChain</li><li>LangGraph</li><li>RAG</li><li>MCP</li><li>Claude API</li></ul></dd></div>
    <div class="row"><dt>XR and IoT</dt><dd><ul class="tags" style="--c:var(--te)"><li>A-Frame</li><li>WebXR</li><li>ESP32</li><li>Blynk</li></ul></dd></div>
    <div class="row"><dt>Currently learning</dt><dd><ul class="tags" style="--c:var(--mu)"><li>Machine Learning</li><li>Java</li><li>Data Structures &amp; Algorithms</li></ul></dd></div>
  </dl>
</section>

<section id="projects">
  <h2>Projects</h2><p class="desc">Solo and team builds. Amber is AI, teal is XR and IoT, blue is web.</p>
  <div class="grid">
    <article class="box card" style="--c:var(--am)"><span class="pill">Early stage</span><h3>Rekonix</h3><p class="sub">AI agent that uses tools</p>
      <p class="d">Calls recon tools (subfinder, nmap, httpx) through the Claude API and puts their results together. Focus: tool-calling and agent design.</p>
      <ul class="tags"><li>Python</li><li>FastAPI</li><li>Claude API</li></ul></article>
    <article class="box card" style="--c:var(--te)"><span class="pill">SIH 2026</span><h3>3D ULPIN</h3><p class="sub">Vertical Property Mapping</p>
      <p class="d">Links land parcel, ULPIN, building, floors and units in one 3D view. Demo built with simple LOD-1 building models and WebXR.</p>
      <ul class="tags"><li>3D GIS</li><li>LOD-1</li><li>WebXR</li></ul></article>
    <article class="box card" style="--c:var(--te)"><span class="pill">YISL workshop</span><h3>Nalanda Mahavihara</h3><p class="sub">Virtual Reconstruction, Team CAMPER X</p>
      <p class="d">WebXR VR experience of ancient Nalanda, built with A-Frame and GLB 3D models and tested on a Meta Quest 3S.</p>
      <ul class="tags"><li>A-Frame</li><li>WebXR</li><li>GLB</li><li>Quest 3S</li></ul></article>
    <article class="box card" style="--c:var(--te)"><span class="pill">Lab project</span><h3>Auto Solar Tracker</h3><p class="sub">with IoT Monitoring, team of 4</p>
      <p class="d">Dual-axis prototype: 4 LDR sensors and 2 servos turn the panel towards light. My part: ESP32 code, tracking logic, Blynk, docs and presentation.</p>
      <ul class="tags"><li>ESP32</li><li>LDR</li><li>Servo</li><li>Blynk</li></ul></article>
    <article class="box card" style="--c:var(--pe)"><span class="pill">Capstone</span><h3>CSE Department Website</h3><p class="sub">IIT Patna, Capstone-I, team of 4</p>
      <p class="d">Department website built as a team. My part: managing the GitHub repo, joining my teammates’ pages and hosting on GitHub Pages.</p>
      <ul class="tags"><li>HTML</li><li>CSS</li><li>JavaScript</li><li>GitHub Pages</li></ul></article>
    <a class="box card more" style="--c:var(--am)" href="https://github.com/AICyberShubham?tab=repositories"><h3>See every repository</h3><p class="sub">github.com/AICyberShubham</p></a>
  </div>
</section>

<section id="certs">
  <h2>Certificates</h2><p class="desc">Courses and workshops.</p>
  <ul class="box certs">
    <li><span class="ck">✓</span><div><b>Programming with Generative AI</b><small>IIT Guwahati, Feb 2025 to Sep 2025</small></div></li>
    <li><span class="ck">✓</span><div><b>Complete Agentic AI Bootcamp with LangGraph and LangChain</b><small>Udemy</small></div></li>
    <li><span class="ck">✓</span><div><b>Master Python Programming from Scratch</b></div></li>
    <li><span class="ck">✓</span><div><b>AR/VR Workshop</b><small>Young Innovators STEM Lab (YISL), IIT Patna, Sep 2026</small></div></li>
  </ul>
</section>
</main>

<footer><b>Learning • Building • Breaking</b>
<a href="https://shubhampandey.dev">Portfolio</a><a href="https://www.linkedin.com/in/shubham-kumar-pandey-iitp/">LinkedIn</a><a href="https://github.com/AICyberShubham">GitHub</a><a href="mailto:shubhamkpandey009@gmail.com">Email</a></footer>
</body>
</html>
