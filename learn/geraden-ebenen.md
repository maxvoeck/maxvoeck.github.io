---
layout: page
title:
permalink: /learn/geraden-ebenen/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root {
  --math:#c45c3e;--geo:#c49a6c;--sumi:#1a1a18;--kuro:#2c2c28;--hai:#3d3d38;--kinari:#f0ece4;--shiro:#f7f5f0;--kinu:#e8e3d8;--ishi:#b8b3a8;--sugi:#8a8578;--beni:#c45c3e;--matcha:#7a8c6e;--ai:#5b7a8c;--kitsune:#c49a6c;--sakura:#c4868a;
  --bg-primary:#f7f5f0;--bg-secondary:#f0ece4;--bg-tertiary:#e8e3d8;
  --text-primary:#1a1a18;--text-secondary:#8a8578;--text-tertiary:#b8b3a8;
  --separator:rgba(26,26,24,0.08);
  --font-stack:'DM Sans','Noto Sans JP',-apple-system,BlinkMacSystemFont,sans-serif;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.6;letter-spacing:-0.015em;}
.post-header,.page-heading,header.post-header{display:none!important;}
.ch-wrap{width:100%;box-sizing:border-box;}
.cb,.math-block,.steps,.ch-section{max-width:100%;box-sizing:border-box;}
#chapter-content{min-width:0;overflow:hidden;}
.katex-display{overflow-x:auto!important;overflow-y:hidden;padding-bottom:4px;}
.ch-wrap{max-width:1100px;margin:0 auto;padding:var(--space-10) var(--space-5);display:grid;grid-template-columns:1fr 220px;gap:var(--space-12);align-items:start;}
@media(max-width:860px){.ch-wrap{grid-template-columns:1fr;}.ch-toc{display:none;}}
.ch-breadcrumb{display:flex;align-items:center;gap:var(--space-2);font-size:13px;color:var(--text-tertiary);margin-bottom:var(--space-8);}
.ch-breadcrumb a{color:var(--text-tertiary);text-decoration:none;}.ch-breadcrumb a:hover{color:var(--text-primary);}.ch-breadcrumb-sep{opacity:0.4;}
.ch-header{margin-bottom:var(--space-10);padding-bottom:var(--space-8);border-bottom:1px solid var(--separator);}
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--geo);background:rgba(91,122,140,.08);border:1px solid rgba(0,122,255,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-family:\'Cormorant Garamond\',\'Noto Serif JP\',Georgia,serif;font-weight:300;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
.ch-header-meta{font-size:14px;color:var(--text-tertiary);display:flex;gap:var(--space-4);flex-wrap:wrap;}
.ch-section{margin-bottom:var(--space-12);}
.ch-section h2{font-size:22px;font-weight:700;letter-spacing:-.02em;color:var(--text-primary);margin-bottom:var(--space-5);display:flex;align-items:center;gap:var(--space-3);}
.ch-section h2::before{content:'';display:block;width:3px;height:22px;background:var(--geo);border-radius:2px;flex-shrink:0;}
.ch-section h3{font-size:17px;font-weight:600;color:var(--text-secondary);margin:var(--space-6) 0 var(--space-3);}
.ch-section p{font-size:16px;color:var(--text-secondary);line-height:1.75;margin-bottom:var(--space-4);}
.ch-section ul{margin:0 0 var(--space-4) var(--space-5);}
.ch-section li{font-size:16px;color:var(--text-secondary);line-height:1.7;margin-bottom:var(--space-1);}
.cb{border-radius:var(--radius-lg);padding:var(--space-5) var(--space-6);margin:var(--space-6) 0;border-left:3px solid;}
.cb-label{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;margin-bottom:var(--space-3);}
.cb-title{font-size:16px;font-weight:600;margin-bottom:var(--space-2);}
.cb p{font-size:15px;line-height:1.7;margin-bottom:var(--space-3);}.cb p:last-child{margin-bottom:0;}
.cb-def{background:rgba(91,122,140,.08);border-color:var(--ai);}.cb-def .cb-label{color:var(--ai);}
.cb-ex{background:rgba(122,140,110,.08);border-color:var(--matcha);}.cb-ex .cb-label{color:var(--matcha);}
.cb-task{background:rgba(196,154,108,.08);border-color:var(--kitsune);}.cb-task .cb-label{color:var(--kitsune);}
.cb-note{background:rgba(91,122,140,.08);border-color:var(--geo);}.cb-note .cb-label{color:var(--geo);}
.cb-tip{background:rgba(196,134,138,.08);border-color:var(--sakura);}.cb-tip .cb-label{color:var(--sakura);}
.math-block{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-md);padding:var(--space-5) var(--space-6);margin:var(--space-4) 0;overflow-x:auto;text-align:center;font-size:1.05em;}
.steps{list-style:none;padding:0;margin:var(--space-3) 0;counter-reset:step;}
.steps li{counter-increment:step;display:flex;gap:var(--space-3);margin-bottom:var(--space-4);font-size:15px;color:var(--text-secondary);line-height:1.65;}
.steps li::before{content:counter(step);min-width:24px;height:24px;border-radius:50%;background:rgba(0,122,255,.15);color:var(--geo);font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}
.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--geo);background:rgba(91,122,140,.08);}
.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav a{display:inline-flex;align-items:center;gap:var(--space-2);font-size:14px;font-weight:500;color:var(--text-tertiary);text-decoration:none;padding:var(--space-3) var(--space-4);border:1px solid var(--separator);border-radius:var(--radius-md);transition:all var(--transition-base);}
.ch-nav a:hover{color:var(--text-primary);border-color:rgba(var(--text-rgb),0.15);background:var(--bg-secondary);}
.ch-nav a.primary{color:var(--geo);border-color:rgba(0,122,255,.3);background:rgba(0,122,255,.05);}
.ch-nav a.primary:hover{background:rgba(0,122,255,.12);}
@media(max-width:600px){
.ch-wrap{padding:var(--space-6) var(--space-4);}
.ch-header h1{font-family:'Cormorant Garamond','Noto Serif JP',Georgia,serif;font-weight:300;font-size:26px;}
.ch-section h2{font-size:18px;}
.ch-section p,.ch-section li,.cb p{font-size:15px;}
.math-block{padding:var(--space-4) var(--space-3);font-size:.88em;}
.cb{padding:var(--space-4);}
.ch-section,.math-block{max-width:100%;overflow-x:auto;-webkit-overflow-scrolling:touch;}
.ch-nav{flex-direction:column;gap:var(--space-3);}
.ch-nav a{width:100%;justify-content:center;text-align:center;}
}
@media(max-width:480px){
.ch-wrap{padding:var(--space-5) var(--space-3);}
.ch-breadcrumb{font-size:12px;flex-wrap:wrap;}
.ch-header h1{font-family:'Cormorant Garamond','Noto Serif JP',Georgia,serif;font-weight:300;font-size:22px;}
.ch-header-meta{font-size:12px;flex-direction:column;gap:4px;}
.ch-section h2{font-size:16px;}
.ch-section p,.ch-section li,.cb p{font-size:14px;}
.math-block{font-size:.82em;overflow-x:auto;}
.cb{padding:var(--space-3) var(--space-4);}
}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important;}}
</style>

