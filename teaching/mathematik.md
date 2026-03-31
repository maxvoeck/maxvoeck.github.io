---
layout: page
title: 
permalink: /teaching/mathematik/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   和北 JAPANDI DESIGN SYSTEM – Mathematik für Studienkolleg
   Japanese × Norwegian Minimalism
   ═══════════════════════════════════════════════════════════════ */

/* ─── Design Tokens ─── */
:root {
  /* Japandi Palette */
  --sumi: #1a1a18;
  --kuro: #2c2c28;
  --hai: #3d3d38;
  --kinari: #f0ece4;
  --shiro: #f7f5f0;
  --kinu: #e8e3d8;
  --ishi: #b8b3a8;
  --sugi: #8a8578;

  /* Akzentfarben */
  --beni: #c45c3e;
  --matcha: #7a8c6e;
  --ai: #5b7a8c;
  --kitsune: #c49a6c;
  --sakura: #c4868a;

  /* Semantische Farben */
  --algebra: var(--ai);
  --vektor: var(--kitsune);
  --diff: var(--beni);
  --integral: var(--matcha);
  --tools: var(--sakura);

  /* Flächen */
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
  max-width: 920px;
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
  stroke: var(--beni);
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
.ma-section:nth-child(4) { animation-delay: 0.3s; }
.ma-section:nth-child(5) { animation-delay: 0.4s; }
.ma-section:nth-child(6) { animation-delay: 0.5s; }

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
}

.ma-section.collapsed .ma-section-toggle {
  transform: rotate(-90deg);
}

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

/* ─── Quick Actions ─── */
.ma-quick-actions {
  display: flex;
  gap: var(--space-4);
  justify-content: center;
  flex-wrap: wrap;
  margin-top: var(--space-6);
}

/* ─── Mobile Optimierungen ─── */
@media (max-width: 600px) {
  /* Fix Minima theme double-padding */
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

  /* ─ Hero ─ */
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

  /* ─ Quick Actions: stapeln statt nebeneinander ─ */
  .ma-quick-actions {
    flex-direction: column;
    gap: var(--space-3);
    align-items: stretch;
  }

  .ma-quick-actions .ma-btn {
    justify-content: center;
    padding: var(--space-3) var(--space-4) !important;
    font-size: 14px !important;
  }

  /* ─ Section Headers ─ */
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
    flex-shrink: 0;
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
    flex-shrink: 0;
  }

  /* ─ Cards ─ */
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

  /* ─ Buttons & Check ─ */
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

  /* ─ Footer ─ */
  .ma-footer {
    margin-top: var(--space-12);
    flex-direction: column;
    text-align: center;
  }
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

