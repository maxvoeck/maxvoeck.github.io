---
layout: page
title: 
permalink: /teaching/
---

<style>
/* Japandi Design mit Apple-Style Rounded Corners */

body {
  background: linear-gradient(135deg, #f7f5f2 0%, #f0ede8 25%, #e8e5e0 50%, #f0ede8 75%, #f7f5f2 100%);
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Inter", "Segoe UI", sans-serif;
  line-height: 1.7;
  color: #3d3d3d;
  min-height: 100vh;
  background-attachment: fixed;
}

.intro-text {
  font-size: 0.95rem;
  color: #6b6b6b;
  font-weight: 400;
  margin-bottom: 3.5rem;
  padding: 2rem 2.5rem;
  background: #ffffff;
  border-radius: 18px;
  border-left: 3px solid #8b9e9f;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  letter-spacing: 0.02em;
  line-height: 1.8;
}

.sections {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.section-card {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 20px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

/* Dezente, natürliche Farbpalette */
.section-card.math {
  border-top: 2px solid #b8a89a;
}

.section-card.econ {
  border-top: 2px solid #c9a690;
}

.section-card.cs {
  border-top: 2px solid #8b9e9f;
}

/* Minimalistischer Akzent */
.section-card::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 1px;
  height: 60px;
  opacity: 0.15;
  transition: all 0.4s ease;
}

.section-card.math::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.section-card.econ::before {
  background: linear-gradient(to bottom, #c9a690, transparent);
}

.section-card.cs::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

/* Dezenter Cover-Effekt */
.section-card::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 20px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.4s ease;
  z-index: 0;
}

.section-card.math::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.section-card.econ::after {
  background: linear-gradient(180deg, rgba(201, 166, 144, 0.04) 0%, rgba(201, 166, 144, 0.02) 100%);
}

.section-card.cs::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
}

.section-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  border-color: #d5d0ca;
}

.section-card:hover::after {
  opacity: 1;
}

.section-card:hover::before {
  height: 100%;
  width: 3px;
  opacity: 0.4;
}

.card-header {
  padding: 2rem 2rem 1.5rem 2rem;
  position: relative;
  z-index: 2;
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
}

.icon-wrapper {
  width: 48px;
  height: 48px;
  background: transparent;
  border: 1px solid #e8e5e0;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  transition: all 0.3s ease;
  position: relative;
  z-index: 3;
}

.section-card.math:hover .icon-wrapper {
  background: #b8a89a;
  border-color: #b8a89a;
}

.section-card.econ:hover .icon-wrapper {
  background: #c9a690;
  border-color: #c9a690;
}

.section-card.cs:hover .icon-wrapper {
  background: #8b9e9f;
  border-color: #8b9e9f;
}

.icon-wrapper svg {
  width: 24px;
  height: 24px;
  fill: #6b6b6b;
  transition: fill 0.3s ease;
}

.section-card:hover .icon-wrapper svg {
  fill: #ffffff;
}

.card-title-wrapper {
  flex-grow: 1;
}

.section-card h2 {
  margin: 0;
  color: #3d3d3d;
  font-size: 1.15rem;
  font-weight: 500;
  letter-spacing: 0.01em;
  line-height: 1.4;
  transition: color 0.3s ease;
}

.section-card.math:hover h2 {
  color: #b8a89a;
}

.section-card.econ:hover h2 {
  color: #c9a690;
}

.section-card.cs:hover h2 {
  color: #8b9e9f;
}

.card-content {
  padding: 0 2rem 2rem 2rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  position: relative;
  z-index: 2;
}

.section-card p {
  color: #6b6b6b;
  line-height: 1.8;
  margin: 0 0 1.5rem 0;
  font-size: 0.88rem;
  font-weight: 400;
  letter-spacing: 0.01em;
}

.topics-preview {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}

.tag {
  background: #fafaf9;
  color: #6b6b6b;
  padding: 0.35rem 0.85rem;
  border: 1px solid #e8e5e0;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 400;
  letter-spacing: 0.02em;
  transition: all 0.3s ease;
}

.section-card.math:hover .tag {
  border-color: #b8a89a;
  background: rgba(184, 168, 154, 0.08);
  color: #7d7169;
}

.section-card.econ:hover .tag {
  border-color: #c9a690;
  background: rgba(201, 166, 144, 0.08);
  color: #8d7a6a;
}

