---
layout: page
title:
permalink: /teaching/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
/* ═══════════════════════════════════════════════════════
   NACHTPROGRAMM — Lehrmaterialien-Übersicht
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
.mw-page h1, .mw-page h2, .mw-page h3, .mw-page h4, .mw-page h5, .mw-page h6 {
  color: var(--elfenbein);
}

.mw-wrap { max-width: 900px; margin: 0 auto; padding: 0 28px; }

/* ─── Hero ─── */
.mw-hero { padding: 96px 0 56px; }
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
  font-size: clamp(44px, 7vw, 72px);
  line-height: 1;
  letter-spacing: -0.02em;
}
.mw-hero-sub {
  margin-top: 18px;
  max-width: 50ch;
  color: var(--nebel);
  font-size: 16px;
}

/* ─── Semester-Kapitel ─── */
.mw-kapitel { padding: 56px 0 12px; }
.mw-kapitel-kopf {
  display: flex;
  align-items: baseline;
  gap: 22px;
  margin-bottom: 8px;
}
.mw-numeral {
  font-family: var(--display);
  font-style: italic;
  font-weight: 300;
  font-size: 36px;
  color: var(--messing);
  min-width: 50px;
}
.mw-kapitel-kopf h2 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 26px;
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

/* ─── Fächerliste ─── */
.mw-liste { border-top: 1px solid var(--linie2); }
.mw-fach {
  display: grid;
  grid-template-columns: 56px 1fr auto;
  gap: 20px;
  align-items: center;
  padding: 28px 8px;
  border-bottom: 1px solid var(--linie2);
  text-decoration: none;
  color: inherit;
  transition: background 180ms ease, padding 180ms ease;
}
.mw-fach:hover { background: rgba(236,231,220,0.025); padding-left: 16px; }
.mw-fach-nr {
  font-family: var(--mono);
  font-size: 13px;
  color: var(--nebel);
  transition: color 180ms ease;
}
.mw-fach:hover .mw-fach-nr { color: var(--messing); }
.mw-fach h2 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 26px;
  letter-spacing: -0.005em;
  transition: color 180ms ease;
}
.mw-fach:hover h2 { color: var(--messing2); }
.mw-fach-meta {
  color: var(--nebel);
  font-size: 13.5px;
  margin-top: 4px;
}
.mw-fach-pfeil {
  font-family: var(--mono);
  font-size: 20px;
  color: var(--nebel);
  transition: transform 180ms ease, color 180ms ease;
}
.mw-fach:hover .mw-fach-pfeil { color: var(--messing); transform: translateX(4px); }

/* ─── Leerer Zustand ─── */
.mw-leer {
  padding: 28px 8px 40px;
  border-top: 1px solid var(--linie2);
  color: var(--nebel);
  font-size: 14px;
  font-style: italic;
}

/* ─── Responsiv ─── */
@media (max-width: 600px) {
  .mw-hero { padding: 64px 0 40px; }
  .mw-fach { grid-template-columns: 40px 1fr auto; gap: 14px; padding: 22px 4px; }
  .mw-fach h2 { font-size: 20px; }
  .mw-kapitel-kopf .mw-meta { display: none; }
}

@media (prefers-reduced-motion: reduce) {
  * { transition-duration: 1ms !important; animation: none !important; }
}
</style>

