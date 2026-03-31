---
layout: page
title: 
permalink: /teaching/informatik/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   JAPANDI DESIGN SYSTEM – Informatik für Studienkolleg
   ═══════════════════════════════════════════════════════════════ */

/* ─── Design Tokens ─── */
:root {
  --sumi: #1a1a18;
  --kuro: #2c2c28;
  --hai: #3d3d38;
  --kinari: #f0ece4;
  --shiro: #f7f5f0;
  --kinu: #e8e3d8;
  --ishi: #b8b3a8;
  --sugi: #8a8578;

  --beni: #c45c3e;
  --matcha: #7a8c6e;
  --ai: #5b7a8c;
  --kitsune: #c49a6c;
  --sakura: #c4868a;

  /* Semantische Farben */
  --python: var(--ai);

  --bg-primary: var(--shiro);
  --bg-secondary: var(--kinari);
  --bg-tertiary: var(--kinu);
  --text-primary: var(--sumi);
  --text-secondary: var(--sugi);
  --text-tertiary: var(--ishi);
  --border: rgba(26, 26, 24, 0.08);
  --border-strong: rgba(26, 26, 24, 0.15);

  /* Typografie */
  --font-display: 'Cormorant Garamond', 'Noto Serif JP', Georgia, serif;
  --font-body: 'Noto Sans', 'Noto Sans Arabic', 'Noto Sans SC', 'Noto Sans KR', 'Noto Sans JP', system-ui, sans-serif;
  --font-mono: 'SF Mono', 'Fira Code', monospace;
  
  /* Abstände (8-Punkt-Grid) */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  
  /* Radien */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 20px;
  --radius-2xl: 24px;
  --radius-full: 9999px;
  
  /* Schatten */
  --shadow-sm: 0 1px 2px rgba(var(--text-rgb),0.06);
  --shadow-md: 0 4px 12px rgba(var(--text-rgb),0.08);
  --shadow-lg: 0 12px 24px rgba(var(--text-rgb),0.12);
  --shadow-xl: 0 24px 48px rgba(0,0,0,0.64);
  
  /* Transitions */
  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

/* ─── Reset & Base ─── */
*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
  font-family: var(--font-body);
  line-height: 1.47059;
  letter-spacing: -0.022em;
}

.post-header, .page-heading, header.post-header { 
  display: none !important; 
}

/* ─── Container ─── */
.ma-container {
  max-width: 980px;
  margin: 0 auto;
  padding: var(--space-8) var(--space-5);
}

@media (min-width: 768px) {
  .ma-container {
    padding: var(--space-16) var(--space-8);
  }
}

/* ─── Hero Section ─── */
.ma-hero {
  text-align: center;
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}

.ma-hero-eyebrow {
  font-size: 17px;
  font-weight: 600;
  color: var(--text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: var(--space-3);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
}

.ma-hero-eyebrow::before,
.ma-hero-eyebrow::after {
  display: none;
}

.ma-hero h1 {
  font-size: 48px;
  font-weight: 300;
  letter-spacing: -0.003em;
  line-height: 1.08349;
  margin-bottom: var(--space-3);
  color: var(--text-primary);
  font-family: var(--font-display);
}

@media (min-width: 768px) {
  .ma-hero h1 {
    font-size: 64px;
  }
}

.ma-hero-subtitle {
  font-size: 21px;
  font-weight: 400;
  color: var(--text-secondary);
  margin-bottom: var(--space-8);
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  line-height: 1.381;
}

/* Progress Ring */
.ma-progress-container {
  display: inline-flex;
  flex-direction: column;
  align-items: center;
  gap: var(--space-4);
}

.ma-progress-ring {
  position: relative;
  width: 120px;
  height: 120px;
}

.ma-progress-ring svg {
  transform: rotate(-90deg);
  width: 100%;
  height: 100%;
}

.ma-progress-ring-bg {
  fill: none;
  stroke: var(--border);
  stroke-width: 8;
}

.ma-progress-ring-fill {
  fill: none;
  stroke: var(--accent, #b85c38);
  stroke-width: 8;
  stroke-linecap: round;
  stroke-dasharray: 339.292;
  stroke-dashoffset: 339.292;
  transition: stroke-dashoffset 1s cubic-bezier(0.16, 1, 0.3, 1);
}

.ma-progress-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 28px;
  font-weight: 600;
  color: var(--text-primary);
}

.ma-progress-label {
  font-size: 14px;
  color: var(--text-tertiary);
  font-weight: 500;
}

/* ─── Section Styling ─── */
.ma-section {
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) backwards;
}

