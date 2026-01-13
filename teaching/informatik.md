---
layout: page
title: Informatik
permalink: /teaching/informatik/
---

<style>
/* Japandi Design - Japanisch-Skandinavische Fusion */

body {
  background: #f7f5f2;
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Inter", "Segoe UI", sans-serif;
  line-height: 1.7;
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
  border-left: 3px solid #8b9e9f;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  letter-spacing: 0.02em;
}

.post-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.post-item {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 2px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  display: flex;
  flex-direction: column;
  min-height: 280px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

/* Dezente, natürliche Farbpalette für Kategorien */
.category-programmierung .post-item {
  border-top: 2px solid #b8a89a;
}

.category-algorithmen .post-item {
  border-top: 2px solid #8b9e9f;
}

/* Minimalistischer Akzent */
.post-item::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 1px;
  height: 60px;
  opacity: 0.15;
  transition: all 0.4s ease;
}

.category-programmierung .post-item::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.category-algorithmen .post-item::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

/* Dezenter Cover-Effekt */
.post-item::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 2px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.4s ease;
  z-index: 0;
}

.category-programmierung .post-item::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.category-algorithmen .post-item::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
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

/* Card Header Styling */
.post-item h3 {
  margin: 0;
  padding: 2rem 2rem 1.25rem 2rem;
  position: relative;
  z-index: 2;
  border-bottom: 1px solid #f5f3f0;
  transition: border-bottom-color 0.4s ease;
}

.post-item:hover h3 {
  border-bottom-color: transparent;
}

.post-item h3::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 1px;
  opacity: 0;
  transform: scaleX(0);
  transform-origin: left;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
}

.category-programmierung .post-item h3::after {
  background: linear-gradient(90deg, #b8a89a 0%, transparent 100%);
}

.category-algorithmen .post-item h3::after {
  background: linear-gradient(90deg, #8b9e9f 0%, transparent 100%);
}

.post-item:hover h3::after {
  opacity: 1;
  transform: scaleX(1);
}

.post-item h3 a {
  color: #3d3d3d;
  text-decoration: none;
  font-size: 1.05rem;
  font-weight: 500;
  line-height: 1.6;
  letter-spacing: 0.01em;
  transition: color 0.3s ease;
}

.category-programmierung .post-item:hover h3 a {
  color: #b8a89a;
}

.category-algorithmen .post-item:hover h3 a {
  color: #8b9e9f;
}

.post-item p {
  font-size: 0.88rem;
  color: #6b6b6b;
  margin: 0;
  padding: 1.5rem 2rem;
  flex-grow: 1;
  line-height: 1.8;
  font-weight: 400;
  letter-spacing: 0.01em;
  position: relative;
  z-index: 2;
}

.post-item p em {
  font-style: italic;
  color: #8a8a8a;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin: 0 2rem 2rem 2rem;
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
  z-index: 2;
}

.btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.category-programmierung .btn::before {
  background: linear-gradient(180deg, #b8a89a 0%, #cbbfb3 100%);
}

.category-algorithmen .btn::before {
  background: linear-gradient(180deg, #8b9e9f 0%, #a5b5b6 100%);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.12);
  border-color: transparent;
  color: #ffffff !important;
}

.btn:hover::before {
  opacity: 1;
}

.btn:hover::after {
  opacity: 1;
  transform: translateX(0);
}

.btn::after {
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

.btn span {
  position: relative;
  z-index: 2;
}

.section-header {
  position: relative;
  padding: 0.5rem 0 0.5rem 1rem;
  margin: 4.5rem 0 2rem 0;
  font-weight: 500;
  font-size: 1.2rem;
  letter-spacing: 0.02em;
  display: inline-block;
  border-left: 2px solid;
}

/* Natürliche Farbcodierung */
h2.section-header:nth-of-type(1),
.category-programmierung .section-header {
  border-left-color: #b8a89a;
  color: #7d7169;
}

h2.section-header:nth-of-type(2),
.category-algorithmen .section-header {
  border-left-color: #8b9e9f;
  color: #5d6f70;
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
  background: radial-gradient(circle, rgba(139, 158, 159, 0.06) 0%, transparent 60%);
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

.back-link-container {
  margin-top: 4rem;
}

.back-link-container a {
  display: inline-block;
  padding: 0.9rem 2.5rem;
  background: #ffffff;
  color: #5a5a5a !important;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.85rem;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  border: 1px solid #e8e5e0;
  border-radius: 1px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.04);
}

.back-link-container a::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, #8b9e9f 0%, #a5b5b6 100%);
  opacity: 0;
  transition: opacity 0.3s ease;
  z-index: -1;
}

.back-link-container a:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.1);
  border-color: transparent;
  color: #ffffff !important;
}

.back-link-container a:hover::before {
  opacity: 1;
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
    radial-gradient(circle at 20% 30%, rgba(184, 168, 154, 0.02) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(139, 158, 159, 0.02) 0%, transparent 50%);
  pointer-events: none;
  z-index: -1;
}

@media (max-width: 768px) {
  .post-list {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
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
  
  .post-item {
    min-height: auto;
  }
  
  .section-header {
    font-size: 1.1rem;
  }
  
  .intro-text {
    font-size: 0.9rem;
    padding: 1.5rem 1.75rem;
  }
  
  .post-item h3 {
    padding: 1.75rem 1.5rem 1rem 1.5rem;
  }
  
  .post-item p {
    padding: 1.25rem 1.5rem;
  }
  
  .btn {
    margin: 0 1.5rem 1.75rem 1.5rem;
  }
}
</style>

<p class="intro-text">
  Materialien zur Informatik für die Prüfungsvorbereitung am Studienkolleg
</p>

<h2 class="section-header">Programmierung</h2>
<div class="post-list category-programmierung">
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
  <article class="post-item">
    <p><em>Materialien werden in Kürze hinzugefügt...</em></p>
  </article>
{% endif %}
</div>

<h2 class="section-header">Algorithmen und Datenstrukturen</h2>
<div class="post-list category-algorithmen">
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
  <article class="post-item">
    <p><em>Materialien werden in Kürze hinzugefügt...</em></p>
  </article>
{% endif %}
</div>

<div class="back-link-container">
  <a href="/teaching/">← Zurück zur Übersicht</a>
</div>