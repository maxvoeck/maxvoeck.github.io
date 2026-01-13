---
layout: page
title: Mathematik
permalink: /teaching/mathematik/
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
.category-vektor .material-card {
  border-top: 8px solid #e63946; /* Red */
}

.category-algebra .material-card {
  border-top: 8px solid #f4d03f; /* Yellow */
}

.category-differential .material-card {
  border-top: 8px solid #457b9d; /* Blue */
}

.category-integral .material-card {
  border-top: 8px solid #000000; /* Black */
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

.category-vektor .material-card::before {
  background: #e63946;
  clip-path: polygon(100% 0, 100% 100%, 0 0);
}

.category-algebra .material-card::before {
  background: #f4d03f;
  clip-path: polygon(100% 0, 100% 100%, 0 0);
}

.category-differential .material-card::before {
  background: #457b9d;
  clip-path: polygon(100% 0, 100% 100%, 0 0);
}

.category-integral .material-card::before {
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
.category-vektor .btn-small:first-child::before {
  background: #e63946;
}

.category-algebra .btn-small:first-child::before {
  background: #f4d03f;
}

.category-differential .btn-small:first-child::before {
  background: #457b9d;
}

.category-integral .btn-small:first-child::before {
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

.materials-grid.category-vektor + h2.section-header::after,
h2.section-header:nth-of-type(1)::after {
  background: #e63946;
  border-radius: 50%;
}

.materials-grid.category-algebra + h2.section-header::after,
h2.section-header:nth-of-type(2)::after {
  background: #f4d03f;
  border-radius: 0;
}

.materials-grid.category-differential + h2.section-header::after,
h2.section-header:nth-of-type(3)::after {
  background: #457b9d;
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  border-radius: 0;
}

.materials-grid.category-integral + h2.section-header::after,
h2.section-header:nth-of-type(4)::after {
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
  background: #f4d03f;
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

.materials-grid.category-algebra::after {
  content: '';
  position: fixed;
  top: 200px;
  right: 60px;
  width: 80px;
  height: 80px;
  background: #f4d03f;
  opacity: 0.1;
  pointer-events: none;
  z-index: -1;
  transform: rotate(45deg);
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