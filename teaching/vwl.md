---
layout: page
title: 
permalink: /teaching/vwl/
---
<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Space+Grotesk:wght@400;500;600&display=swap');

:root {
  --bg-deep: #0a0a0f;
  --bg-card: rgba(18, 18, 28, 0.85);
  --bg-card-hover: rgba(24, 24, 38, 0.9);
  --border: rgba(255,255,255,0.08);
  --border-hover: rgba(255,255,255,0.14);
  --text-primary: rgba(255,255,255,0.92);
  --text-secondary: rgba(255,255,255,0.55);
  --text-muted: rgba(255,255,255,0.32);
  --accent-1: #6366f1;
  --accent-2: #8b5cf6;
  --accent-3: #a78bfa;
  --mikro: #f59e0b;
  --mikro-soft: rgba(245, 158, 11, 0.12);
  --makro: #06b6d4;
  --makro-soft: rgba(6, 182, 212, 0.12);
  --success: #34d399;
  --success-soft: rgba(52, 211, 153, 0.12);
  --radius: 16px;
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-deep) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }
a { color: var(--text-secondary); }
a:hover { color: var(--text-primary); }

/* ═══ AMBIENT – 3 orbs, reduced blur ═══ */
.sv-ambient {
  position: fixed; top: 0; left: 0; right: 0; bottom: 0;
  z-index: 0; overflow: hidden; pointer-events: none;
}
.sv-ambient-orb {
  position: absolute; border-radius: 50%;
  filter: blur(80px); opacity: 0.35;
  will-change: transform;
  animation: sv-drift 25s ease-in-out infinite;
}
.sv-ambient-orb:nth-child(1) {
  width: 450px; height: 450px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.2) 0%, transparent 70%);
  top: -12%; left: -8%;
}
.sv-ambient-orb:nth-child(2) {
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(139, 92, 246, 0.15) 0%, transparent 70%);
  top: 35%; right: -12%;
  animation-delay: -10s;
}
.sv-ambient-orb:nth-child(3) {
  width: 350px; height: 350px;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.1) 0%, transparent 70%);
  bottom: -5%; left: 20%;
  animation-delay: -18s;
}
@keyframes sv-drift {
  0%, 100% { transform: translate(0, 0); }
  33% { transform: translate(20px, -15px); }
  66% { transform: translate(-15px, 20px); }
}
.sv-ambient::after {
  content: ''; position: absolute; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  opacity: 0.4; pointer-events: none;
}
@media (max-width: 768px) {
  .sv-ambient-orb { animation: none !important; filter: blur(60px); opacity: 0.25; }
}

/* ═══ LAYOUT ═══ */
.sv-content {
  position: relative; z-index: 1;
  max-width: 780px; margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  font-family: 'Inter', -apple-system, sans-serif;
}

