---
layout: page
title: 
permalink: /teaching/informatik/
---

{%- assign kurs = site.data.kurse.informatik -%}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

{% include kurs/styles.html %}

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung</div>
      <h1>Informatik</h1>
      <p class="mw-hero-sub">Python-Grundlagen, Datenstrukturen und angewandte Programmierung — zu jedem Modul der Foliensatz, zu den meisten ein Quiz zum Üben.</p>
    </div>
    {% include kurs/ring.html kurs=kurs %}
  </header>

  {% include kurs/liste.html kurs=kurs %}

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div><strong style="color:var(--elfenbein)">7 Module</strong> · Python</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

{% include kurs/player.html kurs=kurs %}
</div>

{% include kurs/script.html kurs=kurs %}
