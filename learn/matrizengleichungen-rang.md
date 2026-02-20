---
layout: page
title:
permalink: /learn/matrizengleichungen-rang/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root{--math:#FF2D55;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;--bg-primary:#000000;--bg-secondary:#1C1C1E;--bg-tertiary:#2C2C2E;--text-primary:#FFFFFF;--text-secondary:#EBEBF5;--text-tertiary:#8E8E93;--separator:rgba(255,255,255,0.10);--font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.6;letter-spacing:-0.015em;}
.post-header,.page-heading,header.post-header{display:none!important;}
.ch-wrap{max-width:1100px;margin:0 auto;padding:var(--space-10) var(--space-5);display:grid;grid-template-columns:1fr 220px;gap:var(--space-12);align-items:start;}
@media(max-width:860px){.ch-wrap{grid-template-columns:1fr;}.ch-toc{display:none;}}
.ch-breadcrumb{display:flex;align-items:center;gap:var(--space-2);font-size:13px;color:var(--text-tertiary);margin-bottom:var(--space-8);}
.ch-breadcrumb a{color:var(--text-tertiary);text-decoration:none;}.ch-breadcrumb a:hover{color:var(--text-primary);}
.ch-breadcrumb-sep{opacity:0.4;}
.ch-header{margin-bottom:var(--space-10);padding-bottom:var(--space-8);border-bottom:1px solid var(--separator);}
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--math);background:rgba(255,45,85,.1);border:1px solid rgba(255,45,85,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-weight:700;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
.ch-header-meta{font-size:14px;color:var(--text-tertiary);display:flex;gap:var(--space-4);flex-wrap:wrap;}
.ch-section{margin-bottom:var(--space-12);}
.ch-section h2{font-size:22px;font-weight:700;letter-spacing:-.02em;color:var(--text-primary);margin-bottom:var(--space-5);display:flex;align-items:center;gap:var(--space-3);}
.ch-section h2::before{content:'';display:block;width:3px;height:22px;background:var(--math);border-radius:2px;flex-shrink:0;}
.ch-section h3{font-size:17px;font-weight:600;color:var(--text-secondary);margin:var(--space-6) 0 var(--space-3);}
.ch-section p{font-size:16px;color:var(--text-secondary);line-height:1.75;margin-bottom:var(--space-4);}
.ch-section ul,.ch-section ol{margin:0 0 var(--space-4) var(--space-5);}
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
.rules-table{width:100%;border-collapse:collapse;margin:var(--space-4) 0;font-size:15px;}
.rules-table th{background:var(--bg-secondary);color:var(--text-tertiary);font-size:11px;text-transform:uppercase;letter-spacing:.06em;padding:var(--space-3) var(--space-4);text-align:left;border-bottom:1px solid var(--separator);}
.rules-table td{padding:var(--space-3) var(--space-4);border-bottom:1px solid rgba(255,255,255,.05);color:var(--text-secondary);vertical-align:middle;}
.rules-table tr:last-child td{border-bottom:none;}
.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--math);background:rgba(255,45,85,.1);}
.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav-prev,.ch-nav-next{display:flex;align-items:center;gap:var(--space-3);background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-3) var(--space-5);text-decoration:none;color:inherit;transition:all var(--transition-base);}
.ch-nav-prev:hover{background:var(--bg-tertiary);border-color:rgba(255,255,255,.2);transform:translateX(-3px);}
.ch-nav-next:hover{background:var(--bg-tertiary);border-color:rgba(255,255,255,.2);transform:translateX(3px);}
.ch-nav-label{font-size:11px;color:var(--text-tertiary);text-transform:uppercase;letter-spacing:.06em;margin-bottom:2px;}
.ch-nav-title{font-size:14px;font-weight:600;}
@keyframes fadeIn{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
.ch-main{animation:fadeIn .5s ease backwards;}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;}}
</style>

