---
layout: page
title: 
permalink: /teaching/mikrooekonomie/
---

{%- assign kurs = site.data.kurse.mikrooekonomie -%}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

{% include kurs/styles.html %}

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung · 1. Semester</div>
      <h1>Mikroökonomie</h1>
      <p class="mw-hero-sub">Der erste Teil der Volkswirtschaftslehre — von Bedürfnis und Nachfrage über Angebot, Marktgleichgewicht und Marktformen bis zur Budgetgerade. Zu jedem Modul der Foliensatz, zu den meisten ein Quiz zum Üben.</p>
    </div>
    {% include kurs/ring.html kurs=kurs %}
  </header>

  <!-- Wochenplan -->
  <section class="mw-plan">
    <div class="mw-plan-kopf">
      <div>
        <h3>Wochenplan</h3>
        <p>17.08.–27.11.2026 · 14 Unterrichtswochen · ein Termin VWL pro Woche · Klausuren gemeinsam mit BWL: 22.09. · 20.10. · 17.11.</p>
      </div>
      <a href="/assets/pdfs/Wochenplan_BWL_VWL_W.pdf" class="mw-btn" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6"/></svg>
        Wochenplan als PDF
      </a>
    </div>
  </section>

  {% include kurs/liste.html kurs=kurs %}

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div>Der zweite Teil der Volkswirtschaftslehre folgt im 2. Semester.</div>
    <div class="mw-fuss-links">
      <a href="/teaching/makrooekonomie/" class="mw-btn">Makroökonomie →</a>
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

{% include kurs/player.html kurs=kurs %}
</div>

{% include kurs/script.html kurs=kurs %}
