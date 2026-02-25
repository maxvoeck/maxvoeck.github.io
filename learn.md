---
layout: page
title:
permalink: /learn/
---

<style>
:root {
  --system-indigo: #5856D6;
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;

  --bg-primary: #262624;
  --bg-secondary: #30302e;
  --bg-tertiary: #3a3a37;
  --text-primary: #c1c0b6;
  --text-secondary: #908f87;
  --text-tertiary: #706f69;
  --separator: rgba(var(--text-rgb), 0.08);
  --separator-strong: rgba(var(--text-rgb), 0.15);

  --shadow-md: 0 4px 12px rgba(var(--text-rgb),0.08);
  --shadow-lg: 0 12px 24px rgba(var(--text-rgb),0.12);

  --font-stack: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", "Helvetica Neue", Helvetica, Arial, sans-serif;

  --space-1: 4px; --space-2: 8px; --space-3: 12px; --space-4: 16px;
  --space-5: 20px; --space-6: 24px; --space-8: 32px; --space-10: 40px;
  --space-12: 48px; --space-16: 64px;

  --radius-md: 12px; --radius-lg: 16px; --radius-xl: 20px; --radius-2xl: 24px;
  --radius-full: 9999px;

  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
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
.ln-container {
  max-width: 780px;
  margin: 0 auto;
  padding: var(--space-16) var(--space-5);
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

/* ─── Badge ─── */
.ln-badge {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-2) var(--space-4);
  background: rgba(88, 86, 214, 0.12);
  border: 1px solid rgba(88, 86, 214, 0.3);
  border-radius: var(--radius-full);
  font-size: 13px;
  font-weight: 600;
  color: var(--system-indigo);
  letter-spacing: 0.04em;
  text-transform: uppercase;
  margin-bottom: var(--space-8);
  animation: fadeInUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) backwards;
}

.ln-badge-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--system-indigo);
  animation: pulse 2s ease-in-out infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50%       { opacity: 0.4; transform: scale(0.8); }
}

/* ─── Hero ─── */
.ln-title {
  font-size: clamp(48px, 8vw, 80px);
  font-weight: 700;
  letter-spacing: -0.025em;
  line-height: 1.05;
  margin-bottom: var(--space-6);
  background: linear-gradient(135deg, var(--text-primary) 40%, var(--text-tertiary) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: fadeInUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.05s backwards;
}

.ln-subtitle {
  font-size: 19px;
  font-weight: 400;
  color: var(--text-tertiary);
  max-width: 520px;
  line-height: 1.55;
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.1s backwards;
}

/* ─── Preview Cards ─── */
.ln-preview {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--space-4);
  width: 100%;
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.15s backwards;
}

.ln-preview-card {
  background: var(--bg-secondary);
  border: 1px solid var(--separator);
  border-radius: var(--radius-xl);
  padding: var(--space-6) var(--space-5);
  display: flex;
  flex-direction: column;
  gap: var(--space-3);
  opacity: 0.5;
  transition: opacity var(--transition-base);
}

.ln-preview-card:hover {
  opacity: 0.7;
}

.ln-preview-icon {
  font-size: 28px;
  line-height: 1;
}

.ln-preview-label {
  font-size: 15px;
  font-weight: 600;
  color: var(--text-primary);
  letter-spacing: -0.01em;
}

.ln-preview-count {
  font-size: 12px;
  color: var(--text-tertiary);
}

.ln-preview-card--math  { border-top: 2px solid rgba(255, 45, 85, 0.4); }
.ln-preview-card--econ  { border-top: 2px solid rgba(255, 149, 0, 0.4); }
.ln-preview-card--cs    { border-top: 2px solid rgba(0, 122, 255, 0.4); }

/* ─── Coming Soon Box ─── */
.ln-soon {
  background: var(--bg-secondary);
  border: 1px solid var(--separator);
  border-radius: var(--radius-2xl);
  padding: var(--space-10) var(--space-8);
  max-width: 480px;
  width: 100%;
  animation: fadeInUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) 0.2s backwards;
}

.ln-soon-icon {
  font-size: 40px;
  margin-bottom: var(--space-4);
}

.ln-soon-title {
  font-size: 22px;
  font-weight: 600;
  letter-spacing: -0.02em;
  color: var(--text-primary);
  margin-bottom: var(--space-3);
}

.ln-soon-text {
  font-size: 15px;
  color: var(--text-tertiary);
  line-height: 1.6;
}

/* ─── Animations ─── */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(16px); }
  to   { opacity: 1; transform: translateY(0); }
}

@media (max-width: 600px) {
  .ln-container { padding: var(--space-8) var(--space-4); }
  .ln-hero-title { font-size: 36px; }
  .ln-hero-sub { font-size: 15px; }
  .ln-preview { grid-template-columns: 1fr; gap: var(--space-3); }
  .ln-preview-card { padding: var(--space-4); }
  .ln-soon { padding: var(--space-8) var(--space-5); }
  .ln-soon-title { font-size: 20px; }
}

@media (prefers-reduced-motion: reduce) {
  * { animation-duration: 0.01ms !important; }
}
</style>

<div class="ln-container">

  <div class="ln-badge">
    <span class="ln-badge-dot"></span>
  </div>

  <h1 class="ln-title">Learn</h1>
  <p class="ln-subtitle">Mathematik, VWL und Informatik – direkt im Browser, kapitelweise erklärt. Kein Download, kein PDF.</p>

  <div class="ln-preview">
    <a href="/learn/mathematik/" class="ln-preview-card ln-preview-card--math" style="text-decoration:none;color:inherit;opacity:1;cursor:pointer;transition:all 250ms cubic-bezier(0.4,0,0.2,1);" onmouseover="this.style.transform='translateY(-3px)';this.style.borderColor='rgba(255,45,85,0.4)'" onmouseout="this.style.transform='';this.style.borderColor=''">
      <div class="ln-preview-icon">📐</div>
      <div class="ln-preview-label">Mathematik</div>
      <div class="ln-preview-count" style="color:#34C759;font-weight:500;">5 Kapitel verfügbar →</div>
    </a>
    <a href="/learn/vwl/" class="ln-preview-card ln-preview-card--econ" style="text-decoration:none;color:inherit;opacity:1;cursor:pointer;transition:all 250ms cubic-bezier(0.4,0,0.2,1);" onmouseover="this.style.transform='translateY(-3px)';this.style.borderColor='rgba(255,149,0,0.4)'" onmouseout="this.style.transform='';this.style.borderColor=''">
      <div class="ln-preview-icon">📊</div>
      <div class="ln-preview-label">VWL</div>
      <div class="ln-preview-count" style="color:#34C759;font-weight:500;">4 Kapitel verfügbar →</div>
    </a>
    <div class="ln-preview-card ln-preview-card--cs">
      <div class="ln-preview-icon">🐍</div>
      <div class="ln-preview-label">Informatik</div>
      <div class="ln-preview-count">Demnächst</div>
    </div>
  </div>

  

</div>
