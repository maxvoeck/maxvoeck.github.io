---
layout: page
title:
permalink: /teaching/mathematik-uebungen/
---

<style>
/* Same CSS as materialien page - reusing the Apple Design System */
:root {
  --system-blue: #007AFF;
  --system-green: #34C759;
  --system-indigo: #5856D6;
  --system-orange: #FF9500;
  --system-pink: #FF2D55;
  --system-purple: #AF52DE;
  --system-red: #FF3B30;
  --system-teal: #5AC8FA;
  --system-yellow: #FFCC00;
  
  --vektor: #FF9500;
  --algebra: #5AC8FA;
  --diff: #FF2D55;
  --integral: #34C759;
  --tools: #AF52DE;
  
  --gray-1: #F5F5F7;
  --gray-2: #E5E5EA;
  --gray-3: #D1D1D6;
  --gray-4: #C7C7CC;
  --gray-5: #AEAEB2;
  --gray-6: #8E8E93;
  --gray-7: #636366;
  --gray-8: #48484A;
  --gray-9: #3A3A3C;
  --gray-10: #303036;
  --gray-11: #252529;
  --gray-12: #e3e3e8;
  
  --bg-primary: #1a1a1e;
  --bg-secondary: #252529;
  --bg-tertiary: #303036;
  --text-primary: #e3e3e8;
  --text-secondary: #a0a0a8;
  --text-tertiary: #6b6b74;
  --separator: rgba(227, 227, 232, 0.08);
  --separator-strong: rgba(227, 227, 232, 0.15);
  
  --font-stack: -apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", "Helvetica Neue", Helvetica, Arial, sans-serif;
  --font-mono: "SF Mono", SFMono-Regular, ui-monospace, Menlo, Monaco, monospace;
  
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 20px;
  --radius-2xl: 24px;
  --radius-full: 9999px;
  
  --shadow-sm: 0 1px 2px rgba(227,227,232,0.06);
  --shadow-md: 0 4px 12px rgba(227,227,232,0.08);
  --shadow-lg: 0 12px 24px rgba(227,227,232,0.12);
  --shadow-xl: 0 24px 48px rgba(0,0,0,0.64);
  
  --transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);
  --transition-spring: 500ms cubic-bezier(0.34, 1.56, 0.64, 1);
}

*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-primary) !important;
  color: var(--text-primary);
  font-family: var(--font-stack);
  line-height: 1.47059;
  letter-spacing: -0.022em;
}

.post-header, .page-heading, header.post-header {
  display: none !important;
}

.ma-container {
  max-width: 980px;
  margin: 0 auto;
  padding: var(--space-8) var(--space-5);
}

@media (min-width: 768px) {
  .ma-container {
    padding: var(--space-16) var(--space-8);
  }
}

.ma-hero {
  text-align: center;
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}

.ma-hero-eyebrow {
  font-size: 17px;
  font-weight: 600;
  color: var(--system-purple);
  text-transform: uppercase;
  letter-spacing: 0.05em;
  margin-bottom: var(--space-3);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-2);
}

.ma-hero-eyebrow::before,
.ma-hero-eyebrow::after {
  content: '';
  width: 24px;
  height: 1px;
  background: var(--separator-strong);
}

