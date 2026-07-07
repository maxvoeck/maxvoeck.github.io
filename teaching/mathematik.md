---
layout: page
title: 
permalink: /teaching/mathematik/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
/* ═══════════════════════════════════════════════════════
   NACHTPROGRAMM — Mathematik für das Studienkolleg
   Konzertprogramm-Ästhetik: Tinte, Elfenbein, Messing
   ═══════════════════════════════════════════════════════ */
:root {
  --ink:      #101014;
  --graphit:  #17171d;
  --graphit2: #1e1e26;
  --linie:    rgba(236, 231, 220, 0.09);
  --linie2:   rgba(236, 231, 220, 0.18);
  --elfenbein:#ece7dc;
  --nebel:    #8f8e97;
  --messing:  #c2a15c;
  --messing2: #dfc48a;
  --gruen:    #8fa284;

  --display: 'Fraunces', Georgia, serif;
  --body:    'Inter', system-ui, sans-serif;
  --mono:    'JetBrains Mono', monospace;
}

body, html, .page-content, .wrapper, main {
  background: #101014 !important;
}
.post-header, .page-heading, header.post-header {
  display: none !important;
}

.mw-page * { box-sizing: border-box; margin: 0; padding: 0; }

.mw-page {
  background: var(--ink);
  color: var(--elfenbein);
  font-family: var(--body);
  font-size: 15px;
  line-height: 1.55;
  -webkit-font-smoothing: antialiased;
  padding-bottom: 120px;
}
.mw-page h1, .mw-page h2, .mw-page h3, .mw-page h4, .mw-page h5, .mw-page h6 {
  color: var(--elfenbein);
}

.mw-wrap { max-width: 1060px; margin: 0 auto; padding: 0 28px; }

/* ─── Hero ─── */
.mw-hero {
  padding: 96px 0 72px;
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 48px;
  align-items: end;
  border-bottom: 1px solid var(--linie2);
}
.mw-eyebrow {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: var(--messing);
  margin-bottom: 20px;
}
.mw-hero h1 {
  font-family: var(--display);
  font-weight: 300;
  font-size: clamp(52px, 8vw, 92px);
  line-height: 0.98;
  letter-spacing: -0.02em;
}
.mw-hero h1 em {
  font-style: italic;
  font-weight: 300;
  color: var(--messing2);
}
.mw-hero-sub {
  margin-top: 22px;
  max-width: 46ch;
  color: var(--nebel);
  font-size: 16px;
}

/* Fortschrittsbogen */
.mw-progress { text-align: center; }
.mw-ring { width: 120px; height: 120px; }
.mw-ring circle { fill: none; stroke-width: 3; }
.mw-ring .bg { stroke: var(--linie2); }
.mw-ring .fg {
  stroke: var(--messing);
  stroke-linecap: round;
  transform: rotate(-90deg);
  transform-origin: 50% 50%;
  transition: stroke-dashoffset 600ms cubic-bezier(0.4,0,0.2,1);
}
.mw-ring-label {
  font-family: var(--display);
  font-size: 30px;
  font-weight: 300;
  fill: var(--elfenbein);
}
.mw-ring-caption {
  margin-top: 10px;
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--nebel);
}

/* ─── Gesamtskript ─── */
.mw-feature {
  margin: 56px 0 24px;
  padding: 30px 34px;
  background: linear-gradient(120deg, var(--graphit2), var(--graphit));
  border: 1px solid var(--linie2);
  border-radius: 4px;
  display: flex;
  align-items: center;
  gap: 28px;
  flex-wrap: wrap;
}
.mw-feature-titel h3 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 26px;
  letter-spacing: -0.01em;
}
.mw-feature-titel p { color: var(--nebel); font-size: 14px; margin-top: 6px; max-width: 52ch; }
.mw-feature .mw-btn { margin-left: auto; }

/* ─── Kapitel ─── */
.mw-kapitel { padding: 72px 0 12px; }
.mw-kapitel-kopf {
  display: flex;
  align-items: baseline;
  gap: 22px;
  margin-bottom: 34px;
}
.mw-numeral {
  font-family: var(--display);
  font-style: italic;
  font-weight: 300;
  font-size: 44px;
  color: var(--messing);
  min-width: 64px;
}
.mw-kapitel-kopf h2 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 32px;
  letter-spacing: -0.01em;
}
.mw-kapitel-kopf .mw-meta {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--nebel);
  margin-left: auto;
  white-space: nowrap;
}

