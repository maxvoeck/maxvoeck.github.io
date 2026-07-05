---
layout: page
title: 
permalink: /teaching/mathematik/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

<!-- KaTeX -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.js"></script>

<style>
/* ═══════════════════════════════════════════════════════
   NACHTPROGRAMM — Mathematik-Hub für das Studienkolleg
   Konzertprogramm-Ästhetik: Tinte, Elfenbein, Messing
   ═══════════════════════════════════════════════════════ */
:root {
  --ink:      #101014;
  --graphit:  #17171d;
  --graphit2: #1e1e26;
  --linie:    rgba(236, 231, 220, 0.09);
  --linie2:   rgba(236, 231, 220, 0.18);
  --elfenbein:#ece7dc;
  --nebel:    #8f8e97;
  --messing:  #c2a15c;
  --messing2: #dfc48a;
  --gruen:    #8fa284;
  --rost:     #b3705c;

  --display: 'Fraunces', Georgia, serif;
  --body:    'Inter', system-ui, sans-serif;
  --mono:    'JetBrains Mono', monospace;
}

body, html, .page-content, .wrapper, main {
  background: #101014 !important;
}
.post-header, .page-heading, header.post-header {
  display: none !important;
}

.mw-page * { box-sizing: border-box; margin: 0; padding: 0; }

.mw-page {
  background: var(--ink);
  color: var(--elfenbein);
  font-family: var(--body);
  font-size: 15px;
  line-height: 1.55;
  -webkit-font-smoothing: antialiased;
  padding-bottom: 120px;
}

.mw-wrap { max-width: 1060px; margin: 0 auto; padding: 0 28px; }

/* ─── Hero ─── */
.mw-hero {
  padding: 96px 0 72px;
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 48px;
  align-items: end;
  border-bottom: 1px solid var(--linie2);
}
.mw-eyebrow {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: var(--messing);
  margin-bottom: 20px;
}
.mw-hero h1 {
  font-family: var(--display);
  font-weight: 300;
  font-size: clamp(52px, 8vw, 92px);
  line-height: 0.98;
  letter-spacing: -0.02em;
}
.mw-hero-sub {
  margin-top: 22px;
  max-width: 46ch;
  color: var(--nebel);
  font-size: 16px;
}

/* Fortschrittsbogen */
.mw-progress { text-align: center; }
.mw-ring { width: 120px; height: 120px; }
.mw-ring circle { fill: none; stroke-width: 3; }
.mw-ring .bg { stroke: var(--linie2); }
.mw-ring .fg {
  stroke: var(--messing);
  stroke-linecap: round;
  transform: rotate(-90deg);
  transform-origin: 50% 50%;
  transition: stroke-dashoffset 600ms cubic-bezier(0.4,0,0.2,1);
}
.mw-ring-label {
  font-family: var(--display);
  font-size: 26px;
  font-weight: 300;
  fill: var(--elfenbein);
}
.mw-ring-caption {
  margin-top: 10px;
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--nebel);
}

/* ─── Gesamtskript-Feature ─── */
.mw-feature {
  margin: 56px 0 24px;
  padding: 30px 34px;
  background: linear-gradient(120deg, var(--graphit2), var(--graphit));
  border: 1px solid var(--linie2);
  border-radius: 4px;
  display: flex;
  align-items: center;
  gap: 28px;
  flex-wrap: wrap;
}
.mw-feature-titel h3 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 26px;
  letter-spacing: -0.01em;
}
.mw-feature-titel p { color: var(--nebel); font-size: 14px; margin-top: 6px; max-width: 52ch; }
.mw-feature .mw-btn { margin-left: auto; }

