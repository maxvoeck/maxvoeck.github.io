---
layout: page
title:
permalink: /teaching/vwl/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   JAPANDI DESIGN SYSTEM – VWL für Studienkolleg
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
  --mikro: var(--kitsune);
  --makro: var(--ai);

  --bg-primary: var(--shiro);
  --bg-secondary: var(--kinari);
  --bg-tertiary: var(--kinu);
  --text-primary: var(--sumi);
  --text-secondary: var(--sugi);
  --text-tertiary: var(--ishi);
  --border: rgba(26, 26, 24, 0.08);
  --border-strong: rgba(26, 26, 24, 0.15);

  --font-display: 'Cormorant Garamond', 'Noto Serif JP', Georgia, serif;
  --font-body: 'Noto Sans', 'Noto Sans Arabic', 'Noto Sans SC', 'Noto Sans KR', 'Noto Sans JP', system-ui, sans-serif;
  --font-mono: 'SF Mono', 'Fira Code', monospace;

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

  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 20px;
  --radius-2xl: 24px;
  --radius-full: 9999px;

  --shadow-sm: 0 1px 2px rgba(26, 26, 24, 0.06);
  --shadow-md: 0 4px 12px rgba(26, 26, 24, 0.08);
  --shadow-lg: 0 12px 24px rgba(26, 26, 24, 0.12);
  --shadow-xl: 0 24px 48px rgba(26, 26, 24, 0.3);

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