/* ─── Modulzeilen (Tracklist) ─── */
.mw-liste { border-top: 1px solid var(--linie); }
.mw-modul {
  display: grid;
  grid-template-columns: 56px 1fr auto;
  gap: 20px;
  align-items: center;
  padding: 20px 8px;
  border-bottom: 1px solid var(--linie);
  transition: background 180ms ease, padding 180ms ease;
}
.mw-modul:hover { background: rgba(236,231,220,0.025); padding-left: 16px; }
.mw-nr {
  font-family: var(--mono);
  font-size: 13px;
  color: var(--nebel);
  transition: color 180ms;
}
.mw-modul:hover .mw-nr { color: var(--messing); }
.mw-modul.done .mw-nr { color: var(--gruen); }
.mw-modul h4 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 19px;
  letter-spacing: 0.005em;
}
.mw-modul.done h4 { color: var(--nebel); }
.mw-desc { color: var(--nebel); font-size: 13.5px; margin-top: 3px; }

/* Aktionen */
.mw-actions { display: flex; align-items: center; gap: 8px; flex-wrap: wrap; justify-content: flex-end; }
.mw-btn {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  font-family: var(--body);
  font-size: 12.5px;
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--elfenbein);
  background: transparent;
  border: 1px solid var(--linie2);
  border-radius: 999px;
  padding: 7px 15px;
  cursor: pointer;
  text-decoration: none;
  transition: all 160ms ease;
  white-space: nowrap;
}
.mw-btn:hover { border-color: var(--messing); color: var(--messing2); }
.mw-btn--voll {
  background: var(--messing);
  border-color: var(--messing);
  color: var(--ink);
}
.mw-btn--voll:hover { background: var(--messing2); border-color: var(--messing2); color: var(--ink); }
.mw-btn svg { width: 13px; height: 13px; flex-shrink: 0; }

/* Haken */
.mw-check {
  width: 30px; height: 30px;
  border-radius: 50%;
  border: 1px solid var(--linie2);
  background: transparent;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  transition: all 200ms ease;
  margin-left: 6px;
  flex-shrink: 0;
}
.mw-check svg { width: 13px; height: 13px; stroke: var(--ink); opacity: 0; transform: scale(0.4); transition: all 260ms cubic-bezier(0.34,1.56,0.64,1); }
.mw-check:hover { border-color: var(--gruen); }
.mw-modul.done .mw-check { background: var(--gruen); border-color: var(--gruen); }
.mw-modul.done .mw-check svg { opacity: 1; transform: scale(1); }

/* ─── Mini-Player ─── */
.mw-player {
  position: fixed;
  left: 50%;
  bottom: 20px;
  transform: translate(-50%, 140%);
  width: min(680px, calc(100% - 32px));
  background: rgba(30, 30, 38, 0.92);
  backdrop-filter: blur(18px);
  -webkit-backdrop-filter: blur(18px);
  border: 1px solid var(--linie2);
  border-radius: 14px;
  padding: 14px 20px;
  display: flex;
  align-items: center;
  gap: 16px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.5);
  transition: transform 420ms cubic-bezier(0.22, 1, 0.36, 1);
  z-index: 50;
}
.mw-player.offen { transform: translate(-50%, 0); }
.mw-play {
  width: 42px; height: 42px;
  border-radius: 50%;
  background: var(--messing);
  border: none;
  cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
  transition: background 160ms;
}
.mw-play:hover { background: var(--messing2); }
.mw-play svg { width: 15px; height: 15px; fill: var(--ink); }
.mw-player-info { flex: 1; min-width: 0; }
.mw-player-info .laeuft {
  font-family: var(--mono);
  font-size: 9.5px;
  letter-spacing: 0.24em;
  text-transform: uppercase;
  color: var(--messing);
}
.mw-player-info .titel {
  font-family: var(--display);
  font-size: 16px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  margin-top: 2px;
}
.mw-player-bar {
  height: 3px;
  background: var(--linie2);
  border-radius: 2px;
  margin-top: 8px;
  overflow: hidden;
}
.mw-player-bar > div {
  height: 100%;
  width: 0%;
  background: var(--messing);
  border-radius: 2px;
}
.mw-player-close {
  background: none; border: none;
  color: var(--nebel);
  font-size: 20px;
  cursor: pointer;
  line-height: 1;
  padding: 6px;
  transition: color 160ms;
}
.mw-player-close:hover { color: var(--elfenbein); }

