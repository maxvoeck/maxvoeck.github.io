---
layout: page
title: Mathematik
permalink: /teaching/mathematik/
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

/* Remove category colors for minimalist approach */
.category-vektor .material-card::after {
  background: #1a1a1a;
}

.category-algebra .material-card::after {
  background: #1a1a1a;
}

.category-differential .material-card::after {
  background: #1a1a1a;
}

.category-integral .material-card::after {
  background: #1a1a1a;
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
 Materialien zur Prüfungsvorbereitung am Studienkolleg
</p>

<h2 class="section-header">Vektorrechnung und Analytische Geometrie</h2>
<div class="materials-grid category-vektor">
  <div class="material-card">
    <h4>Vektorrechnung – Grundlagen</h4>
    <p>Einführung in Vektoren, Koordinatensysteme, Skalare vs. vektorielle Größen, Betrag, Einheitsvektoren, Basisvektoren und Grundoperationen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Geo_2_1-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Vektorprodukt und Spatprodukt</h4>
    <p>Kreuzprodukt, geometrische Bedeutung, Flächenberechnung, Spatprodukt, Volumenberechnung und Anwendungen in der Raumgeometrie</p>
    <div class="button-group">
      <a href="/assets/pdfs/Geo_2_2-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_vektorprodukt.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Geraden und Ebenen im Raum</h4>
    <p>Parametergleichungen von Geraden und Ebenen, Normalenvektor, Koordinatenform, Lagebeziehungen und Schnittwinkelberechnung</p>
    <div class="button-group">
      <a href="/assets/pdfs/Geo_2_3.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Lagebeziehungen und Abstände</h4>
    <p>Ebene-Ebene-Lagen, Abstandsberechnungen zwischen Punkten, Geraden und Ebenen, Hessesche Normalenform und praktische Anwendungen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Geo_2_4.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
</div>

<h2 class="section-header">Lineare Algebra</h2>
<div class="materials-grid category-algebra">
  <div class="material-card">
    <h4>Matrizen – Einführung und Rechenoperationen</h4>
    <p>Grundlagen der Matrizenrechnung: Addition, Multiplikation, Transponieren, spezielle Matrizen und Rechenregeln mit praktischen Beispielen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Matrizen_2_1-5.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Determinanten – Grundlagen und Rechenregeln</h4>
    <p>Determinantenberechnung, Laplace-Entwicklung, Sarrus-Regel, reguläre/singuläre Matrizen, geometrische Bedeutung und Inverse Matrizen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Matrizen_2_2-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_determinanten.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Matrizengleichungen – Übungsaufgaben</h4>
    <p>Umfangreiche Übungsaufgaben zu Matrizengleichungen, Rangbestimmung, Gauß-Elimination und Lösungsstrategien für verschiedene Matrixgrößen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Matrizen_2_3-3.pdf" class="btn-small">PDF öffnen</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Lineare Gleichungssysteme – Grundlagen</h4>
    <p>Einführung in LGS, Matrixschreibweise, Gauß-Algorithmus, Lösbarkeitskriterien und praktische Anwendungen in Ingenieurwesen und Wirtschaft</p>
    <div class="button-group">
      <a href="/assets/pdfs/LGS_2_1-5.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Lineare Gleichungssysteme – Parameterabhängigkeit</h4>
    <p>Untersuchung von LGS mit Parametern, Determinantentest, Fallunterscheidungen und Lösbarkeitsanalyse für verschiedene Parameterwerte</p>
    <div class="button-group">
      <a href="/assets/pdfs/LGS_2_2-2.pdf" class="btn-small">PDF öffnen</a>
    </div>
  </div>
</div>

<h2 class="section-header">Differentialrechnung</h2>
<div class="materials-grid category-differential">
  <div class="material-card">
    <h4>Zahlenfolgen – Grundlagen</h4>
    <p>Explizite und rekursive Bildungsvorschriften, Beschränktheit, Monotonie, arithmetische und geometrische Folgen mit Summenformeln</p>
    <div class="button-group">
      <a href="/assets/pdfs/Folgen_2_1-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Grenzwerte von Zahlenfolgen</h4>
    <p>Konvergenz und Divergenz, Nullfolgen, Grenzwertsätze, Eulersche Zahl e und Methoden zur Grenzwertbestimmung.           </p>
    <div class="button-group">
      <a href="/assets/pdfs/Grenzwerte_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Grenzwerte von Funktionen – Verhalten im Unendlichen</h4>
    <p>Einführung in Grenzwerte von Funktionen, Verhalten für x → ±∞, Dominanzprinzip, waagerechte Asymptoten und typische Aufgabentypen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Funktion_2_2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Grenzwerte von Funktionen – Grenzwerte an einer Stelle</h4>
    <p>Grenzwerte an festen Stellen, Unstetigkeitsarten, einseitige Grenzwerte, Polstellen, hebbare Lücken und Asymptoten. Mit vielen Beispielen und Übungen.</p>
    <div class="button-group">
      <a href="/assets/pdfs/Grenzwerte_2_2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Grenzwerte von Funktionen – Asymptoten & Polynomdivision</h4>
    <p>Waagerechte, senkrechte und schräge Asymptoten, Polynomdivision zur Bestimmung des Funktionsverhaltens im Unendlichen, vollständige Funktionsanalyse.</p>
    <div class="button-group">
      <a href="/assets/pdfs/Grenzwerte_2_3.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_asymptoten.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Wie steil ist eine Funktion?</h4>
    <p>Einführung in die Differentialrechnung: Steigung linearer und nicht-linearer Funktionen, Sekanten und Tangenten, Definition der Ableitung, Differenzierbarkeit und Tangentengleichungen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Funktion_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Ableitungsregeln – Produkt-, Quotienten- und Kettenregel</h4>
    <p>Systematische Einführung in alle wichtigen Ableitungsregeln: Potenz-, Summen-, Produkt-, Quotienten- und Kettenregel. Mit vielen Beispielen, typischen Prüfungsaufgaben und Übungen.</p>
    <div class="button-group">
      <a href="/assets/pdfs/Funktion_2_4.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Die Regel von de L'Hospital</h4>
    <p>Systematische Methode zur Berechnung unbestimmter Ausdrücke: Typen 0/0, ∞/∞, ∞·0, ∞-∞, 0⁰, ∞⁰, 1∞. Mit Anwendungsbeispielen, Übungen und wichtigen Grenzwerten.</p>
    <div class="button-group">
      <a href="/assets/pdfs/Hospital_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_hospital.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Extrempunkte</h4>
    <p>Definition von Extremstellen, notwendige und hinreichende Bedingungen, zweite Ableitung, systematische Bestimmung von Hoch- und Tiefpunkten, Sattelpunkte erkennen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Extremwert_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_extrempunkte.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>

  <div class="material-card">
    <h4>Wendepunkte</h4>
    <p>Definition von Wendepunkten, Krümmungswechsel, notwendige und hinreichende Bedingungen, dritte Ableitung, Sattelpunkte erkennen, Links-Rechts- und Rechts-Links-Wendepunkte</p>
    <div class="button-group">
      <a href="/assets/pdfs/Wendepunkt_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_wendepunkte.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
  <h4>Kurvendiskussion</h4>
  <p>Systematische Funktionsanalyse: Definitionsbereich, Symmetrie, Grenzwerte, Asymptoten, Nullstellen, Extrempunkte, Wendepunkte. Mit vollständigen Beispielen und Zeichenkonventionen</p>
  <div class="button-group">
    <a href="/assets/pdfs/Kurvendiskusion_2_1.pdf" class="btn-small">PDF öffnen</a>
    <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="btn-small btn-quiz">Quiz starten</a>
  </div>
</div>

  <div class="material-card">
    <h4>Extremwertaufgaben</h4>
    <p>Systematisches Lösen von Optimierungsproblemen: Haupt- und Nebenbedingungen, Zielfunktionen, Kurvendiskussion mit Beispielen aus Technik und Wirtschaft</p>
    <div class="button-group">
      <a href="/assets/pdfs/Extrem_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
</div>

<h2 class="section-header">Integralrechnung</h2>
<div class="materials-grid category-integral">
  <div class="material-card">
    <h4>Einführung</h4>
    <p>Stammfunktionen, Grundintegrale, Faktor- und Summenregel, bestimmtes Integral</p>
    <div class="button-group">
      <a href="/assets/pdfs/Integral_2_1.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Integrationsmethoden</h4> 
    <p>Substitution, partielle Integration, LIATE-Regel, Partialbruchzerlegung</p>
    <div class="button-group">
      <a href="/assets/pdfs/Integral_2_2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Hauptsatz & Flächen</h4>
    <p>Hauptsatz, bestimmte Integrale, Flächenberechnung zwischen Graphen</p>
    <div class="button-group">
      <a href="/assets/pdfs/Integral_2_3.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
  
  <div class="material-card">
    <h4>Flächenberechnung & Rotationsvolumen</h4>
    <p>Flächenberechnung mit komplexeren Funktionen, Volumen von Rotationskörpern um x- und y-Achse</p>
    <div class="button-group">
      <a href="/assets/pdfs/Intergal_2_4-2.pdf" class="btn-small">PDF öffnen</a>
      <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="btn-small btn-quiz">Quiz starten</a>
    </div>
  </div>
</div>

<a href="/teaching/" class="back-link">← Zurück zur Übersicht</a>