.ma-section:nth-child(2) { animation-delay: 0.1s; }

.ma-section-header {
  display: flex;
  align-items: flex-start;
  gap: var(--space-4);
  margin-bottom: var(--space-6);
  padding: 0 var(--space-2);
}

.ma-section-icon {
  width: 48px;
  height: 48px;
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  flex-shrink: 0;
  background: var(--bg-secondary);
  transition: transform var(--transition-spring);
}

.ma-section:hover .ma-section-icon {
  transform: scale(1.1) rotate(-5deg);
}

.ma-section--python .ma-section-icon {
  background: rgba(91, 122, 140, 0.12);
  color: var(--python);
}

.ma-section-title-group {
  flex: 1;
}

.ma-section-title {
  font-size: 28px;
  font-weight: 300;
  letter-spacing: -0.021em;
  line-height: 1.14286;
  color: var(--text-primary);
  margin-bottom: var(--space-1);
  font-family: var(--font-display);
}

.ma-section-subtitle {
  font-size: 15px;
  color: var(--text-tertiary);
  font-weight: 400;
}

/* ─── Grid Layout ─── */
.ma-grid {
  display: grid;
  gap: var(--space-4);
}

@media (min-width: 768px) {
  .ma-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: var(--space-5);
  }
}

/* ─── Cards ─── */
.ma-card {
  background: var(--bg-secondary);
  border-radius: var(--radius-xl);
  padding: var(--space-5);
  position: relative;
  overflow: hidden;
  transition: all var(--transition-base);
  border: 2px solid transparent;
}

.ma-card::before {
  display: none;
}

.ma-card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
  background: var(--bg-tertiary);
}

.ma-card:hover::before {
  opacity: 1;
}

.ma-card:active {
  transform: scale(0.98);
  transition-duration: var(--transition-fast);
}

.ma-card-complete {
  border-color: var(--matcha);
  background: linear-gradient(135deg, rgba(122, 140, 110, 0.05) 0%, var(--bg-secondary) 100%);
}

.ma-card-header {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  margin-bottom: var(--space-3);
}

