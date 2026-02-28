---
layout: page
title:
permalink: /learn/vektorprodukt-spatprodukt/
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
.vol-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:var(--space-3);margin:var(--space-5) 0;}
.vol-card{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-lg);padding:var(--space-4);text-align:center;}
.vol-card-icon{font-size:22px;margin-bottom:var(--space-2);}
.vol-card-name{font-size:12px;font-weight:700;color:var(--text-tertiary);margin-bottom:var(--space-1);}
.vol-card-formula{font-size:13px;color:var(--text-secondary);}
.sum-table{width:100%;border-collapse:collapse;font-size:14px;margin:var(--space-4) 0;}
.sum-table th{background:var(--bg-tertiary);color:var(--text-tertiary);font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.06em;padding:var(--space-3) var(--space-4);text-align:left;border-bottom:1px solid var(--separator);}
.sum-table tr{background:transparent!important;}
.sum-table td{padding:var(--space-3) var(--space-4);border-bottom:1px solid rgba(var(--text-rgb),0.06);color:var(--text-secondary);background:transparent!important;}
.sum-table tr:last-child td{border-bottom:none;}
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
.sum-table{display:block;overflow-x:auto;}
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
.vol-grid{grid-template-columns:repeat(2,1fr);}
}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01ms!important;transition-duration:.01ms!important;}}
</style>