<div class="ch-wrap">
<div id="chapter-content">

  <div class="ch-breadcrumb">
    <a href="/learn/">Learn</a><span class="ch-breadcrumb-sep">›</span>
    <a href="/learn/mathematik/">Mathematik</a><span class="ch-breadcrumb-sep">›</span>
    <span>Kapitel 3</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">Analytische Geometrie · Kapitel 3 von 4</div>
    <h1>Geraden und Ebenen</h1>
    <div class="ch-header-meta">
      <span>ca. 40 min</span><span>·</span>
      <span>Parameterform · Normalenvektor · Koordinatenform · Spurpunkte</span>
    </div>
  </div>

  <!-- Geradengleichung -->
  <div class="ch-section" id="sec-geraden">
    <h2>Geradengleichung im Raum</h2>
    <p>Eine <strong>Gerade</strong> im Raum wird durch einen <strong>Stützpunkt</strong> und einen <strong>Richtungsvektor</strong> festgelegt. Die Parameterdarstellung beschreibt jeden Punkt der Geraden als Funktion eines einzigen Parameters \(t\).</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Parameterform der Geraden</div>
      <p>Gegeben: Stützpunkt \(A\) (Ortsvektor \(\vec{a}\)) und Richtungsvektor \(\vec{u} \neq \vec{0}\):</p>
      \[ g\colon \vec{x} = \vec{a} + t\,\vec{u}, \quad t \in \mathbb{R} \]
      <p>Jeder Wert von \(t\) liefert genau einen Punkt auf \(g\). Für \(t=0\) erhält man den Stützpunkt \(A\).</p>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Merke</div>
      <p>Die Parameterform ist <strong>nicht eindeutig</strong>: jeder Punkt auf \(g\) kann als Stützpunkt dienen, und jedes Vielfaches \(k\vec{u}\) (\(k \neq 0\)) ist ein gültiger Richtungsvektor.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Gerade durch zwei Punkte</div>
      <p>Gegeben: \(A(1\,|\,2\,|\,3)\) und \(B(4\,|\,0\,|\,1)\)</p>
      <p>Richtungsvektor: \(\overrightarrow{AB} = \begin{pmatrix}3\\-2\\-2\end{pmatrix}\)</p>
      \[ g\colon \vec{x} = \begin{pmatrix}1\\2\\3\end{pmatrix} + t\begin{pmatrix}3\\-2\\-2\end{pmatrix}, \quad t \in \mathbb{R} \]
      <p>Probe: Für \(t=1\) ergibt sich \(\begin{pmatrix}4\\0\\1\end{pmatrix} = B\) ✓</p>
    </div>

    <h3>Punktprobe</h3>
    <p>Um zu prüfen, ob ein Punkt \(P\) auf einer Geraden liegt, setzt man \(\vec{p}\) in die Gleichung ein und löst nach \(t\). Liegt \(P\) auf \(g\), muss in <strong>allen drei Komponenten</strong> derselbe Wert für \(t\) herauskommen.</p>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Punktprobe</div>
      <p>Liegt \(P(7\,|\,-2\,|\,-1)\) auf obiger Gerade?</p>
      <p>\(7 = 1 + 3t \Rightarrow t = 2\), \quad \(-2 = 2 - 2t \Rightarrow t = 2\), \quad \(-1 = 3 - 2t \Rightarrow t = 2\)</p>
      <p>Alle Gleichungen liefern \(t = 2\) → \(P \in g\) ✓</p>
    </div>
  </div>

  <!-- Ebenengleichungen -->
  <div class="ch-section" id="sec-ebenen">
    <h2>Ebenengleichungen</h2>
    <p>Ebenen lassen sich auf verschiedene Arten darstellen. Die drei gängigsten Formen sind die <strong>Parameterform</strong>, die <strong>Normalenform</strong> und die <strong>Koordinatenform</strong>.</p>

    <h3>Parameterform</h3>
    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <p>Gegeben: Stützpunkt \(A\) und zwei <strong>linear unabhängige</strong> Richtungsvektoren \(\vec{u}\) und \(\vec{v}\):</p>
      \[ E\colon \vec{x} = \vec{a} + s\,\vec{u} + t\,\vec{v}, \quad s, t \in \mathbb{R} \]
      <p>Die Vektoren \(\vec{u}\) und \(\vec{v}\) heißen <strong>Spannvektoren</strong> der Ebene.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Ebene durch drei Punkte</div>
      <p>Gegeben: \(A(1\,|\,0\,|\,2)\), \(B(3\,|\,1\,|\,0)\), \(C(0\,|\,2\,|\,1)\)</p>
      <p>\(\overrightarrow{AB} = \begin{pmatrix}2\\1\\-2\end{pmatrix}\), \quad \(\overrightarrow{AC} = \begin{pmatrix}-1\\2\\-1\end{pmatrix}\)</p>
      \[ E\colon \vec{x} = \begin{pmatrix}1\\0\\2\end{pmatrix} + s\begin{pmatrix}2\\1\\-2\end{pmatrix} + t\begin{pmatrix}-1\\2\\-1\end{pmatrix} \]
    </div>

    <h3>Normalenform und Koordinatenform</h3>
    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Normalenvektor</div>
      <p>Der <strong>Normalenvektor</strong> \(\vec{n}\) steht senkrecht auf der Ebene und berechnet sich als Kreuzprodukt der Spannvektoren:</p>
      \[ \vec{n} = \vec{u} \times \vec{v} \]
      <p><strong>Normalenform:</strong> \(\vec{n} \cdot (\vec{x} - \vec{a}) = 0\)</p>
      <p><strong>Koordinatenform:</strong> \(n_1 x + n_2 y + n_3 z = d\) mit \(d = \vec{n} \cdot \vec{a}\)</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Umwandlung</div>
      <p>Aus dem vorigen Beispiel:</p>
      \[ \vec{n} = \begin{pmatrix}2\\1\\-2\end{pmatrix} \times \begin{pmatrix}-1\\2\\-1\end{pmatrix} = \begin{pmatrix}1\cdot(-1)-(-2)\cdot2 \\ (-2)\cdot(-1)-2\cdot(-1) \\ 2\cdot2-1\cdot(-1)\end{pmatrix} = \begin{pmatrix}3\\4\\5\end{pmatrix} \]
      <p>\(d = \vec{n} \cdot \vec{a} = 3\cdot1 + 4\cdot0 + 5\cdot2 = 13\)</p>
      <p><strong>Koordinatenform:</strong> \(3x + 4y + 5z = 13\)</p>
      <p>Probe mit \(B(3\,|\,1\,|\,0)\): \(3\cdot3 + 4\cdot1 + 5\cdot0 = 13\) ✓</p>
    </div>
  </div>

  <!-- Umwandlung -->
  <div class="ch-section" id="sec-umwandlung">
    <h2>Formumwandlung</h2>
    <p>Im Abitur muss man häufig zwischen den Darstellungsformen wechseln. Hier die wichtigsten Wege:</p>

    <h3>Parameterform → Koordinatenform</h3>
    <ol class="steps">
      <li>Normalenvektor berechnen: \(\vec{n} = \vec{u} \times \vec{v}\)</li>
      <li>\(d\) bestimmen durch Einsetzen des Stützpunktes: \(d = \vec{n} \cdot \vec{a}\)</li>
      <li>Koordinatenform aufschreiben: \(n_1 x + n_2 y + n_3 z = d\)</li>
    </ol>

    <h3>Koordinatenform → Parameterform</h3>
    <ol class="steps">
      <li>Zwei der drei Variablen als Parameter setzen, z.B. \(y = s\), \(z = t\)</li>
      <li>Dritte Variable (hier \(x\)) durch die Gleichung ausdrücken</li>
      <li>Vektor \(\vec{x}\) als Stützvektor + Vielfache der Parameter schreiben</li>
    </ol>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Koordinatenform → Parameterform</div>
      <p>Gegeben: \(2x + y - z = 6\)</p>
      <p>Setze \(y = s\), \(z = t\) → \(x = \frac{6 - s + t}{2} = 3 - \frac{s}{2} + \frac{t}{2}\)</p>
      \[ \vec{x} = \begin{pmatrix}3\\0\\0\end{pmatrix} + s\begin{pmatrix}-\frac{1}{2}\\1\\0\end{pmatrix} + t\begin{pmatrix}\frac{1}{2}\\0\\1\end{pmatrix} \]
    </div>
  </div>

  <!-- Spurpunkte und Spurgeraden -->
  <div class="ch-section" id="sec-spurpunkte">
    <h2>Spurpunkte und Spurgeraden</h2>
    <p>Die <strong>Spurpunkte</strong> einer Ebene sind die Schnittpunkte mit den Koordinatenachsen. Die <strong>Spurgeraden</strong> sind die Schnittgeraden mit den Koordinatenebenen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <p>Für die Ebene \(n_1 x + n_2 y + n_3 z = d\):</p>
      <p><strong>Spurpunkt \(S_x\)</strong> (auf der x-Achse): setze \(y = 0, z = 0\) → \(S_x\!\left(\frac{d}{n_1}\,\middle|\,0\,\middle|\,0\right)\)</p>
      <p><strong>Spurpunkt \(S_y\)</strong> (auf der y-Achse): setze \(x = 0, z = 0\) → \(S_y\!\left(0\,\middle|\,\frac{d}{n_2}\,\middle|\,0\right)\)</p>
      <p><strong>Spurpunkt \(S_z\)</strong> (auf der z-Achse): setze \(x = 0, y = 0\) → \(S_z\!\left(0\,\middle|\,0\,\middle|\,\frac{d}{n_3}\right)\)</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Gegeben: \(3x + 4y + 5z = 60\)</p>
      <p>\(S_x(20\,|\,0\,|\,0)\), \quad \(S_y(0\,|\,15\,|\,0)\), \quad \(S_z(0\,|\,0\,|\,12)\)</p>
      <p><strong>Spurgerade</strong> in der xy-Ebene (\(z = 0\)): \(3x + 4y = 60\), also \(y = 15 - \frac{3}{4}x\)</p>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Tipp</div>
      <p>Die <strong>Achsenabschnittsform</strong> \(\frac{x}{a} + \frac{y}{b} + \frac{z}{c} = 1\) lässt die Spurpunkte direkt ablesen: \(S_x(a\,|\,0\,|\,0)\), \(S_y(0\,|\,b\,|\,0)\), \(S_z(0\,|\,0\,|\,c)\).</p>
    </div>
  </div>

  <!-- Besondere Lagen -->
  <div class="ch-section" id="sec-besondere-lagen">
    <h2>Besondere Lagen von Ebenen</h2>
    <p>Manche Ebenen haben eine besonders einfache Gleichung, weil sie parallel zu Koordinatenachsen oder -ebenen verlaufen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Übersicht</div>
      <p><strong>Parallel zur xy-Ebene:</strong> \(z = c\) (Normalenvektor \(\vec{n} = \begin{pmatrix}0\\0\\1\end{pmatrix}\))</p>
      <p><strong>Parallel zur xz-Ebene:</strong> \(y = b\) (Normalenvektor \(\vec{n} = \begin{pmatrix}0\\1\\0\end{pmatrix}\))</p>
      <p><strong>Parallel zur yz-Ebene:</strong> \(x = a\) (Normalenvektor \(\vec{n} = \begin{pmatrix}1\\0\\0\end{pmatrix}\))</p>
      <p><strong>Durch den Ursprung:</strong> \(n_1 x + n_2 y + n_3 z = 0\) (Stützpunkt \(O\))</p>
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Merkhilfe</div>
      <p>Fehlt eine Variable in der Koordinatenform, verläuft die Ebene <strong>parallel zur Achse</strong> dieser Variable. Beispiel: In \(2x + 3y = 6\) fehlt \(z\), also ist die Ebene parallel zur z-Achse.</p>
    </div>
  </div>

  <!-- Lage Gerade-Ebene -->
  <div class="ch-section" id="sec-gerade-ebene">
    <h2>Lage einer Geraden zur Ebene</h2>
    <p>Um die Lage einer Geraden \(g\) zu einer Ebene \(E\) zu bestimmen, setzt man die Geradengleichung in die Koordinatenform der Ebene ein.</p>

    <ol class="steps">
      <li>Gerade \(g\colon \vec{x} = \vec{a} + t\,\vec{u}\) in Komponenten: \(x = a_1 + t\,u_1\) usw.</li>
      <li>Einsetzen in die Ebene \(n_1 x + n_2 y + n_3 z = d\)</li>
      <li>Nach \(t\) auflösen und Ergebnis interpretieren</li>
    </ol>

    <div class="cb cb-def">
      <div class="cb-label">Fallunterscheidung</div>
      <p><strong>Genau ein \(t\):</strong> Gerade schneidet Ebene → Schnittpunkt einsetzen</p>
      <p><strong>\(0 = 0\) (wahre Aussage):</strong> Gerade liegt in der Ebene (\(g \subset E\))</p>
      <p><strong>\(0 = c \neq 0\) (Widerspruch):</strong> Gerade ist parallel zur Ebene (\(g \parallel E\))</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Schnitt Gerade–Ebene</div>
      <p>Gerade: \(\vec{x} = \begin{pmatrix}1\\0\\2\end{pmatrix} + t\begin{pmatrix}2\\1\\-1\end{pmatrix}\), Ebene: \(x + 2y + z = 7\)</p>
      <p>Einsetzen: \((1+2t) + 2(t) + (2-t) = 7\)</p>
      <p>\(3 + 3t = 7 \Rightarrow t = \frac{4}{3}\)</p>
      <p>Schnittpunkt: \(S = \begin{pmatrix}1+\frac{8}{3}\\[2pt]\frac{4}{3}\\[2pt]2-\frac{4}{3}\end{pmatrix} = \begin{pmatrix}\frac{11}{3}\\[2pt]\frac{4}{3}\\[2pt]\frac{2}{3}\end{pmatrix}\)</p>
    </div>

    <h3>Schnittwinkel</h3>
    <p>Der Schnittwinkel \(\alpha\) zwischen einer Geraden (Richtung \(\vec{u}\)) und einer Ebene (Normale \(\vec{n}\)) ergibt sich aus:</p>
    \[ \sin\alpha = \frac{|\vec{u} \cdot \vec{n}|}{|\vec{u}|\,|\vec{n}|} \]

    <div class="cb cb-note">
      <div class="cb-label">Beachte</div>
      <p>Hier steht \(\sin\) statt \(\cos\), denn der Schnittwinkel wird zur Ebene (nicht zur Normalen) gemessen. Es gilt: \(\alpha + \beta = 90°\), wobei \(\beta\) der Winkel zwischen \(\vec{u}\) und \(\vec{n}\) ist.</p>
    </div>
  </div>

  <!-- Aufgaben -->
  <div class="ch-section" id="sec-aufgaben">
    <h2>Übungsaufgaben</h2>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 1</div>
      <p>Gegeben sind \(A(2\,|\,1\,|\,0)\), \(B(0\,|\,3\,|\,1)\), \(C(1\,|\,0\,|\,4)\). Bestimme die Koordinatenform der Ebene durch \(A\), \(B\), \(C\).</p>
      <p><em>Hinweis:</em> Spannvektoren \(\overrightarrow{AB}\) und \(\overrightarrow{AC}\) bilden, Kreuzprodukt berechnen, \(d\) durch Einsetzen.</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 2</div>
      <p>Bestimme die Lage der Geraden \(g\colon \vec{x} = \begin{pmatrix}1\\2\\3\end{pmatrix} + t\begin{pmatrix}1\\-1\\2\end{pmatrix}\) zur Ebene \(E\colon 2x + y - z = 3\).</p>
      <p><em>Hinweis:</em> Einsetzen ergibt \(2(1+t) + (2-t) - (3+2t) = 3\), also \(1 - t = 3\), also \(t = -2\). Schnittpunkt berechnen.</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 3</div>
      <p>Bestimme die Spurpunkte der Ebene \(4x + 2y + 8z = 16\) und gib die Achsenabschnittsform an.</p>
      <p><em>Hinweis:</em> \(S_x(4\,|\,0\,|\,0)\), \(S_y(0\,|\,8\,|\,0)\), \(S_z(0\,|\,0\,|\,2)\). Achsenabschnittsform: \(\frac{x}{4} + \frac{y}{8} + \frac{z}{2} = 1\).</p>
    </div>
  </div>

  <div class="ch-nav">
    <a href="/learn/vektorprodukt-spatprodukt/">← Kapitel 2: Vektorprodukt & Spatprodukt</a>
    <a href="/learn/lagebeziehungen-abstaende/" class="primary">Kapitel 4: Lagebeziehungen & Abstände →</a>
  </div>

</div>

<nav class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#sec-geraden">Geradengleichung</a></li>
    <li><a href="#sec-ebenen">Ebenengleichungen</a></li>
    <li><a href="#sec-umwandlung">Formumwandlung</a></li>
    <li><a href="#sec-spurpunkte">Spurpunkte & Spurgeraden</a></li>
    <li><a href="#sec-besondere-lagen">Besondere Lagen</a></li>
    <li><a href="#sec-gerade-ebene">Gerade & Ebene</a></li>
    <li><a href="#sec-aufgaben">Aufgaben</a></li>
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
