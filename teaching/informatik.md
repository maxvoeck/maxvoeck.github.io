---
layout: page
title: 
permalink: /teaching/informatik/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Space+Grotesk:wght@400;500;600&display=swap');

:root {
  --bg-deep: #0a0a0f;
  --bg-card: rgba(255,255,255,0.06);
  --bg-card-hover: rgba(255,255,255,0.09);
  --border: rgba(255,255,255,0.08);
  --border-hover: rgba(255,255,255,0.14);
  --text-primary: rgba(255,255,255,0.92);
  --text-secondary: rgba(255,255,255,0.55);
  --text-muted: rgba(255,255,255,0.32);
  --accent-1: #6366f1;
  --accent-2: #8b5cf6;
  --accent-3: #a78bfa;
  --python: #3b82f6;
  --python-soft: rgba(59, 130, 246, 0.12);
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

/* ═══ AMBIENT ═══ */
.inf-ambient {
  position: fixed; top: 0; left: 0; right: 0; bottom: 0;
  z-index: 0; overflow: hidden; pointer-events: none;
}
.inf-ambient-orb {
  position: absolute; border-radius: 50%;
  filter: blur(120px); opacity: 0.45;
  animation: inf-drift 20s ease-in-out infinite;
}
.inf-ambient-orb:nth-child(1) {
  width: 550px; height: 550px;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.22) 0%, transparent 70%);
  top: -12%; left: -8%;
}
.inf-ambient-orb:nth-child(2) {
  width: 450px; height: 450px;
  background: radial-gradient(circle, rgba(139, 92, 246, 0.16) 0%, transparent 70%);
  top: 40%; right: -12%;
  animation-delay: -7s; animation-duration: 24s;
}
.inf-ambient-orb:nth-child(3) {
  width: 380px; height: 380px;
  background: radial-gradient(circle, rgba(52, 211, 153, 0.1) 0%, transparent 70%);
  bottom: -10%; left: 25%;
  animation-delay: -13s; animation-duration: 22s;
}
@keyframes inf-drift {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(25px, -18px) scale(1.04); }
  50% { transform: translate(-18px, 25px) scale(0.96); }
  75% { transform: translate(12px, 12px) scale(1.02); }
}
.inf-ambient::after {
  content: ''; position: absolute; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  opacity: 0.4; pointer-events: none;
}

/* ═══ CONTENT ═══ */
.inf-content {
  position: relative; z-index: 1;
  max-width: 780px; margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  font-family: 'Inter', -apple-system, sans-serif;
}

/* ═══ HERO ═══ */
.inf-hero {
  background: var(--bg-card);
  backdrop-filter: blur(40px); -webkit-backdrop-filter: blur(40px);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.5rem 2.25rem 2rem;
  margin-bottom: 3rem;
  position: relative; overflow: hidden;
}
.inf-hero::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
}
.inf-hero-eyebrow {
  font-size: 0.72rem; font-weight: 500;
  letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--accent-3); margin-bottom: 0.75rem;
}
.inf-hero h1 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 2.5rem; font-weight: 600;
  letter-spacing: -0.03em; line-height: 1.1;
  margin-bottom: 0.4rem;
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.inf-hero-sub {
  font-size: 0.92rem; color: var(--text-secondary);
  font-weight: 300; margin-bottom: 2rem;
}
.inf-progress-track {
  background: rgba(255,255,255,0.06);
  border-radius: 100px; height: 4px;
  overflow: hidden; margin-bottom: 0.75rem;
}
.inf-progress-fill {
  height: 100%; border-radius: 100px;
  background: linear-gradient(90deg, var(--python), var(--accent-2), var(--accent-3));
  width: 0%;
  transition: width 0.8s cubic-bezier(0.23, 1, 0.32, 1);
  box-shadow: 0 0 12px rgba(59, 130, 246, 0.3);
}
.inf-progress-meta { display: flex; justify-content: space-between; }
.inf-progress-meta span { font-size: 0.75rem; color: var(--text-muted); font-weight: 400; }
.inf-progress-meta .inf-pct { color: var(--accent-3); font-weight: 500; }