.ma-hero h1 {
  font-size: 48px;
  font-weight: 700;
  letter-spacing: -0.003em;
  line-height: 1.08349;
  margin-bottom: var(--space-3);
  background: linear-gradient(135deg, var(--text-primary) 0%, var(--gray-6) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

@media (min-width: 768px) {
  .ma-hero h1 {
    font-size: 64px;
  }
}

.ma-hero-subtitle {
  font-size: 21px;
  font-weight: 400;
  color: var(--text-secondary);
  margin-bottom: var(--space-8);
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  line-height: 1.381;
}

.ma-section {
  margin-bottom: var(--space-16);
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) backwards;
}

.ma-section:nth-child(2) { animation-delay: 0.1s; }
.ma-section:nth-child(3) { animation-delay: 0.2s; }
.ma-section:nth-child(4) { animation-delay: 0.3s; }
.ma-section:nth-child(5) { animation-delay: 0.4s; }
.ma-section:nth-child(6) { animation-delay: 0.5s; }
.ma-section:nth-child(7) { animation-delay: 0.6s; }

.ma-section-header {
  display: flex;
  align-items: flex-start;
  gap: var(--space-4);
  margin-bottom: var(--space-6);
  padding: 0 var(--space-2);
}

.ma-section-icon {
  width: 48px;
  height: 48px;
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  flex-shrink: 0;
  background: var(--bg-secondary);
  transition: transform var(--transition-spring);
}

.ma-section:hover .ma-section-icon {
  transform: scale(1.1) rotate(-5deg);
}

.ma-section--vektor .ma-section-icon {
  background: rgba(255, 149, 0, 0.12);
  color: var(--vektor);
}
.ma-section--algebra .ma-section-icon {
  background: rgba(90, 200, 250, 0.12);
  color: var(--algebra);
}
.ma-section--diff .ma-section-icon {
  background: rgba(255, 45, 85, 0.12);
  color: var(--diff);
}
.ma-section--integral .ma-section-icon {
  background: rgba(52, 199, 89, 0.12);
  color: var(--integral);
}
.ma-section--tools .ma-section-icon {
  background: rgba(175, 82, 222, 0.12);
  color: var(--tools);
}

.ma-section-title-group {
  flex: 1;
}

.ma-section-title {
  font-size: 28px;
  font-weight: 600;
  letter-spacing: -0.021em;
  line-height: 1.14286;
  color: var(--text-primary);
  margin-bottom: var(--space-1);
}

.ma-section-subtitle {
  font-size: 15px;
  color: var(--text-tertiary);
  font-weight: 400;
}

.ma-grid {
  display: grid;
  gap: var(--space-4);
}

@media (min-width: 768px) {
  .ma-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: var(--space-5);
  }
}

@media (min-width: 1024px) {
  .ma-grid--tools {
    grid-template-columns: repeat(3, 1fr);
  }
}

.ma-card {
  background: var(--bg-secondary);
  border-radius: var(--radius-xl);
  padding: var(--space-5);
  position: relative;
  overflow: hidden;
  transition: all var(--transition-base);
  border: 2px solid transparent;
}

.ma-card::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(227,227,232,0.03) 0%, transparent 50%);
  opacity: 0;
  transition: opacity var(--transition-base);
}

.ma-card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
  background: var(--bg-tertiary);
}

.ma-card:hover::before {
  opacity: 1;
}

.ma-card:active {
  transform: scale(0.98);
  transition-duration: var(--transition-fast);
}

.ma-card-header {
  display: flex;
  align-items: center;
  gap: var(--space-3);
  margin-bottom: var(--space-3);
}

