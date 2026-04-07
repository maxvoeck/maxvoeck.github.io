---
layout: page
title:
permalink: /termine/
---

<style>
body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }

.tr-container {
  max-width: 920px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
}

.tr-eyebrow {
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: 0.75rem;
}

.tr-title {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 2.75rem);
  font-weight: 300;
  letter-spacing: -0.03em;
  line-height: 1.15;
  color: var(--text-primary);
  margin-bottom: 0.75rem;
}

.tr-subtitle {
  font-size: 1rem;
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 2.5rem;
  max-width: 520px;
}

.tr-section {
  margin-bottom: 2.5rem;
}

.tr-section-label {
  font-size: 0.72rem;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: 1rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid var(--separator-strong);
}

.tr-row {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.9rem 0;
  border-bottom: 1px solid var(--separator);
}

.tr-row-left {
  flex: 1;
}

.tr-kurs {
  display: block;
  font-size: 1rem;
  font-weight: 500;
  color: var(--text-primary);
}

.tr-themen {
  display: block;
  font-size: 0.82rem;
  color: var(--text-tertiary);
  margin-top: 0.15rem;
}

.tr-datum {
  font-size: 0.9rem;
  color: var(--text-secondary);
  white-space: nowrap;
  margin-left: 1.5rem;
  font-variant-numeric: tabular-nums;
}

.tr-empty {
  padding: 2rem 0;
  font-size: 0.9rem;
  color: var(--text-tertiary);
  font-style: italic;
}

@media (max-width: 480px) {
  .tr-container { padding: 1.5rem 1.25rem 3rem; }
  .tr-row { flex-direction: column; gap: 0.25rem; }
  .tr-datum { margin-left: 0; font-size: 0.82rem; }
}
</style>

<div class="tr-container">

  <div class="tr-eyebrow">Studienkolleg Leipzig</div>
  <h1 class="tr-title">Termine</h1>
  <p class="tr-subtitle">Klausurtermine und organisatorische Hinweise für das laufende Semester.</p>

  <div class="tr-section">
    <div class="tr-section-label">Informatik</div>

    <div class="tr-row">
      <div class="tr-row-left">
        <span class="tr-kurs">25w-T3</span>
        <span class="tr-themen">Themen 1–3</span>
      </div>
      <span class="tr-datum">3. März 2026</span>
    </div>

    <div class="tr-row">
      <div class="tr-row-left">
        <span class="tr-kurs">25w-T1</span>
        <span class="tr-themen">Themen 4–6</span>
      </div>
      <span class="tr-datum">9. April 2026</span>
    </div>

    <div class="tr-row">
      <div class="tr-row-left">
        <span class="tr-kurs">25w-T4 & 25w-T2</span>
        <span class="tr-themen">Themen 1–3</span>
      </div>
      <span class="tr-datum">13. März 2026</span>
    </div>
  </div>

  <div class="tr-section">
    <div class="tr-section-label">Mathematik</div>
    <div class="tr-empty">Noch keine Termine eingetragen.</div>
  </div>

  <div class="tr-section">
    <div class="tr-section-label">Volkswirtschaftslehre</div>
    <div class="tr-empty">Noch keine Termine eingetragen.</div>
  </div>

</div>
