---
layout: page
title:
permalink: /learn/matrizen-grundlagen/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root {
  --math: #FF2D55;
  --system-indigo: #5856D6;
  --system-green: #34C759;
  --system-orange: #FF9500;
  --system-blue: #007AFF;
  --bg-primary: #000000;
  --bg-secondary: #1C1C1E;
  --bg-tertiary: #2C2C2E;
  --text-primary: #FFFFFF;
  --text-secondary: #EBEBF5;
  --text-tertiary: #8E8E93;
  --separator: rgba(255,255,255,0.10);
  --font-stack: -apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;
  --font-mono: "SF Mono",SFMono-Regular,ui-monospace,Menlo,Monaco,monospace;
  --space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;
  --space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;
  --radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;
  --transition-base:250ms cubic-bezier(0.4,0,0.2,1);
}

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.6;letter-spacing:-0.015em;}
.post-header,.page-heading,header.post-header{display:none!important;}

/* ─── Layout ─── */
.ch-wrap {
  max-width: 1100px;
  margin: 0 auto;
  padding: var(--space-10) var(--space-5);
  display: grid;
  grid-template-columns: 1fr 220px;
  gap: var(--space-12);
  align-items: start;
}

@media(max-width: 860px) {
  .ch-wrap { grid-template-columns: 1fr; gap: var(--space-8); }
  .ch-toc { display: none; }
}

/* ─── Breadcrumb ─── */
.ch-breadcrumb {
  display: flex; align-items: center; gap: var(--space-2);
  font-size: 13px; color: var(--text-tertiary); margin-bottom: var(--space-8);
}
.ch-breadcrumb a { color: var(--text-tertiary); text-decoration: none; }
.ch-breadcrumb a:hover { color: var(--text-primary); }
.ch-breadcrumb-sep { opacity: 0.4; }

/* ─── Chapter header ─── */
.ch-header { margin-bottom: var(--space-10); padding-bottom: var(--space-8); border-bottom: 1px solid var(--separator); }
.ch-eyebrow {
  display: inline-flex; align-items: center; gap: 6px;
  font-size: 12px; font-weight: 600; text-transform: uppercase; letter-spacing: .08em;
  color: var(--math); background: rgba(255,45,85,.1); border: 1px solid rgba(255,45,85,.2);
  border-radius: var(--radius-full); padding: 3px 10px; margin-bottom: var(--space-4);
}
.ch-header h1 {
  font-size: clamp(28px,4vw,42px); font-weight: 700; letter-spacing: -.025em;
  line-height: 1.08; margin-bottom: var(--space-3);
}
.ch-header-meta {
  font-size: 14px; color: var(--text-tertiary);
  display: flex; gap: var(--space-4); flex-wrap: wrap;
}
.ch-header-meta span { display: flex; align-items: center; gap: 5px; }

/* ─── Content sections ─── */
.ch-section { margin-bottom: var(--space-12); }
.ch-section h2 {
  font-size: 22px; font-weight: 700; letter-spacing: -.02em;
  color: var(--text-primary); margin-bottom: var(--space-5);
  padding-top: var(--space-2);
  display: flex; align-items: center; gap: var(--space-3);
}
.ch-section h2::before {
  content: '';
  display: block; width: 3px; height: 22px;
  background: var(--math); border-radius: 2px; flex-shrink: 0;
}
.ch-section h3 {
  font-size: 17px; font-weight: 600; color: var(--text-secondary);
  margin: var(--space-6) 0 var(--space-3);
}
.ch-section p { font-size: 16px; color: var(--text-secondary); line-height: 1.75; margin-bottom: var(--space-4); }
.ch-section ul { margin: 0 0 var(--space-4) var(--space-5); }
.ch-section li { font-size: 16px; color: var(--text-secondary); line-height: 1.7; margin-bottom: var(--space-1); }

/* ─── Callout boxes ─── */
.cb {
  border-radius: var(--radius-lg);
  padding: var(--space-5) var(--space-6);
  margin: var(--space-6) 0;
  border-left: 3px solid;
}
.cb-label {
  font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: .08em;
  margin-bottom: var(--space-3);
}
.cb-title { font-size: 16px; font-weight: 600; margin-bottom: var(--space-2); }
.cb p { font-size: 15px; line-height: 1.7; margin-bottom: var(--space-3); }
.cb p:last-child { margin-bottom: 0; }