/* ─── Progress Ring ─── */
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
  stroke: var(--accent, #c45c3e);
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
.ma-section:nth-child(3) { animation-delay: 0.2s; }

.ma-section-header {
  display: flex;
  align-items: flex-start;
  gap: var(--space-4);
  margin-bottom: var(--space-6);
  padding: var(--space-4);
  cursor: pointer;
  user-select: none;
  border-radius: var(--radius-lg);
  transition: background var(--transition-fast);
}

.ma-section-header:hover {
  background: var(--bg-secondary);
}

.ma-section-toggle {
  margin-left: auto;
  font-size: 20px;
  transition: transform var(--transition-base);
  color: var(--text-tertiary);
  flex-shrink: 0;
}

.ma-section.collapsed .ma-section-toggle {
  transform: rotate(-90deg);
}

/* ─── Collapsible Grid ─── */
.ma-section .ma-grid {
  max-height: 5000px;
  opacity: 1;
  overflow: hidden;
  padding-top: 4px; /* Verhindert dass hover-translateY oben abgeschnitten wird */
  transition: max-height 0.4s cubic-bezier(0.4, 0, 0.2, 1),
              opacity 0.25s ease;
}

.ma-section.collapsed .ma-grid {
  max-height: 0;
  opacity: 0;
  pointer-events: none;
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

.ma-section--mikro .ma-section-icon {
  background: rgba(196, 154, 108, 0.12);
  color: var(--mikro);
}
.ma-section--makro .ma-section-icon {
  background: rgba(91, 122, 140, 0.12);
  color: var(--makro);
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
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(var(--text-rgb),0.03) 0%, transparent 50%);
  opacity: 0;
  transition: opacity var(--transition-base);
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

.ma-section--mikro .ma-card-number { color: var(--mikro); }
.ma-section--makro .ma-card-number { color: var(--makro); }

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
  color: var(--accent, #c45c3e);
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
  background: var(--accent, #c45c3e);
  color: white !important;
}

.ma-btn--primary:hover {
  background: #b85030;
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
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.4s backwards;
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
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ─── Reduced Motion ─── */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

/* ─── Mobile Optimierungen ─── */
@media (max-width: 600px) {
  .wrapper, .page-content, .post-content {
    padding-left: 0 !important;
    padding-right: 0 !important;
  }

  html, body {
    overflow-x: hidden;
  }

  .ma-container {
    padding: var(--space-6) var(--space-4);
  }

  .ma-hero {
    margin-bottom: var(--space-8);
  }

  .ma-hero h1 {
    font-size: 32px;
    margin-bottom: var(--space-2);
  }

  .ma-hero-subtitle {
    font-size: 15px;
    margin-bottom: var(--space-5);
    line-height: 1.5;
  }

  .ma-progress-ring {
    width: 96px;
    height: 96px;
  }

  .ma-progress-text {
    font-size: 20px;
  }

  .ma-progress-label {
    font-size: 13px;
  }

  .ma-section-header {
    padding: var(--space-4) var(--space-3);
    gap: var(--space-3);
    min-height: 60px;
    align-items: center;
  }

  .ma-section-icon {
    width: 40px;
    height: 40px;
    font-size: 18px;
  }

  .ma-section-title {
    font-size: 18px;
  }

  .ma-section-subtitle {
    font-size: 12px;
    line-height: 1.4;
  }

  .ma-section-toggle {
    font-size: 16px;
  }

  .ma-card {
    padding: var(--space-4);
  }

  .ma-card h4 {
    font-size: 15px;
  }

  .ma-card p {
    font-size: 13px;
    margin-bottom: var(--space-3);
  }

  .ma-btn {
    padding: var(--space-2) var(--space-3);
    font-size: 13px;
    min-height: 44px;
  }

  .ma-check {
    width: 40px;
    height: 40px;
    flex-shrink: 0;
  }

  .ma-footer {
    margin-top: var(--space-12);
    flex-direction: column;
    text-align: center;
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

<!-- KaTeX for VWL formulas -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.js"></script>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Volkswirtschaftslehre</h1>

    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 14 abgeschlossen</div>
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

  <!-- Mikroökonomie -->
  <div class="ma-section ma-section--mikro collapsed">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Mikroökonomie</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="m1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Bedürfnis, Bedarf und Nachfrage</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_1-3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
      <div class="ma-card" data-module="m2">
        <div class="ma-card-header">
          <span class="ma-card-number">02</span>
          <h4>Güterarten in der Wirtschaft</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_2-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_gueterarten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m3">
        <div class="ma-card-header">
          <span class="ma-card-number">03</span>
          <h4>Angebot und Angebotskurve</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_3-4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_angebot.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m4">
        <div class="ma-card-header">
          <span class="ma-card-number">04</span>
          <h4>Nachfrage und Nachfragekurve</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_4-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_nachfrage.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m5">
        <div class="ma-card-header">
          <span class="ma-card-number">05</span>
          <h4>Marktgleichgewicht</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_5-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_marktgleichgewicht.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m6">
        <div class="ma-card-header">
          <span class="ma-card-number">06</span>
          <h4>Konsumenten- und Produzentenrente</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_6.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_renten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m6', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m7">
        <div class="ma-card-header">
          <span class="ma-card-number">07</span>
          <h4>Marktformen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_7.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_marktformen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m7', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m8">
        <div class="ma-card-header">
          <span class="ma-card-number">08</span>
          <h4>Budgetgerade</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_8-3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_budgetgerade.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m8', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card ma-card--exam">
  <div class="ma-card-header">
    <span class="ma-card-number" style="color: var(--beni);">✦</span>
    <h4>Klausur Mikroökonomie</h4>
  </div>
  <p style="font-size:13px; color: var(--text-tertiary); margin-bottom: var(--space-4);">
    Übungsklausur zu allen Mikrothemen
  </p>
  <div class="ma-actions">
    <a href="/assets/pdfs/Übungsheft_W_1.pdf" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">PDF</a>
  </div>
</div>



    </div>
  </div>

  <!-- Makroökonomie -->
  <div class="ma-section ma-section--makro collapsed">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Makroökonomie</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid">

      <div class="ma-card" data-module="m9">
        <div class="ma-card-header">
          <span class="ma-card-number">09</span>
          <h4>Volkswirtschaftliche Gesamtrechnung</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_11.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vgr.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m9', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m10">
        <div class="ma-card-header">
          <span class="ma-card-number">10</span>
          <h4>Nominales vs. reales BIP</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_12.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vgr2.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m10', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m11">
        <div class="ma-card-header">
          <span class="ma-card-number">11</span>
          <h4>Konjunktur & Konjunkturzyklen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_11_Konjunktur.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_konjunktur.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m11', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m12">
        <div class="ma-card-header">
          <span class="ma-card-number">12</span>
          <h4>Antizyklische Konjunkturpolitik</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_12_Konjunkturpolitik.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_konjunkturpolitik.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m12', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m13">
        <div class="ma-card-header">
          <span class="ma-card-number">13</span>
          <h4>Arbeitslosigkeit & Arbeitsmarktpolitik</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_arbeitslosigkeit.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m13', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m14">
        <div class="ma-card-header">
          <span class="ma-card-number">14</span>
          <h4>Inflation & Preisniveaustabilität</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_14_Preisniveau.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_preisniveau.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m14', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m15">
  <div class="ma-card-header">
    <span class="ma-card-number">15</span>
    <h4>Magisches Viereck</h4>
  </div>
  <div class="ma-actions">
    <a href="/assets/pdfs/VWL_15.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
    <a href="/assets/quizzes/quiz_magisches_viereck.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
    <button class="ma-check" onclick="toggleModule('m15', event)" aria-label="Als erledigt markieren">
      <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
    </button>
  </div>
  <div class="ma-card ma-card--exam">
  <div class="ma-card-header">
    <span class="ma-card-number" style="color: var(--ai);">✦</span>
    <h4>Klausur Makroökonomie</h4>
  </div>
  <p style="font-size:13px; color: var(--text-tertiary); margin-bottom: var(--space-4);">
    Übungsklausur zu allen Makrothemen
  </p>
  <div class="ma-actions">
    <a href="/assets/pdfs/Klausur_Makro.pdf" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">PDF</a>
  </div>
</div>
</div>

    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>14 Module</strong> · Mikroökonomie & Makroökonomie
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
      <button class="ma-btn ma-btn--ghost" onclick="resetProgress()">Zurücksetzen</button>
    </div>
  </div>

  

</div>

<script>
const STORAGE_KEY = 'vwl-progress';
const TOTAL_MODULES = 14;
const CIRCUMFERENCE = 339.292;

function getProgress() {
  try {
    return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {};
  } catch {
    return {};
  }
}

function saveProgress(progress) {
  try {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(progress));
  } catch {
    console.warn('Failed to save progress to localStorage');
  }
}

function updateUI() {
  const progress = getProgress();
  const completed = Object.keys(progress).length;
  const percentage = Math.round((completed / TOTAL_MODULES) * 100);

  const ring = document.getElementById('progressRing');
  const text = document.getElementById('progressText');
  const count = document.getElementById('completedCount');

  if (ring && text && count) {
    const offset = CIRCUMFERENCE - (percentage / 100) * CIRCUMFERENCE;
    ring.style.strokeDashoffset = offset;
    text.textContent = percentage + '%';
    count.textContent = completed;
  }

  document.querySelectorAll('[data-module]').forEach(card => {
    if (progress[card.dataset.module]) {
      card.classList.add('ma-card-complete');
    } else {
      card.classList.remove('ma-card-complete');
    }
  });
}

function toggleModule(moduleId, event) {
  event.preventDefault();
  event.stopPropagation();

  const progress = getProgress();
  const card = event.target.closest('[data-module]');

  if (progress[moduleId]) {
    delete progress[moduleId];
    if (card) card.classList.remove('ma-card-complete');
  } else {
    progress[moduleId] = true;
    if (card) card.classList.add('ma-card-complete');
  }

  saveProgress(progress);
  updateUI();
}

function toggleSection(header) {
  const section = header.parentElement;
  section.classList.toggle('collapsed');
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
      frage: "Was ist der Unterschied zwischen einem Bedürfnis, einem Bedarf und der Nachfrage?",
      antwort: "Bedürfnis = Mangelempfinden (z.B. Hunger). Bedarf = auf ein konkretes Gut gerichtet (z.B. Pizza). Nachfrage = Bedarf tritt mit Kaufkraft am Markt auf.",
      quiz: "/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html"
    },
    {
      diff: "Grundlagen",
      frage: "Nenne drei Merkmale eines vollkommenen Marktes.",
      antwort: "Homogene Güter, vollständige Markttransparenz, keine persönlichen/zeitlichen/räumlichen Präferenzen.",
      quiz: "/assets/quizzes/quiz_marktformen.html"
    },
    {
      diff: "Mittel",
      frage: "Nachfrage: $p = 100 - 2q$, Angebot: $p = 20 + 3q$. Bestimme Gleichgewichtspreis und -menge.",
      antwort: "$100 - 2q = 20 + 3q \\Rightarrow q^* = 16$. Einsetzen: $p^* = 68$.",
      quiz: "/assets/quizzes/quiz_marktgleichgewicht.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was versteht man unter einem öffentlichen Gut? Nenne ein Beispiel.",
      antwort: "Nicht-rivalisierend und nicht-ausschließbar. Beispiele: Straßenbeleuchtung, Landesverteidigung.",
      quiz: "/assets/quizzes/quiz_gueterarten.html"
    },
    {
      diff: "Mittel",
      frage: "Erkläre das Gesetz der Nachfrage und warum die Nachfragekurve fallend verläuft.",
      antwort: "Steigt der Preis, sinkt die nachgefragte Menge (ceteris paribus). Grund: Substitutionseffekt (Ausweichen auf günstigere Alternativen) und Einkommenseffekt (reale Kaufkraft sinkt).",
      quiz: "/assets/quizzes/quiz_nachfrage.html"
    },
    {
      diff: "Mittel",
      frage: "Nenne die vier Phasen eines Konjunkturzyklus.",
      antwort: "Aufschwung (Expansion), Hochkonjunktur (Boom), Abschwung (Rezession), Tiefstand (Depression).",
      quiz: "/assets/quizzes/quiz_konjunktur.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Erkläre den Unterschied zwischen Entstehungs-, Verwendungs- und Verteilungsrechnung des BIP.",
      antwort: "Entstehung: Summe der Bruttowertschöpfung. Verwendung: $BIP = C + I + G + (Ex - Im)$. Verteilung: Summe aus Arbeitnehmerentgelten, Gewinnen, Abschreibungen, Produktionsabgaben.",
      quiz: "/assets/quizzes/quiz_vgr.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was ist Inflation und wie wird sie gemessen?",
      antwort: "Anhaltender Anstieg des allgemeinen Preisniveaus. Gemessen über den Verbraucherpreisindex (VPI) eines repräsentativen Warenkorbs.",
      quiz: "/assets/quizzes/quiz_preisniveau.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was versteht man unter dem ökonomischen Prinzip? Nenne die zwei Ausprägungen.",
      antwort: "Maximalprinzip: Mit gegebenen Mitteln den größtmöglichen Erfolg erzielen. Minimalprinzip: Ein bestimmtes Ziel mit möglichst geringem Aufwand erreichen.",
      quiz: "/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html"
    },
    {
      diff: "Mittel",
      frage: "Was passiert am Markt, wenn der Staat einen Höchstpreis unter dem Gleichgewichtspreis festlegt?",
      hint: "Denke an Angebot und Nachfrage bei diesem Preis.",
      antwort: "Es entsteht eine Überschussnachfrage (Nachfrage > Angebot). Die nachgefragte Menge übersteigt die angebotene Menge, es kommt zu Versorgungsengpässen.",
      quiz: "/assets/quizzes/quiz_marktgleichgewicht.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Erkläre, wie eine expansive Geldpolitik der Zentralbank die Konjunktur beeinflusst.",
      antwort: "Senkung des Leitzinses → günstigere Kredite → mehr Investitionen und Konsum → höhere Gesamtnachfrage → BIP steigt → kann aber auch Inflation fördern.",
      quiz: "/assets/quizzes/quiz_konjunkturpolitik.html"
    },
    {
      diff: "Mittel",
      frage: "Was ist die Budgetgerade und wovon hängt ihre Lage ab?",
      antwort: "Die Budgetgerade zeigt alle Güterkombinationen, die ein Haushalt bei gegebenem Einkommen und gegebenen Preisen kaufen kann. Lage hängt ab von: Einkommen (Parallelverschiebung) und Preisen der Güter (Drehung).",
      quiz: "/assets/quizzes/quiz_budgetgerade.html"
    },
    {
      diff: "Grundlagen",
      frage: "Was unterscheidet ein Oligopol von einem Polypol?",
      antwort: "Oligopol: wenige Anbieter, die sich gegenseitig beobachten und beeinflussen. Polypol: viele kleine Anbieter, die keinen individuellen Einfluss auf den Marktpreis haben.",
      quiz: "/assets/quizzes/quiz_marktformen.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Nenne drei Arten von Arbeitslosigkeit und erkläre sie kurz.",
      antwort: "Friktionelle (Sucharbeitslosigkeit beim Jobwechsel), saisonale (wetterbedingt, z.B. Bau im Winter), konjunkturelle (durch Nachfragerückgang in der Rezession). Dazu: strukturelle (durch Wandel der Wirtschaft).",
      quiz: "/assets/quizzes/quiz_arbeitslosigkeit.html"
    }
  ];

  function renderMath(el) {
    var html = el.innerHTML;
    html = html.replace(/\$\$([\s\S]+?)\$\$/g, function(m, tex) {
      var s = document.createElement('span');
      try { katex.render(tex.trim(), s, { displayMode: true, throwOnError: false }); } catch(e) { s.textContent = tex; }
      return s.outerHTML;
    });
    html = html.replace(/\$([^\$]+?)\$/g, function(m, tex) {
      var s = document.createElement('span');
      try { katex.render(tex.trim(), s, { displayMode: false, throwOnError: false }); } catch(e) { s.textContent = tex; }
      return s.outerHTML;
    });
    el.innerHTML = html;
  }

  var dayOfYear = Math.floor((new Date() - new Date(new Date().getFullYear(),0,0)) / 86400000);
  var t = pool[dayOfYear % pool.length];

  var diffs = { "Grundlagen": "I", "Mittel": "II", "Klausurniveau": "III" };
  document.getElementById('adt-diff').textContent = (diffs[t.diff]||"") + " " + t.diff;
  var qEl = document.getElementById('adt-question');
  qEl.innerHTML = t.frage; renderMath(qEl);
  if (t.hint) { var h = document.getElementById('adt-hint'); h.textContent = t.hint; h.style.display = 'block'; }
  var aEl = document.getElementById('adt-answer');
  aEl.innerHTML = t.antwort; renderMath(aEl);
  if (t.quiz) { var q = document.getElementById('adt-quiz'); q.href = t.quiz; q.style.display = 'inline-flex'; }

  window.adtToggle = function() {
    var sol = document.getElementById('adt-solution');
    sol.classList.toggle('visible');
    document.getElementById('adt-toggle').textContent = sol.classList.contains('visible') ? 'Antwort verbergen' : 'Antwort zeigen';
  };
})();
</script>
{% endraw %}
