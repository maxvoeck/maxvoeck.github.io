---
layout: page
title:
permalink: /learn/
---

<style>
body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }

.ln-container {
  max-width: 920px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
}

.ln-eyebrow {
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: 0.75rem;
}

.ln-title {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 2.75rem);
  font-weight: 300;
  letter-spacing: -0.02em;
  line-height: 1.15;
  color: var(--text-primary);
  margin-bottom: 0.75rem;
}

.ln-subtitle {
  font-size: 1rem;
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 2.5rem;
  max-width: 480px;
}

.ln-grid {
  display: flex;
  flex-direction: column;
  border-top: 1px solid var(--separator-strong);
}

.ln-card {
  display: block;
  padding: 1.25rem 0;
  border-bottom: 1px solid var(--separator);
  text-decoration: none;
  color: inherit;
  transition: padding-left 0.2s ease;
}

.ln-card:hover {
  padding-left: 0.5rem;
}

.ln-card-head {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 1rem;
}

.ln-card-label {
  font-size: 1.05rem;
  font-weight: 500;
  color: var(--text-primary);
  transition: color 0.15s ease;
}

.ln-card:hover .ln-card-label {
  color: var(--accent, #b85c38);
}

.ln-card-status {
  font-size: 0.78rem;
  color: var(--text-tertiary);
  white-space: nowrap;
}

.ln-card-status--active {
  color: var(--success, #34d399);
}

.ln-card--disabled {
  opacity: 0.45;
}

.ln-card--disabled .ln-card-label {
  color: var(--text-tertiary);
}

@media (max-width: 480px) {
  .ln-container { padding: 1.5rem 1.25rem 3rem; }
}
</style>

<div class="ln-container">

  <div class="ln-eyebrow">Interaktiv</div>
  <h1 class="ln-title">Learn</h1>
  <p class="ln-subtitle">Mathematik, VWL und Informatik – direkt im Browser, kapitelweise erklärt.</p>

  <nav class="ln-grid">
    <a href="/learn/mathematik/" class="ln-card">
      <div class="ln-card-head">
        <span class="ln-card-label">Mathematik</span>
        <span class="ln-card-status ln-card-status--active">5 Kapitel</span>
      </div>
    </a>
    <a href="/learn/vwl/" class="ln-card">
      <div class="ln-card-head">
        <span class="ln-card-label">Volkswirtschaftslehre</span>
        <span class="ln-card-status ln-card-status--active">4 Kapitel</span>
      </div>
    </a>
    <div class="ln-card ln-card--disabled">
      <div class="ln-card-head">
        <span class="ln-card-label">Informatik</span>
        <span class="ln-card-status">Demnächst</span>
      </div>
    </div>
  </nav>

</div>
