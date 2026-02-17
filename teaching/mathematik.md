---
layout: page
title:
permalink: /teaching/mathematik/
---

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Mathematik</h1>
    <p class="ma-hero-subtitle">25 Module und interaktive Tools für Vektoren, Algebra, Analysis und Integralrechnung</p>
    
    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 28 abgeschlossen</div>
    </div>
  </div>

  <!-- Algebra -->
  <div class="ma-section ma-section--algebra">
    <div class="ma-section-header">
      <div class="ma-section-icon">🔢</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Lineare Algebra</h2>
        <p class="ma-section-subtitle">5 Module · Matrizen, Determinanten & Gleichungssysteme</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="a1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Matrizen</h4>
        </div>
        <p>Addition, Multiplikation, Transponieren und spezielle Matrizen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Matrizen_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('a1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a2">
        <div class="ma-card-header">
          <span class="ma-card-number">02</span>
          <h4>Determinanten</h4>
        </div>
        <p>Laplace-Entwicklung, Sarrus-Regel und Inverse Matrizen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Matrizen_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_determinanten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('a2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a3">
        <div class="ma-card-header">
          <span class="ma-card-number">03</span>
          <h4>Matrizengleichungen</h4>
        </div>
        <p>Übungsaufgaben, Rangbestimmung und Gauß-Elimination</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Matrizen_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <button class="ma-check" onclick="toggleModule('a3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a4">
        <div class="ma-card-header">
          <span class="ma-card-number">04</span>
          <h4>Lineare Gleichungssysteme</h4>
        </div>
        <p>Matrixschreibweise, Gauß-Algorithmus und Lösbarkeitskriterien</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/LGS_2_1-5.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('a4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="a5">
        <div class="ma-card-header">
          <span class="ma-card-number">05</span>
          <h4>Parameterabhängigkeit</h4>
        </div>
        <p>LGS mit Parametern, Determinantentest und Fallunterscheidungen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/LGS_2_2-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <button class="ma-check" onclick="toggleModule('a5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- Vektorrechnung -->
  <div class="ma-section ma-section--vektor">
    <div class="ma-section-header">
      <div class="ma-section-icon">📐</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Vektorrechnung</h2>
        <p class="ma-section-subtitle">4 Module · Grundlagen bis Raumgeometrie</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="v1">
        <div class="ma-card-header">
          <span class="ma-card-number">06</span>
          <h4>Grundlagen</h4>
        </div>
        <p>Einführung in Vektoren, Koordinatensysteme, Betrag, Einheitsvektoren und Grundoperationen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_1-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="v2">
        <div class="ma-card-header">
          <span class="ma-card-number">07</span>
          <h4>Vektor- & Spatprodukt</h4>
        </div>
        <p>Kreuzprodukt, Flächenberechnung, Spatprodukt und Volumenberechnung im Raum</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_2-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vektorprodukt.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="v3">
        <div class="ma-card-header">
          <span class="ma-card-number">08</span>
          <h4>Geraden und Ebenen</h4>
        </div>
        <p>Parametergleichungen, Normalenvektor, Koordinatenform und Lagebeziehungen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="v4">
        <div class="ma-card-header">
          <span class="ma-card-number">09</span>
          <h4>Abstände und Lagen</h4>
        </div>
        <p>Abstandsberechnungen, Hessesche Normalenform und praktische Anwendungen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Geo_2_4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('v4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>
    </div>
  </div>

  

  <!-- Differentialrechnung -->
  <div class="ma-section ma-section--diff">
    <div class="ma-section-header">
      <div class="ma-section-icon">📉</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Differentialrechnung</h2>
        <p class="ma-section-subtitle">12 Module · Von Folgen bis Kurvendiskussion</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="d1">
        <div class="ma-card-header"><span class="ma-card-number">10</span><h4>Zahlenfolgen</h4></div>
        <p>Explizite und rekursive Vorschriften, Monotonie und Beschränktheit</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Folgen_2_1-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d1', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d2">
        <div class="ma-card-header"><span class="ma-card-number">11</span><h4>Grenzwerte von Folgen</h4></div>
        <p>Konvergenz, Divergenz, Grenzwertsätze und Eulersche Zahl</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Grenzwerte_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d2', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d3">
        <div class="ma-card-header"><span class="ma-card-number">12</span><h4>Grenzwerte im Unendlichen</h4></div>
        <p>Dominanzprinzip und waagerechte Asymptoten</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Funktion_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d3', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d4">
        <div class="ma-card-header"><span class="ma-card-number">13</span><h4>Grenzwerte an einer Stelle</h4></div>
        <p>Einseitige Grenzwerte, Polstellen und hebbare Lücken</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Grenzwerte_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d4', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d5">
        <div class="ma-card-header"><span class="ma-card-number">14</span><h4>Asymptoten</h4></div>
        <p>Waagerechte, senkrechte und schräge Asymptoten</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Grenzwerte_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_asymptoten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d5', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d6">
        <div class="ma-card-header"><span class="ma-card-number">15</span><h4>Steigung und Ableitung</h4></div>
        <p>Sekanten, Tangenten und Differenzierbarkeit</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Funktion_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d6', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d7">
        <div class="ma-card-header"><span class="ma-card-number">16</span><h4>Ableitungsregeln</h4></div>
        <p>Potenz-, Produkt-, Quotienten- und Kettenregel</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Funktion_2_4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d7', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d8">
        <div class="ma-card-header"><span class="ma-card-number">17</span><h4>Regel von de L'Hôpital</h4></div>
        <p>Unbestimmte Ausdrücke: 0/0, ∞/∞, ∞·0</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Hospital_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_hospital.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d8', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d9">
        <div class="ma-card-header"><span class="ma-card-number">18</span><h4>Extrempunkte</h4></div>
        <p>Notwendige und hinreichende Bedingungen, Sattelpunkte</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Extremwert_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_extrempunkte.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d9', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d10">
        <div class="ma-card-header"><span class="ma-card-number">19</span><h4>Wendepunkte</h4></div>
        <p>Krümmungswechsel und dritte Ableitung</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Wendepunkt_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_wendepunkte.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d10', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d11">
        <div class="ma-card-header"><span class="ma-card-number">20</span><h4>Kurvendiskussion</h4></div>
        <p>Systematische Funktionsanalyse mit allen Kriterien</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Kurvendiskusion_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d11', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="d12">
        <div class="ma-card-header"><span class="ma-card-number">21</span><h4>Extremwertaufgaben</h4></div>
        <p>Optimierungsprobleme mit Nebenbedingungen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Extrem_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('d12', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
    </div>
  </div>

  <!-- Integralrechnung -->
  <div class="ma-section ma-section--integral">
    <div class="ma-section-header">
      <div class="ma-section-icon">∫</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Integralrechnung</h2>
        <p class="ma-section-subtitle">4 Module · Stammfunktionen bis Rotationsvolumen</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" data-module="i1">
        <div class="ma-card-header"><span class="ma-card-number">22</span><h4>Einführung</h4></div>
        <p>Stammfunktionen, Grundintegrale und bestimmtes Integral</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Integral_2_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i1', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="i2">
        <div class="ma-card-header"><span class="ma-card-number">23</span><h4>Integrationsmethoden</h4></div>
        <p>Substitution, partielle Integration und Partialbruchzerlegung</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Integral_2_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i2', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="i3">
        <div class="ma-card-header"><span class="ma-card-number">24</span><h4>Hauptsatz & Flächen</h4></div>
        <p>HDI, bestimmte Integrale und Flächen zwischen Graphen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Integral_2_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i3', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="i4">
        <div class="ma-card-header"><span class="ma-card-number">25</span><h4>Rotationsvolumen</h4></div>
        <p>Volumen von Rotationskörpern um x- und y-Achse</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Intergal_2_4-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('i4', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
    </div>
  </div>

  <!-- Interaktive Tools -->
  <div class="ma-section ma-section--tools">
    <div class="ma-section-header">
      <div class="ma-section-icon">⚡</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Interaktive Tools</h2>
        <p class="ma-section-subtitle">3 Tools · Hands-on Mathematik</p>
      </div>
    </div>
    <div class="ma-grid ma-grid--tools">
      <div class="ma-card" data-module="t1">
        <div class="ma-tool-icon">📐</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T1</span>
          <h4>Tangenten-Explorer</h4>
        </div>
        <p>Interaktive Visualisierung von Tangenten und Ableitungen mit Live-Steigungsänderung</p>
        <div class="ma-actions">
          <a href="/assets/interactive/tangenten_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;" onclick="event.stopPropagation()">Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t1', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="t2">
        <div class="ma-tool-icon">🔷</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T2</span>
          <h4>3D-Vektor-Explorer</h4>
        </div>
        <p>Drehe und manipuliere Vektoren im 3D-Raum, visualisiere Produkte interaktiv</p>
        <div class="ma-actions">
          <a href="/assets/interactive/vektor_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;" onclick="event.stopPropagation()">Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t2', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>
      <div class="ma-card" data-module="t3">
        <div class="ma-tool-icon">🎯</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T3</span>
          <h4>Geraden & Ebenen</h4>
        </div>
        <p>Erkunde Lagebeziehungen im 3D-Raum: schneidend, parallel, windschief</p>
        <div class="ma-actions">
          <a href="/assets/interactive/geraden_ebenen_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;" onclick="event.stopPropagation()">Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t3', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>

      <div class="ma-card" data-module="t4">
        <div class="ma-tool-icon">🔲</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T4</span>
          <h4>Matrizen-Explorer</h4>
        </div>
        <p>Sieh, was eine Matrix geometrisch bewirkt: Transformationen, Determinante und Flächenfaktor live</p>
        <div class="ma-actions">
          <a href="/assets/interactive/matrizen_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;" onclick="event.stopPropagation()">Öffnen</a>
          <button class="ma-check" onclick="toggleModule('t4', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
        </div>
      </div>

      <div class="ma-card" data-module="t5">
<div class="ma-tool-icon">🧮</div>
<div class="ma-card-header" style="margin-bottom: var(--space-2);">
<span class="ma-card-number">T5</span>
<h4>Determinanten-Rechner</h4>
</div>
<p>Sarrus-Regel Schritt für Schritt animiert: 2×2 und 3×3 Determinanten visuell berechnen</p>
<div class="ma-actions">
<a href="/assets/interactive/determinanten_rechner.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;" onclick="event.stopPropagation()">Öffnen</a>
<button class="ma-check" onclick="toggleModule('t5', event)"><svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></button>
</div>
</div>
    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>28 Module</strong> 
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
      <button class="ma-btn ma-btn--ghost" onclick="resetProgress()">Zurücksetzen</button>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'math-progress-v2';
const TOTAL_MODULES = 28;
const CIRCUMFERENCE = 339.292; // 2 * PI * 54

function getProgress() {
  try {
    return JSON.parse(localStorage.getItem(STORAGE_KEY)) || {};
  } catch {
    return {};
  }
}

function saveProgress(progress) {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(progress));
}

function updateUI() {
  const progress = getProgress();
  const completed = Object.keys(progress).length;
  const percentage = Math.round((completed / TOTAL_MODULES) * 100);
  
  // Update ring
  const offset = CIRCUMFERENCE - (percentage / 100) * CIRCUMFERENCE;
  document.getElementById('progressRing').style.strokeDashoffset = offset;
  document.getElementById('progressText').textContent = percentage + '%';
  document.getElementById('completedCount').textContent = completed;
  
  // Update cards
  document.querySelectorAll('.ma-card').forEach(card => {
    const moduleId = card.dataset.module;
    if (progress[moduleId]) {
      card.classList.add('ma-card-complete');
    } else {
      card.classList.remove('ma-card-complete');
    }
  });
}

function toggleModule(id, event) {
  // Nur den Check-Button-Click behandeln, nicht die Links
  if (event) {
    event.preventDefault();
    event.stopPropagation();
  }
  
  const progress = getProgress();
  if (progress[id]) {
    delete progress[id];
  } else {
    progress[id] = Date.now();
  }
  saveProgress(progress);
  updateUI();
}

function resetProgress() {
  if (confirm('Möchtest du wirklich deinen gesamten Fortschritt zurücksetzen?')) {
    localStorage.removeItem(STORAGE_KEY);
    updateUI();
  }
}

// Initialize
document.addEventListener('DOMContentLoaded', updateUI);
if (document.readyState !== 'loading') updateUI();
</script>