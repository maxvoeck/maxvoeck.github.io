---
layout: page
permalink: /chatbot/
title: Lernbaum
---

<style>
  .post-header, .page-heading, header.post-header {
    display: none !important;
  }

  @media (max-width: 600px) {
    .site-header {
      display: none !important;
    }
    .page-content {
      padding-top: 0 !important;
      margin-top: 0 !important;
    }
  }

  .tree-wrap {
    --sumi: #1a1a18;
    --kuro: #2c2c28;
    --hai: #3d3d38;
    --kinari: #f0ece4;
    --shiro: #f7f5f0;
    --kinu: #e8e3d8;
    --ishi: #b8b3a8;
    --sugi: #8a8578;
    --beni: #c45c3e;
    --matcha: #7a8c6e;
    --ai: #5b7a8c;
    --kitsune: #c49a6c;
    --sakura: #c4868a;
    --font-display: 'Cormorant Garamond', Georgia, serif;
    --font-body: 'Noto Sans', system-ui, sans-serif;
    font-family: var(--font-body);
    color: var(--sumi);
    max-width: 720px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    min-height: calc(100vh - 80px);
  }

  html[data-theme="dark"] .tree-wrap {
    --sumi: #f0ece4;
    --kuro: #e8e3d8;
    --hai: #b8b3a8;
    --kinari: #2c2c28;
    --shiro: #1a1a18;
    --kinu: #3d3d38;
    --ishi: #5a5750;
    --sugi: #8a8578;
  }

  /* Header */
  .tree-header {
    padding: 24px 24px 16px;
    border-bottom: 1px solid var(--kinu);
  }

  .tree-header h1 {
    font-family: var(--font-display);
    font-size: 1.6rem;
    font-weight: 500;
    margin: 0 0 4px;
    color: var(--sumi);
  }

  .tree-header p {
    font-size: 0.85rem;
    color: var(--sugi);
    margin: 0;
  }

  /* Breadcrumb */
  .tree-breadcrumb {
    padding: 12px 24px;
    display: flex;
    align-items: center;
    gap: 6px;
    flex-wrap: wrap;
    font-size: 0.78rem;
    color: var(--sugi);
    border-bottom: 1px solid var(--kinu);
    min-height: 42px;
  }

  .tree-breadcrumb-item {
    background: none;
    border: none;
    color: var(--ai);
    font-size: 0.78rem;
    font-family: var(--font-body);
    cursor: pointer;
    padding: 2px 4px;
    border-radius: 4px;
    transition: all 0.15s;
  }

  .tree-breadcrumb-item:hover {
    background: var(--kinu);
    color: var(--sumi);
  }

  .tree-breadcrumb-sep {
    color: var(--ishi);
    font-size: 0.7rem;
    user-select: none;
  }

  .tree-breadcrumb-current {
    color: var(--sumi);
    font-weight: 500;
    padding: 2px 4px;
  }

  /* Content area */
  .tree-content {
    flex: 1;
    overflow-y: auto;
    padding: 24px;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .tree-content::-webkit-scrollbar { width: 5px; }
  .tree-content::-webkit-scrollbar-track { background: transparent; }
  .tree-content::-webkit-scrollbar-thumb { background: var(--ishi); border-radius: 3px; }

  /* Question / info bubble */
  .tree-question {
    display: flex;
    gap: 10px;
    animation: treeFadeIn 0.3s ease;
  }

  .tree-avatar {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background: var(--kinu);
    color: var(--sugi);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.75rem;
    flex-shrink: 0;
    font-weight: 600;
  }

  .tree-bubble {
    padding: 14px 18px;
    border-radius: 16px;
    border-bottom-left-radius: 4px;
    background: var(--kinu);
    color: var(--sumi);
    max-width: 85%;
    font-size: 0.9rem;
    line-height: 1.55;
  }

  .tree-bubble p { margin: 0; }

  /* Options */
  .tree-options {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding-left: 42px;
    animation: treeFadeIn 0.35s ease;
  }

  .tree-option {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 14px 18px;
    border: 1px solid var(--kinu);
    border-radius: 14px;
    background: transparent;
    color: var(--sumi);
    font-size: 0.88rem;
    font-family: var(--font-body);
    cursor: pointer;
    text-align: left;
    transition: all 0.2s;
    line-height: 1.4;
  }

  .tree-option:hover {
    background: var(--kinu);
    border-color: var(--ishi);
    transform: translateX(4px);
  }

  .tree-option:active {
    transform: translateX(2px);
  }

  .tree-option-icon {
    font-size: 1.1rem;
    flex-shrink: 0;
    width: 28px;
    text-align: center;
  }

  .tree-option-text {
    flex: 1;
  }

  .tree-option-meta {
    font-size: 0.75rem;
    color: var(--sugi);
    display: block;
    margin-top: 2px;
  }

  /* Leaf node (module with PDF/Quiz links) */
  .tree-leaf {
    padding-left: 42px;
    animation: treeFadeIn 0.35s ease;
  }

  .tree-leaf-card {
    padding: 20px;
    border: 1px solid var(--kinu);
    border-radius: 16px;
    background: var(--kinari);
  }

  .tree-leaf-card h4 {
    font-family: var(--font-display);
    font-size: 1.15rem;
    font-weight: 500;
    margin: 0 0 6px;
    color: var(--sumi);
  }

  .tree-leaf-card .tree-leaf-desc {
    font-size: 0.82rem;
    color: var(--sugi);
    margin: 0 0 16px;
    line-height: 1.5;
  }

  .tree-leaf-actions {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }

  .tree-leaf-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 10px 18px;
    border-radius: 10px;
    font-size: 0.84rem;
    font-family: var(--font-body);
    font-weight: 500;
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
    border: none;
  }

  .tree-leaf-btn--pdf {
    background: var(--kinu);
    color: var(--sumi);
  }

  .tree-leaf-btn--pdf:hover {
    background: var(--ishi);
    color: var(--shiro);
  }

  .tree-leaf-btn--quiz {
    background: var(--beni);
    color: #fff;
  }

  .tree-leaf-btn--quiz:hover {
    opacity: 0.85;
  }

  .tree-leaf-btn--tool {
    background: var(--ai);
    color: #fff;
  }

  .tree-leaf-btn--tool:hover {
    opacity: 0.85;
  }

  /* Back button in footer */
  .tree-footer {
    padding: 16px 24px 24px;
    border-top: 1px solid var(--kinu);
    display: flex;
    gap: 10px;
    align-items: center;
  }

  .tree-back-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 10px 20px;
    border: 1px solid var(--kinu);
    border-radius: 24px;
    background: transparent;
    color: var(--sugi);
    font-size: 0.84rem;
    font-family: var(--font-body);
    cursor: pointer;
    transition: all 0.2s;
  }

  .tree-back-btn:hover {
    background: var(--kinu);
    color: var(--sumi);
  }

  .tree-home-btn {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 10px 20px;
    border: 1px solid var(--kinu);
    border-radius: 24px;
    background: transparent;
    color: var(--sugi);
    font-size: 0.84rem;
    font-family: var(--font-body);
    cursor: pointer;
    transition: all 0.2s;
    margin-left: auto;
  }

  .tree-home-btn:hover {
    background: var(--kinu);
    color: var(--sumi);
  }

  /* Mobile */
  @media (max-width: 600px) {
    .tree-wrap {
      min-height: 100vh;
      min-height: 100dvh;
    }

    .tree-header {
      padding: 16px 16px 12px;
    }

    .tree-header h1 {
      font-size: 1.3rem;
    }

    .tree-breadcrumb {
      padding: 10px 16px;
      font-size: 0.72rem;
    }

    .tree-content {
      padding: 16px 12px;
      gap: 12px;
    }

    .tree-avatar {
      width: 28px;
      height: 28px;
      font-size: 0.65rem;
    }

    .tree-bubble {
      padding: 10px 14px;
      font-size: 0.85rem;
      max-width: 90%;
    }

    .tree-options {
      padding-left: 36px;
      gap: 6px;
    }

    .tree-option {
      padding: 12px 14px;
      font-size: 0.82rem;
      border-radius: 12px;
      gap: 10px;
    }

    .tree-leaf {
      padding-left: 36px;
    }

    .tree-leaf-card {
      padding: 16px;
    }

    .tree-footer {
      padding: 12px 16px 16px;
    }
  }

  @media (max-width: 380px) {
    .tree-avatar {
      display: none;
    }

    .tree-options {
      padding-left: 0;
    }

    .tree-leaf {
      padding-left: 0;
    }

    .tree-option {
      padding: 10px 12px;
      font-size: 0.78rem;
    }
  }

  @supports (padding-bottom: env(safe-area-inset-bottom)) {
    .tree-footer {
      padding-bottom: calc(16px + env(safe-area-inset-bottom));
    }
  }

  @keyframes treeFadeIn {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>

<div class="tree-wrap">
  <div class="tree-header">
    <h1>Lernassistent</h1>
    <p>Studienkolleg Leipzig</p>
  </div>

  <div class="tree-breadcrumb" id="breadcrumb"></div>

  <div class="tree-content" id="treeContent"></div>

  <div class="tree-footer" id="treeFooter" style="display: none;">
    <button class="tree-back-btn" onclick="goBack()">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="15 18 9 12 15 6"/></svg>
      Zurück
    </button>
    <button class="tree-home-btn" onclick="goHome()">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
      Start
    </button>
  </div>
</div>

<script>
const TREE = {
  root: {
    question: "Hallo! Was möchtest du lernen?",
    options: [
      { label: "Mathematik", icon: "📐", meta: "30 Module · Algebra, Vektoren, Analysis, Integralrechnung", next: "mathe" },
      { label: "Volkswirtschaftslehre", icon: "📊", meta: "14 Module · Mikro- & Makroökonomie", next: "vwl" },
      { label: "Informatik", icon: "💻", meta: "6 Module · Python", next: "info" }
    ]
  },

  // ─── MATHEMATIK ───
  mathe: {
    question: "Welches Thema in Mathematik interessiert dich?",
    options: [
      { label: "Lineare Algebra", icon: "🔢", meta: "5 Module · Matrizen, Determinanten, LGS", next: "mathe_algebra" },
      { label: "Vektorrechnung", icon: "➡️", meta: "4 Module · Grundlagen, Produkte, Geraden, Ebenen", next: "mathe_vektor" },
      { label: "Differentialrechnung", icon: "📈", meta: "12 Module · Folgen, Grenzwerte, Ableitungen, Kurvendiskussion", next: "mathe_diff" },
      { label: "Integralrechnung", icon: "∫", meta: "4 Module · Stammfunktionen, Flächen, Rotation", next: "mathe_integral" },
      { label: "Interaktive Tools", icon: "🛠️", meta: "5 Tools · Explorer & Rechner", next: "mathe_tools" }
    ]
  },

  // Lineare Algebra
  mathe_algebra: {
    question: "Lineare Algebra — wähle ein Modul:",
    options: [
      { label: "01 · Matrizen", icon: "📄", next: "leaf_a1" },
      { label: "02 · Determinanten", icon: "📄", next: "leaf_a2" },
      { label: "03 · Matrizengleichungen", icon: "📄", next: "leaf_a3" },
      { label: "04 · Lineare Gleichungssysteme", icon: "📄", next: "leaf_a4" },
      { label: "05 · Parameterabhängigkeit", icon: "📄", next: "leaf_a5" }
    ]
  },
  leaf_a1: { leaf: true, title: "Matrizen", desc: "Grundlagen der Matrizenrechnung: Addition, Multiplikation und Transposition.", pdf: "/assets/pdfs/Matrizen_2_1.pdf", quiz: "/assets/quizzes/quiz_matrizen_grundlagen.html" },
  leaf_a2: { leaf: true, title: "Determinanten", desc: "Berechnung von Determinanten (2×2 und 3×3) mit Sarrus und Laplace.", pdf: "/assets/pdfs/Matrizen_2_2.pdf", quiz: "/assets/quizzes/quiz_determinanten.html" },
  leaf_a3: { leaf: true, title: "Matrizengleichungen", desc: "Lösung von Gleichungen mit Matrizen und inversen Matrizen.", pdf: "/assets/pdfs/Matrizen_2_3.pdf" },
  leaf_a4: { leaf: true, title: "Lineare Gleichungssysteme", desc: "LGS lösen mit Gauß-Algorithmus und Matrizenmethoden.", pdf: "/assets/pdfs/LGS_2_1-5.pdf", quiz: "/assets/quizzes/quiz_lgs_grundlagen.html" },
  leaf_a5: { leaf: true, title: "Parameterabhängigkeit", desc: "LGS mit Parametern und ihre Lösbarkeitsanalyse.", pdf: "/assets/pdfs/LGS_2_2-2.pdf" },

  // Vektorrechnung
  mathe_vektor: {
    question: "Vektorrechnung — wähle ein Modul:",
    options: [
      { label: "06 · Grundlagen", icon: "📄", next: "leaf_v1" },
      { label: "07 · Vektor- & Spatprodukt", icon: "📄", next: "leaf_v2" },
      { label: "08 · Geraden und Ebenen", icon: "📄", next: "leaf_v3" },
      { label: "09 · Abstände und Lagen", icon: "📄", next: "leaf_v4" }
    ]
  },
  leaf_v1: { leaf: true, title: "Grundlagen der Vektorrechnung", desc: "Vektoren im Raum, Skalarprodukt und Betrag.", pdf: "/assets/pdfs/Geo_2_1-2.pdf", quiz: "/assets/quizzes/quiz_vektorrechnung_grundlagen.html" },
  leaf_v2: { leaf: true, title: "Vektor- & Spatprodukt", desc: "Kreuzprodukt, Spatprodukt und Flächenberechnung.", pdf: "/assets/pdfs/Geo_2_2-2.pdf", quiz: "/assets/quizzes/quiz_vektorprodukt.html" },
  leaf_v3: { leaf: true, title: "Geraden und Ebenen", desc: "Parameterdarstellungen, Koordinatenform und Umrechnungen.", pdf: "/assets/pdfs/Geo_2_3.pdf", quiz: "/assets/quizzes/quiz_geraden_ebenen.html" },
  leaf_v4: { leaf: true, title: "Abstände und Lagen", desc: "Lagebeziehungen und Abstandsberechnungen im Raum.", pdf: "/assets/pdfs/Geo_2_4.pdf", quiz: "/assets/quizzes/quiz_lagebeziehungen.html" },

  // Differentialrechnung
  mathe_diff: {
    question: "Differentialrechnung ist ein großes Thema. Was genau?",
    options: [
      { label: "Folgen & Grenzwerte", icon: "🔄", meta: "5 Module", next: "mathe_diff_grenz" },
      { label: "Ableitungen", icon: "📐", meta: "3 Module", next: "mathe_diff_abl" },
      { label: "Kurvenuntersuchung", icon: "📈", meta: "4 Module", next: "mathe_diff_kurve" }
    ]
  },

  mathe_diff_grenz: {
    question: "Folgen & Grenzwerte — wähle ein Modul:",
    options: [
      { label: "10 · Zahlenfolgen", icon: "📄", next: "leaf_d1" },
      { label: "11 · Grenzwerte von Folgen", icon: "📄", next: "leaf_d2" },
      { label: "12 · Grenzwerte im Unendlichen", icon: "📄", next: "leaf_d3" },
      { label: "13 · Grenzwerte an einer Stelle", icon: "📄", next: "leaf_d4" },
      { label: "14 · Asymptoten", icon: "📄", next: "leaf_d5" }
    ]
  },
  leaf_d1: { leaf: true, title: "Zahlenfolgen", desc: "Arithmetische und geometrische Folgen, Bildungsgesetze.", pdf: "/assets/pdfs/Zahlenfolgen_2_1.pdf", quiz: "/assets/quizzes/quiz_zahlenfolgen.html" },
  leaf_d2: { leaf: true, title: "Grenzwerte von Folgen", desc: "Konvergenz, Divergenz und Grenzwertbestimmung.", pdf: "/assets/pdfs/Grenzwerte_2_1.pdf", quiz: "/assets/quizzes/quiz_grenzwerte_folgen.html" },
  leaf_d3: { leaf: true, title: "Grenzwerte im Unendlichen", desc: "Verhalten von Funktionen für x → ±∞.", pdf: "/assets/pdfs/Funktion_2_2.pdf", quiz: "/assets/quizzes/quiz_grenzwerte_funktionen_1.html" },
  leaf_d4: { leaf: true, title: "Grenzwerte an einer Stelle", desc: "Linksseitige und rechtsseitige Grenzwerte, Stetigkeit.", pdf: "/assets/pdfs/Grenzwerte_2_2.pdf", quiz: "/assets/quizzes/quiz_grenzwerte_funktionen_2.html" },
  leaf_d5: { leaf: true, title: "Asymptoten", desc: "Horizontale, vertikale und schiefe Asymptoten bestimmen.", pdf: "/assets/pdfs/Grenzwerte_2_3.pdf", quiz: "/assets/quizzes/quiz_asymptoten.html" },

  mathe_diff_abl: {
    question: "Ableitungen — wähle ein Modul:",
    options: [
      { label: "15 · Steigung und Ableitung", icon: "📄", next: "leaf_d6" },
      { label: "16 · Ableitungsregeln", icon: "📄", next: "leaf_d7" },
      { label: "17 · Regel von de L'Hôpital", icon: "📄", next: "leaf_d8" }
    ]
  },
  leaf_d6: { leaf: true, title: "Steigung und Ableitung", desc: "Differenzenquotient, Differentialquotient und Ableitungsbegriff.", pdf: "/assets/pdfs/Funktion_2_1.pdf", quiz: "/assets/quizzes/quiz_ableitung_grundlagen.html" },
  leaf_d7: { leaf: true, title: "Ableitungsregeln", desc: "Summen-, Produkt-, Quotienten- und Kettenregel.", pdf: "/assets/pdfs/Funktion_2_4.pdf", quiz: "/assets/quizzes/quiz_ableitungsregeln.html" },
  leaf_d8: { leaf: true, title: "Regel von de L'Hôpital", desc: "Grenzwertberechnung bei unbestimmten Ausdrücken 0/0 und ∞/∞.", pdf: "/assets/pdfs/Hospital_2_1.pdf", quiz: "/assets/quizzes/quiz_hospital.html" },

  mathe_diff_kurve: {
    question: "Kurvenuntersuchung — wähle ein Modul:",
    options: [
      { label: "18 · Extrempunkte", icon: "📄", next: "leaf_d9" },
      { label: "19 · Wendepunkte", icon: "📄", next: "leaf_d10" },
      { label: "20 · Kurvendiskussion", icon: "📄", next: "leaf_d11" },
      { label: "21 · Extremwertaufgaben", icon: "📄", next: "leaf_d12" }
    ]
  },
  leaf_d9: { leaf: true, title: "Extrempunkte", desc: "Hoch- und Tiefpunkte bestimmen mit der 1. und 2. Ableitung.", pdf: "/assets/pdfs/Extremwert_2_1.pdf", quiz: "/assets/quizzes/quiz_extrempunkte.html" },
  leaf_d10: { leaf: true, title: "Wendepunkte", desc: "Wendepunkte und Krümmungsverhalten analysieren.", pdf: "/assets/pdfs/Wendepunkt_2_1.pdf", quiz: "/assets/quizzes/quiz_wendepunkte.html" },
  leaf_d11: { leaf: true, title: "Kurvendiskussion", desc: "Vollständige Untersuchung einer Funktion: Nullstellen, Extrema, Wendepunkte, Asymptoten.", pdf: "/assets/pdfs/Kurvendiskusion_2_1.pdf", quiz: "/assets/quizzes/quiz_kurvendiskussion.html" },
  leaf_d12: { leaf: true, title: "Extremwertaufgaben", desc: "Optimierungsprobleme aus der Praxis lösen.", pdf: "/assets/pdfs/Extrem_2_1.pdf", quiz: "/assets/quizzes/quiz_extremwertaufgaben.html" },

  // Integralrechnung
  mathe_integral: {
    question: "Integralrechnung — wähle ein Modul:",
    options: [
      { label: "22 · Einführung", icon: "📄", next: "leaf_i1" },
      { label: "23 · Integrationsmethoden", icon: "📄", next: "leaf_i2" },
      { label: "24 · Hauptsatz & Flächen", icon: "📄", next: "leaf_i3" },
      { label: "25 · Rotationsvolumen", icon: "📄", next: "leaf_i4" }
    ]
  },
  leaf_i1: { leaf: true, title: "Einführung in die Integralrechnung", desc: "Stammfunktionen und unbestimmtes Integral.", pdf: "/assets/pdfs/Integral_2_1.pdf", quiz: "/assets/quizzes/quiz_integral_einfuehrung.html" },
  leaf_i2: { leaf: true, title: "Integrationsmethoden", desc: "Substitution, partielle Integration und Partialbruchzerlegung.", pdf: "/assets/pdfs/Integral_2_2.pdf", quiz: "/assets/quizzes/quiz_integrationsmethoden.html" },
  leaf_i3: { leaf: true, title: "Hauptsatz & Flächen", desc: "Hauptsatz der Differential- und Integralrechnung, Flächenberechnung.", pdf: "/assets/pdfs/Integral_2_3.pdf", quiz: "/assets/quizzes/quiz_hauptsatz_flaechen.html" },
  leaf_i4: { leaf: true, title: "Rotationsvolumen", desc: "Volumenberechnung von Rotationskörpern.", pdf: "/assets/pdfs/Intergal_2_4-2.pdf", quiz: "/assets/quizzes/quiz_rotationsvolumen.html" },

  // Interaktive Tools
  mathe_tools: {
    question: "Interaktive Tools — wähle ein Tool:",
    options: [
      { label: "Tangenten-Explorer", icon: "🎯", next: "leaf_t1" },
      { label: "3D-Vektor-Explorer", icon: "🧊", next: "leaf_t2" },
      { label: "Geraden & Ebenen", icon: "📏", next: "leaf_t3" },
      { label: "Matrizen-Explorer", icon: "🔲", next: "leaf_t4" },
      { label: "Determinanten-Rechner", icon: "🧮", next: "leaf_t5" }
    ]
  },
  leaf_t1: { leaf: true, title: "Tangenten-Explorer", desc: "Interaktiv Tangenten an Funktionsgraphen erkunden.", tool: "/assets/interactive/tangenten_explorer.html" },
  leaf_t2: { leaf: true, title: "3D-Vektor-Explorer", desc: "Vektoren im dreidimensionalen Raum visualisieren.", tool: "/assets/interactive/vektor_explorer.html" },
  leaf_t3: { leaf: true, title: "Geraden & Ebenen", desc: "Geraden und Ebenen im 3D-Raum interaktiv erkunden.", tool: "/assets/interactive/geraden_ebenen_explorer.html" },
  leaf_t4: { leaf: true, title: "Matrizen-Explorer", desc: "Matrizenoperationen visuell verstehen.", tool: "/assets/interactive/matrizen_explorer.html" },
  leaf_t5: { leaf: true, title: "Determinanten-Rechner", desc: "Determinanten Schritt für Schritt berechnen.", tool: "/assets/interactive/determinanten_rechner.html" },

  // ─── VWL ───
  vwl: {
    question: "Welches Thema in VWL interessiert dich?",
    options: [
      { label: "Mikroökonomie", icon: "🏪", meta: "8 Module · Angebot, Nachfrage, Märkte", next: "vwl_mikro" },
      { label: "Makroökonomie", icon: "🌍", meta: "6 Module · BIP, Konjunktur, Arbeitsmarkt", next: "vwl_makro" }
    ]
  },

  vwl_mikro: {
    question: "Mikroökonomie — wähle ein Modul:",
    options: [
      { label: "01 · Bedürfnis, Bedarf und Nachfrage", icon: "📄", next: "leaf_m1" },
      { label: "02 · Güterarten in der Wirtschaft", icon: "📄", next: "leaf_m2" },
      { label: "03 · Angebot und Angebotskurve", icon: "📄", next: "leaf_m3" },
      { label: "04 · Nachfrage und Nachfragekurve", icon: "📄", next: "leaf_m4" },
      { label: "05 · Marktgleichgewicht", icon: "📄", next: "leaf_m5" },
      { label: "06 · Konsumenten- und Produzentenrente", icon: "📄", next: "leaf_m6" },
      { label: "07 · Marktformen", icon: "📄", next: "leaf_m7" },
      { label: "08 · Budgetgerade", icon: "📄", next: "leaf_m8" }
    ]
  },
  leaf_m1: { leaf: true, title: "Bedürfnis, Bedarf und Nachfrage", desc: "Grundbegriffe der Volkswirtschaftslehre und das ökonomische Prinzip.", pdf: "/assets/pdfs/WS_VWL_1-3.pdf", quiz: "/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html" },
  leaf_m2: { leaf: true, title: "Güterarten in der Wirtschaft", desc: "Freie und wirtschaftliche Güter, Konsum- und Investitionsgüter.", pdf: "/assets/pdfs/WS_VWL_2-2.pdf", quiz: "/assets/quizzes/quiz_gueterarten.html" },
  leaf_m3: { leaf: true, title: "Angebot und Angebotskurve", desc: "Das Gesetz des Angebots und Verschiebungen der Kurve.", pdf: "/assets/pdfs/WS_VWL_3-4.pdf", quiz: "/assets/quizzes/quiz_angebot.html" },
  leaf_m4: { leaf: true, title: "Nachfrage und Nachfragekurve", desc: "Das Gesetz der Nachfrage, Preis- und Einkommenseffekte.", pdf: "/assets/pdfs/WS_VWL_4-2.pdf", quiz: "/assets/quizzes/quiz_nachfrage.html" },
  leaf_m5: { leaf: true, title: "Marktgleichgewicht", desc: "Gleichgewichtspreis und -menge, Störungen des Gleichgewichts.", pdf: "/assets/pdfs/WS_VWL_5-2.pdf", quiz: "/assets/quizzes/quiz_marktgleichgewicht.html" },
  leaf_m6: { leaf: true, title: "Konsumenten- und Produzentenrente", desc: "Wohlfahrtsanalyse und Renten im Marktmodell.", pdf: "/assets/pdfs/WS_VWL_6.pdf", quiz: "/assets/quizzes/quiz_renten.html" },
  leaf_m7: { leaf: true, title: "Marktformen", desc: "Polypol, Oligopol und Monopol im Vergleich.", pdf: "/assets/pdfs/WS_VWL_7.pdf", quiz: "/assets/quizzes/quiz_marktformen.html" },
  leaf_m8: { leaf: true, title: "Budgetgerade", desc: "Budgetbeschränkung, optimale Konsumentscheidung.", pdf: "/assets/pdfs/WS_VWL_8-3.pdf", quiz: "/assets/quizzes/quiz_budgetgerade.html" },

  vwl_makro: {
    question: "Makroökonomie — wähle ein Modul:",
    options: [
      { label: "09 · Volkswirtschaftliche Gesamtrechnung", icon: "📄", next: "leaf_m9" },
      { label: "10 · Nominales vs. reales BIP", icon: "📄", next: "leaf_m10" },
      { label: "11 · Konjunktur & Konjunkturzyklen", icon: "📄", next: "leaf_m11" },
      { label: "12 · Antizyklische Konjunkturpolitik", icon: "📄", next: "leaf_m12" },
      { label: "13 · Arbeitslosigkeit & Arbeitsmarktpolitik", icon: "📄", next: "leaf_m13" },
      { label: "14 · Inflation & Preisniveaustabilität", icon: "📄", next: "leaf_m14" }
    ]
  },
  leaf_m9: { leaf: true, title: "Volkswirtschaftliche Gesamtrechnung", desc: "BIP-Berechnung: Entstehungs-, Verwendungs- und Verteilungsrechnung.", pdf: "/assets/pdfs/VWL_11.pdf", quiz: "/assets/quizzes/quiz_vgr.html" },
  leaf_m10: { leaf: true, title: "Nominales vs. reales BIP", desc: "Preisbereinigung, BIP-Deflator und Kaufkraftvergleiche.", pdf: "/assets/pdfs/VWL_12.pdf", quiz: "/assets/quizzes/quiz_vgr2.html" },
  leaf_m11: { leaf: true, title: "Konjunktur & Konjunkturzyklen", desc: "Aufschwung, Boom, Abschwung und Rezession verstehen.", pdf: "/assets/pdfs/VWL_11_Konjunktur.pdf", quiz: "/assets/quizzes/quiz_konjunktur.html" },
  leaf_m12: { leaf: true, title: "Antizyklische Konjunkturpolitik", desc: "Fiskal- und Geldpolitik zur Stabilisierung der Wirtschaft.", pdf: "/assets/pdfs/VWL_12_Konjunkturpolitik.pdf", quiz: "/assets/quizzes/quiz_konjunkturpolitik.html" },
  leaf_m13: { leaf: true, title: "Arbeitslosigkeit & Arbeitsmarktpolitik", desc: "Arten der Arbeitslosigkeit und politische Gegenmaßnahmen.", pdf: "/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf", quiz: "/assets/quizzes/quiz_arbeitslosigkeit.html" },
  leaf_m14: { leaf: true, title: "Inflation & Preisniveaustabilität", desc: "Ursachen und Folgen von Inflation, Rolle der Zentralbank.", pdf: "/assets/pdfs/VWL_14_Preisniveau.pdf", quiz: "/assets/quizzes/quiz_preisniveau.html" },

  // ─── INFORMATIK ───
  info: {
    question: "Informatik (Python) — wähle ein Modul:",
    options: [
      { label: "01 · Python Grundlagen – print() und input()", icon: "📄", next: "leaf_p1" },
      { label: "02 · Variablen und Datentypen", icon: "📄", next: "leaf_p2" },
      { label: "03 · Listen und Datenstrukturen", icon: "📄", next: "leaf_p3" },
      { label: "04 · Kontrollstrukturen – if, for, while", icon: "📄", next: "leaf_p4" },
      { label: "05 · Funktionen in Python", icon: "📄", next: "leaf_p5" },
      { label: "06 · NumPy – Kurvendiskussion & Ableitungen", icon: "📄", next: "leaf_p6" }
    ]
  },
  leaf_p1: { leaf: true, title: "Python Grundlagen – print() und input()", desc: "Erste Schritte: Ausgabe, Eingabe und der Python-Interpreter.", pdf: "/assets/pdfs/Info_1.pdf", quiz: "/assets/quizzes/quiz_python_grundlage.html" },
  leaf_p2: { leaf: true, title: "Variablen und Datentypen", desc: "int, float, str, bool und Typumwandlungen.", pdf: "/assets/pdfs/Info_2.pdf", quiz: "/assets/quizzes/quiz_variablen_datentypen.html" },
  leaf_p3: { leaf: true, title: "Listen und Datenstrukturen", desc: "Listen, Tupel, Dictionaries und ihre Methoden.", pdf: "/assets/pdfs/Info_3.pdf", quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html" },
  leaf_p4: { leaf: true, title: "Kontrollstrukturen – if, for, while", desc: "Bedingte Anweisungen und Schleifen in Python.", pdf: "/assets/pdfs/Info_4.pdf", quiz: "/assets/quizzes/quiz_kontrollstrukturen.html" },
  leaf_p5: { leaf: true, title: "Funktionen in Python", desc: "Eigene Funktionen definieren, Parameter und Rückgabewerte.", pdf: "/assets/pdfs/Info_5.pdf", quiz: "/assets/quizzes/quiz_funktionen.html" },
  leaf_p6: { leaf: true, title: "NumPy – Kurvendiskussion & Ableitungen", desc: "Numerische Mathematik mit NumPy: Ableitungen und Kurvenanalyse.", pdf: "/assets/pdfs/Info_6.pdf", quiz: "/assets/quizzes/quiz_numpy_kurvendiskussion.html" }
};

// Navigation names for breadcrumb
const NODE_NAMES = {
  root: "Start",
  mathe: "Mathematik",
  vwl: "VWL",
  info: "Informatik",
  mathe_algebra: "Lineare Algebra",
  mathe_vektor: "Vektorrechnung",
  mathe_diff: "Differentialrechnung",
  mathe_integral: "Integralrechnung",
  mathe_tools: "Interaktive Tools",
  mathe_diff_grenz: "Folgen & Grenzwerte",
  mathe_diff_abl: "Ableitungen",
  mathe_diff_kurve: "Kurvenuntersuchung",
  vwl_mikro: "Mikroökonomie",
  vwl_makro: "Makroökonomie"
};

let history = [];
let currentNode = 'root';

function renderNode(nodeId) {
  currentNode = nodeId;
  const node = TREE[nodeId];
  const contentEl = document.getElementById('treeContent');
  const footerEl = document.getElementById('treeFooter');
  const breadcrumbEl = document.getElementById('breadcrumb');

  contentEl.innerHTML = '';

  // Breadcrumb
  renderBreadcrumb(breadcrumbEl);

  // Show/hide footer
  footerEl.style.display = nodeId === 'root' ? 'none' : 'flex';

  if (node.leaf) {
    // Leaf node: show module card
    const questionHTML = `
      <div class="tree-question">
        <div class="tree-avatar">STK</div>
        <div class="tree-bubble"><p>Hier ist dein Material:</p></div>
      </div>
    `;

    let actionsHTML = '';
    if (node.pdf) {
      actionsHTML += `<a href="${node.pdf}" class="tree-leaf-btn tree-leaf-btn--pdf" target="_blank">📄 PDF öffnen</a>`;
    }
    if (node.quiz) {
      actionsHTML += `<a href="${node.quiz}" class="tree-leaf-btn tree-leaf-btn--quiz" target="_blank">✏️ Quiz starten</a>`;
    }
    if (node.tool) {
      actionsHTML += `<a href="${node.tool}" class="tree-leaf-btn tree-leaf-btn--tool" target="_blank">🛠️ Tool öffnen</a>`;
    }

    const leafHTML = `
      <div class="tree-leaf">
        <div class="tree-leaf-card">
          <h4>${node.title}</h4>
          <p class="tree-leaf-desc">${node.desc}</p>
          <div class="tree-leaf-actions">${actionsHTML}</div>
        </div>
      </div>
    `;

    contentEl.innerHTML = questionHTML + leafHTML;
  } else {
    // Branch node: show question + options
    const questionHTML = `
      <div class="tree-question">
        <div class="tree-avatar">STK</div>
        <div class="tree-bubble"><p>${node.question}</p></div>
      </div>
    `;

    let optionsHTML = '<div class="tree-options">';
    for (const opt of node.options) {
      const metaStr = opt.meta ? `<span class="tree-option-meta">${opt.meta}</span>` : '';
      optionsHTML += `
        <button class="tree-option" onclick="navigate('${opt.next}')">
          <span class="tree-option-icon">${opt.icon || ''}</span>
          <span class="tree-option-text">${opt.label}${metaStr}</span>
        </button>
      `;
    }
    optionsHTML += '</div>';

    contentEl.innerHTML = questionHTML + optionsHTML;
  }

  contentEl.scrollTop = 0;
}

function renderBreadcrumb(el) {
  if (history.length === 0 && currentNode === 'root') {
    el.innerHTML = '<span class="tree-breadcrumb-current">Start</span>';
    return;
  }

  let html = '';
  // Root is always first
  html += `<button class="tree-breadcrumb-item" onclick="jumpTo(0)">Start</button>`;

  for (let i = 0; i < history.length; i++) {
    const id = history[i];
    const name = NODE_NAMES[id] || id;
    html += `<span class="tree-breadcrumb-sep">›</span>`;
    html += `<button class="tree-breadcrumb-item" onclick="jumpTo(${i + 1})">${name}</button>`;
  }

  // Current node
  const currentName = NODE_NAMES[currentNode] || (TREE[currentNode] && TREE[currentNode].title) || currentNode;
  html += `<span class="tree-breadcrumb-sep">›</span>`;
  html += `<span class="tree-breadcrumb-current">${currentName}</span>`;

  el.innerHTML = html;
}

function navigate(nodeId) {
  history.push(currentNode);
  renderNode(nodeId);
}

function goBack() {
  if (history.length > 0) {
    const prev = history.pop();
    renderNode(prev);
  }
}

function goHome() {
  history = [];
  renderNode('root');
}

function jumpTo(index) {
  if (index === 0) {
    goHome();
    return;
  }
  // Jump to a specific point in history
  const targetNode = history[index - 1];
  // Keep history up to but not including that index
  // Actually history[index-1] is the node at that breadcrumb position
  // We want to navigate TO that node, so trim history before it
  history = history.slice(0, index - 1);
  renderNode(targetNode);
}

// Initialize
renderNode('root');
</script>
