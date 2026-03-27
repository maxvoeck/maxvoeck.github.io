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
    --font-math: 'Georgia', 'Times New Roman', serif;
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

  .tree-option-text {
    flex: 1;
  }

  .tree-option-meta {
    font-size: 0.75rem;
    color: var(--sugi);
    display: block;
    margin-top: 2px;
  }

  /* Leaf node */
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

  /* Formula preview */
  .tree-preview {
    margin-bottom: 16px;
  }

  .tree-preview-section {
    margin-bottom: 10px;
  }

  .tree-preview-label {
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 0.07em;
    text-transform: uppercase;
    color: var(--sugi);
    margin-bottom: 6px;
  }

  .tree-formula-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 7px;
  }

  .tree-formula-grid--single {
    grid-template-columns: 1fr;
  }

  .tree-formula-card {
    background: var(--shiro);
    border: 1px solid var(--kinu);
    border-radius: 10px;
    padding: 10px 13px;
    transition: border-color 0.15s;
  }

  html[data-theme="dark"] .tree-formula-card {
    background: var(--kuro);
  }

  html[data-theme="dark"] .tree-leaf-card {
    background: #1e1e1c;
    border-color: var(--hai);
  }

  html[data-theme="dark"] .tree-formula-card {
    background: #1e1e1c;
    border-color: var(--hai);
  }

  .tree-formula-rule {
    font-size: 0.69rem;
    font-weight: 600;
    color: var(--sugi);
    margin-bottom: 4px;
    letter-spacing: 0.02em;
  }

  .tree-formula-expr {
    font-family: var(--font-math);
    font-size: 0.92rem;
    color: var(--sumi);
    line-height: 1.5;
  }

  .tree-formula-example {
    font-family: var(--font-math);
    font-size: 0.71rem;
    color: var(--sugi);
    margin-top: 5px;
    padding-top: 5px;
    border-top: 1px solid var(--kinu);
    line-height: 1.4;
  }

  .tree-preview-tip {
    background: var(--shiro);
    border-left: 2px solid var(--ai);
    border-radius: 0 8px 8px 0;
    padding: 9px 13px;
    font-size: 0.79rem;
    color: var(--sugi);
    line-height: 1.5;
    margin-top: 4px;
  }

  html[data-theme="dark"] .tree-preview-tip {
    background: #1e1e1c;
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
    .tree-wrap { min-height: 100vh; min-height: 100dvh; }
    .tree-header { padding: 16px 16px 12px; }
    .tree-header h1 { font-size: 1.3rem; }
    .tree-breadcrumb { padding: 10px 16px; font-size: 0.72rem; }
    .tree-content { padding: 16px 12px; gap: 12px; }
    .tree-avatar { width: 28px; height: 28px; font-size: 0.65rem; }
    .tree-bubble { padding: 10px 14px; font-size: 0.85rem; max-width: 90%; }
    .tree-options { padding-left: 36px; gap: 6px; }
    .tree-option { padding: 12px 14px; font-size: 0.82rem; border-radius: 12px; gap: 10px; }
    .tree-leaf { padding-left: 36px; }
    .tree-leaf-card { padding: 16px; }
    .tree-footer { padding: 12px 16px 16px; }
    .tree-formula-grid { grid-template-columns: 1fr; }
  }

  @media (max-width: 380px) {
    .tree-avatar { display: none; }
    .tree-options { padding-left: 0; }
    .tree-leaf { padding-left: 0; }
    .tree-option { padding: 10px 12px; font-size: 0.78rem; }
  }

  @supports (padding-bottom: env(safe-area-inset-bottom)) {
    .tree-footer { padding-bottom: calc(16px + env(safe-area-inset-bottom)); }
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
      { label: "Mathematik", icon: "", meta: "30 Module · Algebra, Vektoren, Analysis, Integralrechnung", next: "mathe" },
      { label: "Volkswirtschaftslehre", icon: "", meta: "14 Module · Mikro- & Makroökonomie", next: "vwl" },
      { label: "Informatik", icon: "", meta: "6 Module · Python", next: "info" }
    ]
  },

  // ─── MATHEMATIK ───
  mathe: {
    question: "Welches Thema in Mathematik interessiert dich?",
    options: [
      { label: "Lineare Algebra", icon: "", meta: "5 Module · Matrizen, Determinanten, LGS", next: "mathe_algebra" },
      { label: "Vektorrechnung", icon: "", meta: "4 Module · Grundlagen, Produkte, Geraden, Ebenen", next: "mathe_vektor" },
      { label: "Differentialrechnung", icon: "", meta: "12 Module · Folgen, Grenzwerte, Ableitungen, Kurvendiskussion", next: "mathe_diff" },
      { label: "Integralrechnung", icon: "", meta: "4 Module · Stammfunktionen, Flächen, Rotation", next: "mathe_integral" },
      { label: "Interaktive Tools", icon: "", meta: "5 Tools · Explorer & Rechner", next: "mathe_tools" }
    ]
  },

  // Lineare Algebra
  mathe_algebra: {
    question: "Lineare Algebra — wähle ein Modul:",
    options: [
      { label: "01 · Matrizen", icon: "", next: "leaf_a1" },
      { label: "02 · Determinanten", icon: "", next: "leaf_a2" },
      { label: "03 · Matrizengleichungen", icon: "", next: "leaf_a3" },
      { label: "04 · Lineare Gleichungssysteme", icon: "", next: "leaf_a4" },
      { label: "05 · Parameterabhängigkeit", icon: "", next: "leaf_a5" }
    ]
  },
  leaf_a1: {
    leaf: true, title: "Matrizen",
    desc: "Grundlagen der Matrizenrechnung: Addition, Multiplikation und Transposition.",
    preview: [
      {
        label: "Grundoperationen",
        formulas: [
          { rule: "Addition", expr: "A + B = (aᵢⱼ + bᵢⱼ)", example: "Elementweise Addition" },
          { rule: "Skalarmultiplikation", expr: "c · A = (c · aᵢⱼ)", example: "z.B. 3·A verdreifacht jeden Eintrag" }
        ]
      },
      {
        label: "Matrizenmultiplikation",
        formulas: [
          { rule: "Produkt (m×n)·(n×p)", expr: "(AB)ᵢⱼ = Σₖ aᵢₖ · bₖⱼ", example: "Zeile × Spalte, Ergebnis: m×p" },
          { rule: "Transposition", expr: "(Aᵀ)ᵢⱼ = aⱼᵢ", example: "(AB)ᵀ = BᵀAᵀ" }
        ]
      }
    ],
    tip: "Matrizenmultiplikation ist nicht kommutativ: AB ≠ BA im Allgemeinen.",
    pdf: "/assets/pdfs/Matrizen_2_1.pdf", quiz: "/assets/quizzes/quiz_matrizen_grundlagen.html"
  },
  leaf_a2: {
    leaf: true, title: "Determinanten",
    desc: "Berechnung von Determinanten (2×2 und 3×3) mit Sarrus und Laplace.",
    preview: [
      {
        label: "2×2 Determinante",
        formulas: [
          { rule: "Formel", expr: "det(A) = ad − bc", example: "A = [[a,b],[c,d]]" }
        ]
      },
      {
        label: "3×3 Regel von Sarrus",
        formulas: [
          { rule: "Hauptdiagonalen (+)", expr: "aei + bfg + cdh", example: "Diagonalen von links nach rechts" },
          { rule: "Nebendiagonalen (−)", expr: "− (ceg + afh + bdi)", example: "Diagonalen von rechts nach links" }
        ]
      }
    ],
    tip: "det(A) = 0 ⟺ Zeilen/Spalten linear abhängig ⟺ keine Inverse vorhanden.",
    pdf: "/assets/pdfs/Matrizen_2_2.pdf", quiz: "/assets/quizzes/quiz_determinanten.html"
  },
  leaf_a3: {
    leaf: true, title: "Matrizengleichungen",
    desc: "Lösung von Gleichungen mit Matrizen und inversen Matrizen.",
    preview: [
      {
        label: "Inverse Matrix",
        formulas: [
          { rule: "Definition", expr: "A · A⁻¹ = A⁻¹ · A = I", example: "I = Einheitsmatrix" },
          { rule: "2×2 Inverse", expr: "A⁻¹ = 1/det(A) · [[d,−b],[−c,a]]", example: "Nur wenn det(A) ≠ 0" }
        ]
      },
      {
        label: "Gleichung lösen",
        formulas: [
          { rule: "AX = B", expr: "X = A⁻¹ · B", example: "von links mit A⁻¹ multiplizieren" },
          { rule: "XA = B", expr: "X = B · A⁻¹", example: "von rechts mit A⁻¹ multiplizieren" }
        ]
      }
    ],
    tip: "Reihenfolge beachten: Matrizen sind nicht kommutativ — links oder rechts multiplizieren macht einen Unterschied.",
    pdf: "/assets/pdfs/Matrizen_2_3.pdf"
  },
  leaf_a4: {
    leaf: true, title: "Lineare Gleichungssysteme",
    desc: "LGS lösen mit Gauß-Algorithmus und Matrizenmethoden.",
    preview: [
      {
        label: "Gauß-Algorithmus Schritte",
        formulas: [
          { rule: "1. Erweiterte Matrix", expr: "(A | b)", example: "Koeffizientenmatrix + rechte Seite" },
          { rule: "2. Zeilenstufenform", expr: "Eliminiere Einträge unter Pivots", example: "durch Zeilenoperationen" },
          { rule: "3. Rücksubstitution", expr: "von unten nach oben lösen", example: "Letzte Zeile zuerst" }
        ]
      }
    ],
    tip: "Erlaubte Zeilenoperationen: Zeile tauschen, Zeile mit Skalar multiplizieren, Vielfaches einer Zeile addieren.",
    pdf: "/assets/pdfs/LGS_2_1-5.pdf", quiz: "/assets/quizzes/quiz_lgs_grundlagen.html"
  },
  leaf_a5: {
    leaf: true, title: "Parameterabhängigkeit",
    desc: "LGS mit Parametern und ihre Lösbarkeitsanalyse.",
    preview: [
      {
        label: "Lösbarkeit nach Gauß",
        formulas: [
          { rule: "Eindeutige Lösung", expr: "rang(A) = rang(A|b) = n", example: "voller Rang" },
          { rule: "Unendlich viele", expr: "rang(A) = rang(A|b) < n", example: "freie Parameter" },
          { rule: "Keine Lösung", expr: "rang(A) < rang(A|b)", example: "Widerspruch in einer Zeile" }
        ]
      }
    ],
    tip: "Bei Parameter λ: kritische Werte finden, bei denen der Rang springt.",
    pdf: "/assets/pdfs/LGS_2_2-2.pdf"
  },

  // Vektorrechnung
  mathe_vektor: {
    question: "Vektorrechnung — wähle ein Modul:",
    options: [
      { label: "06 · Grundlagen", icon: "", next: "leaf_v1" },
      { label: "07 · Vektor- & Spatprodukt", icon: "", next: "leaf_v2" },
      { label: "08 · Geraden und Ebenen", icon: "", next: "leaf_v3" },
      { label: "09 · Abstände und Lagen", icon: "", next: "leaf_v4" }
    ]
  },
  leaf_v1: {
    leaf: true, title: "Grundlagen der Vektorrechnung",
    desc: "Vektoren im Raum, Skalarprodukt und Betrag.",
    preview: [
      {
        label: "Betrag & Einheitsvektor",
        formulas: [
          { rule: "Betrag", expr: "|v| = √(x² + y² + z²)", example: "v = (x, y, z)" },
          { rule: "Einheitsvektor", expr: "v̂ = v / |v|", example: "|v̂| = 1" }
        ]
      },
      {
        label: "Skalarprodukt",
        formulas: [
          { rule: "Komponentenform", expr: "a · b = a₁b₁ + a₂b₂ + a₃b₃", example: "" },
          { rule: "Winkelformel", expr: "cos α = (a · b) / (|a| · |b|)", example: "a · b = 0 ⟺ a ⊥ b" }
        ]
      }
    ],
    tip: "Skalarprodukt = 0 bedeutet Orthogonalität — nützlich beim Prüfen auf Rechtwinkligkeit.",
    pdf: "/assets/pdfs/Geo_2_1-2.pdf", quiz: "/assets/quizzes/quiz_vektorrechnung_grundlagen.html"
  },
  leaf_v2: {
    leaf: true, title: "Vektor- & Spatprodukt",
    desc: "Kreuzprodukt, Spatprodukt und Flächenberechnung.",
    preview: [
      {
        label: "Kreuzprodukt",
        formulas: [
          { rule: "a × b =", expr: "(a₂b₃−a₃b₂, a₃b₁−a₁b₃, a₁b₂−a₂b₁)", example: "steht senkrecht auf a und b" },
          { rule: "Fläche Parallelogramm", expr: "A = |a × b|", example: "Dreieck: A = ½ |a × b|" }
        ]
      },
      {
        label: "Spatprodukt",
        formulas: [
          { rule: "Volumen Spat", expr: "V = |a · (b × c)|", example: "= |det([a,b,c])|" },
          { rule: "Koplanar?", expr: "a · (b × c) = 0", example: "⟺ Vektoren liegen in einer Ebene" }
        ]
      }
    ],
    tip: "Kreuzprodukt ist antikommutativ: a × b = −(b × a).",
    pdf: "/assets/pdfs/Geo_2_2-2.pdf", quiz: "/assets/quizzes/quiz_vektorprodukt.html"
  },
  leaf_v3: {
    leaf: true, title: "Geraden und Ebenen",
    desc: "Parameterdarstellungen, Koordinatenform und Umrechnungen.",
    preview: [
      {
        label: "Gerade",
        formulas: [
          { rule: "Parameterform", expr: "g: x = p + t · v", example: "p = Stützpunkt, v = Richtung" }
        ]
      },
      {
        label: "Ebene",
        formulas: [
          { rule: "Parameterform", expr: "E: x = p + s·u + t·v", example: "zwei Richtungsvektoren" },
          { rule: "Normalenform", expr: "n · (x − p) = 0", example: "n = Normalenvektor" },
          { rule: "Koordinatenform", expr: "ax + by + cz = d", example: "n = (a, b, c)" }
        ]
      }
    ],
    tip: "Normalenvektor einer Ebene in Parameterform: n = u × v (Kreuzprodukt der Richtungsvektoren).",
    pdf: "/assets/pdfs/Geo_2_3.pdf", quiz: "/assets/quizzes/quiz_geraden_ebenen.html"
  },
  leaf_v4: {
    leaf: true, title: "Abstände und Lagen",
    desc: "Lagebeziehungen und Abstandsberechnungen im Raum.",
    preview: [
      {
        label: "Abstände",
        formulas: [
          { rule: "Punkt–Ebene", expr: "d = |n·x₀ − d| / |n|", example: "Ebene: n·x = d" },
          { rule: "Punkt–Gerade", expr: "d = |AP × v| / |v|", example: "A auf Gerade, v Richtung" }
        ]
      },
      {
        label: "Lagebeziehungen Gerade–Ebene",
        formulas: [
          { rule: "Parallel", expr: "n · v = 0  und  P ∉ E", example: "" },
          { rule: "Enthalten", expr: "n · v = 0  und  P ∈ E", example: "" },
          { rule: "Schneidend", expr: "n · v ≠ 0", example: "Schnittpunkt per Einsetzen" }
        ]
      }
    ],
    tip: "Vor der Abstandsberechnung immer Lagebeziehung prüfen — parallele Objekte zuerst identifizieren.",
    pdf: "/assets/pdfs/Geo_2_4.pdf", quiz: "/assets/quizzes/quiz_lagebeziehungen.html"
  },

  // Differentialrechnung
  mathe_diff: {
    question: "Differentialrechnung ist ein großes Thema. Was genau?",
    options: [
      { label: "Folgen & Grenzwerte", icon: "", meta: "5 Module", next: "mathe_diff_grenz" },
      { label: "Ableitungen", icon: "", meta: "3 Module", next: "mathe_diff_abl" },
      { label: "Kurvenuntersuchung", icon: "", meta: "4 Module", next: "mathe_diff_kurve" }
    ]
  },

  mathe_diff_grenz: {
    question: "Folgen & Grenzwerte — wähle ein Modul:",
    options: [
      { label: "10 · Zahlenfolgen", icon: "", next: "leaf_d1" },
      { label: "11 · Grenzwerte von Folgen", icon: "", next: "leaf_d2" },
      { label: "12 · Grenzwerte im Unendlichen", icon: "", next: "leaf_d3" },
      { label: "13 · Grenzwerte an einer Stelle", icon: "", next: "leaf_d4" },
      { label: "14 · Asymptoten", icon: "", next: "leaf_d5" }
    ]
  },
  leaf_d1: {
    leaf: true, title: "Zahlenfolgen",
    desc: "Arithmetische und geometrische Folgen, Bildungsgesetze.",
    preview: [
      {
        label: "Arithmetische Folge",
        formulas: [
          { rule: "Allgemeines Glied", expr: "aₙ = a₁ + (n−1) · d", example: "d = konstante Differenz" },
          { rule: "Summe (Gauß)", expr: "Sₙ = n/2 · (a₁ + aₙ)", example: "z.B. 1+2+…+100 = 5050" }
        ]
      },
      {
        label: "Geometrische Folge",
        formulas: [
          { rule: "Allgemeines Glied", expr: "aₙ = a₁ · qⁿ⁻¹", example: "q = konstanter Quotient" },
          { rule: "Summe", expr: "Sₙ = a₁ · (qⁿ − 1) / (q − 1)", example: "für q ≠ 1" }
        ]
      }
    ],
    tip: "Arithmetisch: addieren. Geometrisch: multiplizieren. Am einfachsten durch Differenzen/Quotienten erkennen.",
    pdf: "/assets/pdfs/Zahlenfolgen_2_1.pdf", quiz: "/assets/quizzes/quiz_zahlenfolgen.html"
  },
  leaf_d2: {
    leaf: true, title: "Grenzwerte von Folgen",
    desc: "Konvergenz, Divergenz und Grenzwertbestimmung.",
    preview: [
      {
        label: "Grenzwertregeln",
        formulas: [
          { rule: "Grundgrenzwert", expr: "lim(1/nᵏ) = 0  für k > 0", example: "n → ∞" },
          { rule: "Geometrisch", expr: "lim(qⁿ) = 0  für |q| < 1", example: "n → ∞" }
        ]
      },
      {
        label: "Rechenregeln",
        formulas: [
          { rule: "Summe", expr: "lim(aₙ ± bₙ) = A ± B", example: "wenn aₙ→A, bₙ→B" },
          { rule: "Produkt", expr: "lim(aₙ · bₙ) = A · B", example: "" }
        ]
      }
    ],
    tip: "Bei Brüchen: Zähler und Nenner durch die höchste Potenz von n dividieren.",
    pdf: "/assets/pdfs/Grenzwerte_2_1.pdf", quiz: "/assets/quizzes/quiz_grenzwerte_folgen.html"
  },
  leaf_d3: {
    leaf: true, title: "Grenzwerte im Unendlichen",
    desc: "Verhalten von Funktionen für x → ±∞.",
    preview: [
      {
        label: "Polynome & Brüche",
        formulas: [
          { rule: "Polynom", expr: "lim xⁿ = ±∞", example: "höchste Potenz bestimmt Verhalten" },
          { rule: "Gebrochen-rational", expr: "Grad Zähler vs. Nenner", example: "gleich: Leitkoeffizient; Z<N: 0; Z>N: ±∞" }
        ]
      },
      {
        label: "Wichtige Grenzwerte",
        formulas: [
          { rule: "Exponential", expr: "lim eˣ = ∞,  lim e⁻ˣ = 0", example: "x → +∞" },
          { rule: "Logarithmus", expr: "lim ln(x) = ∞", example: "x → +∞" }
        ]
      }
    ],
    tip: "Bei gebrochen-rationalen Funktionen immer den Grad von Zähler und Nenner vergleichen.",
    pdf: "/assets/pdfs/Funktion_2_2.pdf", quiz: "/assets/quizzes/quiz_grenzwerte_funktionen_1.html"
  },
  leaf_d4: {
    leaf: true, title: "Grenzwerte an einer Stelle",
    desc: "Linksseitige und rechtsseitige Grenzwerte, Stetigkeit.",
    preview: [
      {
        label: "Einseitige Grenzwerte",
        formulas: [
          { rule: "Linksseitig", expr: "lim f(x) = L  (x → a⁻)", example: "von links annähern" },
          { rule: "Rechtsseitig", expr: "lim f(x) = L  (x → a⁺)", example: "von rechts annähern" }
        ]
      },
      {
        label: "Stetigkeit",
        formulas: [
          { rule: "Bedingung", expr: "lim f(x) = f(a)", example: "x → a von beiden Seiten" },
          { rule: "Unstetigkeitsstellen", expr: "Sprung, Lücke, Pol", example: "links ≠ rechts, nicht def., ±∞" }
        ]
      }
    ],
    tip: "Stetigkeit prüfen: (1) f(a) definiert? (2) Grenzwert existiert? (3) Grenzwert = Funktionswert?",
    pdf: "/assets/pdfs/Grenzwerte_2_2.pdf", quiz: "/assets/quizzes/quiz_grenzwerte_funktionen_2.html"
  },
  leaf_d5: {
    leaf: true, title: "Asymptoten",
    desc: "Horizontale, vertikale und schiefe Asymptoten bestimmen.",
    preview: [
      {
        label: "Typen",
        formulas: [
          { rule: "Vertikal (Pol)", expr: "x = a  wenn lim f(x) = ±∞", example: "Nenner = 0, Zähler ≠ 0" },
          { rule: "Horizontal", expr: "y = c  wenn lim f(x) = c", example: "x → ±∞" },
          { rule: "Schief", expr: "y = mx + b  per Polynomdivision", example: "Grad Zähler = Grad Nenner + 1" }
        ]
      }
    ],
    tip: "Schiefe Asymptote: Polynomdivision Zähler ÷ Nenner durchführen — der Rest ergibt keinen Beitrag für x → ±∞.",
    pdf: "/assets/pdfs/Grenzwerte_2_3.pdf", quiz: "/assets/quizzes/quiz_asymptoten.html"
  },

  mathe_diff_abl: {
    question: "Ableitungen — wähle ein Modul:",
    options: [
      { label: "15 · Steigung und Ableitung", icon: "", next: "leaf_d6" },
      { label: "16 · Ableitungsregeln", icon: "", next: "leaf_d7" },
      { label: "17 · Regel von de L'Hôpital", icon: "", next: "leaf_d8" }
    ]
  },
  leaf_d6: {
    leaf: true, title: "Steigung und Ableitung",
    desc: "Differenzenquotient, Differentialquotient und Ableitungsbegriff.",
    preview: [
      {
        label: "Vom Differenzen- zum Differentialquotienten",
        formulas: [
          { rule: "Differenzenquotient", expr: "Δy/Δx = (f(x+h)−f(x)) / h", example: "mittlere Steigung" },
          { rule: "Differentialquotient", expr: "f'(x) = lim[h→0] (f(x+h)−f(x)) / h", example: "momentane Steigung" }
        ]
      },
      {
        label: "Grundableitungen",
        formulas: [
          { rule: "Potenzfunktion", expr: "(xⁿ)' = n · xⁿ⁻¹", example: "(x³)' = 3x²" },
          { rule: "Konstante", expr: "(c)' = 0", example: "(5)' = 0" }
        ]
      }
    ],
    tip: "Der Differentialquotient ist der Grenzwert des Differenzenquotienten — geometrisch: Grenzlage der Sekante = Tangente.",
    pdf: "/assets/pdfs/Funktion_2_1.pdf", quiz: "/assets/quizzes/quiz_ableitung_grundlagen.html"
  },
  leaf_d7: {
    leaf: true, title: "Ableitungsregeln",
    desc: "Summen-, Produkt-, Quotienten- und Kettenregel.",
    preview: [
      {
        label: "Grundregeln",
        formulas: [
          { rule: "Faktorregel", expr: "(c · f)' = c · f'", example: "(3x²)' = 6x" },
          { rule: "Summenregel", expr: "(f ± g)' = f' ± g'", example: "(x³+x)' = 3x²+1" }
        ]
      },
      {
        label: "Produktregeln",
        formulas: [
          { rule: "Produktregel", expr: "(u · v)' = u'v + uv'", example: "(x·eˣ)' = eˣ + x·eˣ" },
          { rule: "Quotientenregel", expr: "(u/v)' = (u'v − uv') / v²", example: "Nenner² im Nenner" }
        ]
      },
      {
        label: "Verkettung",
        formulas: [
          { rule: "Kettenregel", expr: "(f(g(x)))' = f'(g(x)) · g'(x)", example: "(sin x²)' = cos x² · 2x" }
        ]
      }
    ],
    tip: "Kettenregel: äußere Funktion ableiten (innere stehen lassen), dann mal innere Ableitung.",
    pdf: "/assets/pdfs/Funktion_2_4.pdf", quiz: "/assets/quizzes/quiz_ableitungsregeln.html"
  },
  leaf_d8: {
    leaf: true, title: "Regel von de L'Hôpital",
    desc: "Grenzwertberechnung bei unbestimmten Ausdrücken 0/0 und ∞/∞.",
    preview: [
      {
        label: "Regel",
        formulas: [
          { rule: "Anwendung", expr: "lim f/g = lim f'/g'", example: "wenn lim f = lim g = 0 oder ∞" },
          { rule: "Mehrfach anwenden", expr: "solange unbestimmt bleibt", example: "bis bestimmter Ausdruck" }
        ]
      },
      {
        label: "Unbestimmte Formen",
        formulas: [
          { rule: "Direkt", expr: "0/0,   ∞/∞", example: "L'Hôpital direkt anwendbar" },
          { rule: "Umformen", expr: "0·∞,  ∞−∞,  0⁰,  1^∞", example: "erst in 0/0 oder ∞/∞ umschreiben" }
        ]
      }
    ],
    tip: "Voraussetzung prüfen: Liegt wirklich 0/0 oder ∞/∞ vor? Sonst ist L'Hôpital nicht erlaubt.",
    pdf: "/assets/pdfs/Hospital_2_1.pdf", quiz: "/assets/quizzes/quiz_hospital.html"
  },

  mathe_diff_kurve: {
    question: "Kurvenuntersuchung — wähle ein Modul:",
    options: [
      { label: "18 · Extrempunkte", icon: "", next: "leaf_d9" },
      { label: "19 · Wendepunkte", icon: "", next: "leaf_d10" },
      { label: "20 · Kurvendiskussion", icon: "", next: "leaf_d11" },
      { label: "21 · Extremwertaufgaben", icon: "", next: "leaf_d12" }
    ]
  },
  leaf_d9: {
    leaf: true, title: "Extrempunkte",
    desc: "Hoch- und Tiefpunkte bestimmen mit der 1. und 2. Ableitung.",
    preview: [
      {
        label: "Vorgehen",
        formulas: [
          { rule: "1. Notwendige Bedingung", expr: "f'(x₀) = 0", example: "kandidaten für Extrema" },
          { rule: "2. Hinreichend (2. Abl.)", expr: "f''(x₀) < 0 → Maximum", example: "f''(x₀) > 0 → Minimum" },
          { rule: "Alternativ (VZW)", expr: "f' wechselt Vorzeichen bei x₀", example: "+→− : Max,   −→+ : Min" }
        ]
      }
    ],
    tip: "f''(x₀) = 0 ist kein Ergebnis — dann Vorzeichenwechsel der ersten Ableitung prüfen.",
    pdf: "/assets/pdfs/Extremwert_2_1.pdf", quiz: "/assets/quizzes/quiz_extrempunkte.html"
  },
  leaf_d10: {
    leaf: true, title: "Wendepunkte",
    desc: "Wendepunkte und Krümmungsverhalten analysieren.",
    preview: [
      {
        label: "Wendepunkt",
        formulas: [
          { rule: "Notwendig", expr: "f''(x₀) = 0", example: "Kandidaten für Wendepunkte" },
          { rule: "Hinreichend", expr: "f'''(x₀) ≠ 0", example: "VZW von f'' bei x₀" }
        ]
      },
      {
        label: "Krümmung",
        formulas: [
          { rule: "Linkskrümmung", expr: "f''(x) > 0", example: "konvex, Schale nach oben" },
          { rule: "Rechtskrümmung", expr: "f''(x) < 0", example: "konkav, Schale nach unten" }
        ]
      }
    ],
    tip: "Sattelpunkt: Wendepunkt mit f'(x₀) = 0 — Extrempunkt-Kriterium fällt aus, aber auch kein Extremum.",
    pdf: "/assets/pdfs/Wendepunkt_2_1.pdf", quiz: "/assets/quizzes/quiz_wendepunkte.html"
  },
  leaf_d11: {
    leaf: true, title: "Kurvendiskussion",
    desc: "Vollständige Untersuchung einer Funktion.",
    preview: [
      {
        label: "Standardschritte",
        formulas: [
          { rule: "1. Definitionsbereich", expr: "D = ℝ  oder Ausnahmen angeben", example: "Polstellen ausschließen" },
          { rule: "2. Symmetrie", expr: "f(−x)=f(x): gerade; =−f(x): ungerade", example: "" },
          { rule: "3. Nullstellen", expr: "f(x) = 0 lösen", example: "" },
          { rule: "4. Extrema & Wendepunkte", expr: "f', f'', f''' berechnen", example: "" },
          { rule: "5. Asymptoten", expr: "Verhalten für x → ±∞, Pole", example: "" }
        ]
      }
    ],
    tip: "Reihenfolge einhalten — Symmetrie zuerst, spart oft Rechenarbeit bei späteren Schritten.",
    pdf: "/assets/pdfs/Kurvendiskusion_2_1.pdf", quiz: "/assets/quizzes/quiz_kurvendiskussion.html"
  },
  leaf_d12: {
    leaf: true, title: "Extremwertaufgaben",
    desc: "Optimierungsprobleme aus der Praxis lösen.",
    preview: [
      {
        label: "Lösungsschema",
        formulas: [
          { rule: "1. Zielfunktion", expr: "Z = f(x, y, …) aufstellen", example: "was wird optimiert?" },
          { rule: "2. Nebenbedingung", expr: "Constraint in Z einsetzen", example: "auf eine Variable reduzieren" },
          { rule: "3. Ableiten & Nullsetzen", expr: "Z'(x) = 0 → Kandidat", example: "" },
          { rule: "4. Überprüfen", expr: "Z'' > 0: Min;  Z'' < 0: Max", example: "Randwerte nicht vergessen" }
        ]
      }
    ],
    tip: "Randbedingungen am Ende prüfen: Oft liegt das Optimum am Rand des Definitionsbereichs.",
    pdf: "/assets/pdfs/Extrem_2_1.pdf", quiz: "/assets/quizzes/quiz_extremwertaufgaben.html"
  },

  // Integralrechnung
  mathe_integral: {
    question: "Integralrechnung — wähle ein Modul:",
    options: [
      { label: "22 · Einführung", icon: "", next: "leaf_i1" },
      { label: "23 · Integrationsmethoden", icon: "", next: "leaf_i2" },
      { label: "24 · Hauptsatz & Flächen", icon: "", next: "leaf_i3" },
      { label: "25 · Rotationsvolumen", icon: "", next: "leaf_i4" }
    ]
  },
  leaf_i1: {
    leaf: true, title: "Einführung in die Integralrechnung",
    desc: "Stammfunktionen und unbestimmtes Integral.",
    preview: [
      {
        label: "Grundintegrale",
        formulas: [
          { rule: "Potenzregel", expr: "∫ xⁿ dx = xⁿ⁺¹/(n+1) + C", example: "für n ≠ −1" },
          { rule: "Logarithmus", expr: "∫ 1/x dx = ln|x| + C", example: "" },
          { rule: "Exponential", expr: "∫ eˣ dx = eˣ + C", example: "" },
          { rule: "Trigonometrie", expr: "∫ sin x dx = −cos x + C", example: "∫ cos x dx = sin x + C" }
        ]
      }
    ],
    tip: "Integrationskonstante C nie vergessen beim unbestimmten Integral.",
    pdf: "/assets/pdfs/Integral_2_1.pdf", quiz: "/assets/quizzes/quiz_integral_einfuehrung.html"
  },
  leaf_i2: {
    leaf: true, title: "Integrationsmethoden",
    desc: "Substitution, partielle Integration und Partialbruchzerlegung.",
    preview: [
      {
        label: "Substitution",
        formulas: [
          { rule: "Schema", expr: "∫ f(g(x))·g'(x) dx", example: "u = g(x),  du = g'(x) dx" }
        ]
      },
      {
        label: "Partielle Integration",
        formulas: [
          { rule: "Formel", expr: "∫ u·v' dx = u·v − ∫ u'·v dx", example: "LIATE-Reihenfolge für u" }
        ]
      },
      {
        label: "Partialbruch",
        formulas: [
          { rule: "Ansatz", expr: "P(x)/Q(x) = A/(x−a) + B/(x−b)", example: "Q(x) in Linearfaktoren zerlegen" }
        ]
      }
    ],
    tip: "LIATE für partielle Integration: Logarithmus, Invers-trigo, Algebraisch, Trigo, Exponential — das ist die bevorzugte Reihenfolge für u.",
    pdf: "/assets/pdfs/Integral_2_2.pdf", quiz: "/assets/quizzes/quiz_integrationsmethoden.html"
  },
  leaf_i3: {
    leaf: true, title: "Hauptsatz & Flächen",
    desc: "Hauptsatz der Differential- und Integralrechnung, Flächenberechnung.",
    preview: [
      {
        label: "Hauptsatz",
        formulas: [
          { rule: "Berechnung", expr: "∫ₐᵇ f(x) dx = F(b) − F(a)", example: "F = Stammfunktion von f" }
        ]
      },
      {
        label: "Flächenberechnung",
        formulas: [
          { rule: "Fläche zwischen Kurve & x-Achse", expr: "A = ∫ₐᵇ |f(x)| dx", example: "Betragsstriche! Nullstellen prüfen" },
          { rule: "Zwischen zwei Kurven", expr: "A = ∫ₐᵇ |f(x) − g(x)| dx", example: "Schnittpunkte als Grenzen" }
        ]
      }
    ],
    tip: "Vorzeichen beachten: Flächen unter der x-Achse geben negative Integralwerte — deshalb Betragsstriche.",
    pdf: "/assets/pdfs/Integral_2_3.pdf", quiz: "/assets/quizzes/quiz_hauptsatz_flaechen.html"
  },
  leaf_i4: {
    leaf: true, title: "Rotationsvolumen",
    desc: "Volumenberechnung von Rotationskörpern.",
    preview: [
      {
        label: "Rotation um x-Achse",
        formulas: [
          { rule: "Formel", expr: "V = π · ∫ₐᵇ [f(x)]² dx", example: "Rotation um die x-Achse" }
        ]
      },
      {
        label: "Rotation um y-Achse",
        formulas: [
          { rule: "Formel", expr: "V = π · ∫_c^d [g(y)]² dy", example: "f nach x auflösen: x = g(y)" }
        ]
      }
    ],
    tip: "Das π vor dem Integral nicht vergessen — es entsteht aus der Kreisfläche π·r² mit r = f(x).",
    pdf: "/assets/pdfs/Intergal_2_4-2.pdf", quiz: "/assets/quizzes/quiz_rotationsvolumen.html"
  },

  // Interaktive Tools
  mathe_tools: {
    question: "Interaktive Tools — wähle ein Tool:",
    options: [
      { label: "Tangenten-Explorer", icon: "", next: "leaf_t1" },
      { label: "3D-Vektor-Explorer", icon: "", next: "leaf_t2" },
      { label: "Geraden & Ebenen", icon: "", next: "leaf_t3" },
      { label: "Matrizen-Explorer", icon: "", next: "leaf_t4" },
      { label: "Determinanten-Rechner", icon: "", next: "leaf_t5" }
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
      { label: "Mikroökonomie", icon: "", meta: "8 Module · Angebot, Nachfrage, Märkte", next: "vwl_mikro" },
      { label: "Makroökonomie", icon: "", meta: "6 Module · BIP, Konjunktur, Arbeitsmarkt", next: "vwl_makro" }
    ]
  },

  vwl_mikro: {
    question: "Mikroökonomie — wähle ein Modul:",
    options: [
      { label: "01 · Bedürfnis, Bedarf und Nachfrage", icon: "", next: "leaf_m1" },
      { label: "02 · Güterarten in der Wirtschaft", icon: "", next: "leaf_m2" },
      { label: "03 · Angebot und Angebotskurve", icon: "", next: "leaf_m3" },
      { label: "04 · Nachfrage und Nachfragekurve", icon: "", next: "leaf_m4" },
      { label: "05 · Marktgleichgewicht", icon: "", next: "leaf_m5" },
      { label: "06 · Konsumenten- und Produzentenrente", icon: "", next: "leaf_m6" },
      { label: "07 · Marktformen", icon: "", next: "leaf_m7" },
      { label: "08 · Budgetgerade", icon: "", next: "leaf_m8" }
    ]
  },
  leaf_m1: {
    leaf: true, title: "Bedürfnis, Bedarf und Nachfrage",
    desc: "Grundbegriffe der Volkswirtschaftslehre und das ökonomische Prinzip.",
    preview: [
      {
        label: "Begriffe & Prinzip",
        formulas: [
          { rule: "Ökonomisches Prinzip", expr: "Minimalprinzip: Ziel mit minimalem Einsatz", example: "oder: Maximalprinzip" },
          { rule: "Bedürfnis → Bedarf", expr: "Bedürfnis + Kaufkraft = Bedarf", example: "Bedarf + Kaufakt = Nachfrage" }
        ]
      },
      {
        label: "Bedürfnispyramide (Maslow)",
        formulas: [
          { rule: "Hierarchie", expr: "Physiologisch → Sicherheit → Sozial → Wertschätzung → Selbstverwirklichung", example: "niedrigere Ebenen zuerst" }
        ]
      }
    ],
    tip: "Unterschied merken: Bedürfnis (subjektiv) → Bedarf (konkretisiert) → Nachfrage (zahlungswirksam).",
    pdf: "/assets/pdfs/WS_VWL_1-3.pdf", quiz: "/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html"
  },
  leaf_m2: {
    leaf: true, title: "Güterarten in der Wirtschaft",
    desc: "Freie und wirtschaftliche Güter, Konsum- und Investitionsgüter.",
    preview: [
      {
        label: "Klassifikationen",
        formulas: [
          { rule: "Knappheit", expr: "Freie Güter (Luft) vs. Wirtschaftsgüter", example: "Wirtschaftsgüter = knapp" },
          { rule: "Verwendung", expr: "Konsumgüter vs. Investitionsgüter", example: "Verbrauch vs. Produktion" },
          { rule: "Ausschließbarkeit", expr: "Öffentlich vs. Privat", example: "Rivalität & Ausschließbarkeit" }
        ]
      }
    ],
    tip: "Öffentliche Güter: nicht-rival + nicht-ausschließbar (z.B. Straßenbeleuchtung). Führt zu Marktversagen.",
    pdf: "/assets/pdfs/WS_VWL_2-2.pdf", quiz: "/assets/quizzes/quiz_gueterarten.html"
  },
  leaf_m3: {
    leaf: true, title: "Angebot und Angebotskurve",
    desc: "Das Gesetz des Angebots und Verschiebungen der Kurve.",
    preview: [
      {
        label: "Gesetz des Angebots",
        formulas: [
          { rule: "Grundprinzip", expr: "Preis ↑  →  Angebotsmenge ↑", example: "positive Steigung der Kurve" }
        ]
      },
      {
        label: "Kurvenverschiebungen",
        formulas: [
          { rule: "Rechtsverschiebung (mehr)", expr: "Produktionskosten ↓, Technologie ↑", example: "oder: mehr Anbieter" },
          { rule: "Linksverschiebung (weniger)", expr: "Input-Preise ↑, Steuern ↑", example: "oder: Naturkatastrophe" }
        ]
      }
    ],
    tip: "Bewegung auf der Kurve (Preisänderung) vs. Verschiebung der Kurve (alle anderen Faktoren) unterscheiden.",
    pdf: "/assets/pdfs/WS_VWL_3-4.pdf", quiz: "/assets/quizzes/quiz_angebot.html"
  },
  leaf_m4: {
    leaf: true, title: "Nachfrage und Nachfragekurve",
    desc: "Das Gesetz der Nachfrage, Preis- und Einkommenseffekte.",
    preview: [
      {
        label: "Gesetz der Nachfrage",
        formulas: [
          { rule: "Grundprinzip", expr: "Preis ↑  →  Nachfragemenge ↓", example: "negative Steigung der Kurve" }
        ]
      },
      {
        label: "Kurvenverschiebungen",
        formulas: [
          { rule: "Rechtsverschiebung (mehr)", expr: "Einkommen ↑, Präferenzen ↑", example: "oder: Substitut teurer" },
          { rule: "Linksverschiebung (weniger)", expr: "Einkommen ↓, Komplement teurer", example: "oder: Erwartungen negativ" }
        ]
      }
    ],
    tip: "Giffen-Gut: Ausnahme vom Gesetz der Nachfrage — Preis ↑ → Nachfrage ↑ (sehr seltenes Phänomen).",
    pdf: "/assets/pdfs/WS_VWL_4-2.pdf", quiz: "/assets/quizzes/quiz_nachfrage.html"
  },
  leaf_m5: {
    leaf: true, title: "Marktgleichgewicht",
    desc: "Gleichgewichtspreis und -menge, Störungen des Gleichgewichts.",
    preview: [
      {
        label: "Gleichgewicht",
        formulas: [
          { rule: "Bedingung", expr: "Qₐ(p*) = Qₙ(p*)", example: "p* = Gleichgewichtspreis" },
          { rule: "Berechnung", expr: "Angebotsfunktion = Nachfragefunktion", example: "nach p auflösen" }
        ]
      },
      {
        label: "Marktungleichgewichte",
        formulas: [
          { rule: "Überschussangebot", expr: "p > p*  →  Qₐ > Qₙ", example: "Preis sinkt" },
          { rule: "Überschussnachfrage", expr: "p < p*  →  Qₙ > Qₐ", example: "Preis steigt" }
        ]
      }
    ],
    tip: "Algebraisch: Angebots- und Nachfragefunktion gleichsetzen und nach p auflösen, dann Menge einsetzen.",
    pdf: "/assets/pdfs/WS_VWL_5-2.pdf", quiz: "/assets/quizzes/quiz_marktgleichgewicht.html"
  },
  leaf_m6: {
    leaf: true, title: "Konsumenten- und Produzentenrente",
    desc: "Wohlfahrtsanalyse und Renten im Marktmodell.",
    preview: [
      {
        label: "Renten",
        formulas: [
          { rule: "Konsumentenrente", expr: "KR = Zahlungsbereitschaft − tatsächlicher Preis", example: "Fläche über p* unter Nachfragekurve" },
          { rule: "Produzentenrente", expr: "PR = tatsächlicher Preis − Mindestpreis", example: "Fläche unter p* über Angebotskurve" },
          { rule: "Gesamtwohlfahrt", expr: "W = KR + PR", example: "Maximal im Gleichgewicht" }
        ]
      }
    ],
    tip: "Wohlfahrtsverlust (Deadweight Loss) entsteht bei Preiskontrollen oder Monopol — grafisch als Dreieck erkennbar.",
    pdf: "/assets/pdfs/WS_VWL_6.pdf", quiz: "/assets/quizzes/quiz_renten.html"
  },
  leaf_m7: {
    leaf: true, title: "Marktformen",
    desc: "Polypol, Oligopol und Monopol im Vergleich.",
    preview: [
      {
        label: "Klassifikation",
        formulas: [
          { rule: "Polypol", expr: "viele Anbieter, viele Nachfrager", example: "vollständiger Wettbewerb" },
          { rule: "Oligopol", expr: "wenige Anbieter, viele Nachfrager", example: "strategische Interdependenz" },
          { rule: "Monopol", expr: "ein Anbieter, viele Nachfrager", example: "Preissetzungsmacht" }
        ]
      },
      {
        label: "Monopol",
        formulas: [
          { rule: "Gewinnmaximierung", expr: "Grenzerlös = Grenzkosten: MR = MC", example: "p > MC im Monopol" }
        ]
      }
    ],
    tip: "Im Polypol ist der Anbieter Preisnehmer (p = MC). Im Monopol ist er Preissetzer (p > MC = Wohlfahrtsverlust).",
    pdf: "/assets/pdfs/WS_VWL_7.pdf", quiz: "/assets/quizzes/quiz_marktformen.html"
  },
  leaf_m8: {
    leaf: true, title: "Budgetgerade",
    desc: "Budgetbeschränkung, optimale Konsumentscheidung.",
    preview: [
      {
        label: "Budgetgerade",
        formulas: [
          { rule: "Gleichung", expr: "p₁·x₁ + p₂·x₂ = I", example: "I = Einkommen, p = Preise" },
          { rule: "Steigung", expr: "−p₁/p₂", example: "relatives Preisverhältnis" }
        ]
      },
      {
        label: "Optimum",
        formulas: [
          { rule: "Tangentialbedingung", expr: "MRS = p₁/p₂", example: "Indifferenzkurve berührt Budgetgerade" },
          { rule: "MRS", expr: "MRS = MU₁/MU₂", example: "Grenznutzenrate" }
        ]
      }
    ],
    tip: "Einkommensänderung: Parallelverschiebung der Budgetgeraden. Preisänderung: Drehung der Budgetgeraden.",
    pdf: "/assets/pdfs/WS_VWL_8-3.pdf", quiz: "/assets/quizzes/quiz_budgetgerade.html"
  },

  vwl_makro: {
    question: "Makroökonomie — wähle ein Modul:",
    options: [
      { label: "09 · Volkswirtschaftliche Gesamtrechnung", icon: "", next: "leaf_m9" },
      { label: "10 · Nominales vs. reales BIP", icon: "", next: "leaf_m10" },
      { label: "11 · Konjunktur & Konjunkturzyklen", icon: "", next: "leaf_m11" },
      { label: "12 · Antizyklische Konjunkturpolitik", icon: "", next: "leaf_m12" },
      { label: "13 · Arbeitslosigkeit & Arbeitsmarktpolitik", icon: "", next: "leaf_m13" },
      { label: "14 · Inflation & Preisniveaustabilität", icon: "", next: "leaf_m14" }
    ]
  },
  leaf_m9: {
    leaf: true, title: "Volkswirtschaftliche Gesamtrechnung",
    desc: "BIP-Berechnung: Entstehungs-, Verwendungs- und Verteilungsrechnung.",
    preview: [
      {
        label: "Drei Methoden (identisch)",
        formulas: [
          { rule: "Verwendung", expr: "BIP = C + I + G + (Ex − Im)", example: "C=Konsum, I=Invest., G=Staat" },
          { rule: "Entstehung", expr: "BIP = Σ Bruttowertschöpfung", example: "abzüglich Vorleistungen" },
          { rule: "Verteilung", expr: "BIP = Arbeitnehmerentgelt + Unternehmensgewinne + Abschreibungen + Steuern", example: "" }
        ]
      }
    ],
    tip: "Alle drei Methoden liefern dasselbe Ergebnis — das ist kein Zufall, sondern ein buchhalterisches Identitätsprinzip.",
    pdf: "/assets/pdfs/VWL_11.pdf", quiz: "/assets/quizzes/quiz_vgr.html"
  },
  leaf_m10: {
    leaf: true, title: "Nominales vs. reales BIP",
    desc: "Preisbereinigung, BIP-Deflator und Kaufkraftvergleiche.",
    preview: [
      {
        label: "Formeln",
        formulas: [
          { rule: "Reales BIP", expr: "Reales BIP = Nominales BIP / BIP-Deflator × 100", example: "" },
          { rule: "BIP-Deflator", expr: "Deflator = (Nominales BIP / Reales BIP) × 100", example: "Basisjahr: Deflator = 100" },
          { rule: "Wachstumsrate", expr: "g = (BIPₜ − BIPₜ₋₁) / BIPₜ₋₁ × 100%", example: "immer reales BIP verwenden" }
        ]
      }
    ],
    tip: "Reales BIP verwendet Preise eines Basisjahres — eliminiert Inflation und zeigt echtes Mengenwachstum.",
    pdf: "/assets/pdfs/VWL_12.pdf", quiz: "/assets/quizzes/quiz_vgr2.html"
  },
  leaf_m11: {
    leaf: true, title: "Konjunktur & Konjunkturzyklen",
    desc: "Aufschwung, Boom, Abschwung und Rezession verstehen.",
    preview: [
      {
        label: "Phasen des Zyklus",
        formulas: [
          { rule: "Aufschwung (Expansion)", expr: "BIP-Wachstum ↑, Arbeitslosigkeit ↓", example: "" },
          { rule: "Boom (Hochkonjunktur)", expr: "Vollbeschäftigung, Inflation ↑", example: "Überauslastung möglich" },
          { rule: "Abschwung (Kontraktion)", expr: "BIP-Wachstum ↓, Lagerabbau", example: "" },
          { rule: "Rezession", expr: "2 Quartale neg. BIP-Wachstum", example: "Arbeitslosigkeit steigt" }
        ]
      }
    ],
    tip: "Rezession = technisch definiert als zwei aufeinanderfolgende Quartale mit negativem Wachstum.",
    pdf: "/assets/pdfs/VWL_11_Konjunktur.pdf", quiz: "/assets/quizzes/quiz_konjunktur.html"
  },
  leaf_m12: {
    leaf: true, title: "Antizyklische Konjunkturpolitik",
    desc: "Fiskal- und Geldpolitik zur Stabilisierung der Wirtschaft.",
    preview: [
      {
        label: "Instrumente",
        formulas: [
          { rule: "Fiskalpolitik (expansiv)", expr: "G ↑ oder Steuern ↓  →  BIP ↑", example: "in der Rezession" },
          { rule: "Fiskalpolitik (restriktiv)", expr: "G ↓ oder Steuern ↑  →  BIP ↓", example: "im Boom" },
          { rule: "Geldpolitik (expansiv)", expr: "Zinsen ↓  →  Kredite ↑  →  I ↑", example: "EZB senkt Leitzins" },
          { rule: "Geldpolitik (restriktiv)", expr: "Zinsen ↑  →  Investitionen ↓", example: "gegen Inflation" }
        ]
      }
    ],
    tip: "Antizyklisch = gegen den Zyklus: In der Rezession stimulieren, im Boom bremsen.",
    pdf: "/assets/pdfs/VWL_12_Konjunkturpolitik.pdf", quiz: "/assets/quizzes/quiz_konjunkturpolitik.html"
  },
  leaf_m13: {
    leaf: true, title: "Arbeitslosigkeit & Arbeitsmarktpolitik",
    desc: "Arten der Arbeitslosigkeit und politische Gegenmaßnahmen.",
    preview: [
      {
        label: "Arten der Arbeitslosigkeit",
        formulas: [
          { rule: "Friktionell", expr: "Übergang zwischen Jobs", example: "kurzfristig, unvermeidlich" },
          { rule: "Strukturell", expr: "Qualifikationsmismatch", example: "Umschulung nötig" },
          { rule: "Konjunkturell", expr: "fehlende Nachfrage", example: "in Rezessionen" },
          { rule: "Saisonell", expr: "Jahreszeit-bedingt", example: "Bau, Tourismus" }
        ]
      },
      {
        label: "Kennzahl",
        formulas: [
          { rule: "Arbeitslosenquote", expr: "ALQ = (Arbeitslose / Erwerbspersonen) × 100%", example: "" }
        ]
      }
    ],
    tip: "Natürliche Arbeitslosigkeit = friktionell + strukturell — kann nicht durch Konjunkturpolitik beseitigt werden.",
    pdf: "/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf", quiz: "/assets/quizzes/quiz_arbeitslosigkeit.html"
  },
  leaf_m14: {
    leaf: true, title: "Inflation & Preisniveaustabilität",
    desc: "Ursachen und Folgen von Inflation, Rolle der Zentralbank.",
    preview: [
      {
        label: "Messung",
        formulas: [
          { rule: "Inflationsrate", expr: "π = (Pₜ − Pₜ₋₁) / Pₜ₋₁ × 100%", example: "P = Preisniveau (VPI)" },
          { rule: "Ziel EZB", expr: "π ≈ 2% (mittelfristig)", example: "Preisniveaustabilität" }
        ]
      },
      {
        label: "Ursachen",
        formulas: [
          { rule: "Nachfragesog", expr: "Nachfrage ↑ bei konstantem Angebot", example: "demand-pull" },
          { rule: "Kostendruck", expr: "Produktionskosten ↑ → Preise ↑", example: "cost-push, z.B. Ölpreisschock" },
          { rule: "Geldmenge", expr: "M ↑ → langfristig π ↑", example: "Quantitätstheorie: MV = PY" }
        ]
      }
    ],
    tip: "Quantitätsgleichung: MV = PY — Geldmenge × Umlaufgeschwindigkeit = Preisniveau × reales BIP.",
    pdf: "/assets/pdfs/VWL_14_Preisniveau.pdf", quiz: "/assets/quizzes/quiz_preisniveau.html"
  },

  // ─── INFORMATIK ───
  info: {
    question: "Informatik (Python) — wähle ein Modul:",
    options: [
      { label: "01 · Python Grundlagen – print() und input()", icon: "", next: "leaf_p1" },
      { label: "02 · Variablen und Datentypen", icon: "", next: "leaf_p2" },
      { label: "03 · Listen und Datenstrukturen", icon: "", next: "leaf_p3" },
      { label: "04 · Kontrollstrukturen – if, for, while", icon: "", next: "leaf_p4" },
      { label: "05 · Funktionen in Python", icon: "", next: "leaf_p5" },
      { label: "06 · NumPy – Kurvendiskussion & Ableitungen", icon: "", next: "leaf_p6" }
    ]
  },
  leaf_p1: {
    leaf: true, title: "Python Grundlagen – print() und input()",
    desc: "Erste Schritte: Ausgabe, Eingabe und der Python-Interpreter.",
    preview: [
      {
        label: "Ausgabe",
        formulas: [
          { rule: "print()", expr: 'print("Hallo Welt")', example: 'print("x =", x)  # mehrere Werte' },
          { rule: "f-String", expr: 'print(f"x = {x}")', example: "Variablen direkt einbetten" }
        ]
      },
      {
        label: "Eingabe",
        formulas: [
          { rule: "input()", expr: 'name = input("Dein Name: ")', example: "gibt immer einen String zurück" },
          { rule: "Typumwandlung", expr: 'x = int(input("Zahl: "))', example: "nötig für Rechenoperationen" }
        ]
      }
    ],
    tip: "input() gibt immer str zurück — für Berechnungen immer int() oder float() drum herum.",
    pdf: "/assets/pdfs/Info_1.pdf", quiz: "/assets/quizzes/quiz_python_grundlage.html"
  },
  leaf_p2: {
    leaf: true, title: "Variablen und Datentypen",
    desc: "int, float, str, bool und Typumwandlungen.",
    preview: [
      {
        label: "Datentypen",
        formulas: [
          { rule: "int", expr: "x = 42", example: "ganze Zahlen" },
          { rule: "float", expr: "x = 3.14", example: "Dezimalzahlen" },
          { rule: "str", expr: 'x = "Hallo"', example: "Zeichenketten" },
          { rule: "bool", expr: "x = True", example: "True / False" }
        ]
      },
      {
        label: "Typumwandlung",
        formulas: [
          { rule: "Konvertierung", expr: "int(x),  float(x),  str(x)", example: 'int("42") → 42' },
          { rule: "Typ prüfen", expr: "type(x)", example: 'type(42) → <class "int">' }
        ]
      }
    ],
    tip: "Python ist dynamisch typisiert — der Typ einer Variable kann sich ändern. Mit type() immer prüfbar.",
    pdf: "/assets/pdfs/Info_2.pdf", quiz: "/assets/quizzes/quiz_variablen_datentypen.html"
  },
  leaf_p3: {
    leaf: true, title: "Listen und Datenstrukturen",
    desc: "Listen, Tupel, Dictionaries und ihre Methoden.",
    preview: [
      {
        label: "Liste",
        formulas: [
          { rule: "Erstellen", expr: "lst = [1, 2, 3]", example: "veränderbar, geordnet" },
          { rule: "Zugriff", expr: "lst[0],  lst[-1]", example: "Index ab 0, negativ von hinten" },
          { rule: "Methoden", expr: "lst.append(x),  lst.pop()", example: "hinzufügen, entfernen" }
        ]
      },
      {
        label: "Dictionary",
        formulas: [
          { rule: "Erstellen", expr: 'd = {"key": "value"}', example: "Schlüssel-Wert-Paare" },
          { rule: "Zugriff", expr: 'd["key"]', example: 'd.get("key", default)' }
        ]
      }
    ],
    tip: "Listen: geordnet, mit Duplikaten. Dictionaries: Schlüssel müssen eindeutig sein.",
    pdf: "/assets/pdfs/Info_3.pdf", quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html"
  },
  leaf_p4: {
    leaf: true, title: "Kontrollstrukturen – if, for, while",
    desc: "Bedingte Anweisungen und Schleifen in Python.",
    preview: [
      {
        label: "if-Anweisung",
        formulas: [
          { rule: "Syntax", expr: "if Bedingung:\n    ...\nelif ...:\n    ...\nelse:\n    ...", example: "Einrückung = Block" }
        ]
      },
      {
        label: "Schleifen",
        formulas: [
          { rule: "for-Schleife", expr: "for i in range(n):", example: "range(5) → 0,1,2,3,4" },
          { rule: "while-Schleife", expr: "while Bedingung:", example: "läuft bis Bedingung falsch" }
        ]
      }
    ],
    tip: "break beendet die Schleife sofort, continue springt zur nächsten Iteration.",
    pdf: "/assets/pdfs/Info_4.pdf", quiz: "/assets/quizzes/quiz_kontrollstrukturen.html"
  },
  leaf_p5: {
    leaf: true, title: "Funktionen in Python",
    desc: "Eigene Funktionen definieren, Parameter und Rückgabewerte.",
    preview: [
      {
        label: "Definition & Aufruf",
        formulas: [
          { rule: "def", expr: "def name(param1, param2):\n    return ergebnis", example: "Einrückung beachten" },
          { rule: "Standardwert", expr: "def f(x, n=2):", example: "n optional mit Default 2" }
        ]
      },
      {
        label: "Scope",
        formulas: [
          { rule: "Lokale Variable", expr: "innerhalb der Funktion", example: "außen nicht sichtbar" },
          { rule: "global", expr: "global x  # Zugriff auf globale Variable", example: "sparsam verwenden" }
        ]
      }
    ],
    tip: "Ohne return gibt eine Funktion None zurück. return beendet die Funktion sofort.",
    pdf: "/assets/pdfs/Info_5.pdf", quiz: "/assets/quizzes/quiz_funktionen.html"
  },
  leaf_p6: {
    leaf: true, title: "NumPy – Kurvendiskussion & Ableitungen",
    desc: "Numerische Mathematik mit NumPy: Ableitungen und Kurvenanalyse.",
    preview: [
      {
        label: "NumPy Grundlagen",
        formulas: [
          { rule: "Import", expr: "import numpy as np", example: "Konvention: np als Alias" },
          { rule: "Array", expr: "x = np.linspace(a, b, n)", example: "n gleichmäßige Punkte in [a,b]" }
        ]
      },
      {
        label: "Ableitung & Analyse",
        formulas: [
          { rule: "Numerische Ableitung", expr: "dy = np.diff(y) / np.diff(x)", example: "Vorwärtsdifferenz" },
          { rule: "Nullstellen", expr: "np.roots([a, b, c])", example: "Koeffizienten des Polynoms" }
        ]
      }
    ],
    tip: "np.linspace(0, 10, 1000) erzeugt 1000 Punkte — für glatte Graphen immer genug Punkte wählen.",
    pdf: "/assets/pdfs/Info_6.pdf", quiz: "/assets/quizzes/quiz_numpy_kurvendiskussion.html"
  }
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

