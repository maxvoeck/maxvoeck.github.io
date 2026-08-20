---
layout: page
title: 
permalink: /teaching/mathematik-w/
---

{%- comment -%} Klammer-Syntax nötig: der Bindestrich im Namen wäre in Punktnotation eine Subtraktion. {%- endcomment -%}
{%- assign kurs = site.data.kurse["mathematik-w"] -%}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

{% include kurs/styles.html %}

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung · W-Kurs</div>
      <h1>Mathematik,<br><em>2. Semester.</em></h1>
      <p class="mw-hero-sub">Module, Skripte und Übungen für den W-Kurs im zweiten Semester. Die Inhalte werden nach und nach ergänzt.</p>
    </div>
    <div class="mw-status">In Vorbereitung</div>
  </header>

  {% include kurs/liste.html kurs=kurs %}

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div>Materialien folgen Kapitel für Kapitel — hier lohnt sich regelmäßiges Vorbeischauen.</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

{% include kurs/player.html kurs=kurs %}
</div>

{% include kurs/script.html kurs=kurs %}
