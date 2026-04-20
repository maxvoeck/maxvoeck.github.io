---
layout: page
title:
permalink: /teaching/mathematik-wkurs/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   和北 JAPANDI DESIGN SYSTEM – Mathematik W-Kurs (2. Semester)
   Identisch zum T-Kurs-Design, eigener Progress-Scope
   ═══════════════════════════════════════════════════════════════ */

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

  /* W-Kurs Themenfarben (Platzhalter – passen zum Japandi-Palette) */
  --wk-analysis: var(--ai);
  --wk-finanz:   var(--kitsune);
  --wk-stoch:    var(--sakura);
  --wk-lin:      var(--matcha);
  --wk-tools:    var(--beni);

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

  --space-1: 4px; --space-2: 8px; --space-3: 12px; --space-4: 16px;
  --space-5: 20px; --space-6: 24px; --space-8: 32px; --space-10: 40px;
  --space-12: 48px; --space-16: 64px; --space-20: 80px;

  --radius-sm: 8px; --radius-md: 12px; --radius-lg: 16px;
  --radius-xl: 20px; --radius-2xl: 24px; --radius-full: 9999px;

  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

*, *::before, *::after {
  box-sizing: border-box; margin: 0; padding: 0;
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

.post-header, .page-heading, header.post-header { display: none !important; }

.mw-container {
  max-width: 920px;
  margin: 0 auto;
  padding: var(--space-8) var(--space-5);
}
@media (min-width: 768px) {
  .mw-container { padding: var(--space-16) var(--space-8); }
}

/* ─── Hero ─── */
.mw-hero {
  text-align: center;
  margin-bottom: var(--space-16);
  animation: mwFadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}
.mw-hero-eyebrow {
  font-size: 17px;
  font-weight: 600;
  color: var(--text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: var(--space-3);
}
.mw-hero h1 {
  font-size: 48px;
  font-weight: 300;
  letter-spacing: -0.003em;
  line-height: 1.08349;
  margin-bottom: var(--space-3);
  color: var(--text-primary);
  font-family: var(--font-display);
}
@media (min-width: 768px) { .mw-hero h1 { font-size: 64px; } }

.mw-hero-subtitle {
  font-size: 17px;
  font-weight: 400;
  color: var(--text-secondary);
  margin: 0 auto var(--space-8);
  max-width: 600px;
  line-height: 1.5;
}

/* Progress Ring */
.mw-progress-container {
  display: inline-flex;
  flex-direction: column;
  align-items: center;
  gap: var(--space-4);
}
.mw-progress-ring { position: relative; width: 120px; height: 120px; }
.mw-progress-ring svg { transform: rotate(-90deg); width: 100%; height: 100%; }
.mw-progress-ring-bg { fill: none; stroke: var(--border-strong); stroke-width: 8; }
.mw-progress-ring-fill {
  fill: none;
  stroke: var(--beni);
  stroke-width: 8;
  stroke-linecap: round;
  stroke-dasharray: 339.292;
  stroke-dashoffset: 339.292;
  transition: stroke-dashoffset 1s cubic-bezier(0.16, 1, 0.3, 1);
}
.mw-progress-text {
  position: absolute; top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  font-size: 28px; font-weight: 600;
  color: var(--text-primary);
}
.mw-progress-label {
  font-size: 14px; color: var(--text-tertiary); font-weight: 500;
}

/* ─── Sections ─── */
.mw-section {
  margin-bottom: var(--space-16);
  animation: mwFadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) backwards;
}
.mw-section:nth-child(2) { animation-delay: 0.1s; }
.mw-section:nth-child(3) { animation-delay: 0.2s; }
.mw-section:nth-child(4) { animation-delay: 0.3s; }
.mw-section:nth-child(5) { animation-delay: 0.4s; }

.mw-section-header {
  display: flex;
  align-items: center;
  gap: var(--space-4);
  margin-bottom: var(--space-6);
  padding: var(--space-4);
  cursor: pointer;
  user-select: none;
  border-radius: var(--radius-lg);
  transition: background var(--transition-fast);
}
.mw-section-header:hover { background: var(--bg-secondary); }

.mw-section-title-group { flex: 1; }
.mw-section-title {
  font-size: 28px;
  font-weight: 600;
  letter-spacing: -0.021em;
  line-height: 1.14286;
  color: var(--text-primary);
  margin-bottom: var(--space-1);
  font-family: var(--font-display);
}
.mw-section-subtitle {
  font-size: 15px;
  color: var(--text-tertiary);
  font-weight: 400;
}
.mw-section-toggle {
  margin-left: auto;
  font-size: 20px;
  transition: transform var(--transition-base);
  color: var(--text-tertiary);
}
.mw-section.collapsed .mw-section-toggle { transform: rotate(-90deg); }

.mw-section .mw-grid {
  max-height: 5000px;
  opacity: 1;
  overflow: hidden;
  padding-top: 4px;
  transition: max-height 0.4s cubic-bezier(0.4, 0, 0.2, 1),
              opacity 0.25s ease;
}
.mw-section.collapsed .mw-grid {
  max-height: 0;
  opacity: 0;
  pointer-events: none;
}

/* ─── Grid & Cards ─── */
.mw-grid { display: grid; gap: var(--space-4); }
@media (min-width: 768px) {
  .mw-grid { grid-template-columns: repeat(2, 1fr); gap: var(--space-5); }
}

.mw-card {
  background: var(--bg-secondary);
  border-radius: var(--radius-xl);
  padding: var(--space-5);
  position: relative;
  overflow: hidden;
  transition: all var(--transition-base);
  border: 2px solid transparent;
}
.mw-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 24px rgba(0,0,0,0.08);
  background: var(--bg-tertiary);
}
.mw-card-complete {
  border-color: var(--matcha);
  background: linear-gradient(135deg, rgba(122, 140, 110, 0.08) 0%, var(--bg-secondary) 100%);
}

