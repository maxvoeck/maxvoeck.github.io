---
layout: page
title:
permalink: /learn/mathematik/
---

<style>
:root {
  --system-indigo: #5856D6;
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;
  --math: #FF2D55;

  --bg-primary: #262624;
  --bg-secondary: #30302e;
  --bg-tertiary: #3a3a37;
  --text-primary: #c1c0b6;
  --text-secondary: #908f87;
  --text-tertiary: #706f69;
  --separator: rgba(var(--text-rgb), 0.08);

  --font-stack: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", "Helvetica Neue", Helvetica, Arial, sans-serif;
  --space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;
  --space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;
  --radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;
  --transition-base:250ms cubic-bezier(0.4,0,0.2,1);
  --transition-spring:500ms cubic-bezier(0.34,1.56,0.64,1);
}

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.47059;letter-spacing:-0.022em;}
.post-header,.page-heading,header.post-header{display:none!important;}

.lm-container {
  max-width: 860px;
  margin: 0 auto;
  padding: var(--space-12) var(--space-5);
}

/* Breadcrumb */
.lm-breadcrumb {
  display: flex;
  align-items: center;
  gap: var(--space-2);
  font-size: 13px;
  color: var(--text-tertiary);
  margin-bottom: var(--space-10);
}
.lm-breadcrumb a { color: var(--text-tertiary); text-decoration: none; }
.lm-breadcrumb a:hover { color: var(--text-primary); }
.lm-breadcrumb-sep { opacity: 0.4; }
.lm-breadcrumb-current { color: var(--text-secondary); }

/* Hero */
.lm-hero { margin-bottom: var(--space-12); animation: fadeIn .6s ease backwards; }
.lm-hero-eyebrow {
  display: inline-flex; align-items: center; gap: var(--space-2);
  font-size: 12px; font-weight: 600; text-transform: uppercase;
  letter-spacing: .08em; color: var(--math);
  background: rgba(255,45,85,.1); border: 1px solid rgba(255,45,85,.2);
  border-radius: var(--radius-full); padding: var(--space-1) var(--space-3);
  margin-bottom: var(--space-5);
}
.lm-hero h1 {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, "SF Pro Display", "Segoe UI", sans-serif; font-weight: 500;
  font-size: clamp(36px,5vw,56px); font-weight: 400; letter-spacing: -.02em;
  line-height: 1.06; margin-bottom: var(--space-4);
  color: var(--text-primary);
}
.lm-hero-sub {
  font-size: 17px; color: var(--text-tertiary); line-height: 1.6; max-width: 560px;
}

/* Chapter grid */
.lm-chapters { display: flex; flex-direction: column; gap: var(--space-3); }

.lm-chapter {
  display: flex; align-items: center; gap: var(--space-5);
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-xl); padding: var(--space-5) var(--space-6);
  text-decoration: none; color: inherit;
  transition: all var(--transition-base);
  animation: fadeIn .5s ease backwards;
}
.lm-chapter:nth-child(1){animation-delay:.05s}
.lm-chapter:nth-child(2){animation-delay:.1s}
.lm-chapter:nth-child(3){animation-delay:.15s}
.lm-chapter:nth-child(4){animation-delay:.2s}
.lm-chapter:nth-child(5){animation-delay:.25s}

.lm-chapter:hover {
  background: var(--bg-tertiary);
  border-color: rgba(var(--text-rgb),0.12);
  transform: translateX(4px);
}
.lm-chapter--locked { opacity: .45; cursor: not-allowed; pointer-events: none; }

.lm-chapter-num {
  width: 40px; height: 40px; border-radius: var(--radius-md);
  background: rgba(255,45,85,.12); color: var(--math);
  font-size: 15px; font-weight: 700; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
}
.lm-chapter--locked .lm-chapter-num { background: var(--bg-tertiary); color: var(--text-tertiary); }

.lm-chapter-body { flex: 1; }
.lm-chapter-title { font-size: 16px; font-weight: 600; margin-bottom: 3px; }
.lm-chapter-desc { font-size: 13px; color: var(--text-tertiary); line-height: 1.5; }