/* ─── Fußzeile ─── */
.mw-fuss {
  margin-top: 88px;
  padding: 36px 0;
  border-top: 1px solid var(--linie2);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  flex-wrap: wrap;
  color: var(--nebel);
  font-size: 13px;
}
.mw-fuss-links { display: flex; gap: 10px; }

/* ─── Responsiv ─── */
@media (max-width: 760px) {
  .mw-hero { grid-template-columns: 1fr; gap: 36px; padding: 64px 0 48px; }
  .mw-progress { text-align: left; }
  .mw-modul { grid-template-columns: 40px 1fr; }
  .mw-actions { grid-column: 1 / -1; padding-left: 60px; flex-wrap: wrap; justify-content: flex-start; }
  .mw-kapitel-kopf .mw-meta { display: none; }
  .mw-feature .mw-btn { margin-left: 0; }
}
@media (max-width: 760px) { .mw-actions { padding-left: 0; } }

@media (prefers-reduced-motion: reduce) {
  * { transition-duration: 1ms !important; animation: none !important; }
  html { scroll-behavior: auto; }
}
</style>

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung</div>
      <h1>Mathematik,<br><em>Satz für Satz.</em></h1>
      <p class="mw-hero-sub">26 Module in vier Kapiteln plus interaktive Tools — jedes Modul mit Skript, Quiz, Podcast zum Hören und vertiefendem Text.</p>
    </div>
    <div class="mw-progress">
      <svg class="mw-ring" viewBox="0 0 120 120">
        <circle class="bg" cx="60" cy="60" r="52"/>
        <circle class="fg" cx="60" cy="60" r="52" id="ringFg"/>
        <text class="mw-ring-label" x="60" y="60" text-anchor="middle" dominant-baseline="central" id="ringLabel">0</text>
      </svg>
      <div class="mw-ring-caption">von <span id="ringTotal">0</span> Modulen</div>
    </div>
  </header>

  <!-- Gesamtskript -->
  <div class="mw-feature">
    <div class="mw-feature-titel">
      <h3>Das Gesamtskript</h3>
      <p>Alle Module in einem Dokument — zum durchgehenden Lernen oder als Nachschlagewerk vor der FSP.</p>
    </div>
    <a href="/assets/pdfs/Mathematik_Skript.pdf" class="mw-btn">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 3v12m0 0l-4-4m4 4l4-4M4 21h16"/></svg>
      Skript öffnen · 1,1 MB
    </a>
  </div>

  <div id="kapitel"></div>

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div><strong style="color:var(--elfenbein)">26 Module</strong> · Lineare Algebra, Vektorrechnung, Differentialrechnung, Integralrechnung &amp; interaktive Tools</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

<!-- Mini-Player -->
<div class="mw-player" id="player">
  <button class="mw-play" id="playBtn" aria-label="Abspielen / Pausieren">
    <svg id="playIcon" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
  </button>
  <div class="mw-player-info">
    <div class="laeuft">Jetzt läuft</div>
    <div class="titel" id="playerTitel">—</div>
    <div class="mw-player-bar"><div id="playerBar"></div></div>
  </div>
  <button class="mw-player-close" id="playerClose" aria-label="Player schließen">×</button>
</div>
<audio id="audio"></audio>
</div>