/* ═══ SECTION ═══ */
.inf-section { margin-bottom: 3rem; }
.inf-section-head {
  display: flex; align-items: center;
  gap: 0.85rem; margin-bottom: 0.4rem; padding: 0 0.25rem;
}
.inf-section-badge {
  width: 36px; height: 36px; border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 0.68rem; font-weight: 600;
  letter-spacing: 0.06em; text-transform: uppercase;
  background: var(--python-soft); color: var(--python);
  border: 1px solid rgba(59, 130, 246, 0.2);
}
.inf-section-title {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.35rem; font-weight: 500;
  letter-spacing: -0.01em; color: var(--text-primary); margin: 0;
}
.inf-section-meta {
  font-size: 0.78rem; color: var(--text-muted);
  padding-left: calc(36px + 0.85rem + 0.25rem);
  margin-bottom: 1.5rem;
}

/* ═══ TIMELINE ═══ */
.inf-path {
  position: relative; padding-left: 2.5rem;
}
.inf-path::before {
  content: ''; position: absolute;
  left: 17px; top: 20px; bottom: 20px; width: 1px;
  background: linear-gradient(180deg, var(--border) 0%, rgba(255,255,255,0.03) 100%);
}
.inf-module { position: relative; margin-bottom: 0.75rem; }
.inf-module-dot {
  position: absolute; left: -2.5rem; top: 50%; transform: translateY(-50%);
  width: 11px; height: 11px; border-radius: 50%;
  background: var(--bg-deep); border: 2px solid var(--border);
  z-index: 2; transition: all 0.3s ease;
}
.inf-module.is-complete .inf-module-dot {
  background: var(--success); border-color: var(--success);
  box-shadow: 0 0 8px rgba(52,211,153,0.3);
}

/* ═══ CARD ═══ */
.inf-card {
  background: var(--bg-card);
  backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 1.35rem 1.5rem;
  transition: all 0.35s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative; overflow: hidden;
}
.inf-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
  opacity: 0; transition: opacity 0.3s ease;
}
.inf-card:hover {
  background: var(--bg-card-hover); border-color: var(--border-hover);
  transform: translateY(-2px); box-shadow: 0 8px 32px rgba(0,0,0,0.3);
}
.inf-card:hover::before { opacity: 1; }
.inf-module.is-complete .inf-card { border-left: 2px solid var(--success); }

.inf-card-top { display: flex; align-items: center; gap: 0.65rem; margin-bottom: 0.3rem; }
.inf-step-num {
  font-size: 0.65rem; font-weight: 600;
  letter-spacing: 0.1em; text-transform: uppercase;
  padding: 0.15rem 0.55rem; border-radius: 6px; flex-shrink: 0;
  color: var(--python); background: var(--python-soft);
}
.inf-module.is-complete .inf-step-num { color: var(--success); background: var(--success-soft); }

.inf-card h4 {
  font-size: 0.95rem; font-weight: 500;
  color: var(--text-primary); margin: 0; line-height: 1.45;
}
.inf-card-desc {
  font-size: 0.82rem; color: var(--text-secondary);
  font-weight: 300; line-height: 1.7;
  margin: 0.25rem 0 1.1rem 0;
}
.inf-card-prereq {
  font-size: 0.72rem; color: var(--text-muted);
  margin: -0.2rem 0 0.9rem 0; font-style: italic;
}
.inf-card-prereq::before { content: '↗ '; color: var(--accent-3); }

