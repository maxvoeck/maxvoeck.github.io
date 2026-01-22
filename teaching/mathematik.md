---
layout: page
title: 
permalink: /teaching/mathematik/
---

<style>
/* Apple Design - Modern Rounded Aesthetics */

body {
  background: #f5f5f7;
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", system-ui, sans-serif;
  line-height: 1.6;
  color: #1d1d1f;
}

.intro-text {
  font-size: 1rem;
  color: #6e6e73;
  font-weight: 400;
  margin-bottom: 3.5rem;
  padding: 2rem 2.5rem;
  background: #ffffff;
  border-radius: 18px;
  box-shadow: 0 2px 16px rgba(0, 0, 0, 0.06);
  letter-spacing: -0.01em;
}

.materials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 1.5rem;
  margin: 2.5rem 0;
}

.material-card {
  background: #ffffff;
  border-radius: 20px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  display: flex;
  flex-direction: column;
  min-height: 320px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
}

/* Moderne Farbakzente */
.category-vektor .material-card {
  background: linear-gradient(135deg, #ffffff 0%, #fdfcfb 100%);
  border: 1px solid rgba(184, 168, 154, 0.15);
}

.category-algebra .material-card {
  background: linear-gradient(135deg, #ffffff 0%, #fefdf9 100%);
  border: 1px solid rgba(201, 184, 150, 0.15);
}

.category-differential .material-card {
  background: linear-gradient(135deg, #ffffff 0%, #fbfcfd 100%);
  border: 1px solid rgba(139, 158, 159, 0.15);
}

.category-integral .material-card {
  background: linear-gradient(135deg, #ffffff 0%, #fcfcfb 100%);
  border: 1px solid rgba(164, 155, 142, 0.15);
}

/* Apple-Style Hover */
.material-card:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.category-vektor .material-card:hover {
  border-color: rgba(184, 168, 154, 0.3);
  box-shadow: 0 20px 40px rgba(184, 168, 154, 0.2);
}

.category-algebra .material-card:hover {
  border-color: rgba(201, 184, 150, 0.3);
  box-shadow: 0 20px 40px rgba(201, 184, 150, 0.2);
}

.category-differential .material-card:hover {
  border-color: rgba(139, 158, 159, 0.3);
  box-shadow: 0 20px 40px rgba(139, 158, 159, 0.2);
}

.category-integral .material-card:hover {
  border-color: rgba(164, 155, 142, 0.3);
  box-shadow: 0 20px 40px rgba(164, 155, 142, 0.2);
}

.card-header {
  padding: 2rem 2rem 1rem 2rem;
  position: relative;
  z-index: 2;
}

.material-card h4 {
  margin: 0;
  color: #1d1d1f;
  font-size: 1.125rem;
  font-weight: 600;
  line-height: 1.4;
  letter-spacing: -0.02em;
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
  padding: 1rem 2rem 2rem 2rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  position: relative;
  z-index: 2;
}

.material-card p {
  font-size: 0.9375rem;
  color: #6e6e73;
  margin: 0 0 2rem 0;
  flex-grow: 1;
  line-height: 1.6;
  font-weight: 400;
  letter-spacing: -0.01em;
}

.button-group {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.75rem;
  margin-top: auto;
}

.btn-small {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.875rem 1.25rem;
  background: #f5f5f7;
  color: #1d1d1f !important;
  text-decoration: none;
  border: none;
  border-radius: 12px;
  font-size: 0.875rem;
  font-weight: 500;
  letter-spacing: -0.01em;
  transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
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
  border-radius: 12px;
}

/* Gradient Hover für Primary Button */
.category-vektor .btn-small:first-child::before {
  background: linear-gradient(135deg, #b8a89a 0%, #cbbfb3 100%);
}

.category-algebra .btn-small:first-child::before {
  background: linear-gradient(135deg, #c9b896 0%, #d9ccad 100%);
}

.category-differential .btn-small:first-child::before {
  background: linear-gradient(135deg, #8b9e9f 0%, #a5b5b6 100%);
}

.category-integral .btn-small:first-child::before {
  background: linear-gradient(135deg, #a49b8e 0%, #b8afa4 100%);
}

.btn-small:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
  color: #ffffff !important;
}

.btn-small:hover::before {
  opacity: 1;
}

.btn-small:active {
  transform: scale(0.98);
}

.btn-small span {
  position: relative;
  z-index: 2;
}

.btn-quiz {
  background: #ffffff;
  border: 1px solid #e5e5e7;
}

.btn-quiz::before {
  background: linear-gradient(135deg, #6e6e73 0%, #8e8e93 100%);
}

.section-header {
  position: relative;
  padding: 1rem 1.5rem;
  margin: 4.5rem 0 2rem 0;
  font-weight: 600;
  font-size: 1.5rem;
  letter-spacing: -0.02em;
  display: inline-block;
  border-radius: 16px;
  background: #ffffff;
  box-shadow: 0 2px 12px rgba(0, 0, 0, 0.06);
}

/* Farbcodierung für Sections */
h2.section-header:nth-of-type(1) {
  color: #7d7169;
  border-left: 4px solid #b8a89a;
}

h2.section-header:nth-of-type(2) {
  color: #8d7f5e;
  border-left: 4px solid #c9b896;
}

h2.section-header:nth-of-type(3) {
  color: #5d6f70;
  border-left: 4px solid #8b9e9f;
}

h2.section-header:nth-of-type(4) {
  color: #706960;
  border-left: 4px solid #a49b8e;
}

.page-header {
  background: linear-gradient(135deg, #ffffff 0%, #f5f5f7 100%);
  color: #1d1d1f;
  padding: 4rem 2.5rem;
  margin: -2rem -2rem 4rem -2rem;
  position: relative;
  overflow: hidden;
  border-radius: 0 0 32px 32px;
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.06);
}

/* Moderne Dekoration */
.page-header::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -10%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(139, 158, 159, 0.08) 0%, transparent 70%);
  border-radius: 50%;
}

.page-header::after {
  content: '';
  position: absolute;
  bottom: -30%;
  right: 20%;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(184, 168, 154, 0.06) 0%, transparent 70%);
  border-radius: 50%;
}

.page-header h1 {
  margin: 0;
  font-size: 2.5rem;
  font-weight: 700;
  letter-spacing: -0.03em;
  position: relative;
  z-index: 1;
  color: #1d1d1f;
}

.back-link {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  margin-top: 4rem;
  padding: 1rem 2rem;
  background: #ffffff;
  color: #1d1d1f !important;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.9375rem;
  letter-spacing: -0.01em;
  transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  border-radius: 14px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

.back-link::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #8b9e9f 0%, #a5b5b6 100%);
  opacity: 0;
  transition: opacity 0.3s ease;
  z-index: -1;
  border-radius: 14px;
}

.back-link:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.15);
  color: #ffffff !important;
}

.back-link:hover::before {
  opacity: 1;
}

.back-link:active {
  transform: translateY(-2px);
}

/* Glassmorphism Effekt für moderne Optik */
@supports (backdrop-filter: blur(20px)) {
  .material-card {
    backdrop-filter: blur(20px);
  }
  
  .section-header {
    backdrop-filter: blur(10px);
  }
}

@media (max-width: 768px) {
  .materials-grid {
    grid-template-columns: 1fr;
    gap: 1.25rem;
  }
  
  .page-header {
    margin: -1rem -1rem 2.5rem -1rem;
    padding: 2.5rem 1.75rem;
    border-radius: 0 0 24px 24px;
  }
  
  .page-header h1 {
    font-size: 2rem;
  }
  
  .material-card {
    min-height: auto;
    border-radius: 16px;
  }
  
  .section-header {
    font-size: 1.25rem;
    border-radius: 12px;
    padding: 0.875rem 1.25rem;
  }
  
  .intro-text {
    font-size: 0.9375rem;
    padding: 1.5rem 1.75rem;
    border-radius: 16px;
  }
  
  .card-header {
    padding: 1.75rem 1.5rem 0.875rem 1.5rem;
  }
  
  .card-content {
    padding: 0.875rem 1.5rem 1.75rem 1.5rem;
  }
  
  .btn-small {
    border-radius: 10px;
    padding: 0.75rem 1rem;
  }
  
  .back-link {
    border-radius: 12px;
  }
}
</style>

<p class="intro-text">
 Materialien zur Prüfungsvorbereitung am Studienkolleg
</p>

<h2 class="section-header">Vektorrechnung und Analytische Geometrie</h2>
<div class="materials-grid category-vektor">
  <div class="material-card">
    <div class="card-header">
      <h4>Vektorrechnung – Grundlagen</h4>
    </div>
    <div class="card-content">
      <p>Einführung in Vektoren, Koordinatensysteme, Skalare vs. vektorielle Größen, Betrag, Einheitsvektoren, Basisvektoren und Grundoperationen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Geo_2_1-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Vektorprodukt und Spatprodukt</h4>
    </div>
    <div class="card-content">
      <p>Kreuzprodukt, geometrische Bedeutung, Flächenberechnung, Spatprodukt, Volumenberechnung und Anwendungen in der Raumgeometrie</p>
      <div class="button-group">
        <a href="/assets/pdfs/Geo_2_2-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_vektorprodukt.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Geraden und Ebenen im Raum</h4>
    </div>
    <div class="card-content">
      <p>Parametergleichungen von Geraden und Ebenen, Normalenvektor, Koordinatenform, Lagebeziehungen und Schnittwinkelberechnung</p>
      <div class="button-group">
        <a href="/assets/pdfs/Geo_2_3.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Lagebeziehungen und Abstände</h4>
    </div>
    <div class="card-content">
      <p>Ebene-Ebene-Lagen, Abstandsberechnungen zwischen Punkten, Geraden und Ebenen, Hessesche Normalenform und praktische Anwendungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Geo_2_4.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
</div>

<h2 class="section-header">Lineare Algebra</h2>
<div class="materials-grid category-algebra">
  <div class="material-card">
    <div class="card-header">
      <h4>Matrizen – Einführung und Rechenoperationen</h4>
    </div>
    <div class="card-content">
      <p>Grundlagen der Matrizenrechnung: Addition, Multiplikation, Transponieren, spezielle Matrizen und Rechenregeln mit praktischen Beispielen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Matrizen_2_1-5.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Determinanten – Grundlagen und Rechenregeln</h4>
    </div>
    <div class="card-content">
      <p>Determinantenberechnung, Laplace-Entwicklung, Sarrus-Regel, reguläre/singuläre Matrizen, geometrische Bedeutung und Inverse Matrizen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Matrizen_2_2-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_determinanten.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Matrizengleichungen – Übungsaufgaben</h4>
    </div>
    <div class="card-content">
      <p>Umfangreiche Übungsaufgaben zu Matrizengleichungen, Rangbestimmung, Gauß-Elimination und Lösungsstrategien für verschiedene Matrixgrößen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Matrizen_2_3-3.pdf" class="btn-small"><span>PDF</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Lineare Gleichungssysteme – Grundlagen</h4>
    </div>
    <div class="card-content">
      <p>Einführung in LGS, Matrixschreibweise, Gauß-Algorithmus, Lösbarkeitskriterien und praktische Anwendungen in Ingenieurwesen und Wirtschaft</p>
      <div class="button-group">
        <a href="/assets/pdfs/LGS_2_1-5.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Lineare Gleichungssysteme – Parameterabhängigkeit</h4>
    </div>
    <div class="card-content">
      <p>Untersuchung von LGS mit Parametern, Determinantentest, Fallunterscheidungen und Lösbarkeitsanalyse für verschiedene Parameterwerte</p>
      <div class="button-group">
        <a href="/assets/pdfs/LGS_2_2-2.pdf" class="btn-small"><span>PDF</span></a>
      </div>
    </div>
  </div>
</div>

<h2 class="section-header">Differentialrechnung</h2>
<div class="materials-grid category-differential">
  <div class="material-card">
    <div class="card-header">
      <h4>Zahlenfolgen – Grundlagen</h4>
    </div>
    <div class="card-content">
      <p>Explizite und rekursive Bildungsvorschriften, Beschränktheit, Monotonie, arithmetische und geometrische Folgen mit Summenformeln</p>
      <div class="button-group">
        <a href="/assets/pdfs/Folgen_2_1-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Grenzwerte von Zahlenfolgen</h4>
    </div>
    <div class="card-content">
      <p>Konvergenz und Divergenz, Nullfolgen, Grenzwertsätze, Eulersche Zahl e und Methoden zur Grenzwertbestimmung</p>
      <div class="button-group">
        <a href="/assets/pdfs/Grenzwerte_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Grenzwerte von Funktionen – Verhalten im Unendlichen</h4>
    </div>
    <div class="card-content">
      <p>Einführung in Grenzwerte von Funktionen, Verhalten für x → ±∞, Dominanzprinzip, waagerechte Asymptoten und typische Aufgabentypen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Funktion_2_2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Grenzwerte von Funktionen – Grenzwerte an einer Stelle</h4>
    </div>
    <div class="card-content">
      <p>Grenzwerte an festen Stellen, Unstetigkeitsarten, einseitige Grenzwerte, Polstellen, hebbare Lücken und Asymptoten. Mit vielen Beispielen und Übungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Grenzwerte_2_2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Grenzwerte von Funktionen – Asymptoten & Polynomdivision</h4>
    </div>
    <div class="card-content">
      <p>Waagerechte, senkrechte und schräge Asymptoten, Polynomdivision zur Bestimmung des Funktionsverhaltens im Unendlichen, vollständige Funktionsanalyse</p>
      <div class="button-group">
        <a href="/assets/pdfs/Grenzwerte_2_3.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_asymptoten.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Wie steil ist eine Funktion?</h4>
    </div>
    <div class="card-content">
      <p>Einführung in die Differentialrechnung: Steigung linearer und nicht-linearer Funktionen, Sekanten und Tangenten, Definition der Ableitung, Differenzierbarkeit und Tangentengleichungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Funktion_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Ableitungsregeln – Produkt-, Quotienten- und Kettenregel</h4>
    </div>
    <div class="card-content">
      <p>Systematische Einführung in alle wichtigen Ableitungsregeln: Potenz-, Summen-, Produkt-, Quotienten- und Kettenregel. Mit vielen Beispielen, typischen Prüfungsaufgaben und Übungen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Funktion_2_4.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Die Regel von de L'Hospital</h4>
    </div>
    <div class="card-content">
      <p>Systematische Methode zur Berechnung unbestimmter Ausdrücke: Typen 0/0, ∞/∞, ∞·0, ∞-∞, 0⁰, ∞⁰, 1∞. Mit Anwendungsbeispielen, Übungen und wichtigen Grenzwerten</p>
      <div class="button-group">
        <a href="/assets/pdfs/Hospital_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_hospital.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Extrempunkte</h4>
    </div>
    <div class="card-content">
      <p>Definition von Extremstellen, notwendige und hinreichende Bedingungen, zweite Ableitung, systematische Bestimmung von Hoch- und Tiefpunkten, Sattelpunkte erkennen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Extremwert_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_extrempunkte.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Wendepunkte</h4>
    </div>
    <div class="card-content">
      <p>Definition von Wendepunkten, Krümmungswechsel, notwendige und hinreichende Bedingungen, dritte Ableitung, Sattelpunkte erkennen, Links-Rechts- und Rechts-Links-Wendepunkte</p>
      <div class="button-group">
        <a href="/assets/pdfs/Wendepunkt_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_wendepunkte.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Kurvendiskussion</h4>
    </div>
    <div class="card-content">
      <p>Systematische Funktionsanalyse: Definitionsbereich, Symmetrie, Grenzwerte, Asymptoten, Nullstellen, Extrempunkte, Wendepunkte. Mit vollständigen Beispielen und Zeichenkonventionen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Kurvendiskusion_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>

  <div class="material-card">
    <div class="card-header">
      <h4>Extremwertaufgaben</h4>
    </div>
    <div class="card-content">
      <p>Systematisches Lösen von Optimierungsproblemen: Haupt- und Nebenbedingungen, Zielfunktionen, Kurvendiskussion mit Beispielen aus Technik und Wirtschaft</p>
      <div class="button-group">
        <a href="/assets/pdfs/Extrem_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
</div>

<h2 class="section-header">Integralrechnung</h2>
<div class="materials-grid category-integral">
  <div class="material-card">
    <div class="card-header">
      <h4>Einführung</h4>
    </div>
    <div class="card-content">
      <p>Stammfunktionen, Grundintegrale, Faktor- und Summenregel, bestimmtes Integral</p>
      <div class="button-group">
        <a href="/assets/pdfs/Integral_2_1.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Integrationsmethoden</h4>
    </div>
    <div class="card-content">
      <p>Substitution, partielle Integration, LIATE-Regel, Partialbruchzerlegung</p>
      <div class="button-group">
        <a href="/assets/pdfs/Integral_2_2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Hauptsatz & Flächen</h4>
    </div>
    <div class="card-content">
      <p>Hauptsatz, bestimmte Integrale, Flächenberechnung zwischen Graphen</p>
      <div class="button-group">
        <a href="/assets/pdfs/Integral_2_3.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
  
  <div class="material-card">
    <div class="card-header">
      <h4>Flächenberechnung & Rotationsvolumen</h4>
    </div>
    <div class="card-content">
      <p>Flächenberechnung mit komplexeren Funktionen, Volumen von Rotationskörpern um x- und y-Achse</p>
      <div class="button-group">
        <a href="/assets/pdfs/Intergal_2_4-2.pdf" class="btn-small"><span>PDF</span></a>
        <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="btn-small btn-quiz"><span>Quiz</span></a>
      </div>
    </div>
  </div>
</div>

<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>