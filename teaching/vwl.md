---
layout: page
title: Volkswirtschaftslehre
permalink: /teaching/vwl/
---

<style>
body {
  background: #f5f5f4;
}

.materials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.material-card {
  border: none;
  border-radius: 8px;
  padding: 2rem;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  background: #fafaf9;
  display: flex;
  flex-direction: column;
  min-height: 240px;
  position: relative;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
}

.material-card::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 1px;
  background: #1a1a1a;
  transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.material-card:hover {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
  transform: translateY(-2px);
}

.material-card:hover::after {
  width: 100%;
}

.material-card h4 {
  margin-top: 0;
  color: #1a1a1a;
  font-size: 1rem;
  font-weight: 500;
  flex-shrink: 0;
  letter-spacing: 0.02em;
  transition: opacity 0.3s ease;
}

.material-card:hover h4 {
  opacity: 0.7;
}

.material-card p {
  font-size: 0.875rem;
  color: #666;
  margin: 1rem 0 1.5rem 0;
  flex-grow: 1;
  line-height: 1.7;
  font-weight: 300;
}

.btn-small {
  display: inline-block;
  padding: 0.5rem 1.2rem;
  background: transparent;
  color: #1a1a1a !important;
  text-decoration: none;
  border: 1px solid #1a1a1a;
  border-radius: 4px;
  font-size: 0.8rem;
  font-weight: 400;
  letter-spacing: 0.05em;
  transition: all 0.3s ease;
  margin-top: 0.5rem;
}

.btn-small:hover {
  background: #1a1a1a;
  color: white !important;
}

.btn-quiz {
  background: transparent;
  border: 1px solid #666;
  color: #666 !important;
  margin-left: 0.5rem;
}

.btn-quiz:hover {
  background: #666;
  color: white !important;
  border-color: #666;
}

.button-group {
  display: flex;
  gap: 0.5rem;
  flex-wrap: nowrap;
  margin-top: auto;
  padding-top: 0.5rem;
}

