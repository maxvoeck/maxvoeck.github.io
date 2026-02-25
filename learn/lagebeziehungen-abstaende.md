---
layout: page
title:
permalink: /learn/lagebeziehungen-abstaende/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root{--geo:#007AFF;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;--system-purple:#AF52DE;--bg-primary:#262624;--bg-secondary:#30302e;--bg-tertiary:#3a3a37;--text-primary:#c1c0b6;--text-secondary:#908f87;--text-tertiary:#706f69;--separator:rgba(var(--text-rgb),0.08);--font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
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
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--geo);background:rgba(0,122,255,.1);border:1px solid rgba(0,122,255,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-weight:700;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
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
.cb-def{background:rgba(88,86,214,.1);border-color:var(--system-indigo);}.cb-def .cb-label{color:var(--system-indigo);}
.cb-ex{background:rgba(52,199,89,.08);border-color:var(--system-green);}.cb-ex .cb-label{color:var(--system-green);}
.cb-task{background:rgba(255,149,0,.08);border-color:var(--system-orange);}.cb-task .cb-label{color:var(--system-orange);}
.cb-note{background:rgba(0,122,255,.08);border-color:var(--geo);}.cb-note .cb-label{color:var(--geo);}
.cb-tip{background:rgba(175,82,222,.08);border-color:var(--system-purple);}.cb-tip .cb-label{color:var(--system-purple);}
.math-block{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-md);padding:var(--space-5) var(--space-6);margin:var(--space-4) 0;overflow-x:auto;text-align:center;font-size:1.05em;}
.steps{list-style:none;padding:0;margin:var(--space-3) 0;counter-reset:step;}
.steps li{counter-increment:step;display:flex;gap:var(--space-3);margin-bottom:var(--space-4);font-size:15px;color:var(--text-secondary);line-height:1.65;}
.steps li::before{content:counter(step);min-width:24px;height:24px;border-radius:50%;background:rgba(0,122,255,.15);color:var(--geo);font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}
.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--geo);background:rgba(0,122,255,.1);}
.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav a{display:inline-flex;align-items:center;gap:var(--space-2);font-size:14px;font-weight:500;color:var(--text-tertiary);text-decoration:none;padding:var(--space-3) var(--space-4);border:1px solid var(--separator);border-radius:var(--radius-md);transition:all var(--transition-base);}
.ch-nav a:hover{color:var(--text-primary);border-color:rgba(var(--text-rgb),0.15);background:var(--bg-secondary);}
.ch-nav a.primary{color:var(--geo);border-color:rgba(0,122,255,.3);background:rgba(0,122,255,.05);}
.ch-nav a.primary:hover{background:rgba(0,122,255,.12);}
@media(max-width:600px){
.ch-wrap{padding:var(--space-6) var(--space-4);}
.ch-header h1{font-size:26px;}
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
.ch-header h1{font-size:22px;}
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
    <span>Kapitel 4</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">📍 Analytische Geometrie · Kapitel 4 von 4</div>
    <h1>Lagebeziehungen & Abstände</h1>
    <div class="ch-header-meta">
      <span>⏱ ca. 45 min</span><span>·</span>
      <span>Ebene↔Ebene · Gerade↔Gerade · Hesse-Formel · Abstandsberechnungen</span>
    </div>
  </div>

  <!-- Lage zweier Ebenen -->
  <div class="ch-section" id="sec-ebene-ebene">
    <h2>Lage zweier Ebenen</h2>
    <p>Zwei Ebenen \(E_1\) und \(E_2\) können zueinander <strong>identisch</strong>, <strong>parallel</strong> oder sich in einer <strong>Schnittgeraden</strong> schneiden.</p>

    <div class="cb cb-def">
      <div class="cb-label">Vorgehen</div>
      <div class="cb-title">Normalenvektoren vergleichen</div>
      <p>Gegeben: \(E_1\colon n_1 x + n_2 y + n_3 z = d_1\) und \(E_2\colon m_1 x + m_2 y + m_3 z = d_2\)</p>
      <p><strong>Fall 1:</strong> \(\vec{n}_1\) und \(\vec{n}_2\) sind <strong>nicht parallel</strong> → die Ebenen schneiden sich in einer Geraden</p>
      <p><strong>Fall 2:</strong> \(\vec{n}_1 = k\,\vec{n}_2\) und \(d_1 = k\,d_2\) → Ebenen sind <strong>identisch</strong></p>
      <p><strong>Fall 3:</strong> \(\vec{n}_1 = k\,\vec{n}_2\) aber \(d_1 \neq k\,d_2\) → Ebenen sind <strong>echt parallel</strong></p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Schnittgerade</div>
      <p>\(E_1\colon x + 2y + z = 5\) und \(E_2\colon 2x - y + 3z = 4\)</p>
      <p>\(\vec{n}_1 = \begin{pmatrix}1\\2\\1\end{pmatrix}\), \(\vec{n}_2 = \begin{pmatrix}2\\-1\\3\end{pmatrix}\) — nicht parallel, also Schnitt.</p>
      <p>Setze \(z = t\): aus \(E_1\) und \(E_2\) entsteht ein 2×2-LGS in \(x, y\).</p>
      <p>Aus \(E_1\): \(x = 5 - 2y - t\). Einsetzen in \(E_2\): \(2(5-2y-t) - y + 3t = 4\)</p>
      <p>\(10 - 4y - 2t - y + 3t = 4 \Rightarrow -5y + t = -6 \Rightarrow y = \frac{t+6}{5}\)</p>
      <p>\(x = 5 - \frac{2(t+6)}{5} - t = \frac{13 - 7t}{5}\)</p>
      \[ g\colon \vec{x} = \begin{pmatrix}\frac{13}{5}\\[2pt]\frac{6}{5}\\[2pt]0\end{pmatrix} + t\begin{pmatrix}-\frac{7}{5}\\[2pt]\frac{1}{5}\\[2pt]1\end{pmatrix} \]
    </div>

    <h3>Schnittwinkel zweier Ebenen</h3>
    <p>Der Winkel \(\varphi\) zwischen zwei Ebenen entspricht dem Winkel zwischen ihren Normalenvektoren:</p>
    \[ \cos\varphi = \frac{|\vec{n}_1 \cdot \vec{n}_2|}{|\vec{n}_1|\,|\vec{n}_2|} \]

    <div class="cb cb-note">
      <div class="cb-label">Merke</div>
      <p>Der Betrag im Zähler stellt sicher, dass stets der <strong>spitze</strong> Schnittwinkel berechnet wird (\(0° \leq \varphi \leq 90°\)).</p>
    </div>
  </div>

  <!-- Lage zweier Geraden -->
  <div class="ch-section" id="sec-gerade-gerade">
    <h2>Lage zweier Geraden</h2>
    <p>Zwei Geraden \(g\) und \(h\) im Raum können vier verschiedene Lagebeziehungen haben.</p>

    <div class="cb cb-def">
      <div class="cb-label">Systematik</div>
      <p><strong>Schritt 1 — Richtungsvektoren vergleichen:</strong></p>
      <p>Sind \(\vec{u}\) und \(\vec{v}\) parallel (\(\vec{u} = k\vec{v}\))?</p>
      <p>→ Ja: Punktprobe → <strong>identisch</strong> oder <strong>echt parallel</strong></p>
      <p>→ Nein: Gleichungssystem aufstellen</p>
      <p><strong>Schritt 2 — LGS lösen</strong> (wenn nicht parallel):</p>
      <p>Setze \(\vec{a} + s\vec{u} = \vec{b} + t\vec{v}\). Das ergibt 3 Gleichungen in 2 Unbekannten.</p>
      <p>→ Lösung existiert und ist konsistent: <strong>Schnittpunkt</strong></p>
      <p>→ Keine konsistente Lösung: <strong>windschief</strong></p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Windschief</div>
      <p>\(g\colon \vec{x} = \begin{pmatrix}1\\0\\2\end{pmatrix} + s\begin{pmatrix}1\\1\\0\end{pmatrix}\), \quad \(h\colon \vec{x} = \begin{pmatrix}0\\1\\0\end{pmatrix} + t\begin{pmatrix}0\\1\\1\end{pmatrix}\)</p>
      <p>Richtungsvektoren nicht parallel (kein \(k\) mit \(\begin{pmatrix}1\\1\\0\end{pmatrix} = k\begin{pmatrix}0\\1\\1\end{pmatrix}\)).</p>
      <p>LGS: \(1+s = 0\), \(s = 1+t\), \(2 = t\)</p>
      <p>Aus (1): \(s = -1\). Aus (3): \(t = 2\). Probe in (2): \(-1 = 1+2 = 3\) ✗</p>
      <p>Widerspruch → \(g\) und \(h\) sind <strong>windschief</strong>.</p>
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Entscheidungsbaum</div>
      <p>\(\vec{u} \parallel \vec{v}\)? → Ja: Punkt von \(g\) in \(h\) einsetzen → identisch oder parallel</p>
      <p>\(\vec{u} \parallel \vec{v}\)? → Nein: LGS aufstellen → lösbar: Schnitt, nicht lösbar: windschief</p>
    </div>
  </div>

  <!-- Hesse'sche Normalenform -->
  <div class="ch-section" id="sec-hesse">
    <h2>Hesse'sche Normalenform</h2>
    <p>Die <strong>Hesse'sche Normalenform (HNF)</strong> ist das zentrale Werkzeug für Abstandsberechnungen. Sie normiert die Ebenengleichung so, dass man den Abstand eines beliebigen Punktes direkt ablesen kann.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">HNF</div>
      <p>Aus der Koordinatenform \(n_1 x + n_2 y + n_3 z = d\) erhält man die HNF durch Division durch \(|\vec{n}|\):</p>
      \[ \frac{n_1 x + n_2 y + n_3 z - d}{|\vec{n}|} = 0 \]
      <p>Der <strong>Abstand</strong> eines Punktes \(P(p_1, p_2, p_3)\) zur Ebene ist dann:</p>
      \[ d(P, E) = \frac{|n_1\,p_1 + n_2\,p_2 + n_3\,p_3 - d|}{|\vec{n}|} \]
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Abstand Punkt–Ebene</div>
      <p>Ebene: \(2x + y - 2z = 10\), Punkt: \(P(3\,|\,1\,|\,-1)\)</p>
      <p>\(|\vec{n}| = \sqrt{4 + 1 + 4} = 3\)</p>
      \[ d(P, E) = \frac{|2\cdot3 + 1\cdot1 - 2\cdot(-1) - 10|}{3} = \frac{|6 + 1 + 2 - 10|}{3} = \frac{|-1|}{3} = \frac{1}{3} \]
    </div>
  </div>

  <!-- Abstandsberechnungen -->
  <div class="ch-section" id="sec-abstaende">
    <h2>Abstandsberechnungen</h2>
    <p>Die HNF bildet die Grundlage für alle Abstandsfälle im Raum. Hier eine Übersicht aller Fälle:</p>

    <h3>Abstand Punkt–Ebene</h3>
    <p>Direkt mit der HNF (siehe oben):</p>
    \[ d(P, E) = \frac{|n_1\,p_1 + n_2\,p_2 + n_3\,p_3 - d|}{\sqrt{n_1^2 + n_2^2 + n_3^2}} \]

    <h3>Abstand Punkt–Gerade</h3>
    <div class="cb cb-def">
      <div class="cb-label">Formel</div>
      <p>Gegeben: Gerade \(g\colon \vec{x} = \vec{a} + t\,\vec{u}\) und Punkt \(P\). Der Abstand berechnet sich über das Kreuzprodukt:</p>
      \[ d(P, g) = \frac{|\overrightarrow{AP} \times \vec{u}|}{|\vec{u}|} \]
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Gerade: \(\vec{x} = \begin{pmatrix}1\\0\\0\end{pmatrix} + t\begin{pmatrix}0\\1\\0\end{pmatrix}\), Punkt: \(P(3\,|\,2\,|\,4)\)</p>
      <p>\(\overrightarrow{AP} = \begin{pmatrix}2\\2\\4\end{pmatrix}\), \quad \(\overrightarrow{AP} \times \vec{u} = \begin{pmatrix}2\\2\\4\end{pmatrix} \times \begin{pmatrix}0\\1\\0\end{pmatrix} = \begin{pmatrix}-4\\0\\2\end{pmatrix}\)</p>
      <p>\(d = \frac{\sqrt{16 + 0 + 4}}{1} = \sqrt{20} = 2\sqrt{5} \approx 4{,}47\)</p>
    </div>

    <h3>Abstand paralleler Ebenen</h3>
    <p>Für parallele Ebenen \(E_1\) und \(E_2\): wähle einen beliebigen Punkt auf \(E_1\) und berechne seinen Abstand zu \(E_2\) mit der HNF.</p>

    <h3>Abstand paralleler Geraden</h3>
    <p>Für parallele Geraden \(g \parallel h\): wähle einen Punkt auf \(g\) und berechne seinen Abstand zu \(h\) mit der Kreuzprodukt-Formel.</p>

    <h3>Abstand windschiefer Geraden</h3>
    <div class="cb cb-def">
      <div class="cb-label">Formel</div>
      <p>Gegeben: \(g\colon \vec{x} = \vec{a} + s\,\vec{u}\) und \(h\colon \vec{x} = \vec{b} + t\,\vec{v}\) windschief. Dann:</p>
      \[ d(g, h) = \frac{|\overrightarrow{AB} \cdot (\vec{u} \times \vec{v})|}{|\vec{u} \times \vec{v}|} \]
      <p>wobei \(\overrightarrow{AB} = \vec{b} - \vec{a}\).</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Windschiefer Abstand</div>
      <p>\(g\colon \vec{x} = \begin{pmatrix}1\\0\\2\end{pmatrix} + s\begin{pmatrix}1\\1\\0\end{pmatrix}\), \quad \(h\colon \vec{x} = \begin{pmatrix}0\\1\\0\end{pmatrix} + t\begin{pmatrix}0\\1\\1\end{pmatrix}\)</p>
      <p>\(\overrightarrow{AB} = \begin{pmatrix}-1\\1\\-2\end{pmatrix}\), \quad \(\vec{u}\times\vec{v} = \begin{pmatrix}1\\1\\0\end{pmatrix}\times\begin{pmatrix}0\\1\\1\end{pmatrix} = \begin{pmatrix}1\\-1\\1\end{pmatrix}\)</p>
      <p>\(|\vec{u}\times\vec{v}| = \sqrt{1+1+1} = \sqrt{3}\)</p>
      <p>\(\overrightarrow{AB}\cdot(\vec{u}\times\vec{v}) = -1\cdot1 + 1\cdot(-1) + (-2)\cdot1 = -4\)</p>
      \[ d(g,h) = \frac{|-4|}{\sqrt{3}} = \frac{4}{\sqrt{3}} = \frac{4\sqrt{3}}{3} \approx 2{,}31 \]
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Interpretation</div>
      <p>Im Zähler steht ein <strong>Spatprodukt</strong>. Der Abstand windschiefer Geraden entspricht der Höhe des Spats, den die drei Vektoren \(\overrightarrow{AB}\), \(\vec{u}\), \(\vec{v}\) aufspannen.</p>
    </div>
  </div>

  <!-- Zusammenfassung -->
  <div class="ch-section" id="sec-zusammenfassung">
    <h2>Zusammenfassung aller Abstandsfälle</h2>

    <div class="cb cb-tip">
      <div class="cb-label">Übersicht</div>
      <p><strong>Punkt ↔ Ebene:</strong> HNF anwenden</p>
      <p><strong>Punkt ↔ Gerade:</strong> Kreuzprodukt-Formel \(\frac{|\overrightarrow{AP}\times\vec{u}|}{|\vec{u}|}\)</p>
      <p><strong>Parallele Ebenen:</strong> Punkt auf \(E_1\) wählen → Abstand zu \(E_2\) mit HNF</p>
      <p><strong>Parallele Geraden:</strong> Punkt auf \(g\) wählen → Abstand zu \(h\) mit Kreuzprodukt-Formel</p>
      <p><strong>Gerade ∥ Ebene:</strong> Punkt auf \(g\) wählen → Abstand zu \(E\) mit HNF</p>
      <p><strong>Windschiefe Geraden:</strong> Spatprodukt-Formel \(\frac{|\overrightarrow{AB}\cdot(\vec{u}\times\vec{v})|}{|\vec{u}\times\vec{v}|}\)</p>
    </div>
  </div>

  <!-- Aufgaben -->
  <div class="ch-section" id="sec-aufgaben">
    <h2>Übungsaufgaben</h2>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 1</div>
      <p>Bestimme die Lage der Ebenen \(E_1\colon 2x - y + 3z = 6\) und \(E_2\colon 4x - 2y + 6z = 8\). Falls parallel: berechne den Abstand.</p>
      <p><em>Hinweis:</em> \(\vec{n}_2 = 2\vec{n}_1\), aber \(8 \neq 2 \cdot 6 = 12\). Echt parallel. Abstand: wähle \(P(3\,|\,0\,|\,0) \in E_1\), dann \(d = \frac{|12-0+0-8|}{\sqrt{16+4+36}} = \frac{4}{\sqrt{56}} = \frac{4}{2\sqrt{14}} = \frac{2}{\sqrt{14}} \approx 0{,}53\).</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 2</div>
      <p>Berechne den Abstand des Punktes \(P(2\,|\,-1\,|\,3)\) von der Geraden \(g\colon \vec{x} = \begin{pmatrix}0\\0\\1\end{pmatrix} + t\begin{pmatrix}1\\2\\2\end{pmatrix}\).</p>
      <p><em>Hinweis:</em> \(\overrightarrow{AP} = \begin{pmatrix}2\\-1\\2\end{pmatrix}\), Kreuzprodukt mit \(\vec{u}\) berechnen, dann Betrag durch \(|\vec{u}|=3\) teilen.</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 3</div>
      <p>Untersuche die Lage der Geraden \(g\colon \vec{x} = \begin{pmatrix}1\\2\\3\end{pmatrix} + s\begin{pmatrix}2\\-1\\1\end{pmatrix}\) und \(h\colon \vec{x} = \begin{pmatrix}3\\1\\4\end{pmatrix} + t\begin{pmatrix}4\\-2\\2\end{pmatrix}\). Falls parallel oder identisch: begründe. Falls windschief: berechne den Abstand.</p>
      <p><em>Hinweis:</em> \(\vec{v} = 2\vec{u}\) → parallel. Punkt \(A(1\,|\,2\,|\,3)\) in \(h\) einsetzen: \(\begin{pmatrix}1\\2\\3\end{pmatrix} = \begin{pmatrix}3+4t\\1-2t\\4+2t\end{pmatrix}\). Aus Gl. 1: \(t = -\frac{1}{2}\) → Gl. 2: \(2 = 2\) ✓, Gl. 3: \(3 = 3\) ✓ → identisch.</p>
    </div>
  </div>

  <div class="ch-nav">
    <a href="/learn/geraden-ebenen/">← Kapitel 3: Geraden und Ebenen</a>
    <a href="/learn/mathematik/" class="primary">Zurück zur Übersicht →</a>
  </div>

</div>

<nav class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#sec-ebene-ebene">Ebene ↔ Ebene</a></li>
    <li><a href="#sec-gerade-gerade">Gerade ↔ Gerade</a></li>
    <li><a href="#sec-hesse">Hesse'sche Normalenform</a></li>
    <li><a href="#sec-abstaende">Abstandsberechnungen</a></li>
    <li><a href="#sec-zusammenfassung">Zusammenfassung</a></li>
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
