---
layout: page
title: 
permalink: /teaching/mathematik/
---

<style>
/* ═══════════════════════════════════════════════════════════════
   APPLE DESIGN SYSTEM – Mathematik für Studienkolleg
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
  --vektor: #FF9500;
  --algebra: #5AC8FA;
  --diff: #FF2D55;
  --integral: #34C759;
  --tools: #AF52DE;
  
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
.ma-section:nth-child(4) { animation-delay: 0.3s; }
.ma-section:nth-child(5) { animation-delay: 0.4s; }
.ma-section:nth-child(6) { animation-delay: 0.5s; }

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
</style>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Mathematik</h1>
    <p class="ma-hero-subtitle">Gesamtskript, 28 Module, interaktive Tools und Übungsgeneratoren für Vektoren, Algebra, Analysis und Integralrechnung</p>
    
    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 28 abgeschlossen</div>
    </div>

  </div>

  <!-- Navigation Cards -->
  <div style="display: grid; gap: var(--space-6); max-width: 800px; margin: 0 auto;">

    <a href="/teaching/mathematik-materialien/" style="text-decoration: none; display: block;">
      <div class="ma-card" style="padding: var(--space-8); cursor: pointer;">
        <div style="display: flex; align-items: center; gap: var(--space-5);">
          <div class="ma-section-icon" style="width: 64px; height: 64px; font-size: 32px; background: rgba(90, 200, 250, 0.12); color: var(--algebra);">📚</div>
          <div style="flex: 1;">
            <h3 style="font-size: 24px; font-weight: 600; color: var(--text-primary); margin-bottom: var(--space-2);">Lehrmaterialien</h3>
            <p style="font-size: 15px; color: var(--text-secondary); margin: 0;">Gesamtskript und alle 28 Module als PDFs — Algebra, Vektoren, Analysis und Integralrechnung</p>
          </div>
          <div style="font-size: 24px; color: var(--text-tertiary);">→</div>
        </div>
      </div>
    </a>

    <a href="/teaching/mathematik-uebungen/" style="text-decoration: none; display: block;">
      <div class="ma-card" style="padding: var(--space-8); cursor: pointer;">
        <div style="display: flex; align-items: center; gap: var(--space-5);">
          <div class="ma-section-icon" style="width: 64px; height: 64px; font-size: 32px; background: rgba(175, 82, 222, 0.12); color: var(--tools);">✍️</div>
          <div style="flex: 1;">
            <h3 style="font-size: 24px; font-weight: 600; color: var(--text-primary); margin-bottom: var(--space-2);">Übungen & Quizzes</h3>
            <p style="font-size: 15px; color: var(--text-secondary); margin: 0;">Interaktive Quizzes, Tools und Aufgabengeneratoren zum Üben und Vertiefen</p>
          </div>
          <div style="font-size: 24px; color: var(--text-tertiary);">→</div>
        </div>
      </div>
    </a>

  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>28 Module</strong> · Algebra, Vektoren, Analysis & Integralrechnung
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'math-progress-v2';
const TOTAL_MODULES = 28;
const CIRCUMFERENCE = 339.292;

function getProgress() {
  try {
    return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {};
  } catch {
    return {};
  }
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
}

document.addEventListener('DOMContentLoaded', updateUI);
if (document.readyState !== 'loading') updateUI();
</script>