<script>
/* ─── Daten: hier neue Module, PDFs, Quiz, Podcasts & Texte eintragen ─── */
const KAPITEL = [
  {
    numeral: 'I', titel: 'Lineare Algebra', meta: '5 Module',
    module: [
      { id:'a1', nr:'01', titel:'Matrizen', desc:'Addition, Multiplikation, Transponieren und spezielle Matrizen', pdf:'/assets/pdfs/Matrizen_2_1.pdf', quiz:'/assets/quizzes/quiz_matrizen_grundlagen.html', podcast:'/assets/audio/matrizen.mp3', text:'/assets/texte/matrizen.pdf' },
      { id:'a2', nr:'02', titel:'Determinanten', desc:'Laplace-Entwicklung, Sarrus-Regel und inverse Matrizen', pdf:'/assets/pdfs/Matrizen_2_2.pdf', quiz:'/assets/quizzes/quiz_determinanten.html', podcast:'/assets/audio/determinanten.mp3', text:'/assets/texte/determinanten.pdf' },
      { id:'a3', nr:'03', titel:'Matrizengleichungen', desc:'Übungsaufgaben, Rangbestimmung und Gauß-Elimination', pdf:'/assets/pdfs/Matrizen_2_3.pdf', podcast:'/assets/audio/matrizengleichungen.mp3', text:'/assets/texte/matrizengleichungen.pdf' },
      { id:'a4', nr:'04', titel:'Lineare Gleichungssysteme', desc:'Matrixschreibweise, Gauß-Algorithmus und Lösbarkeitskriterien', pdf:'/assets/pdfs/LGS_2_1-5.pdf', quiz:'/assets/quizzes/quiz_lgs_grundlagen.html', podcast:'/assets/audio/lgs.mp3', text:'/assets/texte/lgs.pdf' },
      { id:'a5', nr:'05', titel:'Parameterabhängigkeit', desc:'LGS mit Parametern, Determinantentest und Fallunterscheidungen', pdf:'/assets/pdfs/LGS_2_2-2.pdf', podcast:'/assets/audio/parameter.mp3', text:'/assets/texte/parameter.pdf' },
    ]
  },
  {
    numeral: 'II', titel: 'Vektorrechnung', meta: '4 Module',
    module: [
      { id:'v1', nr:'06', titel:'Grundlagen', desc:'Vektoren, Koordinatensysteme, Betrag und Grundoperationen', pdf:'/assets/pdfs/Geo_2_1-2.pdf', quiz:'/assets/quizzes/quiz_vektorrechnung_grundlagen.html', podcast:'/assets/audio/vektoren-grundlagen.mp3', text:'/assets/texte/vektoren-grundlagen.pdf' },
      { id:'v2', nr:'07', titel:'Vektor- & Spatprodukt', desc:'Kreuzprodukt, Flächen, Spatprodukt und Volumen im Raum', pdf:'/assets/pdfs/Geo_2_2-2.pdf', quiz:'/assets/quizzes/quiz_vektorprodukt.html', podcast:'/assets/audio/spatprodukt.mp3', text:'/assets/texte/spatprodukt.pdf' },
      { id:'v3', nr:'08', titel:'Geraden und Ebenen', desc:'Parametergleichungen, Normalenvektor und Lagebeziehungen', pdf:'/assets/pdfs/Geo_2_3.pdf', quiz:'/assets/quizzes/quiz_geraden_ebenen.html', podcast:'/assets/audio/geraden-ebenen.mp3', text:'/assets/texte/geraden-ebenen.pdf' },
      { id:'v4', nr:'09', titel:'Abstände und Lagen', desc:'Abstandsberechnungen und Hessesche Normalenform', pdf:'/assets/pdfs/Geo_2_4.pdf', quiz:'/assets/quizzes/quiz_lagebeziehungen.html', podcast:'/assets/audio/abstaende.mp3', text:'/assets/texte/abstaende.pdf' },
    ]
  },
  {
    numeral: 'III', titel: 'Differentialrechnung', meta: '12 Module',
    module: [
      { id:'d1', nr:'10', titel:'Zahlenfolgen', desc:'Explizite und rekursive Vorschriften, Monotonie, Beschränktheit', pdf:'/assets/pdfs/Folgen_2_1-2.pdf', quiz:'/assets/quizzes/quiz_zahlenfolgen.html', podcast:'/assets/audio/folgen.mp3', text:'/assets/texte/folgen.pdf' },
      { id:'d2', nr:'11', titel:'Grenzwerte von Folgen', desc:'Konvergenz, Divergenz, Grenzwertsätze und Eulersche Zahl', pdf:'/assets/pdfs/Grenzwerte_2_1.pdf', quiz:'/assets/quizzes/quiz_grenzwerte_folgen.html', podcast:'/assets/audio/grenzwerte-folgen.mp3', text:'/assets/texte/grenzwerte-folgen.pdf' },
      { id:'d3', nr:'12', titel:'Grenzwerte im Unendlichen', desc:'Dominanzprinzip und waagerechte Asymptoten', pdf:'/assets/pdfs/Funktion_2_2.pdf', quiz:'/assets/quizzes/quiz_grenzwerte_funktionen_1.html', podcast:'/assets/audio/grenzwerte-unendlich.mp3', text:'/assets/texte/grenzwerte-unendlich.pdf' },
      { id:'d4', nr:'13', titel:'Grenzwerte an einer Stelle', desc:'Einseitige Grenzwerte, Polstellen und hebbare Lücken', pdf:'/assets/pdfs/Grenzwerte_2_2.pdf', quiz:'/assets/quizzes/quiz_grenzwerte_funktionen_2.html', podcast:'/assets/audio/grenzwerte-stelle.mp3', text:'/assets/texte/grenzwerte-stelle.pdf' },
      { id:'d5', nr:'14', titel:'Asymptoten', desc:'Waagerechte, senkrechte und schräge Asymptoten', pdf:'/assets/pdfs/Grenzwerte_2_3.pdf', quiz:'/assets/quizzes/quiz_asymptoten.html', podcast:'/assets/audio/asymptoten.mp3', text:'/assets/texte/asymptoten.pdf' },
      { id:'d6', nr:'15', titel:'Steigung und Ableitung', desc:'Sekanten, Tangenten und Differenzierbarkeit', pdf:'/assets/pdfs/Funktion_2_1.pdf', quiz:'/assets/quizzes/quiz_ableitung_grundlagen.html', podcast:'/assets/audio/ableitung.mp3', text:'/assets/texte/ableitung.pdf' },
      { id:'d7', nr:'16', titel:'Ableitungsregeln', desc:'Potenz-, Produkt-, Quotienten- und Kettenregel', pdf:'/assets/pdfs/Funktion_2_4.pdf', quiz:'/assets/quizzes/quiz_ableitungsregeln.html', podcast:'/assets/audio/ableitungsregeln.mp3', text:'/assets/texte/ableitungsregeln.pdf' },
      { id:'d8', nr:'17', titel:'Regel von de L’Hôpital', desc:'Unbestimmte Ausdrücke: 0/0, ∞/∞, ∞·0', pdf:'/assets/pdfs/Hospital_2_1.pdf', quiz:'/assets/quizzes/quiz_hospital.html', podcast:'/assets/audio/hospital.mp3', text:'/assets/texte/hospital.pdf' },
      { id:'d9', nr:'18', titel:'Extrempunkte', desc:'Notwendige und hinreichende Bedingungen, Sattelpunkte', pdf:'/assets/pdfs/Extremwert_2_1.pdf', quiz:'/assets/quizzes/quiz_extrempunkte.html', podcast:'/assets/audio/extrempunkte.mp3', text:'/assets/texte/extrempunkte.pdf' },
      { id:'d10', nr:'19', titel:'Wendepunkte', desc:'Krümmungswechsel und dritte Ableitung', pdf:'/assets/pdfs/Wendepunkt_2_1.pdf', quiz:'/assets/quizzes/quiz_wendepunkte.html', podcast:'/assets/audio/wendepunkte.mp3', text:'/assets/texte/wendepunkte.pdf' },
      { id:'d11', nr:'20', titel:'Kurvendiskussion', desc:'Systematische Funktionsanalyse mit allen Kriterien', pdf:'/assets/pdfs/Kurvendiskusion_2_1.pdf', quiz:'/assets/quizzes/quiz_kurvendiskussion.html', podcast:'/assets/audio/kurvendiskussion.mp3', text:'/assets/texte/kurvendiskussion.pdf' },
      { id:'d12', nr:'21', titel:'Extremwertaufgaben', desc:'Optimierungsprobleme mit Nebenbedingungen', pdf:'/assets/pdfs/Extrem_2_1.pdf', quiz:'/assets/quizzes/quiz_extremwertaufgaben.html', podcast:'/assets/audio/extremwertaufgaben.mp3', text:'/assets/texte/extremwertaufgaben.pdf' },
    ]
  },
  {
    numeral: 'IV', titel: 'Integralrechnung', meta: '5 Module',
    module: [
      { id:'i1', nr:'22', titel:'Einführung', desc:'Stammfunktionen, Grundintegrale und bestimmtes Integral', pdf:'/assets/pdfs/Integral_2_1.pdf', quiz:'/assets/quizzes/quiz_integral_einfuehrung.html', podcast:'/assets/audio/integral-einfuehrung.mp3', text:'/assets/texte/integral-einfuehrung.pdf' },
      { id:'i2', nr:'23', titel:'Integrationsmethoden', desc:'Substitution, partielle Integration, Partialbruchzerlegung', pdf:'/assets/pdfs/Integral_2_2.pdf', quiz:'/assets/quizzes/quiz_integrationsmethoden.html', podcast:'/assets/audio/integrationsmethoden.mp3', text:'/assets/texte/integrationsmethoden.pdf' },
      { id:'i3', nr:'24', titel:'Hauptsatz & Flächen', desc:'HDI, bestimmte Integrale und Flächen zwischen Graphen', pdf:'/assets/pdfs/Integral_2_3.pdf', quiz:'/assets/quizzes/quiz_hauptsatz_flaechen.html', podcast:'/assets/audio/hauptsatz.mp3', text:'/assets/texte/hauptsatz.pdf' },
      { id:'i4', nr:'25', titel:'Rotationsvolumen', desc:'Volumen von Rotationskörpern um x- und y-Achse', pdf:'/assets/pdfs/Intergal_2_4-2.pdf', quiz:'/assets/quizzes/quiz_rotationsvolumen.html', podcast:'/assets/audio/rotationsvolumen.mp3', text:'/assets/texte/rotationsvolumen.pdf' },
      { id:'i5', nr:'26', titel:'Flächen zwischen Funktionen', desc:'Flächenberechnung zwischen zwei Funktionsgraphen', pdf:'/assets/pdfs/Fläche_zwichen_Funktionen.pdf', podcast:'/assets/audio/flaechen-zwischen-funktionen.mp3', text:'/assets/texte/flaechen-zwischen-funktionen.pdf' },
    ]
  },
  {
    numeral: 'V', titel: 'Interaktive Tools', meta: '5 Anwendungen',
    module: [
      { id:'t1', nr:'27', titel:'Tangenten-Explorer', desc:'Interaktive Visualisierung von Tangenten und Sekanten', tool:'/assets/interactive/tangenten_explorer.html' },
      { id:'t2', nr:'28', titel:'3D-Vektor-Explorer', desc:'Vektoren, Kreuzprodukt und Volumen im dreidimensionalen Raum', tool:'/assets/interactive/vektor_explorer.html' },
      { id:'t3', nr:'29', titel:'Geraden & Ebenen', desc:'Lagebeziehungen und Schnittpunkte interaktiv erkunden', tool:'/assets/interactive/geraden_ebenen_explorer.html' },
      { id:'t4', nr:'30', titel:'Matrizen-Explorer', desc:'Matrixoperationen und Transformationen visualisieren', tool:'/assets/interactive/matrizen_explorer.html' },
      { id:'t5', nr:'31', titel:'Determinanten-Rechner', desc:'Determinanten beliebiger Matrizen berechnen', tool:'/assets/interactive/determinanten_rechner.html' },
    ]
  }
];