.lm-chapter-badge {
  font-size: 11px; font-weight: 500; padding: 3px 8px;
  border-radius: var(--radius-full); flex-shrink: 0;
}
.lm-chapter-badge--new {
  background: rgba(52,199,89,.12); color: var(--system-green);
  border: 1px solid rgba(52,199,89,.2);
}
.lm-chapter-badge--soon {
  background: var(--bg-tertiary); color: var(--text-tertiary);
  border: 1px solid var(--separator);
}

.lm-chapter-arrow { color: var(--text-tertiary); font-size: 16px; flex-shrink: 0; transition: transform var(--transition-base); }
.lm-chapter:hover .lm-chapter-arrow { transform: translateX(3px); color: var(--text-primary); }

/* Section headers */
.lm-section { margin-bottom: var(--space-6); }
.lm-section-header {
  display: flex; align-items: center; gap: var(--space-3);
  margin-bottom: var(--space-4); padding-bottom: var(--space-3);
  border-bottom: 1px solid var(--separator);
}
.lm-section-eyebrow {
  font-size: 11px; font-weight: 700; text-transform: uppercase;
  letter-spacing: .08em; padding: 3px 10px; border-radius: var(--radius-full);
}
.lm-section-eyebrow--math { color: var(--math); background: rgba(255,45,85,.1); border: 1px solid rgba(255,45,85,.2); }
.lm-section-eyebrow--geo { color: var(--system-blue); background: rgba(0,122,255,.1); border: 1px solid rgba(0,122,255,.2); }
.lm-section-title { font-size: 18px; font-weight: 700; }
/* Blue variant for Analytische Geometrie chapters */
.lm-chapter--geo .lm-chapter-num { background: rgba(0,122,255,.12); color: var(--system-blue); }

/* PDF hint */
.lm-pdf-hint {
  margin-top: var(--space-10);
  display: flex; align-items: center; gap: var(--space-3);
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-lg); padding: var(--space-4) var(--space-5);
  font-size: 14px; color: var(--text-tertiary); text-decoration: none;
  transition: all var(--transition-base);
}
.lm-pdf-hint:hover { border-color: rgba(var(--text-rgb),0.12); color: var(--text-secondary); }

@keyframes fadeIn { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:none} }
@media(max-width:600px){
.lm-container{padding:var(--space-8) var(--space-4);}
.lm-hero h1{font-size:32px;}
.lm-hero-sub{font-size:15px;}
.lm-chapter{padding:var(--space-4);gap:var(--space-3);}
.lm-chapter-num{width:34px;height:34px;font-size:13px;}
.lm-chapter-title{font-size:15px;}
.lm-chapter-desc{font-size:12px;}
.lm-chapter-badge{display:none;}
.lm-pdf-hint{font-size:13px;}
}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important;}}
</style>