/* Definition */
.cb-def { background: rgba(88,86,214,.1); border-color: var(--system-indigo); }
.cb-def .cb-label { color: var(--system-indigo); }

/* Beispiel */
.cb-ex { background: rgba(52,199,89,.08); border-color: var(--system-green); }
.cb-ex .cb-label { color: var(--system-green); }

/* Übung */
.cb-task { background: rgba(255,149,0,.08); border-color: var(--system-orange); }
.cb-task .cb-label { color: var(--system-orange); }

/* Merke / Achtung */
.cb-note { background: rgba(255,45,85,.08); border-color: var(--math); }
.cb-note .cb-label { color: var(--math); }

/* Tipp */
.cb-tip { background: rgba(0,122,255,.08); border-color: var(--system-blue); }
.cb-tip .cb-label { color: var(--system-blue); }

/* ─── Math display ─── */
.math-block {
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-md); padding: var(--space-5) var(--space-6);
  margin: var(--space-4) 0; overflow-x: auto; text-align: center;
  font-size: 1.05em;
}
.math-label {
  font-size: 12px; color: var(--text-tertiary); font-style: italic;
  margin-bottom: var(--space-2); text-align: left;
}

/* ─── Matrix grid (visual helper) ─── */
.matrix-types {
  display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: var(--space-3); margin: var(--space-4) 0;
}
.matrix-card {
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-md); padding: var(--space-4);
}
.matrix-card-name { font-size: 13px; font-weight: 600; color: var(--text-secondary); margin-bottom: var(--space-2); }
.matrix-card-math { font-size: 13px; }

/* ─── Step list ─── */
.steps { list-style: none; padding: 0; margin: var(--space-3) 0; counter-reset: step; }
.steps li {
  counter-increment: step;
  display: flex; gap: var(--space-3); margin-bottom: var(--space-4);
  font-size: 15px; color: var(--text-secondary); line-height: 1.65;
}
.steps li::before {
  content: counter(step);
  min-width: 24px; height: 24px; border-radius: 50%;
  background: rgba(255,45,85,.15); color: var(--math);
  font-size: 12px; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0; margin-top: 1px;
}

/* ─── Rules grid ─── */
.rules-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: var(--space-3); margin: var(--space-4) 0;
}
@media(max-width:600px){ .rules-grid { grid-template-columns: 1fr; } }
.rule-card {
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-md); padding: var(--space-4);
}
.rule-card-title { font-size: 13px; font-weight: 600; color: var(--text-tertiary); margin-bottom: var(--space-3); text-transform: uppercase; letter-spacing: .05em; }
.rule-card ul { list-style: none; padding: 0; }
.rule-card li { font-size: 14px; color: var(--text-secondary); padding: 3px 0; }

/* ─── TOC (Sidebar) ─── */
.ch-toc {
  position: sticky; top: 80px;
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-xl); padding: var(--space-5);
}
.ch-toc-title { font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: .08em; color: var(--text-tertiary); margin-bottom: var(--space-4); }
.ch-toc ul { list-style: none; padding: 0; }
.ch-toc li { margin-bottom: var(--space-1); }
.ch-toc a {
  font-size: 13px; color: var(--text-tertiary); text-decoration: none;
  display: block; padding: 4px 8px; border-radius: var(--radius-sm);
  transition: all var(--transition-base); line-height: 1.4;
}
.ch-toc a:hover { color: var(--text-primary); background: var(--bg-tertiary); }
.ch-toc a.active { color: var(--math); background: rgba(255,45,85,.1); }

/* ─── Next chapter nav ─── */
.ch-nav {
  margin-top: var(--space-12); padding-top: var(--space-8);
  border-top: 1px solid var(--separator);
  display: flex; justify-content: space-between; align-items: center; gap: var(--space-4);
  flex-wrap: wrap;
}
.ch-nav-back {
  font-size: 14px; color: var(--text-tertiary); text-decoration: none;
  display: flex; align-items: center; gap: 6px; transition: color var(--transition-base);
}
.ch-nav-back:hover { color: var(--text-primary); }
.ch-nav-next {
  display: flex; align-items: center; gap: var(--space-3);
  background: var(--bg-secondary); border: 1px solid var(--separator);
  border-radius: var(--radius-xl); padding: var(--space-3) var(--space-5);
  text-decoration: none; color: inherit; transition: all var(--transition-base);
}
.ch-nav-next:hover { background: var(--bg-tertiary); border-color: rgba(255,255,255,.2); transform: translateX(3px); }
.ch-nav-next-label { font-size: 11px; color: var(--text-tertiary); text-transform: uppercase; letter-spacing: .06em; margin-bottom: 2px; }
.ch-nav-next-title { font-size: 14px; font-weight: 600; }

