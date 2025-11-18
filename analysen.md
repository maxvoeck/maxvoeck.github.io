---
layout: page
title: Wirtschaftsanalysen
permalink: /analysen/
---

Hier veröffentliche ich Analysen zu wirtschaftlichen Themen, Marktentwicklungen und wirtschaftspolitischen Fragestellungen.

<div class="post-list">
{% for analyse in site.analysen %}
  <article class="post-item">
    <h2><a href="{{ analyse.url | relative_url }}">{{ analyse.title }}</a></h2>
    <p class="post-meta">{{ analyse.date | date: "%d. %B %Y" }}</p>
    <p>{{ analyse.excerpt }}</p>
    <a href="{{ analyse.url | relative_url }}" class="read-more">Weiterlesen →</a>
  </article>
{% endfor %}
</div>

{% if site.analysen.size == 0 %}
<p><em>Bald erscheinen hier die ersten Analysen...</em></p>
{% endif %}
