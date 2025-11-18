---
layout: page
title: Projekte
permalink: /projekte/
---

Eine Auswahl meiner Programmier- und Datenanalyseprojekte.

<div class="post-list">
{% for projekt in site.projekte %}
  <article class="post-item">
    <h2><a href="{{ projekt.url | relative_url }}">{{ projekt.title }}</a></h2>
    {% if projekt.tags %}
    <p class="tags">
      {% for tag in projekt.tags %}
        <span class="tag">{{ tag }}</span>
      {% endfor %}
    </p>
    {% endif %}
    <p>{{ projekt.excerpt }}</p>
    <a href="{{ projekt.url | relative_url }}" class="read-more">Mehr erfahren →</a>
  </article>
{% endfor %}
</div>

{% if site.projekte.size == 0 %}
<p><em>Bald erscheinen hier die ersten Projekte...</em></p>
{% endif %}
