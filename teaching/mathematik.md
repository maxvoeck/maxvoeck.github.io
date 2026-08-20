---
layout: page
title: 
permalink: /teaching/mathematik/
---

{%- assign kurs = site.data.kurse.mathematik -%}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

{% include kurs/styles.html %}

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung · 1. Semester</div>
      <h1>Mathematik,<br><em>Satz für Satz.</em></h1>
      <p class="mw-hero-sub">26 Module in vier Kapiteln plus fünf interaktive Tools — zu jedem Modul der Foliensatz, zu den meisten ein Quiz zum Üben.</p>
    </div>
    {% include kurs/ring.html kurs=kurs %}
  </header>

  <!-- Gesamtskript -->
  <div class="mw-feature">
    <div class="mw-feature-titel">
      <h3>Das Gesamtskript</h3>
      <p>Alle Module in einem Dokument — zum durchgehenden Lernen oder als Nachschlagewerk vor der FSP.</p>
    </div>
    <a href="/assets/pdfs/Mathematik_Skript.pdf" class="mw-btn">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 3v12m0 0l-4-4m4 4l4-4M4 21h16"/></svg>
      Skript öffnen · 1,1 MB
    </a>
  </div>

  {% include kurs/liste.html kurs=kurs %}

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div><strong style="color:var(--elfenbein)">26 Module</strong> · Lineare Algebra, Vektorrechnung, Differentialrechnung, Integralrechnung &amp; interaktive Tools</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

{% include kurs/player.html kurs=kurs %}
</div>

{% include kurs/script.html kurs=kurs %}
