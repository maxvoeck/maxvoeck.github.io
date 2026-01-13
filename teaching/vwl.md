---
layout: page
title: Volkswirtschaftslehre
permalink: /teaching/vwl/
---

<style>
/* Radical Bauhaus design with primary colors and geometric emphasis */

body {
  background: #ffffff;
  font-family: -apple-system, BlinkMacSystemFont, "Futura", "Avenir Next", "Helvetica Neue", Arial, sans-serif;
}

.intro-text {
  font-size: 1rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: #000000;
  font-weight: 300;
  margin-bottom: 3rem;
  border-left: 4px solid #000000;
  padding-left: 1rem;
}

.materials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.material-card {
  background: #ffffff;
  border: 3px solid #000000;
  padding: 0;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  display: flex;
  flex-direction: column;
  min-height: 300px;
  position: relative;
  overflow: hidden;
}

/* Bold primary color accents per category - Bauhaus style */
.category-mikro .material-card {
  border-top: 8px solid #e63946; /* Red for Mikroökonomie */
}

.category-makro .material-card {
  border-top: 8px solid #457b9d; /* Blue for Makroökonomie */
}

.category-klausur .material-card {
  border-top: 8px solid #000000; /* Black for Klausuraufgaben */
}

.material-card::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 60px;
  height: 60px;
  transition: transform 0.3s ease;
}

.category-mikro .material-card::before {
  background: #e63946;
  clip-path: polygon(100% 0, 100% 100%, 0 0);
}

.category-makro .material-card::before {
  background: #457b9d;
  clip-path: polygon(100% 0, 100% 100%, 0 0);
}

.category-klausur .material-card::before {
  background: #000000;
  clip-path: polygon(100% 0, 100% 100%, 0 0);
}

.material-card:hover {
  transform: translateY(-4px);
  box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.2);
}

.material-card:hover::before {
  transform: scale(1.2);
}

.card-header {
  background: #000000;
  color: #ffffff;
  padding: 1.5rem;
  position: relative;
  z-index: 1;
}

.material-card h4 {
  margin: 0;
  color: #ffffff;
  font-size: 1rem;
  font-weight: 500;
  letter-spacing: 0.05em;
  line-height: 1.4;
  text-transform: uppercase;
}

.card-content {
  padding: 1.5rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  background: #ffffff;
}

.material-card p {
  font-size: 0.9rem;
  color: #000000;
  margin: 0 0 1.5rem 0;
  flex-grow: 1;
  line-height: 1.6;
  font-weight: 300;
}

.button-group {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0;
  margin-top: auto;
}

.btn-small {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem;
  background: #ffffff;
  color: #000000 !important;
  text-decoration: none;
  border: 2px solid #000000;
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  transition: all 0.2s ease;
  position: relative;
  overflow: hidden;
}

.btn-small::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  transition: left 0.3s ease;
}

/* Color the PDF button with category color */
.category-mikro .btn-small:first-child::before {
  background: #e63946;
}

.category-makro .btn-small:first-child::before {
  background: #457b9d;
}

.category-klausur .btn-small:first-child::before {
  background: #000000;
}

.btn-small:hover::before {
  left: 0;
}

.btn-small:hover {
  color: #ffffff !important;
  position: relative;
  z-index: 1;
}

.btn-small span {
  position: relative;
  z-index: 2;
}

.btn-quiz {
  background: #f5f5f5;
  border-left: none;
}

.btn-quiz::before {
  background: #000000;
}

.section-header {
  position: relative;
  padding: 1rem 1.5rem;
  margin: 4rem 0 2rem 0;
  color: #ffffff;
  font-weight: 500;
  font-size: 1.1rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  background: #000000;
  display: inline-block;
  clip-path: polygon(0 0, calc(100% - 20px) 0, 100% 50%, calc(100% - 20px) 100%, 0 100%);
  padding-right: 2.5rem;
}

/* Add geometric shapes to section headers */
.section-header::after {
  content: '';
  position: absolute;
  right: -40px;
  top: 50%;
  transform: translateY(-50%);
  width: 30px;
  height: 30px;
  border: 3px solid #000000;
}

.materials-grid.category-mikro + h2.section-header::after,
h2.section-header:nth-of-type(1)::after {
  background: #e63946;
  border-radius: 50%;
}

.materials-grid.category-makro + h2.section-header::after,
h2.section-header:nth-of-type(2)::after {
  background: #457b9d;
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  border-radius: 0;
}

.materials-grid.category-klausur + h2.section-header::after,
h2.section-header:nth-of-type(3)::after {
  background: #000000;
  clip-path: polygon(50% 0%, 100% 100%, 0% 100%);
  border-radius: 0;
}

.page-header {
  background: #000000;
  color: white;
  padding: 3rem 2rem;
  margin: -2rem -2rem 3rem -2rem;
  position: relative;
  overflow: hidden;
}

/* Geometric background elements */
.page-header::before {
  content: '';
  position: absolute;
  top: 20px;
  right: 20px;
  width: 80px;
  height: 80px;
  background: #e63946;
  border-radius: 50%;
  opacity: 0.8;
}

.page-header::after {
  content: '';
  position: absolute;
  bottom: 20px;
  right: 120px;
  width: 60px;
  height: 60px;
  background: #457b9d;
  opacity: 0.8;
}

.page-header h1 {
  margin: 0;
  font-size: 2.5rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  position: relative;
  z-index: 1;
}

.back-link {
  display: inline-block;
  margin-top: 3rem;
  padding: 1rem 2.5rem;
  background: #000000;
  color: #ffffff !important;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.85rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  border: 3px solid #000000;
  position: relative;
  overflow: hidden;
}

