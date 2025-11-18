---
layout: page
title: Informatik
permalink: /teaching/informatik/
---

Materialien zur Informatik für die Prüfungsvorbereitung am Studienkolleg.

## Programmierung

<div class="post-list">
{% assign prog = site.teaching | where: "category", "programmierung" %}
{% for material in prog %}
  <article class="post-item">
    <h3><a href="{{ material.url | relative_url }}">{{ material.title }}</a></h3>
    <p>{{ material.excerpt }}</p>
    {% if material.pdf %}
    <a href="{{ material.pdf }}" class="btn">PDF herunterladen</a>
    {% endif %}
  </article>
{% endfor %}
{% if prog.size == 0 %}
<p><em>Materialien werden in Kürze hinzugefügt...</em></p>
{% endif %}
</div>

## Algorithmen und Datenstrukturen

<div class="post-list">
{% assign algo = site.teaching | where: "category", "algorithmen" %}
{% for material in algo %}
  <article class="post-item">
    <h3><a href="{{ material.url | relative_url }}">{{ material.title }}</a></h3>
    <p>{{ material.excerpt }}</p>
    {% if material.pdf %}
    <a href="{{ material.pdf }}" class="btn">PDF herunterladen</a>
    {% endif %}
  </article>
{% endfor %}
{% if algo.size == 0 %}
<p><em>Materialien werden in Kürze hinzugefügt...</em></p>
{% endif %}
</div>

<p style="margin-top: 3rem;"><a href="/teaching/">← Zurück zur Übersicht</a></p>