/* ─── Aufgabe des Tages ─── */
.mw-adt {
  margin: 24px 0 24px;
  padding: 34px 36px;
  background: linear-gradient(120deg, var(--graphit2), var(--graphit));
  border: 1px solid var(--linie2);
  border-radius: 4px;
}
.mw-adt-label {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.24em;
  text-transform: uppercase;
  color: var(--messing);
  margin-bottom: 18px;
}
.mw-adt-diff {
  display: inline-block;
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.1em;
  color: var(--nebel);
  border: 1px solid var(--linie2);
  border-radius: 999px;
  padding: 4px 12px;
  margin-bottom: 18px;
}
.mw-adt-frage {
  font-family: var(--display);
  font-size: 22px;
  font-weight: 400;
  letter-spacing: -0.005em;
  line-height: 1.5;
  margin-bottom: 12px;
}
.mw-adt-hint {
  font-size: 13.5px;
  color: var(--nebel);
  font-style: italic;
  line-height: 1.6;
  margin-bottom: 22px;
}
.mw-adt-actions { display: flex; align-items: center; gap: 12px; flex-wrap: wrap; }
.mw-adt-loesung {
  display: none;
  margin-top: 22px;
  padding-top: 22px;
  border-top: 1px solid var(--linie2);
}
.mw-adt-loesung.offen { display: block; animation: mwFade 300ms ease; }
@keyframes mwFade {
  from { opacity: 0; transform: translateY(6px); }
  to   { opacity: 1; transform: translateY(0); }
}
.mw-adt-loesung-label {
  font-family: var(--mono);
  font-size: 10.5px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gruen);
  margin-bottom: 10px;
}
.mw-adt-loesung-text { font-size: 15px; color: var(--elfenbein); line-height: 1.7; }

/* ─── Kapitel (klappbar) ─── */
.mw-kapitel { padding: 56px 0 12px; border-bottom: 1px solid var(--linie2); }
.mw-kapitel:last-of-type { border-bottom: none; }
.mw-kapitel-kopf {
  display: flex;
  align-items: baseline;
  gap: 22px;
  padding-bottom: 34px;
  cursor: pointer;
  user-select: none;
}
.mw-numeral {
  font-family: var(--display);
  font-style: italic;
  font-weight: 300;
  font-size: 44px;
  color: var(--messing);
  min-width: 64px;
}
.mw-kapitel-kopf h2 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 32px;
  letter-spacing: -0.01em;
}
.mw-kapitel-kopf .mw-meta {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--nebel);
  margin-left: auto;
  white-space: nowrap;
}
.mw-chevron {
  color: var(--nebel);
  font-size: 15px;
  transition: transform 220ms ease;
  margin-left: 12px;
}
.mw-kapitel.zu .mw-chevron { transform: rotate(-90deg); }

.mw-liste-outer {
  max-height: 3000px;
  opacity: 1;
  overflow: hidden;
  transition: max-height 420ms cubic-bezier(0.4,0,0.2,1), opacity 250ms ease;
}
.mw-kapitel.zu .mw-liste-outer { max-height: 0; opacity: 0; }

/* ─── Modulzeilen ─── */
.mw-liste { border-top: 1px solid var(--linie); }
.mw-modul {
  display: grid;
  grid-template-columns: 56px 1fr auto;
  gap: 20px;
  align-items: center;
  padding: 20px 8px;
  border-bottom: 1px solid var(--linie);
  transition: background 180ms ease, padding 180ms ease;
}
.mw-modul:hover { background: rgba(236,231,220,0.025); padding-left: 16px; }
.mw-nr {
  font-family: var(--mono);
  font-size: 13px;
  color: var(--nebel);
  transition: color 180ms;
}
.mw-modul:hover .mw-nr { color: var(--messing); }
.mw-modul.done .mw-nr { color: var(--gruen); }
.mw-modul h4 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 19px;
  letter-spacing: 0.005em;
}
.mw-modul.done h4 { color: var(--nebel); }

/* Aktionen */
.mw-actions { display: flex; align-items: center; gap: 8px; }
.mw-btn {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  font-family: var(--body);
  font-size: 12.5px;
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--elfenbein);
  background: transparent;
  border: 1px solid var(--linie2);
  border-radius: 999px;
  padding: 7px 15px;
  cursor: pointer;
  text-decoration: none;
  transition: all 160ms ease;
  white-space: nowrap;
}
.mw-btn:hover { border-color: var(--messing); color: var(--messing2); }
.mw-btn--voll {
  background: var(--messing);
  border-color: var(--messing);
  color: var(--ink);
}
.mw-btn--voll:hover { background: var(--messing2); border-color: var(--messing2); color: var(--ink); }
.mw-btn--deaktiviert {
  opacity: 0.45;
  cursor: not-allowed;
  pointer-events: none;
}
.mw-btn svg { width: 13px; height: 13px; flex-shrink: 0; }