<div class="ch-wrap">
<div id="chapter-content">

  <div class="ch-breadcrumb">
    <a href="/learn/">Learn</a><span class="ch-breadcrumb-sep">›</span>
    <a href="/learn/mathematik/">Mathematik</a><span class="ch-breadcrumb-sep">›</span>
    <span>Kapitel 2</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">Analytische Geometrie · Kapitel 2 von 4</div>
    <h1>Vektorprodukt & Spatprodukt</h1>
    <div class="ch-header-meta">
      <span>ca. 30 min</span><span>·</span>
      <span>Kreuzprodukt · Flächen · Volumen · Geometrische Nachweise</span>
    </div>
  </div>

  <div class="ch-section" id="sec-vektorprodukt">
    <h2>Das Vektorprodukt (Kreuzprodukt)</h2>
    <p>Das Vektorprodukt zweier Vektoren liefert — anders als das Skalarprodukt — einen <strong>neuen Vektor</strong>, der senkrecht auf beiden Ausgangsvektoren steht.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Vektorprodukt \(\vec{a} \times \vec{b}\)</div>
      <p>Für \(\vec{a} = \begin{pmatrix}a_1\\a_2\\a_3\end{pmatrix}\) und \(\vec{b} = \begin{pmatrix}b_1\\b_2\\b_3\end{pmatrix}\) gilt:</p>
      \[\vec{a} \times \vec{b} = \begin{pmatrix}a_2 b_3 - a_3 b_2 \\ a_3 b_1 - a_1 b_3 \\ a_1 b_2 - a_2 b_1\end{pmatrix}\]
      <p><strong>Anti-Kommutativität:</strong> \(\vec{a} \times \vec{b} = -(\vec{b} \times \vec{a})\) — Reihenfolge dreht das Vorzeichen um!</p>
      <p><strong>Geometrisch:</strong> \(\vec{a} \times \vec{b}\) steht senkrecht auf \(\vec{a}\) und auf \(\vec{b}\).</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Vektorprodukt berechnen</div>
      <p>Gegeben: \(\vec{a} = \begin{pmatrix}2\\1\\-3\end{pmatrix}\), \(\vec{b} = \begin{pmatrix}1\\4\\2\end{pmatrix}\)</p>
      \[\vec{a}\times\vec{b} = \begin{pmatrix}1\cdot2-(-3)\cdot4 \\ (-3)\cdot1-2\cdot2 \\ 2\cdot4-1\cdot1\end{pmatrix} = \begin{pmatrix}2+12 \\ -3-4 \\ 8-1\end{pmatrix} = \begin{pmatrix}14\\-7\\7\end{pmatrix}\]
    </div>
  </div>

  <div class="ch-section" id="sec-flaechen">
    <h2>Parallelität & Flächenberechnung</h2>

    <h3>Parallelitätskriterium</h3>
    <p>Zwei Vektoren sind genau dann <strong>parallel</strong>, wenn ihr Vektorprodukt der Nullvektor ist:</p>
    \[\vec{a} \times \vec{b} = \vec{0} \quad\Longleftrightarrow\quad \vec{a} \parallel \vec{b}\]

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Parallelität prüfen</div>
      <p>Sind \(\vec{a} = \begin{pmatrix}2\\-1\\4\end{pmatrix}\) und \(\vec{b} = \begin{pmatrix}-6\\3\\-12\end{pmatrix}\) parallel?</p>
      <p>\(\vec{a}\times\vec{b} = \begin{pmatrix}(-1)(-12)-4\cdot3 \\ 4\cdot(-6)-2\cdot(-12) \\ 2\cdot3-(-1)(-6)\end{pmatrix} = \begin{pmatrix}12-12\\-24+24\\6-6\end{pmatrix} = \vec{0}\) ✓ parallel</p>
      <p>(Probe: \(\vec{b} = -3\vec{a}\))</p>
    </div>

    <h3>Flächenformeln</h3>
    <div class="cb cb-def">
      <div class="cb-label">Formeln</div>
      <p><strong>Parallelogramm</strong> mit Seiten \(\vec{a}\), \(\vec{b}\): \(\quad A = |\vec{a}\times\vec{b}|\)</p>
      <p><strong>Dreieck</strong> mit Seiten \(\vec{a}\), \(\vec{b}\): \(\quad A = \dfrac{1}{2}|\vec{a}\times\vec{b}|\)</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Dreiecksfläche</div>
      <p>Dreieck mit \(A(0,0,0)\), \(B(3,0,0)\), \(C(1,2,0)\): \(\overrightarrow{AB}=\begin{pmatrix}3\\0\\0\end{pmatrix}\), \(\overrightarrow{AC}=\begin{pmatrix}1\\2\\0\end{pmatrix}\)</p>
      <p>\(\overrightarrow{AB}\times\overrightarrow{AC} = \begin{pmatrix}0\\0\\6\end{pmatrix}\), \quad |\overrightarrow{AB}\times\overrightarrow{AC}| = 6\)</p>
      <p>Dreiecksfläche: \(A = \frac{1}{2}\cdot 6 = 3\) FE</p>
    </div>
  </div>

  <div class="ch-section" id="sec-spatprodukt">
    <h2>Das Spatprodukt</h2>
    <p>Das Spatprodukt kombiniert Vektor- und Skalarprodukt und liefert das <strong>Volumen</strong> des von drei Vektoren aufgespannten Spats (schiefer Quader).</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <p>\[[\vec{a},\vec{b},\vec{c}] = \vec{a}\cdot(\vec{b}\times\vec{c}) = \det\begin{pmatrix}a_1&a_2&a_3\\b_1&b_2&b_3\\c_1&c_2&c_3\end{pmatrix}\]</p>
      <p><strong>Komplanarität:</strong> \([\vec{a},\vec{b},\vec{c}] = 0\) genau dann, wenn die drei Vektoren in einer Ebene liegen.</p>
    </div>

    <p>Das Spatprodukt liefert das Volumen verschiedener Körper:</p>
    <div class="vol-grid">
      <div class="vol-card"><div class="vol-card-icon"></div><div class="vol-card-name">Spat</div><div class="vol-card-formula">\(V = |[a,b,c]|\)</div></div>
      <div class="vol-card"><div class="vol-card-icon"></div><div class="vol-card-name">Prisma</div><div class="vol-card-formula">\(V = \tfrac{1}{2}|[a,b,c]|\)</div></div>
      <div class="vol-card"><div class="vol-card-icon"></div><div class="vol-card-name">Pyramide</div><div class="vol-card-formula">\(V = \tfrac{1}{3}|[a,b,c]|\)</div></div>
      <div class="vol-card"><div class="vol-card-icon"></div><div class="vol-card-name">Tetraeder</div><div class="vol-card-formula">\(V = \tfrac{1}{6}|[a,b,c]|\)</div></div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Spatvolumen</div>
      <p>Gegeben: \(\vec{a}=\begin{pmatrix}1\\2\\3\end{pmatrix}\), \(\vec{b}=\begin{pmatrix}2\\0\\1\end{pmatrix}\), \(\vec{c}=\begin{pmatrix}1\\1\\0\end{pmatrix}\)</p>
      <p>Schritt 1: \(\vec{b}\times\vec{c} = \begin{pmatrix}0\cdot0-1\cdot1\\1\cdot1-2\cdot0\\2\cdot1-0\cdot1\end{pmatrix} = \begin{pmatrix}-1\\1\\2\end{pmatrix}\)</p>
      <p>Schritt 2: \([\vec{a},\vec{b},\vec{c}] = \vec{a}\cdot\begin{pmatrix}-1\\1\\2\end{pmatrix} = -1+2+6 = 7\)</p>
      <p>Volumen des Spats: \(V = 7\) VE; Tetraeder: \(V = \frac{7}{6} \approx 1{,}17\) VE</p>
    </div>
  </div>

  <div class="ch-section" id="sec-nachweise">
    <h2>Geometrische Nachweise</h2>
    <p>Mit Verbindungs- und Skalarprodukt lassen sich geometrische Eigenschaften von Vierecken und Dreiecken exakt beweisen.</p>

    <h3>Vierecke nachweisen</h3>
    <ul>
      <li><strong>Parallelogramm:</strong> \(\overrightarrow{AB} = \overrightarrow{DC}\) und \(\overrightarrow{AD} = \overrightarrow{BC}\)</li>
      <li><strong>Rhombus:</strong> Parallelogramm + alle Seiten gleich lang</li>
      <li><strong>Rechteck:</strong> Parallelogramm + ein rechter Winkel (\(\overrightarrow{AB}\cdot\overrightarrow{AD}=0\))</li>
      <li><strong>Quadrat:</strong> Rechteck + Rhombus</li>
    </ul>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel — Parallelogramm</div>
      <p>Gegeben: \(A(1,2,0)\), \(B(4,3,1)\), \(C(5,6,2)\), \(D(2,5,1)\)</p>
      <p>\(\overrightarrow{AB} = \begin{pmatrix}3\\1\\1\end{pmatrix} = \overrightarrow{DC}\) ✓ und \(\overrightarrow{AD} = \begin{pmatrix}1\\3\\1\end{pmatrix} = \overrightarrow{BC}\) ✓ → Parallelogramm</p>
      <p>Rechteck-Test: \(\overrightarrow{AB}\cdot\overrightarrow{AD} = 3+3+1 = 7 \neq 0\) → <em>kein</em> Rechteck</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe</div>
      <p>Berechne das Volumen des Tetraeders \(ABCD\) mit \(A(0,0,0)\), \(B(3,0,0)\), \(C(0,4,0)\), \(D(0,0,5)\).</p>
      <p><em>Hinweis:</em> \(\overrightarrow{AB}=\begin{pmatrix}3\\0\\0\end{pmatrix}\), \(\overrightarrow{AC}=\begin{pmatrix}0\\4\\0\end{pmatrix}\), \(\overrightarrow{AD}=\begin{pmatrix}0\\0\\5\end{pmatrix}\). \(\det = 60\), \(V = \frac{60}{6} = 10\) VE.</p>
    </div>
  </div>

  <div class="ch-nav">
    <a href="/learn/vektoren-grundlagen/">← Kapitel 1: Vektoren Grundlagen</a>
    <a href="/learn/geraden-ebenen/" class="primary">Kapitel 3: Geraden und Ebenen →</a>
  </div>

</div>

<nav class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#sec-vektorprodukt">Vektorprodukt</a></li>
    <li><a href="#sec-flaechen">Parallelität & Flächen</a></li>
    <li><a href="#sec-spatprodukt">Spatprodukt</a></li>
    <li><a href="#sec-nachweise">Geometrische Nachweise</a></li>
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