.ma-card-number {
  font-family: var(--font-mono);
  font-size: 12px;
  font-weight: 600;
  color: var(--text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.ma-section--python .ma-card-number { color: var(--python); }

.ma-card h4 {
  font-size: 17px;
  font-weight: 600;
  color: var(--text-primary);
  letter-spacing: -0.022em;
  line-height: 1.23536;
  margin: 0;
}

.ma-card p {
  font-size: 14px;
  line-height: 1.42859;
  color: var(--text-secondary);
  margin-bottom: var(--space-4);
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.ma-card-prereq {
  font-size: 12px;
  color: var(--text-tertiary);
  font-style: italic;
  margin-bottom: var(--space-4);
  margin-top: calc(-1 * var(--space-2));
}

.ma-card-prereq::before {
  content: '↗ ';
  color: var(--accent, #b85c38);
}

/* ─── Actions ─── */
.ma-actions {
  display: flex;
  gap: var(--space-2);
  flex-wrap: wrap;
  align-items: center;
}

.ma-btn {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-2) var(--space-3);
  border-radius: var(--radius-md);
  font-size: 13px;
  font-weight: 500;
  text-decoration: none;
  transition: all var(--transition-fast);
  border: none;
  cursor: pointer;
  font-family: inherit;
  position: relative;
  z-index: 2;
}

.ma-btn--primary {
  background: var(--accent, #b85c38);
  color: white !important;
}

.ma-btn--primary:hover {
  background: #a84a31;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(196, 92, 62, 0.3);
}

.ma-btn--secondary {
  background: rgba(255, 255, 255, 0.1);
  color: var(--text-primary) !important;
}

.ma-btn--secondary:hover {
  background: rgba(255, 255, 255, 0.15);
}

.ma-btn--ghost {
  background: transparent;
  color: var(--text-tertiary) !important;
  padding: var(--space-2);
}

.ma-btn--ghost:hover {
  color: var(--matcha) !important;
  background: rgba(122, 140, 110, 0.1);
}

/* ─── Check Button ─── */
.ma-check {
  margin-left: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 32px;
  height: 32px;
  border-radius: var(--radius-full);
  background: transparent;
  border: 2px solid var(--border-strong);
  cursor: pointer;
  transition: all var(--transition-fast);
  position: relative;
  z-index: 2;
  padding: 0;
}

.ma-check:hover {
  border-color: var(--matcha);
  background: rgba(122, 140, 110, 0.05);
}

.ma-check svg {
  width: 16px;
  height: 16px;
  color: white;
  opacity: 0;
  transform: scale(0.5);
  transition: all var(--transition-spring);
  pointer-events: none;
}

.ma-card-complete .ma-check {
  background: var(--matcha);
  border-color: var(--matcha);
}

.ma-card-complete .ma-check svg {
  opacity: 1;
  transform: scale(1);
}

/* ─── Footer ─── */
.ma-footer {
  margin-top: var(--space-20);
  padding-top: var(--space-8);
  border-top: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  gap: var(--space-5);
  align-items: center;
  text-align: center;
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.3s backwards;
}

@media (min-width: 768px) {
  .ma-footer {
    flex-direction: row;
    justify-content: space-between;
    text-align: left;
  }
}

.ma-footer-text {
  font-size: 12px;
  color: var(--text-tertiary);
}

.ma-footer-text strong {
  color: var(--text-secondary);
  font-weight: 600;
}

.ma-footer-actions {
  display: flex;
  gap: var(--space-3);
}

/* ─── Animations ─── */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ─── Reduced Motion ─── */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

/* ─── Touch Optimizations ─── */
@media (hover: none) {
  .ma-card:hover {
    transform: none;
    box-shadow: var(--shadow-sm);
  }
  
  .ma-card:active {
    transform: scale(0.98);
    background: var(--bg-tertiary);
  }
}

/* ─── Print Styles ─── */
@media print {
  .ma-btn, .ma-check { display: none; }
  .ma-card { break-inside: avoid; }
}

/* ─── Aufgabe des Tages ─── */
.adt {
  max-width: 980px;
  margin: 0 auto var(--space-12);
  padding: 0 var(--space-5);
}
@media (min-width: 768px) {
  .adt { padding: 0 var(--space-8); }
}
.adt-label {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: var(--space-3);
}
.adt-card {
  border: 1px solid var(--border-strong);
  border-radius: var(--radius-lg, 16px);
  padding: var(--space-8);
  background: var(--bg-elevated, rgba(255,255,255,0.03));
  transition: border-color 250ms;
}
.adt-card:hover { border-color: var(--border-hover, var(--border-strong)); }
.adt-meta {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  margin-bottom: var(--space-5);
  flex-wrap: wrap;
}
.adt-diff {
  font-size: 11px;
  color: var(--text-tertiary);
}
.adt-question {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 400;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  line-height: 1.45;
  margin-bottom: var(--space-3);
}
.adt-hint {
  font-size: 13px;
  color: var(--text-tertiary);
  font-weight: 300;
  line-height: 1.6;
  margin-bottom: var(--space-6);
  font-style: italic;
}
.adt-code {
  display: block;
  background: var(--bg-secondary, #3d3d38);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm, 8px);
  padding: var(--space-4);
  font-family: var(--font-mono);
  font-size: 13px;
  color: var(--text-primary);
  white-space: pre;
  overflow-x: auto;
  margin: var(--space-4) 0 var(--space-5);
  line-height: 1.6;
}
.adt-actions {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  flex-wrap: wrap;
}
.adt-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  font-weight: 500;
  padding: 8px 16px;
  border-radius: var(--radius-sm, 8px);
  border: 1px solid var(--border-strong);
  background: transparent;
  color: var(--text-primary);
  cursor: pointer;
  transition: all 200ms;
  text-decoration: none;
  font-family: var(--font-body);
}
.adt-btn:hover {
  background: var(--bg-elevated, rgba(255,255,255,0.06));
  border-color: var(--accent);
  color: var(--accent);
}
.adt-btn--accent {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
}
.adt-btn--accent:hover { opacity: 0.88; color: #fff; }
.adt-solution {
  display: none;
  margin-top: var(--space-5);
  padding-top: var(--space-5);
  border-top: 1px solid var(--border);
}
.adt-solution.visible {
  display: block;
  animation: adtFade 300ms ease;
}
@keyframes adtFade {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}
.adt-solution-label {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--matcha, #7a8c6e);
  margin-bottom: var(--space-3);
}
.adt-solution-text {
  font-size: 15px;
  color: var(--text-primary);
  line-height: 1.7;
  font-weight: 300;
}
.adt-solution-text code {
  font-family: var(--font-mono);
  font-size: 13px;
  background: var(--bg-secondary, #3d3d38);
  padding: 2px 6px;
  border-radius: 4px;
}
.adt-link {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  font-size: 13px;
  color: var(--text-tertiary);
  text-decoration: none;
  margin-top: var(--space-4);
  transition: color 200ms;
}
.adt-link:hover { color: var(--accent); }
@media (max-width: 480px) {
  .adt-question { font-size: 18px; }
  .adt-card { padding: var(--space-5); }
}
</style>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Informatik</h1>

    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 6 abgeschlossen</div>
    </div>
  </div>

  <!-- Aufgabe des Tages -->
  <div class="adt">
    <div class="adt-label">Aufgabe des Tages</div>
    <div class="adt-card">
      <div class="adt-meta">
        <span class="adt-diff" id="adt-diff"></span>
      </div>
      <div class="adt-question" id="adt-question"></div>
      <div class="adt-hint" id="adt-hint" style="display:none"></div>
      <div id="adt-code-wrap"></div>
      <div class="adt-actions">
        <button class="adt-btn adt-btn--accent" id="adt-toggle" onclick="window.adtToggle()">Antwort zeigen</button>
        <a class="adt-btn" id="adt-quiz" style="display:none">Quiz &rarr;</a>
      </div>
      <div class="adt-solution" id="adt-solution">
        <div class="adt-solution-label">Antwort</div>
        <div class="adt-solution-text" id="adt-answer"></div>
      </div>
    </div>
  </div>

  <!-- Python -->
  <div class="ma-grid">

      <div class="ma-card" data-module="p1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Python Grundlagen – print() und input()</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_python_grundlage.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p2">
        <div class="ma-card-header">
          <span class="ma-card-number">02</span>
          <h4>Variablen und Datentypen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_variablen_datentypen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p3">
        <div class="ma-card-header">
          <span class="ma-card-number">03</span>
          <h4>Listen und Datenstrukturen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_listen_datenstrukturen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p4">
        <div class="ma-card-header">
          <span class="ma-card-number">04</span>
          <h4>Kontrollstrukturen – if, for, while</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_kontrollstrukturen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p5">
        <div class="ma-card-header">
          <span class="ma-card-number">05</span>
          <h4>Funktionen in Python</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_5.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_funktionen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p6">
        <div class="ma-card-header">
          <span class="ma-card-number">06</span>
          <h4>NumPy – Kurvendiskussion & Ableitungen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_6.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_numpy_kurvendiskussion.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p6', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

    </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>6 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
      <button class="ma-btn ma-btn--ghost" onclick="resetProgress()">Zurücksetzen</button>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'info-progress';
const TOTAL_MODULES = 6;
const CIRCUMFERENCE = 339.292;

function getProgress() {
  try {
    return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {};
  } catch {
    return {};
  }
}

function saveProgress(progress) {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(progress));
}

function updateUI() {
  const progress = getProgress();
  const completed = Object.keys(progress).length;
  const percentage = Math.round((completed / TOTAL_MODULES) * 100);
  
  const offset = CIRCUMFERENCE - (percentage / 100) * CIRCUMFERENCE;
  document.getElementById('progressRing').style.strokeDashoffset = offset;
  document.getElementById('progressText').textContent = percentage + '%';
  document.getElementById('completedCount').textContent = completed;
  
  document.querySelectorAll('.ma-card').forEach(card => {
    const moduleId = card.dataset.module;
    if (progress[moduleId]) {
      card.classList.add('ma-card-complete');
    } else {
      card.classList.remove('ma-card-complete');
    }
  });
}

function toggleModule(id, event) {
  if (event) {
    event.preventDefault();
    event.stopPropagation();
  }
  
  const progress = getProgress();
  if (progress[id]) {
    delete progress[id];
  } else {
    progress[id] = Date.now();
  }
  saveProgress(progress);
  updateUI();
}

function resetProgress() {
  if (confirm('Möchtest du wirklich deinen gesamten Fortschritt zurücksetzen?')) {
    localStorage.removeItem(STORAGE_KEY);
    updateUI();
  }
}

document.addEventListener('DOMContentLoaded', updateUI);
if (document.readyState !== 'loading') updateUI();
</script>

<!-- Aufgabe des Tages Script -->
{% raw %}
<script>
(function() {
  var pool = [
    {
      diff: "Grundlagen",
      frage: "Was ist der Unterschied zwischen einer Liste und einem Tupel in Python?",
      antwort: "Listen sind veränderbar (mutable), Tupel unveränderbar (immutable). Listen: <code>[ ]</code>, Tupel: <code>( )</code>.",
      quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was gibt dieser Python-Code aus?",
      code: "x = [1, 2, 3, 4, 5]\nprint(x[1:4])",
      antwort: "<code>[2, 3, 4]</code> — Slicing geht von Index 1 (inklusive) bis 4 (exklusive).",
      quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html"
    },
    {
      diff: "Mittel",
      frage: "Schreibe eine Python-Funktion, die prüft, ob eine Zahl eine Primzahl ist.",
      hint: "Du brauchst nur bis zur Wurzel der Zahl zu prüfen.",
      code: "def ist_primzahl(n):\n    # Dein Code hier\n    pass",
      antwort: "<code>def ist_primzahl(n):</code><br><code>&nbsp;&nbsp;if n < 2: return False</code><br><code>&nbsp;&nbsp;for i in range(2, int(n**0.5)+1):</code><br><code>&nbsp;&nbsp;&nbsp;&nbsp;if n % i == 0: return False</code><br><code>&nbsp;&nbsp;return True</code>",
      quiz: "/assets/quizzes/quiz_kontrollstrukturen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was ist der Unterschied zwischen <code>=</code> und <code>==</code> in Python?",
      antwort: "<code>=</code> ist Zuweisung (speichert Wert). <code>==</code> ist Vergleich (prüft Gleichheit, ergibt <code>True</code>/<code>False</code>).",
      quiz: "/assets/quizzes/quiz_variablen_datentypen.html"
    },
    {
      diff: "Mittel",
      frage: "Was gibt dieser Code aus?",
      code: "for i in range(5):\n    if i % 2 == 0:\n        print(i, end=\" \")",
      antwort: "<code>0 2 4</code> — Die Schleife geht von 0 bis 4, die Bedingung filtert gerade Zahlen.",
      quiz: "/assets/quizzes/quiz_kontrollstrukturen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was gibt <code>type(3.14)</code> in Python zurück?",
      antwort: "<code>&lt;class 'float'&gt;</code> — 3.14 ist eine Gleitkommazahl (float).",
      quiz: "/assets/quizzes/quiz_variablen_datentypen.html"
    },
    {
      diff: "Mittel",
      frage: "Was ist der Unterschied zwischen <code>append()</code> und <code>extend()</code> bei Listen?",
      code: "a = [1, 2]\na.append([3, 4])\nprint(a)\n\nb = [1, 2]\nb.extend([3, 4])\nprint(b)",
      antwort: "<code>append</code> fügt das Argument als einzelnes Element hinzu: <code>[1, 2, [3, 4]]</code>. <code>extend</code> fügt jedes Element einzeln hinzu: <code>[1, 2, 3, 4]</code>.",
      quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was passiert bei diesem Code?",
      code: "name = input(\"Name: \")\nprint(\"Hallo, \" + name + \"!\")",
      antwort: "Das Programm fragt den Benutzer nach einem Namen und gibt dann eine Begrüßung aus, z.B. <code>Hallo, Anna!</code>.",
      quiz: "/assets/quizzes/quiz_python_grundlage.html"
    },
    {
      diff: "Mittel",
      frage: "Schreibe eine List Comprehension, die alle geraden Zahlen von 0 bis 20 in eine Liste packt.",
      antwort: "<code>gerade = [x for x in range(21) if x % 2 == 0]</code><br>Ergebnis: <code>[0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]</code>",
      quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Was gibt dieser Code aus?",
      code: "def mystery(n):\n    if n <= 1:\n        return n\n    return mystery(n-1) + mystery(n-2)\n\nprint(mystery(6))",
      hint: "Erkennst du das Muster?",
      antwort: "<code>8</code> — Die Funktion berechnet Fibonacci-Zahlen rekursiv. F(6) = F(5)+F(4) = 5+3 = 8.",
      quiz: "/assets/quizzes/quiz_kontrollstrukturen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Welche drei Kontrollstrukturen gibt es in Python?",
      antwort: "Sequenz (Anweisungen nacheinander), Selektion (<code>if/elif/else</code>), Iteration (<code>for</code>- und <code>while</code>-Schleifen).",
      quiz: "/assets/quizzes/quiz_kontrollstrukturen.html"
    },
    {
      diff: "Mittel",
      frage: "Was gibt dieser Code aus und warum?",
      code: "x = \"Python\"\nprint(x[::-1])",
      antwort: "<code>nohtyP</code> — <code>[::-1]</code> ist ein Slice mit Schritt -1, der den String umkehrt.",
      quiz: "/assets/quizzes/quiz_variablen_datentypen.html"
    }
  ];

  var dayOfYear = Math.floor((new Date() - new Date(new Date().getFullYear(),0,0)) / 86400000);
  var t = pool[dayOfYear % pool.length];

  var diffs = { "Grundlagen": "I", "Mittel": "II", "Klausurniveau": "III" };
  document.getElementById('adt-diff').textContent = (diffs[t.diff]||"") + " " + t.diff;
  document.getElementById('adt-question').innerHTML = t.frage;
  if (t.hint) { var h = document.getElementById('adt-hint'); h.textContent = t.hint; h.style.display = 'block'; }
  if (t.code) {
    var pre = document.createElement('code');
    pre.className = 'adt-code';
    pre.textContent = t.code;
    document.getElementById('adt-code-wrap').appendChild(pre);
  }
  document.getElementById('adt-answer').innerHTML = t.antwort;
  if (t.quiz) { var q = document.getElementById('adt-quiz'); q.href = t.quiz; q.style.display = 'inline-flex'; }

  window.adtToggle = function() {
    var sol = document.getElementById('adt-solution');
    sol.classList.toggle('visible');
    document.getElementById('adt-toggle').textContent = sol.classList.contains('visible') ? 'Antwort verbergen' : 'Antwort zeigen';
  };
})();
</script>
{% endraw %}