---
layout: page
title: 
permalink: /teaching/bwl/
---

{%- assign kurs = site.data.kurse.bwl -%}
{%- assign modulzahl = 0 -%}
{%- for k in kurs.kapitel -%}{%- assign modulzahl = modulzahl | plus: k.module.size -%}{%- endfor -%}

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

{% include kurs/styles.html %}

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung · W-Kurs</div>
      <h1>Betriebswirtschaftslehre</h1>
      <p class="mw-hero-sub">Module, Skripte und Übungen für den W-Kurs — von den Grundlagen der Allgemeinen BWL über Buchführung bis zu Erfolg, Steuern und Abschreibungen. Die Inhalte werden nach und nach ergänzt.</p>
    </div>
    <div class="mw-progress">
      <svg class="mw-ring" viewBox="0 0 120 120">
        <circle class="bg" cx="60" cy="60" r="52"/>
        <circle class="fg" cx="60" cy="60" r="52" id="ringFg"/>
        <text class="mw-ring-label" x="60" y="60" text-anchor="middle" dominant-baseline="central" id="ringLabel">0</text>
      </svg>
      <div class="mw-ring-caption">von <span id="ringTotal">{{ modulzahl }}</span> Modulen</div>
    </div>
  </header>

  <!-- Wochenplan -->
  <section class="mw-plan">
    <div class="mw-plan-kopf">
      <div>
        <h3>Wochenplan</h3>
        <p>17.08.–27.11.2026 · 14 Unterrichtswochen · zwei Blöcke BWL pro Woche · Klausuren gemeinsam mit VWL: 22.09. · 23.10. · 19.11.</p>
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
    <div>Materialien folgen Block für Block — hier lohnt sich regelmäßiges Vorbeischauen.</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

{% include kurs/player.html kurs=kurs %}
</div>

{% include kurs/script.html kurs=kurs %}
