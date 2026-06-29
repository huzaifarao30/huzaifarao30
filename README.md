<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Huzaifa Sikandar Rao</title>
<link href="https://fonts.googleapis.com/css2?family=Bangers&family=Rajdhani:wght@400;600;700&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  background: #05000f;
  color: #e8e0ff;
  font-family: 'Rajdhani', sans-serif;
  min-height: 100vh;
  overflow-x: hidden;
  position: relative;
}

.bg-canvas {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  pointer-events: none;
  z-index: 0;
}

.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(60px);
  animation: floatOrb 8s ease-in-out infinite;
  opacity: 0.35;
}
.orb1 { width: 300px; height: 300px; background: #7000ff; top: -100px; left: -100px; animation-delay: 0s; }
.orb2 { width: 200px; height: 200px; background: #ff4400; top: 30%; right: -80px; animation-delay: 2s; }
.orb3 { width: 250px; height: 250px; background: #0099ff; bottom: 10%; left: 20%; animation-delay: 4s; }
.orb4 { width: 180px; height: 180px; background: #ff0066; bottom: 20%; right: 10%; animation-delay: 1s; }

@keyframes floatOrb {
  0%, 100% { transform: translateY(0px) scale(1); }
  50% { transform: translateY(-30px) scale(1.1); }
}

.speed-lines {
  position: fixed;
  top: 50%; left: 50%;
  width: 200%; height: 200%;
  transform: translate(-50%, -50%);
  pointer-events: none;
  z-index: 0;
  opacity: 0.03;
}

.content { position: relative; z-index: 10; padding: 0 0 40px; max-width: 680px; margin: 0 auto; }

.hero {
  position: relative;
  padding: 40px 30px 30px;
  text-align: center;
  border-bottom: 1px solid rgba(112, 0, 255, 0.3);
}

.manga-frame {
  display: inline-block;
  position: relative;
  margin-bottom: 8px;
}
.manga-frame::before, .manga-frame::after {
  content: '';
  position: absolute;
  top: 0; bottom: 0;
  width: 4px;
  background: linear-gradient(180deg, #ff6b00, #7000ff, #ff6b00);
  animation: energyPulse 2s ease-in-out infinite;
}
.manga-frame::before { left: -14px; }
.manga-frame::after { right: -14px; }

@keyframes energyPulse {
  0%, 100% { opacity: 1; box-shadow: 0 0 8px #ff6b00; }
  50% { opacity: 0.6; box-shadow: 0 0 20px #7000ff; }
}

.hero-name {
  font-family: 'Bangers', cursive;
  font-size: 52px;
  letter-spacing: 3px;
  background: linear-gradient(90deg, #ff6b00, #ffffff, #7000ff, #ff6b00);
  background-size: 300%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: shimmer 4s linear infinite;
  line-height: 1;
}
@keyframes shimmer {
  0% { background-position: 0% 50%; }
  100% { background-position: 300% 50%; }
}

.hero-title {
  font-family: 'Share Tech Mono', monospace;
  font-size: 12px;
  color: #ff6b00;
  letter-spacing: 4px;
  text-transform: uppercase;
  margin: 6px 0 16px;
  animation: blink 3s ease-in-out infinite;
}
@keyframes blink {
  0%, 90%, 100% { opacity: 1; }
  95% { opacity: 0.3; }
}

.power-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(112, 0, 255, 0.15);
  border: 1px solid rgba(112, 0, 255, 0.5);
  border-radius: 20px;
  padding: 5px 16px;
  font-size: 12px;
  font-family: 'Share Tech Mono', monospace;
  color: #c084fc;
  animation: borderGlow 2s ease-in-out infinite;
  margin: 0 4px;
}
@keyframes borderGlow {
  0%, 100% { border-color: rgba(112,0,255,0.5); box-shadow: 0 0 10px rgba(112,0,255,0.2); }
  50% { border-color: rgba(255,107,0,0.8); box-shadow: 0 0 20px rgba(255,107,0,0.3); }
}

.dot-online { width: 7px; height: 7px; border-radius: 50%; background: #22c55e; animation: pulse 1.5s infinite; display:inline-block; }
@keyframes pulse { 0%,100%{box-shadow:0 0 0 0 rgba(34,197,94,0.6)} 50%{box-shadow:0 0 0 5px rgba(34,197,94,0)} }

.spirit-meter {
  display: flex;
  align-items: center;
  gap: 3px;
  justify-content: center;
  margin: 16px 0 0;
}
.spirit-block {
  width: 18px;
  height: 8px;
  border-radius: 2px;
  background: #ff6b00;
  animation: spiritFlicker 0.8s ease-in-out infinite;
}
.spirit-block:nth-child(2) { animation-delay: 0.1s; background: #ff4400; }
.spirit-block:nth-child(3) { animation-delay: 0.2s; background: #cc00ff; }
.spirit-block:nth-child(4) { animation-delay: 0.3s; background: #7000ff; }
.spirit-block:nth-child(5) { animation-delay: 0.4s; background: #0099ff; }
.spirit-block:nth-child(6) { animation-delay: 0.5s; background: #00ccff; }
.spirit-block:nth-child(7) { animation-delay: 0.6s; background: #22c55e; }
@keyframes spiritFlicker {
  0%,100% { opacity: 1; transform: scaleY(1); }
  50% { opacity: 0.6; transform: scaleY(0.7); }
}

.char-card {
  margin: 24px 20px 0;
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(112,0,255,0.25);
  border-radius: 12px;
  overflow: hidden;
  position: relative;
}
.char-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 2px;
  background: linear-gradient(90deg, transparent, #ff6b00, #7000ff, #ff6b00, transparent);
  animation: scanLine 3s linear infinite;
  background-size: 200%;
}
@keyframes scanLine {
  0% { background-position: -200% 0; }
  100% { background-position: 200% 0; }
}

.card-header {
  background: rgba(112,0,255,0.08);
  border-bottom: 1px solid rgba(112,0,255,0.2);
  padding: 10px 16px;
  display: flex;
  align-items: center;
  gap: 8px;
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: #7000ff;
  text-transform: uppercase;
  letter-spacing: 2px;
}
.card-dot { width: 8px; height: 8px; border-radius: 50%; }
.dot-r { background: #ff4444; }
.dot-y { background: #ffaa00; }
.dot-g { background: #44ff88; }

.code-block {
  padding: 16px;
  font-family: 'Share Tech Mono', monospace;
  font-size: 12px;
  line-height: 1.8;
  color: #c9d1d9;
}
.ck { color: #c084fc; }
.cs { color: #7dd3fc; }
.cc { color: #6b7280; }
.cn { color: #ff6b00; }
.cp { color: #34d399; }

.sec-label {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 24px 20px 12px;
}
.sec-label-text {
  font-family: 'Bangers', cursive;
  font-size: 22px;
  letter-spacing: 2px;
  color: #ff6b00;
  text-shadow: 0 0 20px rgba(255,107,0,0.5);
  white-space: nowrap;
}
.sec-line { flex: 1; height: 1px; background: linear-gradient(90deg, rgba(255,107,0,0.6), transparent); }
.sec-line.right { background: linear-gradient(270deg, rgba(112,0,255,0.6), transparent); }

.skill-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
  padding: 0 20px;
}
.skill-row {
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 10px;
  padding: 12px 14px;
  transition: all 0.3s;
}
.skill-row:hover {
  border-color: rgba(112,0,255,0.5);
  background: rgba(112,0,255,0.08);
  transform: translateY(-2px);
}
.skill-label {
  font-size: 10px;
  font-family: 'Share Tech Mono', monospace;
  color: #6b7280;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 8px;
}
.skill-tags { display: flex; flex-wrap: wrap; gap: 5px; }
.tag { font-size: 11px; font-family: 'Share Tech Mono', monospace; padding: 2px 8px; border-radius: 4px; border: 1px solid; }
.tag-purple { color: #c084fc; border-color: rgba(192,132,252,0.3); background: rgba(112,0,255,0.1); }
.tag-orange { color: #fb923c; border-color: rgba(251,146,60,0.3); background: rgba(255,107,0,0.1); }
.tag-blue { color: #60a5fa; border-color: rgba(96,165,250,0.3); background: rgba(0,153,255,0.1); }
.tag-green { color: #34d399; border-color: rgba(52,211,153,0.3); background: rgba(0,200,100,0.1); }

.stat-section { padding: 0 20px; }
.stat-item { margin-bottom: 14px; }
.stat-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 5px; }
.stat-name { font-family: 'Rajdhani', sans-serif; font-size: 13px; font-weight: 600; color: #e2e8f0; text-transform: uppercase; letter-spacing: 1px; }
.stat-val { font-family: 'Share Tech Mono', monospace; font-size: 12px; color: #ff6b00; }
.stat-bar-bg { height: 6px; background: rgba(255,255,255,0.06); border-radius: 3px; overflow: hidden; }
.stat-bar-fill { height: 100%; border-radius: 3px; width: 0%; transition: width 1.4s ease-out; }
.bar-python { background: linear-gradient(90deg, #ff6b00, #ffd700); }
.bar-django { background: linear-gradient(90deg, #7000ff, #c084fc); }
.bar-react  { background: linear-gradient(90deg, #0099ff, #00ccff); }
.bar-js     { background: linear-gradient(90deg, #ffd700, #ff6b00); }
.bar-db     { background: linear-gradient(90deg, #34d399, #0099ff); }
.bar-cpp    { background: linear-gradient(90deg, #ff4466, #c084fc); }

.mission-grid { padding: 0 20px; display: flex; flex-direction: column; gap: 12px; }
.mission-card {
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 10px;
  padding: 14px 16px;
  position: relative;
  overflow: hidden;
  transition: all 0.3s;
}
.mission-card:hover { border-color: rgba(255,107,0,0.5); transform: translateX(4px); }
.mission-card::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 3px; background: linear-gradient(180deg, #ff6b00, #7000ff); }
.mission-rank { display: inline-block; font-family: 'Bangers', cursive; font-size: 11px; letter-spacing: 2px; padding: 2px 8px; border-radius: 4px; margin-bottom: 6px; }
.rank-s { background: rgba(255,215,0,0.15); color: #ffd700; border: 1px solid rgba(255,215,0,0.3); }
.rank-a { background: rgba(112,0,255,0.15); color: #c084fc; border: 1px solid rgba(112,0,255,0.3); }
.mission-title { font-family: 'Rajdhani', sans-serif; font-size: 16px; font-weight: 700; color: #f1f5f9; margin-bottom: 4px; }
.mission-desc { font-size: 12px; color: #94a3b8; line-height: 1.5; margin-bottom: 8px; }
.mission-chips { display: flex; flex-wrap: wrap; gap: 4px; }
.chip { font-size: 10px; font-family: 'Share Tech Mono', monospace; padding: 2px 7px; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 3px; color: #94a3b8; }

.flow-row { display: flex; align-items: center; gap: 0; padding: 0 20px; }
.flow-step { flex: 1; text-align: center; padding: 14px 8px; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.07); border-radius: 8px; transition: all 0.3s; }
.flow-step:hover { background: rgba(112,0,255,0.1); border-color: rgba(112,0,255,0.4); transform: translateY(-3px); }
.flow-icon { font-size: 22px; margin-bottom: 5px; }
.flow-label { font-family: 'Bangers', cursive; font-size: 14px; letter-spacing: 1px; color: #ff6b00; }
.flow-sub { font-size: 10px; color: #64748b; margin-top: 2px; font-family: 'Share Tech Mono', monospace; }
.flow-arrow { color: #7000ff; font-size: 18px; padding: 0 4px; flex-shrink: 0; animation: arrowPulse 1.5s ease-in-out infinite; }
@keyframes arrowPulse {
  0%,100% { opacity: 1; transform: translateX(0); }
  50% { opacity: 0.4; transform: translateX(3px); }
}

.contact-row { display: flex; gap: 10px; padding: 0 20px; flex-wrap: wrap; }
.contact-btn {
  flex: 1; min-width: 120px;
  display: flex; align-items: center; justify-content: center; gap: 8px;
  padding: 12px 16px; border-radius: 8px; border: 1px solid;
  font-family: 'Rajdhani', sans-serif; font-size: 14px; font-weight: 700; letter-spacing: 1px;
  text-decoration: none; transition: all 0.3s; cursor: pointer; position: relative; overflow: hidden;
}
.contact-btn:hover { transform: translateY(-2px); }
.btn-gmail { color: #ff6b6b; border-color: rgba(255,107,107,0.4); background: rgba(255,0,0,0.08); }
.btn-gmail:hover { box-shadow: 0 0 20px rgba(255,107,107,0.3); border-color: rgba(255,107,107,0.8); }
.btn-li { color: #60a5fa; border-color: rgba(96,165,250,0.4); background: rgba(0,119,181,0.08); }
.btn-li:hover { box-shadow: 0 0 20px rgba(96,165,250,0.3); border-color: rgba(96,165,250,0.8); }
.btn-gh { color: #c084fc; border-color: rgba(192,132,252,0.4); background: rgba(112,0,255,0.08); }
.btn-gh:hover { box-shadow: 0 0 20px rgba(192,132,252,0.3); border-color: rgba(192,132,252,0.8); }

.footer-bar { margin-top: 30px; padding: 16px 20px; border-top: 1px solid rgba(112,0,255,0.2); text-align: center; font-family: 'Share Tech Mono', monospace; font-size: 11px; color: #475569; letter-spacing: 2px; }
.footer-bar span { color: #ff6b00; }
</style>
</head>
<body>

<div class="bg-canvas">
  <div class="orb orb1"></div>
  <div class="orb orb2"></div>
  <div class="orb orb3"></div>
  <div class="orb orb4"></div>
  <svg class="speed-lines" id="speedSvg" viewBox="0 0 800 800"></svg>
</div>

<div class="content">

  <div class="hero">
    <div class="manga-frame">
      <div class="hero-name">Huzaifa Sikandar Rao</div>
    </div>
    <div class="hero-title">⚡ Software Engineer • Backend Architect • Builder ⚡</div>
    <div style="display:flex;gap:8px;justify-content:center;flex-wrap:wrap;">
      <span class="power-badge"><span class="dot-online"></span> Open to Opportunities</span>
      <span class="power-badge">🇵🇰 Lahore, PK</span>
      <span class="power-badge">📚 Sem 5 · COMSATS</span>
    </div>
    <div class="spirit-meter">
      <span style="font-family:'Share Tech Mono',monospace;font-size:10px;color:#475569;margin-right:6px;">SPIRIT</span>
      <div class="spirit-block"></div>
      <div class="spirit-block"></div>
      <div class="spirit-block"></div>
      <div class="spirit-block"></div>
      <div class="spirit-block"></div>
      <div class="spirit-block"></div>
      <div class="spirit-block"></div>
      <span style="font-family:'Share Tech Mono',monospace;font-size:10px;color:#ff6b00;margin-left:6px;">MAX</span>
    </div>
  </div>

  <div class="char-card">
    <div class="card-header">
      <div class="card-dot dot-r"></div>
      <div class="card-dot dot-y"></div>
      <div class="card-dot dot-g"></div>
      character.profile — active arc
    </div>
    <div class="code-block">
      <span class="cc"># ──── THE BACKEND SHINOBI ────</span><br>
      <span class="ck">class</span> <span class="cn">HuzaifaSikandarRao</span>:<br>
      &nbsp;&nbsp;<span class="cp">current_arc</span>  = <span class="cs">"Full Time Intern @ App Aura"</span><br>
      &nbsp;&nbsp;<span class="cp">previous</span>    = <span class="cs">"Backend Intern @ Zweidevs (Winter Arc)"</span><br>
      &nbsp;&nbsp;<span class="cp">special_moves</span> = {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Bankai"</span>      : <span class="cs">"Django REST Framework"</span>,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Domain Exp"</span>  : <span class="cs">"System Design & Architecture"</span>,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Cursed Tech"</span> : <span class="cs">"8086 Assembly & CPU Internals"</span>,<br>
      &nbsp;&nbsp;&nbsp;&nbsp;<span class="cs">"Hollow Mask"</span> : <span class="cs">"MERN Stack & Modern Web"</span>,<br>
      &nbsp;&nbsp;}<br>
      &nbsp;&nbsp;<span class="cp">sensei</span> = [<span class="cs">"Claude"</span>, <span class="cs">"Gemini"</span>, <span class="cs">"ChatGPT"</span>]<br>
      &nbsp;&nbsp;<span class="cc"># Ship faster. Write cleaner. Always shipping.</span>
    </div>
  </div>

  <div class="sec-label">
    <div class="sec-line"></div>
    <div class="sec-label-text">⚔️ JUTSU ARSENAL</div>
    <div class="sec-line right"></div>
  </div>

  <div class="skill-grid">
    <div class="skill-row">
      <div class="skill-label">🔥 Core Languages</div>
      <div class="skill-tags">
        <span class="tag tag-orange">Python</span>
        <span class="tag tag-orange">JavaScript</span>
        <span class="tag tag-orange">TypeScript</span>
        <span class="tag tag-orange">C++</span>
        <span class="tag tag-orange">Bash</span>
      </div>
    </div>
    <div class="skill-row">
      <div class="skill-label">⚡ Backend</div>
      <div class="skill-tags">
        <span class="tag tag-purple">Django</span>
        <span class="tag tag-purple">Node.js</span>
        <span class="tag tag-purple">Express</span>
        <span class="tag tag-purple">REST API</span>
      </div>
    </div>
    <div class="skill-row">
      <div class="skill-label">📊 Database</div>
      <div class="skill-tags">
        <span class="tag tag-green">PostgreSQL</span>
        <span class="tag tag-green">MongoDB</span>
        <span class="tag tag-green">Supabase</span>
      </div>
    </div>
    <div class="skill-row">
      <div class="skill-label">🌐 Frontend</div>
      <div class="skill-tags">
        <span class="tag tag-blue">React</span>
        <span class="tag tag-blue">Tailwind</span>
        <span class="tag tag-blue">Vite</span>
        <span class="tag tag-blue">Figma</span>
      </div>
    </div>
    <div class="skill-row" style="grid-column:1/-1;">
      <div class="skill-label">☁️ Cloud & Infra</div>
      <div class="skill-tags">
        <span class="tag tag-blue">GCP</span>
        <span class="tag tag-green">Vercel</span>
        <span class="tag tag-orange">Git</span>
        <span class="tag tag-orange">GitHub</span>
        <span class="tag tag-purple">Postman</span>
        <span class="tag tag-green">Linux</span>
      </div>
    </div>
  </div>

  <div class="sec-label">
    <div class="sec-line"></div>
    <div class="sec-label-text">📈 POWER LEVELS</div>
    <div class="sec-line right"></div>
  </div>

  <div class="stat-section">
    <div class="stat-item">
      <div class="stat-header"><span class="stat-name">Python</span><span class="stat-val">92 / 100</span></div>
      <div class="stat-bar-bg"><div class="stat-bar-fill bar-python" data-width="92"></div></div>
    </div>
    <div class="stat-item">
      <div class="stat-header"><span class="stat-name">Django · REST</span><span class="stat-val">88 / 100</span></div>
      <div class="stat-bar-bg"><div class="stat-bar-fill bar-django" data-width="88"></div></div>
    </div>
    <div class="stat-item">
      <div class="stat-header"><span class="stat-name">JavaScript · TS</span><span class="stat-val">78 / 100</span></div>
      <div class="stat-bar-bg"><div class="stat-bar-fill bar-js" data-width="78"></div></div>
    </div>
    <div class="stat-item">
      <div class="stat-header"><span class="stat-name">React · Node</span><span class="stat-val">70 / 100</span></div>
      <div class="stat-bar-bg"><div class="stat-bar-fill bar-react" data-width="70"></div></div>
    </div>
    <div class="stat-item">
      <div class="stat-header"><span class="stat-name">Databases</span><span class="stat-val">82 / 100</span></div>
      <div class="stat-bar-bg"><div class="stat-bar-fill bar-db" data-width="82"></div></div>
    </div>
    <div class="stat-item">
      <div class="stat-header"><span class="stat-name">Systems · C++</span><span class="stat-val">65 / 100</span></div>
      <div class="stat-bar-bg"><div class="stat-bar-fill bar-cpp" data-width="65"></div></div>
    </div>
  </div>

  <div class="sec-label">
    <div class="sec-line"></div>
    <div class="sec-label-text">📜 MISSION BOARD</div>
    <div class="sec-line right"></div>
  </div>

  <div class="mission-grid">
    <div class="mission-card">
      <div class="mission-rank rank-s">S RANK</div>
      <div class="mission-title">🧵 Stitch & Twine</div>
      <div class="mission-desc">Full stack e-commerce storefront with real-time database ops, auth, and edge deployment. Complete shopping experience from catalogue to checkout.</div>
      <div class="mission-chips">
        <span class="chip">Full Stack</span><span class="chip">Supabase</span><span class="chip">Vercel</span><span class="chip">E-Commerce</span><span class="chip">✓ Complete</span>
      </div>
    </div>
    <div class="mission-card">
      <div class="mission-rank rank-a">A RANK</div>
      <div class="mission-title">🎮 Esportify</div>
      <div class="mission-desc">Desktop-grade esports management suite engineered with Python and PyQt5. Team rosters, tournament brackets, and match scheduling in a slick native UI.</div>
      <div class="mission-chips">
        <span class="chip">Python</span><span class="chip">PyQt5</span><span class="chip">Desktop App</span><span class="chip">GUI</span><span class="chip">✓ Complete</span>
      </div>
    </div>
  </div>

  <div class="sec-label">
    <div class="sec-line"></div>
    <div class="sec-label-text">🌀 COMBAT FLOW</div>
    <div class="sec-line right"></div>
  </div>

  <div class="flow-row">
    <div class="flow-step">
      <div class="flow-icon">🎯</div>
      <div class="flow-label">Perceive</div>
      <div class="flow-sub">Read battlefield</div>
    </div>
    <div class="flow-arrow">➤</div>
    <div class="flow-step">
      <div class="flow-icon">🏗️</div>
      <div class="flow-label">Architect</div>
      <div class="flow-sub">Design system</div>
    </div>
    <div class="flow-arrow">➤</div>
    <div class="flow-step">
      <div class="flow-icon">⚔️</div>
      <div class="flow-label">Execute</div>
      <div class="flow-sub">Build + debug</div>
    </div>
    <div class="flow-arrow">➤</div>
    <div class="flow-step">
      <div class="flow-icon">🚀</div>
      <div class="flow-label">Ship</div>
      <div class="flow-sub">Deploy precise</div>
    </div>
  </div>

  <div class="sec-label">
    <div class="sec-line"></div>
    <div class="sec-label-text">📡 SEND TRANSMISSION</div>
    <div class="sec-line right"></div>
  </div>

  <div class="contact-row">
    <a class="contact-btn btn-gmail" href="mailto:huzaifasikandarrao@gmail.com">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
      Gmail
    </a>
    <a class="contact-btn btn-li" href="https://www.linkedin.com/in/huzaifa-sikandar-rao-822a103a3/" target="_blank">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M19 3a2 2 0 012 2v14a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h14m-.5 15.5v-5.3a3.26 3.26 0 00-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 011.4 1.4v4.93h2.79M6.88 8.56a1.68 1.68 0 001.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 00-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37h2.77z"/></svg>
      LinkedIn
    </a>
    <a class="contact-btn btn-gh" href="https://github.com/huzaifarao30" target="_blank">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2A10 10 0 002 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0012 2z"/></svg>
      GitHub
    </a>
  </div>

  <div class="footer-bar">
    <span>⚡</span> BUILT WITH INTENT · DEPLOYED WITH PRECISION · THE ARC NEVER ENDS <span>⚡</span>
  </div>

</div>

<script>
// Speed lines
const svg = document.getElementById('speedSvg');
let html = '';
const cx = 400, cy = 400;
for (let i = 0; i < 80; i++) {
  const angle = (i / 80) * 360;
  const rad = angle * Math.PI / 180;
  const r1 = 80 + Math.random() * 40;
  const r2 = 500 + Math.random() * 200;
  html += `<line x1="${cx + Math.cos(rad)*r1}" y1="${cy + Math.sin(rad)*r1}" x2="${cx + Math.cos(rad)*r2}" y2="${cy + Math.sin(rad)*r2}" stroke="white" stroke-width="${(0.3 + Math.random()*0.7).toFixed(2)}" opacity="${(0.3 + Math.random()*0.7).toFixed(2)}"/>`;
}
svg.innerHTML = `<g>${html}</g>`;

// Animate stat bars
setTimeout(() => {
  document.querySelectorAll('.stat-bar-fill').forEach((bar, i) => {
    setTimeout(() => {
      bar.style.width = bar.dataset.width + '%';
    }, i * 150);
  });
}, 300);
</script>
</body>
</html>
