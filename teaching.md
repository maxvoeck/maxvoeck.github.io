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

/* ─── Fächerliste ─── */
.mw-liste { border-top: 1px solid var(--linie2); padding-bottom: 40px; }
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
  font-family: var(--display);
  font-style: italic;
  font-weight: 300;
  font-size: 30px;
  color: var(--messing);
}
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

/* ─── Responsiv ─── */
@media (max-width: 600px) {
  .mw-hero { padding: 64px 0 40px; }
  .mw-fach { grid-template-columns: 40px 1fr auto; gap: 14px; padding: 22px 4px; }
  .mw-fach-nr { font-size: 22px; }
  .mw-fach h2 { font-size: 20px; }
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
    <p class="mw-hero-sub">Module, Skripte und Übungen für die Feststellungsprüfung — nach Fach sortiert.</p>
  </header>

  <div class="mw-liste">
    <a href="/teaching/mathematik/" class="mw-fach">
      <span class="mw-fach-nr">I</span>
      <div>
        <h2>Mathematik</h2>
        <div class="mw-fach-meta">30 Module · Algebra, Vektoren, Analysis, Integralrechnung</div>
      </div>
      <span class="mw-fach-pfeil">→</span>
    </a>
    <a href="/teaching/vwl/" class="mw-fach">
      <span class="mw-fach-nr">II</span>
      <div>
        <h2>Volkswirtschaftslehre</h2>
        <div class="mw-fach-meta">17 Module · Mikro- &amp; Makroökonomie</div>
      </div>
      <span class="mw-fach-pfeil">→</span>
    </a>
    <a href="/teaching/informatik/" class="mw-fach">
      <span class="mw-fach-nr">III</span>
      <div>
        <h2>Informatik</h2>
        <div class="mw-fach-meta">6 Module · Python</div>
      </div>
      <span class="mw-fach-pfeil">→</span>
    </a>
  </div>

</div>
</div>