/* Actions */
.inf-actions { display: flex; align-items: center; gap: 0.6rem; flex-wrap: wrap; }
.inf-btn {
  display: inline-flex; align-items: center; gap: 0.35rem;
  padding: 0.55rem 1rem; border-radius: 10px;
  font-size: 0.76rem; font-weight: 500;
  letter-spacing: 0.04em; text-transform: uppercase;
  text-decoration: none;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.03);
  color: var(--text-secondary) !important;
  transition: all 0.25s ease;
  cursor: pointer;
  font-family: 'Inter', -apple-system, sans-serif;
}
.inf-btn:hover {
  transform: translateY(-1px); border-color: var(--border-hover);
  background: rgba(255,255,255,0.08);
  color: var(--text-primary) !important;
  box-shadow: 0 4px 16px rgba(0,0,0,0.2);
  text-decoration: none;
}
.inf-btn--pdf:hover { border-color: rgba(59,130,246,0.4); box-shadow: 0 4px 16px rgba(59,130,246,0.1); }
.inf-btn--quiz:hover { border-color: rgba(99,102,241,0.4); box-shadow: 0 4px 16px rgba(99,102,241,0.1); }

.inf-check {
  margin-left: auto;
  display: flex; align-items: center; gap: 0.4rem;
  font-size: 0.72rem; color: var(--text-muted);
  cursor: pointer; padding: 0.35rem 0.55rem;
  border-radius: 8px; transition: all 0.2s ease; user-select: none;
}
.inf-check:hover { background: var(--success-soft); color: var(--success); }
.inf-check-box {
  width: 18px; height: 18px; border-radius: 6px;
  border: 1.5px solid var(--border);
  display: flex; align-items: center; justify-content: center;
  transition: all 0.2s ease; flex-shrink: 0;
}
.inf-check-box svg { opacity: 0; transition: opacity 0.2s ease; width: 11px; height: 11px; }
.inf-module.is-complete .inf-check-box {
  background: var(--success); border-color: var(--success);
  box-shadow: 0 0 8px rgba(52,211,153,0.2);
}
.inf-module.is-complete .inf-check-box svg { opacity: 1; }
.inf-module.is-complete .inf-check { color: var(--success); }

/* ═══ FOOTER ═══ */
.inf-footer {
  margin-top: 2rem; padding: 1.5rem 1.75rem;
  background: var(--bg-card); backdrop-filter: blur(20px);
  border: 1px solid var(--border); border-radius: 20px;
  display: flex; align-items: center;
  justify-content: space-between; flex-wrap: wrap; gap: 1rem;
}
.inf-footer-text { font-size: 0.8rem; color: var(--text-muted); font-weight: 300; }
.inf-footer-text strong { color: var(--text-secondary); font-weight: 500; }
.inf-footer-actions { display: flex; gap: 0.6rem; }
.inf-btn-reset {
  display: inline-flex; align-items: center;
  padding: 0.55rem 1rem; border-radius: 10px;
  font-size: 0.72rem; font-weight: 400; letter-spacing: 0.04em;
  border: 1px solid transparent; background: transparent;
  color: var(--text-muted) !important;
  transition: all 0.25s ease; cursor: pointer;
  font-family: 'Inter', -apple-system, sans-serif;
}
.inf-btn-reset:hover { border-color: var(--border); color: var(--text-secondary) !important; }

/* ═══ ANIMATIONS ═══ */
@keyframes inf-fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}
.inf-hero { animation: inf-fadeUp 0.6s ease both; }
.inf-section { animation: inf-fadeUp 0.6s ease both; animation-delay: 0.1s; }
.inf-module { animation: inf-fadeUp 0.4s ease both; }
.inf-module:nth-child(1) { animation-delay: 0.05s; }
.inf-module:nth-child(2) { animation-delay: 0.1s; }
.inf-module:nth-child(3) { animation-delay: 0.15s; }
.inf-module:nth-child(4) { animation-delay: 0.2s; }
.inf-module:nth-child(5) { animation-delay: 0.25s; }

