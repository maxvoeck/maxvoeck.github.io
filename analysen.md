---
layout: page
title: Wirtschaftsanalysen
permalink: /analysen/
---

<style>
body {
  background: #f5f5f4;
}

.intro-text {
  font-size: 1rem;
  color: #666;
  margin-bottom: 2.5rem;
  line-height: 1.7;
  font-weight: 300;
}

.post-list {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  margin: 2.5rem 0;
}

.post-item {
  background: #fafaf9;
  border-radius: 8px;
  padding: 2rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
}

.post-item::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background: #1a1a1a;
  transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.post-item:hover {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  transform: translateY(-2px);
}

.post-item:hover::after {
  width: 100%;
}

.post-item h2 {
  margin: 0 0 0.5rem 0;
  font-size: 1.25rem;
  font-weight: 500;
  letter-spacing: 0.02em;
}

.post-item h2 a {
  color: #1a1a1a;
  text-decoration: none;
  transition: opacity 0.3s ease;
}

.post-item:hover h2 a {
  opacity: 0.7;
}

.post-meta {
  color: #999;
  font-size: 0.75rem;
  font-weight: 300;
  letter-spacing: 0.05em;
  margin: 0 0 1rem 0;
  text-transform: uppercase;
}

.post-item p {
  color: #666;
  font-size: 0.875rem;
  line-height: 1.7;
  margin: 1rem 0;
  font-weight: 300;
}

.read-more {
  display: inline-block;
  padding: 0.5rem 1.2rem;
  margin-top: 1rem;
  background: transparent;
  color: #1a1a1a !important;
  text-decoration: none;
  border: 1px solid #1a1a1a;
  border-radius: 4px;
  font-size: 0.8rem;
  font-weight: 400;
  letter-spacing: 0.05em;
  transition: all 0.3s ease;
}

.read-more:hover {
  background: #1a1a1a;
  color: white !important;
}

.empty-state {
  text-align: center;
  padding: 4rem 2rem;
  color: #999;
  font-size: 0.875rem;
  font-weight: 300;
  font-style: italic;
}

@media (max-width: 768px) {
  .post-item {
    padding: 1.5rem;
  }
  
  .post-item h2 {
    font-size: 1.1rem;
  }
}
</style>

<p class="intro-text">
Hier veröffentliche ich Analysen zu wirtschaftlichen Themen, Marktentwicklungen und wirtschaftspolitischen Fragestellungen.
</p>

<div class="post-list">
{% for analyse in site.analysen %}
  <article class="post-item">
    <h2><a href="{{ analyse.url | relative_url }}">{{ analyse.title }}</a></h2>
    <p class="post-meta">{{ analyse.date | date: "%d. %B %Y" }}</p>
    <p>{{ analyse.excerpt }}</p>
    <a href="{{ analyse.url | relative_url }}" class="read-more">Weiterlesen</a>
  </article>
{% endfor %}
</div>

{% if site.analysen.size == 0 %}
<div class="empty-state">
  <p>Bald erscheinen hier die ersten Analysen...</p>
</div>
{% endif %}