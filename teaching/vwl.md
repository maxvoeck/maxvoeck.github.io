---
layout: page
title: 
permalink: /teaching/vwl/
---

<style>
/* Japandi Design mit Apple-Style Rounded Corners */

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
  border-radius: 18px;
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
  border-radius: 20px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  display: flex;
  flex-direction: column;
  min-height: 320px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

/* Dezente, natürliche Farbpalette */
.category-vektor .material-card {
  border-top: 2px solid #b8a89a;
}

.category-algebra .material-card {
  border-top: 2px solid #c9b896;
}

.category-differential .material-card {
  border-top: 2px solid #8b9e9f;
}

.category-integral .material-card {
  border-top: 2px solid #a49b8e;
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

.category-vektor .material-card::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.category-algebra .material-card::before {
  background: linear-gradient(to bottom, #c9b896, transparent);
}

.category-differential .material-card::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

.category-integral .material-card::before {
  background: linear-gradient(to bottom, #a49b8e, transparent);
}

/* Dezenter Cover-Effekt */
.material-card::after {
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

.category-vektor .material-card::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.category-algebra .material-card::after {
  background: linear-gradient(180deg, rgba(201, 184, 150, 0.04) 0%, rgba(201, 184, 150, 0.02) 100%);
}

.category-differential .material-card::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
}

.category-integral .material-card::after {
  background: linear-gradient(180deg, rgba(164, 155, 142, 0.04) 0%, rgba(164, 155, 142, 0.02) 100%);
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

/* Zusätzlicher Hover-Effekt - sanftes Glow */
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

.category-vektor .card-header::after {
  background: linear-gradient(90deg, #b8a89a 0%, transparent 100%);
}

.category-algebra .card-header::after {
  background: linear-gradient(90deg, #c9b896 0%, transparent 100%);
}

.category-differential .card-header::after {
  background: linear-gradient(90deg, #8b9e9f 0%, transparent 100%);
}

.category-integral .card-header::after {
  background: linear-gradient(90deg, #a49b8e 0%, transparent 100%);
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

.category-vektor .material-card:hover h4 {
  color: #b8a89a;
}

.category-algebra .material-card:hover h4 {
  color: #c9b896;
}

.category-differential .material-card:hover h4 {
  color: #8b9e9f;
}

.category-integral .material-card:hover h4 {
  color: #a49b8e;
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
  border-radius: 12px;
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

/* Dezente Hover-Farben */
.category-vektor .btn-small:first-child::before {
  background: linear-gradient(180deg, #b8a89a 0%, #cbbfb3 100%);
}

.category-algebra .btn-small:first-child::before {
  background: linear-gradient(180deg, #c9b896 0%, #d9ccad 100%);
}

.category-differential .btn-small:first-child::before {
  background: linear-gradient(180deg, #8b9e9f 0%, #a5b5b6 100%);
}

.category-integral .btn-small:first-child::before {
  background: linear-gradient(180deg, #a49b8e 0%, #b8afa4 100%);
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
  border-radius: 0 16px 16px 0;
}

/* Natürliche Farbcodierung */
h2.section-header:nth-of-type(1) {
  border-left-color: #b8a89a;
  color: #7d7169;
}

h2.section-header:nth-of-type(2) {
  border-left-color: #c9b896;
  color: #8d7f5e;
}

h2.section-header:nth-of-type(3) {
  border-left-color: #8b9e9f;
  color: #5d6f70;
}

h2.section-header:nth-of-type(4) {
  border-left-color: #a49b8e;
  color: #706960;
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
  border-radius: 14px;
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
    border-radius: 0 0 24px 24px;
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
    border-radius: 16px;
  }
  
  .material-card::after {
    border-radius: 16px;
  }
  
  .section-header {
    font-size: 1.1rem;
    border-radius: 0 12px 12px 0;
  }
  
  .intro-text {
    font-size: 0.9rem;
    padding: 1.5rem 1.75rem;
    border-radius: 16px;
  }
  
  .card-header {
    padding: 1.75rem 1.5rem 1rem 1.5rem;
  }
  
  .card-content {
    padding: 1.25rem 1.5rem 1.75rem 1.5rem;
  }
  
  .btn-small {
    border-radius: 10px;
  }
  
  .back-link {
    border-radius: 12px;
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
  
  <div class="material-card">
    <div class="card-header">
      <h4>VGR II: Nominales vs. reales BIP</h4>
    </div>
    <div class="card-content">
      <p>Unterschied zwischen nominalem und realem BIP, BIP-Deflator als Inflationsmaß, BIP pro Kopf und Kaufkraftbereinigung (PPP), Grenzen des BIP als Wohlstandsindikator, alternative Wohlstandsindikatoren (HDI, World Happiness Report, Gini-Koeffizient), umfangreiche Übungsaufgaben mit Lösungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/VWL_12.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_vgr2.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
  <div class="card-header">
    <h4>Konjunktur & Konjunkturzyklen</h4>
  </div>
  <div class="card-content">
    <p>Die 4 Konjunkturphasen (Aufschwung, Boom, Abschwung, Depression), BIP-Berechnung, Wachstumsraten, Rezessionsdefinition, Früh- und Spätindikatoren, wirtschaftspolitische Maßnahmen</p>
    <div class="button-group">
      <a href="/assets/pdfs/VWL_11_Konjunktur.pdf" class="btn-small"><span>PDF</span></a>
      <a href="/assets/quizzes/quiz_konjunktur.html" class="btn-small btn-quiz"><span>Quiz</span></a>
    </div>
  </div>
</div>


<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>