/* ═══ HERO – only element with real blur ═══ */
.sv-hero {
  background: rgba(18, 18, 28, 0.7);
  backdrop-filter: blur(30px); -webkit-backdrop-filter: blur(30px);
  border: 1px solid var(--border); border-radius: 24px;
  padding: 2.5rem 2.25rem 2rem; margin-bottom: 3rem;
  position: relative; overflow: hidden;
}
.sv-hero::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
}
.sv-hero-eyebrow {
  font-size: 0.72rem; font-weight: 500; letter-spacing: 0.12em;
  text-transform: uppercase; color: var(--accent-3); margin-bottom: 0.75rem;
}
.sv-hero h1 {
  font-family: 'Space Grotesk', sans-serif; font-size: 2.5rem; font-weight: 600;
  letter-spacing: -0.03em; line-height: 1.1; margin-bottom: 0.4rem;
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.sv-hero-sub { font-size: 0.92rem; color: var(--text-secondary); font-weight: 300; margin-bottom: 2rem; }
.sv-progress-track { background: rgba(255,255,255,0.06); border-radius: 100px; height: 4px; overflow: hidden; margin-bottom: 0.75rem; }
.sv-progress-fill {
  height: 100%; border-radius: 100px;
  background: linear-gradient(90deg, var(--accent-1), var(--accent-2), var(--accent-3));
  width: 0%; transition: width 0.6s ease;
  box-shadow: 0 0 10px rgba(99, 102, 241, 0.3);
}
.sv-progress-meta { display: flex; justify-content: space-between; }
.sv-progress-meta span { font-size: 0.75rem; color: var(--text-muted); font-weight: 400; }
.sv-progress-meta .sv-pct { color: var(--accent-3); font-weight: 500; }

/* ═══ SECTIONS ═══ */
.sv-section { margin-bottom: 3rem; }
.sv-section-head { display: flex; align-items: center; gap: 0.85rem; margin-bottom: 0.4rem; padding: 0 0.25rem; }
.sv-section-badge {
  width: 36px; height: 36px; border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 0.68rem; font-weight: 600; letter-spacing: 0.06em; text-transform: uppercase;
}
.sv-section--mikro .sv-section-badge { background: var(--mikro-soft); color: var(--mikro); border: 1px solid rgba(245,158,11,0.2); }
.sv-section--makro .sv-section-badge { background: var(--makro-soft); color: var(--makro); border: 1px solid rgba(6,182,212,0.2); }
.sv-section-title { font-family: 'Space Grotesk', sans-serif; font-size: 1.35rem; font-weight: 500; letter-spacing: -0.01em; color: var(--text-primary); margin: 0; }
.sv-section-meta { font-size: 0.78rem; color: var(--text-muted); padding-left: calc(36px + 0.85rem + 0.25rem); margin-bottom: 1.5rem; }

/* ═══ TIMELINE ═══ */
.sv-path { position: relative; padding-left: 2.5rem; }
.sv-path::before {
  content: ''; position: absolute; left: 17px; top: 20px; bottom: 20px; width: 1px;
  background: linear-gradient(180deg, var(--border) 0%, rgba(255,255,255,0.03) 100%);
}
.sv-module { position: relative; margin-bottom: 0.75rem; }
.sv-module-dot {
  position: absolute; left: -2.5rem; top: 50%; transform: translateY(-50%);
  width: 11px; height: 11px; border-radius: 50%;
  background: var(--bg-deep); border: 2px solid var(--border); z-index: 2;
  transition: background 0.15s ease, border-color 0.15s ease, box-shadow 0.15s ease;
}
.sv-module.is-complete .sv-module-dot {
  background: var(--success); border-color: var(--success);
  box-shadow: 0 0 8px rgba(52,211,153,0.3);
}

/* ═══ CARD – fake glass, NO backdrop-filter ═══ */
.sv-card {
  background: var(--bg-card); border: 1px solid var(--border);
  border-radius: var(--radius); padding: 1.35rem 1.5rem;
  position: relative; overflow: hidden;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease, background 0.15s ease;
}
.sv-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
  opacity: 0; transition: opacity 0.15s ease;
}
.sv-card:hover {
  background: var(--bg-card-hover); border-color: var(--border-hover);
  transform: translateY(-2px); box-shadow: 0 8px 24px rgba(0,0,0,0.3);
}
.sv-card:hover::before { opacity: 1; }
.sv-module.is-complete .sv-card { border-left: 2px solid var(--success); }

.sv-card-top { display: flex; align-items: center; gap: 0.65rem; margin-bottom: 0.3rem; }
.sv-step-num {
  font-size: 0.65rem; font-weight: 600; letter-spacing: 0.1em;
  text-transform: uppercase; padding: 0.15rem 0.55rem; border-radius: 6px; flex-shrink: 0;
}
.sv-section--mikro .sv-step-num { color: var(--mikro); background: var(--mikro-soft); }
.sv-section--makro .sv-step-num { color: var(--makro); background: var(--makro-soft); }
.sv-module.is-complete .sv-step-num { color: var(--success); background: var(--success-soft); }