<div class="lm-container">

  <div class="lm-breadcrumb">
    <a href="/learn/">Learn</a>
    <span class="lm-breadcrumb-sep">›</span>
    <span class="lm-breadcrumb-current">Mathematik</span>
  </div>

  <div class="lm-hero">
    <div class="lm-hero-eyebrow">Mathematik</div>
    <h1>Mathematik</h1>
    <p class="lm-hero-sub">Von Matrizen und Determinanten über Vektoren bis zu Geraden und Ebenen — Schritt für Schritt erklärt, direkt im Browser.</p>
  </div>

  <!-- Lineare Algebra -->
  <div class="lm-section">
    <div class="lm-section-header">
      <span class="lm-section-eyebrow lm-section-eyebrow--math">Lineare Algebra</span>
      <span class="lm-section-title">Matrizen & Gleichungssysteme</span>
    </div>
    <div class="lm-chapters">

    <a href="/learn/matrizen-grundlagen/" class="lm-chapter">
      <div class="lm-chapter-num">1</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Matrizen – Grundlagen</div>
        <div class="lm-chapter-desc">Definition, besondere Matrizen, Addition, Multiplikation, Transponieren</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
      <span class="lm-chapter-arrow">→</span>
    </a>

    <a href="/learn/determinanten/" class="lm-chapter">
      <div class="lm-chapter-num">2</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Determinanten</div>
        <div class="lm-chapter-desc">2×2, Regel von Sarrus, Laplace-Entwicklung, inverse Matrizen</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
      <span class="lm-chapter-arrow">→</span>
    </a>

    <a href="/learn/matrizengleichungen-rang/" class="lm-chapter">
      <div class="lm-chapter-num">3</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Matrizengleichungen & Rang</div>
        <div class="lm-chapter-desc">Gleichungen mit Matrizen lösen, Rang, Zeilenstufenform</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
      <span class="lm-chapter-arrow">→</span>
    </a>

    <a href="/learn/lgs-grundlagen/" class="lm-chapter">
      <div class="lm-chapter-num">4</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Lineare Gleichungssysteme</div>
        <div class="lm-chapter-desc">Ax = b, Gauß-Algorithmus, Lösbarkeit mit Rang-Kriterium</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
      <span class="lm-chapter-arrow">→</span>
    </a>

    <a href="/learn/lgs-parameter/" class="lm-chapter">
      <div class="lm-chapter-num">5</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">LGS mit Parametern</div>
        <div class="lm-chapter-desc">Lösbarkeit in Abhängigkeit von λ, Fallunterscheidung, Determinantentest</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
      <span class="lm-chapter-arrow">→</span>
    </a>

    </div><!-- end lm-chapters Lineare Algebra -->
  </div><!-- end lm-section -->

  <!-- Analytische Geometrie -->
  <div class="lm-section">
    <div class="lm-section-header">
      <span class="lm-section-eyebrow lm-section-eyebrow--geo">Analytische Geometrie</span>
      <span class="lm-section-title">Vektoren & Raum</span>
    </div>
    <div class="lm-chapters">

      <a href="/learn/vektoren-grundlagen/" class="lm-chapter lm-chapter--geo">
        <div class="lm-chapter-num">1</div>
        <div class="lm-chapter-body">
          <div class="lm-chapter-title">Vektoren – Grundlagen</div>
          <div class="lm-chapter-desc">Betrag, Einheitsvektor, Addition, Skalarprodukt, Winkelberechnung</div>
        </div>
        <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
        <span class="lm-chapter-arrow">→</span>
      </a>

      <a href="/learn/vektorprodukt-spatprodukt/" class="lm-chapter lm-chapter--geo">
        <div class="lm-chapter-num">2</div>
        <div class="lm-chapter-body">
          <div class="lm-chapter-title">Vektorprodukt & Spatprodukt</div>
          <div class="lm-chapter-desc">Kreuzprodukt, Flächen, Volumen, geometrische Nachweise</div>
        </div>
        <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
        <span class="lm-chapter-arrow">→</span>
      </a>

      <a href="/learn/geraden-ebenen/" class="lm-chapter lm-chapter--geo">
        <div class="lm-chapter-num">3</div>
        <div class="lm-chapter-body">
          <div class="lm-chapter-title">Geraden und Ebenen</div>
          <div class="lm-chapter-desc">Parameterform, Normalenvektor, Koordinatenform, Lagebeziehungen</div>
        </div>
        <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
        <span class="lm-chapter-arrow">→</span>
      </a>

      <a href="/learn/lagebeziehungen-abstaende/" class="lm-chapter lm-chapter--geo">
        <div class="lm-chapter-num">4</div>
        <div class="lm-chapter-body">
          <div class="lm-chapter-title">Lagebeziehungen & Abstände</div>
          <div class="lm-chapter-desc">Ebene↔Ebene, Hesse-Formel, windschief, alle Abstands­fälle</div>
        </div>
        <span class="lm-chapter-badge lm-chapter-badge--new">Neu</span>
        <span class="lm-chapter-arrow">→</span>
      </a>

    </div><!-- end lm-chapters Geo -->
  </div><!-- end lm-section -->

  <a href="/assets/pdfs/Mathematik_Skript.pdf" class="lm-pdf-hint">
    Lieber als PDF? Das vollständige Skript steht zum Download bereit.
  </a>

</div>
