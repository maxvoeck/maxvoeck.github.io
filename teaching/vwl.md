---
layout: page
title: 
permalink: /teaching/vwl/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Instrument+Serif:ital@0;1&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap');

/* ═══════════════════════════════════════
   DESIGN SYSTEM – Japandi Learning Platform
   ═══════════════════════════════════════ */

:root {
  --bg: #f5f2ed;
  --surface: #ffffff;
  --surface-hover: #fafaf8;
  --border: #e8e4dc;
  --border-light: #f0ede7;
  
  --text-primary: #2c2c2c;
  --text-secondary: #6b6560;
  --text-muted: #9b9590;
  
  --mikro: #b8a89a;
  --mikro-deep: #9a8a7a;
  --mikro-light: rgba(184, 168, 154, 0.08);
  
  --makro: #8b9e9f;
  --makro-deep: #6d8486;
  --makro-light: rgba(139, 158, 159, 0.08);
  
  --accent: #c9b896;
  --success: #7a9e7e;
  --success-light: rgba(122, 158, 126, 0.1);
  
  --radius-sm: 10px;
  --radius-md: 16px;
  --radius-lg: 24px;
  --radius-xl: 32px;
}

body {
  background: var(--bg);
  font-family: 'DM Sans', -apple-system, sans-serif;
  line-height: 1.7;
  color: var(--text-primary);
}

/* ═══════════════════════════════════════
   HERO / HEADER
   ═══════════════════════════════════════ */

.lp-hero {
  background: var(--surface);
  padding: 3rem 2.5rem 2.5rem;
  margin: -2rem -2rem 0 -2rem;
  border-bottom: 1px solid var(--border);
  border-radius: 0 0 var(--radius-xl) var(--radius-xl);
  position: relative;
  overflow: hidden;
}

.lp-hero::before {
  content: '';
  position: absolute;
  top: -80px;
  right: -40px;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(184, 168, 154, 0.06) 0%, transparent 65%);
  border-radius: 50%;
}

.lp-hero::after {
  content: '';
  position: absolute;
  bottom: -60px;
  right: 120px;
  width: 180px;
  height: 180px;
  background: radial-gradient(circle, rgba(139, 158, 159, 0.05) 0%, transparent 65%);
  border-radius: 50%;
}

.lp-hero-content {
  position: relative;
  z-index: 1;
}

.lp-hero h1 {
  font-family: 'Instrument Serif', Georgia, serif;
  font-size: 2.4rem;
  font-weight: 400;
  color: var(--text-primary);
  margin: 0 0 0.5rem 0;
  letter-spacing: -0.01em;
  line-height: 1.2;
}

.lp-hero-subtitle {
  font-size: 0.95rem;
  color: var(--text-secondary);
  margin: 0 0 2rem 0;
  font-weight: 300;
}

/* Progress Overview */
.lp-progress-bar-outer {
  background: var(--border-light);
  border-radius: 100px;
  height: 6px;
  overflow: hidden;
  margin-bottom: 0.75rem;
}

.lp-progress-bar-inner {
  height: 100%;
  border-radius: 100px;
  background: linear-gradient(90deg, var(--mikro) 0%, var(--makro) 100%);
  transition: width 0.8s cubic-bezier(0.23, 1, 0.32, 1);
  width: 0%;
}

.lp-progress-stats {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.lp-progress-text {
  font-size: 0.8rem;
  color: var(--text-muted);
  font-weight: 400;
  letter-spacing: 0.03em;
}

.lp-progress-percent {
  font-size: 0.8rem;
  color: var(--text-secondary);
  font-weight: 500;
}

/* ═══════════════════════════════════════
   LEARNING PATH SECTION
   ═══════════════════════════════════════ */

.lp-section {
  margin: 3rem 0 0 0;
}

.lp-section-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 0.5rem;
  padding: 0 0.25rem;
}

.lp-section-icon {
  width: 36px;
  height: 36px;
  border-radius: var(--radius-sm);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  flex-shrink: 0;
}

.lp-section--mikro .lp-section-icon {
  background: var(--mikro-light);
  color: var(--mikro-deep);
  border: 1px solid rgba(184, 168, 154, 0.15);
}

.lp-section--makro .lp-section-icon {
  background: var(--makro-light);
  color: var(--makro-deep);
  border: 1px solid rgba(139, 158, 159, 0.15);
}