.sv-card h4 { font-size: 0.95rem; font-weight: 500; color: var(--text-primary); margin: 0; line-height: 1.45; }
.sv-card-desc { font-size: 0.82rem; color: var(--text-secondary); font-weight: 300; line-height: 1.7; margin: 0.25rem 0 1.1rem 0; }
.sv-card-prereq { font-size: 0.72rem; color: var(--text-muted); margin: -0.2rem 0 0.9rem 0; font-style: italic; }
.sv-card-prereq::before { content: '↗ '; color: var(--accent-3); }

/* ═══ ACTIONS – all 0.15s ═══ */
.sv-actions { display: flex; align-items: center; gap: 0.6rem; flex-wrap: wrap; }
.sv-btn {
  display: inline-flex; align-items: center; gap: 0.35rem;
  padding: 0.55rem 1rem; border-radius: 10px;
  font-size: 0.76rem; font-weight: 500; letter-spacing: 0.04em;
  text-transform: uppercase; text-decoration: none;
  border: 1px solid var(--border); background: rgba(255,255,255,0.03);
  color: var(--text-secondary) !important; cursor: pointer;
  font-family: 'Inter', -apple-system, sans-serif;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease, background 0.15s ease, color 0.15s ease;
}
.sv-btn:hover {
  transform: translateY(-1px); border-color: var(--border-hover);
  background: rgba(255,255,255,0.08); color: var(--text-primary) !important;
  box-shadow: 0 4px 12px rgba(0,0,0,0.2); text-decoration: none;
}
.sv-btn--pdf:hover { border-color: rgba(245,158,11,0.4); box-shadow: 0 4px 12px rgba(245,158,11,0.1); }
.sv-section--makro .sv-btn--pdf:hover { border-color: rgba(6,182,212,0.4); box-shadow: 0 4px 12px rgba(6,182,212,0.1); }
.sv-btn--quiz:hover { border-color: rgba(99,102,241,0.4); box-shadow: 0 4px 12px rgba(99,102,241,0.1); }

.sv-check {
  margin-left: auto; display: flex; align-items: center; gap: 0.4rem;
  font-size: 0.72rem; color: var(--text-muted); cursor: pointer;
  padding: 0.35rem 0.55rem; border-radius: 8px; user-select: none;
  transition: background 0.15s ease, color 0.15s ease;
}
.sv-check:hover { background: var(--success-soft); color: var(--success); }
.sv-check-box {
  width: 18px; height: 18px; border-radius: 6px;
  border: 1.5px solid var(--border);
  display: flex; align-items: center; justify-content: center; flex-shrink: 0;
  transition: background 0.15s ease, border-color 0.15s ease, box-shadow 0.15s ease;
}
.sv-check-box svg { opacity: 0; transition: opacity 0.15s ease; width: 11px; height: 11px; }
.sv-module.is-complete .sv-check-box { background: var(--success); border-color: var(--success); box-shadow: 0 0 8px rgba(52,211,153,0.2); }
.sv-module.is-complete .sv-check-box svg { opacity: 1; }
.sv-module.is-complete .sv-check { color: var(--success); }

/* ═══ FOOTER – second element with blur ═══ */
.sv-footer {
  margin-top: 2rem; padding: 1.5rem 1.75rem;
  background: rgba(18, 18, 28, 0.7);
  backdrop-filter: blur(30px); -webkit-backdrop-filter: blur(30px);
  border: 1px solid var(--border); border-radius: 20px;
  display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 1rem;
}
.sv-footer-text { font-size: 0.8rem; color: var(--text-muted); font-weight: 300; }
.sv-footer-text strong { color: var(--text-secondary); font-weight: 500; }
.sv-footer-actions { display: flex; gap: 0.6rem; }
.sv-btn-reset {
  display: inline-flex; align-items: center; padding: 0.55rem 1rem; border-radius: 10px;
  font-size: 0.72rem; font-weight: 400; letter-spacing: 0.04em;
  border: 1px solid transparent; background: transparent;
  color: var(--text-muted) !important; cursor: pointer;
  font-family: 'Inter', -apple-system, sans-serif;
  transition: border-color 0.15s ease, color 0.15s ease;
}
.sv-btn-reset:hover { border-color: var(--border); color: var(--text-secondary) !important; }

