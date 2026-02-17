---
layout: page
title: 
permalink: /teaching/vwl/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   APPLE DESIGN SYSTEM – VWL für Studienkolleg
   ═══════════════════════════════════════════════════════════════ */

/* ─── Design Tokens ─── */
:root {
  /* iOS/macOS Farbsystem */
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-indigo: #5856D6;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;
  --system-purple: #AF52DE;
  --system-red: #FF3B30;
  --system-teal: #5AC8FA;
  --system-yellow: #FFCC00;
  
  /* Semantische Farben */
  --mikro: #FF9500;
  --makro: #5AC8FA;
  
  /* Neutrale Palette */
  --gray-1: #F5F5F7;
  --gray-2: #E5E5EA;
  --gray-3: #D1D1D6;
  --gray-4: #C7C7CC;
  --gray-5: #AEAEB2;
  --gray-6: #8E8E93;
  --gray-7: #636366;
  --gray-8: #48484A;
  --gray-9: #3A3A3C;
  --gray-10: #2C2C2E;
  --gray-11: #1C1C1E;
  --gray-12: #000000;
  
  /* Dynamische Farben (Light/Dark Mode) */
  --bg-primary: #FFFFFF;
  --bg-secondary: #F5F5F7;
  --bg-tertiary: #FFFFFF;
  --text-primary: #000000;
  --text-secondary: #3A3A3C;
  --text-tertiary: #8E8E93;
  --separator: rgba(0, 0, 0, 0.08);
  --separator-strong: rgba(0, 0, 0, 0.16);
  
  /* Typografie */
  --font-stack: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", "Helvetica Neue", Helvetica, Arial, sans-serif;
  --font-mono: "SF Mono", SFMono-Regular, ui-monospace, Menlo, Monaco, monospace;
  
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
  --shadow-sm: 0 1px 2px rgba(0,0,0,0.04);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
  --shadow-lg: 0 12px 24px rgba(0,0,0,0.12);
  --shadow-xl: 0 24px 48px rgba(0,0,0,0.16);
  
  /* Transitions */
  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

/* Dark Mode Support */
@media (prefers-color-scheme: dark) {
  :root {
    --bg-primary: #000000;
    --bg-secondary: #1C1C1E;
    --bg-tertiary: #2C2C2E;
    --text-primary: #FFFFFF;
    --text-secondary: #EBEBF5;
    --text-tertiary: #8E8E93;
    --separator: rgba(255, 255, 255, 0.12);
    --separator-strong: rgba(255, 255, 255, 0.24);
    
    --shadow-sm: 0 1px 2px rgba(0,0,0,0.24);
    --shadow-md: 0 4px 12px rgba(0,0,0,0.32);
    --shadow-lg: 0 12px 24px rgba(0,0,0,0.48);
    --shadow-xl: 0 24px 48px rgba(0,0,0,0.64);
  }
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
  font-family: var(--font-stack);
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
  color: var(--system-indigo);
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
  content: '';
  width: 24px;
  height: 1px;
  background: var(--separator-strong);
}

.ma-hero h1 {
  font-size: 48px;
  font-weight: 700;
  letter-spacing: -0.003em;
  line-height: 1.08349;
  margin-bottom: var(--space-3);
  background: linear-gradient(135deg, var(--text-primary) 0%, var(--gray-6) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
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
  stroke: var(--separator);
  stroke-width: 8;
}

.ma-progress-ring-fill {
  fill: none;
  stroke: var(--system-indigo);
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

.ma-section--mikro .ma-section-icon { 
  background: rgba(255, 149, 0, 0.12); 
  color: var(--mikro);
}
.ma-section--makro .ma-section-icon { 
  background: rgba(90, 200, 250, 0.12); 
  color: var(--makro);
}

.ma-section-title-group {
  flex: 1;
}

.ma-section-title {
  font-size: 28px;
  font-weight: 600;
  letter-spacing: -0.021em;
  line-height: 1.14286;
  color: var(--text-primary);
  margin-bottom: var(--space-1);
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
  background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, transparent 50%);
  opacity: 0;
  transition: opacity var(--transition-base);
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
  border-color: var(--system-green);
  background: linear-gradient(135deg, rgba(52, 199, 89, 0.05) 0%, var(--bg-secondary) 100%);
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
  color: var(--system-indigo);
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
  background: var(--system-indigo);
  color: white !important;
}

.ma-btn--primary:hover {
  background: #0051D5;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 122, 255, 0.3);
}

.ma-btn--secondary {
  background: rgba(0, 0, 0, 0.05);
  color: var(--text-primary) !important;
}

@media (prefers-color-scheme: dark) {
  .ma-btn--secondary {
    background: rgba(255, 255, 255, 0.1);
  }
}

.ma-btn--secondary:hover {
  background: rgba(0, 0, 0, 0.1);
}

@media (prefers-color-scheme: dark) {
  .ma-btn--secondary:hover {
    background: rgba(255, 255, 255, 0.15);
  }
}

.ma-btn--ghost {
  background: transparent;
  color: var(--text-tertiary) !important;
  padding: var(--space-2);
}

.ma-btn--ghost:hover {
  color: var(--system-green) !important;
  background: rgba(52, 199, 89, 0.1);
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
  border: 2px solid var(--separator-strong);
  cursor: pointer;
  transition: all var(--transition-fast);
  position: relative;
  z-index: 2;
  padding: 0;
}

.ma-check:hover {
  border-color: var(--system-green);
  background: rgba(52, 199, 89, 0.05);
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
  background: var(--system-green);
  border-color: var(--system-green);
}

.ma-card-complete .ma-check svg {
  opacity: 1;
  transform: scale(1);
}

/* ─── Footer ─── */
.ma-footer {
  margin-top: var(--space-20);
  padding-top: var(--space-8);
  border-top: 1px solid var(--separator);
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
</style>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Volkswirtschaftslehre</h1>
    <p class="ma-hero-subtitle">13 Module für Mikroökonomie und Makroökonomie</p>
    
    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 13 abgeschlossen</div>
    </div>
  </div>

  <!-- Mikroökonomie -->
  <div class="ma-section ma-section--mikro">
    <div class="ma-section-header">
      <div class="ma-section-icon">📊</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Mikroökonomie</h2>
        <p class="ma-section-subtitle">8 Module · Vom Grundbegriff zum Marktmodell</p>
      </div>
    </div>
    <div class="ma-grid">

      <div class="ma-card" data-module="m1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Bedürfnis, Bedarf und Nachfrage</h4>
        </div>
        <p>Grundkonzepte der Wirtschaft: Definition und Unterscheidung von Bedürfnis, Bedarf und Nachfrage, Bedürfnisarten, Maslows Bedürfnispyramide</p>
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
        <p>Freie und wirtschaftliche Güter, inferiore und superiore Güter, Einkommenselastizität, meritorische und demeritorische Güter</p>
        <p class="ma-card-prereq">Baut auf: Bedürfnis, Bedarf und Nachfrage</p>
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
        <p>Gesetz des Angebots, Angebotsfunktion, aggregiertes Marktangebot, Verschiebung vs. Bewegung auf der Kurve</p>
        <p class="ma-card-prereq">Baut auf: Güterarten</p>
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
        <p>Gesetz der Nachfrage, Nachfragefunktion, aggregierte Marktnachfrage, Einflussfaktoren wie Einkommen und Präferenzen</p>
        <p class="ma-card-prereq">Baut auf: Angebot und Angebotskurve</p>
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
        <p>Gleichgewichtspreis und -menge, Angebots- und Nachfrageüberhang, Anpassungsprozesse, Steuern und Subventionen</p>
        <p class="ma-card-prereq">Baut auf: Angebot und Nachfrage</p>
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
        <p>Definition und Berechnung der Renten, ökonomische Wohlfahrt, Prohibitivpreis, graphische Darstellung</p>
        <p class="ma-card-prereq">Baut auf: Marktgleichgewicht</p>
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
        <p>Monopol, Oligopol, Polypol – Marktmacht, Marktstruktur, Vor- und Nachteile für Verbraucher</p>
        <p class="ma-card-prereq">Baut auf: Marktgleichgewicht</p>
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
        <p>Konsumentscheidungen: Budgetrestriktion, Gleichung und graphische Darstellung, Einkommens- und Preisänderungen, Opportunitätskosten</p>
        <p class="ma-card-prereq">Baut auf: Nachfrage und Güterarten</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_8-3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_budgetgerade.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m8', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

    </div>
  </div>

  <!-- Makroökonomie -->
  <div class="ma-section ma-section--makro">
    <div class="ma-section-header">
      <div class="ma-section-icon">🌐</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Makroökonomie</h2>
        <p class="ma-section-subtitle">5 Module · Von der Gesamtrechnung zur Wirtschaftspolitik</p>
      </div>
    </div>
    <div class="ma-grid">

      <div class="ma-card" data-module="m9">
        <div class="ma-card-header">
          <span class="ma-card-number">09</span>
          <h4>Volkswirtschaftliche Gesamtrechnung</h4>
        </div>
        <p>Definition und Ziele der VGR, Bruttoinlandsprodukt, drei Berechnungsmethoden, Inlandsprinzip vs. Inländerprinzip</p>
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
        <p>BIP-Deflator, BIP pro Kopf und Kaufkraftbereinigung, Grenzen des BIP, alternative Indikatoren (HDI, Gini-Koeffizient)</p>
        <p class="ma-card-prereq">Baut auf: Volkswirtschaftliche Gesamtrechnung</p>
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
        <p>Die 4 Konjunkturphasen, BIP-Berechnung, Wachstumsraten, Rezessionsdefinition, Früh- und Spätindikatoren</p>
        <p class="ma-card-prereq">Baut auf: Nominales vs. reales BIP</p>
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
        <p>Grundprinzipien antizyklischer Politik, Fiskal- und Geldpolitik, expansive vs. restriktive Maßnahmen, Finanzkrise 2008</p>
        <p class="ma-card-prereq">Baut auf: Konjunkturzyklen</p>
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
        <p>Arbeitslosenquote, drei Arten der Arbeitslosigkeit, Okun's Gesetz, aktive vs. passive Arbeitsmarktpolitik</p>
        <p class="ma-card-prereq">Baut auf: Konjunktur und Konjunkturpolitik</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_arbeitslosigkeit.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m13', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>13 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
      <button class="ma-btn ma-btn--ghost" onclick="resetProgress()">Zurücksetzen</button>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'vwl-progress';
const TOTAL_MODULES = 13;
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