.lp-section-title {
  font-family: 'Instrument Serif', Georgia, serif;
  font-size: 1.5rem;
  font-weight: 400;
  color: var(--text-primary);
  margin: 0;
  letter-spacing: -0.005em;
}

.lp-section-meta {
  font-size: 0.82rem;
  color: var(--text-muted);
  padding: 0 0.25rem 0 calc(36px + 1rem);
  margin-bottom: 1.75rem;
}

/* ═══════════════════════════════════════
   LEARNING PATH – VERTICAL TIMELINE
   ═══════════════════════════════════════ */

.lp-path {
  position: relative;
  padding-left: 2.5rem;
}

/* Vertical connector line */
.lp-path::before {
  content: '';
  position: absolute;
  left: 17px;
  top: 24px;
  bottom: 24px;
  width: 1px;
  background: var(--border);
}

/* ═══════════════════════════════════════
   MODULE CARD
   ═══════════════════════════════════════ */

.lp-module {
  position: relative;
  margin-bottom: 1rem;
}

/* Step dot on the timeline */
.lp-module-dot {
  position: absolute;
  left: -2.5rem;
  top: 50%;
  transform: translateY(-50%);
  width: 11px;
  height: 11px;
  border-radius: 50%;
  background: var(--surface);
  border: 2px solid var(--border);
  z-index: 2;
  transition: all 0.3s ease;
}

.lp-module.is-complete .lp-module-dot {
  background: var(--success);
  border-color: var(--success);
  box-shadow: 0 0 0 3px var(--success-light);
}

.lp-module-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius-md);
  padding: 1.5rem 1.75rem;
  transition: all 0.35s cubic-bezier(0.23, 1, 0.32, 1);
  cursor: default;
  position: relative;
}

.lp-module-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.06);
  border-color: #d8d4cc;
}

.lp-module.is-complete .lp-module-card {
  border-left: 2px solid var(--success);
}

/* Step number + title row */
.lp-module-top {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
  margin-bottom: 0.5rem;
}

.lp-module-step {
  font-size: 0.7rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-muted);
  background: var(--border-light);
  padding: 0.2rem 0.55rem;
  border-radius: 6px;
  white-space: nowrap;
  margin-top: 0.15rem;
  flex-shrink: 0;
}

.lp-section--mikro .lp-module-step {
  color: var(--mikro-deep);
  background: var(--mikro-light);
}

.lp-section--makro .lp-module-step {
  color: var(--makro-deep);
  background: var(--makro-light);
}

.lp-module.is-complete .lp-module-step {
  color: var(--success);
  background: var(--success-light);
}

.lp-module-title {
  font-size: 1rem;
  font-weight: 500;
  color: var(--text-primary);
  margin: 0;
  line-height: 1.5;
}

.lp-module-desc {
  font-size: 0.84rem;
  color: var(--text-secondary);
  line-height: 1.75;
  margin: 0.25rem 0 1.25rem 0;
  font-weight: 300;
}

/* Prerequisite hint */
.lp-module-prereq {
  font-size: 0.75rem;
  color: var(--text-muted);
  font-style: italic;
  margin: -0.25rem 0 1rem 0;
}

.lp-module-prereq::before {
  content: '↗ ';
}

/* Actions row */
.lp-module-actions {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  flex-wrap: wrap;
}

.lp-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.6rem 1.1rem;
  border-radius: var(--radius-sm);
  font-size: 0.8rem;
  font-weight: 500;
  letter-spacing: 0.04em;
  text-decoration: none;
  transition: all 0.25s ease;
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text-secondary) !important;
  cursor: pointer;
  text-transform: uppercase;
}

.lp-btn:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.lp-btn--pdf:hover {
  background: var(--mikro);
  border-color: var(--mikro);
  color: #fff !important;
}

.lp-section--makro .lp-btn--pdf:hover {
  background: var(--makro);
  border-color: var(--makro);
}

.lp-btn--quiz:hover {
  background: var(--text-primary);
  border-color: var(--text-primary);
  color: #fff !important;
}

.lp-btn--icon {
  font-size: 0.85rem;
}

/* Completion toggle */
.lp-check {
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 0.4rem;
  font-size: 0.75rem;
  color: var(--text-muted);
  cursor: pointer;
  user-select: none;
  padding: 0.4rem 0.6rem;
  border-radius: 8px;
  transition: all 0.2s ease;
}

