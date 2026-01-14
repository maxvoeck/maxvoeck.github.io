---
layout: page
title: 
permalink: /analysen/
---

<style>
/* Japandi Design - Japanisch-Skandinavische Fusion */

body {
  background: #f7f5f2;
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Inter", "Segoe UI", sans-serif;
  line-height: 1.7;
  color: #3d3d3d;
}

.page-header {
  background: #ffffff;
  color: #3d3d3d;
  padding: 3.5rem 2.5rem;
  margin: -2rem -2rem 4rem -2rem;
  position: relative;
  overflow: hidden;
  border-bottom: 1px solid #e8e5e0;
}

/* Zen-inspirierte Dekoration */
.page-header::before {
  content: '';
  position: absolute;
  top: 50%;
  right: 60px;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(201, 166, 144, 0.06) 0%, transparent 60%);
  border-radius: 50%;
  transform: translateY(-50%);
}

.page-header::after {
  content: '';
  position: absolute;
  top: 50%;
  right: 180px;
  width: 120px;
  height: 120px;
  background: radial-gradient(circle, rgba(184, 168, 154, 0.04) 0%, transparent 60%);
  border-radius: 50%;
  transform: translateY(-50%);
}

.page-header h1 {
  margin: 0;
  font-size: 2.2rem;
  font-weight: 400;
  letter-spacing: 0.02em;
  position: relative;
  z-index: 1;
  color: #3d3d3d;
}

.intro-text {
  font-size: 0.95rem;
  color: #6b6b6b;
  font-weight: 400;
  margin-bottom: 3.5rem;
  padding: 2rem 2.5rem;
  background: #ffffff;
  border-radius: 2px;
  border-left: 3px solid #c9a690;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  letter-spacing: 0.02em;
  line-height: 1.8;
}

.post-list {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  margin: 2.5rem 0;
}

.post-item {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 2px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
  border-top: 2px solid #c9a690;
}

/* Minimalistischer Akzent */
.post-item::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 1px;
  height: 60px;
  background: linear-gradient(to bottom, #c9a690, transparent);
  opacity: 0.15;
  transition: all 0.4s ease;
}

/* Dezenter Cover-Effekt */
.post-item::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(180deg, rgba(201, 166, 144, 0.04) 0%, rgba(201, 166, 144, 0.02) 100%);
  border-radius: 2px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.4s ease;
  z-index: 0;
}

.post-item:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  border-color: #d5d0ca;
}

.post-item:hover::after {
  opacity: 1;
}

.post-item:hover::before {
  height: 100%;
  width: 3px;
  opacity: 0.4;
}

.post-content {
  padding: 2rem 2.5rem;
  position: relative;
  z-index: 2;
}

.post-item h2 {
  margin: 0 0 0.75rem 0;
  font-size: 1.15rem;
  font-weight: 500;
  letter-spacing: 0.01em;
  line-height: 1.4;
}

.post-item h2 a {
  color: #3d3d3d;
  text-decoration: none;
  transition: color 0.3s ease;
}

.post-item:hover h2 a {
  color: #c9a690;
}

.post-meta {
  color: #8a8a8a;
  font-size: 0.75rem;
  font-weight: 400;
  letter-spacing: 0.05em;
  margin: 0 0 1.25rem 0;
  text-transform: uppercase;
}

.post-item p {
  color: #6b6b6b;
  font-size: 0.88rem;
  line-height: 1.8;
  margin: 1rem 0 1.5rem 0;
  font-weight: 400;
  letter-spacing: 0.01em;
}

.read-more {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.9rem 1.5rem;
  background: #fafaf9;
  color: #5a5a5a !important;
  text-decoration: none;
  border: 1px solid #e8e5e0;
  border-radius: 1px;
  font-size: 0.85rem;
  font-weight: 500;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.read-more::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, #c9a690 0%, #dbc0af 100%);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.read-more:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.12);
  border-color: transparent;
  color: #ffffff !important;
}

.read-more:hover::before {
  opacity: 1;
}

.read-more:hover::after {
  opacity: 1;
  transform: translateX(0);
}

.read-more::after {
  content: '→';
  position: absolute;
  right: 1.5rem;
  opacity: 0;
  transform: translateX(-10px);
  transition: all 0.3s ease;
  z-index: 3;
  color: #ffffff;
  font-size: 1rem;
}

.read-more span {
  position: relative;
  z-index: 2;
}

.empty-state {
  text-align: center;
  padding: 4rem 2.5rem;
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 2px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
}

.empty-state p {
  color: #8a8a8a;
  font-size: 0.88rem;
  font-weight: 400;
  font-style: italic;
  letter-spacing: 0.01em;
  margin: 0;
}

/* Wabi-Sabi Textur-Effekt */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(circle at 20% 30%, rgba(201, 166, 144, 0.02) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(184, 168, 154, 0.02) 0%, transparent 50%);
  pointer-events: none;
  z-index: -1;
}

@media (max-width: 768px) {
  .page-header {
    margin: -1rem -1rem 2.5rem -1rem;
    padding: 2.5rem 1.75rem;
  }

  .page-header h1 {
    font-size: 1.8rem;
  }

  .page-header::before,
  .page-header::after {
    display: none;
  }

  .intro-text {
    font-size: 0.9rem;
    padding: 1.5rem 1.75rem;
    margin-bottom: 2.5rem;
  }

  .post-content {
    padding: 1.75rem 1.5rem;
  }

  .post-item h2 {
    font-size: 1.05rem;
  }

  .empty-state {
    padding: 3rem 1.5rem;
  }
}
</style>

<p class="intro-text">
  Hier veröffentliche ich Analysen zu wirtschaftlichen Themen, Marktentwicklungen und wirtschaftspolitischen Fragestellungen.
</p>

<div class="post-list">
  {% for analyse in site.analysen %}
  <article class="post-item">
    <div class="post-content">
      <h2><a href="{{ analyse.url | relative_url }}">{{ analyse.title }}</a></h2>
      <p class="post-meta">{{ analyse.date | date: "%d. %B %Y" }}</p>
      <p>{{ analyse.excerpt }}</p>
      <a href="{{ analyse.url | relative_url }}" class="read-more"><span>Weiterlesen</span></a>
    </div>
  </article>
  {% endfor %}
</div>

{% if site.analysen.size == 0 %}
<div class="empty-state">
  <p>Bald erscheinen hier die ersten Analysen...</p>
</div>
{% endif %}