/* ═══ RESPONSIVE ═══ */
@media (max-width: 768px) {
  .inf-content { padding: 1.5rem 1rem 4rem; }
  .inf-hero { padding: 2rem 1.5rem 1.5rem; border-radius: 20px; }
  .inf-hero h1 { font-size: 1.9rem; }
  .inf-path { padding-left: 2rem; }
  .inf-module-dot { left: -2rem; }
  .inf-card { padding: 1.1rem 1.2rem; }
  .inf-actions { flex-direction: column; align-items: stretch; }
  .inf-btn { justify-content: center; }
  .inf-check { margin-left: 0; justify-content: center; }
  .inf-footer { flex-direction: column; text-align: center; }
  .inf-footer-actions { width: 100%; flex-direction: column; }
  .inf-section-meta { padding-left: calc(36px + 0.85rem); }
}
</style>

<!-- AMBIENT -->
<div class="inf-ambient">
  <div class="inf-ambient-orb"></div>
  <div class="inf-ambient-orb"></div>
  <div class="inf-ambient-orb"></div>
</div>

<div class="inf-content">

  <!-- HERO -->
  <div class="inf-hero">
    <div class="inf-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Informatik</h1>
    <p class="inf-hero-sub">5 Module · Python-Programmierung von Grund auf</p>
    <div class="inf-progress-track">
      <div class="inf-progress-fill" id="infProgressBar"></div>
    </div>
    <div class="inf-progress-meta">
      <span><span id="infCompletedCount">0</span> von <span id="infTotalCount">5</span> Modulen</span>
      <span class="inf-pct" id="infProgressPercent">0 %</span>
    </div>
  </div>

  <!-- PYTHON -->
  <div class="inf-section">
    <div class="inf-section-head">
      <div class="inf-section-badge">Py</div>
      <h2 class="inf-section-title">Python</h2>
    </div>
    <p class="inf-section-meta">5 Module · Von print() bis Funktionen</p>
    <div class="inf-path">

      <div class="inf-module" data-module="p1">
        <div class="inf-module-dot"></div>
        <div class="inf-card">
          <div class="inf-card-top"><span class="inf-step-num">01</span><h4>Python Grundlagen – print() und input()</h4></div>
          <p class="inf-card-desc">Einführung in Python: Die print()-Funktion zur Ausgabe von Text und Zahlen, Parameter sep und end, input() für Benutzereingaben, Datentypen (str, int, float) und Umwandlung. Praktische Übungen zu Altersrechner, BMI und Einkaufslisten</p>
          <div class="inf-actions">
            <a href="/assets/pdfs/Info_1.pdf" class="inf-btn inf-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_python_grundlage.html" class="inf-btn inf-btn--quiz"><span>✎</span> Quiz</a>
            <label class="inf-check" onclick="infToggle('p1')"><span class="inf-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="inf-module" data-module="p2">
        <div class="inf-module-dot"></div>
        <div class="inf-card">
          <div class="inf-card-top"><span class="inf-step-num">02</span><h4>Variablen und Datentypen</h4></div>
          <p class="inf-card-desc">Variablen erstellen und verwenden, Datentypen unterscheiden (str, int, float, bool), Rechenoperationen und Operatoren, Typkonvertierung, Namenskonventionen. Übungen zu Kreisberechnungen und Temperaturumrechnung</p>
          <p class="inf-card-prereq">Baut auf: print() und input()</p>
          <div class="inf-actions">
            <a href="/assets/pdfs/Info_2.pdf" class="inf-btn inf-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_variablen_datentypen.html" class="inf-btn inf-btn--quiz"><span>✎</span> Quiz</a>
            <label class="inf-check" onclick="infToggle('p2')"><span class="inf-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="inf-module" data-module="p3">
        <div class="inf-module-dot"></div>
        <div class="inf-card">
          <div class="inf-card-top"><span class="inf-step-num">03</span><h4>Listen und Datenstrukturen</h4></div>
          <p class="inf-card-desc">Erstellen und Verstehen von Listen, Zugriff über Index und Slicing (start:stop:step), mutable Listen, append(), insert(), remove(), pop(), sort(), reverse(), index() und count()</p>
          <p class="inf-card-prereq">Baut auf: Variablen und Datentypen</p>
          <div class="inf-actions">
            <a href="/assets/pdfs/Info_3.pdf" class="inf-btn inf-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_listen_datenstrukturen.html" class="inf-btn inf-btn--quiz"><span>✎</span> Quiz</a>
            <label class="inf-check" onclick="infToggle('p3')"><span class="inf-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="inf-module" data-module="p4">
        <div class="inf-module-dot"></div>
        <div class="inf-card">
          <div class="inf-card-top"><span class="inf-step-num">04</span><h4>Kontrollstrukturen – if, for, while</h4></div>
          <p class="inf-card-desc">Bedingte Anweisungen mit if/elif/else, Vergleichs- und logische Operatoren, for-Schleifen über Sequenzen und range(), while-Schleifen, break und continue, verschachtelte Schleifen, Fehlersuche-Übungen</p>
          <p class="inf-card-prereq">Baut auf: Listen und Datenstrukturen</p>
          <div class="inf-actions">
            <a href="/assets/pdfs/Info_4.pdf" class="inf-btn inf-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_kontrollstrukturen.html" class="inf-btn inf-btn--quiz"><span>✎</span> Quiz</a>
            <label class="inf-check" onclick="infToggle('p4')"><span class="inf-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="inf-module" data-module="p5">
        <div class="inf-module-dot"></div>
        <div class="inf-card">
          <div class="inf-card-top"><span class="inf-step-num">05</span><h4>Funktionen in Python</h4></div>
          <p class="inf-card-desc">Funktionen definieren mit def, Parameter und Rückgabewerte, print vs. return, benannte Parameter und Standardwerte, Funktionen mit Kontrollstrukturen kombinieren, Funktionen die andere Funktionen aufrufen</p>
          <p class="inf-card-prereq">Baut auf: Kontrollstrukturen</p>
          <div class="inf-actions">
            <a href="/assets/pdfs/Info_5.pdf" class="inf-btn inf-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_funktionen.html" class="inf-btn inf-btn--quiz"><span>✎</span> Quiz</a>
            <label class="inf-check" onclick="infToggle('p5')"><span class="inf-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- FOOTER -->
  <div class="inf-footer">
    <div class="inf-footer-text"><strong>5 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar</div>
    <div class="inf-footer-actions">
      <a href="/teaching/" class="inf-btn">← Übersicht</a>
      <button class="inf-btn-reset" onclick="infReset()">Fortschritt zurücksetzen</button>
    </div>
  </div>