.lp-check:hover {
  background: var(--success-light);
  color: var(--success);
}

.lp-check-box {
  width: 18px;
  height: 18px;
  border-radius: 6px;
  border: 1.5px solid var(--border);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s ease;
  flex-shrink: 0;
  background: var(--surface);
}

.lp-check-box svg {
  opacity: 0;
  transition: opacity 0.2s ease;
  width: 11px;
  height: 11px;
}

.lp-module.is-complete .lp-check-box {
  background: var(--success);
  border-color: var(--success);
}

.lp-module.is-complete .lp-check-box svg {
  opacity: 1;
}

.lp-module.is-complete .lp-check {
  color: var(--success);
}

/* ═══════════════════════════════════════
   BOTTOM SECTION
   ═══════════════════════════════════════ */

.lp-footer {
  margin-top: 4rem;
  padding: 2rem 2rem;
  background: var(--surface);
  border-radius: var(--radius-lg);
  border: 1px solid var(--border);
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
}

.lp-footer-text {
  font-size: 0.84rem;
  color: var(--text-muted);
  font-weight: 300;
}

.lp-footer-text strong {
  color: var(--text-secondary);
  font-weight: 500;
}

.lp-footer-actions {
  display: flex;
  gap: 0.75rem;
}

.lp-btn-back {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.7rem 1.5rem;
  background: var(--surface);
  color: var(--text-secondary) !important;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.8rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  transition: all 0.25s ease;
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
}

.lp-btn-back:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  background: var(--makro);
  border-color: var(--makro);
  color: #fff !important;
}

.lp-btn-reset {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.7rem 1.2rem;
  background: transparent;
  color: var(--text-muted) !important;
  text-decoration: none;
  font-weight: 400;
  font-size: 0.75rem;
  letter-spacing: 0.04em;
  transition: all 0.25s ease;
  border: 1px solid transparent;
  border-radius: var(--radius-sm);
  cursor: pointer;
}

.lp-btn-reset:hover {
  border-color: var(--border);
  color: var(--text-secondary) !important;
}

/* ═══════════════════════════════════════
   RESPONSIVE
   ═══════════════════════════════════════ */

@media (max-width: 768px) {
  .lp-hero {
    margin: -1rem -1rem 0 -1rem;
    padding: 2.5rem 1.5rem 2rem;
    border-radius: 0 0 var(--radius-lg) var(--radius-lg);
  }
  
  .lp-hero h1 {
    font-size: 1.85rem;
  }
  
  .lp-hero::before,
  .lp-hero::after {
    display: none;
  }
  
  .lp-section-meta {
    padding-left: calc(36px + 1rem);
  }
  
  .lp-path {
    padding-left: 2rem;
  }
  
  .lp-module-dot {
    left: -2rem;
  }
  
  .lp-module-card {
    padding: 1.25rem 1.25rem;
  }
  
  .lp-module-actions {
    flex-direction: column;
    align-items: stretch;
  }
  
  .lp-btn {
    justify-content: center;
    padding: 0.75rem;
  }
  
  .lp-check {
    margin-left: 0;
    justify-content: center;
  }
  
  .lp-footer {
    flex-direction: column;
    text-align: center;
    padding: 1.5rem;
  }
  
  .lp-footer-actions {
    width: 100%;
    flex-direction: column;
  }
  
  .lp-btn-back, .lp-btn-reset {
    justify-content: center;
  }
}

/* ═══════════════════════════════════════
   ANIMATION
   ═══════════════════════════════════════ */

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

.lp-module {
  animation: fadeInUp 0.5s ease both;
}

.lp-module:nth-child(1) { animation-delay: 0.05s; }
.lp-module:nth-child(2) { animation-delay: 0.1s; }
.lp-module:nth-child(3) { animation-delay: 0.15s; }
.lp-module:nth-child(4) { animation-delay: 0.2s; }
.lp-module:nth-child(5) { animation-delay: 0.25s; }
.lp-module:nth-child(6) { animation-delay: 0.3s; }
.lp-module:nth-child(7) { animation-delay: 0.35s; }
.lp-module:nth-child(8) { animation-delay: 0.4s; }

/* ═══════════════════════════════════════
   QUIZ SCORE BADGE
   ═══════════════════════════════════════ */

.lp-quiz-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  font-size: 0.72rem;
  font-weight: 500;
  letter-spacing: 0.03em;
  padding: 0.25rem 0.65rem;
  border-radius: 100px;
  white-space: nowrap;
}

