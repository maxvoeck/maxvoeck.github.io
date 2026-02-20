---
layout: page
title:
permalink: /learn/lgs-grundlagen/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.getElementById('chapter-content'),{delimiters:[{left:'\\(',right:'\\)',display:false},{left:'\\[',right:'\\]',display:true}]})"></script>

<style>
:root{--math:#FF2D55;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;--system-purple:#AF52DE;--bg-primary:#000000;--bg-secondary:#1C1C1E;--bg-tertiary:#2C2C2E;--text-primary:#FFFFFF;--text-secondary:#EBEBF5;--text-tertiary:#8E8E93;--separator:rgba(255,255,255,0.10);--font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-font-smoothing:antialiased;}
body,html,.page-content,.wrapper,main,.post-content{background:var(--bg-primary)!important;color:var(--text-primary);font-family:var(--font-stack);line-height:1.6;letter-spacing:-0.015em;}
.post-header,.page-heading,header.post-header{display:none!important;}
.ch-wrap{max-width:1100px;margin:0 auto;padding:var(--space-10) var(--space-5);display:grid;grid-template-columns:1fr 220px;gap:var(--space-12);align-items:start;}
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
.losbar-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:var(--space-3);margin:var(--space-5) 0;}
@media(max-width:600px){.losbar-grid{grid-template-columns:1fr;}}
.losbar-card{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-lg);padding:var(--space-5);}
.losbar-card-icon{font-size:24px;margin-bottom:var(--space-2);}
.losbar-card-title{font-size:14px;font-weight:700;margin-bottom:var(--space-2);}
.losbar-card-crit{font-size:12px;font-family:monospace;background:var(--bg-tertiary);border-radius:var(--radius-sm);padding:3px 6px;margin-bottom:var(--space-2);display:inline-block;}
.losbar-card-desc{font-size:13px;color:var(--text-tertiary);line-height:1.5;}
.losbar-card--unique{border-top:2px solid var(--system-green);}.losbar-card--unique .losbar-card-title{color:var(--system-green);}
.losbar-card--inf{border-top:2px solid var(--system-orange);}.losbar-card--inf .losbar-card-title{color:var(--system-orange);}
.losbar-card--none{border-top:2px solid var(--math);}.losbar-card--none .losbar-card-title{color:var(--math);}
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
    <span>Kapitel 4</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">📐 Kapitel 4</div>
    <h1>Lineare Gleichungssysteme</h1>
    <div class="ch-header-meta">
      <span>📄 Basiert auf LGS_2_1-5</span>
      <span>⏱ ca. 30 Min</span>
      <span>🎯 Lineare Algebra</span>
    </div>
  </div>

  <!-- 1. Was ist ein LGS? -->
  <div class="ch-section" id="s1">
    <h2>Was ist ein LGS?</h2>
    <p>Ein <strong>lineares Gleichungssystem (LGS)</strong> besteht aus mehreren linearen Gleichungen mit gemeinsamen Unbekannten. Ziel ist es, alle Werte der Unbekannten zu finden, die alle Gleichungen gleichzeitig erfüllen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Lineares Gleichungssystem</div>
      <p>\(m\) lineare Gleichungen mit \(n\) Unbekannten \(x_1, \ldots, x_n\):</p>
      <div class="math-block">
        \[\begin{aligned} a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= b_1 \\ a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= b_2 \\ &\vdots \\ a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= b_m \end{aligned}\]
      </div>
      <p><strong>Begriffe:</strong> \(a_{ij}\) = Koeffizienten, \(x_j\) = Unbekannte, \(b_i\) = Störvektor</p>
    </div>

    <h3>Matrixschreibweise</h3>
    <p>Jedes LGS lässt sich kompakt als Matrizengleichung schreiben:</p>
    <div class="math-block">\[A\mathbf{x} = \mathbf{b} \qquad \text{mit} \quad A \in \mathbb{R}^{m\times n},\ \mathbf{x} \in \mathbb{R}^n,\ \mathbf{b} \in \mathbb{R}^m\]</div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">LGS in Matrixform</div>
      <p>Das System \(\begin{cases}2x+3y=7\\x-y=1\end{cases}\) wird zu:</p>
      <div class="math-block">
        \[\underbrace{\begin{pmatrix}2&3\\1&-1\end{pmatrix}}_{A} \underbrace{\begin{pmatrix}x\\y\end{pmatrix}}_{\mathbf{x}} = \underbrace{\begin{pmatrix}7\\1\end{pmatrix}}_{\mathbf{b}}\]
      </div>
    </div>

    <h3>Erweiterte Koeffizientenmatrix</h3>
    <p>Für die Gauß-Elimination arbeitet man mit der <strong>erweiterten Matrix</strong> \([A|\mathbf{b}]\), die den Störvektor als zusätzliche Spalte enthält:</p>
    <div class="math-block">
      \[[A|\mathbf{b}] = \left(\begin{array}{cc|c}2&3&7\\1&-1&1\end{array}\right)\]
    </div>

    <div class="cb cb-tip">
      <div class="cb-label">Tipp</div>
      <p><strong>Homogen:</strong> \(A\mathbf{x} = \mathbf{0}\) — hat immer die triviale Lösung \(\mathbf{x} = \mathbf{0}\).<br>
      <strong>Inhomogen:</strong> \(A\mathbf{x} = \mathbf{b}\) mit \(\mathbf{b} \neq \mathbf{0}\) — kann null, eine oder unendlich viele Lösungen haben.</p>
    </div>
  </div>

  <!-- 2. Lösung mit inverser Matrix -->
  <div class="ch-section" id="s2">
    <h2>Lösung mit inverser Matrix</h2>
    <p>Falls \(A\) quadratisch und invertierbar ist, kann man die Lösung direkt berechnen.</p>

    <div class="cb cb-def">
      <div class="cb-label">Methode</div>
      <div class="cb-title">Inverse Matrix</div>
      <p><strong>Voraussetzungen:</strong> \(A\) muss quadratisch (\(n \times n\)) und regulär (\(\det(A) \neq 0\)) sein.</p>
      <div class="math-block">\[\mathbf{x} = A^{-1}\mathbf{b}\]</div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <p>Für \(\begin{pmatrix}2&3\\1&-1\end{pmatrix}\mathbf{x} = \begin{pmatrix}7\\1\end{pmatrix}\):</p>
      <p>\(\det(A) = 2\cdot(-1) - 3\cdot1 = -5 \neq 0\) ✓</p>
      <div class="math-block">
        \[A^{-1} = \frac{1}{-5}\begin{pmatrix}-1&-3\\-1&2\end{pmatrix} \qquad \Rightarrow \qquad \mathbf{x} = A^{-1}\mathbf{b} = \begin{pmatrix}2\\1\end{pmatrix}\]
      </div>
      <p>Also: \(x = 2\), \(y = 1\).</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Löse mit der inversen Matrix. Überprüfe zuerst, ob \(\det(A) \neq 0\):</p>
      <div class="math-block">\[\begin{cases}3x+y=7\\2x+y=5\end{cases}\]</div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ \(\det(A)=1\neq0\). \(A^{-1}=\begin{pmatrix}1&-1\\-2&3\end{pmatrix}\). \(\mathbf{x}=\begin{pmatrix}2\\1\end{pmatrix}\).</p>
    </div>
  </div>

  <!-- 3. Gauß-Algorithmus -->
  <div class="ch-section" id="s3">
    <h2>Der Gauß-Algorithmus</h2>
    <p>Der <strong>Gauß-Algorithmus</strong> ist die universelle Methode zum Lösen von LGS — er funktioniert für jede Größe und liefert immer die richtige Antwort.</p>

    <div class="cb cb-def">
      <div class="cb-label">Grundidee</div>
      <p>Man bringt die erweiterte Matrix \([A|\mathbf{b}]\) durch elementare Zeilenoperationen in die <strong>Zeilenstufenform</strong> und löst dann durch <strong>Rückwärtseinsetzen</strong>.</p>
    </div>

    <ol class="steps">
      <li><strong>Erweiterte Matrix</strong> \([A|\mathbf{b}]\) aufschreiben.</li>
      <li><strong>Zeilenoperationen</strong> anwenden: Pivotelement wählen, Spalte unterhalb auf null bringen.</li>
      <li><strong>Zeilenstufenform</strong> erreichen — Nicht-Nullzeilen zählen ergibt den Rang.</li>
      <li><strong>Rückwärtseinsetzen</strong>: von der letzten Gleichung nach oben auflösen.</li>
    </ol>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">3×3-System, eindeutig lösbar</div>
      <div class="math-block">
        \[\left(\begin{array}{ccc|c}1&1&1&6\\2&1&-1&3\\1&-1&1&2\end{array}\right) \xrightarrow{\text{Gauß}} \left(\begin{array}{ccc|c}1&1&1&6\\0&-1&-3&-9\\0&0&4&8\end{array}\right)\]
      </div>
      <p>Rückwärtseinsetzen: \(4z = 8 \Rightarrow z = 2\), dann \(-y - 6 = -9 \Rightarrow y = 3\), dann \(x = 6-3-2=1\).</p>
      <p>\(\text{Rg}(A) = \text{Rg}([A|\mathbf{b}]) = 3 = n\) → <strong>genau eine Lösung</strong>: \((x,y,z)=(1,3,2)\).</p>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Übung</div>
      <p>Löse mit dem Gauß-Algorithmus:</p>
      <div class="math-block">
        \[\begin{cases}x+2y-z=1\\2x-y+3z=9\\3x+y+2z=10\end{cases}\]
      </div>
      <p style="color:var(--text-tertiary);font-size:14px;margin-top:var(--space-3)">→ Lösung: \((x,y,z) = (1,1,2)\).</p>
    </div>
  </div>

  <!-- 4. Lösbarkeit -->
  <div class="ch-section" id="s4">
    <h2>Wann ist ein LGS lösbar?</h2>
    <p>Das <strong>Rang-Kriterium</strong> entscheidet über die Lösbarkeit — es ist das wichtigste Werkzeug in der Klausur.</p>

    <div class="losbar-grid">
      <div class="losbar-card losbar-card--unique">
        <div class="losbar-card-icon">✅</div>
        <div class="losbar-card-title">Eindeutig lösbar</div>
        <div class="losbar-card-crit">Rg(A) = Rg([A|b]) = n</div>
        <div class="losbar-card-desc">Genau eine Lösung. Anzahl der Gleichungen = Anzahl der Unbekannten.</div>
      </div>
      <div class="losbar-card losbar-card--inf">
        <div class="losbar-card-icon">∞</div>
        <div class="losbar-card-title">Unendlich viele</div>
        <div class="losbar-card-crit">Rg(A) = Rg([A|b]) &lt; n</div>
        <div class="losbar-card-desc">Freie Parameter: \(k = n - \text{Rg}(A)\). Lösungsmenge ist eine Gerade, Ebene, ...</div>
      </div>
      <div class="losbar-card losbar-card--none">
        <div class="losbar-card-icon">❌</div>
        <div class="losbar-card-title">Nicht lösbar</div>
        <div class="losbar-card-crit">Rg(A) &lt; Rg([A|b])</div>
        <div class="losbar-card-desc">Widerspruchszeile: eine Zeile der Form \(0 = c\) mit \(c \neq 0\).</div>
      </div>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Nicht lösbar — Widerspruch</div>
      <div class="math-block">
        \[\left(\begin{array}{cc|c}1&1&2\\2&2&5\end{array}\right) \xrightarrow{R_2 \leftarrow R_2-2R_1} \left(\begin{array}{cc|c}1&1&2\\0&0&1\end{array}\right)\]
      </div>
      <p>Die zweite Zeile liest sich: \(0 = 1\) — ein Widerspruch. \(\text{Rg}(A) = 1 < \text{Rg}([A|\mathbf{b}]) = 2\) → <strong>keine Lösung</strong>.</p>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Unendlich viele Lösungen</div>
      <div class="math-block">
        \[\left(\begin{array}{cc|c}1&1&2\\2&2&4\end{array}\right) \xrightarrow{R_2 \leftarrow R_2-2R_1} \left(\begin{array}{cc|c}1&1&2\\0&0&0\end{array}\right)\]
      </div>
      <p>\(\text{Rg}(A) = \text{Rg}([A|\mathbf{b}]) = 1 < 2 = n\) → 1 freier Parameter. Lösung: \(x = 2-y,\ y \in \mathbb{R}\).</p>
    </div>

    <div class="cb cb-note">
      <div class="cb-label">Klausurrelevant</div>
      <p>Die drei Fälle immer zuerst mit dem Rang-Kriterium prüfen! Ein Widerspruch (\(0 = c \neq 0\)) bedeutet sofort: keine Lösung — kein weiteres Rechnen nötig.</p>
    </div>
  </div>

  <div class="ch-nav">
    <a href="/learn/matrizengleichungen-rang/" class="ch-nav-prev">
      <div><div class="ch-nav-label">← Vorheriges</div><div class="ch-nav-title">Matrizengleichungen & Rang</div></div>
    </a>
    <a href="/learn/lgs-parameter/" class="ch-nav-next">
      <div><div class="ch-nav-label">Nächstes Kapitel</div><div class="ch-nav-title">LGS mit Parametern →</div></div>
    </a>
  </div>

</div>

<aside class="ch-toc">
  <div class="ch-toc-title">Inhalt</div>
  <ul>
    <li><a href="#s1">1. Was ist ein LGS?</a></li>
    <li><a href="#s2">2. Lösung mit Inverser</a></li>
    <li><a href="#s3">3. Gauß-Algorithmus</a></li>
    <li><a href="#s4">4. Lösbarkeit & Rang</a></li>
  </ul>
</aside>
</div>

<script>
const sections=document.querySelectorAll('.ch-section');const tocLinks=document.querySelectorAll('.ch-toc a');
const observer=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){const id=e.target.id;tocLinks.forEach(l=>{l.classList.toggle('active',l.getAttribute('href')==='#'+id);});}});},{rootMargin:'-20% 0px -70% 0px'});
sections.forEach(s=>observer.observe(s));
</script>