<div class="ch-wrap">
<div class="ch-main" id="chapter-content">

  <div class="ch-breadcrumb">
    <a href="/learn/">Learn</a><span class="ch-breadcrumb-sep">›</span>
    <a href="/learn/mathematik/">Mathematik</a><span class="ch-breadcrumb-sep">›</span>
    <span>Kapitel 3</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">📐 Kapitel 3</div>
    <h1>Matrizengleichungen & Rang</h1>
    <div class="ch-header-meta">
      <span>📄 Basiert auf Matrizen_2_3</span>
      <span>⏱ ca. 25 Min</span>
      <span>🎯 Lineare Algebra</span>
    </div>
  </div>

  <!-- 1. Grundprinzip -->
  <div class="ch-section" id="s1">
    <h2>Matrizengleichungen lösen</h2>
    <p>Matrizengleichungen funktionieren ähnlich wie normale Gleichungen — man isoliert \(X\) durch Multiplikation mit der inversen Matrix. Der entscheidende Unterschied: Matrizenmultiplikation ist <strong>nicht kommutativ</strong>, deshalb muss man genau unterscheiden, ob man <em>von links</em> oder <em>von rechts</em> multipliziert.</p>

    <div class="cb cb-def">
      <div class="cb-label">Grundregeln</div>
      <div class="cb-title">Links- vs. Rechtsmultiplikation</div>
      <table class="rules-table">
        <thead><tr><th>Gleichung</th><th>Lösung</th><th>Vorgehen</th></tr></thead>
        <tbody>
          <tr><td>\(AX = B\)</td><td>\(X = A^{-1}B\)</td><td>von links mit \(A^{-1}\) multiplizieren</td></tr>
          <tr><td>\(XA = B\)</td><td>\(X = BA^{-1}\)</td><td>von rechts mit \(A^{-1}\) multiplizieren</td></tr>
          <tr><td>\(AXB = C\)</td><td>\(X = A^{-1}CB^{-1}\)</td><td>links und rechts invertieren</td></tr>
        </tbody>
      </table>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Achtung</div>
      <p>\(AB \neq BA\) — deshalb ist die Reihenfolge beim Multiplizieren entscheidend. Immer darauf achten, ob man <em>von links</em> oder <em>von rechts</em> mit \(A^{-1}\) multipliziert!</p>
    </div>
  </div>

  <!-- 2. Beispiele -->
  <div class="ch-section" id="s2">
    <h2>Fünf Beispieltypen</h2>
    <p>In Klausuren begegnen immer wieder dieselben Grundtypen. Hier sind die wichtigsten mit Lösungsweg:</p>

    <h3>Typ 1: Sammeln und Auflösen</h3>
    <div class="cb cb-ex">
      <div class="cb-label">Beispiel 1</div>
      <p>Löse nach \(X\): \(\quad X + A^T = \dfrac{1}{2}(B-I) + 2X\)</p>
      <ol class="steps">
        <li>Alle \(X\)-Terme auf eine Seite: \(X - 2X = \frac{1}{2}(B-I) - A^T\)</li>
        <li>Zusammenfassen: \(-X = \frac{1}{2}(B-I) - A^T\), also \(\frac{3}{2}A^T - \frac{1}{2}B + \frac{1}{2}I = X\) ... nach Umformen:</li>
        <li>Ergebnis: \(\displaystyle X = \frac{2}{3}(A^T - B + I)\)</li>
      </ol>
    </div>

    <h3>Typ 2: Von links multiplizieren</h3>
    <div class="cb cb-ex">
      <div class="cb-label">Beispiel 2</div>
      <p>Löse nach \(X\): \(\quad AXB = I\)</p>
      <ol class="steps">
        <li>Von links mit \(A^{-1}\): \(\quad XB = A^{-1}\)</li>
        <li>Von rechts mit \(B^{-1}\): \(\quad X = A^{-1}B^{-1}\)</li>
      </ol>
    </div>

    <h3>Typ 3: Ausklammern</h3>
    <div class="cb cb-ex">
      <div class="cb-label">Beispiel 3</div>
      <p>Löse nach \(X\): \(\quad AX = BX + I\)</p>
      <ol class="steps">
        <li>Alle \(X\)-Terme links: \(AX - BX = I\)</li>
        <li>Ausklammern: \((A - B)X = I\)</li>
        <li>Von links mit \((A-B)^{-1}\): \(X = (A-B)^{-1}\)</li>
      </ol>
    </div>

    <h3>Typ 4: Ausmultiplizieren</h3>
    <div class="cb cb-ex">
      <div class="cb-label">Beispiel 4</div>
      <p>Löse nach \(X\): \(\quad 2X(A + I) = 2X + B\)</p>
      <ol class="steps">
        <li>Ausmultiplizieren: \(2XA + 2X = 2X + B\)</li>
        <li>Kürzen: \(2XA = B\), also \(XA = \frac{1}{2}B\)</li>
        <li>Von rechts mit \(A^{-1}\): \(X = \frac{1}{2}BA^{-1}\)</li>
      </ol>
    </div>

    <h3>Typ 5: Mit Transponieren</h3>
    <div class="cb cb-ex">
      <div class="cb-label">Beispiel 5</div>
      <p>Löse nach \(X\): \(\quad (X+A)^T = (B^{-1}+I)X^T\)</p>
      <ol class="steps">
        <li>Transponieren auflösen: \(X^T + A^T = (B^{-1}+I)X^T\)</li>
        <li>Umformen: \(A^T = B^{-1}X^T\)</li>
        <li>Von links mit \(B\): \(BA^T = X^T\), also \(X = (BA^T)^T = AB^T\)</li>
      </ol>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Gegeben: \(A = \begin{pmatrix}2&1\\0&3\end{pmatrix}\), \(B = \begin{pmatrix}1&-1\\2&0\end{pmatrix}\), \(I = \begin{pmatrix}1&0\\0&1\end{pmatrix}\). Löse nach \(X\):</p>
      <ol style="margin-left:var(--space-5);color:var(--text-secondary);font-size:15px;">
        <li style="margin-bottom:var(--space-2)">\(X + A^T = \frac{1}{2}(B-I) + 2X\)</li>
        <li style="margin-bottom:var(--space-2)">\(AXB = I\)</li>
        <li>\(AX = BX + I\)</li>
      </ol>
    </div>
  </div>

  <!-- 3. Rang -->
  <div class="ch-section" id="s3">
    <h2>Rang einer Matrix</h2>
    <p>Der <strong>Rang</strong> einer Matrix ist eine der wichtigsten Kennzahlen in der linearen Algebra. Er entscheidet über die Lösbarkeit von Gleichungssystemen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Rang (Rg)</div>
      <p>Der Rang einer Matrix ist die <strong>maximale Anzahl linear unabhängiger Zeilen</strong> (= Spalten).</p>
      <p>Praktisch: <strong>Rang = Anzahl der Nicht-Nullzeilen in der Zeilenstufenform</strong></p>
      <p>Es gilt stets: \(\text{Zeilenrang} = \text{Spaltenrang}\)</p>
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Intuition</div>
      <p>Der Rang gibt an, in welche Dimension der Raum durch die Matrix transformiert wird: Rang 2 bedeutet, ein 3D-Körper wird auf eine Fläche projiziert; Rang 1 auf eine Linie.</p>
    </div>
  </div>

  <!-- 4. Zeilenstufenform -->
  <div class="ch-section" id="s4">
    <h2>Zeilenstufenform (ZSF)</h2>
    <p>Die <strong>Zeilenstufenform</strong> ist die Zielform der Gauß-Elimination. Aus ihr lässt sich der Rang direkt ablesen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Merkmale der ZSF</div>
      <ol style="margin-left:var(--space-5);color:var(--text-secondary);font-size:15px;">
        <li style="margin-bottom:var(--space-2)">Nullzeilen stehen <strong>ganz unten</strong>.</li>
        <li>Das erste Element ungleich null in einer Zeile (<strong>Pivot</strong>) steht immer <strong>rechts vom Pivot</strong> der Zeile darüber.</li>
      </ol>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Rang ablesen</div>
      <div class="math-block">
        \[A = \begin{pmatrix}2&3&5&1\\0&1&4&2\\0&0&0&3\\0&0&0&0\end{pmatrix} \quad \Rightarrow \quad \text{Rg}(A) = 3\]
      </div>
      <p>Drei Nicht-Nullzeilen → Rang 3. Die vierte Zeile (Nullzeile) trägt nichts bei.</p>
    </div>
  </div>

  <!-- 5. Gauß für Rang -->
  <div class="ch-section" id="s5">
    <h2>Gauß-Elimination für den Rang</h2>
    <p>Um den Rang einer beliebigen Matrix zu bestimmen, bringt man sie durch elementare Zeilenoperationen in die Zeilenstufenform und zählt dann die Nicht-Nullzeilen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Erlaubte Zeilenoperationen</div>
      <ul style="list-style:none;padding:0;">
        <li style="font-size:15px;color:var(--text-secondary);padding:4px 0;">↕ Zwei Zeilen <strong>vertauschen</strong></li>
        <li style="font-size:15px;color:var(--text-secondary);padding:4px 0;">× Zeile mit \(\lambda \neq 0\) <strong>multiplizieren</strong></li>
        <li style="font-size:15px;color:var(--text-secondary);padding:4px 0;">+ Vielfaches einer Zeile zu einer anderen <strong>addieren</strong></li>
      </ul>
      <p style="font-size:14px;color:var(--text-tertiary);margin-top:var(--space-3)">Diese Operationen ändern den Rang nicht!</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Rang bestimmen</div>
      <div class="math-block">
        \[\begin{pmatrix}1&2&3\\2&4&6\\0&1&1\end{pmatrix} \xrightarrow{R_2 \leftarrow R_2 - 2R_1} \begin{pmatrix}1&2&3\\0&0&0\\0&1&1\end{pmatrix} \xrightarrow{R_2 \leftrightarrow R_3} \begin{pmatrix}1&2&3\\0&1&1\\0&0&0\end{pmatrix}\]
      </div>
      <p>Zwei Nicht-Nullzeilen → \(\text{Rg}(A) = 2\).</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Bestimme den Rang durch Gauß-Elimination:</p>
      <div class="math-block">
        \[B = \begin{pmatrix}1&2&1\\3&6&3\\2&4&2\end{pmatrix}\]
      </div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(R_2 \leftarrow R_2 - 3R_1\), \(R_3 \leftarrow R_3 - 2R_1\): beide werden Nullzeilen. → \(\text{Rg}(B) = 1\).</p>
    </div>
  </div>

  <div class="ch-nav">
    <a href="/learn/determinanten/" class="ch-nav-prev">
      <div><div class="ch-nav-label">← Vorheriges</div><div class="ch-nav-title">Determinanten</div></div>
    </a>
    <a href="/learn/lgs-grundlagen/" class="ch-nav-next">
      <div><div class="ch-nav-label">Nächstes Kapitel</div><div class="ch-nav-title">LGS Grundlagen →</div></div>
    </a>
  </div>

</div>

<aside class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#s1">1. Matrizengleichungen</a></li>
    <li><a href="#s2">2. Fünf Beispieltypen</a></li>
    <li><a href="#s3">3. Rang einer Matrix</a></li>
    <li><a href="#s4">4. Zeilenstufenform</a></li>
    <li><a href="#s5">5. Gauß für den Rang</a></li>
  </ul>
</aside>
</div>

<script>
const sections=document.querySelectorAll('.ch-section');const tocLinks=document.querySelectorAll('.ch-toc a');
const observer=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){const id=e.target.id;tocLinks.forEach(l=>{l.classList.toggle('active',l.getAttribute('href')==='#'+id);});}});},{rootMargin:'-20% 0px -70% 0px'});
sections.forEach(s=>observer.observe(s));
</script>
