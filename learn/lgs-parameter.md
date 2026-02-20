---
layout: page
title:
permalink: /learn/lgs-parameter/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root{--math:#FF2D55;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;--system-purple:#AF52DE;--bg-primary:#000000;--bg-secondary:#1C1C1E;--bg-tertiary:#2C2C2E;--text-primary:#FFFFFF;--text-secondary:#EBEBF5;--text-tertiary:#8E8E93;--separator:rgba(255,255,255,0.10);--font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.6;letter-spacing:-0.015em;}
html,body{overflow-x:hidden;max-width:100%;}
.ch-wrap{overflow-x:hidden;width:100%;box-sizing:border-box;}
.cb,.math-block,.steps,.ch-section{max-width:100%;box-sizing:border-box;word-break:break-word;}

.post-header,.page-heading,header.post-header{display:none!important;}
.ch-wrap{max-width:1100px;margin:0 auto;padding:var(--space-10) var(--space-5);display:grid;grid-template-columns:1fr 220px;gap:var(--space-12);align-items:start;}
.katex-display{overflow-x:auto!important;overflow-y:hidden;padding-bottom:4px;}
@media(max-width:860px){.ch-wrap{grid-template-columns:1fr;}.ch-toc{display:none;}}
.ch-breadcrumb{display:flex;align-items:center;gap:var(--space-2);font-size:13px;color:var(--text-tertiary);margin-bottom:var(--space-8);}
.ch-breadcrumb a{color:var(--text-tertiary);text-decoration:none;}.ch-breadcrumb a:hover{color:var(--text-primary);}.ch-breadcrumb-sep{opacity:0.4;}
.ch-header{margin-bottom:var(--space-10);padding-bottom:var(--space-8);border-bottom:1px solid var(--separator);}
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--math);background:rgba(255,45,85,.1);border:1px solid rgba(255,45,85,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-weight:700;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
.ch-header-meta{font-size:14px;color:var(--text-tertiary);display:flex;gap:var(--space-4);flex-wrap:wrap;}
.ch-section{margin-bottom:var(--space-12);}
.ch-section h2{font-size:22px;font-weight:700;letter-spacing:-.02em;color:var(--text-primary);margin-bottom:var(--space-5);display:flex;align-items:center;gap:var(--space-3);}
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
.case-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:var(--space-4);margin:var(--space-5) 0;}
.case-card{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-lg);padding:var(--space-5);}
.case-card-label{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;margin-bottom:var(--space-2);}
.case-card-cond{font-size:15px;font-weight:600;margin-bottom:var(--space-2);}
.case-card-desc{font-size:13px;color:var(--text-tertiary);line-height:1.5;}
.case-card--unique{border-top:2px solid var(--system-green);}.case-card--unique .case-card-label{color:var(--system-green);}
.case-card--inf{border-top:2px solid var(--system-orange);}.case-card--inf .case-card-label{color:var(--system-orange);}
.case-card--none{border-top:2px solid var(--math);}.case-card--none .case-card-label{color:var(--math);}
.param-table{width:100%;border-collapse:collapse;font-size:14px;margin:var(--space-4) 0;}
.param-table th{background:var(--bg-tertiary);color:var(--text-tertiary);font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.06em;padding:var(--space-3) var(--space-4);text-align:left;border-bottom:1px solid var(--separator);}
.param-table tr{background:transparent!important;}
.param-table td{padding:var(--space-3) var(--space-4);border-bottom:1px solid rgba(255,255,255,.05);color:var(--text-secondary);vertical-align:top;background:transparent!important;}
.param-table tr:last-child td{border-bottom:none;}
.tag-green{display:inline-block;font-size:11px;font-weight:600;background:rgba(52,199,89,.12);color:var(--system-green);border-radius:var(--radius-full);padding:2px 8px;}
.tag-orange{display:inline-block;font-size:11px;font-weight:600;background:rgba(255,149,0,.12);color:var(--system-orange);border-radius:var(--radius-full);padding:2px 8px;}
.tag-red{display:inline-block;font-size:11px;font-weight:600;background:rgba(255,45,85,.12);color:var(--math);border-radius:var(--radius-full);padding:2px 8px;}
.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--math);background:rgba(255,45,85,.1);}
.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav a{display:inline-flex;align-items:center;gap:var(--space-2);font-size:14px;font-weight:500;color:var(--text-tertiary);text-decoration:none;padding:var(--space-3) var(--space-4);border:1px solid var(--separator);border-radius:var(--radius-md);transition:all var(--transition-base);}
.ch-nav a:hover{color:var(--text-primary);border-color:rgba(255,255,255,.3);background:var(--bg-secondary);}
.ch-nav a.primary{color:var(--math);border-color:rgba(255,45,85,.3);background:rgba(255,45,85,.05);}
.ch-nav a.primary:hover{background:rgba(255,45,85,.1);}
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
</style>

