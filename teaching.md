---
layout: page
title: 
permalink: /teaching/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   APPLE DESIGN SYSTEM – Lehrmaterialien Übersicht
   ═══════════════════════════════════════════════════════════════ */

/* ─── Design Tokens ─── */
:root {
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-indigo: #5856D6;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;
  --system-purple: #AF52DE;
  --system-red: #FF3B30;
  --system-teal: #5AC8FA;
  --system-yellow: #FFCC00;

  --math: #FF2D55;
  --econ: #FF9500;
  --cs: #007AFF;

  --gray-1: #F5F5F7;
  --gray-6: #8E8E93;

  --bg-primary: #FFFFFF;
  --bg-secondary: #F5F5F7;
  --bg-tertiary: #FFFFFF;
  --text-primary: #000000;
  --text-secondary: #3A3A3C;
  --text-tertiary: #8E8E93;
  --separator: rgba(0, 0, 0, 0.08);
  --separator-strong: rgba(0, 0, 0, 0.16);

  --font-stack: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", "Helvetica Neue", Helvetica, Arial, sans-serif;
  --font-mono: "SF Mono", SFMono-Regular, ui-monospace, Menlo, Monaco, monospace;

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

  --shadow-sm: 0 1px 2px rgba(0,0,0,0.04);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
  --shadow-lg: 0 12px 24px rgba(0,0,0,0.12);
  --shadow-xl: 0 24px 48px rgba(0,0,0,0.16);

  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

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
  margin-bottom: var(--space-4);
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
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  line-height: 1.381;
}

/* ─── Course Cards Grid ─── */
.ma-courses {
  display: grid;
  gap: var(--space-5);
  margin-bottom: var(--space-16);
}

/* ─── Course Card ─── */
.ma-course {
  background: var(--bg-secondary);
  border-radius: var(--radius-2xl);
  padding: var(--space-8);
  position: relative;
  overflow: hidden;
  transition: all var(--transition-base);
  border: 2px solid transparent;
  text-decoration: none !important;
  display: block;
  color: inherit !important;
}

.ma-course::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, transparent 50%);
  opacity: 0;
  transition: opacity var(--transition-base);
}

.ma-course:hover {
  transform: translateY(-3px);
  box-shadow: var(--shadow-lg);
  background: var(--bg-tertiary);
  text-decoration: none !important;
}

.ma-course:hover::before {
  opacity: 1;
}

.ma-course:active {
  transform: scale(0.98);
  transition-duration: var(--transition-fast);
}

.ma-course--math { border-left: 4px solid var(--math); }
.ma-course--econ { border-left: 4px solid var(--econ); }
.ma-course--cs { border-left: 4px solid var(--cs); }

.ma-course--math:hover { box-shadow: 0 12px 32px rgba(255, 45, 85, 0.1); }
.ma-course--econ:hover { box-shadow: 0 12px 32px rgba(255, 149, 0, 0.1); }
.ma-course--cs:hover { box-shadow: 0 12px 32px rgba(0, 122, 255, 0.1); }

/* ─── Course Header ─── */
.ma-course-header {
  display: flex;
  align-items: center;
  gap: var(--space-4);
  margin-bottom: var(--space-4);
}

.ma-course-icon {
  width: 52px;
  height: 52px;
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  flex-shrink: 0;
  transition: transform var(--transition-spring);
}

.ma-course:hover .ma-course-icon {
  transform: scale(1.1) rotate(-5deg);
}

.ma-course--math .ma-course-icon { background: rgba(255, 45, 85, 0.12); }
.ma-course--econ .ma-course-icon { background: rgba(255, 149, 0, 0.12); }
.ma-course--cs .ma-course-icon { background: rgba(0, 122, 255, 0.12); }

.ma-course-title-group {
  flex: 1;
}

.ma-course h2 {
  font-size: 24px;
  font-weight: 600;
  letter-spacing: -0.021em;
  line-height: 1.14286;
  color: var(--text-primary);
  margin: 0 0 var(--space-1) 0;
}

.ma-course-count {
  font-size: 14px;
  color: var(--text-tertiary);
  font-weight: 400;
}

/* ─── Course Description ─── */
.ma-course-desc {
  font-size: 15px;
  line-height: 1.5;
  color: var(--text-secondary);
  margin-bottom: var(--space-5);
}

/* ─── Tags ─── */
.ma-tags {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-2);
  margin-bottom: var(--space-6);
}

.ma-tag {
  padding: var(--space-1) var(--space-3);
  border-radius: var(--radius-sm);
  font-size: 12px;
  font-weight: 500;
  letter-spacing: 0.02em;
  background: rgba(0, 0, 0, 0.04);
  color: var(--text-tertiary);
  transition: all var(--transition-fast);
}

@media (prefers-color-scheme: dark) {
  .ma-tag {
    background: rgba(255, 255, 255, 0.06);
  }
}

