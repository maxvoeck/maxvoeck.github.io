---
layout: page
title: Volkswirtschaftslehre
permalink: /teaching/vwl/
---

Materialien zur Volkswirtschaftslehre für die Prüfungsvorbereitung am Studienkolleg.

## Mikroökonomie

<div class="post-list">
{% assign mikro = site.teaching | where: "category", "mikrooekonomie" %}
{% for material in mikro %}
  <article class="post-item">
    <h3><a href="{{ material.url | relative_url }}">{{ material.title }}</a></h3>
    <p>{{ material.excerpt }}</p>
    {% if material.pdf %}
    <a href="{{ material.pdf }}" class="btn">PDF herunterladen</a>
    {% endif %}
  </article>
{% endfor %}
{% if mikro.size == 0 %}
<p><em>Materialien werden in Kürze hinzugefügt...</em></p>
{% endif %}
</div>

## Makroökonomie

<div class="post-list">
{% assign makro = site.teaching | where: "category", "makrooekonomie" %}
{% for material in makro %}
  <article class="post-item">
    <h3><a href="{{ material.url | relative_url }}">{{ material.title }}</a></h3>
    <p>{{ material.excerpt }}</p>
    {% if material.pdf %}
    <a href="{{ material.pdf }}" class="btn">PDF herunterladen</a>
    {% endif %}
  </article>
{% endfor %}
{% if makro.size == 0 %}
<p><em>Materialien werden in Kürze hinzugefügt...</em></p>
{% endif %}
</div>

<p style="margin-top: 3rem;"><a href="/teaching/">← Zurück zur Übersicht</a></p>