/* ═══ ANIMATIONS – first 4 staggered, rest instant ═══ */
@keyframes sv-fadeUp {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}
.sv-hero { animation: sv-fadeUp 0.4s ease both; }
.sv-section { animation: sv-fadeUp 0.35s ease both; }
.sv-module:nth-child(-n+4) { animation: sv-fadeUp 0.3s ease both; }
.sv-module:nth-child(1) { animation-delay: 0.03s; }
.sv-module:nth-child(2) { animation-delay: 0.06s; }
.sv-module:nth-child(3) { animation-delay: 0.09s; }
.sv-module:nth-child(4) { animation-delay: 0.12s; }
.sv-module:nth-child(n+5) { opacity: 1; }

/* ═══ RESPONSIVE ═══ */
@media (max-width: 768px) {
  .sv-content { padding: 1.5rem 1rem 4rem; }
  .sv-hero { padding: 2rem 1.5rem 1.5rem; border-radius: 20px; backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px); }
  .sv-hero h1 { font-size: 1.9rem; }
  .sv-path { padding-left: 2rem; }
  .sv-module-dot { left: -2rem; }
  .sv-card { padding: 1.1rem 1.2rem; }
  .sv-actions { flex-direction: column; align-items: stretch; }
  .sv-btn { justify-content: center; }
  .sv-check { margin-left: 0; justify-content: center; }
  .sv-footer { flex-direction: column; text-align: center; backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px); }
  .sv-footer-actions { width: 100%; flex-direction: column; }
  .sv-section-meta { padding-left: calc(36px + 0.85rem); }
  .sv-card:hover { transform: none; box-shadow: none; }
}
</style>

<!-- AMBIENT – 3 orbs instead of 4 -->
<div class="sv-ambient">
  <div class="sv-ambient-orb"></div>
  <div class="sv-ambient-orb"></div>
  <div class="sv-ambient-orb"></div>
</div>

