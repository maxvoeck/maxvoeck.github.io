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
  max-width: 920px;
  margin: 0 auto;
  padding: 2rem 1.5rem 4rem;
}

.ab-eyebrow {
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: var(--s8);
}

.ab-title {
  font-family: var(--font-display);
  font-size: clamp(2rem, 5vw, 2.75rem);
  font-weight: 300;
  letter-spacing: -0.02em;
  line-height: 1.15;
  color: var(--text-primary);
  margin-bottom: var(--s4);
}

.ab-lead {
  font-size: 15px;
  font-weight: 300;
  color: var(--text-secondary);
  line-height: 1.8;
  max-width: 600px;
  margin-bottom: var(--s16);
}

.ab-section {
  margin-bottom: var(--s12);
  animation: breatheIn 0.8s var(--ease-out) backwards;
}
.ab-section:nth-child(2) { animation-delay: 0.05s; }
.ab-section:nth-child(3) { animation-delay: 0.1s; }
.ab-section:nth-child(4) { animation-delay: 0.15s; }
.ab-section:nth-child(5) { animation-delay: 0.2s; }

.ab-section-title {
  font-family: var(--font-display);
  font-size: 24px;
  font-weight: 400;
  letter-spacing: -0.01em;
  line-height: 1.2;
  color: var(--text-primary);
  margin-bottom: var(--s6);
  padding-bottom: var(--s4);
  border-bottom: 1px solid var(--border);
}

.ab-text {
  font-size: 15px;
  font-weight: 300;
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: var(--s4);
}

.ab-text:last-child { margin-bottom: 0; }

.ab-highlight {
  color: var(--text-primary);
  font-weight: 400;
}

.ab-grid {
  display: grid;
  gap: var(--s4);
}

@media (min-width: 600px) {
  .ab-grid { grid-template-columns: repeat(2, 1fr); gap: var(--s5); }
}

.ab-card {
  background: var(--bg-elevated);
  border: 1px solid var(--border);
  border-radius: var(--r-md);
  padding: var(--s5) var(--s6);
  transition: border-color var(--t-fast), box-shadow var(--t-fast);
}

.ab-card:hover {
  border-color: var(--border-strong);
  box-shadow: var(--shadow-sm);
}