.ma-course--math .ma-tag { color: var(--math); background: rgba(255, 45, 85, 0.08); }
.ma-course--econ .ma-tag { color: var(--econ); background: rgba(255, 149, 0, 0.08); }
.ma-course--cs .ma-tag { color: var(--cs); background: rgba(0, 122, 255, 0.08); }

/* ─── Course Actions ─── */
.ma-course-actions {
  display: flex;
  gap: var(--space-3);
  flex-wrap: wrap;
  position: relative;
  z-index: 2;
}

.ma-btn {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius-md);
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
  transition: all var(--transition-fast);
  border: none;
  cursor: pointer;
  font-family: inherit;
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

.ma-btn-arrow {
  font-size: 14px;
  opacity: 0;
  transform: translateX(-4px);
  transition: all var(--transition-fast);
}

.ma-btn:hover .ma-btn-arrow {
  opacity: 1;
  transform: translateX(0);
}

/* ─── Footer ─── */
.ma-footer {
  padding-top: var(--space-8);
  border-top: 1px solid var(--separator);
  text-align: center;
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.4s backwards;
}

.ma-footer-text {
  font-size: 14px;
  color: var(--text-tertiary);
  font-weight: 400;
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

.ma-course {
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) backwards;
}

.ma-course:nth-child(1) { animation-delay: 0.1s; }
.ma-course:nth-child(2) { animation-delay: 0.2s; }
.ma-course:nth-child(3) { animation-delay: 0.3s; }

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
  .ma-course:hover {
    transform: none;
    box-shadow: var(--shadow-sm);
  }

  .ma-course:active {
    transform: scale(0.98);
    background: var(--bg-tertiary);
  }
}

/* ─── Print Styles ─── */
@media print {
  .ma-btn { display: none; }
  .ma-course { break-inside: avoid; }
}
</style>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Lehrmaterialien</h1>
    <p class="ma-hero-subtitle">Ausgewählte Materialien aus meiner Lehrtätigkeit, abgestimmt auf die Anforderungen der Feststellungsprüfung</p>
  </div>

  <!-- Course Cards -->
  <div class="ma-courses">

    <!-- Mathematik -->
    <div class="ma-course ma-course--math">
      <div class="ma-course-header">
        <div class="ma-course-icon">📐</div>
        <div class="ma-course-title-group">
          <h2>Mathematik</h2>
          <div class="ma-course-count">28 Module · 3 interaktive Tools</div>
        </div>
      </div>
      <p class="ma-course-desc">Fundierte Vorbereitung auf Analysis und Lineare Algebra für technische Studiengänge – von Vektorrechnung bis Rotationsvolumen</p>
      <div class="ma-tags">
        <span class="ma-tag">Vektorrechnung</span>
        <span class="ma-tag">Lineare Algebra</span>
        <span class="ma-tag">Differentialrechnung</span>
        <span class="ma-tag">Integralrechnung</span>
      </div>
      <div class="ma-course-actions">
        <a href="/teaching/mathematik/" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Lernpfad öffnen <span class="ma-btn-arrow">→</span></a>
        <a href="/assets/pdfs/Mathematik_Skript.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">📄 Gesamtskript</a>
      </div>
    </div>

    <!-- VWL -->
    <div class="ma-course ma-course--econ">
      <div class="ma-course-header">
        <div class="ma-course-icon">📊</div>
        <div class="ma-course-title-group">
          <h2>Volkswirtschaftslehre</h2>
          <div class="ma-course-count">13 Module · Mikro & Makro</div>
        </div>
      </div>
      <p class="ma-course-desc">Makro- und Mikroökonomie mit praxisnahen Beispielen – von Bedürfnissen bis zur Arbeitsmarktpolitik</p>
      <div class="ma-tags">
        <span class="ma-tag">Marktgleichgewicht</span>
        <span class="ma-tag">Konsumentenrente</span>
        <span class="ma-tag">BIP & Konjunktur</span>
        <span class="ma-tag">Wirtschaftspolitik</span>
      </div>
      <div class="ma-course-actions">
        <a href="/teaching/vwl/" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Lernpfad öffnen <span class="ma-btn-arrow">→</span></a>
      </div>
    </div>

    <!-- Informatik -->
    <div class="ma-course ma-course--cs">
      <div class="ma-course-header">
        <div class="ma-course-icon">🐍</div>
        <div class="ma-course-title-group">
          <h2>Informatik</h2>
          <div class="ma-course-count">5 Module · Python</div>
        </div>
      </div>
      <p class="ma-course-desc">Grundlagen der Programmierung und algorithmisches Denken – von print() bis zu eigenen Funktionen</p>
      <div class="ma-tags">
        <span class="ma-tag">Python</span>
        <span class="ma-tag">Kontrollstrukturen</span>
        <span class="ma-tag">Listen</span>
        <span class="ma-tag">Funktionen</span>
      </div>
      <div class="ma-course-actions">
        <a href="/teaching/informatik/" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Lernpfad öffnen <span class="ma-btn-arrow">→</span></a>
      </div>
    </div>

  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <p class="ma-footer-text">Alle Materialien frei verwendbar für Bildungszwecke</p>
  </div>

</div>