.back-link::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: #e63946;
  transition: left 0.3s ease;
  z-index: -1;
}

.back-link:hover::before {
  left: 0;
}

.back-link:hover {
  border-color: #e63946;
}

/* Bauhaus geometric decorations */
.materials-grid::before {
  content: '';
  position: fixed;
  bottom: 40px;
  left: 40px;
  width: 100px;
  height: 100px;
  border: 4px solid #457b9d;
  border-radius: 50%;
  opacity: 0.15;
  pointer-events: none;
  z-index: -1;
}

@media (max-width: 768px) {
  .materials-grid {
    grid-template-columns: 1fr;
  }
  
  .page-header {
    margin: -1rem -1rem 2rem -1rem;
    padding: 2rem 1.5rem;
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
    font-size: 0.9rem;
    clip-path: none;
    display: block;
    padding-right: 1.5rem;
  }
  
  .section-header::after {
    display: none;
  }
}
</style>

<p class="intro-text">
Materialien zur Prüfungsvorbereitung am Studienkolleg Leipzig
</p>

<h2 class="section-header">Mikroökonomie</h2>
<div class="materials-grid category-mikro">
  <div class="material-card">
    <div class="card-header">
      <h4>Bedürfnis, Bedarf und Nachfrage</h4>
    </div>
    <div class="card-content">
      <p>Grundkonzepte der Wirtschaft: Definition und Unterscheidung von Bedürfnis, Bedarf und Nachfrage, Bedürfnisarten, Maslows Bedürfnispyramide mit praktischen Beispielen</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_1-3.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Güterarten in der Wirtschaft</h4>
    </div>
    <div class="card-content">
      <p>Freie und wirtschaftliche Güter, inferiore und superiore Güter, Einkommenselastizität der Nachfrage, meritorische und demeritorische Güter, staatliche Markteingriffe</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_2-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_gueterarten.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Angebot und Angebotskurve</h4>
    </div>
    <div class="card-content">
      <p>Das Marktmodell, Gesetz des Angebots, Angebotsfunktion, aggregiertes Marktangebot, Verschiebung vs. Bewegung auf der Angebotskurve, Einflussfaktoren</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_3-4.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_angebot.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Nachfrage und Nachfragekurve</h4>
    </div>
    <div class="card-content">
      <p>Gesetz der Nachfrage, Nachfragefunktion, aggregierte Marktnachfrage, Verschiebung der Nachfragekurve, Einflussfaktoren wie Einkommen, Präferenzen und Preise verwandter Güter</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_4-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_nachfrage.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Marktgleichgewicht</h4>
    </div>
    <div class="card-content">
      <p>Gleichgewichtspreis und -menge, Angebots- und Nachfrageüberhang, Anpassungsprozesse, Auswirkungen von Steuern und Subventionen, praktische Beispiele und Berechnungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_5-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_marktgleichgewicht.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Konsumenten- und Produzentenrente</h4>
    </div>
    <div class="card-content">
      <p>Definition und Berechnung der Konsumenten- und Produzentenrente, ökonomische Wohlfahrt, Prohibitivpreis, graphische Darstellung, Beispielrechnungen am Smartwatch-Markt, Übungsaufgaben mit Lösungswegen</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_6.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_renten.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Marktformen: Monopol, Oligopol, Polypol</h4>
    </div>
    <div class="card-content">
      <p>Übersicht über Marktformen, Marktmacht, Marktstruktur, Vor- und Nachteile für Verbraucher, zahlreiche Beispiele und Übungsaufgaben zur Einordnung realer Märkte</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_7.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_marktformen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Die Budgetgerade – Konsumentscheidungen des Haushalts</h4>
    </div>
    <div class="card-content">
      <p>Mathematische Grundlagen der Konsumentscheidung: Budgetrestriktion, Gleichung und graphische Darstellung der Budgetgerade, Einkommens- und Preisänderungen, Opportunitätskosten sowie zahlreiche Übungsaufgaben mit Lösungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/WS_VWL_8-3.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_budgetgerade.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
</div>

<h2 class="section-header">Makroökonomie</h2>
<div class="materials-grid category-makro">
  <div class="material-card">
    <div class="card-header">
      <h4>Volkswirtschaftliche Gesamtrechnung</h4>
    </div>
    <div class="card-content">
      <p>Systematische Erfassung wirtschaftlicher Aktivitäten: Definition und Ziele der VGR, Bruttoinlandsprodukt (BIP), drei Berechnungsmethoden (Entstehung, Verwendung, Verteilung), Inlandsprinzip vs. Inländerprinzip, Vermeidung von Doppelzählung, praktische Beispiele und Übungsaufgaben</p>
      <div class="button-group">
        <a href="/assets/pdfs/VWL_11.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_vgr.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
</div>

<h2 class="section-header">Klausuraufgaben</h2>
<div class="materials-grid category-klausur">
  <div class="material-card">
    <div class="card-header">
      <h4>Klausuraufgaben Mikroökonomie</h4>
    </div>
    <div class="card-content">
      <p>Umfangreiche Sammlung von Übungsaufgaben zur Prüfungsvorbereitung: Bedürfnis und Nachfrage, Güterarten, Einkommenselastizität, Angebots- und Nachfragefunktionen, Marktgleichgewicht, Steuern und Subventionen, Konsumenten- und Produzentenrente</p>
      <div class="button-group">
        <a href="/assets/pdfs/VWL_Klausuren_Gesamt.pdf" class="btn-small"><span>PDF</span></a>
      </div>
    </div>
  </div>
</div>

<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>