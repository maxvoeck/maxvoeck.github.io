---
layout: page
title: Mathematik
permalink: /teaching/mathematik/
---

<style>
.materials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.material-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1.5rem;
  transition: box-shadow 0.3s ease;
  background: #fff;
}

.material-card:hover {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.material-card h4 {
  margin-top: 0;
  color: #333;
  font-size: 1.1rem;
}

.material-card p {
  font-size: 0.9rem;
  color: #666;
  margin: 0.5rem 0 1rem 0;
}

.btn-small {
  display: inline-block;
  padding: 0.4rem 0.8rem;
  background: linear-gradient(135deg, #374151 0%, #1f2937 100%);
  color: white !important;
  text-decoration: none;
  border-radius: 4px;
  font-size: 0.85rem;
  transition: all 0.3s ease;
}

.btn-small:hover {
  background: linear-gradient(135deg, #4b5563 0%, #374151 100%);
  transform: translateY(-1px);
  color: black !important;
}

.section-header {
  border-bottom: 2px solid #374151;
  padding-bottom: 0.5rem;
  margin: 2rem 0 1rem 0;
  color: #1f2937;
}

.coming-soon {
  background: #f8f9fa;
  padding: 1rem;
  border-radius: 4px;
  color: #666;
  font-style: italic;
  border-left: 4px solid #374151;
}

.page-header {
  background: linear-gradient(135deg, #374151 0%, #1f2937 100%);
  color: white;
  padding: 2rem;
  margin: -2rem -2rem 2rem -2rem;
  border-radius: 0 0 12px 12px;
}

.page-header h1 {
  margin: 0;
  font-size: 2rem;
}

.back-link {
  display: inline-block;
  margin-top: 2rem;
  color: #374151;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.back-link:hover {
  color: #1f2937;
}

@media (max-width: 768px) {
  .materials-grid {
    grid-template-columns: 1fr;
  }
  
  .page-header {
    margin: -1rem -1rem 2rem -1rem;
    padding: 1.5rem;
  }
  
  .page-header h1 {
    font-size: 1.5rem;
  }
}
</style>

<div class="page-header">
  <h1>Mathematik</h1>
  <p>Materialien zur Prüfungsvorbereitung am Studienkolleg</p>
</div>

<h2 class="section-header">Lineare Algebra</h2>
<div class="coming-soon">Materialien werden in Kürze hinzugefügt...</div>

<h2 class="section-header">Differentialrechnung</h2>
<div class="coming-soon">Materialien werden in Kürze hinzugefügt...</div>

<h2 class="section-header">Integralrechnung</h2>
<div class="materials-grid">
  <div class="material-card">
    <h4>📘 Einführung</h4>
    <p>Stammfunktionen, Grundintegrale, Faktor- und Summenregel, bestimmtes Integral</p>
    <a href="/assets/pdfs/Integral_2_1.pdf" class="btn-small">PDF öffnen</a>
  </div>
  
  <div class="material-card">
    <h4>📗 Integrationsmethoden</h4>
    <p>Substitution, partielle Integration, LIATE-Regel, Partialbruchzerlegung</p>
    <a href="/assets/pdfs/Integral_2_2.pdf" class="btn-small">PDF öffnen</a>
  </div>
  
  <div class="material-card">
    <h4>📙 Hauptsatz & Flächen</h4>
    <p>Hauptsatz, bestimmte Integrale, Flächenberechnung zwischen Graphen</p>
    <a href="/assets/pdfs/Integral_2_3.pdf" class="btn-small">PDF öffnen</a>
  </div>
</div>

<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>