.mw-card-header {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  margin-bottom: var(--space-3);
}
.mw-card-number {
  font-family: var(--font-mono);
  font-size: 12px;
  font-weight: 600;
  color: var(--text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
.mw-card h4 {
  font-size: 17px;
  font-weight: 600;
  color: var(--text-primary);
  letter-spacing: -0.022em;
  line-height: 1.23536;
  margin: 0;
}

.mw-actions {
  display: flex;
  gap: var(--space-2);
  flex-wrap: wrap;
  align-items: center;
}
.mw-btn {
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
  font-family: var(--font-body);
  position: relative;
  z-index: 2;
}
.mw-btn--primary { background: var(--beni); color: white !important; }
.mw-btn--primary:hover { opacity: 0.9; transform: translateY(-1px); }
.mw-btn--secondary {
  background: rgba(26, 26, 24, 0.06);
  color: var(--text-primary) !important;
}
.mw-btn--secondary:hover { background: rgba(26, 26, 24, 0.1); }

.mw-check {
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
.mw-check:hover {
  border-color: var(--matcha);
  background: rgba(122, 140, 110, 0.08);
}
.mw-check svg {
  width: 16px;
  height: 16px;
  color: white;
  opacity: 0;
  transform: scale(0.5);
  transition: all var(--transition-spring);
  pointer-events: none;
}
.mw-card-complete .mw-check {
  background: var(--matcha);
  border-color: var(--matcha);
}
.mw-card-complete .mw-check svg {
  opacity: 1;
  transform: scale(1);
}

/* ─── Platzhalter (leeres Gerüst) ─── */
.mw-placeholder {
  padding: var(--space-8) var(--space-5);
  text-align: center;
  border: 1px dashed var(--border-strong);
  border-radius: var(--radius-lg);
  color: var(--text-tertiary);
  font-size: 14px;
  font-style: italic;
  background: var(--bg-secondary);
}
.mw-placeholder strong {
  display: block;
  font-style: normal;
  font-weight: 600;
  color: var(--text-secondary);
  margin-bottom: var(--space-2);
  font-size: 15px;
}

/* ─── Footer ─── */
.mw-footer {
  margin-top: var(--space-20);
  padding-top: var(--space-8);
  border-top: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  gap: var(--space-5);
  align-items: center;
  text-align: center;
}
@media (min-width: 768px) {
  .mw-footer {
    flex-direction: row;
    justify-content: space-between;
    text-align: left;
  }
}
.mw-footer-text { font-size: 12px; color: var(--text-tertiary); }
.mw-footer-text strong { color: var(--text-secondary); font-weight: 600; }
.mw-footer-actions { display: flex; gap: var(--space-3); }

/* ─── Animations ─── */
@keyframes mwFadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to   { opacity: 1; transform: translateY(0); }
}
@media (prefers-reduced-motion: reduce) {
  * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; }
}

/* ─── Mobile ─── */
@media (max-width: 600px) {
  .wrapper, .page-content, .post-content { padding-left: 0 !important; padding-right: 0 !important; }
  html, body { overflow-x: hidden; }
  .mw-container { padding: var(--space-6) var(--space-4); }
  .mw-hero { margin-bottom: var(--space-8); }
  .mw-hero h1 { font-size: 32px; margin-bottom: var(--space-2); }
  .mw-hero-subtitle { font-size: 15px; margin-bottom: var(--space-5); }
  .mw-progress-ring { width: 96px; height: 96px; }
  .mw-progress-text { font-size: 20px; }
  .mw-section-header { padding: var(--space-4) var(--space-3); gap: var(--space-3); min-height: 60px; }
  .mw-section-title { font-size: 18px; }
  .mw-section-subtitle { font-size: 12px; line-height: 1.4; }
  .mw-section-toggle { font-size: 16px; flex-shrink: 0; }
  .mw-card { padding: var(--space-4); }
  .mw-card h4 { font-size: 15px; }
  .mw-btn { padding: var(--space-2) var(--space-3); font-size: 13px; min-height: 44px; }
  .mw-check { width: 40px; height: 40px; flex-shrink: 0; }
  .mw-footer { margin-top: var(--space-12); flex-direction: column; text-align: center; }
}
</style>

<div class="mw-container">

  <!-- Hero -->
  <div class="mw-hero">
    <div class="mw-hero-eyebrow">Studienkolleg Leipzig · 2. Semester</div>
    <h1>Mathematik · W-Kurs</h1>
    <p class="mw-hero-subtitle">
      Materialsammlung für den wirtschaftswissenschaftlichen Schwerpunkt.
      Module und Aufgaben werden im Lauf des Semesters ergänzt.
    </p>

    <div class="mw-progress-container">
      <div class="mw-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="mw-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="mw-progress-ring-fill" id="mwProgressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="mw-progress-text" id="mwProgressText">0%</div>
      </div>
      <div class="mw-progress-label"><span id="mwCompletedCount">0</span> von <span id="mwTotalCount">0</span> abgeschlossen</div>
    </div>
  </div>

  <!-- Differentialrechnung -->
  <div class="mw-section">
    <div class="mw-section-header" onclick="mwToggleSection(this)">
      <div class="mw-section-title-group">
        <h2 class="mw-section-title">Differentialrechnung</h2>
      </div>
      <div class="mw-section-toggle">▼</div>
    </div>
    <div class="mw-grid">
      <div class="mw-card" data-module="wk-diff-01">
        <div class="mw-card-header">
          <span class="mw-card-number">01</span>
          <h4>Wiederholung Differentialrechnung</h4>
        </div>
        <div class="mw-actions">
          <a href="/assets/pdfs/WKurs_Wiederholung_Differentialrechnung.pdf" class="mw-btn mw-btn--primary" onclick="event.stopPropagation()">PDF</a>
          <button class="mw-check" onclick="mwToggleModule('wk-diff-01', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="mw-card" data-module="wk-diff-02">
        <div class="mw-card-header">
          <span class="mw-card-number">02</span>
          <h4>Extremwertaufgaben mit Nebenbedingung</h4>
        </div>
        <div class="mw-actions">
          <a href="/assets/pdfs/WKurs_Extremwertaufgaben_Nebenbedingung.pdf" class="mw-btn mw-btn--primary" onclick="event.stopPropagation()">PDF</a>
          <button class="mw-check" onclick="mwToggleModule('wk-diff-02', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <!-- Neue Karte 03 im Differentialrechnung-Abschnitt -->
<div class="mw-card" data-module="wk-diff-03">
  <div class="mw-card-header">
    <span class="mw-card-number">03</span>
    <h4>Extremwertaufgaben — Vertiefung</h4>
  </div>
  <div class="mw-actions">
    <a href="/assets/pdfs/Extremwertaufgaben_2.pdf" class="mw-btn mw-btn--primary" onclick="event.stopPropagation()">PDF</a>
    <button class="mw-check" onclick="mwToggleModule('wk-diff-03', event)" aria-label="Als erledigt markieren">
      <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
    </button>
  </div>
</div>

<div class="mw-card" data-module="wk-diff-04">
  <div class="mw-card-header">
    <span class="mw-card-number">04</span>
    <h4>Kurvendiskussion &amp; Ausblick Integralrechnung</h4>
  </div>
  <div class="mw-actions">
    <a href="/assets/pdfs/Kurvendiskusion_1.pdf" class="mw-btn mw-btn--primary" onclick="event.stopPropagation()">PDF</a>
    <button class="mw-check" onclick="mwToggleModule('wk-diff-04', event)" aria-label="Als erledigt markieren">
      <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
    </button>
  </div>
</div>

    </div>
  </div>

  <!-- Integralrechnung -->
<div class="mw-section">
  <div class="mw-section-header" onclick="mwToggleSection(this)">
    <div class="mw-section-title-group">
      <h2 class="mw-section-title">Integralrechnung</h2>
    </div>
    <div class="mw-section-toggle">▼</div>
  </div>
  <div class="mw-grid">

    <div class="mw-card" data-module="wk-int-01">
      <div class="mw-card-header">
        <span class="mw-card-number">01</span>
        <h4>Stammfunktion &amp; unbestimmtes Integral</h4>
      </div>
      <div class="mw-actions">
        <a href="/assets/pdfs/Stammfunktion.pdf" class="mw-btn mw-btn--primary" onclick="event.stopPropagation()">PDF</a>
        <button class="mw-check" onclick="mwToggleModule('wk-int-01', event)" aria-label="Als erledigt markieren">
          <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
        </button>
      </div>
    </div>

    <div class="mw-card" data-module="wk-int-02">
      <div class="mw-card-header">
        <span class="mw-card-number">02</span>
        <h4>Bestimmtes Integral &amp; Hauptsatz</h4>
      </div>
      <div class="mw-actions">
        <a href="/assets/pdfs/bestimmtes_integral.pdf" class="mw-btn mw-btn--primary" onclick="event.stopPropagation()">PDF</a>
        <button class="mw-check" onclick="mwToggleModule('wk-int-02', event)" aria-label="Als erledigt markieren">
          <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
        </button>
      </div>
    </div>

  <!-- Themenblock 3 -->
  <div class="mw-section collapsed">
    <div class="mw-section-header" onclick="mwToggleSection(this)">
      <div class="mw-section-title-group">
        <h2 class="mw-section-title">Themenblock 3</h2>
        <div class="mw-section-subtitle">Platzhalter – Inhalte folgen</div>
      </div>
      <div class="mw-section-toggle">▼</div>
    </div>
    <div class="mw-grid">
      <div class="mw-placeholder">
        <strong>Noch keine Module</strong>
        Hier erscheinen demnächst die Kapitel und Quizze für Themenblock&nbsp;3.
      </div>
    </div>
  </div>

  <!-- Footer -->
  <div class="mw-footer">
    <div class="mw-footer-text">
      <strong>W-Kurs · 2. Semester</strong> · Materialien werden laufend ergänzt
    </div>
    <div class="mw-footer-actions">
      <a href="/teaching/" class="mw-btn mw-btn--secondary">← Übersicht</a>
      <a href="/teaching/mathematik/" class="mw-btn mw-btn--secondary">T-Kurs Mathematik</a>
    </div>
  </div>

</div>

<script>
(function() {
  // Eigener Storage-Scope, damit der W-Kurs-Fortschritt nicht mit
  // dem T-Kurs-Fortschritt kollidiert.
  var STORAGE_KEY = 'math-wkurs-progress-v1';
  var CIRCUMFERENCE = 339.292;

  function getProgress() {
    try { return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {}; }
    catch (e) { return {}; }
  }
  function saveProgress(progress) {
    try { localStorage.setItem(STORAGE_KEY, JSON.stringify(progress)); }
    catch (e) { /* ignore */ }
  }

  // Gesamtanzahl dynamisch aus dem DOM — so funktioniert die Seite
  // auch, wenn später Module hinzugefügt werden, ohne dass ein
  // Konstantenwert angepasst werden muss.
  function getTotal() {
    return document.querySelectorAll('[data-module]').length;
  }

  window.mwToggleModule = function(moduleId, event) {
    event.preventDefault();
    event.stopPropagation();
    var progress = getProgress();
    var card = event.target.closest('[data-module]');
    if (progress[moduleId]) {
      delete progress[moduleId];
      if (card) card.classList.remove('mw-card-complete');
    } else {
      progress[moduleId] = true;
      if (card) card.classList.add('mw-card-complete');
    }
    saveProgress(progress);
    updateUI();
  };

  function updateUI() {
    var progress = getProgress();
    var total = getTotal();
    var completed = Object.keys(progress).filter(function(k) {
      return document.querySelector('[data-module="' + k + '"]');
    }).length;
    var percentage = total > 0 ? Math.round((completed / total) * 100) : 0;

    var ring = document.getElementById('mwProgressRing');
    var text = document.getElementById('mwProgressText');
    var count = document.getElementById('mwCompletedCount');
    var totalEl = document.getElementById('mwTotalCount');

    if (ring && text && count && totalEl) {
      var offset = CIRCUMFERENCE - (percentage / 100) * CIRCUMFERENCE;
      ring.style.strokeDashoffset = offset;
      text.textContent = percentage + '%';
      count.textContent = completed;
      totalEl.textContent = total;
    }

    document.querySelectorAll('[data-module]').forEach(function(card) {
      if (progress[card.dataset.module]) card.classList.add('mw-card-complete');
      else card.classList.remove('mw-card-complete');
    });
  }

  window.mwToggleSection = function(header) {
    var section = header.parentElement;
    section.classList.toggle('collapsed');
  };

  document.addEventListener('DOMContentLoaded', updateUI);
  if (document.readyState !== 'loading') updateUI();
})();
</script>
