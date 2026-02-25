---
layout: page
title:
permalink: /learn/determinanten/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root {
  --math:#FF2D55;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;
  --bg-primary:#1a1a1e;--bg-secondary:#252529;--bg-tertiary:#303036;
  --text-primary:#e3e3e8;--text-secondary:#a0a0a8;--text-tertiary:#6b6b74;
  --separator:rgba(227,227,232,0.08);
  --font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;
  --space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;
  --space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;
  --radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;
  --transition-base:250ms cubic-bezier(0.4,0,0.2,1);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.6;letter-spacing:-0.015em;}
.ch-wrap{width:100%;box-sizing:border-box;}
.cb,.math-block,.steps,.ch-section{max-width:100%;box-sizing:border-box;}

.post-header,.page-heading,header.post-header{display:none!important;}

#chapter-content{min-width:0;overflow:hidden;}
.ch-wrap{max-width:1100px;margin:0 auto;padding:var(--space-10) var(--space-5);display:grid;grid-template-columns:1fr 220px;gap:var(--space-12);align-items:start;}
.katex-display{overflow-x:auto!important;overflow-y:hidden;padding-bottom:4px;}
@media(max-width:860px){.ch-wrap{grid-template-columns:1fr;gap:var(--space-8);}.ch-toc{display:none;}}

.ch-breadcrumb{display:flex;align-items:center;gap:var(--space-2);font-size:13px;color:var(--text-tertiary);margin-bottom:var(--space-8);}
.ch-breadcrumb a{color:var(--text-tertiary);text-decoration:none;}.ch-breadcrumb a:hover{color:var(--text-primary);}
.ch-breadcrumb-sep{opacity:0.4;}

.ch-header{margin-bottom:var(--space-10);padding-bottom:var(--space-8);border-bottom:1px solid var(--separator);}
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--math);background:rgba(255,45,85,.1);border:1px solid rgba(255,45,85,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-weight:700;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
.ch-header-meta{font-size:14px;color:var(--text-tertiary);display:flex;gap:var(--space-4);flex-wrap:wrap;}

.ch-section{margin-bottom:var(--space-12);}
.ch-section h2{font-size:22px;font-weight:700;letter-spacing:-.02em;color:var(--text-primary);margin-bottom:var(--space-5);padding-top:var(--space-2);display:flex;align-items:center;gap:var(--space-3);}
.ch-section h2::before{content:'';display:block;width:3px;height:22px;background:var(--math);border-radius:2px;flex-shrink:0;}
.ch-section h3{font-size:17px;font-weight:600;color:var(--text-secondary);margin:var(--space-6) 0 var(--space-3);}
.ch-section p{font-size:16px;color:var(--text-secondary);line-height:1.75;margin-bottom:var(--space-4);}
.ch-section ul{margin:0 0 var(--space-4) var(--space-5);}
.ch-section li{font-size:16px;color:var(--text-secondary);line-height:1.7;margin-bottom:var(--space-1);}

.cb{border-radius:var(--radius-lg);padding:var(--space-5) var(--space-6);margin:var(--space-6) 0;border-left:3px solid;}
.cb-label{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;margin-bottom:var(--space-3);}
.cb-title{font-size:16px;font-weight:600;margin-bottom:var(--space-2);}
.cb p{font-size:15px;line-height:1.7;margin-bottom:var(--space-3);}.cb p:last-child{margin-bottom:0;}
.cb-def{background:rgba(88,86,214,.1);border-color:var(--system-indigo);}.cb-def .cb-label{color:var(--system-indigo);}
.cb-ex{background:rgba(52,199,89,.08);border-color:var(--system-green);}.cb-ex .cb-label{color:var(--system-green);}
.cb-task{background:rgba(255,149,0,.08);border-color:var(--system-orange);}.cb-task .cb-label{color:var(--system-orange);}
.cb-note{background:rgba(255,45,85,.08);border-color:var(--math);}.cb-note .cb-label{color:var(--math);}
.cb-tip{background:rgba(0,122,255,.08);border-color:var(--system-blue);}.cb-tip .cb-label{color:var(--system-blue);}

.math-block{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-md);padding:var(--space-5) var(--space-6);margin:var(--space-4) 0;overflow-x:auto;text-align:center;font-size:1.05em;}

.steps{list-style:none;padding:0;margin:var(--space-3) 0;counter-reset:step;}
.steps li{counter-increment:step;display:flex;gap:var(--space-3);margin-bottom:var(--space-4);font-size:15px;color:var(--text-secondary);line-height:1.65;}
.steps li::before{content:counter(step);min-width:24px;height:24px;border-radius:50%;background:rgba(255,45,85,.15);color:var(--math);font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}