<div class="mw-page">
<div class="mw-wrap">

  <header class="mw-hero">
    <div class="mw-eyebrow">Studienkolleg Leipzig</div>
    <h1>Lehrmaterialien</h1>
    <p class="mw-hero-sub">Module, Skripte und Übungen für die Feststellungsprüfung — nach Semester sortiert.</p>
  </header>

  {%- comment -%}
    Modulzahlen kommen aus _data/kurse/*.yml und werden berechnet —
    nicht von Hand pflegen. Fächer ohne Datendatei tragen ihre Zahl noch selbst.
  {%- endcomment -%}
  {%- assign mathe_module = 0 -%}
  {%- for k in site.data.kurse.mathematik.kapitel -%}
    {%- unless k.fortschritt == false -%}{%- assign mathe_module = mathe_module | plus: k.module.size -%}{%- endunless -%}
  {%- endfor -%}
  {%- assign mikro_module = site.data.kurse.mikrooekonomie.kapitel[0].module.size -%}
  {%- assign makro_module = site.data.kurse.makrooekonomie.kapitel[0].module.size -%}
  {%- assign bwl_module = 0 -%}
  {%- for k in site.data.kurse.bwl.kapitel -%}{%- assign bwl_module = bwl_module | plus: k.module.size -%}{%- endfor -%}

  <!-- 1. Semester -->
  <section class="mw-kapitel">
    <div class="mw-kapitel-kopf">
      <span class="mw-numeral">I</span>
      <h2>1. Semester</h2>
      <span class="mw-meta">2 Fächer</span>
    </div>
    <div class="mw-liste">
      <a href="/teaching/mathematik/" class="mw-fach">
        <span class="mw-fach-nr">01</span>
        <div>
          <h2>Mathematik</h2>
          <div class="mw-fach-meta">{{ mathe_module }} Module &amp; 5 interaktive Tools · Algebra, Vektoren, Analysis, Integralrechnung</div>
        </div>
        <span class="mw-fach-pfeil">&rarr;</span>
      </a>
      <a href="/teaching/mikrooekonomie/" class="mw-fach">
        <span class="mw-fach-nr">02</span>
        <div>
          <h2>Volkswirtschaftslehre &middot; Mikro&ouml;konomie</h2>
          <div class="mw-fach-meta">{{ mikro_module }} Module · Nachfrage, Angebot, Marktgleichgewicht, Marktformen</div>
        </div>
        <span class="mw-fach-pfeil">&rarr;</span>
      </a>
    </div>
  </section>

  <!-- 2. Semester -->
  <section class="mw-kapitel">
    <div class="mw-kapitel-kopf">
      <span class="mw-numeral">II</span>
      <h2>2. Semester</h2>
      <span class="mw-meta">4 F&auml;cher</span>
    </div>
    <div class="mw-liste">
      <a href="/teaching/mathematik-w/" class="mw-fach">
        <span class="mw-fach-nr">01</span>
        <div>
          <h2>Mathematik (W-Kurs)</h2>
          <div class="mw-fach-meta">7 Module · Algebra, Finanzmathematik, Analysis, Integralrechnung</div>
        </div>
        <span class="mw-fach-pfeil">&rarr;</span>
      </a>
      <a href="/teaching/makrooekonomie/" class="mw-fach">
        <span class="mw-fach-nr">02</span>
        <div>
          <h2>Volkswirtschaftslehre &middot; Makro&ouml;konomie</h2>
          <div class="mw-fach-meta">{{ makro_module }} Module · VGR, Konjunktur, Arbeitsmarkt, Inflation</div>
        </div>
        <span class="mw-fach-pfeil">&rarr;</span>
      </a>
      <a href="/teaching/bwl/" class="mw-fach">
        <span class="mw-fach-nr">03</span>
        <div>
          <h2>Betriebswirtschaftslehre</h2>
          <div class="mw-fach-meta">{{ bwl_module }} Module · Allgemeine BWL, Buchf&uuml;hrung, Erfolg &amp; Steuern</div>
        </div>
        <span class="mw-fach-pfeil">&rarr;</span>
      </a>
      <a href="/teaching/informatik/" class="mw-fach">
        <span class="mw-fach-nr">04</span>
        <div>
          <h2>Informatik</h2>
          <div class="mw-fach-meta">7 Module · Python</div>
        </div>
        <span class="mw-fach-pfeil">&rarr;</span>
      </a>
    </div>
  </section>

</div>
</div>