.ma-card-number {
  font-family: var(--font-mono);
  font-size: 12px;
  font-weight: 600;
  color: var(--text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.ma-section--vektor .ma-card-number { color: var(--vektor); }
.ma-section--algebra .ma-card-number { color: var(--algebra); }
.ma-section--diff .ma-card-number { color: var(--diff); }
.ma-section--integral .ma-card-number { color: var(--integral); }
.ma-section--tools .ma-card-number { color: var(--tools); }

.ma-card h4 {
  font-size: 17px;
  font-weight: 600;
  color: var(--text-primary);
  letter-spacing: -0.022em;
  line-height: 1.23536;
  margin: 0;
}

.ma-card p {
  font-size: 14px;
  line-height: 1.42859;
  color: var(--text-secondary);
  margin-bottom: var(--space-4);
}

.ma-btn {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-2) var(--space-3);
  border-radius: var(--radius-md);
  font-size: 13px;
  font-weight: 500;
  text-decoration: none;
  transition: all var(--transition-fast);
  border: none;
  cursor: pointer;
  font-family: inherit;
  position: relative;
  z-index: 2;
}

.ma-btn--primary {
  background: var(--system-purple);
  color: white !important;
}

.ma-btn--primary:hover {
  background: #9333ea;
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(175, 82, 222, 0.3);
}

.ma-btn--secondary {
  background: rgba(255, 255, 255, 0.1);
  color: var(--text-primary) !important;
}

.ma-btn--secondary:hover {
  background: rgba(255, 255, 255, 0.15);
}

.ma-tool-icon {
  width: 40px;
  height: 40px;
  border-radius: var(--radius-md);
  background: linear-gradient(135deg, var(--tools) 0%, #BF5AF2 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  margin-bottom: var(--space-3);
  box-shadow: 0 4px 12px rgba(175, 82, 222, 0.3);
}

.ma-section--tools .ma-card {
  background: linear-gradient(135deg, var(--bg-secondary) 0%, rgba(175, 82, 222, 0.05) 100%);
  border: 1px solid rgba(175, 82, 222, 0.1);
}

.ma-section--tools .ma-card:hover {
  border-color: rgba(175, 82, 222, 0.2);
  box-shadow: 0 8px 32px rgba(175, 82, 222, 0.15);
}

.ma-footer {
  margin-top: var(--space-20);
  padding-top: var(--space-8);
  border-top: 1px solid var(--separator);
  display: flex;
  flex-direction: column;
  gap: var(--space-5);
  align-items: center;
  text-align: center;
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) 0.6s backwards;
}

@media (min-width: 768px) {
  .ma-footer {
    flex-direction: row;
    justify-content: space-between;
    text-align: left;
  }
}

.ma-footer-text {
  font-size: 12px;
  color: var(--text-tertiary);
}

.ma-footer-text strong {
  color: var(--text-secondary);
  font-weight: 600;
}

.ma-footer-actions {
  display: flex;
  gap: var(--space-3);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

@media (hover: none) {
  .ma-card:hover {
    transform: none;
    box-shadow: var(--shadow-sm);
  }
  
  .ma-card:active {
    transform: scale(0.98);
    background: var(--bg-tertiary);
  }
}
</style>

<div class="ma-container">

  <!-- Hero -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Übungen & Quizzes</h1>
    <p class="ma-hero-subtitle">Interaktive Quizzes, Tools und Aufgabengeneratoren zum Üben und Vertiefen</p>
  </div>

  <!-- Quizzes Algebra -->
  <div class="ma-section ma-section--algebra">
    <div class="ma-section-header">
      <div class="ma-section-icon">🔢</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Algebra Quizzes</h2>
        <p class="ma-section-subtitle">3 Quizzes · Matrizen, Determinanten & LGS</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q01</span>
          <h4>Matrizen Grundlagen</h4>
        </div>
        <p>Addition, Multiplikation und Transponieren von Matrizen</p>
        <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q02</span>
          <h4>Determinanten</h4>
        </div>
        <p>Laplace-Entwicklung, Sarrus-Regel und inverse Matrizen</p>
        <a href="/assets/quizzes/quiz_determinanten.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q03</span>
          <h4>LGS Grundlagen</h4>
        </div>
        <p>Lineare Gleichungssysteme und Gauß-Algorithmus</p>
        <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>
    </div>
  </div>

  <!-- Quizzes Vektoren -->
  <div class="ma-section ma-section--vektor">
    <div class="ma-section-header">
      <div class="ma-section-icon">📐</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Vektor Quizzes</h2>
        <p class="ma-section-subtitle">4 Quizzes · Von Grundlagen bis Raumgeometrie</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q04</span>
          <h4>Vektorrechnung Grundlagen</h4>
        </div>
        <p>Koordinatensysteme, Betrag und Grundoperationen</p>
        <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q05</span>
          <h4>Vektorprodukt</h4>
        </div>
        <p>Kreuzprodukt, Spatprodukt und Anwendungen</p>
        <a href="/assets/quizzes/quiz_vektorprodukt.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q06</span>
          <h4>Geraden und Ebenen</h4>
        </div>
        <p>Parametergleichungen und Normalenvektoren</p>
        <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q07</span>
          <h4>Lagebeziehungen</h4>
        </div>
        <p>Abstände und Lagebeziehungen im Raum</p>
        <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>
    </div>
  </div>

  <!-- Quizzes Differentialrechnung -->
  <div class="ma-section ma-section--diff">
    <div class="ma-section-header">
      <div class="ma-section-icon">📉</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Analysis Quizzes</h2>
        <p class="ma-section-subtitle">12 Quizzes · Folgen, Grenzwerte & Ableitungen</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q08</span>
          <h4>Zahlenfolgen</h4>
        </div>
        <p>Rekursive Folgen, Monotonie und Beschränktheit</p>
        <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q09</span>
          <h4>Grenzwerte von Folgen</h4>
        </div>
        <p>Konvergenz, Divergenz und Grenzwertsätze</p>
        <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q10</span>
          <h4>Grenzwerte im Unendlichen</h4>
        </div>
        <p>Dominanzprinzip und waagerechte Asymptoten</p>
        <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q11</span>
          <h4>Grenzwerte an einer Stelle</h4>
        </div>
        <p>Einseitige Grenzwerte und Polstellen</p>
        <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q12</span>
          <h4>Asymptoten</h4>
        </div>
        <p>Waagerechte, senkrechte und schräge Asymptoten</p>
        <a href="/assets/quizzes/quiz_asymptoten.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q13</span>
          <h4>Ableitung Grundlagen</h4>
        </div>
        <p>Steigung, Tangenten und Differenzierbarkeit</p>
        <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q14</span>
          <h4>Ableitungsregeln</h4>
        </div>
        <p>Potenz-, Produkt-, Quotienten- und Kettenregel</p>
        <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q15</span>
          <h4>Regel von de L'Hôpital</h4>
        </div>
        <p>Unbestimmte Ausdrücke: 0/0, ∞/∞, ∞·0</p>
        <a href="/assets/quizzes/quiz_hospital.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q16</span>
          <h4>Extrempunkte</h4>
        </div>
        <p>Notwendige und hinreichende Bedingungen</p>
        <a href="/assets/quizzes/quiz_extrempunkte.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q17</span>
          <h4>Wendepunkte</h4>
        </div>
        <p>Krümmungswechsel und dritte Ableitung</p>
        <a href="/assets/quizzes/quiz_wendepunkte.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q18</span>
          <h4>Kurvendiskussion</h4>
        </div>
        <p>Systematische Funktionsanalyse</p>
        <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q19</span>
          <h4>Extremwertaufgaben</h4>
        </div>
        <p>Optimierungsprobleme mit Nebenbedingungen</p>
        <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>
    </div>
  </div>

  <!-- Quizzes Integralrechnung -->
  <div class="ma-section ma-section--integral">
    <div class="ma-section-header">
      <div class="ma-section-icon">∫</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Integral Quizzes</h2>
        <p class="ma-section-subtitle">4 Quizzes · Stammfunktionen bis Rotationsvolumen</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q20</span>
          <h4>Integral Einführung</h4>
        </div>
        <p>Stammfunktionen und Grundintegrale</p>
        <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q21</span>
          <h4>Integrationsmethoden</h4>
        </div>
        <p>Substitution, partielle Integration</p>
        <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q22</span>
          <h4>Hauptsatz & Flächen</h4>
        </div>
        <p>HDI und Flächen zwischen Graphen</p>
        <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>

      <div class="ma-card">
        <div class="ma-card-header">
          <span class="ma-card-number">Q23</span>
          <h4>Rotationsvolumen</h4>
        </div>
        <p>Volumen von Rotationskörpern</p>
        <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Quiz starten</a>
      </div>
    </div>
  </div>

  <!-- Interaktive Tools -->
  <div class="ma-section ma-section--tools">
    <div class="ma-section-header">
      <div class="ma-section-icon">⚡</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Interaktive Tools</h2>
        <p class="ma-section-subtitle">5 Tools · Hands-on Mathematik</p>
      </div>
    </div>
    <div class="ma-grid ma-grid--tools">
      <div class="ma-card">
        <div class="ma-tool-icon">📐</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T1</span>
          <h4>Tangenten-Explorer</h4>
        </div>
        <p>Interaktive Visualisierung von Tangenten und Ableitungen</p>
        <a href="/assets/interactive/tangenten_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Öffnen</a>
      </div>

      <div class="ma-card">
        <div class="ma-tool-icon">🔷</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T2</span>
          <h4>3D-Vektor-Explorer</h4>
        </div>
        <p>Drehe und manipuliere Vektoren im 3D-Raum</p>
        <a href="/assets/interactive/vektor_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Öffnen</a>
      </div>

      <div class="ma-card">
        <div class="ma-tool-icon">🎯</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T3</span>
          <h4>Geraden & Ebenen</h4>
        </div>
        <p>Erkunde Lagebeziehungen im 3D-Raum</p>
        <a href="/assets/interactive/geraden_ebenen_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Öffnen</a>
      </div>

      <div class="ma-card">
        <div class="ma-tool-icon">🔲</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T4</span>
          <h4>Matrizen-Explorer</h4>
        </div>
        <p>Sieh, was eine Matrix geometrisch bewirkt</p>
        <a href="/assets/interactive/matrizen_explorer.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Öffnen</a>
      </div>

      <div class="ma-card">
        <div class="ma-tool-icon">🧮</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <span class="ma-card-number">T5</span>
          <h4>Determinanten-Rechner</h4>
        </div>
        <p>Sarrus-Regel Schritt für Schritt animiert</p>
        <a href="/assets/interactive/determinanten_rechner.html" class="ma-btn ma-btn--primary" style="width: 100%; justify-content: center;">Öffnen</a>
      </div>
    </div>
  </div>

  <!-- Aufgabengeneratoren (Coming Soon) -->
  <div class="ma-section ma-section--tools">
    <div class="ma-section-header">
      <div class="ma-section-icon">🎲</div>
      <div class="ma-section-title-group">
        <h2 class="ma-section-title">Aufgabengeneratoren</h2>
        <p class="ma-section-subtitle">Bald verfügbar · Zufällige Aufgaben mit Lösungen</p>
      </div>
    </div>
    <div class="ma-grid">
      <div class="ma-card" style="opacity: 0.6;">
        <div class="ma-tool-icon" style="background: linear-gradient(135deg, var(--gray-6) 0%, var(--gray-7) 100%);">🎲</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <h4>Zufallsaufgaben-Generator</h4>
        </div>
        <p>Generiere individuelle Übungsaufgaben nach Thema und Schwierigkeit — mit Schritt-für-Schritt Lösungen</p>
        <button class="ma-btn ma-btn--secondary" style="width: 100%; justify-content: center; cursor: not-allowed;" disabled>
          In Entwicklung
        </button>
      </div>

      <div class="ma-card" style="opacity: 0.6;">
        <div class="ma-tool-icon" style="background: linear-gradient(135deg, var(--gray-6) 0%, var(--gray-7) 100%);">📝</div>
        <div class="ma-card-header" style="margin-bottom: var(--space-2);">
          <h4>Übungsblatt-Generator</h4>
        </div>
        <p>Erstelle personalisierte Übungsblätter zum Ausdrucken — wähle Themen, Anzahl und Schwierigkeitsgrad</p>
        <button class="ma-btn ma-btn--secondary" style="width: 100%; justify-content: center; cursor: not-allowed;" disabled>
          In Entwicklung
        </button>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <div class="ma-footer">
    <div class="ma-footer-text">
      <strong>23 Quizzes</strong> · 5 interaktive Tools · 2 Generatoren (bald)
    </div>
    <div class="ma-footer-actions">
      <a href="/teaching/mathematik/" class="ma-btn ma-btn--secondary">← Zurück</a>
      <a href="/teaching/mathematik-materialien/" class="ma-btn ma-btn--primary">Zu den Materialien →</a>
    </div>
  </div>

</div>
