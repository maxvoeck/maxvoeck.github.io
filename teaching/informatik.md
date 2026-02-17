---
layout: page
title:
permalink: /teaching/informatik/
---

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Informatik</h1>
    <p class="ma-hero-subtitle">5 Module · Python-Programmierung von Grund auf</p>
    
    <div class="ma-progress-container">
      <div class="ma-progress-ring">
        <svg viewBox="0 0 120 120">
          <circle class="ma-progress-ring-bg" cx="60" cy="60" r="54"/>
          <circle class="ma-progress-ring-fill" id="progressRing" cx="60" cy="60" r="54"/>
        </svg>
        <div class="ma-progress-text" id="progressText">0%</div>
      </div>
      <div class="ma-progress-label"><span id="completedCount">0</span> von 5 abgeschlossen</div>
    </div>
  </div>

  <!-- Python -->
  <div class="ma-section ma-section--python">
    <div class="ma-section-header">
      <div class="ma-section-icon">🐍</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Python</h2>
        <p class="ma-section-subtitle">5 Module · Von print() bis Funktionen</p>
      </div>
    </div>
    <div class="ma-grid">

      <div class="ma-card" data-module="p1">
        <div class="ma-card-header">
          <span class="ma-card-number">01</span>
          <h4>Python Grundlagen – print() und input()</h4>
        </div>
        <p>Einführung in Python: Die print()-Funktion zur Ausgabe von Text und Zahlen, Parameter sep und end, input() für Benutzereingaben, Datentypen und Umwandlung</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_1.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_python_grundlage.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p1', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p2">
        <div class="ma-card-header">
          <span class="ma-card-number">02</span>
          <h4>Variablen und Datentypen</h4>
        </div>
        <p>Variablen erstellen und verwenden, Datentypen unterscheiden (str, int, float, bool), Rechenoperationen, Typkonvertierung, Namenskonventionen</p>
        <p class="ma-card-prereq">Baut auf: print() und input()</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_2.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_variablen_datentypen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p2', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p3">
        <div class="ma-card-header">
          <span class="ma-card-number">03</span>
          <h4>Listen und Datenstrukturen</h4>
        </div>
        <p>Erstellen und Verstehen von Listen, Zugriff über Index und Slicing, mutable Listen, append(), insert(), remove(), pop(), sort(), reverse()</p>
        <p class="ma-card-prereq">Baut auf: Variablen und Datentypen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_3.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_listen_datenstrukturen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p3', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p4">
        <div class="ma-card-header">
          <span class="ma-card-number">04</span>
          <h4>Kontrollstrukturen – if, for, while</h4>
        </div>
        <p>Bedingte Anweisungen mit if/elif/else, Vergleichs- und logische Operatoren, for-Schleifen, while-Schleifen, break und continue</p>
        <p class="ma-card-prereq">Baut auf: Listen und Datenstrukturen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_4.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_kontrollstrukturen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p4', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

      <div class="ma-card" data-module="p5">
        <div class="ma-card-header">
          <span class="ma-card-number">05</span>
          <h4>Funktionen in Python</h4>
        </div>
        <p>Funktionen definieren mit def, Parameter und Rückgabewerte, print vs. return, benannte Parameter und Standardwerte, Funktionen kombinieren</p>
        <p class="ma-card-prereq">Baut auf: Kontrollstrukturen</p>
        <div class="ma-actions">
          <a href="/assets/pdfs/Info_5.pdf" class="ma-btn ma-btn--secondary" onclick="event.stopPropagation()">PDF</a>
          <a href="/assets/quizzes/quiz_funktionen.html" class="ma-btn ma-btn--primary" onclick="event.stopPropagation()">Quiz</a>
          <button class="ma-check" onclick="toggleModule('p5', event)" aria-label="Als erledigt markieren">
            <svg viewBox="0 0 12 12" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>
          </button>
        </div>
      </div>

    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>5 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn ma-btn--secondary">← Übersicht</a>
      <button class="ma-btn ma-btn--ghost" onclick="resetProgress()">Zurücksetzen</button>
    </div>
  </div>

</div>

<script>
const STORAGE_KEY = 'info-progress';
const TOTAL_MODULES = 5;
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