/* Haken */
.mw-check {
  width: 30px; height: 30px;
  border-radius: 50%;
  border: 1px solid var(--linie2);
  background: transparent;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  transition: all 200ms ease;
  margin-left: 6px;
  flex-shrink: 0;
}
.mw-check svg { width: 13px; height: 13px; stroke: var(--ink); opacity: 0; transform: scale(0.4); transition: all 260ms cubic-bezier(0.34,1.56,0.64,1); }
.mw-check:hover { border-color: var(--gruen); }
.mw-modul.done .mw-check,
.mw-karte.done .mw-check { background: var(--gruen); border-color: var(--gruen); }
.mw-modul.done .mw-check svg,
.mw-karte.done .mw-check svg { opacity: 1; transform: scale(1); }

/* ─── Karten-Raster (Tools & Klausuren) ─── */
.mw-raster {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
  padding-top: 8px;
}
.mw-karte {
  background: var(--graphit);
  border: 1px solid var(--linie2);
  border-radius: 6px;
  padding: 22px 24px;
  transition: border-color 180ms ease, transform 180ms ease;
}
.mw-karte:hover { border-color: var(--messing); transform: translateY(-2px); }
.mw-karte h4 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 18px;
  margin-bottom: 14px;
}
.mw-karte-tags { margin-bottom: 16px; display: flex; flex-wrap: wrap; gap: 6px; }
.mw-tag {
  font-family: var(--mono);
  font-size: 10.5px;
  letter-spacing: 0.03em;
  color: var(--nebel);
  border: 1px solid var(--linie2);
  border-radius: 999px;
  padding: 3px 10px;
}
.mw-karte-aktionen { display: flex; align-items: center; gap: 8px; }
.mw-karte--bald { opacity: 0.55; }

/* ─── Fußzeile ─── */
.mw-fuss {
  margin-top: 88px;
  padding: 36px 0;
  border-top: 1px solid var(--linie2);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  flex-wrap: wrap;
  color: var(--nebel);
  font-size: 13px;
}
.mw-fuss-links { display: flex; gap: 10px; }

/* ─── Responsiv ─── */
@media (max-width: 760px) {
  .mw-hero { grid-template-columns: 1fr; gap: 36px; padding: 64px 0 48px; }
  .mw-progress { text-align: left; }
  .mw-modul { grid-template-columns: 40px 1fr; }
  .mw-actions { grid-column: 1 / -1; padding-left: 60px; flex-wrap: wrap; }
  .mw-kapitel-kopf .mw-meta { display: none; }
  .mw-feature .mw-btn { margin-left: 0; }
  .mw-raster { grid-template-columns: 1fr; }
}
@media (max-width: 760px) { .mw-actions { padding-left: 0; } }