@keyframes fadeIn { from{opacity:0;transform:translateY(10px)} to{opacity:1;transform:none} }
.ch-main { animation: fadeIn .5s ease backwards; }
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important;}}
</style>

<div class="ch-wrap">

<!-- ═══ MAIN CONTENT ═══ -->
<div class="ch-main" id="chapter-content">

  <div class="ch-breadcrumb">
    <a href="/learn/">Learn</a>
    <span class="ch-breadcrumb-sep">›</span>
    <a href="/learn/mathematik/">Mathematik</a>
    <span class="ch-breadcrumb-sep">›</span>
    <span>Kapitel 1</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">📐 Kapitel 1</div>
    <h1>Matrizen – Grundlagen</h1>
    <div class="ch-header-meta">
      <span>📄 Basiert auf Matrizen_2_1</span>
      <span>⏱ ca. 20 Min</span>
      <span>🎯 Lineare Algebra</span>
    </div>
  </div>

  <!-- ═══ 1. Was ist eine Matrix? ═══ -->
  <div class="ch-section" id="s1">
    <h2>Was ist eine Matrix?</h2>

    <p>Eine <strong>Matrix</strong> ist eine rechteckige Anordnung von Zahlen, geordnet in Zeilen und Spalten. Man begegnet ihnen überall in der Mathematik: beim Lösen von Gleichungssystemen, in der Geometrie, in der Datenwissenschaft.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Matrix</div>
      <p>Eine Matrix \(A\) mit \(m\) Zeilen und \(n\) Spalten schreibt man:</p>
      <div class="math-block">
        \[A = \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn} \end{pmatrix} \in \mathbb{R}^{m \times n}\]
      </div>
      <p>Das Element \(a_{ij}\) steht in Zeile \(i\) und Spalte \(j\). Die <strong>Größe</strong> der Matrix ist \(m \times n\) (Zeilen × Spalten).</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Zwei konkrete Matrizen</div>
      <p>Eine \(2 \times 2\)-Matrix und eine \(3 \times 2\)-Matrix:</p>
      <div class="math-block">
        \[A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \qquad B = \begin{pmatrix} 2 & 5 \\ 0 & 3 \\ 7 & 1 \end{pmatrix}\]
      </div>
      <p>Bei \(B\) gilt: \(b_{23} = 3\) (Zeile 2, Spalte 2... Moment: \(b_{23}\) wäre Zeile 2, Spalte 3 — aber \(B\) hat nur 2 Spalten, also existiert \(b_{23}\) nicht!). Das Element \(b_{21} = 0\).</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Gegeben: \(\displaystyle A = \begin{pmatrix} 2 & 4 & 1 \\ 0 & 3 & 5 \end{pmatrix}\)</p>
      <p>Bestimme die Größe der Matrix und das Element \(a_{23}\).</p>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ Lösung: \(2 \times 3\)-Matrix. \(a_{23} = 5\).</p>
    </div>
  </div>

  <!-- ═══ 2. Besondere Matrizen ═══ -->
  <div class="ch-section" id="s2">
    <h2>Besondere Matrizen</h2>

    <p>Einige Matrizen treten so häufig auf, dass sie eigene Namen haben:</p>

    <h3>Nullmatrix \(O\)</h3>
    <p>Alle Einträge sind null. Sie ist das neutrale Element der Matrizenaddition.</p>
    <div class="math-block">
      \[O = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}\]
    </div>

    <h3>Einheitsmatrix \(I\)</h3>
    <p>Auf der Hauptdiagonale stehen Einsen, überall sonst Nullen. Sie ist das neutrale Element der Matrizenmultiplikation: \(A \cdot I = I \cdot A = A\).</p>
    <div class="math-block">
      \[I_3 = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}\]
    </div>

    <h3>Diagonalmatrix</h3>
    <p>Nur auf der Hauptdiagonale stehen Einträge ungleich null. Der Rest ist null.</p>
    <div class="math-block">
      \[D = \begin{pmatrix} 3 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 2 \end{pmatrix}\]
    </div>

    <h3>Dreiecksmatrizen</h3>
    <p>Bei einer <strong>oberen Dreiecksmatrix</strong> sind alle Einträge <em>unterhalb</em> der Hauptdiagonale null:</p>
    <div class="math-block">
      \[T = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & 6 \end{pmatrix}\]
    </div>
    <p>Entsprechend ist bei einer <strong>unteren Dreiecksmatrix</strong> alles <em>oberhalb</em> der Diagonale null.</p>

    <h3>Vektoren als Matrizen</h3>
    <p>Ein <strong>Spaltenvektor</strong> ist eine \(n \times 1\)-Matrix, ein <strong>Zeilenvektor</strong> eine \(1 \times n\)-Matrix:</p>
    <div class="math-block">
      \[\mathbf{v} = \begin{pmatrix} 2 \\ 5 \\ 1 \end{pmatrix} \quad (3 \times 1) \qquad \mathbf{w} = \begin{pmatrix} 2 & 5 & 1 \end{pmatrix} \quad (1 \times 3)\]
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Prüfungstipp</div>
      <p>Die Einheitsmatrix \(I\) und die Nullmatrix \(O\) spielen in der Linearen Algebra dieselbe Rolle wie die 1 und die 0 in den reellen Zahlen. Das hilft beim Merken der Rechenregeln.</p>
    </div>
  </div>

  <!-- ═══ 3. Addition und Subtraktion ═══ -->
  <div class="ch-section" id="s3">
    <h2>Addition und Subtraktion</h2>

    <p>Zwei Matrizen lassen sich nur addieren oder subtrahieren, wenn sie <strong>dieselbe Größe</strong> haben. Die Rechenoperation erfolgt dann <strong>elementweise</strong>.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Matrizenaddition</div>
      <p>Für \(A, B \in \mathbb{R}^{m \times n}\) gilt:</p>
      <div class="math-block">
        \[(A + B)_{ij} = a_{ij} + b_{ij}\]
      </div>
      <p>Jeder Eintrag von \(A+B\) ergibt sich aus der Summe der entsprechenden Einträge von \(A\) und \(B\).</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Addition und Subtraktion</div>
      <div class="math-block">
        \[\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} + \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix} = \begin{pmatrix} 6 & 8 \\ 10 & 12 \end{pmatrix}\]
      </div>
      <div class="math-block">
        \[\begin{pmatrix} 4 & 1 \\ 2 & 3 \end{pmatrix} - \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 3 & -1 \\ 2 & 2 \end{pmatrix}\]
      </div>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Berechne \(A + B\) und \(A - B\) für:</p>
      <div class="math-block">
        \[A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}, \quad B = \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix}\]
      </div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(A+B = \begin{pmatrix}6&8\\10&12\end{pmatrix}\), \(A-B = \begin{pmatrix}-4&-4\\-4&-4\end{pmatrix}\)</p>
    </div>
  </div>

  <!-- ═══ 4. Skalarmultiplikation ═══ -->
  <div class="ch-section" id="s4">
    <h2>Skalarmultiplikation</h2>

    <p>Bei der <strong>Skalarmultiplikation</strong> wird eine Matrix mit einer einzelnen Zahl (einem <em>Skalar</em> \(\lambda\)) multipliziert. Das Ergebnis: jeder Eintrag der Matrix wird mit \(\lambda\) multipliziert.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Skalarmultiplikation</div>
      <div class="math-block">
        \[(\lambda \cdot A)_{ij} = \lambda \cdot a_{ij}\]
      </div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="math-block">
        \[2 \cdot \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 6 & 8 \end{pmatrix}\]
      </div>
      <div class="math-block">
        \[-1 \cdot \begin{pmatrix} 2 & 0 \\ 1 & 3 \end{pmatrix} = \begin{pmatrix} -2 & 0 \\ -1 & -3 \end{pmatrix}\]
      </div>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Berechne \(2A\) und \(-3B\) für \(A = \begin{pmatrix}1&2\\3&4\end{pmatrix}\), \(B = \begin{pmatrix}5&6\\7&8\end{pmatrix}\).</p>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(2A = \begin{pmatrix}2&4\\6&8\end{pmatrix}\), \(-3B = \begin{pmatrix}-15&-18\\-21&-24\end{pmatrix}\)</p>
    </div>
  </div>

  <!-- ═══ 5. Matrixmultiplikation ═══ -->
  <div class="ch-section" id="s5">
    <h2>Matrixmultiplikation</h2>

    <p>Die Matrixmultiplikation ist die wichtigste — und zunächst ungewohnteste — Operation. Sie funktioniert nur unter einer bestimmten Bedingung.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Matrixmultiplikation</div>
      <p><strong>Voraussetzung:</strong> \(A \in \mathbb{R}^{m \times n}\) und \(B \in \mathbb{R}^{n \times p}\). Die Spaltenzahl von \(A\) muss gleich der Zeilenzahl von \(B\) sein.</p>
      <p>Das Ergebnis \(C = AB\) ist eine \(m \times p\)-Matrix mit:</p>
      <div class="math-block">
        \[c_{ik} = \sum_{j=1}^{n} a_{ij} \cdot b_{jk} \qquad \text{(Zeile } i \text{ von } A \text{ mal Spalte } k \text{ von } B)\]
      </div>
    </div>

    <h3>Schritt-für-Schritt-Vorgehen</h3>
    <ol class="steps">
      <li>Prüfe: Kann man multiplizieren? Spalten von \(A\) = Zeilen von \(B\)?</li>
      <li>Bestimme die Größe des Ergebnisses: Zeilen von \(A\) × Spalten von \(B\).</li>
      <li>Berechne jeden Eintrag \(c_{ik}\): Zeile \(i\) von \(A\) skalar multipliziert mit Spalte \(k\) von \(B\).</li>
    </ol>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Zwei 2×2-Matrizen multiplizieren</div>
      <div class="math-block">
        \[\begin{pmatrix} 2 & 0 \\ 1 & 3 \end{pmatrix} \cdot \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}\]
      </div>
      <p>Eintrag \(c_{11}\): Zeile 1 von \(A\) · Spalte 1 von \(B\): \(2 \cdot 1 + 0 \cdot 3 = 2\)</p>
      <p>Eintrag \(c_{12}\): Zeile 1 von \(A\) · Spalte 2 von \(B\): \(2 \cdot 2 + 0 \cdot 4 = 4\)</p>
      <p>Eintrag \(c_{21}\): Zeile 2 von \(A\) · Spalte 1 von \(B\): \(1 \cdot 1 + 3 \cdot 3 = 10\)</p>
      <p>Eintrag \(c_{22}\): Zeile 2 von \(A\) · Spalte 2 von \(B\): \(1 \cdot 2 + 3 \cdot 4 = 14\)</p>
      <div class="math-block">
        \[\Rightarrow\quad \begin{pmatrix} 2 & 0 \\ 1 & 3 \end{pmatrix} \cdot \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 10 & 14 \end{pmatrix}\]
      </div>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Achtung</div>
      <div class="cb-title">Matrixmultiplikation ist nicht kommutativ!</div>
      <p>Im Allgemeinen gilt \(AB \neq BA\). Das ist der größte Unterschied zu den gewöhnlichen Zahlen. Immer auf die Reihenfolge achten!</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Berechne \(AB\) und \(BA\) für \(A = \begin{pmatrix}1&2\\3&4\end{pmatrix}\), \(B = \begin{pmatrix}5&6\\7&8\end{pmatrix}\). Was fällt auf?</p>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(AB = \begin{pmatrix}19&22\\43&50\end{pmatrix}\), \(BA = \begin{pmatrix}23&34\\31&46\end{pmatrix}\). Es gilt \(AB \neq BA\).</p>
    </div>
  </div>

  <!-- ═══ 6. Transponieren ═══ -->
  <div class="ch-section" id="s6">
    <h2>Transponieren</h2>

    <p>Die <strong>Transponierte</strong> einer Matrix entsteht, indem man Zeilen und Spalten vertauscht: Zeile 1 wird Spalte 1, Zeile 2 wird Spalte 2, usw.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Transponierte Matrix \(A^T\)</div>
      <div class="math-block">
        \[(A^T)_{ij} = a_{ji}\]
      </div>
      <p>Eine \(m \times n\)-Matrix wird zur \(n \times m\)-Matrix.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Quadratische und nicht-quadratische Matrix</div>
      <div class="math-block">
        \[A = \begin{pmatrix}1&2\\3&4\end{pmatrix} \Rightarrow A^T = \begin{pmatrix}1&3\\2&4\end{pmatrix}\]
      </div>
      <div class="math-block">
        \[B = \begin{pmatrix}2&5&1\\0&3&4\end{pmatrix} \Rightarrow B^T = \begin{pmatrix}2&0\\5&3\\1&4\end{pmatrix}\]
      </div>
      <p>Aus einer \(2 \times 3\)-Matrix wird eine \(3 \times 2\)-Matrix.</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Bestimme \(C^T\) für \(C = \begin{pmatrix}1&4&7\\2&5&8\end{pmatrix}\).</p>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(C^T = \begin{pmatrix}1&2\\4&5\\7&8\end{pmatrix}\) (aus \(2\times3\) wird \(3\times2\))</p>
    </div>
  </div>

  <!-- ═══ 7. Rechenregeln ═══ -->
  <div class="ch-section" id="s7">
    <h2>Rechenregeln im Überblick</h2>

    <p>Hier sind die wichtigsten Rechenregeln zusammengefasst — besonders die Unterschiede zur gewöhnlichen Arithmetik sind klausurrelevant.</p>

    <div class="rules-grid">
      <div class="rule-card">
        <div class="rule-card-title">Addition</div>
        <ul>
          <li>\(A + B = B + A\) ✓</li>
          <li>\((A+B)+C = A+(B+C)\)</li>
          <li>\(A + O = A\)</li>
        </ul>
      </div>
      <div class="rule-card">
        <div class="rule-card-title">Skalarmultiplikation</div>
        <ul>
          <li>\(\lambda(A+B) = \lambda A + \lambda B\)</li>
          <li>\((\lambda+\mu)A = \lambda A + \mu A\)</li>
          <li>\(\lambda(\mu A) = (\lambda\mu)A\)</li>
        </ul>
      </div>
      <div class="rule-card">
        <div class="rule-card-title">Matrixmultiplikation</div>
        <ul>
          <li>\((AB)C = A(BC)\)</li>
          <li>\(A(B+C) = AB + AC\)</li>
          <li>\(\lambda(AB) = (\lambda A)B = A(\lambda B)\)</li>
          <li style="color:var(--math)"><strong>\(AB \neq BA\) (!)</strong></li>
        </ul>
      </div>
      <div class="rule-card">
        <div class="rule-card-title">Transponieren</div>
        <ul>
          <li>\((A^T)^T = A\)</li>
          <li>\((A+B)^T = A^T + B^T\)</li>
          <li>\((AB)^T = B^T A^T\) (!)</li>
          <li>\((\lambda A)^T = \lambda A^T\)</li>
        </ul>
      </div>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Klausurrelevant</div>
      <p>Zwei Regeln werden besonders oft abgefragt: \(AB \neq BA\) (Matrixmultiplikation nicht kommutativ) und \((AB)^T = B^T A^T\) — bei Transponieren kehrt sich die Reihenfolge um!</p>
    </div>
  </div>

  <!-- ─── Navigation ─── -->
  <div class="ch-nav">
    <a href="/learn/mathematik/" class="ch-nav-back">← Alle Kapitel</a>
    <a href="#" class="ch-nav-next" style="opacity:.45;pointer-events:none;">
      <div>
        <div class="ch-nav-next-label">Nächstes Kapitel</div>
        <div class="ch-nav-next-title">Determinanten →</div>
      </div>
    </a>
  </div>

</div><!-- end ch-main -->

<!-- ═══ TOC SIDEBAR ═══ -->
<aside class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#s1">1. Was ist eine Matrix?</a></li>
    <li><a href="#s2">2. Besondere Matrizen</a></li>
    <li><a href="#s3">3. Addition & Subtraktion</a></li>
    <li><a href="#s4">4. Skalarmultiplikation</a></li>
    <li><a href="#s5">5. Matrixmultiplikation</a></li>
    <li><a href="#s6">6. Transponieren</a></li>
    <li><a href="#s7">7. Rechenregeln</a></li>
  </ul>
</aside>

</div><!-- end ch-wrap -->

<script>
// Highlight active TOC item on scroll
const sections = document.querySelectorAll('.ch-section');
const tocLinks = document.querySelectorAll('.ch-toc a');

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const id = entry.target.id;
      tocLinks.forEach(l => {
        l.classList.toggle('active', l.getAttribute('href') === '#' + id);
      });
    }
  });
}, { rootMargin: '-20% 0px -70% 0px' });

sections.forEach(s => observer.observe(s));
</script>