.lp-quiz-badge--passed {
  background: var(--success-light);
  color: var(--success);
}

.lp-quiz-badge--failed {
  background: rgba(200, 100, 80, 0.08);
  color: #b07060;
}

.lp-quiz-badge--none {
  background: var(--border-light);
  color: var(--text-muted);
}

.lp-module-meta {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  flex-wrap: wrap;
  margin-bottom: 1rem;
}

</style>

<!-- ═══════════════════════════════════════
     HERO
     ═══════════════════════════════════════ -->

<div class="lp-hero">
  <div class="lp-hero-content">
    <h1>Volkswirtschaftslehre</h1>
    <p class="lp-hero-subtitle">Lernpfad zur Prüfungsvorbereitung · Studienkolleg Leipzig</p>
    
    <div class="lp-progress-bar-outer">
      <div class="lp-progress-bar-inner" id="progressBar"></div>
    </div>
    <div class="lp-progress-stats">
      <span class="lp-progress-text"><span id="completedCount">0</span> von <span id="totalCount">13</span> Modulen abgeschlossen</span>
      <span class="lp-progress-percent" id="progressPercent">0 %</span>
    </div>
  </div>
</div>

<!-- ═══════════════════════════════════════
     MIKROÖKONOMIE
     ═══════════════════════════════════════ -->

<div class="lp-section lp-section--mikro">
  <div class="lp-section-header">
    <div class="lp-section-icon">Mi</div>
    <h2 class="lp-section-title">Mikroökonomie</h2>
  </div>
  <p class="lp-section-meta">8 Module · Vom Grundbegriff zum Marktmodell</p>
  
  <div class="lp-path">

    <div class="lp-module" data-module="m1">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">01</span>
          <h4 class="lp-module-title">Bedürfnis, Bedarf und Nachfrage</h4>
        </div>
        <p class="lp-module-desc">Grundkonzepte der Wirtschaft: Definition und Unterscheidung von Bedürfnis, Bedarf und Nachfrage, Bedürfnisarten, Maslows Bedürfnispyramide mit praktischen Beispielen</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_1-3.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m1')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m2">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">02</span>
          <h4 class="lp-module-title">Güterarten in der Wirtschaft</h4>
        </div>
        <p class="lp-module-desc">Freie und wirtschaftliche Güter, inferiore und superiore Güter, Einkommenselastizität der Nachfrage, meritorische und demeritorische Güter, staatliche Markteingriffe</p>
        <p class="lp-module-prereq">Baut auf: Bedürfnis, Bedarf und Nachfrage</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_2-2.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_gueterarten.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m2')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m3">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">03</span>
          <h4 class="lp-module-title">Angebot und Angebotskurve</h4>
        </div>
        <p class="lp-module-desc">Das Marktmodell, Gesetz des Angebots, Angebotsfunktion, aggregiertes Marktangebot, Verschiebung vs. Bewegung auf der Angebotskurve, Einflussfaktoren</p>
        <p class="lp-module-prereq">Baut auf: Güterarten</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_3-4.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_angebot.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m3')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m4">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">04</span>
          <h4 class="lp-module-title">Nachfrage und Nachfragekurve</h4>
        </div>
        <p class="lp-module-desc">Gesetz der Nachfrage, Nachfragefunktion, aggregierte Marktnachfrage, Verschiebung der Nachfragekurve, Einflussfaktoren wie Einkommen, Präferenzen und Preise verwandter Güter</p>
        <p class="lp-module-prereq">Baut auf: Angebot und Angebotskurve</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_4-2.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_nachfrage.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m4')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m5">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">05</span>
          <h4 class="lp-module-title">Marktgleichgewicht</h4>
        </div>
        <p class="lp-module-desc">Gleichgewichtspreis und -menge, Angebots- und Nachfrageüberhang, Anpassungsprozesse, Auswirkungen von Steuern und Subventionen, praktische Beispiele und Berechnungen</p>
        <p class="lp-module-prereq">Baut auf: Angebot und Nachfrage</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_5-2.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_marktgleichgewicht.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m5')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m6">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">06</span>
          <h4 class="lp-module-title">Konsumenten- und Produzentenrente</h4>
        </div>
        <p class="lp-module-desc">Definition und Berechnung der Konsumenten- und Produzentenrente, ökonomische Wohlfahrt, Prohibitivpreis, graphische Darstellung, Beispielrechnungen am Smartwatch-Markt</p>
        <p class="lp-module-prereq">Baut auf: Marktgleichgewicht</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_6.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_renten.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m6')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m7">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">07</span>
          <h4 class="lp-module-title">Marktformen: Monopol, Oligopol, Polypol</h4>
        </div>
        <p class="lp-module-desc">Übersicht über Marktformen, Marktmacht, Marktstruktur, Vor- und Nachteile für Verbraucher, zahlreiche Beispiele und Übungsaufgaben zur Einordnung realer Märkte</p>
        <p class="lp-module-prereq">Baut auf: Marktgleichgewicht</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_7.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_marktformen.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m7')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m8">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">08</span>
          <h4 class="lp-module-title">Budgetgerade – Konsumentscheidungen</h4>
        </div>
        <p class="lp-module-desc">Mathematische Grundlagen der Konsumentscheidung: Budgetrestriktion, Gleichung und graphische Darstellung, Einkommens- und Preisänderungen, Opportunitätskosten</p>
        <p class="lp-module-prereq">Baut auf: Nachfrage und Güterarten</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/WS_VWL_8-3.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_budgetgerade.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m8')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- ═══════════════════════════════════════
     MAKROÖKONOMIE
     ═══════════════════════════════════════ -->