@media (prefers-reduced-motion: reduce) {
  * { transition-duration: 1ms !important; animation: none !important; }
  html { scroll-behavior: auto; }
}
</style>

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung</div>
      <h1>Mathematik</h1>
      <p class="mw-hero-sub">Module, Quiz, interaktive Tools und Klausurvorbereitung — alles an einem Ort.</p>
    </div>
    <div class="mw-progress">
      <svg class="mw-ring" viewBox="0 0 120 120">
        <circle class="bg" cx="60" cy="60" r="52"/>
        <circle class="fg" cx="60" cy="60" r="52" id="progressRing"/>
        <text class="mw-ring-label" x="60" y="60" text-anchor="middle" dominant-baseline="central" id="progressText">0%</text>
      </svg>
      <div class="mw-ring-caption"><span id="completedCount">0</span> von <span id="totalCount">0</span></div>
    </div>
  </header>

  <!-- Gesamtskript -->
  <div class="mw-feature">
    <div class="mw-feature-titel">
      <h3>Gesamtskript</h3>
      <p>Alle Module als zusammenhängendes Dokument — zum durchgehenden Lernen oder als Nachschlagewerk.</p>
    </div>
    <a href="/assets/pdfs/Mathematik_Skript.pdf" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 3v12m0 0l-4-4m4 4l4-4M4 21h16"/></svg>
      Skript öffnen
    </a>
  </div>

  <!-- Aufgabe des Tages -->
  <div class="mw-adt">
    <div class="mw-adt-label">Aufgabe des Tages</div>
    <div class="mw-adt-diff" id="adt-diff"></div>
    <div class="mw-adt-frage" id="adt-question"></div>
    <div class="mw-adt-hint" id="adt-hint" style="display:none"></div>
    <div class="mw-adt-actions">
      <button class="mw-btn mw-btn--voll" id="adt-toggle" onclick="window.adtToggle()">Antwort zeigen</button>
      <a class="mw-btn" id="adt-quiz" style="display:none">Quiz →</a>
    </div>
    <div class="mw-adt-loesung" id="adt-solution">
      <div class="mw-adt-loesung-label">Antwort</div>
      <div class="mw-adt-loesung-text" id="adt-answer"></div>
    </div>
  </div>

  <!-- Lineare Algebra -->
  <section class="mw-kapitel zu" data-section>
    <div class="mw-kapitel-kopf" onclick="toggleSection(this.parentElement)">
      <span class="mw-numeral">I</span>
      <h2>Lineare Algebra</h2>
      <span class="mw-meta">5 Module</span>
      <span class="mw-chevron">▾</span>
    </div>
    <div class="mw-liste-outer">
      <div class="mw-liste">
        <div class="mw-modul" data-module="a1">
          <span class="mw-nr">01</span>
          <div><h4>Matrizen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Matrizen_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('a1', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="a2">
          <span class="mw-nr">02</span>
          <div><h4>Determinanten</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Matrizen_2_2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_determinanten.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('a2', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="a3">
          <span class="mw-nr">03</span>
          <div><h4>Matrizengleichungen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Matrizen_2_3.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <button class="mw-check" onclick="toggleModule('a3', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="a4">
          <span class="mw-nr">04</span>
          <div><h4>Lineare Gleichungssysteme</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/LGS_2_1-5.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('a4', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="a5">
          <span class="mw-nr">05</span>
          <div><h4>Parameterabhängigkeit</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/LGS_2_2-2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <button class="mw-check" onclick="toggleModule('a5', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Vektorrechnung -->
  <section class="mw-kapitel zu" data-section>
    <div class="mw-kapitel-kopf" onclick="toggleSection(this.parentElement)">
      <span class="mw-numeral">II</span>
      <h2>Vektorrechnung</h2>
      <span class="mw-meta">4 Module</span>
      <span class="mw-chevron">▾</span>
    </div>
    <div class="mw-liste-outer">
      <div class="mw-liste">
        <div class="mw-modul" data-module="v1">
          <span class="mw-nr">06</span>
          <div><h4>Grundlagen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Geo_2_1-2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('v1', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="v2">
          <span class="mw-nr">07</span>
          <div><h4>Vektor- &amp; Spatprodukt</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Geo_2_2-2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_vektorprodukt.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('v2', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="v3">
          <span class="mw-nr">08</span>
          <div><h4>Geraden und Ebenen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Geo_2_3.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('v3', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="v4">
          <span class="mw-nr">09</span>
          <div><h4>Abstände und Lagen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Geo_2_4.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('v4', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Differentialrechnung -->
  <section class="mw-kapitel zu" data-section>
    <div class="mw-kapitel-kopf" onclick="toggleSection(this.parentElement)">
      <span class="mw-numeral">III</span>
      <h2>Differentialrechnung</h2>
      <span class="mw-meta">12 Module</span>
      <span class="mw-chevron">▾</span>
    </div>
    <div class="mw-liste-outer">
      <div class="mw-liste">
        <div class="mw-modul" data-module="d1">
          <span class="mw-nr">10</span>
          <div><h4>Zahlenfolgen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Zahlenfolgen_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d1', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d2">
          <span class="mw-nr">11</span>
          <div><h4>Grenzwerte von Folgen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Grenzwerte_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d2', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d3">
          <span class="mw-nr">12</span>
          <div><h4>Grenzwerte im Unendlichen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Funktion_2_2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d3', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d4">
          <span class="mw-nr">13</span>
          <div><h4>Grenzwerte an einer Stelle</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Grenzwerte_2_2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d4', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d5">
          <span class="mw-nr">14</span>
          <div><h4>Asymptoten</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Grenzwerte_2_3.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_asymptoten.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d5', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d6">
          <span class="mw-nr">15</span>
          <div><h4>Steigung und Ableitung</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Funktion_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d6', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d7">
          <span class="mw-nr">16</span>
          <div><h4>Ableitungsregeln</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Funktion_2_4.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d7', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d8">
          <span class="mw-nr">17</span>
          <div><h4>Regel von de L'Hôpital</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Hospital_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_hospital.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d8', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d9">
          <span class="mw-nr">18</span>
          <div><h4>Extrempunkte</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Extremwert_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_extrempunkte.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d9', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d10">
          <span class="mw-nr">19</span>
          <div><h4>Wendepunkte</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Wendepunkt_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_wendepunkte.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d10', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d11">
          <span class="mw-nr">20</span>
          <div><h4>Kurvendiskussion</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Kurvendiskusion_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d11', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="d12">
          <span class="mw-nr">21</span>
          <div><h4>Extremwertaufgaben</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Extrem_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('d12', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Integralrechnung -->
  <section class="mw-kapitel zu" data-section>
    <div class="mw-kapitel-kopf" onclick="toggleSection(this.parentElement)">
      <span class="mw-numeral">IV</span>
      <h2>Integralrechnung</h2>
      <span class="mw-meta">5 Module</span>
      <span class="mw-chevron">▾</span>
    </div>
    <div class="mw-liste-outer">
      <div class="mw-liste">
        <div class="mw-modul" data-module="i1">
          <span class="mw-nr">22</span>
          <div><h4>Einführung</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Integral_2_1.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('i1', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="i2">
          <span class="mw-nr">23</span>
          <div><h4>Integrationsmethoden</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Integral_2_2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('i2', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="i3">
          <span class="mw-nr">24</span>
          <div><h4>Hauptsatz &amp; Flächen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Integral_2_3.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('i3', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="i4">
          <span class="mw-nr">25</span>
          <div><h4>Rotationsvolumen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Intergal_2_4-2.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">Quiz</a>
            <button class="mw-check" onclick="toggleModule('i4', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-modul" data-module="i5">
          <span class="mw-nr">26</span>
          <div><h4>Flächen zwischen Funktionen</h4></div>
          <div class="mw-actions">
            <a href="/assets/pdfs/Fläche_zwichen_Funktionen.pdf" class="mw-btn" onclick="event.stopPropagation()">PDF</a>
            <button class="mw-check" onclick="toggleModule('i5', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Interaktive Tools -->
  <section class="mw-kapitel zu" data-section id="tools">
    <div class="mw-kapitel-kopf" onclick="toggleSection(this.parentElement)">
      <h2>Interaktive Tools</h2>
      <span class="mw-meta">5 Anwendungen</span>
      <span class="mw-chevron">▾</span>
    </div>
    <div class="mw-liste-outer">
      <div class="mw-raster">
        <div class="mw-karte" data-module="t1">
          <h4>Tangenten-Explorer</h4>
          <div class="mw-karte-aktionen">
            <a href="/assets/interactive/tangenten_explorer.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()" style="flex:1; justify-content:center;">→ Öffnen</a>
            <button class="mw-check" onclick="toggleModule('t1', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-karte" data-module="t2">
          <h4>3D-Vektor-Explorer</h4>
          <div class="mw-karte-aktionen">
            <a href="/assets/interactive/vektor_explorer.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()" style="flex:1; justify-content:center;">→ Öffnen</a>
            <button class="mw-check" onclick="toggleModule('t2', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-karte" data-module="t3">
          <h4>Geraden &amp; Ebenen</h4>
          <div class="mw-karte-aktionen">
            <a href="/assets/interactive/geraden_ebenen_explorer.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()" style="flex:1; justify-content:center;">→ Öffnen</a>
            <button class="mw-check" onclick="toggleModule('t3', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-karte" data-module="t4">
          <h4>Matrizen-Explorer</h4>
          <div class="mw-karte-aktionen">
            <a href="/assets/interactive/matrizen_explorer.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()" style="flex:1; justify-content:center;">→ Öffnen</a>
            <button class="mw-check" onclick="toggleModule('t4', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
        <div class="mw-karte" data-module="t5">
          <h4>Determinanten-Rechner</h4>
          <div class="mw-karte-aktionen">
            <a href="/assets/interactive/determinanten_rechner.html" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()" style="flex:1; justify-content:center;">→ Öffnen</a>
            <button class="mw-check" onclick="toggleModule('t5', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Klausuren -->
  <section class="mw-kapitel zu" data-section>
    <div class="mw-kapitel-kopf" onclick="toggleSection(this.parentElement)">
      <h2>Klausuren</h2>
      <span class="mw-meta">Übungsaufgaben zur Klausurvorbereitung</span>
      <span class="mw-chevron">▾</span>
    </div>
    <div class="mw-liste-outer">
      <div class="mw-raster">
        <div class="mw-karte mw-karte--bald">
          <h4>Klausur 1</h4>
          <div class="mw-karte-tags">
            <span class="mw-tag">Differentialrechnung</span>
            <span class="mw-tag">Ableitungsregeln</span>
          </div>
          <div class="mw-karte-aktionen">
            <span class="mw-btn mw-btn--deaktiviert">Demnächst</span>
          </div>
        </div>
        <div class="mw-karte mw-karte--bald">
          <h4>Klausur 2</h4>
          <div class="mw-karte-tags">
            <span class="mw-tag">Extremwertaufgaben</span>
            <span class="mw-tag">Kurvendiskussion</span>
          </div>
          <div class="mw-karte-aktionen">
            <span class="mw-btn mw-btn--deaktiviert">Demnächst</span>
          </div>
        </div>
        <div class="mw-karte" data-module="klausur-03">
          <h4>Klausur 3</h4>
          <div class="mw-karte-tags">
            <span class="mw-tag">Extremwertaufgaben mit NB</span>
            <span class="mw-tag">Fläche unter Kurve</span>
            <span class="mw-tag">Fläche zwischen Kurven</span>
          </div>
          <div class="mw-karte-aktionen">
            <a href="/assets/pdfs/Übungsheft_T_2_3.pdf" class="mw-btn mw-btn--voll" onclick="event.stopPropagation()">PDF</a>
            <button class="mw-check" onclick="toggleModule('klausur-03', event)" aria-label="Als erledigt markieren"><svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div><strong style="color:var(--elfenbein)"><span id="totalModules">0</span> Module &amp; Tools</strong> · Algebra, Vektoren, Analysis &amp; Integralrechnung</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>
</div>

<script>
const STORAGE_KEY = 'math-progress-v2';
const CIRCUMFERENCE = 2 * Math.PI * 52;

function getTotalModules() {
  return document.querySelectorAll('[data-module]').length;
}

function getProgress() {
  try { return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {}; }
  catch { return {}; }
}
function saveProgress(progress) {
  try { localStorage.setItem(STORAGE_KEY, JSON.stringify(progress)); }
  catch { console.warn('Failed to save progress'); }
}

function toggleModule(moduleId, event) {
  event.preventDefault();
  event.stopPropagation();
  const progress = getProgress();
  const card = event.target.closest('[data-module]');
  if (progress[moduleId]) {
    delete progress[moduleId];
    if (card) card.classList.remove('done');
  } else {
    progress[moduleId] = true;
    if (card) card.classList.add('done');
  }
  saveProgress(progress);
  updateUI();
}

function updateUI() {
  const progress = getProgress();
  const total = getTotalModules();
  const completed = Object.keys(progress).filter(k => !!document.querySelector('[data-module="' + k + '"]')).length;
  const percentage = total > 0 ? Math.round((completed / total) * 100) : 0;

  const ring  = document.getElementById('progressRing');
  const text  = document.getElementById('progressText');
  const count = document.getElementById('completedCount');
  const totalEl = document.getElementById('totalCount');
  const footerTotal = document.getElementById('totalModules');

  if (ring && text && count && totalEl && footerTotal) {
    ring.style.strokeDasharray = CIRCUMFERENCE;
    ring.style.strokeDashoffset = CIRCUMFERENCE - (percentage / 100) * CIRCUMFERENCE;
    text.textContent = percentage + '%';
    count.textContent = completed;
    totalEl.textContent = total;
    footerTotal.textContent = total;
  }

  document.querySelectorAll('[data-module]').forEach(card => {
    card.classList.toggle('done', !!progress[card.dataset.module]);
  });
}

function toggleSection(section) {
  section.classList.toggle('zu');
}

document.addEventListener('DOMContentLoaded', updateUI);
if (document.readyState !== 'loading') updateUI();
</script>

{% raw %}
<script>
(function() {
  var pool = [
    { diff:"Grundlagen", frage:"Berechne die Determinante: $\\det\\begin{pmatrix} 3 & 1 \\\\ 5 & 2 \\end{pmatrix}$", hint:"Denk an die Formel ad - bc.", antwort:"$\\det = 3 \\cdot 2 - 1 \\cdot 5 = 6 - 5 = 1$", quiz:"/assets/quizzes/quiz_determinanten.html" },
    { diff:"Grundlagen", frage:"Löse das Gleichungssystem: $2x + y = 7$ und $x - y = 2$", hint:"Addiere beide Gleichungen, um y zu eliminieren.", antwort:"Addition: $3x = 9$, also $x = 3$. Einsetzen: $y = 1$. Lösung: $(3, 1)$.", quiz:"/assets/quizzes/quiz_lgs_grundlagen.html" },
    { diff:"Mittel", frage:"Gegeben: $A = \\begin{pmatrix} 1 & 2 \\\\ 3 & 4 \\end{pmatrix}$. Berechne $A^2$.", antwort:"$A^2 = \\begin{pmatrix} 7 & 10 \\\\ 15 & 22 \\end{pmatrix}$", quiz:"/assets/quizzes/quiz_matrizen_grundlagen.html" },
    { diff:"Grundlagen", frage:"Berechne das Skalarprodukt: $\\vec{a} = \\begin{pmatrix} 2 \\\\ -1 \\\\ 3 \\end{pmatrix}$ und $\\vec{b} = \\begin{pmatrix} 1 \\\\ 4 \\\\ -2 \\end{pmatrix}$", antwort:"$\\vec{a} \\cdot \\vec{b} = 2 - 4 - 6 = -8$", quiz:"/assets/quizzes/quiz_vektorprodukt.html" },
    { diff:"Mittel", frage:"Bestimme den Abstand des Punktes $P(1, 2, 3)$ vom Ursprung.", antwort:"$d = \\sqrt{1^2 + 2^2 + 3^2} = \\sqrt{14} \\approx 3{,}74$" },
    { diff:"Klausurniveau", frage:"Zeige, dass $\\vec{a} = \\begin{pmatrix} 1 \\\\ 0 \\\\ -1 \\end{pmatrix}$ und $\\vec{b} = \\begin{pmatrix} 2 \\\\ 1 \\\\ 2 \\end{pmatrix}$ senkrecht stehen.", antwort:"$\\vec{a} \\cdot \\vec{b} = 2 + 0 - 2 = 0$. Da Skalarprodukt $= 0$, stehen sie senkrecht.", quiz:"/assets/quizzes/quiz_vektorprodukt.html" },
    { diff:"Grundlagen", frage:"Bestimme $f'(x)$ für $f(x) = 3x^4 - 2x^2 + 5x - 1$.", antwort:"$f'(x) = 12x^3 - 4x + 5$", quiz:"/assets/quizzes/quiz_ableitung_grundlagen.html" },
    { diff:"Mittel", frage:"Leite ab: $f(x) = \\sin(x) \\cdot e^x$ (Produktregel).", antwort:"$f'(x) = \\cos(x) \\cdot e^x + \\sin(x) \\cdot e^x = e^x(\\cos x + \\sin x)$", quiz:"/assets/quizzes/quiz_ableitungsregeln.html" },
    { diff:"Mittel", frage:"Finde die Extrempunkte von $f(x) = x^3 - 3x + 2$.", hint:"Setze f'(x) = 0 und prüfe mit f''(x).", antwort:"$x = \\pm 1$. Bei $x=1$: Minimum $(1, 0)$. Bei $x=-1$: Maximum $(-1, 4)$.", quiz:"/assets/quizzes/quiz_extrempunkte.html" },
    { diff:"Klausurniveau", frage:"Bestimme die Wendepunkte von $f(x) = x^4 - 6x^2 + 8x + 1$.", antwort:"$f''(x) = 12x^2 - 12 = 0 \\Rightarrow x = \\pm 1$. Wendepunkte: $W_1(1, 4)$ und $W_2(-1, -12)$.", quiz:"/assets/quizzes/quiz_wendepunkte.html" },
    { diff:"Grundlagen", frage:"Berechne $\\lim_{n \\to \\infty} \\frac{3n^2 + 2n}{n^2 - 1}$.", hint:"Teile durch die höchste Potenz von n.", antwort:"$\\frac{3 + 0}{1 - 0} = 3$", quiz:"/assets/quizzes/quiz_grenzwerte_folgen.html" },
    { diff:"Grundlagen", frage:"Berechne $\\int (4x^3 - 6x + 1)\\,dx$.", antwort:"$x^4 - 3x^2 + x + C$", quiz:"/assets/quizzes/quiz_integral_einfuehrung.html" },
    { diff:"Mittel", frage:"Berechne die Fläche unter $f(x) = x^2$ auf $[0, 3]$.", antwort:"$A = \\left[\\frac{x^3}{3}\\right]_0^3 = 9$ FE", quiz:"/assets/quizzes/quiz_hauptsatz_flaechen.html" },
    { diff:"Klausurniveau", frage:"Berechne $\\int x \\cdot e^x \\, dx$ (partielle Integration).", hint:"Wähle u = x und v' = eˣ.", antwort:"$x \\cdot e^x - e^x + C = e^x(x-1) + C$", quiz:"/assets/quizzes/quiz_integrationsmethoden.html" },
    { diff:"Mittel", frage:"Bestimme mit L'Hôpital: $\\lim_{x \\to 0} \\frac{\\sin x}{x}$", antwort:"Typ $\\frac{0}{0}$. L'Hôpital: $\\frac{\\cos 0}{1} = 1$.", quiz:"/assets/quizzes/quiz_hospital.html" },
    { diff:"Klausurniveau", frage:"Bestimme die Asymptoten von $f(x) = \\frac{2x^2 + 1}{x - 1}$.", hint:"Prüfe senkrechte und schräge Asymptoten.", antwort:"Senkrecht: $x = 1$. Polynomdivision ergibt schräge Asymptote: $y = 2x + 2$.", quiz:"/assets/quizzes/quiz_asymptoten.html" },
    { diff:"Grundlagen", frage:"Berechne: $\\frac{2}{3} + \\frac{3}{4}$", hint:"Finde den gemeinsamen Nenner.", antwort:"$\\frac{8}{12} + \\frac{9}{12} = \\frac{17}{12}$" },
    { diff:"Mittel", frage:"Rotationsvolumen: $f(x) = \\sqrt{x}$ auf $[0, 4]$ um die x-Achse.", antwort:"$V = \\pi \\int_0^4 x\\,dx = \\pi \\cdot 8 = 8\\pi$ VE", quiz:"/assets/quizzes/quiz_rotationsvolumen.html" },
    { diff:"Grundlagen", frage:"Ist die Folge $a_n = \\frac{(-1)^n}{n}$ konvergent? Falls ja, gegen welchen Grenzwert?", antwort:"Ja, konvergent. $\\lim_{n \\to \\infty} \\frac{(-1)^n}{n} = 0$, da $|a_n| = \\frac{1}{n} \\to 0$.", quiz:"/assets/quizzes/quiz_zahlenfolgen.html" },
    { diff:"Mittel", frage:"Bestimme die Gleichung der Tangente an $f(x) = x^2$ im Punkt $P(2, 4)$.", antwort:"$f'(x) = 2x$, also $f'(2) = 4$. Tangente: $y = 4(x - 2) + 4 = 4x - 4$.", quiz:"/assets/quizzes/quiz_ableitung_grundlagen.html" }
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
  var diffs = { "Grundlagen":"I", "Mittel":"II", "Klausurniveau":"III" };
  document.getElementById('adt-diff').textContent = (diffs[t.diff]||'') + ' ' + t.diff;
  var qEl = document.getElementById('adt-question');
  qEl.innerHTML = t.frage; renderMath(qEl);
  if (t.hint) { var h = document.getElementById('adt-hint'); h.textContent = t.hint; h.style.display = 'block'; }
  var aEl = document.getElementById('adt-answer');
  aEl.innerHTML = t.antwort; renderMath(aEl);
  if (t.quiz) { var q = document.getElementById('adt-quiz'); q.href = t.quiz; q.style.display = 'inline-flex'; }

  window.adtToggle = function() {
    var sol = document.getElementById('adt-solution');
    sol.classList.toggle('offen');
    document.getElementById('adt-toggle').textContent = sol.classList.contains('offen') ? 'Antwort verbergen' : 'Antwort zeigen';
  };
})();
</script>
{% endraw %}
