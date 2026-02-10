---
layout: default
---

<style>
/* ═══════════════════════════════════════════════════════════════
   APPLE DESIGN SYSTEM – Startseite
   ═══════════════════════════════════════════════════════════════ */

:root {
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-indigo: #5856D6;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;
  --system-purple: #AF52DE;
  --system-teal: #5AC8FA;

  --about: #5856D6;
  --analysen: #5AC8FA;
  --teaching: #FF9500;

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

  --shadow-sm: 0 1px 2px rgba(0,0,0,0.04);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
  --shadow-lg: 0 12px 24px rgba(0,0,0,0.12);

  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
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
  }
}

*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body, html, .page-content, .wrapper, main {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
  font-family: var(--font-stack);
  line-height: 1.47059;
  letter-spacing: -0.022em;
}

/* ─── Layout ─── */
.ma-home {
  max-width: 980px;
  margin: 0 auto;
  padding: var(--space-8) var(--space-5);
}

@media (min-width: 768px) {
  .ma-home {
    padding: var(--space-16) var(--space-8);
  }
}

/* ─── Hero ─── */
.ma-hero {
  text-align: center;
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1);
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
  max-width: 500px;
  margin: 0 auto;
  line-height: 1.381;
}

/* ─── Cards Grid ─── */
.ma-grid {
  display: grid;
  gap: var(--space-5);
}

@media (min-width: 768px) {
  .ma-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* ─── Section Card ─── */
.ma-card {
  background: var(--bg-secondary);
  border-radius: var(--radius-2xl);
  padding: var(--space-8) var(--space-6);
  position: relative;
  overflow: hidden;
  transition: all var(--transition-base);
  border: 2px solid transparent;
  display: flex;
  flex-direction: column;
  text-decoration: none !important;
  color: inherit !important;
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
  transform: translateY(-3px);
  box-shadow: var(--shadow-lg);
  background: var(--bg-tertiary);
  text-decoration: none !important;
}

.ma-card:hover::before {
  opacity: 1;
}

.ma-card:active {
  transform: scale(0.98);
  transition-duration: var(--transition-fast);
}

/* Card accent colors */
.ma-card--about { border-top: 3px solid var(--about); }
.ma-card--analysen { border-top: 3px solid var(--analysen); }
.ma-card--teaching { border-top: 3px solid var(--teaching); }

.ma-card--about:hover { box-shadow: 0 12px 32px rgba(88, 86, 214, 0.1); }
.ma-card--analysen:hover { box-shadow: 0 12px 32px rgba(90, 200, 250, 0.1); }
.ma-card--teaching:hover { box-shadow: 0 12px 32px rgba(255, 149, 0, 0.1); }

/* ─── Card Icon ─── */
.ma-card-icon {
  width: 52px;
  height: 52px;
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  margin-bottom: var(--space-5);
  transition: transform var(--transition-spring);
}

.ma-card:hover .ma-card-icon {
  transform: scale(1.1) rotate(-5deg);
}

.ma-card--about .ma-card-icon { background: rgba(88, 86, 214, 0.12); }
.ma-card--analysen .ma-card-icon { background: rgba(90, 200, 250, 0.12); }
.ma-card--teaching .ma-card-icon { background: rgba(255, 149, 0, 0.12); }

.ma-card-icon svg {
  width: 24px;
  height: 24px;
  transition: fill var(--transition-fast);
}

.ma-card--about .ma-card-icon svg { fill: var(--about); }
.ma-card--analysen .ma-card-icon svg { fill: var(--analysen); }
.ma-card--teaching .ma-card-icon svg { fill: var(--teaching); }

/* ─── Card Content ─── */
.ma-card h2 {
  font-size: 22px;
  font-weight: 600;
  letter-spacing: -0.021em;
  line-height: 1.2;
  color: var(--text-primary);
  margin: 0 0 var(--space-3) 0;
}

.ma-card p {
  font-size: 15px;
  line-height: 1.5;
  color: var(--text-secondary);
  margin: 0 0 var(--space-6) 0;
  flex-grow: 1;
}

/* ─── Button ─── */
.ma-btn {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-3) var(--space-4);
  border-radius: var(--radius-md);
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
  transition: all var(--transition-fast);
  border: none;
  cursor: pointer;
  font-family: inherit;
  position: relative;
  z-index: 2;
  background: var(--system-indigo);
  color: white !important;
  margin-top: auto;
  align-self: flex-start;
}

.ma-btn:hover {
  background: #0051D5;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 122, 255, 0.3);
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

/* ─── Animations ─── */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.ma-card {
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) backwards;
}

.ma-card:nth-child(1) { animation-delay: 0.1s; }
.ma-card:nth-child(2) { animation-delay: 0.2s; }
.ma-card:nth-child(3) { animation-delay: 0.3s; }

/* ─── Reduced Motion ─── */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

/* ─── Touch ─── */
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

/* ─── Print ─── */
@media print {
  .ma-btn { display: none; }
  .ma-card { break-inside: avoid; }
}
</style>

<div class="ma-home">

  <!-- Hero -->
  <div class="ma-hero">
    <h1></h1>
    <p class="ma-hero-subtitle">Mathematik, Wirtschaft & Datenanalyse</p>
  </div>

  <!-- Cards -->
  <div class="ma-grid">

    <!-- Über mich -->
    <div class="ma-card ma-card--about">
      <div class="ma-card-icon">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM12 5C13.66 5 15 6.34 15 8C15 9.66 13.66 11 12 11C10.34 11 9 9.66 9 8C9 6.34 10.34 5 12 5ZM12 19.2C9.5 19.2 7.29 17.92 6 15.98C6.03 13.99 10 12.9 12 12.9C13.99 12.9 17.97 13.99 18 15.98C16.71 17.92 14.5 19.2 12 19.2Z"/>
        </svg>
      </div>
      <h2>Über mich</h2>
      <p>Hintergrund, Ausbildung und Schwerpunkte</p>
      <a href="/about/" class="ma-btn" onclick="event.stopPropagation()">Mehr erfahren <span class="ma-btn-arrow">→</span></a>
    </div>

    <!-- Analysen -->
    <div class="ma-card ma-card--analysen">
      <div class="ma-card-icon">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M19 3H5C3.9 3 3 3.9 3 5V19C3 20.1 3.9 21 5 21H19C20.1 21 21 20.1 21 19V5C21 3.9 20.1 3 19 3ZM9 17H7V10H9V17ZM13 17H11V7H13V17ZM17 17H15V13H17V17Z"/>
        </svg>
      </div>
      <h2>Analysen</h2>
      <p>Wirtschaftliche Betrachtungen und datengestützte Untersuchungen</p>
      <a href="/analysen/" class="ma-btn" onclick="event.stopPropagation()">Analysen lesen <span class="ma-btn-arrow">→</span></a>
    </div>

    <!-- Unterrichtsmaterialien -->
    <div class="ma-card ma-card--teaching">
      <div class="ma-card-icon">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M5 13.18V17.18L12 21L19 17.18V13.18L12 17L5 13.18ZM12 3L1 9L12 15L21 10.09V17H23V9L12 3Z"/>
        </svg>
      </div>
      <h2>Unterrichtsmaterialien</h2>
      <p>Mathematik, Volkswirtschaftslehre und Informatik</p>
      <a href="/teaching/" class="ma-btn" onclick="event.stopPropagation()">Materialien <span class="ma-btn-arrow">→</span></a>
    </div>

  </div>

</div>