/* ─── Fortschritt (localStorage mit Fallback) ─── */
const KEY = 'math-progress-v2';
let memStore = {};
function getProgress() {
  try { return JSON.parse(localStorage.getItem(KEY)) || {}; }
  catch { return memStore; }
}
function saveProgress(p) {
  try { localStorage.setItem(KEY, JSON.stringify(p)); }
  catch { memStore = p; }
}

const iconPdf  = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6"/></svg>';
const iconQuiz = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 9a3 3 0 1 1 4 2.83c-.7.26-1 .95-1 1.67v.5"/><path d="M12 17.5h.01"/></svg>';
const iconPod  = '<svg viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg>';
const iconText = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 6h16M4 12h16M4 18h10"/></svg>';
const iconTool = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14.7 6.3a1 1 0 0 0 0 1.4l1.6 1.6a1 1 0 0 0 1.4 0l3.77-3.77a6 6 0 0 1-7.94 7.94l-6.91 6.91a2.12 2.12 0 0 1-3-3l6.91-6.91a6 6 0 0 1 7.94-7.94l-3.76 3.76z"/></svg>';
const iconCheck= '<svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>';

/* ─── Rendern ─── */
function actionsFor(m) {
  if (m.tool) {
    return `<a href="${m.tool}" class="mw-btn">${iconTool} Öffnen</a>`;
  }
  let html = `<a href="${m.pdf}" class="mw-btn">${iconPdf} Folien</a>`;
  if (m.quiz) html += `<a href="${m.quiz}" class="mw-btn">${iconQuiz} Quiz</a>`;
  html += `<button class="mw-btn" onclick="startPodcast('${m.nr}', '${m.titel.replace(/'/g, "\\'")}', '${m.podcast}')">${iconPod} Podcast</button>`;
  html += `<a href="${m.text}" class="mw-btn">${iconText} Text</a>`;
  return html;
}