function renderPreview(preview, tip) {
  if (!preview || preview.length === 0) return '';
  let html = '<div class="tree-preview">';
  for (const section of preview) {
    html += '<div class="tree-preview-section">';
    html += `<div class="tree-preview-label">${section.label}</div>`;
    const single = section.formulas.length === 1;
    html += `<div class="tree-formula-grid${single ? ' tree-formula-grid--single' : ''}">`;
    for (const f of section.formulas) {
      html += `<div class="tree-formula-card">
        <div class="tree-formula-rule">${f.rule}</div>
        <div class="tree-formula-expr">${f.expr}</div>
        ${f.example ? `<div class="tree-formula-example">${f.example}</div>` : ''}
      </div>`;
    }
    html += '</div></div>';
  }
  if (tip) {
    html += `<div class="tree-preview-tip">${tip}</div>`;
  }
  html += '</div>';
  return html;
}

function renderNode(nodeId) {
  currentNode = nodeId;
  const node = TREE[nodeId];
  const contentEl = document.getElementById('treeContent');
  const footerEl = document.getElementById('treeFooter');
  const breadcrumbEl = document.getElementById('breadcrumb');

  contentEl.innerHTML = '';
  renderBreadcrumb(breadcrumbEl);
  footerEl.style.display = nodeId === 'root' ? 'none' : 'flex';

  if (node.leaf) {
    const questionHTML = `
      <div class="tree-question">
        <div class="tree-avatar">STK</div>
        <div class="tree-bubble"><p>Hier ist dein Material:</p></div>
      </div>
    `;

    let actionsHTML = '';
    if (node.pdf) actionsHTML += `<a href="${node.pdf}" class="tree-leaf-btn tree-leaf-btn--pdf" target="_blank">PDF öffnen</a>`;
    if (node.quiz) actionsHTML += `<a href="${node.quiz}" class="tree-leaf-btn tree-leaf-btn--quiz" target="_blank">Quiz starten</a>`;
    if (node.tool) actionsHTML += `<a href="${node.tool}" class="tree-leaf-btn tree-leaf-btn--tool" target="_blank">Tool öffnen</a>`;

    const leafHTML = `
      <div class="tree-leaf">
        <div class="tree-leaf-card">
          <h4>${node.title}</h4>
          <p class="tree-leaf-desc">${node.desc}</p>
          ${renderPreview(node.preview, node.tip)}
          <div class="tree-leaf-actions">${actionsHTML}</div>
        </div>
      </div>
    `;

    contentEl.innerHTML = questionHTML + leafHTML;
  } else {
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
  let html = `<button class="tree-breadcrumb-item" onclick="jumpTo(0)">Start</button>`;
  for (let i = 0; i < history.length; i++) {
    const id = history[i];
    const name = NODE_NAMES[id] || id;
    html += `<span class="tree-breadcrumb-sep">›</span>`;
    html += `<button class="tree-breadcrumb-item" onclick="jumpTo(${i + 1})">${name}</button>`;
  }
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
  if (index === 0) { goHome(); return; }
  const targetNode = history[index - 1];
  history = history.slice(0, index - 1);
  renderNode(targetNode);
}

renderNode('root');
</script>