.section-card.cs:hover .tag {
  border-color: #8b9e9f;
  background: rgba(139, 158, 159, 0.08);
  color: #5d6f70;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.9rem 1.5rem;
  background: #fafaf9;
  color: #5a5a5a !important;
  text-decoration: none;
  border: 1px solid #e8e5e0;
  border-radius: 12px;
  font-size: 0.85rem;
  font-weight: 500;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
  margin-top: auto;
  align-self: flex-start;
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

.section-card.math .btn::before {
  background: linear-gradient(180deg, #b8a89a 0%, #cbbfb3 100%);
}

.section-card.econ .btn::before {
  background: linear-gradient(180deg, #c9a690 0%, #dbc0af 100%);
}

.section-card.cs .btn::before {
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

.page-header {
  background: #ffffff;
  color: #3d3d3d;
  padding: 3.5rem 2.5rem;
  margin: -2rem -2rem 4rem -2rem;
  position: relative;
  overflow: hidden;
  border-bottom: 1px solid #e8e5e0;
  border-radius: 0 0 32px 32px;
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

.footer-note {
  text-align: center;
  color: #8a8a8a;
  margin-top: 4rem;
  padding-top: 2.5rem;
  border-top: 1px solid #e8e5e0;
  font-size: 0.85rem;
  font-weight: 400;
  letter-spacing: 0.01em;
  line-height: 1.7;
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
    radial-gradient(circle at 15% 25%, rgba(184, 168, 154, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 85% 75%, rgba(139, 158, 159, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 50% 50%, rgba(201, 184, 150, 0.02) 0%, transparent 60%);
  pointer-events: none;
  z-index: -1;
  opacity: 0.8;
}

@media (max-width: 768px) {
  .sections {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .page-header {
    margin: -1rem -1rem 2.5rem -1rem;
    padding: 2.5rem 1.75rem;
    border-radius: 0 0 24px 24px;
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
    border-radius: 16px;
  }

  .card-header {
    padding: 1.75rem 1.5rem 1.25rem 1.5rem;
  }

  .card-content {
    padding: 0 1.5rem 1.75rem 1.5rem;
  }

  .icon-wrapper {
    width: 40px;
    height: 40px;
    border-radius: 10px;
  }

  .icon-wrapper svg {
    width: 20px;
    height: 20px;
  }

  .section-card h2 {
    font-size: 1.05rem;
  }
  
  .section-card {
    border-radius: 16px;
  }
  
  .section-card::after {
    border-radius: 16px;
  }
  
  .btn {
    border-radius: 10px;
  }
}
</style>

<p class="intro-text">
  Ausgewählte Materialien aus meiner Lehrtätigkeit am Studienkolleg Leipzig. 
  Alle Unterlagen sind speziell auf die Anforderungen der Feststellungsprüfung (FSP) abgestimmt.
</p>

<div class="sections">
  <div class="section-card math">
    <div class="card-header">
      <div class="icon-wrapper">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M18 4H8.5L14 12L8.5 20H18V18H11.5L16 12L11.5 6H18V4Z"/>
        </svg>
      </div>
      <div class="card-title-wrapper">
        <h2>Mathematik</h2>
      </div>
    </div>
    <div class="card-content">
      <p>Fundierte Vorbereitung auf Analysis und Lineare Algebra für technische Studiengänge</p>
      <div class="topics-preview">
        <span class="tag">Integralrechnung</span>
        <span class="tag">Vektorräume</span>
        <span class="tag">Differentialrechnung</span>
      </div>
      <a href="/teaching/mathematik/" class="btn"><span>Materialien ansehen</span></a>
    </div>
  </div>

  <div class="section-card econ">
    <div class="card-header">
      <div class="icon-wrapper">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M3 14L5 12L9 16L14 11L16 13L21 8V18C21 19.1 20.1 20 19 20H5C3.9 20 3 19.1 3 18V14ZM21 5V7L16 12L14 10L9 15L5 11L3 13V5C3 3.9 3.9 3 5 3H19C20.1 3 21 3.9 21 5Z"/>
        </svg>
      </div>
      <div class="card-title-wrapper">
        <h2>Volkswirtschaftslehre</h2>
      </div>
    </div>
    <div class="card-content">
      <p>Makro- und Mikroökonomie mit praxisnahen Beispielen und aktuellen Bezügen</p>
      <div class="topics-preview">
        <span class="tag">Marktgleichgewicht</span>
        <span class="tag">Preiselastizität</span>
        <span class="tag">Wirtschaftskreislauf</span>
      </div>
      <a href="/teaching/vwl/" class="btn"><span>Materialien ansehen</span></a>
    </div>
  </div>

  <div class="section-card cs">
    <div class="card-header">
      <div class="icon-wrapper">
        <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path d="M8 3L4 7L8 11L9.4 9.6L6.8 7L9.4 4.4L8 3ZM16 3L14.6 4.4L17.2 7L14.6 9.6L16 11L20 7L16 3ZM10 13L12 21L14 20L12 12L10 13Z"/>
        </svg>
      </div>
      <div class="card-title-wrapper">
        <h2>Informatik</h2>
      </div>
    </div>
    <div class="card-content">
      <p>Grundlagen der Programmierung und algorithmisches Denken für Einsteiger</p>
      <div class="topics-preview">
        <span class="tag">Python</span>
        <span class="tag">Algorithmen</span>
        <span class="tag">Datenstrukturen</span>
      </div>
      <a href="/teaching/informatik/" class="btn"><span>Materialien ansehen</span></a>
    </div>
  </div>
</div>