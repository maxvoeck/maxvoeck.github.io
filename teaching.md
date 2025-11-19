---
layout: page
title: Unterrichtsmaterialien
permalink: /teaching/
---

<style>
.sections {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.section-card {
  background: #fff;
  border-radius: 12px;
  padding: 2rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  position: relative;
  overflow: hidden;
}

.section-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.section-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #6b7280, #374151);
}

.section-card.math::before {
  background: linear-gradient(90deg, #4b5563, #1f2937);
}

.section-card.econ::before {
  background: linear-gradient(90deg, #6b7280, #4b5563);
}

.section-card.cs::before {
  background: linear-gradient(90deg, #9ca3af, #6b7280);
}

.icon-wrapper {
  width: 60px;
  height: 60px;
  background: linear-gradient(135deg, #6b7280 0%, #4b5563 100%);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
}

.section-card.math .icon-wrapper {
  background: linear-gradient(135deg, #374151 0%, #1f2937 100%);
}

.section-card.econ .icon-wrapper {
  background: linear-gradient(135deg, #6b7280 0%, #4b5563 100%);
}

.section-card.cs .icon-wrapper {
  background: linear-gradient(135deg, #9ca3af 0%, #6b7280 100%);
}

.icon-wrapper svg {
  width: 32px;
  height: 32px;
  fill: white;
}

.section-card h2 {
  margin: 0 0 0.5rem 0;
  color: #333;
  font-size: 1.5rem;
}

.section-card p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.topics-preview {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}

.tag {
  background: #f0f0f0;
  color: #555;
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
}

.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: linear-gradient(135deg, #4b5563 0%, #374151 100%);
  color: white !important;
  text-decoration: none;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.3s ease;
  text-align: center;
}

.btn:hover {
  transform: translateX(4px);
  box-shadow: 0 4px 12px rgba(75, 85, 99, 0.3);
  color: black;
}

.section-card.math .btn {
  background: linear-gradient(135deg, #374151 0%, #1f2937 100%);
}

.section-card.econ .btn {
  background: linear-gradient(135deg, #6b7280 0%, #4b5563 100%);
}

.section-card.cs .btn {
  background: linear-gradient(135deg, #9ca3af 0%, #6b7280 100%);
}

.intro-text {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 2rem;
  line-height: 1.7;
}

.footer-note {
  text-align: center;
  color: #777;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid #e0e0e0;
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .sections {
    grid-template-columns: 1fr;
  }
}
</style>

<p class="intro-text">
  Ausgewählte Materialien aus meiner Lehrtätigkeit am Studienkolleg Leipzig. 
  Alle Unterlagen sind speziell auf die Anforderungen der Feststellungsprüfung (FSP) abgestimmt.
</p>

<div class="sections">
  <div class="section-card math">
    <div class="icon-wrapper">
      <!-- Sigma Symbol für Mathematik -->
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M18 4H8.5L14 12L8.5 20H18V18H11.5L16 12L11.5 6H18V4Z"/>
      </svg>
    </div>
    <h2>Mathematik</h2>
    <p>Fundierte Vorbereitung auf Analysis und Lineare Algebra für technische Studiengänge</p>
    <div class="topics-preview">
      <span class="tag">Integralrechnung</span>
      <span class="tag">Vektorräume</span>
      <span class="tag">Differentialrechnung</span>
    </div>
    <a href="/teaching/mathematik/" class="btn">Materialien ansehen →</a>
  </div>

  <div class="section-card econ">
    <div class="icon-wrapper">
      <!-- Chart Symbol für VWL -->
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M3 14L5 12L9 16L14 11L16 13L21 8V18C21 19.1 20.1 20 19 20H5C3.9 20 3 19.1 3 18V14ZM21 5V7L16 12L14 10L9 15L5 11L3 13V5C3 3.9 3.9 3 5 3H19C20.1 3 21 3.9 21 5Z"/>
      </svg>
    </div>
    <h2>Volkswirtschaftslehre</h2>
    <p>Makro- und Mikroökonomie mit praxisnahen Beispielen und aktuellen Bezügen</p>
    <div class="topics-preview">
      <span class="tag">Marktgleichgewicht</span>
      <span class="tag">Preiselastizität</span>
      <span class="tag">Wirtschaftskreislauf</span>
    </div>
    <a href="/teaching/vwl/" class="btn">Materialien ansehen →</a>
  </div>

  <div class="section-card cs">
    <div class="icon-wrapper">
      <!-- Code Symbol für Informatik -->
      <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M8 3L4 7L8 11L9.4 9.6L6.8 7L9.4 4.4L8 3ZM16 3L14.6 4.4L17.2 7L14.6 9.6L16 11L20 7L16 3ZM10 13L12 21L14 20L12 12L10 13Z"/>
      </svg>
    </div>
    <h2>Informatik</h2>
    <p>Grundlagen der Programmierung und algorithmisches Denken für Einsteiger</p>
    <div class="topics-preview">
      <span class="tag">Python</span>
      <span class="tag">Algorithmen</span>
      <span class="tag">Datenstrukturen</span>
    </div>
    <a href="/teaching/informatik/" class="btn">Materialien ansehen →</a>
  </div>
</div>

<div class="footer-note">
  📚 Diese Materialien sind für Bildungszwecke erstellt und können frei verwendet werden.<br>
  Bei Fragen oder Anregungen stehe ich gerne zur Verfügung.
</div>