.sign-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:var(--space-2);max-width:240px;margin:var(--space-4) 0;}
.sign-cell{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-sm);padding:var(--space-3);text-align:center;font-size:18px;font-weight:700;}
.sign-cell.pos{color:var(--system-green);}
.sign-cell.neg{color:var(--math);}

.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);line-height:1.4;}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--math);background:rgba(255,45,85,.1);}

.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav-back{font-size:14px;color:var(--text-tertiary);text-decoration:none;display:flex;align-items:center;gap:6px;transition:color var(--transition-base);}
.ch-nav-back:hover{color:var(--text-primary);}
.ch-nav-next{display:flex;align-items:center;gap:var(--space-3);background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-3) var(--space-5);text-decoration:none;color:inherit;transition:all var(--transition-base);}
.ch-nav-next:hover{background:var(--bg-tertiary);border-color:rgba(227,227,232,0.12);transform:translateX(3px);}
.ch-nav-prev{display:flex;align-items:center;gap:var(--space-3);background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-3) var(--space-5);text-decoration:none;color:inherit;transition:all var(--transition-base);}
.ch-nav-prev:hover{background:var(--bg-tertiary);border-color:rgba(227,227,232,0.12);transform:translateX(-3px);}
.ch-nav-label{font-size:11px;color:var(--text-tertiary);text-transform:uppercase;letter-spacing:.06em;margin-bottom:2px;}
.ch-nav-title{font-size:14px;font-weight:600;}

@keyframes fadeIn{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
.ch-main{animation:fadeIn .5s ease backwards;}
@media(max-width:600px){
.ch-wrap{padding:var(--space-6) var(--space-4);}
.ch-header h1{font-size:26px;}
.ch-eyebrow{font-size:11px;}
.ch-section h2{font-size:18px;}
.ch-section p,.ch-section li,.cb p{font-size:15px;}
.math-block{padding:var(--space-4) var(--space-3);font-size:.88em;}
.cb{padding:var(--space-4);}
.ch-section,.math-block{max-width:100%;overflow-x:auto;-webkit-overflow-scrolling:touch;}
.ch-nav{flex-direction:column;gap:var(--space-3);}
.ch-nav a{width:100%;justify-content:center;text-align:center;}
.steps li{gap:var(--space-2);}
.losbar-grid,.case-grid{grid-template-columns:1fr;}
.rules-table,.param-table{display:block;overflow-x:auto;-webkit-overflow-scrolling:touch;white-space:nowrap;}
.rules-table th,.rules-table td,.param-table th,.param-table td{white-space:normal;min-width:90px;}
.ch-nav-prev,.ch-nav-next{width:100%;justify-content:center;}
}
@media(max-width:480px){
.ch-wrap{padding:var(--space-5) var(--space-3);}
.ch-breadcrumb{font-size:12px;flex-wrap:wrap;gap:4px;}
.ch-header h1{font-size:22px;letter-spacing:-.02em;}
.ch-header-meta{font-size:12px;flex-direction:column;gap:4px;}
.ch-eyebrow{font-size:10px;padding:2px 8px;}
.ch-section h2{font-size:16px;}
.ch-section h3{font-size:15px;}
.ch-section p,.ch-section li,.cb p{font-size:14px;}
.math-block{padding:var(--space-3);font-size:.82em;overflow-x:auto;}
.cb{padding:var(--space-3) var(--space-4);}
.cb p{font-size:14px;}
.steps li{font-size:14px;}
.ch-nav a{font-size:13px;padding:var(--space-3);}
.losbar-grid,.case-grid{grid-template-columns:1fr;}
.losbar-card,.case-card{padding:var(--space-4);}
.param-table,.rules-table{font-size:12px;}
}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important;}}
</style>

