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
  max-width: 640px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
}

.te-eyebrow {
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: 0.75rem;
}

.te-title {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, "SF Pro Display", "Segoe UI", sans-serif; font-weight: 500;
  font-size: clamp(2rem, 5vw, 2.75rem);
  font-weight: 400;
  letter-spacing: -0.02em;
  line-height: 1.15;
  color: var(--text-primary);
  margin-bottom: 0.75rem;
}

.te-subtitle {
  font-size: 1rem;
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 2.5rem;
  max-width: 520px;
}

.te-grid {
  display: flex;
  flex-direction: column;
  border-top: 1px solid var(--separator-strong);
}

.te-card {
  display: block;
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--separator);
  text-decoration: none;
  color: inherit;
  transition: padding-left 0.2s ease;
}

.te-card:hover {
  padding-left: 0.5rem;
}

.te-card-label {
  display: block;
  font-size: 1.05rem;
  font-weight: 500;
  color: var(--text-primary);
  margin-bottom: 0.15rem;
  transition: color 0.15s ease;
}

.te-card:hover .te-card-label {
  color: var(--accent, #b85c38);
}

.te-card-meta {
  display: block;
  font-size: 0.8rem;
  color: var(--text-tertiary);
  margin-bottom: 0.4rem;
}

.te-card-desc {
  display: block;
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.6;
}

@media (max-width: 480px) {
  .te-container { padding: 1.5rem 1.25rem 3rem; }
}
</style>

<div class="te-container">

  <div class="te-eyebrow">Studienkolleg Leipzig</div>
  <h1 class="te-title">Lehrmaterialien</h1>
  <p class="te-subtitle">Ausgewählte Materialien aus meiner Lehrtätigkeit, abgestimmt auf die Anforderungen der Feststellungsprüfung.</p>

  <div class="te-grid">
    <a href="/teaching/mathematik/" class="te-card">
      <span class="te-card-label">Mathematik</span>
      <span class="te-card-meta">28 Module · 5 interaktive Tools</span>
      <span class="te-card-desc">Analysis und Lineare Algebra – von Vektorrechnung und Matrizen bis zu Kurvendiskussion und Rotationsvolumen</span>
    </a>
    <a href="/teaching/vwl/" class="te-card">
      <span class="te-card-label">Volkswirtschaftslehre</span>
      <span class="te-card-meta">13 Module · Mikro & Makro</span>
      <span class="te-card-desc">Makro- und Mikroökonomie mit praxisnahen Beispielen – von Bedürfnissen und Marktgleichgewicht bis zur Arbeitsmarktpolitik</span>
    </a>
    <a href="/teaching/informatik/" class="te-card">
      <span class="te-card-label">Informatik</span>
      <span class="te-card-meta">5 Module · Python</span>
      <span class="te-card-desc">Grundlagen der Programmierung und algorithmisches Denken – von print() über Kontrollstrukturen bis zu eigenen Funktionen</span>
    </a>
  </div>

</div>