<div class="sv-content">

  <div class="sv-hero">
    <div class="sv-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Volkswirtschaftslehre</h1>
    <p class="sv-hero-sub">13 Module · Mikroökonomie & Makroökonomie</p>
    <div class="sv-progress-track"><div class="sv-progress-fill" id="progressBar"></div></div>
    <div class="sv-progress-meta">
      <span><span id="completedCount">0</span> von <span id="totalCount">13</span> Modulen</span>
      <span class="sv-pct" id="progressPercent">0 %</span>
    </div>
  </div>

  <!-- MIKROÖKONOMIE -->
  <div class="sv-section sv-section--mikro">
    <div class="sv-section-head">
      <div class="sv-section-badge">Mi</div>
      <h2 class="sv-section-title">Mikroökonomie</h2>
    </div>
    <p class="sv-section-meta">8 Module · Vom Grundbegriff zum Marktmodell</p>
    <div class="sv-path">
      <div class="sv-module" data-module="m1"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">01</span><h4>Bedürfnis, Bedarf und Nachfrage</h4></div><p class="sv-card-desc">Grundkonzepte der Wirtschaft: Definition und Unterscheidung von Bedürfnis, Bedarf und Nachfrage, Bedürfnisarten, Maslows Bedürfnispyramide mit praktischen Beispielen</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_1-3.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m1')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m2"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">02</span><h4>Güterarten in der Wirtschaft</h4></div><p class="sv-card-desc">Freie und wirtschaftliche Güter, inferiore und superiore Güter, Einkommenselastizität der Nachfrage, meritorische und demeritorische Güter, staatliche Markteingriffe</p><p class="sv-card-prereq">Baut auf: Bedürfnis, Bedarf und Nachfrage</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_2-2.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_gueterarten.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m2')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m3"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">03</span><h4>Angebot und Angebotskurve</h4></div><p class="sv-card-desc">Das Marktmodell, Gesetz des Angebots, Angebotsfunktion, aggregiertes Marktangebot, Verschiebung vs. Bewegung auf der Angebotskurve, Einflussfaktoren</p><p class="sv-card-prereq">Baut auf: Güterarten</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_3-4.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_angebot.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m3')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m4"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">04</span><h4>Nachfrage und Nachfragekurve</h4></div><p class="sv-card-desc">Gesetz der Nachfrage, Nachfragefunktion, aggregierte Marktnachfrage, Verschiebung der Nachfragekurve, Einflussfaktoren wie Einkommen, Präferenzen und Preise verwandter Güter</p><p class="sv-card-prereq">Baut auf: Angebot und Angebotskurve</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_4-2.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_nachfrage.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m4')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m5"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">05</span><h4>Marktgleichgewicht</h4></div><p class="sv-card-desc">Gleichgewichtspreis und -menge, Angebots- und Nachfrageüberhang, Anpassungsprozesse, Auswirkungen von Steuern und Subventionen, praktische Beispiele und Berechnungen</p><p class="sv-card-prereq">Baut auf: Angebot und Nachfrage</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_5-2.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_marktgleichgewicht.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m5')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m6"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">06</span><h4>Konsumenten- und Produzentenrente</h4></div><p class="sv-card-desc">Definition und Berechnung der Konsumenten- und Produzentenrente, ökonomische Wohlfahrt, Prohibitivpreis, graphische Darstellung, Beispielrechnungen am Smartwatch-Markt</p><p class="sv-card-prereq">Baut auf: Marktgleichgewicht</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_6.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_renten.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m6')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m7"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">07</span><h4>Marktformen: Monopol, Oligopol, Polypol</h4></div><p class="sv-card-desc">Übersicht über Marktformen, Marktmacht, Marktstruktur, Vor- und Nachteile für Verbraucher, zahlreiche Beispiele und Übungsaufgaben zur Einordnung realer Märkte</p><p class="sv-card-prereq">Baut auf: Marktgleichgewicht</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_7.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_marktformen.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m7')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m8"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">08</span><h4>Budgetgerade – Konsumentscheidungen</h4></div><p class="sv-card-desc">Mathematische Grundlagen der Konsumentscheidung: Budgetrestriktion, Gleichung und graphische Darstellung, Einkommens- und Preisänderungen, Opportunitätskosten</p><p class="sv-card-prereq">Baut auf: Nachfrage und Güterarten</p><div class="sv-actions"><a href="/assets/pdfs/WS_VWL_8-3.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_budgetgerade.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m8')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
    </div>
  </div>

  <!-- MAKROÖKONOMIE -->
  <div class="sv-section sv-section--makro">
    <div class="sv-section-head">
      <div class="sv-section-badge">Ma</div>
      <h2 class="sv-section-title">Makroökonomie</h2>
    </div>
    <p class="sv-section-meta">5 Module · Von der Gesamtrechnung zur Wirtschaftspolitik</p>
    <div class="sv-path">
      <div class="sv-module" data-module="m9"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">09</span><h4>Volkswirtschaftliche Gesamtrechnung</h4></div><p class="sv-card-desc">Definition und Ziele der VGR, Bruttoinlandsprodukt (BIP), drei Berechnungsmethoden, Inlandsprinzip vs. Inländerprinzip, Vermeidung von Doppelzählung</p><div class="sv-actions"><a href="/assets/pdfs/VWL_11.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_vgr.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m9')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m10"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">10</span><h4>Nominales vs. reales BIP</h4></div><p class="sv-card-desc">BIP-Deflator, BIP pro Kopf und Kaufkraftbereinigung (PPP), Grenzen des BIP als Wohlstandsindikator, alternative Indikatoren (HDI, Gini-Koeffizient)</p><p class="sv-card-prereq">Baut auf: Volkswirtschaftliche Gesamtrechnung</p><div class="sv-actions"><a href="/assets/pdfs/VWL_12.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_vgr2.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m10')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m11"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">11</span><h4>Konjunktur & Konjunkturzyklen</h4></div><p class="sv-card-desc">Die 4 Konjunkturphasen, BIP-Berechnung, Wachstumsraten, Rezessionsdefinition, Früh- und Spätindikatoren, wirtschaftspolitische Maßnahmen</p><p class="sv-card-prereq">Baut auf: Nominales vs. reales BIP</p><div class="sv-actions"><a href="/assets/pdfs/VWL_11_Konjunktur.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_konjunktur.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m11')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m12"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">12</span><h4>Antizyklische Konjunkturpolitik</h4></div><p class="sv-card-desc">Grundprinzipien antizyklischer Politik, Fiskal- und Geldpolitik, expansive vs. restriktive Maßnahmen, historische Fallbeispiele (Finanzkrise 2008)</p><p class="sv-card-prereq">Baut auf: Konjunkturzyklen</p><div class="sv-actions"><a href="/assets/pdfs/VWL_12_Konjunkturpolitik.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_konjunkturpolitik.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m12')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
      <div class="sv-module" data-module="m13"><div class="sv-module-dot"></div><div class="sv-card"><div class="sv-card-top"><span class="sv-step-num">13</span><h4>Arbeitslosigkeit & Arbeitsmarktpolitik</h4></div><p class="sv-card-desc">Arbeitslosenquote, drei Arten der Arbeitslosigkeit, Okun's Gesetz, aktive vs. passive Arbeitsmarktpolitik, Kurzarbeitergeld, Digitalisierung und demografischer Wandel</p><p class="sv-card-prereq">Baut auf: Konjunktur und Konjunkturpolitik</p><div class="sv-actions"><a href="/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf" class="sv-btn sv-btn--pdf"><span>📄</span> PDF</a><a href="/assets/quizzes/quiz_arbeitslosigkeit.html" class="sv-btn sv-btn--quiz"><span>✎</span> Quiz</a><label class="sv-check" onclick="toggleModule('m13')"><span class="sv-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label></div></div></div>
    </div>
  </div>

  <div class="sv-footer">
    <div class="sv-footer-text"><strong>13 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar</div>
    <div class="sv-footer-actions">
      <a href="/teaching/" class="sv-btn">← Übersicht</a>
      <button class="sv-btn-reset" onclick="resetProgress()">Fortschritt zurücksetzen</button>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'vwl-progress';
const TOTAL_MODULES = 13;
function getProgress() { try { return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {}; } catch(e) { return {}; } }
function saveProgress(p) { localStorage.setItem(STORAGE_KEY, JSON.stringify(p)); }
function toggleModule(id) { const p = getProgress(); if (p[id]) { delete p[id]; } else { p[id] = Date.now(); } saveProgress(p); render(); }
function resetProgress() { if (confirm('Fortschritt wirklich zurücksetzen?')) { localStorage.removeItem(STORAGE_KEY); render(); } }
function render() {
  const p = getProgress(), c = Object.keys(p).length, pct = Math.round((c / TOTAL_MODULES) * 100);
  document.getElementById('progressBar').style.width = pct + '%';
  document.getElementById('completedCount').textContent = c;
  document.getElementById('progressPercent').textContent = pct + ' %';
  document.querySelectorAll('.sv-module').forEach(el => { if (p[el.dataset.module]) el.classList.add('is-complete'); else el.classList.remove('is-complete'); });
}
document.addEventListener('DOMContentLoaded', render);
if (document.readyState !== 'loading') render();
</script>