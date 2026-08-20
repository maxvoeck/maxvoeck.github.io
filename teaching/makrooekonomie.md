---
layout: page
title: 
permalink: /teaching/makrooekonomie/
---

{%- assign kurs = site.data.kurse.makrooekonomie -%}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

{% include kurs/styles.html %}

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung · 2. Semester</div>
      <h1>Makroökonomie</h1>
      <p class="mw-hero-sub">Der zweite Teil der Volkswirtschaftslehre — von der Volkswirtschaftlichen Gesamtrechnung über Konjunktur und Arbeitsmarkt bis zu Inflation und magischem Viereck. Zu jedem Modul der Foliensatz, zu den meisten ein Quiz zum Üben.</p>
    </div>
    {% include kurs/ring.html kurs=kurs %}
  </header>

  {% include kurs/liste.html kurs=kurs %}

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div>Die Grundlagen dazu stehen in der Mikroökonomie aus dem 1. Semester.</div>
    <div class="mw-fuss-links">
      <a href="/teaching/mikrooekonomie/" class="mw-btn">← Mikroökonomie</a>
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

{% include kurs/player.html kurs=kurs %}
</div>

{% include kurs/script.html kurs=kurs %}