<div class="lp-section lp-section--makro">
  <div class="lp-section-header">
    <div class="lp-section-icon">Ma</div>
    <h2 class="lp-section-title">Makroökonomie</h2>
  </div>
  <p class="lp-section-meta">5 Module · Von der Gesamtrechnung zur Wirtschaftspolitik</p>
  
  <div class="lp-path">

    <div class="lp-module" data-module="m9">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">09</span>
          <h4 class="lp-module-title">Volkswirtschaftliche Gesamtrechnung</h4>
        </div>
        <p class="lp-module-desc">Definition und Ziele der VGR, Bruttoinlandsprodukt (BIP), drei Berechnungsmethoden, Inlandsprinzip vs. Inländerprinzip, Vermeidung von Doppelzählung</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/VWL_11.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_vgr.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m9')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m10">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">10</span>
          <h4 class="lp-module-title">Nominales vs. reales BIP</h4>
        </div>
        <p class="lp-module-desc">BIP-Deflator, BIP pro Kopf und Kaufkraftbereinigung (PPP), Grenzen des BIP als Wohlstandsindikator, alternative Indikatoren (HDI, Gini-Koeffizient)</p>
        <p class="lp-module-prereq">Baut auf: Volkswirtschaftliche Gesamtrechnung</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/VWL_12.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_vgr2.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m10')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m11">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">11</span>
          <h4 class="lp-module-title">Konjunktur & Konjunkturzyklen</h4>
        </div>
        <p class="lp-module-desc">Die 4 Konjunkturphasen, BIP-Berechnung, Wachstumsraten, Rezessionsdefinition, Früh- und Spätindikatoren, wirtschaftspolitische Maßnahmen</p>
        <p class="lp-module-prereq">Baut auf: Nominales vs. reales BIP</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/VWL_11_Konjunktur.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_konjunktur.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m11')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m12">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">12</span>
          <h4 class="lp-module-title">Antizyklische Konjunkturpolitik</h4>
        </div>
        <p class="lp-module-desc">Grundprinzipien antizyklischer Politik, Fiskal- und Geldpolitik, expansive vs. restriktive Maßnahmen, historische Fallbeispiele (Finanzkrise 2008)</p>
        <p class="lp-module-prereq">Baut auf: Konjunkturzyklen</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/VWL_12_Konjunkturpolitik.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_konjunkturpolitik.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m12')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

    <div class="lp-module" data-module="m13">
      <div class="lp-module-dot"></div>
      <div class="lp-module-card">
        <div class="lp-module-top">
          <span class="lp-module-step">13</span>
          <h4 class="lp-module-title">Arbeitslosigkeit & Arbeitsmarktpolitik</h4>
        </div>
        <p class="lp-module-desc">Arbeitslosenquote, drei Arten der Arbeitslosigkeit, Okun's Gesetz, aktive vs. passive Arbeitsmarktpolitik, Kurzarbeitergeld, Digitalisierung und demografischer Wandel</p>
        <p class="lp-module-prereq">Baut auf: Konjunktur und Konjunkturpolitik</p>
        <div class="lp-module-actions">
          <a href="/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf" class="lp-btn lp-btn--pdf"><span class="lp-btn--icon">📄</span> <span>PDF</span></a>
          <a href="/assets/quizzes/quiz_arbeitslosigkeit.html" class="lp-btn lp-btn--quiz"><span class="lp-btn--icon">✎</span> <span>Quiz</span></a>
          <label class="lp-check" onclick="toggleModule('m13')">
            <span class="lp-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>
            <span>Erledigt</span>
          </label>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- ═══════════════════════════════════════
     FOOTER
     ═══════════════════════════════════════ -->

