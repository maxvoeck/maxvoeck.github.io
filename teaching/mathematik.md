---
layout: page
title: Mathematik
permalink: /teaching/mathematik/
---

<style>
/* Warme, moderne Lernumgebung mit Erdtönen */

body {
  background: linear-gradient(to bottom, #f9f7f4 0%, #fefdfb 100%);
  font-family: -apple-system, BlinkMacSystemFont, "Inter", "Segoe UI", "Helvetica Neue", Arial, sans-serif;
  line-height: 1.65;
}

.intro-text {
  font-size: 1.05rem;
  color: #5d5349;
  font-weight: 400;
  margin-bottom: 3rem;
  padding: 1.75rem 2rem;
  background: linear-gradient(135deg, #ffffff 0%, #faf8f5 100%);
  border-radius: 20px;
  border-left: 5px solid #c8956e;
  box-shadow: 0 4px 20px rgba(139, 102, 74, 0.08);
}

.materials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.material-card {
  background: #ffffff;
  border: none;
  border-radius: 20px;
  padding: 0;
  transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
  display: flex;
  flex-direction: column;
  min-height: 300px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(93, 83, 73, 0.08);
}

/* Warme Erdtöne für Kategorien */
.category-vektor .material-card {
  background: linear-gradient(to bottom, #ffffff 0%, #fff9f5 100%);
}

.category-algebra .material-card {
  background: linear-gradient(to bottom, #ffffff 0%, #fffbf2 100%);
}

.category-differential .material-card {
  background: linear-gradient(to bottom, #ffffff 0%, #f5f9f7 100%);
}

.category-integral .material-card {
  background: linear-gradient(to bottom, #ffffff 0%, #faf7f2 100%);
}

/* Organische Akzente */
.material-card::before {
  content: '';
  position: absolute;
  top: -20px;
  right: -20px;
  width: 120px;
  height: 120px;
  border-radius: 50%;
  opacity: 0.06;
  transition: all 0.35s ease;
}

.category-vektor .material-card::before {
  background: radial-gradient(circle, #d4836f 0%, transparent 70%);
}

.category-algebra .material-card::before {
  background: radial-gradient(circle, #e6b36a 0%, transparent 70%);
}

.category-differential .material-card::before {
  background: radial-gradient(circle, #7ba68d 0%, transparent 70%);
}

.category-integral .material-card::before {
  background: radial-gradient(circle, #c8956e 0%, transparent 70%);
}

/* Cover-Effekt beim Hover */
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
  transition: opacity 0.35s ease;
  z-index: 0;
}

.category-vektor .material-card::after {
  background: linear-gradient(135deg, rgba(212, 131, 111, 0.08) 0%, rgba(230, 166, 144, 0.05) 100%);
}

.category-algebra .material-card::after {
  background: linear-gradient(135deg, rgba(230, 179, 106, 0.08) 0%, rgba(240, 200, 134, 0.05) 100%);
}

.category-differential .material-card::after {
  background: linear-gradient(135deg, rgba(123, 166, 141, 0.08) 0%, rgba(155, 186, 167, 0.05) 100%);
}

.category-integral .material-card::after {
  background: linear-gradient(135deg, rgba(200, 149, 110, 0.08) 0%, rgba(217, 171, 136, 0.05) 100%);
}

.material-card:hover::after {
  opacity: 1;
}

.material-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 32px rgba(93, 83, 73, 0.15);
}

.material-card:hover::before {
  opacity: 0.12;
  transform: scale(1.3);
}

.card-header {
  padding: 2rem 1.75rem 1rem 1.75rem;
  position: relative;
  z-index: 2;
}

.material-card h4 {
  margin: 0;
  color: #3a342e;
  font-size: 1.15rem;
  font-weight: 600;
  line-height: 1.5;
  letter-spacing: -0.01em;
}

.card-content {
  padding: 0 1.75rem 1.75rem 1.75rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  position: relative;
  z-index: 2;
}

.material-card p {
  font-size: 0.93rem;
  color: #5d5349;
  margin: 0 0 1.75rem 0;
  flex-grow: 1;
  line-height: 1.7;
  font-weight: 400;
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
  padding: 1rem 1.25rem;
  background: #faf8f5;
  color: #5d5349 !important;
  text-decoration: none;
  border: 2px solid rgba(200, 149, 110, 0.2);
  border-radius: 14px;
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 0.01em;
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

/* Warme Hover-Farben passend zu Kategorien */
.category-vektor .btn-small:first-child::before {
  background: linear-gradient(135deg, #d4836f 0%, #e6a690 100%);
}

.category-algebra .btn-small:first-child::before {
  background: linear-gradient(135deg, #e6b36a 0%, #f0c886 100%);
}

.category-differential .btn-small:first-child::before {
  background: linear-gradient(135deg, #7ba68d 0%, #9bbaa7 100%);
}

.category-integral .btn-small:first-child::before {
  background: linear-gradient(135deg, #c8956e 0%, #d9ab88 100%);
}

.btn-small:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(93, 83, 73, 0.12);
  border-color: transparent;
  color: #ffffff !important;
}

.btn-small:hover::before {
  opacity: 1;
}

.btn-small span {
  position: relative;
  z-index: 2;
  transition: color 0.3s ease;
}

.btn-quiz {
  background: #ffffff;
  border-color: rgba(200, 149, 110, 0.15);
}

.btn-quiz::before {
  background: linear-gradient(135deg, #5d5349 0%, #756b61 100%);
}

.section-header {
  position: relative;
  padding: 0.75rem 0 0.75rem 1.5rem;
  margin: 4rem 0 2rem 0;
  color: #3a342e;
  font-weight: 600;
  font-size: 1.4rem;
  letter-spacing: -0.02em;
  display: inline-block;
  border-left: 5px solid;
  border-radius: 0 8px 8px 0;
}

.section-header::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 5px;
  border-radius: 8px 0 0 8px;
}

/* Farbcodierung der Section-Header mit Erdtönen */
h2.section-header:nth-of-type(1) {
  border-left-color: #d4836f;
  color: #d4836f;
}

h2.section-header:nth-of-type(2) {
  border-left-color: #e6b36a;
  color: #e6b36a;
}

h2.section-header:nth-of-type(3) {
  border-left-color: #7ba68d;
  color: #7ba68d;
}

h2.section-header:nth-of-type(4) {
  border-left-color: #c8956e;
  color: #c8956e;
}

.page-header {
  background: linear-gradient(135deg, #faf8f5 0%, #ffffff 100%);
  color: #3a342e;
  padding: 3.5rem 2.5rem;
  margin: -2rem -2rem 3.5rem -2rem;
  position: relative;
  overflow: hidden;
  border-radius: 0 0 32px 32px;
  box-shadow: 0 4px 24px rgba(93, 83, 73, 0.08);
}

/* Organische dekorative Elemente */
.page-header::before {
  content: '';
  position: absolute;
  top: -60px;
  right: -40px;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(200, 149, 110, 0.15) 0%, transparent 70%);
  border-radius: 50%;
}

.page-header::after {
  content: '';
  position: absolute;
  bottom: -80px;
  right: 180px;
  width: 240px;
  height: 240px;
  background: radial-gradient(circle, rgba(123, 166, 141, 0.12) 0%, transparent 70%);
  border-radius: 50%;
}

.page-header h1 {
  margin: 0;
  font-size: 2.75rem;
  font-weight: 700;
  letter-spacing: -0.03em;
  position: relative;
  z-index: 1;
  color: #3a342e;
}

.back-link {
  display: inline-block;
  margin-top: 3.5rem;
  padding: 1rem 2.5rem;
  background: #ffffff;
  color: #5d5349 !important;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.95rem;
  letter-spacing: 0.01em;
  transition: all 0.3s ease;
  border: 2px solid rgba(200, 149, 110, 0.2);
  border-radius: 16px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 2px 12px rgba(93, 83, 73, 0.06);
}

.back-link::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #c8956e 0%, #d9ab88 100%);
  opacity: 0;
  transition: opacity 0.3s ease;
  z-index: -1;
}

.back-link:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 24px rgba(93, 83, 73, 0.15);
  border-color: transparent;
  color: #ffffff !important;
}

.back-link:hover::before {
  opacity: 1;
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
    font-size: 2rem;
  }
  
  .page-header::before,
  .page-header::after {
    display: none;
  }
  
  .material-card {
    min-height: auto;
  }
  
  .section-header {
    font-size: 1.2rem;
  }
  
  .intro-text {
    font-size: 0.95rem;
    padding: 1.5rem;
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