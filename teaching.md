---
layout: page
title: Unterrichtsmaterialien
permalink: /teaching/
---

<style>
body {
  background: #f5f5f4;
}

.sections {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.section-card {
  background: #fafaf9;
  border-radius: 8px;
  padding: 2rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

.section-card::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background: #1a1a1a;
  transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.section-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
}

.section-card:hover::after {
  width: 100%;
}

.icon-wrapper {
  width: 48px;
  height: 48px;
  background: transparent;
  border: 1px solid #1a1a1a;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  transition: all 0.3s ease;
}

.section-card:hover .icon-wrapper {
  background: #1a1a1a;
}

.icon-wrapper svg {
  width: 24px;
  height: 24px;
  fill: #1a1a1a;
  transition: fill 0.3s ease;
}

.section-card:hover .icon-wrapper svg {
  fill: white;
}

.section-card h2 {
  margin: 0 0 0.5rem 0;
  color: #1a1a1a;
  font-size: 1.25rem;
  font-weight: 500;
  letter-spacing: 0.02em;
}

.section-card p {
  color: #666;
  line-height: 1.7;
  margin-bottom: 1.5rem;
  font-size: 0.875rem;
  font-weight: 300;
  flex-grow: 1;
}

.topics-preview {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
}

.tag {
  background: transparent;
  color: #666;
  padding: 0.25rem 0.75rem;
  border: 1px solid #e0e0e0;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 400;
  letter-spacing: 0.03em;
}

.btn {
  display: inline-block;
  padding: 0.5rem 1.2rem;
  background: transparent;
  color: #1a1a1a !important;
  text-decoration: none;
  border: 1px solid #1a1a1a;
  border-radius: 4px;
  font-weight: 400;
  font-size: 0.8rem;
  letter-spacing: 0.05em;
  transition: all 0.3s ease;
  text-align: center;
  margin-top: auto;
}

.btn:hover {
  background: #1a1a1a;
  color: white !important;
}

.intro-text {
  font-size: 1rem;
  color: #666;
  margin-bottom: 2rem;
  line-height: 1.7;
  font-weight: 300;
}

.footer-note {
  text-align: center;
  color: #999;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid #e0e0e0;
  font-size: 0.8rem;
  font-weight: 300;
  letter-spacing: 0.02em;
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
    <a href="/teaching/mathematik/" class="btn">Materialien ansehen</a>
  </div>

  <div class="section-card econ">
    <div class="icon-wrapper">
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
    <a href="/teaching/vwl/" class="btn">Materialien ansehen</a>
  </div>

  <div class="section-card cs">
    <div class="icon-wrapper">
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
    <a href="/teaching/informatik/" class="btn">Materialien ansehen</a>
  </div>
</div>

<div class="footer-note">
  Diese Materialien sind für Bildungszwecke erstellt und können frei verwendet werden.
  Bei Fragen oder Anregungen stehe ich gerne zur Verfügung.
</div>