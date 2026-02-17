---
layout: page
title:
permalink: /teaching/vwl/
---

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Volkswirtschaftslehre</h1>
    <p class="ma-hero-subtitle">13 Module für Mikroökonomie und Makroökonomie</p>
    
    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 13 abgeschlossen</div>
    </div>
  </div>

  <!-- Mikroökonomie -->
  <div class="ma-section ma-section--mikro">
    <div class="ma-section-header">
      <div class="ma-section-icon">📊</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Mikroökonomie</h2>
        <p class="ma-section-subtitle">8 Module · Vom Grundbegriff zum Marktmodell</p>
      </div>
    </div>
    <div class="ma-grid">

      <div class="ma-card" data-module="m1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Bedürfnis, Bedarf und Nachfrage</h4>
        </div>
        <p>Grundkonzepte der Wirtschaft: Definition und Unterscheidung von Bedürfnis, Bedarf und Nachfrage, Bedürfnisarten, Maslows Bedürfnispyramide</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_1-3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m2">
        <div class="ma-card-header">
          <span class="ma-card-number">02</span>
          <h4>Güterarten in der Wirtschaft</h4>
        </div>
        <p>Freie und wirtschaftliche Güter, inferiore und superiore Güter, Einkommenselastizität, meritorische und demeritorische Güter</p>
        <p class="ma-card-prereq">Baut auf: Bedürfnis, Bedarf und Nachfrage</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_2-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_gueterarten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m3">
        <div class="ma-card-header">
          <span class="ma-card-number">03</span>
          <h4>Angebot und Angebotskurve</h4>
        </div>
        <p>Gesetz des Angebots, Angebotsfunktion, aggregiertes Marktangebot, Verschiebung vs. Bewegung auf der Kurve</p>
        <p class="ma-card-prereq">Baut auf: Güterarten</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_3-4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_angebot.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m4">
        <div class="ma-card-header">
          <span class="ma-card-number">04</span>
          <h4>Nachfrage und Nachfragekurve</h4>
        </div>
        <p>Gesetz der Nachfrage, Nachfragefunktion, aggregierte Marktnachfrage, Einflussfaktoren wie Einkommen und Präferenzen</p>
        <p class="ma-card-prereq">Baut auf: Angebot und Angebotskurve</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_4-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_nachfrage.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m5">
        <div class="ma-card-header">
          <span class="ma-card-number">05</span>
          <h4>Marktgleichgewicht</h4>
        </div>
        <p>Gleichgewichtspreis und -menge, Angebots- und Nachfrageüberhang, Anpassungsprozesse, Steuern und Subventionen</p>
        <p class="ma-card-prereq">Baut auf: Angebot und Nachfrage</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_5-2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_marktgleichgewicht.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m6">
        <div class="ma-card-header">
          <span class="ma-card-number">06</span>
          <h4>Konsumenten- und Produzentenrente</h4>
        </div>
        <p>Definition und Berechnung der Renten, ökonomische Wohlfahrt, Prohibitivpreis, graphische Darstellung</p>
        <p class="ma-card-prereq">Baut auf: Marktgleichgewicht</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_6.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_renten.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m6', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m7">
        <div class="ma-card-header">
          <span class="ma-card-number">07</span>
          <h4>Marktformen</h4>
        </div>
        <p>Monopol, Oligopol, Polypol – Marktmacht, Marktstruktur, Vor- und Nachteile für Verbraucher</p>
        <p class="ma-card-prereq">Baut auf: Marktgleichgewicht</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_7.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_marktformen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m7', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m8">
        <div class="ma-card-header">
          <span class="ma-card-number">08</span>
          <h4>Budgetgerade</h4>
        </div>
        <p>Konsumentscheidungen: Budgetrestriktion, Gleichung und graphische Darstellung, Einkommens- und Preisänderungen, Opportunitätskosten</p>
        <p class="ma-card-prereq">Baut auf: Nachfrage und Güterarten</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/WS_VWL_8-3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_budgetgerade.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m8', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

    </div>
  </div>

  <!-- Makroökonomie -->
  <div class="ma-section ma-section--makro">
    <div class="ma-section-header">
      <div class="ma-section-icon">🌐</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Makroökonomie</h2>
        <p class="ma-section-subtitle">5 Module · Von der Gesamtrechnung zur Wirtschaftspolitik</p>
      </div>
    </div>
    <div class="ma-grid">

      <div class="ma-card" data-module="m9">
        <div class="ma-card-header">
          <span class="ma-card-number">09</span>
          <h4>Volkswirtschaftliche Gesamtrechnung</h4>
        </div>
        <p>Definition und Ziele der VGR, Bruttoinlandsprodukt, drei Berechnungsmethoden, Inlandsprinzip vs. Inländerprinzip</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_11.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vgr.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m9', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m10">
        <div class="ma-card-header">
          <span class="ma-card-number">10</span>
          <h4>Nominales vs. reales BIP</h4>
        </div>
        <p>BIP-Deflator, BIP pro Kopf und Kaufkraftbereinigung, Grenzen des BIP, alternative Indikatoren (HDI, Gini-Koeffizient)</p>
        <p class="ma-card-prereq">Baut auf: Volkswirtschaftliche Gesamtrechnung</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_12.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_vgr2.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m10', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m11">
        <div class="ma-card-header">
          <span class="ma-card-number">11</span>
          <h4>Konjunktur & Konjunkturzyklen</h4>
        </div>
        <p>Die 4 Konjunkturphasen, BIP-Berechnung, Wachstumsraten, Rezessionsdefinition, Früh- und Spätindikatoren</p>
        <p class="ma-card-prereq">Baut auf: Nominales vs. reales BIP</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_11_Konjunktur.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_konjunktur.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m11', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m12">
        <div class="ma-card-header">
          <span class="ma-card-number">12</span>
          <h4>Antizyklische Konjunkturpolitik</h4>
        </div>
        <p>Grundprinzipien antizyklischer Politik, Fiskal- und Geldpolitik, expansive vs. restriktive Maßnahmen, Finanzkrise 2008</p>
        <p class="ma-card-prereq">Baut auf: Konjunkturzyklen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/VWL_12_Konjunkturpolitik.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_konjunkturpolitik.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m12', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="m13">
        <div class="ma-card-header">
          <span class="ma-card-number">13</span>
          <h4>Arbeitslosigkeit & Arbeitsmarktpolitik</h4>
        </div>
        <p>Arbeitslosenquote, drei Arten der Arbeitslosigkeit, Okun's Gesetz, aktive vs. passive Arbeitsmarktpolitik</p>
        <p class="ma-card-prereq">Baut auf: Konjunktur und Konjunkturpolitik</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_arbeitslosigkeit.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('m13', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>13 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
      <button class="ma-btn ma-btn--ghost" onclick="resetProgress()">Zurücksetzen</button>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'vwl-progress';
const TOTAL_MODULES = 13;
const CIRCUMFERENCE = 339.292;

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
  
  const offset = CIRCUMFERENCE - (percentage / 100) * CIRCUMFERENCE;
  document.getElementById('progressRing').style.strokeDashoffset = offset;
  document.getElementById('progressText').textContent = percentage + '%';
  document.getElementById('completedCount').textContent = completed;
  
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

document.addEventListener('DOMContentLoaded', updateUI);
if (document.readyState !== 'loading') updateUI();
</script>