.section-header {
  border-bottom: 1px solid #1a1a1a;
  padding-bottom: 0.5rem;
  margin: 3rem 0 2rem 0;
  color: #1a1a1a;
  font-weight: 400;
  font-size: 1.1rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
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

.intro-text {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 2rem;
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
  
  .button-group {
    flex-wrap: wrap;
  }
  
  .btn-small {
    margin-left: 0 !important;
    flex: 1;
    min-width: calc(50% - 0.25rem);
  }
  
  .material-card {
    min-height: auto;
  }
}
</style>

<p class="intro-text">
Materialien zur Prüfungsvorbereitung am Studienkolleg Leipzig
</p>

<h2 class="section-header">Mikroökonomie</h2>
<div class="materials-grid">
  <div class="material-card">
    <h4>Bedürfnis, Bedarf und Nachfrage</h4>
    <p>Grundkonzepte der Wirtschaft: Definition und Unterscheidung von Bedürfnis, Bedarf und Nachfrage, Bedürfnisarten, Maslows Bedürfnispyramide mit praktischen Beispielen</p>
    <div class="button-group">
      <a href="/assets/pdfs/WS_VWL_1-3.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Güterarten in der Wirtschaft</h4>
    <p>Freie und wirtschaftliche Güter, inferiore und superiore Güter, Einkommenselastizität der Nachfrage, meritorische und demeritorische Güter, staatliche Markteingriffe</p>
    <div class="button-group">
      <a href="/assets/pdfs/WS_VWL_2-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_gueterarten.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Angebot und Angebotskurve</h4>
    <p>Das Marktmodell, Gesetz des Angebots, Angebotsfunktion, aggregiertes Marktangebot, Verschiebung vs. Bewegung auf der Angebotskurve, Einflussfaktoren</p>
    <div class="button-group">
      <a href="/assets/pdfs/WS_VWL_3-4.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_angebot.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Nachfragekurve und Nachfragefunktion</h4>
    <p>Gesetz der Nachfrage, Nachfragefunktion, aggregierte Marktnachfrage, Verschiebung der Nachfragekurve, Einflussfaktoren wie Einkommen, Präferenzen und Preise verwandter Güter</p>
    <div class="button-group">
      <a href="/assets/pdfs/WS_VWL_4-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_nachfrage.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Marktgleichgewicht und seine Dynamik</h4>
    <p>Gleichgewichtspreis und -menge, Angebots- und Nachfrageüberhang, Anpassungsprozesse, Auswirkungen von Steuern und Subventionen, praktische Beispiele und Berechnungen</p>
    <div class="button-group">
      <a href="/assets/pdfs/WS_VWL_5-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_marktgleichgewicht.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Konsumenten- und Produzentenrente</h4>
    <p>Definition und Berechnung der Konsumenten- und Produzentenrente, ökonomische Wohlfahrt, Prohibitivpreis, graphische Darstellung, Beispielrechnungen am Smartwatch-Markt, Übungsaufgaben mit Lösungswegen</p>
    <div class="button-group">
      <a href="/assets/pdfs/WS_VWL_6.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_renten.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
   <h4>Marktformen: Monopol, Oligopol, Polypol</h4>
   <p>Übersicht über Marktformen, Marktmacht, Marktstruktur, Vor- und Nachteile für Verbraucher, zahlreiche Beispiele und Übungsaufgaben zur Einordnung realer Märkte.</p>
   <div class="button-group">
     <a href="/assets/pdfs/WS_VWL_7.pdf" class="btn-small">PDF öffnen</a>
     <a href="/assets/quizzes/quiz_marktformen.html" class="btn-small btn-quiz">Quiz starten</a>
   </div>
  </div>
  
  <div class="material-card">
  <h4>Die Budgetgerade – Konsumentscheidungen des Haushalts</h4>
  <p>
    Mathematische Grundlagen der Konsumentscheidung:
    Budgetrestriktion, Gleichung und graphische Darstellung der Budgetgerade,
    Einkommens- und Preisänderungen, Opportunitätskosten sowie zahlreiche
    Übungsaufgaben mit Lösungen.
  </p>
  <div class="button-group">
    <a href="/assets/pdfs/WS_VWL_8-3.pdf" class="btn-small">PDF öffnen</a>
    <a href="/assets/quizzes/quiz_budgetgerade.html" class="btn-small btn-quiz">Quiz starten</a>
  </div>
</div>
</div>

<h2 class="section-header">Makroökonomie</h2>
<div class="materials-grid">
  <div class="material-card">
    <h4>Volkswirtschaftliche Gesamtrechnung (VGR)</h4>
    <p>Systematische Erfassung wirtschaftlicher Aktivitäten: Definition und Ziele der VGR, Bruttoinlandsprodukt (BIP), drei Berechnungsmethoden (Entstehung, Verwendung, Verteilung), Inlandsprinzip vs. Inländerprinzip, Vermeidung von Doppelzählung, praktische Beispiele und Übungsaufgaben</p>
    <div class="button-group">
      <a href="/assets/pdfs/VWL_11.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_vgr.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
</div>

<h2 class="section-header">Klausuraufgaben</h2>
<div class="materials-grid">
  <div class="material-card">
    <h4>Klausuraufgaben Mikroökonomie</h4>
    <p>Umfangreiche Sammlung von Übungsaufgaben zur Prüfungsvorbereitung: Bedürfnis und Nachfrage, Güterarten, Einkommenselastizität, Angebots- und Nachfragefunktionen, Marktgleichgewicht, Steuern und Subventionen, Konsumenten- und Produzentenrente </p>
    <div class="button-group">
      <a href="/assets/pdfs/VWL_Klausuren_Gesamt.pdf" class="btn-small">PDF öffnen</a>
    </div>
  </div>
</div>

<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>