---
layout: page
title:
permalink: /teaching/
---

<style>
body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }

.te-container {
  max-width: 920px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
}

.te-eyebrow {
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: var(--s12);
}

.te-grid {
  display: flex;
  flex-direction: column;
  border-top: 1px solid var(--border-strong);
}

.te-card {
  display: block;
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--border);
  text-decoration: none;
  color: inherit;
  transition: padding-left 0.2s var(--ease-out);
}

.te-card:hover {
  padding-left: 0.75rem;
}

.te-card-label {
  display: block;
  font-family: var(--font-display);
  font-size: 24px;
  font-weight: 400;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  transition: color var(--t-fast);
}

.te-card:hover .te-card-label {
  color: var(--accent);
}

.te-card-meta {
  display: block;
  font-size: 13px;
  font-weight: 300;
  color: var(--text-tertiary);
  margin-top: 0.2rem;
}

@media (max-width: 480px) {
  .te-container { padding: 1.5rem 1.25rem 3rem; }
  .te-card-label { font-size: 20px; }
}
</style>

<div class="te-container">

  <div class="te-eyebrow">Materialien</div>

  <div class="te-grid">
    <a href="/teaching/mathematik/" class="te-card">
      <span class="te-card-label">Mathematik</span>
      <span class="te-card-meta">30 Module · Algebra, Vektoren, Analysis, Integralrechnung</span>
    </a>
    <a href="/teaching/vwl/" class="te-card">
      <span class="te-card-label">Volkswirtschaftslehre</span>
      <span class="te-card-meta">13 Module · Mikro- & Makroökonomie</span>
    </a>
    <a href="/teaching/informatik/" class="te-card">
      <span class="te-card-label">Informatik</span>
      <span class="te-card-meta">6 Module · Python</span>
    </a>
  </div>

</div>