<div class="ch-wrap">
<div id="chapter-content">

  <!-- Breadcrumb -->
  <div class="ch-breadcrumb">
    <a href="/learn/">Learn</a>
    <span class="ch-breadcrumb-sep">›</span>
    <a href="/learn/mathematik/">Mathematik</a>
    <span class="ch-breadcrumb-sep">›</span>
    <span>Kapitel 5</span>
  </div>

  <!-- Header -->
  <div class="ch-header">
    <div class="ch-eyebrow">📐 Lineare Algebra · Kapitel 5 von 5</div>
    <h1>LGS mit Parametern</h1>
    <div class="ch-header-meta">
      <span>⏱ ca. 30 min</span>
      <span>·</span>
      <span>Fallunterscheidung · Determinantentest · Gauß mit Parametern</span>
    </div>
  </div>

  <!-- Abschnitt 1 -->
  <div class="ch-section" id="sec-warum">
    <h2>Warum Parameter?</h2>
    <p>In der Praxis enthält ein LGS oft einen <strong>Parameter</strong> – meist \(t\) oder \(\lambda\) – der einen Wert annehmen kann. Je nach Wert des Parameters ändert sich die Lösungsstruktur des Systems komplett: Es kann eindeutig lösbar, mehrdeutig lösbar oder unlösbar sein.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">LGS mit Parameter</div>
      <p>Ein <em>LGS mit Parameter</em> ist ein lineares Gleichungssystem, dessen Koeffizientenmatrix \(A\) oder der Vektor \(b\) einen reellen Parameter enthält:</p>
      \[ A(t)\,\vec{x} = \vec{b}(t) \]
      <p>Gesucht sind alle Werte von \(t\), für die das System eindeutig lösbar, mehrdeutig lösbar oder unlösbar ist.</p>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Wichtig</div>
      <p>Bei einem LGS mit Parameter muss immer eine <strong>vollständige Fallunterscheidung</strong> gemacht werden. Jeder mögliche Wert des Parameters ist zu untersuchen.</p>
    </div>
  </div>

  <!-- Abschnitt 2 -->
  <div class="ch-section" id="sec-dettest">
    <h2>Der Determinantentest</h2>
    <p>Der schnellste Einstieg bei einem quadratischen LGS mit Parameter ist die Berechnung von \(\det(A(t))\). Das Vorzeichen der Determinante entscheidet direkt über die Lösbarkeit.</p>

    <div class="cb cb-def">
      <div class="cb-label">Satz</div>
      <div class="cb-title">Determinante und Lösbarkeit</div>
      <p>Sei \(A(t) \in \mathbb{R}^{n\times n}\) eine quadratische Koeffizientenmatrix. Dann gilt:</p>
      <ul style="margin-left:1.2em;margin-top:0.5em;">
        <li style="margin-bottom:6px;">\(\det(A(t)) \neq 0\) → System ist <strong>eindeutig lösbar</strong> (genau eine Lösung)</li>
        <li style="margin-bottom:6px;">\(\det(A(t)) = 0\) → System ist <strong>nicht eindeutig lösbar</strong> (keine oder unendlich viele Lösungen)</li>
      </ul>
      <p>Im Fall \(\det = 0\) muss man mit dem Gauß-Algorithmus oder dem Rang weiter unterscheiden.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Determinantentest für ein 2×2-System</div>
      <p>Gegeben:</p>
      \[ A(t) = \begin{pmatrix} t & 2 \\ 3 & t \end{pmatrix} \]
      <p>Berechnung der Determinante:</p>
      \[ \det(A) = t \cdot t - 2 \cdot 3 = t^2 - 6 \]
      <p>Nullstellen: \(t^2 - 6 = 0 \Rightarrow t = \pm\sqrt{6}\)</p>
      <p>Ergebnis:</p>
      <ul style="margin-left:1.2em;margin-top:0.4em;">
        <li>Für \(t \neq \pm\sqrt{6}\): eindeutig lösbar</li>
        <li>Für \(t = \pm\sqrt{6}\): \(\det = 0\), weiter untersuchen</li>
      </ul>
    </div>
  </div>

  <!-- Abschnitt 3 -->
  <div class="ch-section" id="sec-2x2">
    <h2>Fallunterscheidung beim 2×2-System</h2>
    <p>Bei einem \(2 \times 2\)-System ist die vollständige Fallunterscheidung überschaubar. Man berechnet zunächst \(\det(A(t))\), bestimmt die kritischen Parameterwerte und untersucht diese dann gesondert.</p>

    <div class="cb cb-ex">
      <div class="cb-label">Vollständiges Beispiel</div>
      <div class="cb-title">2×2-LGS mit Parameter \(t\)</div>
      <p>Gegeben:</p>
      \[ \begin{pmatrix} 1 & t \\ t & 4 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} 2 \\ 8 \end{pmatrix} \]

      <p><strong>Schritt 1: Determinante berechnen</strong></p>
      \[ \det(A) = 1 \cdot 4 - t \cdot t = 4 - t^2 = (2-t)(2+t) \]
      <p>Kritische Werte: \(t = 2\) und \(t = -2\).</p>

      <p><strong>Schritt 2: Fall \(\det \neq 0\), also \(t \neq \pm 2\)</strong></p>
      <p>Das System hat genau eine Lösung. Mit der Cramerschen Regel oder Gauß:</p>
      \[ x_1 = \frac{8 - 8t}{4 - t^2}, \quad x_2 = \frac{8 - 2t}{4 - t^2} \]

      <p><strong>Schritt 3: Fall \(t = 2\)</strong></p>
      \[ \left(\begin{array}{cc|c} 1 & 2 & 2 \\ 2 & 4 & 8 \end{array}\right) \xrightarrow{Z_2 - 2Z_1} \left(\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 0 & 4 \end{array}\right) \]
      <p>Widerspruch \(0 = 4\) → <strong>keine Lösung</strong>.</p>

      <p><strong>Schritt 4: Fall \(t = -2\)</strong></p>
      \[ \left(\begin{array}{cc|c} 1 & -2 & 2 \\ -2 & 4 & 8 \end{array}\right) \xrightarrow{Z_2 + 2Z_1} \left(\begin{array}{cc|c} 1 & -2 & 2 \\ 0 & 0 & 12 \end{array}\right) \]
      <p>Widerspruch \(0 = 12\) → <strong>keine Lösung</strong>.</p>
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Tipp</div>
      <p>Sobald \(\det(A) = 0\) gilt, muss man die erweiterte Koeffizientenmatrix \((A\,|\,\vec{b})\) mit dem Gauß-Algorithmus untersuchen. Der Rang entscheidet dann, ob keine oder unendlich viele Lösungen vorliegen.</p>
    </div>
  </div>

  <!-- Abschnitt 4 -->
  <div class="ch-section" id="sec-3x3">
    <h2>3×3-System mit Parameter</h2>
    <p>Bei einem \(3 \times 3\)-System wird die Fallunterscheidung aufwändiger, folgt aber demselben Schema. Der Determinantentest liefert die kritischen Parameterwerte, die dann einzeln per Gauß untersucht werden.</p>

    <ol class="steps">
      <li>Determinante \(\det(A(t))\) berechnen und auf Null setzen → kritische Werte \(t_1, t_2, \ldots\) bestimmen.</li>
      <li>Für jeden kritischen Wert: erweiterte Koeffizientenmatrix \((A(t_i)\,|\,\vec{b}(t_i))\) aufschreiben.</li>
      <li>Gauß-Algorithmus anwenden und Rang von \(A\) sowie Rang von \((A\,|\,\vec{b})\) vergleichen.</li>
      <li>Allgemeine Lösung für den Fall \(t \neq t_i\) angeben (mit Cramerscher Regel oder Gauß).</li>
    </ol>

    <h3>Lösungskriterium für \(n\times n\)-Systeme</h3>
    <div class="case-grid">
      <div class="case-card case-card--unique">
        <div class="case-card-label">Eindeutig lösbar</div>
        <div class="case-card-cond">\(\text{rg}(A) = \text{rg}(A|\vec{b}) = n\)</div>
        <div class="case-card-desc">Rang gleich Unbekanntenanzahl → genau eine Lösung</div>
      </div>
      <div class="case-card case-card--inf">
        <div class="case-card-label">Unendlich viele Lösungen</div>
        <div class="case-card-cond">\(\text{rg}(A) = \text{rg}(A|\vec{b}) < n\)</div>
        <div class="case-card-desc">Rang kleiner als \(n\) → \(n - \text{rg}(A)\) freie Parameter</div>
      </div>
      <div class="case-card case-card--none">
        <div class="case-card-label">Keine Lösung</div>
        <div class="case-card-cond">\(\text{rg}(A) < \text{rg}(A|\vec{b})\)</div>
        <div class="case-card-desc">Widerspruchszeile entsteht → System unlösbar</div>
      </div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Vollständiges Beispiel</div>
      <div class="cb-title">3×3-LGS mit Parameter \(t\)</div>
      <p>Gegeben:</p>
      \[ \left(\begin{array}{ccc|c} 1 & 0 & 1 & 2 \\ 0 & t & 2 & 4 \\ 1 & 2 & t & 6 \end{array}\right) \]

      <p><strong>Schritt 1: Determinante</strong></p>
      \[ \det(A) = \begin{vmatrix} 1 & 0 & 1 \\ 0 & t & 2 \\ 1 & 2 & t \end{vmatrix} \]
      <p>Entwicklung nach der ersten Zeile:</p>
      \[ = 1 \cdot (t^2 - 4) - 0 + 1 \cdot (0 - t) = t^2 - 4 - t = t^2 - t - 4 \]
      <p>Nullstellen: \(t = \frac{1 \pm \sqrt{17}}{2}\). Für alle anderen \(t\) ist das System eindeutig lösbar.</p>

      <p><strong>Schritt 2: Fall \(t = 0\) (Sonderuntersuchung)</strong></p>
      \[ \left(\begin{array}{ccc|c} 1 & 0 & 1 & 2 \\ 0 & 0 & 2 & 4 \\ 1 & 2 & 0 & 6 \end{array}\right) \xrightarrow{Z_3 - Z_1} \left(\begin{array}{ccc|c} 1 & 0 & 1 & 2 \\ 0 & 0 & 2 & 4 \\ 0 & 2 & -1 & 4 \end{array}\right) \]
      <p>\(\text{rg}(A) = \text{rg}(A|\vec{b}) = 3\) → eindeutig lösbar (obwohl \(\det\) hier nicht null ist – nur als Übung).</p>
    </div>
  </div>

  <!-- Abschnitt 5 -->
  <div class="ch-section" id="sec-cramer">
    <h2>Lösungsberechnung: Cramersche Regel</h2>
    <p>Wenn \(\det(A(t)) \neq 0\), kann man die Lösung des LGS direkt mit der <strong>Cramerschen Regel</strong> angeben – als rationale Funktion in \(t\).</p>

    <div class="cb cb-def">
      <div class="cb-label">Satz — Cramersche Regel</div>
      <p>Sei \(A\vec{x} = \vec{b}\) mit \(\det(A) \neq 0\). Dann gilt für jede Unbekannte \(x_i\):</p>
      \[ x_i = \frac{\det(A_i)}{\det(A)} \]
      <p>wobei \(A_i\) die Matrix ist, die durch Ersetzen der \(i\)-ten Spalte von \(A\) durch \(\vec{b}\) entsteht.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Cramersche Regel mit Parameter</div>
      <p>Gegeben: \(A(t) = \begin{pmatrix} t & 1 \\ 2 & 1 \end{pmatrix}\), \(\vec{b} = \begin{pmatrix} 3 \\ 4 \end{pmatrix}\)</p>
      \[ \det(A) = t - 2 \quad \Rightarrow \quad \text{kritisch: } t = 2 \]
      <p>Für \(t \neq 2\):</p>
      \[ x_1 = \frac{\det\begin{pmatrix}3&1\\4&1\end{pmatrix}}{t-2} = \frac{3-4}{t-2} = \frac{-1}{t-2} \]
      \[ x_2 = \frac{\det\begin{pmatrix}t&3\\2&4\end{pmatrix}}{t-2} = \frac{4t-6}{t-2} \]
      <p>Für \(t = 2\) ergibt Gauß eine Widerspruchszeile → keine Lösung.</p>
    </div>
  </div>

  <!-- Abschnitt 6 -->
  <div class="ch-section" id="sec-uebersicht">
    <h2>Übersicht: Vollständige Fallunterscheidung</h2>
    <p>Hier ist das bewährte Schema für die vollständige Lösung eines LGS mit einem Parameter zusammengefasst:</p>

    <table class="param-table">
      <thead>
        <tr>
          <th>Schritt</th>
          <th>Aktion</th>
          <th>Ergebnis</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><strong>1</strong></td>
          <td>Determinante \(\det(A(t))\) berechnen</td>
          <td>Polynom in \(t\)</td>
        </tr>
        <tr>
          <td><strong>2</strong></td>
          <td>\(\det(A(t)) = 0\) lösen</td>
          <td>Kritische Werte \(t_1, \ldots, t_k\)</td>
        </tr>
        <tr>
          <td><strong>3</strong></td>
          <td>Für \(t \neq t_i\): Cramer oder Gauß</td>
          <td><span class="tag-green">Eindeutige Lösung</span> in Abhängigkeit von \(t\)</td>
        </tr>
        <tr>
          <td><strong>4</strong></td>
          <td>Für jeden kritischen Wert \(t_i\): Gauß auf \((A|\vec{b})\)</td>
          <td>Rang vergleichen</td>
        </tr>
        <tr>
          <td><strong>5a</strong></td>
          <td>\(\text{rg}(A) = \text{rg}(A|\vec{b}) < n\)</td>
          <td><span class="tag-orange">∞ viele Lösungen</span></td>
        </tr>
        <tr>
          <td><strong>5b</strong></td>
          <td>\(\text{rg}(A) < \text{rg}(A|\vec{b})\)</td>
          <td><span class="tag-red">Keine Lösung</span></td>
        </tr>
      </tbody>
    </table>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe</div>
      <div class="cb-title">Zum Üben</div>
      <p>Untersuche das folgende LGS mit Parameter \(t \in \mathbb{R}\) vollständig:</p>
      \[ \left(\begin{array}{cc|c} t-1 & 2 & 3 \\ 3 & t+1 & 9 \end{array}\right) \]
      <p>Berechne \(\det(A)\), bestimme die kritischen Werte und führe für jeden Wert die Gauß-Untersuchung durch.</p>
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Lösungshinweis</div>
      <p>\(\det(A) = (t-1)(t+1) - 6 = t^2 - 7\). Kritische Werte: \(t = \pm\sqrt{7}\). Für \(t = \sqrt{7}\) → keine Lösung; für \(t = -\sqrt{7}\) ebenfalls untersuchen. Für alle anderen \(t\) gilt \(\det \neq 0\) → eindeutig lösbar.</p>
    </div>
  </div>

  <!-- Navigation -->
  <div class="ch-nav">
    <a href="/learn/lgs-grundlagen/">← Kapitel 4: LGS Grundlagen</a>
    <a href="/learn/mathematik/" class="primary">Zurück zur Übersicht ↑</a>
  </div>

</div>

<!-- TOC Sidebar -->
<nav class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#sec-warum">Warum Parameter?</a></li>
    <li><a href="#sec-dettest">Determinantentest</a></li>
    <li><a href="#sec-2x2">2×2-System</a></li>
    <li><a href="#sec-3x3">3×3-System</a></li>
    <li><a href="#sec-cramer">Cramersche Regel</a></li>
    <li><a href="#sec-uebersicht">Übersicht</a></li>
  </ul>
</nav>

</div>

<script>
(function(){
  const links = document.querySelectorAll('.ch-toc a');
  const sections = Array.from(document.querySelectorAll('.ch-section[id]'));
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{
      if(e.isIntersecting){
        links.forEach(l=>l.classList.remove('active'));
        const a = document.querySelector('.ch-toc a[href="#'+e.target.id+'"]');
        if(a) a.classList.add('active');
      }
    });
  },{rootMargin:'-20% 0px -70% 0px'});
  sections.forEach(s=>obs.observe(s));
})();
</script>
