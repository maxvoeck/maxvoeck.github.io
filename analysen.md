---
layout: page
title:
permalink: /analysen/
---

<!-- AMBIENT -->
<div class="an-ambient">
  <div class="an-ambient-orb"></div>
  <div class="an-ambient-orb"></div>
  <div class="an-ambient-orb"></div>
</div>

<div class="an-content">

  <!-- HERO -->
  <div class="an-hero">
    <div class="an-hero-eyebrow">Wirtschaftsanalysen</div>
    <h1>Analysen</h1>
    <p class="an-hero-sub">Analysen zu wirtschaftlichen Themen, Marktentwicklungen und wirtschaftspolitischen Fragestellungen.</p>
  </div>

  <!-- POST LIST -->
  <div class="an-list">
    {% for analyse in site.analysen %}
    <article class="an-post">
      <p class="an-post-date">{{ analyse.date | date: "%d. %B %Y" }}</p>
      <h2><a href="{{ analyse.url | relative_url }}">{{ analyse.title }}</a></h2>
      <p class="an-post-excerpt">{{ analyse.excerpt | strip_html | truncatewords: 40 }}</p>
      <a href="{{ analyse.url | relative_url }}" class="an-btn"><span>Weiterlesen</span><span class="an-btn-arrow">→</span></a>
    </article>
    {% endfor %}
  </div>

  {% if site.analysen.size == 0 %}
  <div class="an-empty">
    <p>Bald erscheinen hier die ersten Analysen...</p>
  </div>
  {% endif %}

</div>
