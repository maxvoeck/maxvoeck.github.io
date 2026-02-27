---
layout: page
title:
permalink: /about/
---

<style>
body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }

.ab-content {
  max-width: 640px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
}

.ab-eyebrow {
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: 0.75rem;
}

.ab-name {
  font-family: 'Instrument Serif', Georgia, serif;
  font-size: clamp(2rem, 5vw, 2.75rem);
  font-weight: 400;
  letter-spacing: -0.02em;
  line-height: 1.15;
  color: var(--text-primary);
  margin-bottom: 1rem;
}

.ab-intro {
  font-size: 1rem;
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 3rem;
}

.ab-section {
  margin-bottom: 2.5rem;
}

.ab-section-title {
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid var(--separator);
}

.ab-edu-item {
  margin-bottom: 1rem;
}
.ab-edu-item:last-child { margin-bottom: 0; }

.ab-edu-title {
  display: block;
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--text-primary);
}

.ab-edu-place {
  font-size: 0.85rem;
  color: var(--text-tertiary);
}

.ab-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.ab-list li {
  font-size: 0.95rem;
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 0.5rem;
  padding-left: 1.2rem;
  position: relative;
}
.ab-list li:last-child { margin-bottom: 0; }

.ab-list li::before {
  content: '–';
  position: absolute;
  left: 0;
  color: var(--text-tertiary);
}

@media (max-width: 480px) {
  .ab-content { padding: 1.5rem 1.25rem 3rem; }
}
</style>

<div class="ab-content">

  <div class="ab-eyebrow">Über mich</div>
  <h1 class="ab-name">Maximilian Vöcklinghaus</h1>
  <p class="ab-intro">Dozent am Studienkolleg der Rahn Education in Leipzig. Ich begleite internationale Studierende auf ihrem Weg ins deutsche Hochschulstudium und unterrichte Mathematik, Informatik und Volkswirtschaftslehre.</p>

  <div class="ab-section">
    <h2 class="ab-section-title">Ausbildung</h2>
    <div class="ab-edu-item">
      <span class="ab-edu-title">Bachelor in Mathematik</span>
      <span class="ab-edu-place">Heinrich-Heine-Universität Düsseldorf</span>
    </div>
    <div class="ab-edu-item">
      <span class="ab-edu-title">Data Science Master</span>
      <span class="ab-edu-place">RWTH Aachen</span>
    </div>
  </div>

  <div class="ab-section">
    <h2 class="ab-section-title">Schwerpunkte</h2>
    <ul class="ab-list">
      <li>Mathematik & Data Science – Von Analysis und linearer Algebra bis zu praktischer Datenanalyse</li>
      <li>Wirtschaftswissenschaften – Volkswirtschaftslehre, Marktanalysen, kritische Wirtschaftstheorie</li>
      <li>Didaktik & Bildung – Entwicklung interaktiver Lernmaterialien und digitaler Bildungsressourcen</li>
    </ul>
  </div>

  <div class="ab-section">
    <h2 class="ab-section-title">Interessen</h2>
    <ul class="ab-list">
      <li>Kritische Theorie und Kulturanalyse</li>
      <li>Wirtschaftsphilosophie</li>
      <li>Schnittstelle zwischen quantitativen Methoden und gesellschaftlicher Analyse</li>
    </ul>
  </div>

</div>