<div class="lp-footer">
  <div class="lp-footer-text">
    <strong>13 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar
  </div>
  <div class="lp-footer-actions">
    <a href="/teaching/" class="lp-btn-back">← Übersicht</a>
    <button class="lp-btn-reset" onclick="resetProgress()">Fortschritt zurücksetzen</button>
  </div>
</div>

<!-- ═══════════════════════════════════════
     PROGRESS TRACKING (localStorage)
     ═══════════════════════════════════════ -->

<script>
const STORAGE_KEY = 'vwl-progress';
const QUIZ_RESULTS_KEY = 'vwl-quiz-results';
const TOTAL_MODULES = 13;
const PASS_THRESHOLD = 70;

function getProgress() {
  try {
    return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {};
  } catch (e) {
    return {};
  }
}

function getQuizResults() {
  try {
    return JSON.parse(localStorage.getItem(QUIZ_RESULTS_KEY)) || {};
  } catch (e) {
    return {};
  }
}

function saveProgress(progress) {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(progress));
}

function toggleModule(moduleId) {
  const progress = getProgress();
  const quizResults = getQuizResults();
  
  // If quiz was passed, don't allow manual un-checking
  if (progress[moduleId] && quizResults[moduleId]?.passed) {
    if (!confirm('Dieses Modul wurde per Quiz bestanden. Trotzdem zurücksetzen?')) return;
    // Also clear quiz result
    delete quizResults[moduleId];
    localStorage.setItem(QUIZ_RESULTS_KEY, JSON.stringify(quizResults));
  }
  
  if (progress[moduleId]) {
    delete progress[moduleId];
  } else {
    progress[moduleId] = Date.now();
  }
  saveProgress(progress);
  render();
}

function resetProgress() {
  if (confirm('Fortschritt und alle Quiz-Ergebnisse wirklich zurücksetzen?')) {
    localStorage.removeItem(STORAGE_KEY);
    localStorage.removeItem(QUIZ_RESULTS_KEY);
    render();
  }
}

function render() {
  const progress = getProgress();
  const quizResults = getQuizResults();
  const completed = Object.keys(progress).length;
  const percent = Math.round((completed / TOTAL_MODULES) * 100);
  
  // Update progress bar
  document.getElementById('progressBar').style.width = percent + '%';
  document.getElementById('completedCount').textContent = completed;
  document.getElementById('progressPercent').textContent = percent + ' %';
  
  // Update module states + quiz badges
  document.querySelectorAll('.lp-module').forEach(el => {
    const id = el.dataset.module;
    
    // Completion state
    if (progress[id]) {
      el.classList.add('is-complete');
    } else {
      el.classList.remove('is-complete');
    }
    
    // Quiz badge – insert/update after the actions row
    const actionsRow = el.querySelector('.lp-module-actions');
    let metaRow = el.querySelector('.lp-module-meta');
    
    if (!metaRow) {
      metaRow = document.createElement('div');
      metaRow.className = 'lp-module-meta';
      actionsRow.parentNode.insertBefore(metaRow, actionsRow);
    }
    
    const qr = quizResults[id];
    if (qr) {
      const cls = qr.passed ? 'lp-quiz-badge--passed' : 'lp-quiz-badge--failed';
      const icon = qr.passed ? '✓' : '✗';
      const attempts = qr.attempts > 1 ? ` · ${qr.attempts} Versuche` : '';
      metaRow.innerHTML = `<span class="lp-quiz-badge ${cls}">${icon} Quiz: ${qr.percentage}%${attempts}</span>`;
    } else {
      metaRow.innerHTML = '';
    }
  });
}

// Init on page load
document.addEventListener('DOMContentLoaded', render);
if (document.readyState !== 'loading') render();
</script>