function render() {
  const wrap = document.getElementById('kapitel');
  let total = 0;
  wrap.innerHTML = KAPITEL.map(k => {
    total += k.module.length;
    return `
    <section class="mw-kapitel">
      <div class="mw-kapitel-kopf">
        <span class="mw-numeral">${k.numeral}</span>
        <h2>${k.titel}</h2>
        <span class="mw-meta">${k.meta}</span>
      </div>
      <div class="mw-liste">
        ${k.module.map(m => `
          <div class="mw-modul" data-module="${m.id}">
            <span class="mw-nr">${m.nr}</span>
            <div>
              <h4>${m.titel}</h4>
              <p class="mw-desc">${m.desc}</p>
            </div>
            <div class="mw-actions">
              ${actionsFor(m)}
              <button class="mw-check" onclick="toggleModule('${m.id}')" aria-label="Als erledigt markieren">${iconCheck}</button>
            </div>
          </div>
        `).join('')}
      </div>
    </section>
  `;
  }).join('');
  document.getElementById('ringTotal').textContent = total;
  updateUI();
}

function updateUI() {
  const p = getProgress();
  const total = KAPITEL.reduce((sum, k) => sum + k.module.length, 0);
  let done = 0;
  document.querySelectorAll('.mw-modul').forEach(el => {
    const on = !!p[el.dataset.module];
    el.classList.toggle('done', on);
    if (on) done++;
  });
  const r = 52, umfang = 2 * Math.PI * r;
  const fg = document.getElementById('ringFg');
  fg.style.strokeDasharray = umfang;
  fg.style.strokeDashoffset = umfang * (1 - (total ? done / total : 0));
  document.getElementById('ringLabel').textContent = done;
}

