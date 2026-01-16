---
layout: page
title: 
permalink: /teaching/informatik/
---

<style>
/* Japandi Design - wie Mathematik */

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

.materials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.material-card {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 2px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  display: flex;
  flex-direction: column;
  min-height: 320px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

/* Farbpalette für Informatik-Kategorien */
.category-programmierung .material-card {
  border-top: 2px solid #b8a89a;
}

.category-algorithmen .material-card {
  border-top: 2px solid #8b9e9f;
}

/* Minimalistischer Akzent */
.material-card::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 1px;
  height: 60px;
  opacity: 0.15;
  transition: all 0.4s ease;
}

.category-programmierung .material-card::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.category-algorithmen .material-card::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

/* Dezenter Cover-Effekt */
.material-card::after {
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

.category-programmierung .material-card::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.category-algorithmen .material-card::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
}

.material-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  border-color: #d5d0ca;
}

.material-card:hover::after {
  opacity: 1;
}

.material-card:hover::before {
  height: 100%;
  width: 3px;
  opacity: 0.4;
}

/* Header Hover-Linie wie Mathe */
.material-card:hover .card-header {
  border-bottom-color: transparent;
}

.material-card:hover .card-header::after {
  opacity: 1;
  transform: scaleX(1);
}

.card-header::after {
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

.category-programmierung .card-header::after {
  background: linear-gradient(90deg, #b8a89a 0%, transparent 100%);
}

.category-algorithmen .card-header::after {
  background: linear-gradient(90deg, #8b9e9f 0%, transparent 100%);
}

.card-header {
  padding: 2rem 2rem 1.25rem 2rem;
  position: relative;
  z-index: 2;
  border-bottom: 1px solid #f5f3f0;
}

.material-card h4 {
  margin: 0;
  color: #3d3d3d;
  font-size: 1.05rem;
  font-weight: 500;
  line-height: 1.6;
  letter-spacing: 0.01em;
  transition: color 0.3s ease;
}

.category-programmierung .material-card:hover h4 {
  color: #b8a89a;
}

.category-algorithmen .material-card:hover h4 {
  color: #8b9e9f;
}

.card-content {
  padding: 1.5rem 2rem 2rem 2rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  position: relative;
  z-index: 2;
}

.material-card p {
  font-size: 0.88rem;
  color: #6b6b6b;
  margin: 0 0 2rem 0;
  flex-grow: 1;
  line-height: 1.8;
  font-weight: 400;
  letter-spacing: 0.01em;
}

.button-group {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  margin-top: auto;
}

.btn-small {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.9rem 1rem;
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

.btn-small::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.category-programmierung .btn-small:first-child::before {
  background: linear-gradient(180deg, #b8a89a 0%, #cbbfb3 100%);
}

.category-algorithmen .btn-small:first-child::before {
  background: linear-gradient(180deg, #8b9e9f 0%, #a5b5b6 100%);
}

.btn-small:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.12);
  border-color: transparent;
  color: #ffffff !important;
}

.btn-small:hover::before {
  opacity: 1;
}

.btn-small:hover::after {
  opacity: 1;
  transform: translateX(0);
}

.btn-small::after {
  content: '→';
  position: absolute;
  right: 1rem;
  opacity: 0;
  transform: translateX(-10px);
  transition: all 0.3s ease;
  z-index: 3;
  color: #ffffff;
  font-size: 1rem;
}

.btn-quiz:hover::after {
  content: '✓';
}

.btn-small span {
  position: relative;
  z-index: 2;
}

.btn-quiz {
  background: #ffffff;
  border-color: #e0ddd8;
}

.btn-quiz::before {
  background: linear-gradient(180deg, #6b6b6b 0%, #8a8a8a 100%);
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

/* Informatik: 2 Sections */
h2.section-header:nth-of-type(1) {
  border-left-color: #b8a89a;
  color: #7d7169;
}

h2.section-header:nth-of-type(2) {
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

.back-link {
  display: inline-block;
  margin-top: 4rem;
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

.back-link::before {
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

.back-link:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.1);
  border-color: transparent;
  color: #ffffff !important;
}

.back-link:hover::before {
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
  .materials-grid {
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

  .material-card {
    min-height: auto;
  }

  .section-header {
    font-size: 1.1rem;
  }

  .intro-text {
    font-size: 0.9rem;
    padding: 1.5rem 1.75rem;
  }

  .card-header {
    padding: 1.75rem 1.5rem 1rem 1.5rem;
  }

  .card-content {
    padding: 1.25rem 1.5rem 1.75rem 1.5rem;
  }
}
</style>

<p class="intro-text">
  Materialien zur Informatik für die Prüfungsvorbereitung am Studienkolleg
</p>

<h2 class="section-header">Programmierung</h2>
<div class="materials-grid category-programmierung">
  <div class="material-card">
    <div class="card-header">
      <h4>Python Grundlagen – print() und input()</h4>
    </div>
    <div class="card-content">
      <p>
        Einführung in Python: Die print()-Funktion zur Ausgabe von Text und Zahlen, Parameter sep und end, input() für Benutzereingaben,
        Datentypen (str, int, float) und Umwandlung mit int() und float(). Praktische Übungen zu Altersrechner, BMI und Einkaufslisten
      </p>
      <div class="button-group">
        <a href="/assets/pdfs/Info_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/v.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
</div>


<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>