.ma-section--vektor .ma-section-icon { 
  background: rgba(255, 149, 0, 0.12); 
  color: var(--vektor);
}
.ma-section--algebra .ma-section-icon { 
  background: rgba(90, 200, 250, 0.12); 
  color: var(--algebra);
}
.ma-section--diff .ma-section-icon { 
  background: rgba(255, 45, 85, 0.12); 
  color: var(--diff);
}
.ma-section--integral .ma-section-icon { 
  background: rgba(52, 199, 89, 0.12); 
  color: var(--integral);
}
.ma-section--tools .ma-section-icon { 
  background: rgba(175, 82, 222, 0.12); 
  color: var(--tools);
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

@media (min-width: 1024px) {
  .ma-grid--tools {
    grid-template-columns: repeat(3, 1fr);
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

.ma-section--vektor .ma-card-number { color: var(--vektor); }
.ma-section--algebra .ma-card-number { color: var(--algebra); }
.ma-section--diff .ma-card-number { color: var(--diff); }
.ma-section--integral .ma-card-number { color: var(--integral); }
.ma-section--tools .ma-card-number { color: var(--tools); }

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
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
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
  font-family: var(--font-body);
  position: relative;
  z-index: 2;
}

.ma-btn--primary {
  background: var(--beni);
  color: white !important;
}

.ma-btn--primary:hover {
  background: #0051D5;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 122, 255, 0.3);
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
  border-color: var(--matcha);
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
  background: var(--matcha);
  border-color: var(--matcha);
}

.ma-card-complete .ma-check svg {
  opacity: 1;
  transform: scale(1);
}

/* ─── Tools Section Special ─── */
.ma-section--tools .ma-card {
  background: linear-gradient(135deg, var(--bg-secondary) 0%, rgba(175, 82, 222, 0.05) 100%);
  border: 1px solid rgba(175, 82, 222, 0.1);
}

.ma-section--tools .ma-card:hover {
  border-color: rgba(175, 82, 222, 0.2);
  box-shadow: 0 8px 32px rgba(175, 82, 222, 0.15);
}

.ma-tool-icon {
  width: 40px;
  height: 40px;
  border-radius: var(--radius-md);
  background: linear-gradient(135deg, var(--tools) 0%, #BF5AF2 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  margin-bottom: var(--space-3);
  box-shadow: 0 4px 12px rgba(175, 82, 222, 0.3);
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
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.6s backwards;
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

<!-- KaTeX -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.js"></script>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Mathematik</h1>

    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 30 abgeschlossen</div>
    </div>

    <div style="width: 100%; text-align: center; margin-top: var(--space-6);">
      <a href="/assets/pdfs/Mathematik_Skript.pdf" class="ma-btn ma-btn--primary" style="padding: var(--space-3) var(--space-6); font-size: 15px;" onclick="event.stopPropagation()">📄 Gesamtskript herunterladen (PDF)</a>
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

  <!-- Algebra -->
  <div class="ma-section ma-section--algebra collapsed">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Lineare Algebra</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="a1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Matrizen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Matrizen_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('a1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a2">
        <div class="ma-card-header">
          <span class="ma-card-number">02</span>
          <h4>Determinanten</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Matrizen_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_determinanten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('a2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a3">
        <div class="ma-card-header">
          <span class="ma-card-number">03</span>
          <h4>Matrizengleichungen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Matrizen_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <button class="ma-check" onclick="toggleModule('a3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a4">
        <div class="ma-card-header">
          <span class="ma-card-number">04</span>
          <h4>Lineare Gleichungssysteme</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/LGS_2_1-5.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('a4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a5">
        <div class="ma-card-header">
          <span class="ma-card-number">05</span>
          <h4>Parameterabhängigkeit</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/LGS_2_2-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <button class="ma-check" onclick="toggleModule('a5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Vektorrechnung -->
  <div class="ma-section ma-section--vektor collapsed">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Vektorrechnung</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="v1">
        <div class="ma-card-header">
          <span class="ma-card-number">06</span>
          <h4>Grundlagen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_1-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="v2">
        <div class="ma-card-header">
          <span class="ma-card-number">07</span>
          <h4>Vektor- & Spatprodukt</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_2-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vektorprodukt.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="v3">
        <div class="ma-card-header">
          <span class="ma-card-number">08</span>
          <h4>Geraden und Ebenen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="v4">
        <div class="ma-card-header">
          <span class="ma-card-number">09</span>
          <h4>Abstände und Lagen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Differentialrechnung -->
  <div class="ma-section ma-section--diff collapsed">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Differentialrechnung</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="d1">
        <div class="ma-card-header">
          <span class="ma-card-number">10</span>
          <h4>Zahlenfolgen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Zahlenfolgen_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d2">
        <div class="ma-card-header">
          <span class="ma-card-number">11</span>
          <h4>Grenzwerte von Folgen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Grenzwerte_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d3">
        <div class="ma-card-header">
          <span class="ma-card-number">12</span>
          <h4>Grenzwerte im Unendlichen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Funktion_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d4">
        <div class="ma-card-header">
          <span class="ma-card-number">13</span>
          <h4>Grenzwerte an einer Stelle</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Grenzwerte_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d5">
        <div class="ma-card-header">
          <span class="ma-card-number">14</span>
          <h4>Asymptoten</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Grenzwerte_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_asymptoten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d6">
        <div class="ma-card-header">
          <span class="ma-card-number">15</span>
          <h4>Steigung und Ableitung</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Funktion_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d6', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d7">
        <div class="ma-card-header">
          <span class="ma-card-number">16</span>
          <h4>Ableitungsregeln</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Funktion_2_4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d7', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d8">
        <div class="ma-card-header">
          <span class="ma-card-number">17</span>
          <h4>Regel von de L'Hôpital</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Hospital_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_hospital.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d8', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d9">
        <div class="ma-card-header">
          <span class="ma-card-number">18</span>
          <h4>Extrempunkte</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Extremwert_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_extrempunkte.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d9', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d10">
        <div class="ma-card-header">
          <span class="ma-card-number">19</span>
          <h4>Wendepunkte</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Wendepunkt_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_wendepunkte.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d10', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d11">
        <div class="ma-card-header">
          <span class="ma-card-number">20</span>
          <h4>Kurvendiskussion</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Kurvendiskusion_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d11', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="d12">
        <div class="ma-card-header">
          <span class="ma-card-number">21</span>
          <h4>Extremwertaufgaben</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Extrem_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d12', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Integralrechnung -->
  <div class="ma-section ma-section--integral collapsed">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Integralrechnung</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="i1">
        <div class="ma-card-header">
          <span class="ma-card-number">22</span>
          <h4>Einführung</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Integral_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="i2">
        <div class="ma-card-header">
          <span class="ma-card-number">23</span>
          <h4>Integrationsmethoden</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Integral_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="i3">
        <div class="ma-card-header">
          <span class="ma-card-number">24</span>
          <h4>Hauptsatz & Flächen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Integral_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="i4">
        <div class="ma-card-header">
          <span class="ma-card-number">25</span>
          <h4>Rotationsvolumen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/pdfs/Intergal_2_4-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Interaktive Tools -->
  <div class="ma-section ma-section--tools collapsed" id="tools">
    <div class="ma-section-header" onclick="toggleSection(this)">
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Interaktive Tools</h2>
      </div>
      <div class="ma-section-toggle">▼</div>
    </div>
    <div class="ma-grid ma-grid--tools">
      <div class="ma-card" data-module="t1">
        <div class="ma-card-header">
          <h4>Tangenten-Explorer</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/interactive/tangenten_explorer.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()" style="flex: 1;">→ Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="t2">
        <div class="ma-card-header">
          <h4>3D-Vektor-Explorer</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/interactive/vektor_explorer.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()" style="flex: 1;">→ Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="t3">
        <div class="ma-card-header">
          <h4>Geraden & Ebenen</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/interactive/geraden_ebenen_explorer.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()" style="flex: 1;">→ Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="t4">
        <div class="ma-card-header">
          <h4>Matrizen-Explorer</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/interactive/matrizen_explorer.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()" style="flex: 1;">→ Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="t5">
        <div class="ma-card-header">
          <h4>Determinanten-Rechner</h4>
        </div>
        <div class="ma-actions">
          <a href="/assets/interactive/determinanten_rechner.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()" style="flex: 1;">→ Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>30 Module & 5 Tools</strong> · Algebra, Vektoren, Analysis & Integralrechnung
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'math-progress-v2';
const TOTAL_MODULES = 30;
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

  // Mark completed cards
  document.querySelectorAll('[data-module]').forEach(card => {
    if (progress[card.dataset.module]) {
      card.classList.add('ma-card-complete');
    } else {
      card.classList.remove('ma-card-complete');
    }
  });
}

function toggleSection(header) {
  const section = header.parentElement;
  section.classList.toggle('collapsed');
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
      frage: "Berechne die Determinante: $\\det\\begin{pmatrix} 3 & 1 \\\\ 5 & 2 \\end{pmatrix}$",
      hint: "Denk an die Formel ad - bc.",
      antwort: "$\\det = 3 \\cdot 2 - 1 \\cdot 5 = 6 - 5 = 1$",
      quiz: "/assets/quizzes/quiz_determinanten.html"
    },
    {
      diff: "Grundlagen",
      frage: "Löse das Gleichungssystem: $2x + y = 7$ und $x - y = 2$",
      hint: "Addiere beide Gleichungen, um y zu eliminieren.",
      antwort: "Addition: $3x = 9$, also $x = 3$. Einsetzen: $y = 1$. Lösung: $(3, 1)$.",
      quiz: "/assets/quizzes/quiz_lgs_grundlagen.html"
    },
    {
      diff: "Mittel",
      frage: "Gegeben: $A = \\begin{pmatrix} 1 & 2 \\\\ 3 & 4 \\end{pmatrix}$. Berechne $A^2$.",
      antwort: "$A^2 = \\begin{pmatrix} 7 & 10 \\\\ 15 & 22 \\end{pmatrix}$",
      quiz: "/assets/quizzes/quiz_matrizen_grundlagen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Berechne das Skalarprodukt: $\\vec{a} = \\begin{pmatrix} 2 \\\\ -1 \\\\ 3 \\end{pmatrix}$ und $\\vec{b} = \\begin{pmatrix} 1 \\\\ 4 \\\\ -2 \\end{pmatrix}$",
      antwort: "$\\vec{a} \\cdot \\vec{b} = 2 - 4 - 6 = -8$",
      quiz: "/assets/quizzes/quiz_vektorprodukt.html"
    },
    {
      diff: "Mittel",
      frage: "Bestimme den Abstand des Punktes $P(1, 2, 3)$ vom Ursprung.",
      antwort: "$d = \\sqrt{1^2 + 2^2 + 3^2} = \\sqrt{14} \\approx 3{,}74$"
    },
    {
      diff: "Klausurniveau",
      frage: "Zeige, dass $\\vec{a} = \\begin{pmatrix} 1 \\\\ 0 \\\\ -1 \\end{pmatrix}$ und $\\vec{b} = \\begin{pmatrix} 2 \\\\ 1 \\\\ 2 \\end{pmatrix}$ senkrecht stehen.",
      antwort: "$\\vec{a} \\cdot \\vec{b} = 2 + 0 - 2 = 0$. Da Skalarprodukt $= 0$, stehen sie senkrecht.",
      quiz: "/assets/quizzes/quiz_vektorprodukt.html"
    },
    {
      diff: "Grundlagen",
      frage: "Bestimme $f'(x)$ für $f(x) = 3x^4 - 2x^2 + 5x - 1$.",
      antwort: "$f'(x) = 12x^3 - 4x + 5$",
      quiz: "/assets/quizzes/quiz_ableitung_grundlagen.html"
    },
    {
      diff: "Mittel",
      frage: "Leite ab: $f(x) = \\sin(x) \\cdot e^x$ (Produktregel).",
      antwort: "$f'(x) = \\cos(x) \\cdot e^x + \\sin(x) \\cdot e^x = e^x(\\cos x + \\sin x)$",
      quiz: "/assets/quizzes/quiz_ableitungsregeln.html"
    },
    {
      diff: "Mittel",
      frage: "Finde die Extrempunkte von $f(x) = x^3 - 3x + 2$.",
      hint: "Setze f'(x) = 0 und prüfe mit f''(x).",
      antwort: "$x = \\pm 1$. Bei $x=1$: Minimum $(1, 0)$. Bei $x=-1$: Maximum $(-1, 4)$.",
      quiz: "/assets/quizzes/quiz_extrempunkte.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Bestimme die Wendepunkte von $f(x) = x^4 - 6x^2 + 8x + 1$.",
      antwort: "$f''(x) = 12x^2 - 12 = 0 \\Rightarrow x = \\pm 1$. Wendepunkte: $W_1(1, 4)$ und $W_2(-1, -12)$.",
      quiz: "/assets/quizzes/quiz_wendepunkte.html"
    },
    {
      diff: "Grundlagen",
      frage: "Berechne $\\lim_{n \\to \\infty} \\frac{3n^2 + 2n}{n^2 - 1}$.",
      hint: "Teile durch die höchste Potenz von n.",
      antwort: "$\\frac{3 + 0}{1 - 0} = 3$",
      quiz: "/assets/quizzes/quiz_grenzwerte_folgen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Berechne $\\int (4x^3 - 6x + 1)\\,dx$.",
      antwort: "$x^4 - 3x^2 + x + C$",
      quiz: "/assets/quizzes/quiz_integral_einfuehrung.html"
    },
    {
      diff: "Mittel",
      frage: "Berechne die Fläche unter $f(x) = x^2$ auf $[0, 3]$.",
      antwort: "$A = \\left[\\frac{x^3}{3}\\right]_0^3 = 9$ FE",
      quiz: "/assets/quizzes/quiz_hauptsatz_flaechen.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Berechne $\\int x \\cdot e^x \\, dx$ (partielle Integration).",
      hint: "Wähle u = x und v' = eˣ.",
      antwort: "$x \\cdot e^x - e^x + C = e^x(x-1) + C$",
      quiz: "/assets/quizzes/quiz_integrationsmethoden.html"
    },
    {
      diff: "Mittel",
      frage: "Bestimme mit L'Hôpital: $\\lim_{x \\to 0} \\frac{\\sin x}{x}$",
      antwort: "Typ $\\frac{0}{0}$. L'Hôpital: $\\frac{\\cos 0}{1} = 1$.",
      quiz: "/assets/quizzes/quiz_hospital.html"
    },
    {
      diff: "Klausurniveau",
      frage: "Bestimme die Asymptoten von $f(x) = \\frac{2x^2 + 1}{x - 1}$.",
      hint: "Prüfe senkrechte und schräge Asymptoten.",
      antwort: "Senkrecht: $x = 1$. Polynomdivision ergibt schräge Asymptote: $y = 2x + 2$.",
      quiz: "/assets/quizzes/quiz_asymptoten.html"
    },
    {
      diff: "Grundlagen",
      frage: "Berechne: $\\frac{2}{3} + \\frac{3}{4}$",
      hint: "Finde den gemeinsamen Nenner.",
      antwort: "$\\frac{8}{12} + \\frac{9}{12} = \\frac{17}{12}$"
    },
    {
      diff: "Mittel",
      frage: "Rotationsvolumen: $f(x) = \\sqrt{x}$ auf $[0, 4]$ um die x-Achse.",
      antwort: "$V = \\pi \\int_0^4 x\\,dx = \\pi \\cdot 8 = 8\\pi$ VE",
      quiz: "/assets/quizzes/quiz_rotationsvolumen.html"
    },
    {
      diff: "Grundlagen",
      frage: "Ist die Folge $a_n = \\frac{(-1)^n}{n}$ konvergent? Falls ja, gegen welchen Grenzwert?",
      antwort: "Ja, konvergent. $\\lim_{n \\to \\infty} \\frac{(-1)^n}{n} = 0$, da $|a_n| = \\frac{1}{n} \\to 0$.",
      quiz: "/assets/quizzes/quiz_zahlenfolgen.html"
    },
    {
      diff: "Mittel",
      frage: "Bestimme die Gleichung der Tangente an $f(x) = x^2$ im Punkt $P(2, 4)$.",
      antwort: "$f'(x) = 2x$, also $f'(2) = 4$. Tangente: $y = 4(x - 2) + 4 = 4x - 4$.",
      quiz: "/assets/quizzes/quiz_ableitung_grundlagen.html"
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
