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

  --bg-primary: #000000;
  --bg-secondary: #1C1C1E;
  --bg-tertiary: #2C2C2E;
  --text-primary: #FFFFFF;
  --text-secondary: #EBEBF5;
  --text-tertiary: #8E8E93;
  --separator: rgba(255, 255, 255, 0.10);

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
  font-size: clamp(36px,5vw,56px); font-weight: 700; letter-spacing: -.025em;
  line-height: 1.06; margin-bottom: var(--space-4);
  background: linear-gradient(135deg, #fff 50%, #8E8E93 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
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
  border-color: rgba(255,255,255,.18);
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

/* PDF hint */
.lm-pdf-hint {
  margin-top: var(--space-10);
  display: flex; align-items: center; gap: var(--space-3);
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-lg); padding: var(--space-4) var(--space-5);
  font-size: 14px; color: var(--text-tertiary); text-decoration: none;
  transition: all var(--transition-base);
}
.lm-pdf-hint:hover { border-color: rgba(255,255,255,.2); color: var(--text-secondary); }

@keyframes fadeIn { from{opacity:0;transform:translateY(12px)} to{opacity:1;transform:none} }
@media(max-width:600px){.lm-container{padding:var(--space-8) var(--space-4);} .lm-chapter{padding:var(--space-4);gap:var(--space-4);}}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important;}}
</style>

<div class="lm-container">

  <div class="lm-breadcrumb">
    <a href="/learn/">Learn</a>
    <span class="lm-breadcrumb-sep">›</span>
    <span class="lm-breadcrumb-current">Mathematik</span>
  </div>

  <div class="lm-hero">
    <div class="lm-hero-eyebrow">📐 Mathematik</div>
    <h1>Lineare Algebra</h1>
    <p class="lm-hero-sub">Von Matrizen und Determinanten bis zu linearen Gleichungssystemen — Schritt für Schritt erklärt, direkt im Browser.</p>
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

    <div class="lm-chapter lm-chapter--locked">
      <div class="lm-chapter-num">2</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Determinanten</div>
        <div class="lm-chapter-desc">2×2, Regel von Sarrus, Laplace-Entwicklung, inverse Matrizen</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--soon">Bald</span>
    </div>

    <div class="lm-chapter lm-chapter--locked">
      <div class="lm-chapter-num">3</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Matrizengleichungen & Rang</div>
        <div class="lm-chapter-desc">Gleichungen mit Matrizen lösen, Rang, Zeilenstufenform</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--soon">Bald</span>
    </div>

    <div class="lm-chapter lm-chapter--locked">
      <div class="lm-chapter-num">4</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">Lineare Gleichungssysteme</div>
        <div class="lm-chapter-desc">Ax = b, Gauß-Algorithmus, Lösbarkeit mit Rang-Kriterium</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--soon">Bald</span>
    </div>

    <div class="lm-chapter lm-chapter--locked">
      <div class="lm-chapter-num">5</div>
      <div class="lm-chapter-body">
        <div class="lm-chapter-title">LGS mit Parametern</div>
        <div class="lm-chapter-desc">Lösbarkeit in Abhängigkeit von λ, Fallunterscheidung, Determinantentest</div>
      </div>
      <span class="lm-chapter-badge lm-chapter-badge--soon">Bald</span>
    </div>

  </div>

  <a href="/assets/pdfs/Mathematik_Skript.pdf" class="lm-pdf-hint">
    📄 &nbsp;Lieber als PDF? Das vollständige Skript steht zum Download bereit.
  </a>

</div>
