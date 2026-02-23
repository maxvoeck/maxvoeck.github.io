---
layout: page
title:
permalink: /learn/vektoren-grundlagen/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root{--geo:#007AFF;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;--system-purple:#AF52DE;--bg-primary:#000000;--bg-secondary:#1C1C1E;--bg-tertiary:#2C2C2E;--text-primary:#FFFFFF;--text-secondary:#EBEBF5;--text-tertiary:#8E8E93;--separator:rgba(255,255,255,0.10);--font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
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
.ch-nav a:hover{color:var(--text-primary);border-color:rgba(255,255,255,.3);background:var(--bg-secondary);}
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
    <span>Kapitel 1</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">📍 Analytische Geometrie · Kapitel 1 von 4</div>
    <h1>Vektoren – Grundlagen</h1>
    <div class="ch-header-meta">
      <span>⏱ ca. 35 min</span><span>·</span>
      <span>Koordinatensystem · Betrag · Skalarprodukt · Winkelberechnung</span>
    </div>
  </div>

  <div class="ch-section" id="sec-koordinaten">
    <h2>Das Koordinatensystem im R³</h2>
    <p>Der dreidimensionale Raum wird durch ein <strong>rechtshändiges xyz-Koordinatensystem</strong> beschrieben. Die drei Achsen stehen senkrecht aufeinander und erzeugen drei Koordinatenebenen.</p>
    <ul>
      <li><strong>xy-Ebene:</strong> alle Punkte mit \(z = 0\)</li>
      <li><strong>yz-Ebene:</strong> alle Punkte mit \(x = 0\)</li>
      <li><strong>xz-Ebene:</strong> alle Punkte mit \(y = 0\)</li>
    </ul>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Skalar vs. Vektor</div>
      <p><strong>Skalare Größen</strong> werden vollständig durch eine Zahl beschrieben (z.B. Temperatur 25°C, Masse 3 kg). <strong>Vektorielle Größen</strong> benötigen Betrag, Richtung und Richtungssinn (z.B. Geschwindigkeit, Kraft).</p>
      <p>Ein Vektor \(\vec{a}\) im \(\mathbb{R}^3\) wird als Spalte dargestellt:</p>
      \[ \vec{a} = \begin{pmatrix} a_x \\ a_y \\ a_z \end{pmatrix} \]
      <p>Der <strong>Nullvektor</strong> \(\vec{0} = \begin{pmatrix}0\\0\\0\end{pmatrix}\) ist der einzige Vektor ohne definierte Richtung.</p>
    </div>
  </div>

  <div class="ch-section" id="sec-betrag">
    <h2>Betrag und Einheitsvektor</h2>
    <p>Der <strong>Betrag</strong> eines Vektors gibt seine Länge an. Er berechnet sich über den Satz des Pythagoras im Raum:</p>

    <div class="cb cb-def">
      <div class="cb-label">Formeln</div>
      <p><strong>Betrag:</strong> \(\displaystyle|\vec{a}| = \sqrt{a_x^2 + a_y^2 + a_z^2}\)</p>
      <p><strong>Einheitsvektor</strong> (Länge 1, gleiche Richtung): \(\displaystyle\hat{a} = \frac{\vec{a}}{|\vec{a}|}\)</p>
      <p><strong>Gegenvektor:</strong> \(-\vec{a} = \begin{pmatrix}-a_x\\-a_y\\-a_z\end{pmatrix}\) — gleiche Länge, entgegengesetzte Richtung</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Betrag und Einheitsvektor berechnen</div>
      <p>Gegeben: \(\vec{a} = \begin{pmatrix}3\\-4\\0\end{pmatrix}\)</p>
      <p><strong>Schritt 1:</strong> \(|\vec{a}| = \sqrt{9 + 16 + 0} = \sqrt{25} = 5\)</p>
      <p><strong>Schritt 2:</strong> \(\hat{a} = \frac{1}{5}\begin{pmatrix}3\\-4\\0\end{pmatrix} = \begin{pmatrix}0{,}6\\-0{,}8\\0\end{pmatrix}\)</p>
      <p>Probe: \(|\hat{a}| = \sqrt{0{,}36 + 0{,}64} = 1\) ✓</p>
    </div>
  </div>

  <div class="ch-section" id="sec-rechnen">
    <h2>Rechnen mit Vektoren</h2>
    <p>Vektoren werden <strong>komponentenweise</strong> addiert, subtrahiert und mit Skalaren multipliziert.</p>

    <h3>Addition und Subtraktion</h3>
    \[ \vec{a} + \vec{b} = \begin{pmatrix}a_x + b_x \\ a_y + b_y \\ a_z + b_z\end{pmatrix}, \qquad \vec{a} - \vec{b} = \begin{pmatrix}a_x - b_x \\ a_y - b_y \\ a_z - b_z\end{pmatrix} \]
    <p>Der <strong>Verbindungsvektor</strong> von \(A\) nach \(B\) ist \(\overrightarrow{AB} = \vec{b} - \vec{a}\).</p>

    <h3>Skalarmultiplikation</h3>
    \[ k \cdot \vec{a} = \begin{pmatrix}k\,a_x \\ k\,a_y \\ k\,a_z\end{pmatrix} \]
    <p>Für \(k > 1\) wird der Vektor gestreckt, für \(0 < k < 1\) gestaucht, für \(k < 0\) zusätzlich umgekehrt. \(k\vec{a}\) ist immer <strong>parallel</strong> zu \(\vec{a}\).</p>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Gegeben: \(\vec{a} = \begin{pmatrix}5\\-2\\1\end{pmatrix}\), \(\vec{b} = \begin{pmatrix}-3\\4\\2\end{pmatrix}\)</p>
      <p>\(\vec{a} + \vec{b} = \begin{pmatrix}2\\2\\3\end{pmatrix}\), \quad \vec{a} - \vec{b} = \begin{pmatrix}8\\-6\\-1\end{pmatrix}\), \quad \(2\vec{a} = \begin{pmatrix}10\\-4\\2\end{pmatrix}\)</p>
    </div>
  </div>

  <div class="ch-section" id="sec-skalarprodukt">
    <h2>Skalarprodukt</h2>
    <p>Das Skalarprodukt multipliziert zwei Vektoren und liefert eine <strong>Zahl (Skalar)</strong> — kein Vektor.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <p>\[\vec{a} \cdot \vec{b} = a_x b_x + a_y b_y + a_z b_z\]</p>
      <p><strong>Geometrische Bedeutung:</strong> \(\vec{a} \cdot \vec{b} = |\vec{a}|\,|\vec{b}|\,\cos\varphi\)</p>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Interpretation</div>
      <p>\(\vec{a}\cdot\vec{b} > 0\) → spitzer Winkel (\(\varphi < 90°\))</p>
      <p>\(\vec{a}\cdot\vec{b} = 0\) → rechter Winkel — die Vektoren sind <strong>orthogonal</strong> (\(\vec{a} \perp \vec{b}\))</p>
      <p>\(\vec{a}\cdot\vec{b} < 0\) → stumpfer Winkel (\(\varphi > 90°\))</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Orthogonalität prüfen</div>
      <p>Gegeben: \(\vec{a} = \begin{pmatrix}2\\1\\0\end{pmatrix}\), \(\vec{b} = \begin{pmatrix}1\\-2\\0\end{pmatrix}\)</p>
      <p>\(\vec{a}\cdot\vec{b} = 2\cdot1 + 1\cdot(-2) + 0\cdot0 = 2 - 2 = 0\)</p>
      <p>Da das Skalarprodukt null ist: \(\vec{a} \perp \vec{b}\) ✓</p>
    </div>
  </div>

  <div class="ch-section" id="sec-winkel">
    <h2>Winkelberechnung</h2>
    <p>Mit dem Skalarprodukt lässt sich der Winkel zwischen zwei Vektoren berechnen:</p>

    <ol class="steps">
      <li>Skalarprodukt \(\vec{a}\cdot\vec{b}\) berechnen</li>
      <li>Beträge \(|\vec{a}|\) und \(|\vec{b}|\) bestimmen</li>
      <li>Kosinus berechnen: \(\cos\varphi = \dfrac{\vec{a}\cdot\vec{b}}{|\vec{a}|\,|\vec{b}|}\)</li>
      <li>Winkel bestimmen: \(\varphi = \arccos\!\left(\dfrac{\vec{a}\cdot\vec{b}}{|\vec{a}|\,|\vec{b}|}\right)\)</li>
    </ol>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Gegeben: \(\vec{a} = \begin{pmatrix}2\\0\\1\end{pmatrix}\), \(\vec{b} = \begin{pmatrix}1\\1\\1\end{pmatrix}\)</p>
      <p>\(\vec{a}\cdot\vec{b} = 2+0+1 = 3\), \quad |\vec{a}| = \sqrt{5}\), \quad |\vec{b}| = \sqrt{3}\)</p>
      \[\cos\varphi = \frac{3}{\sqrt{5}\cdot\sqrt{3}} = \frac{3}{\sqrt{15}} \approx 0{,}775 \quad\Rightarrow\quad \varphi \approx 39{,}2°\]
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe</div>
      <p>Berechne den Winkel zwischen \(\vec{u} = \begin{pmatrix}1\\2\\-1\end{pmatrix}\) und \(\vec{v} = \begin{pmatrix}3\\0\\2\end{pmatrix}\).</p>
      <p><em>Hinweis:</em> \(\vec{u}\cdot\vec{v} = 1\), \(|\vec{u}| = \sqrt{6}\), \(|\vec{v}| = \sqrt{13}\), \(\varphi = \arccos\!\left(\tfrac{1}{\sqrt{78}}\right) \approx 83{,}5°\)</p>
    </div>
  </div>

  <div class="ch-section" id="sec-ortsvektor">
    <h2>Orts- und Verbindungsvektor</h2>
    <p>Jedem Punkt im Raum kann ein <strong>Ortsvektor</strong> (vom Ursprung zum Punkt) zugeordnet werden.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definitionen</div>
      <p><strong>Ortsvektor</strong> von \(A(a_1, a_2, a_3)\): \(\quad\overrightarrow{OA} = \begin{pmatrix}a_1\\a_2\\a_3\end{pmatrix}\)</p>
      <p><strong>Verbindungsvektor</strong> von \(A\) nach \(B\): \(\quad\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA} = \vec{b} - \vec{a}\)</p>
      <p><strong>Mittelpunkt</strong> von \(AB\): \(\quad M = \dfrac{\vec{a} + \vec{b}}{2}\)</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Gegeben: \(A(1\,|\,2\,|\,-1)\) und \(B(4\,|\,0\,|\,3)\)</p>
      \[\overrightarrow{AB} = \begin{pmatrix}4-1\\0-2\\3-(-1)\end{pmatrix} = \begin{pmatrix}3\\-2\\4\end{pmatrix}, \quad |\overrightarrow{AB}| = \sqrt{9+4+16} = \sqrt{29} \approx 5{,}39\]
      <p>Mittelpunkt: \(M = \frac{1}{2}\begin{pmatrix}5\\2\\2\end{pmatrix} = \begin{pmatrix}2{,}5\\1\\1\end{pmatrix}\)</p>
    </div>
  </div>

  <div class="ch-nav">
    <span style="opacity:.3;font-size:14px;">← Erstes Kapitel</span>
    <a href="/learn/vektorprodukt-spatprodukt/" class="primary">Kapitel 2: Vektorprodukt & Spatprodukt →</a>
  </div>

</div>

<nav class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#sec-koordinaten">Koordinatensystem</a></li>
    <li><a href="#sec-betrag">Betrag & Einheitsvektor</a></li>
    <li><a href="#sec-rechnen">Rechnen mit Vektoren</a></li>
    <li><a href="#sec-skalarprodukt">Skalarprodukt</a></li>
    <li><a href="#sec-winkel">Winkelberechnung</a></li>
    <li><a href="#sec-ortsvektor">Orts- & Verbindungsvektor</a></li>
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
