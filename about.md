---
layout: page
title: 
permalink: /about/
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

.intro-section {
  background: #ffffff;
  border-radius: 2px;
  padding: 2.5rem;
  margin-bottom: 3rem;
  border-left: 3px solid #8b9e9f;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  position: relative;
}

.intro-section p {
  font-size: 1rem;
  color: #6b6b6b;
  line-height: 1.8;
  margin: 0;
  letter-spacing: 0.02em;
  font-weight: 400;
}

.content-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.content-card {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 2px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

.content-card.education {
  border-top: 2px solid #b8a89a;
}

.content-card.focus {
  border-top: 2px solid #c9a690;
}

.content-card.interests {
  border-top: 2px solid #8b9e9f;
}

/* Minimalistischer Akzent */
.content-card::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 1px;
  height: 60px;
  opacity: 0.15;
  transition: all 0.4s ease;
}

.content-card.education::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.content-card.focus::before {
  background: linear-gradient(to bottom, #c9a690, transparent);
}

.content-card.interests::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

/* Dezenter Cover-Effekt */
.content-card::after {
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

.content-card.education::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.content-card.focus::after {
  background: linear-gradient(180deg, rgba(201, 166, 144, 0.04) 0%, rgba(201, 166, 144, 0.02) 100%);
}

.content-card.interests::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
}

.content-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  border-color: #d5d0ca;
}

.content-card:hover::after {
  opacity: 1;
}

.content-card:hover::before {
  height: 100%;
  width: 3px;
  opacity: 0.4;
}

.card-header {
  padding: 2rem 2rem 1rem 2rem;
  position: relative;
  z-index: 2;
}

.card-header h2 {
  margin: 0;
  font-size: 1.15rem;
  font-weight: 500;
  letter-spacing: 0.01em;
  color: #3d3d3d;
  transition: color 0.3s ease;
}

.content-card.education:hover .card-header h2 {
  color: #b8a89a;
}

.content-card.focus:hover .card-header h2 {
  color: #c9a690;
}

.content-card.interests:hover .card-header h2 {
  color: #8b9e9f;
}

.card-content {
  padding: 0 2rem 2rem 2rem;
  position: relative;
  z-index: 2;
}

.education-item {
  margin-bottom: 1.5rem;
}

.education-item:last-child {
  margin-bottom: 0;
}

.education-item strong {
  display: block;
  color: #3d3d3d;
  font-size: 0.9rem;
  font-weight: 500;
  margin-bottom: 0.25rem;
  letter-spacing: 0.01em;
}

.education-item span {
  color: #8a8a8a;
  font-size: 0.8rem;
  font-weight: 400;
  letter-spacing: 0.02em;
}

.focus-list,
.interest-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.focus-list li,
.interest-list li {
  position: relative;
  padding-left: 1.5rem;
  margin-bottom: 1.25rem;
  color: #6b6b6b;
  font-size: 0.88rem;
  line-height: 1.8;
  font-weight: 400;
  letter-spacing: 0.01em;
}

.focus-list li:last-child,
.interest-list li:last-child {
  margin-bottom: 0;
}

.focus-list li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0.65rem;
  width: 6px;
  height: 6px;
  background: #c9a690;
  border-radius: 50%;
}

.interest-list li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0.65rem;
  width: 6px;
  height: 6px;
  background: #8b9e9f;
  border-radius: 50%;
}

.focus-list li strong,
.interest-list li strong {
  color: #3d3d3d;
  font-weight: 500;
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
  .content-grid {
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

  .intro-section {
    padding: 1.75rem;
    margin-bottom: 2.5rem;
  }

  .intro-section p {
    font-size: 0.9rem;
  }

  .card-header {
    padding: 1.75rem 1.5rem 1rem 1.5rem;
  }

  .card-content {
    padding: 0 1.5rem 1.75rem 1.5rem;
  }

  .card-header h2 {
    font-size: 1.05rem;
  }
}
</style>

<div class="intro-section">
  <p>
    Ich bin Mathematik-, Informatik- und Wirtschaftslehrer am Studienkolleg Leipzig, 
    wo ich internationale Studierende auf ihr Hochschulstudium vorbereite.
  </p>
</div>

<div class="content-grid">
  <div class="content-card education">
    <div class="card-header">
      <h2>Ausbildung</h2>
    </div>
    <div class="card-content">
      <div class="education-item">
        <strong>Bachelor in Mathematik</strong>
        <span>Heinrich-Heine-Universität Düsseldorf</span>
      </div>
      <div class="education-item">
        <strong>Data Science Master</strong>
        <span>RWTH Aachen</span>
      </div>
    </div>
  </div>

  <div class="content-card focus">
    <div class="card-header">
      <h2>Schwerpunkte</h2>
    </div>
    <div class="card-content">
      <ul class="focus-list">
        <li><strong>Mathematik & Data Science:</strong> Von Analysis und linearer Algebra bis zu praktischer Datenanalyse</li>
        <li><strong>Wirtschaftswissenschaften:</strong> Volkswirtschaftslehre, Marktanalysen, kritische Wirtschaftstheorie</li>
        <li><strong>Didaktik & Bildung:</strong> Entwicklung interaktiver Lernmaterialien und digitaler Bildungsressourcen</li>
      </ul>
    </div>
  </div>

  <div class="content-card interests">
    <div class="card-header">
      <h2>Interessen</h2>
    </div>
    <div class="card-content">
      <ul class="interest-list">
        <li>Kritische Theorie und Kulturanalyse</li>
        <li>Wirtschaftsphilosophie</li>
        <li>Schnittstelle zwischen quantitativen Methoden und gesellschaftlicher Analyse</li>
      </ul>
    </div>
  </div>
</div>