function toggleModule(id) {
  const p = getProgress();
  if (p[id]) delete p[id]; else p[id] = Date.now();
  saveProgress(p);
  updateUI();
}

/* ─── Mini-Player ─── */
const audio = document.getElementById('audio');
const player = document.getElementById('player');
const playBtn = document.getElementById('playBtn');
const playIcon = document.getElementById('playIcon');

function startPodcast(nr, titel, src) {
  document.getElementById('playerTitel').textContent = `Modul ${nr} · ${titel}`;
  player.classList.add('offen');
  audio.src = src;
  audio.play().catch(() => { /* Datei noch nicht vorhanden — Player bleibt als Vorschau sichtbar */ });
  setIcon();
}
playBtn.addEventListener('click', () => {
  if (audio.paused) audio.play().catch(()=>{}); else audio.pause();
  setIcon();
});
audio.addEventListener('play', setIcon);
audio.addEventListener('pause', setIcon);
audio.addEventListener('timeupdate', () => {
  const pct = audio.duration ? (audio.currentTime / audio.duration) * 100 : 0;
  document.getElementById('playerBar').style.width = pct + '%';
});
function setIcon() {
  playIcon.innerHTML = audio.paused
    ? '<path d="M8 5v14l11-7z"/>'
    : '<path d="M6 5h4v14H6zM14 5h4v14h-4z"/>';
}
document.getElementById('playerClose').addEventListener('click', () => {
  audio.pause();
  player.classList.remove('offen');
});

render();
</script>