<div class="ch-wrap">
<div class="ch-main" id="chapter-content">

  <div class="ch-breadcrumb">
    <a href="/learn/">Learn</a><span class="ch-breadcrumb-sep">›</span>
    <a href="/learn/mathematik/">Mathematik</a><span class="ch-breadcrumb-sep">›</span>
    <span>Kapitel 2</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">📐 Kapitel 2</div>
    <h1>Determinanten</h1>
    <div class="ch-header-meta">
      <span>📄 Basiert auf Matrizen_2_2</span>
      <span>⏱ ca. 25 Min</span>
      <span>🎯 Lineare Algebra</span>
    </div>
  </div>

  <!-- 1. Was ist eine Determinante? -->
  <div class="ch-section" id="s1">
    <h2>Was ist eine Determinante?</h2>
    <p>Die <strong>Determinante</strong> ist eine Funktion, die jeder <em>quadratischen</em> Matrix eine einzelne reelle Zahl zuordnet. Sie liefert wichtige Informationen über die Matrix — zum Beispiel, ob ein Gleichungssystem eindeutig lösbar ist.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Determinante</div>
      <p>Für eine quadratische Matrix \(A \in \mathbb{R}^{n \times n}\) ist die Determinante eine reelle Zahl:</p>
      <div class="math-block">\[\det(A) \in \mathbb{R} \qquad \text{auch geschrieben als} \quad |A|\]</div>
      <p>Die Determinante ist nur für <strong>quadratische</strong> Matrizen definiert.</p>
    </div>

    <h3>Geometrische Bedeutung</h3>
    <p>Anschaulich misst die Determinante das <strong>orientierte Volumen</strong>, das die Spaltenvektoren der Matrix aufspannen:</p>
    <ul>
      <li>\(n = 2\): \(|\det(A)|\) ist die Fläche des Parallelogramms</li>
      <li>\(n = 3\): \(|\det(A)|\) ist das Volumen des Spats</li>
      <li>Das Vorzeichen gibt die Orientierung an (positiv = rechtshändig)</li>
    </ul>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Reguläre und singuläre Matrix</div>
      <p><strong>Regulär</strong> (\(\det(A) \neq 0\)): Die Matrix ist invertierbar, hat vollen Rang, und \(A\mathbf{x} = \mathbf{b}\) hat <em>genau eine</em> Lösung.</p>
      <p><strong>Singulär</strong> (\(\det(A) = 0\)): Die Matrix ist nicht invertierbar, und \(A\mathbf{x} = \mathbf{b}\) hat <em>keine oder unendlich viele</em> Lösungen.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Für \(A = \begin{pmatrix}1&2\\2&4\end{pmatrix}\) gilt: \(\det(A) = 1 \cdot 4 - 2 \cdot 2 = 0\) → <strong>singulär</strong>.</p>
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Prüfungstipp</div>
      <p>„Die Determinante misst das orientierte Volumen" — dieser Satz wird gerne als Kurzantwort in Klausuren verlangt.</p>
    </div>
  </div>

  <!-- 2. 2×2 Determinante -->
  <div class="ch-section" id="s2">
    <h2>Die 2×2-Determinante</h2>
    <p>Für eine \(2 \times 2\)-Matrix gibt es eine einfache Formel: Hauptdiagonale minus Nebendiagonale.</p>

    <div class="cb cb-def">
      <div class="cb-label">Formel</div>
      <div class="cb-title">2×2-Determinante</div>
      <div class="math-block">\[\det\begin{pmatrix}a&b\\c&d\end{pmatrix} = ad - bc\]</div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="math-block">\[\det\begin{pmatrix}1&2\\3&4\end{pmatrix} = 1 \cdot 4 - 2 \cdot 3 = 4 - 6 = -2\]</div>
      <p>Da \(\det(A) = -2 \neq 0\) ist die Matrix <strong>regulär</strong>.</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Berechne die Determinanten von \(A = \begin{pmatrix}2&-1\\3&4\end{pmatrix}\) und \(B = \begin{pmatrix}0&5\\-2&1\end{pmatrix}\).</p>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(\det(A) = 2\cdot4-(-1)\cdot3 = 8+3 = 11\), \(\det(B) = 0\cdot1-5\cdot(-2) = 10\)</p>
    </div>
  </div>

  <!-- 3. Regel von Sarrus -->
  <div class="ch-section" id="s3">
    <h2>Regel von Sarrus (3×3)</h2>
    <p>Für \(3 \times 3\)-Matrizen gibt es ein praktisches Merkschema: die <strong>Regel von Sarrus</strong>. Man erweitert die Matrix um die ersten zwei Spalten rechts und liest dann Diagonalen ab.</p>

    <div class="cb cb-note">
      <div class="cb-label">Achtung</div>
      <p>Die Regel von Sarrus gilt <strong>nur für 3×3-Matrizen</strong>! Für größere Matrizen muss man die Laplace-Entwicklung verwenden.</p>
    </div>

    <ol class="steps">
      <li>Schreibe die Matrix auf und hänge die ersten zwei Spalten rechts nochmal an.</li>
      <li>Addiere die drei <strong>absteigenden</strong> Diagonalen (von links oben nach rechts unten).</li>
      <li>Subtrahiere die drei <strong>aufsteigenden</strong> Diagonalen (von links unten nach rechts oben).</li>
    </ol>

    <div class="cb cb-def">
      <div class="cb-label">Formel</div>
      <div class="cb-title">Sarrus-Regel</div>
      <div class="math-block">
        \[\det(A) = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32}\]
        \[\phantom{\det(A)=}{} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}\]
      </div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Sarrus-Regel anwenden</div>
      <p>Für \(A = \begin{pmatrix}1&2&3\\4&5&6\\7&8&9\end{pmatrix}\):</p>
      <p>Absteigende Diagonalen: \(1\cdot5\cdot9 + 2\cdot6\cdot7 + 3\cdot4\cdot8 = 45+84+96 = 225\)</p>
      <p>Aufsteigende Diagonalen: \(3\cdot5\cdot7 + 1\cdot6\cdot8 + 2\cdot4\cdot9 = 105+48+72 = 225\)</p>
      <div class="math-block">\[\det(A) = 225 - 225 = 0 \quad \Rightarrow \text{ singulär!}\]</div>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Berechne \(\det(D)\) mit der Regel von Sarrus:</p>
      <div class="math-block">\[D = \begin{pmatrix}2&1&3\\0&-1&4\\1&2&0\end{pmatrix}\]</div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ Absteigende: \(2\cdot(-1)\cdot0+1\cdot4\cdot1+3\cdot0\cdot2=0+4+0=4\). Aufsteigende: \(3\cdot(-1)\cdot1+2\cdot4\cdot2+1\cdot0\cdot0=-3+16+0=13\). \(\det(D)=4-13=-9\).</p>
    </div>
  </div>

  <!-- 4. Laplace-Entwicklung -->
  <div class="ch-section" id="s4">
    <h2>Laplace-Entwicklung</h2>
    <p>Die <strong>Laplace-Entwicklung</strong> ist die allgemeine Methode für Determinanten beliebiger Größe. Man zerlegt die Determinante in kleinere \(2\times2\)-Determinanten.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Minor und Kofaktor</div>
      <p><strong>Minor \(M_{ij}\):</strong> Determinante der Matrix, die entsteht, wenn man Zeile \(i\) und Spalte \(j\) streicht.</p>
      <p><strong>Kofaktor:</strong> \(A_{ij} = (-1)^{i+j} \cdot M_{ij}\)</p>
      <p>Das Vorzeichen folgt dem Schachbrettmuster:</p>
    </div>

    <div class="sign-grid">
      <div class="sign-cell pos">+</div><div class="sign-cell neg">−</div><div class="sign-cell pos">+</div>
      <div class="sign-cell neg">−</div><div class="sign-cell pos">+</div><div class="sign-cell neg">−</div>
      <div class="sign-cell pos">+</div><div class="sign-cell neg">−</div><div class="sign-cell pos">+</div>
    </div>

    <div class="cb cb-def">
      <div class="cb-label">Formel</div>
      <div class="cb-title">Laplace-Entwicklung nach Zeile \(i\)</div>
      <div class="math-block">\[\det(A) = \sum_{j=1}^{n} a_{ij} \cdot A_{ij} = \sum_{j=1}^{n} a_{ij} \cdot (-1)^{i+j} \cdot M_{ij}\]</div>
      <p><strong>Strategie:</strong> Wähle immer die Zeile (oder Spalte) mit den meisten Nullen — das reduziert den Rechenaufwand!</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Entwicklung nach der 1. Zeile</div>
      <p>Für \(B = \begin{pmatrix}1&2&3\\4&5&6\\7&8&9\end{pmatrix}\), Entwicklung nach Zeile 1:</p>
      <div class="math-block">
        \[\det(B) = 1\cdot\det\begin{pmatrix}5&6\\8&9\end{pmatrix} - 2\cdot\det\begin{pmatrix}4&6\\7&9\end{pmatrix} + 3\cdot\det\begin{pmatrix}4&5\\7&8\end{pmatrix}\]
      </div>
      <div class="math-block">
        \[= 1\cdot(45-48) - 2\cdot(36-42) + 3\cdot(32-35) = -3+12-9 = 0\]
      </div>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Berechne \(\det(E)\) mit Laplace-Entwicklung nach der 2. Zeile (wegen der Null!):</p>
      <div class="math-block">\[E = \begin{pmatrix}1&2&0\\3&0&1\\-1&1&2\end{pmatrix}\]</div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ Zeile 2 hat eine Null, also Entwicklung: \(-3\cdot\det\begin{pmatrix}2&0\\1&2\end{pmatrix} + 0 - 1\cdot\det\begin{pmatrix}1&2\\-1&1\end{pmatrix} = -3\cdot4-1\cdot3=-15\).</p>
    </div>
  </div>

  <!-- 5. Dreiecksmatrizen -->
  <div class="ch-section" id="s5">
    <h2>Dreiecks- und Diagonalmatrizen</h2>
    <p>Für Dreiecks- und Diagonalmatrizen gibt es eine besonders einfache Regel, die in der Praxis sehr nützlich ist — zum Beispiel nach einer Gauß-Elimination.</p>

    <div class="cb cb-def">
      <div class="cb-label">Regel</div>
      <div class="cb-title">Determinante von Dreiecksmatrizen</div>
      <p>Die Determinante einer oberen oder unteren Dreiecksmatrix (und damit auch jeder Diagonalmatrix) ist das <strong>Produkt der Diagonalelemente</strong>:</p>
      <div class="math-block">\[\det(A) = a_{11} \cdot a_{22} \cdot \ldots \cdot a_{nn}\]</div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="math-block">
        \[\det\begin{pmatrix}2&5&-1\\0&3&4\\0&0&-2\end{pmatrix} = 2 \cdot 3 \cdot (-2) = -12\]
      </div>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Bestimme \(\det(F)\) und \(\det(G)\):</p>
      <div class="math-block">
        \[F = \begin{pmatrix}2&5&-1\\0&3&4\\0&0&-2\end{pmatrix} \qquad G = \begin{pmatrix}-1&0&0\\7&4&0\\2&-3&1\end{pmatrix}\]
      </div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(\det(F) = 2\cdot3\cdot(-2) = -12\), \(\det(G) = (-1)\cdot4\cdot1 = -4\)</p>
    </div>
  </div>

  <!-- 6. Rechenregeln -->
  <div class="ch-section" id="s6">
    <h2>Wichtige Rechenregeln</h2>

    <ul>
      <li>\(\det(AB) = \det(A) \cdot \det(B)\)</li>
      <li>\(\det(A^T) = \det(A)\)</li>
      <li>\(\det(A^{-1}) = \dfrac{1}{\det(A)}\) (falls \(A\) invertierbar)</li>
      <li>\(\det(\lambda A) = \lambda^n \cdot \det(A)\) bei einer \(n\times n\)-Matrix</li>
      <li>Matrix mit zwei <strong>identischen Zeilen</strong>: \(\det(A) = 0\)</li>
      <li>Matrix mit einer <strong>Nullzeile</strong>: \(\det(A) = 0\)</li>
    </ul>

    <div class="cb cb-note">
      <div class="cb-label">Klausurrelevant</div>
      <p>Zwei besonders häufige Fragen: „Warum ist eine Matrix mit zwei gleichen Zeilen singulär?" (weil \(\det = 0\)) und \(\det(AB) = \det(A)\cdot\det(B)\) für konkrete Berechnungen.</p>
    </div>
  </div>

  <div class="ch-nav">
    <a href="/learn/matrizen-grundlagen/" class="ch-nav-prev">
      <div>
        <div class="ch-nav-label">← Vorheriges</div>
        <div class="ch-nav-title">Matrizen Grundlagen</div>
      </div>
    </a>
    <a href="/learn/matrizengleichungen-rang/" class="ch-nav-next">
      <div>
        <div class="ch-nav-label">Nächstes Kapitel</div>
        <div class="ch-nav-title">Matrizengleichungen & Rang →</div>
      </div>
    </a>
  </div>

</div>

<aside class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#s1">1. Was ist eine Determinante?</a></li>
    <li><a href="#s2">2. Die 2×2-Determinante</a></li>
    <li><a href="#s3">3. Regel von Sarrus</a></li>
    <li><a href="#s4">4. Laplace-Entwicklung</a></li>
    <li><a href="#s5">5. Dreiecksmatrizen</a></li>
    <li><a href="#s6">6. Rechenregeln</a></li>
  </ul>
</aside>
</div>

<script>
const sections=document.querySelectorAll('.ch-section');const tocLinks=document.querySelectorAll('.ch-toc a');
const observer=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){const id=e.target.id;tocLinks.forEach(l=>{l.classList.toggle('active',l.getAttribute('href')==='#'+id);});}});},{rootMargin:'-20% 0px -70% 0px'});
sections.forEach(s=>observer.observe(s));
</script>