.ab-card-label {
  display: block;
  font-family: var(--font-body);
  font-size: 12px;
  font-weight: 500;
  color: var(--text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.08em;
  margin-bottom: var(--s2);
}

.ab-card-value {
  display: block;
  font-size: 15px;
  font-weight: 400;
  color: var(--text-primary);
  line-height: 1.5;
}

.ab-card-note {
  display: block;
  font-size: 13px;
  color: var(--text-tertiary);
  margin-top: var(--s1);
}

.ab-time-grid {
  display: grid;
  gap: var(--s3);
}

.ab-time-row {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: var(--s3) 0;
  border-bottom: 1px solid var(--border);
}

.ab-time-fach {
  font-size: 15px;
  font-weight: 400;
  color: var(--text-primary);
}

.ab-time-stunden {
  font-family: var(--font-mono);
  font-size: 13px;
  color: var(--text-tertiary);
  white-space: nowrap;
}

.ab-cta {
  margin-top: var(--s12);
  padding-top: var(--s8);
  border-top: 1px solid var(--border);
}

.ab-cta-text {
  font-size: 14px;
  color: var(--text-secondary);
  font-weight: 300;
  line-height: 1.7;
}

.ab-cta-text a {
  color: var(--accent);
  text-decoration: none;
  border-bottom: 1px solid var(--border);
  transition: border-color var(--t-fast);
}

.ab-cta-text a:hover {
  border-color: var(--accent);
}

@media (max-width: 480px) {
  .ab-content { padding: 1.5rem 1.25rem 3rem; }
  .ab-grid { grid-template-columns: 1fr; }
  .ab-time-row { flex-direction: column; gap: 2px; }
}
</style>

<div class="ab-content">

  <div class="ab-eyebrow">Studienkolleg Leipzig · Rahn Education</div>
  <h1 class="ab-title">Hinweise zum Studium</h1>
  <p class="ab-lead">Das Studienkolleg ist die Brücke zwischen eurer bisherigen Ausbildung und dem deutschen Hochschulstudium. Diese Seite erklärt, wie ihr die Materialien hier nutzen könnt und was von euch erwartet wird.</p>

  <div class="ab-section">
    <h2 class="ab-section-title">Was ist das Studienkolleg?</h2>
    <p class="ab-text">Ihr seid hier, weil euer Schulabschluss in Deutschland nicht direkt zum Studium berechtigt. Das Studienkolleg bereitet euch auf die <span class="ab-highlight">Feststellungsprüfung (FSP)</span> vor – die zentrale Prüfung, die euch den Zugang zur Universität ermöglicht.</p>
    <p class="ab-text">Das bedeutet: Ihr steht an der Schwelle zur Universität. Der Anspruch ist höher als in der Schule, und von euch wird erwartet, dass ihr zunehmend <span class="ab-highlight">eigenständig</span> arbeitet – genau wie im späteren Studium.</p>
  </div>

  <div class="ab-section">
    <h2 class="ab-section-title">Wie ihr diese Seite nutzen sollt</h2>
    <p class="ab-text">Alle Materialien, die ihr für meine Kurse braucht, findet ihr unter <a href="/teaching/">Materialien</a>. Dort gibt es für jedes Fach:</p>
    <div class="ab-grid">
      <div class="ab-card">
        <span class="ab-card-label">Skripte & PDFs</span>
        <span class="ab-card-value">Jedes Thema als einzelnes PDF zum Nachlesen und Üben</span>
      </div>
      <div class="ab-card">
        <span class="ab-card-label">Quizzes</span>
        <span class="ab-card-value">Kurze Selbsttests zu den meisten Kapiteln</span>
      </div>
      <div class="ab-card">
        <span class="ab-card-label">Interaktive Tools</span>
        <span class="ab-card-value">Visualisierungen und Rechner zum Experimentieren</span>
      </div>
      <div class="ab-card">
        <span class="ab-card-label">Fortschrittstracking</span>
        <span class="ab-card-value">Haken setzen bei abgeschlossenen Modulen</span>
      </div>
    </div>
    <p class="ab-text" style="margin-top: var(--s6);">Die Idee: Ihr bekommt <span class="ab-highlight">alles</span>, was ihr braucht, um euch selbst zu organisieren. Nutzt die Materialien vor und nach dem Unterricht. Wer regelmäßig mitarbeitet, wird bei der Prüfung keine Überraschungen erleben.</p>
  </div>

  <div class="ab-section">
    <h2 class="ab-section-title">Wie viel muss ich lernen?</h2>
    <p class="ab-text">Eine ehrliche Antwort: Das Studienkolleg ist ein <span class="ab-highlight">Vollzeitstudium</span>. Neben dem Unterricht solltet ihr pro Fach zusätzliche Stunden einplanen:</p>
    <div class="ab-time-grid">
      <div class="ab-time-row">
        <span class="ab-time-fach">Mathematik</span>
        <span class="ab-time-stunden">4–6 Std / Woche Selbststudium</span>
      </div>
      <div class="ab-time-row">
        <span class="ab-time-fach">Informatik</span>
        <span class="ab-time-stunden">2–3 Std / Woche Selbststudium</span>
      </div>
      <div class="ab-time-row">
        <span class="ab-time-fach">VWL</span>
        <span class="ab-time-stunden">3–4 Std / Woche Selbststudium</span>
      </div>
    </div>
    <p class="ab-text" style="margin-top: var(--s6);">Das sind Richtwerte. Manche brauchen mehr, manche weniger. Entscheidend ist nicht die Stundenanzahl, sondern die <span class="ab-highlight">Regelmäßigkeit</span>. Jeden Tag 45 Minuten bringt mehr als einmal pro Woche 5 Stunden.</p>
  </div>

  <div class="ab-section">
    <h2 class="ab-section-title">Wie der Unterricht funktioniert</h2>
    <p class="ab-text">Im Unterricht erarbeiten wir die Konzepte gemeinsam. Ich erkläre, ihr fragt. Aber das reicht nicht – die eigentliche Arbeit passiert danach: Nachlesen, Üben, Wiederholen.</p>
    <p class="ab-text">Was ich von euch erwarte:</p>
    <div class="ab-grid">
      <div class="ab-card">
        <span class="ab-card-label">Vor dem Unterricht</span>
        <span class="ab-card-value">Lest das Skript zum aktuellen Thema</span>
        <span class="ab-card-note">Ihr müsst es nicht vollständig verstehen – aber ihr wisst, worum es geht</span>
      </div>
      <div class="ab-card">
        <span class="ab-card-label">Nach dem Unterricht</span>
        <span class="ab-card-value">Bearbeitet die Übungsaufgaben und macht die Quizzes</span>
        <span class="ab-card-note">Das ist kein Extra, das ist der Kern des Lernens</span>
      </div>
    </div>
  </div>

  <div class="ab-cta">
    <p class="ab-cta-text">Fragen? Schreibt mir eine <a href="mailto:{{ site.email }}">E-Mail</a> oder sprecht mich nach dem Unterricht an. Klausurtermine und organisatorische Infos findet ihr unter <a href="/termine/">Termine</a>.</p>
  </div>

</div>