</div>

<!-- PROGRESS TRACKING -->
<script>
const INF_KEY = 'info-progress';
const INF_TOTAL = 5;

function infGetProgress() {
  try { return JSON.parse(localStorage.getItem(INF_KEY)) || {}; }
  catch(e) { return {}; }
}
function infSaveProgress(p) { localStorage.setItem(INF_KEY, JSON.stringify(p)); }

function infToggle(id) {
  const p = infGetProgress();
  if (p[id]) { delete p[id]; } else { p[id] = Date.now(); }
  infSaveProgress(p);
  infRender();
}

function infReset() {
  if (confirm('Fortschritt wirklich zurücksetzen?')) {
    localStorage.removeItem(INF_KEY);
    infRender();
  }
}

function infRender() {
  const p = infGetProgress();
  const c = Object.keys(p).length;
  const pct = Math.round((c / INF_TOTAL) * 100);
  document.getElementById('infProgressBar').style.width = pct + '%';
  document.getElementById('infCompletedCount').textContent = c;
  document.getElementById('infProgressPercent').textContent = pct + ' %';
  document.querySelectorAll('.inf-module').forEach(el => {
    const id = el.dataset.module;
    if (p[id]) { el.classList.add('is-complete'); }
    else { el.classList.remove('is-complete'); }
  });
}

document.addEventListener('DOMContentLoaded', infRender);
if (document.readyState !== 'loading') infRender();
</script>