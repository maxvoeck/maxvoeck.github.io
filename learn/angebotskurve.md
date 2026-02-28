---
layout: page
title:
permalink: /learn/angebotskurve/
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js" onload="renderMathInElement(document.body,{delimiters:[{left:'$$',right:'$$',display:true},{left:'$',right:'$',display:false}]});"></script>

<style>
:root{--econ:#FF9500;--system-indigo:#5856D6;--system-green:#34C759;--system-orange:#FF9500;--system-blue:#007AFF;--system-purple:#AF52DE;--bg-primary:#262624;--bg-secondary:#30302e;--bg-tertiary:#3a3a37;--text-primary:#c1c0b6;--text-secondary:#908f87;--text-tertiary:#706f69;--separator:rgba(var(--text-rgb),0.08);--font-stack:-apple-system,BlinkMacSystemFont,"SF Pro Display","SF Pro Text","Helvetica Neue",Helvetica,Arial,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
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
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--econ);background:rgba(255,149,0,.1);border:1px solid rgba(255,149,0,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-weight:700;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
.ch-header-meta{font-size:14px;color:var(--text-tertiary);display:flex;gap:var(--space-4);flex-wrap:wrap;}
.ch-section{margin-bottom:var(--space-12);}
.ch-section h2{font-size:22px;font-weight:700;letter-spacing:-.02em;color:var(--text-primary);margin-bottom:var(--space-5);display:flex;align-items:center;gap:var(--space-3);}
.ch-section h2::before{content:'';display:block;width:3px;height:22px;background:var(--econ);border-radius:2px;flex-shrink:0;}
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
.cb-note{background:rgba(255,149,0,.08);border-color:var(--econ);}.cb-note .cb-label{color:var(--econ);}
.cb-tip{background:rgba(175,82,222,.08);border-color:var(--system-purple);}.cb-tip .cb-label{color:var(--system-purple);}
.math-block{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-md);padding:var(--space-5) var(--space-6);margin:var(--space-4) 0;overflow-x:auto;text-align:center;font-size:1.05em;}
.steps{list-style:none;padding:0;margin:var(--space-3) 0;counter-reset:step;}
.steps li{counter-increment:step;display:flex;gap:var(--space-3);margin-bottom:var(--space-4);font-size:15px;color:var(--text-secondary);line-height:1.65;}
.steps li::before{content:counter(step);min-width:24px;height:24px;border-radius:50%;background:rgba(255,149,0,.15);color:var(--econ);font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}
.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--econ);background:rgba(255,149,0,.1);}
.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav a{display:inline-flex;align-items:center;gap:var(--space-2);font-size:14px;font-weight:500;color:var(--text-tertiary);text-decoration:none;padding:var(--space-3) var(--space-4);border:1px solid var(--separator);border-radius:var(--radius-md);transition:all var(--transition-base);}
.ch-nav a:hover{color:var(--text-primary);border-color:rgba(var(--text-rgb),0.15);background:var(--bg-secondary);}
.ch-nav a.primary{color:var(--econ);border-color:rgba(255,149,0,.3);background:rgba(255,149,0,.05);}
.ch-nav a.primary:hover{background:rgba(255,149,0,.12);}
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

.data-table {
  width: 100%;
  border-collapse: collapse;
  margin: var(--space-4) 0;
  font-size: 15px;
}

.data-table th,
.data-table td {
  padding: var(--space-3) var(--space-4);
  text-align: left;
  border-bottom: 1px solid var(--separator);
  color: var(--text-secondary);
}

.data-table th {
  background: var(--bg-secondary);
  color: var(--text-primary);
  font-weight: 600;
  font-size: 14px;
}

.data-table td {
  color: var(--text-secondary);
}

.data-table tr:hover {
  background: var(--bg-secondary);
}
</style>

<div class="ch-wrap">
  <div id="chapter-content" class="chapter-content">
    <div class="ch-breadcrumb">
      <a href="/learn/">Learn</a>
      <span class="ch-breadcrumb-sep">›</span>
      <a href="/learn/vwl/">VWL</a>
      <span class="ch-breadcrumb-sep">›</span>
      <span>Angebotskurve</span>
    </div>

    <div class="ch-header">
      <div class="ch-eyebrow">VWL · Kapitel 3</div>
      <h1>Die Angebotskurve</h1>
      <div class="ch-header-meta">
        <span>ca. 25 min</span>
        <span>·</span>
        <span>Marktmodell</span>
        <span>·</span>
        <span>Angebotsfunktion</span>
        <span>·</span>
        <span>Aggregiertes Angebot</span>
        <span>·</span>
        <span>Verschiebungen</span>
      </div>
    </div>

    <div class="ch-sections">

      <!-- Section 1: Überblick -->
      <section class="ch-section" id="sec-ueberblick">
        <h2>Überblick – Das Marktmodell</h2>

        <p>Ein Markt ist der ökonomische Ort des Zusammentreffens von Angebot und Nachfrage. An diesem Ort treffen Produzenten (Anbieter) und Konsumenten (Käufer) zusammen, um Güter und Dienstleistungen auszutauschen. Das Marktmodell bildet die Grundlage für das Verständnis, wie Preise entstehen und wie Märkte funktionieren.</p>

        <h3>Grundprinzipien des Marktes</h3>

        <ul>
          <li><strong>Koordination durch Märkte:</strong> Märkte koordinieren automatisch die Aktivitäten von Käufern und Verkäufern, ohne dass eine zentrale Planung notwendig ist. Dies geschieht durch das Preissystem, das Anreize schafft und Information übermittelt.</li>
          <li><strong>Preisbildung:</strong> Der Preis wird durch das Zusammenspiel von Angebot und Nachfrage bestimmt. Ein höheres Angebot bei gleichbleibender Nachfrage führt zu niedrigeren Preisen, während ein geringeres Angebot zu höheren Preisen führt.</li>
          <li><strong>Marktgleichgewicht:</strong> Das Marktgleichgewicht entsteht, wenn die angebotene Menge gleich der nachgefragten Menge ist. In diesem Punkt gibt es keinen Überschuss und keinen Mangel – der Markt räumt sich selbst.</li>
        </ul>

        <p>In diesem Kapitel konzentrieren wir uns auf die <strong>Angebotsseite</strong> des Marktes. Wir werden untersuchen, wie Produzenten ihre Angebote bestimmen, wie sich die Angebotskurve verhält und welche Faktoren zu Verschiebungen der Angebotskurve führen.</p>
      </section>

      <!-- Section 2: Gesetz des Angebots -->
      <section class="ch-section" id="sec-gesetz">
        <h2>Das Gesetz des Angebots</h2>

        <p>Das Gesetz des Angebots beschreibt die grundlegende Beziehung zwischen dem Preis eines Gutes und der Menge, die Produzenten anbieten möchten. Es ist eines der fundamentalsten Konzepte in der Ökonomie.</p>

        <h3>Die Grundregel</h3>

        <p><strong>Bei steigendem Preis steigt die angebotene Menge, während bei sinkendem Preis die angebotene Menge fällt</strong> – ceteris paribus (alles andere bleibt gleich). Dies bedeutet, dass die Angebotskurve eine positive Steigung hat.</p>

        <h3>Warum gilt das Gesetz des Angebots?</h3>

        <ul>
          <li><strong>Produktionskosten und Gewinne:</strong> Ein höherer Preis macht die Produktion profitabler. Produzenten sind bereit, mehr Einheiten herzustellen, wenn der Ertrag pro Einheit steigt. Dies ist besonders wichtig, weil die Produktionskosten häufig mit steigender Produktionsmenge zunehmen (steigende Grenzkosten).</li>
          <li><strong>Grenzkosten decken:</strong> Bei niedrigen Preisen können nur die Produzenten mit den niedrigsten Kosten profitabel produzieren. Wenn der Preis steigt, können auch Produzenten mit höheren Kosten profitabel werden. Sie bieten ihre Produkte an, weil der Preis nun ihre Kosten deckt.</li>
          <li><strong>Markteintritt neuer Anbieter:</strong> Bei höheren Preisen werden neue Produzenten in den Markt eintreten, da sich die Produktion nun lohnt. Bei niedrigeren Preisen werden manche Produzenten den Markt verlassen. Dies führt zu einer erhöhten angebotenen Gesamtmenge bei höheren Preisen.</li>
        </ul>

        <div class="cb cb-def">
          <div class="cb-label">Definition</div>
          <div class="cb-title">Gesetz des Angebots</div>
          <p>Das Gesetz des Angebots besagt, dass bei steigendem Preis eines Gutes die angebotene Menge steigt und bei sinkendem Preis die angebotene Menge sinkt (ceteris paribus). Dies führt zu einer positiven Beziehung zwischen Preis und angebotener Menge und damit zu einer aufwärts gerichteten Angebotskurve.</p>
        </div>
      </section>

      <!-- Section 3: Angebotsfunktion -->
      <section class="ch-section" id="sec-angebotsfunktion">
        <h2>Die Angebotsfunktion</h2>

        <p>Die Angebotsfunktion beschreibt mathematisch die Beziehung zwischen dem Preis und der angebotenen Menge. Sie zeigt, wie viele Einheiten eines Gutes Produzenten bei verschiedenen Preisen anbieten möchten.</p>

        <h3>Lineare Angebotsfunktion</h3>

        <p>Die einfachste und häufig verwendete Form der Angebotsfunktion ist die lineare Angebotsfunktion:</p>

        <div class="math-block">
          $$p(x) = m \cdot x + t$$
        </div>

        <p>Dabei bedeuten:</p>

        <ul>
          <li><strong>$p(x)$:</strong> Der Preis als Funktion der Menge</li>
          <li><strong>$x$:</strong> Die angebotene Menge</li>
          <li><strong>$m$:</strong> Die Steigung der Angebotskurve (immer positiv, $m > 0$). Die Steigung gibt an, um wie viel der Preis steigt, wenn die Menge um eine Einheit erhöht wird: $m = \frac{\Delta p}{\Delta x}$</li>
          <li><strong>$t$:</strong> Der y-Achsenabschnitt. Dies ist der Mindestpreis (Reservationspreis), ab dem ein Produzent bereit ist anzubieten. Unter diesem Preis bietet der Produzent nichts an, da die Kosten nicht gedeckt werden</li>
        </ul>

        <h3>Interpretation</h3>

        <p>Die Parameter haben eine wichtige wirtschaftliche Bedeutung:</p>

        <ul>
          <li>Der Mindestpreis $t$ spiegelt die minimalen Produktionskosten wider oder die Mindestrendite, die der Produzent erwartet</li>
          <li>Die Steigung $m$ zeigt, wie empfindlich das Angebot auf Preisänderungen reagiert. Eine steilere Kurve (größeres $m$) bedeutet, dass das Angebot weniger empfindlich auf Preisänderungen reagiert</li>
        </ul>

        <h3>Beispiel: Fischmarkt</h3>

        <div class="cb cb-ex">
          <div class="cb-label">Beispiel</div>
          <div class="cb-title">Fischmarkt</div>
          <p>Ein Fischhändler hat folgende Angebotsfunktion: $p(x) = \frac{1}{2}x + 2$</p>

          <p><strong>Interpretation:</strong> Der Mindestpreis, bei dem der Fischhändler zu verkaufen bereit ist, liegt bei 2€ pro Kilogramm. Für jede zusätzliche Einheit (kg) steigt der Preis um 0,50€. Dies bedeutet, dass bei höheren Preisen der Händler bereit ist, mehr Fisch zu verkaufen.</p>

          <p><strong>Einzelne Punkte:</strong></p>

          <table class="data-table">
            <thead>
              <tr>
                <th>Menge $x$ (kg)</th>
                <th>Preis $p$ (€)</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>0</td>
                <td>2,00</td>
              </tr>
              <tr>
                <td>2</td>
                <td>3,00</td>
              </tr>
              <tr>
                <td>4</td>
                <td>4,00</td>
              </tr>
              <tr>
                <td>6</td>
                <td>5,00</td>
              </tr>
              <tr>
                <td>10</td>
                <td>7,00</td>
              </tr>
              <tr>
                <td>20</td>
                <td>12,00</td>
              </tr>
            </tbody>
          </table>

          <p><strong>Berechnung für ausgewählte Punkte:</strong></p>
          <ul>
            <li>Für $x = 0$: $p(0) = \frac{1}{2} \cdot 0 + 2 = 2€$</li>
            <li>Für $x = 4$: $p(4) = \frac{1}{2} \cdot 4 + 2 = 4€$</li>
            <li>Für $x = 20$: $p(20) = \frac{1}{2} \cdot 20 + 2 = 12€$</li>
          </ul>
        </div>

        <h3>Alternative Darstellung: Menge als Funktion des Preises</h3>

        <p>Manchmal ist es nützlich, die Angebotsfunktion umzuformen, sodass die Menge als Funktion des Preises ausgedrückt wird. Dies wird durch Umstellen der Gleichung erreicht:</p>

        <div class="math-block">
          $$p = m \cdot x + t$$
          $$p - t = m \cdot x$$
          $$x = \frac{p - t}{m}$$
        </div>

        <p>Im Fischmarkt-Beispiel: $x = \frac{p - 2}{0.5} = 2p - 4$ für $p \geq 2$</p>
      </section>

      <!-- Section 4: Aggregiertes Marktangebot -->
      <section class="ch-section" id="sec-aggregiert">
        <h2>Aggregiertes Marktangebot</h2>

        <p>Auf einem echten Markt gibt es nicht nur einen, sondern viele Anbieter. Das aggregierte Marktangebot ist die Summe aller individuellen Angebotskurven auf einem Markt. Es zeigt die Gesamtmenge, die alle Produzenten zusammen bei verschiedenen Preisen anbieten möchten.</p>

        <h3>Horizontale Addition</h3>

        <p>Das aggregierte Angebot wird durch <strong>horizontale Addition</strong> berechnet. Das bedeutet: Für jeden Preis addieren wir die Mengen auf, die alle einzelnen Produzenten bei diesem Preis anbieten. Dies unterscheidet sich von vertikaler Addition, bei der man für eine gegebene Menge die Preise addiert.</p>

        <h3>Wichtige Regel: Mindestpreis beachten</h3>

        <p>Ein kritischer Punkt bei der Aggregation ist, dass jeder Produzent nur bei oder über seinem Mindestpreis anbietet. Ein Produzent mit einem Mindestpreis von 4€ wird bei einem Marktpreis von 3€ nichts anbieten.</p>

        <h3>Schritte zur Aggregation</h3>

        <ol class="steps">
          <li><strong>Umstellen nach Menge:</strong> Formen Sie jede individuelle Angebotsfunktion so um, dass die Menge als Funktion des Preises ausgedrückt wird: $x_i = \frac{p - t_i}{m_i}$</li>
          <li><strong>Mindestpreis prüfen:</strong> Bestimmen Sie für jeden Produzenten, ab welchem Preis er anbietet. Dies ist sein Mindestpreis $t_i$</li>
          <li><strong>Segmente bilden:</strong> Teilen Sie die Preisachse in Segmente auf, die durch die verschiedenen Mindestpreise definiert werden</li>
          <li><strong>In jedem Segment aggregieren:</strong> Für jedes Preissegment addieren Sie die Mengen der Produzenten, deren Mindestpreis unter oder gleich diesem Preis liegt</li>
        </ol>

        <h3>Beispiel: Zwei Fischfabriken</h3>

        <div class="cb cb-ex">
          <div class="cb-label">Beispiel</div>
          <div class="cb-title">Marktangebot von zwei Fischfabriken</div>

          <p><strong>Gegeben sind zwei Anbieter:</strong></p>
          <ul>
            <li>Nemo GmbH: $p_1(x) = 2x + 4$ (Mindestpreis: 4€)</li>
            <li>Dori KG: $p_2(x) = x + 2$ (Mindestpreis: 2€)</li>
          </ul>

          <p><strong>Schritt 1: Nach Menge umstellen</strong></p>
          <ul>
            <li>Nemo: $p = 2x + 4$ → $x_1 = \frac{p - 4}{2}$ für $p \geq 4$</li>
            <li>Dori: $p = x + 2$ → $x_2 = p - 2$ für $p \geq 2$</li>
          </ul>

          <p><strong>Schritt 2: Aggregation in Preissegmenten</strong></p>

          <p><strong>Für $2 \leq p < 4$:</strong> Nur Dori bietet an (Nemos Preis ist zu niedrig)</p>
          <div class="math-block">
            $$X = x_2 = p - 2$$
          </div>

          <p><strong>Für $p \geq 4$:</strong> Beide bieten an</p>
          <div class="math-block">
            $$X = x_1 + x_2 = \frac{p - 4}{2} + (p - 2) = \frac{p - 4}{2} + \frac{2(p - 2)}{2} = \frac{p - 4 + 2p - 4}{2} = \frac{3p - 8}{2}$$
          </div>

          <p><strong>Gesamtes Marktangebot:</strong></p>
          <div class="math-block">
            X(p) = \begin{cases}
            p - 2 & \text{für } 2 \leq p < 4 \\
            \frac{3p - 8}{2} & \text{für } p \geq 4
            \end{cases}
          </div>

          <p><strong>Verifikation:</strong></p>
          <table class="data-table">
            <thead>
              <tr>
                <th>Preis (€)</th>
                <th>Nemo</th>
                <th>Dori</th>
                <th>Markt ($X$)</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>2</td>
                <td>0</td>
                <td>0</td>
                <td>0</td>
              </tr>
              <tr>
                <td>3</td>
                <td>0</td>
                <td>1</td>
                <td>1</td>
              </tr>
              <tr>
                <td>4</td>
                <td>0</td>
                <td>2</td>
                <td>2</td>
              </tr>
              <tr>
                <td>5</td>
                <td>0,5</td>
                <td>3</td>
                <td>3,5</td>
              </tr>
              <tr>
                <td>6</td>
                <td>1</td>
                <td>4</td>
                <td>5</td>
              </tr>
              <tr>
                <td>8</td>
                <td>2</td>
                <td>6</td>
                <td>8</td>
              </tr>
            </tbody>
          </table>

          <p><strong>Beachte:</strong> Bei $p = 4€$ liegt der Punkt, wo die Angebotskurve einen Knick hat. Davor wird nur von Dori angeboten, danach von beiden. Dies ändert die Steigung der aggregierten Angebotskurve.</p>
        </div>

        <div class="cb cb-note">
          <div class="cb-label">Wichtiger Hinweis</div>
          <div class="cb-title">Mindestpreis-Bedingung</div>
          <p>Bei der Aggregation ist es entscheidend, für jeden Produzenten zu prüfen, ob $p \geq t_i$ (der Preis mindestens gleich dem Mindestpreis ist). Nur wenn diese Bedingung erfüllt ist, bietet der Produzent an. Dies führt häufig dazu, dass das aggregierte Marktangebot aus mehreren linearen Segmenten mit unterschiedlichen Steigungen besteht.</p>
        </div>
      </section>

      <!-- Section 5: Verschiebung vs. Bewegung -->
      <section class="ch-section" id="sec-verschiebung">
        <h2>Verschiebung vs. Bewegung auf der Angebotskurve</h2>

        <p>Es ist wichtig, zwischen zwei verschiedenen Arten von Veränderungen zu unterscheiden: einer <strong>Bewegung entlang der Angebotskurve</strong> und einer <strong>Verschiebung der gesamten Angebotskurve</strong>.</p>

        <h3>Bewegung entlang der Angebotskurve</h3>

        <p>Eine <strong>Bewegung entlang der Angebotskurve</strong> tritt auf, wenn sich der Preis des Gutes selbst ändert, während alle anderen Faktoren konstant bleiben (ceteris paribus). Dies ist eine <strong>Änderung der angebotenen Menge</strong>, keine Änderung des Angebots selbst. Die Angebotskurve bleibt dieselbe, aber wir bewegen uns auf ihr nach oben oder unten.</p>

        <p><strong>Beispiel:</strong> Wenn der Fischpreis von 3€ auf 5€ steigt, bewegen wir uns auf der bestehenden Angebotskurve zu höheren Mengen. Das ist keine Änderung der Angebotsfunktion, sondern eine Reaktion auf die Preisänderung.</p>

        <h3>Verschiebung der Angebotskurve</h3>

        <p>Eine <strong>Verschiebung der Angebotskurve</strong> tritt auf, wenn sich die Angebotsfunktion selbst ändert. Dies ist eine <strong>Änderung des Angebots</strong> – die Menge, die bei jedem Preis angeboten wird, ändert sich, auch wenn der Preis des Gutes selbst gleich bleibt. Die gesamte Kurve verschiebt sich nach links (Angebotsrückgang) oder nach rechts (Angebotsanstieg).</p>

        <p><strong>Beispiel:</strong> Wenn neue Fischerei-Technologie eingeführt wird, die effizienter ist, können Fischhändler bei jedem Preis mehr anbieten. Die Angebotskurve verschiebt sich nach rechts.</p>

        <h3>Die fünf Faktoren der Angebotsverschiebung</h3>

        <div class="cb cb-def">
          <div class="cb-label">Definition</div>
          <div class="cb-title">Faktoren der Angebotsverschiebung</div>

          <ol>
            <li><strong>Produktionsfaktoren (Inputkosten):</strong> Änderungen in den Preisen von Rohstoffen, Arbeitskraft, Energie oder anderen Produktionsfaktoren verschieben die Angebotskurve. Höhere Inputkosten verringern das Angebot (Verschiebung nach links), niedrigere Kosten erhöhen das Angebot (Verschiebung nach rechts).</li>

            <li><strong>Wettbewerb und Markteintritt:</strong> Ein Anstieg der Anzahl von Anbietern auf dem Markt verschiebt das aggregierte Marktangebot nach rechts. Wenn Anbieter den Markt verlassen, verschiebt sich das Angebot nach links.</li>

            <li><strong>Steuern und Subventionen:</strong> Subventionen für Produzenten reduzieren ihre effektiven Kosten und verschieben das Angebot nach rechts. Steuern auf Produzenten erhöhen ihre Kosten und verschieben das Angebot nach links.</li>

            <li><strong>Technologischer Fortschritt:</strong> Verbesserte Produktionstechnologien reduzieren die Produktionskosten und ermöglichen höhere Produktion, wodurch das Angebot nach rechts verschoben wird. Dies ist einer der wichtigsten langfristigen Faktoren für Angebotsänderungen.</li>

            <li><strong>Erwartungen:</strong> Wenn Produzenten erwarten, dass der Preis in der Zukunft steigt, können sie heute weniger anbieten, um mehr zu lagern und später zu höheren Preisen zu verkaufen. Dies verschiebt das Angebot nach links. Umgekehrt verschiebt das Angebot nach rechts, wenn Produzenten mit sinkenden Preisen rechnen.</li>
          </ol>
        </div>

        <h3>Grafische Darstellung</h3>

        <p><strong>Bewegung entlang der Kurve:</strong> Wenn der Preis von $p_1$ auf $p_2$ steigt, bewegen wir uns auf der Kurve vom Punkt A zum Punkt B. Die Menge steigt von $x_1$ auf $x_2$.</p>

        <p><strong>Verschiebung der Kurve:</strong> Wenn sich ein anderer Faktor ändert (z.B. Technologie), kann die gesamte Kurve nach rechts von $S_1$ zu $S_2$ verschoben werden. Bei dem gleichen Preis $p_1$ wird jetzt die Menge $x_3$ angeboten statt $x_1$.</p>

        <h3>Zusammenfassung der Unterschiede</h3>

        <table class="data-table">
          <thead>
            <tr>
              <th>Aspekt</th>
              <th>Bewegung entlang der Kurve</th>
              <th>Verschiebung der Kurve</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td><strong>Ursache</strong></td>
              <td>Preisänderung des Gutes selbst</td>
              <td>Änderung anderer Faktoren (Kosten, Technologie, etc.)</td>
            </tr>
            <tr>
              <td><strong>Was ändert sich</strong></td>
              <td>Angebotene Menge ($x$)</td>
              <td>Gesamte Angebotsfunktion</td>
            </tr>
            <tr>
              <td><strong>Kurve selbst</strong></td>
              <td>Bleibt gleich</td>
              <td>Verschiebt sich</td>
            </tr>
            <tr>
              <td><strong>Richtung</strong></td>
              <td>Auf der Kurve auf und ab</td>
              <td>Links oder rechts</td>
            </tr>
          </tbody>
        </table>
      </section>

      <!-- Section 6: Zusammenfassung -->
      <section class="ch-section" id="sec-zusammenfassung">
        <h2>Zusammenfassung</h2>

        <p>In diesem Kapitel haben wir die Angebotsseite des Marktes gründlich untersucht. Hier sind die wichtigsten Erkenntnisse:</p>

        <h3>Kernpunkte</h3>

        <ul>
          <li><strong>Das Gesetz des Angebots:</strong> Bei höheren Preisen bieten Produzenten größere Mengen an. Dies führt zu einer aufwärts gerichteten (positiv geneigten) Angebotskurve.</li>

          <li><strong>Lineare Angebotsfunktion:</strong> Die Angebotsfunktion $p(x) = m \cdot x + t$ beschreibt die Beziehung zwischen Preis und angebotener Menge. Der Parameter $t$ ist der Mindestpreis, $m$ ist die positive Steigung.</li>

          <li><strong>Aggregiertes Angebot:</strong> Das Marktangebot wird durch horizontale Addition der individuellen Angebotskurven berechnet. Dabei ist es wichtig zu beachten, dass jeder Produzent nur bei Preisen $p \geq t_i$ anbietet.</li>

          <li><strong>Verschiebungen:</strong> Eine Bewegung entlang der Kurve wird durch Preisänderungen verursacht. Eine Verschiebung der Kurve wird durch Änderungen anderer Faktoren verursacht (Inputkosten, Technologie, Wettbewerb, Steuern/Subventionen, Erwartungen).</li>

          <li><strong>Praktische Anwendung:</strong> Das Verständnis der Angebotskurve ist essentiell für die Analyse von Märkten. Es ermöglicht uns, vorherzusagen, wie Märkte auf verschiedene Veränderungen reagieren werden.</li>
        </ul>

        <div class="cb cb-note">
          <div class="cb-label">Merksatz</div>
          <div class="cb-title">Das Angebotsprinzip</div>
          <p><strong>Höherer Preis → Größere angebotene Menge.</strong> Dies ist das fundamentale Prinzip, das die Angebotskurve charakterisiert. Es erklärt, warum Märkte funktionieren und wie sich Produzenten auf Preisänderungen reagieren.</p>
        </div>
      </section>

      <!-- Section 7: Übungsaufgaben -->
      <section class="ch-section" id="sec-aufgaben">
        <h2>Übungsaufgaben</h2>

        <h3>Aufgabe 1: Kerzen-Angebotsfunktion</h3>

        <p>Ein Kerzenhersteller bietet ab einem Mindestpreis von 3€ an. Für jede zusätzliche Einheit steigt der erforderliche Preis um 0,25€.</p>

        <p><strong>Fragen:</strong></p>
        <ol>
          <li>Stellen Sie die Angebotsfunktion auf (in der Form $p(x) = m \cdot x + t$)</li>
          <li>Bei welchem Preis werden genau 20 Kerzen angeboten?</li>
          <li>Wie viele Kerzen werden bei einem Preis von 5€ angeboten?</li>
        </ol>

        <div class="cb cb-ex">
          <div class="cb-label">Lösung</div>

          <p><strong>Frage 1: Angebotsfunktion</strong></p>
          <p>Gegeben: Mindestpreis $t = 3€$, Steigung $m = 0,25$</p>
          <div class="math-block">
            $$p(x) = 0,25x + 3$$
          </div>

          <p><strong>Frage 2: Preis bei 20 Kerzen</strong></p>
          <div class="math-block">
            $$p(20) = 0,25 \cdot 20 + 3 = 5 + 3 = 8€$$
          </div>
          <p>Bei 20 Kerzen beträgt der Preis 8€.</p>

          <p><strong>Frage 3: Menge bei 5€</strong></p>
          <p>Umformen nach $x$: $p = 0,25x + 3$ → $0,25x = p - 3$ → $x = 4(p - 3) = 4p - 12$</p>
          <div class="math-block">
            $$x(5) = 4 \cdot 5 - 12 = 20 - 12 = 8 \text{ Kerzen}$$
          </div>
          <p>Bei einem Preis von 5€ werden 8 Kerzen angeboten.</p>
        </div>

        <h3>Aufgabe 2: Aggregiertes Angebot Biogemüse</h3>

        <p>Auf dem Biogemüse-Markt gibt es zwei Produzenten:</p>
        <ul>
          <li>Bauer A: $p_A(x) = x + 3$</li>
          <li>Bauer B: $p_B(x) = 2x + 1$</li>
        </ul>

        <p><strong>Fragen:</strong></p>
        <ol>
          <li>Berechnen Sie das aggregierte Marktangebot (berücksichtigen Sie die unterschiedlichen Mindestpreise)</li>
          <li>Wie viel wird insgesamt bei einem Preis von 5€ angeboten?</li>
          <li>Zeichnen Sie (skizzieren Sie) die Marktangebotskurve</li>
        </ol>

        <div class="cb cb-ex">
          <div class="cb-label">Lösung</div>

          <p><strong>Frage 1: Aggregiertes Angebot</strong></p>

          <p>Schritt 1: Nach $x$ umformen</p>
          <ul>
            <li>Bauer A: $p = x + 3$ → $x_A = p - 3$ für $p \geq 3$</li>
            <li>Bauer B: $p = 2x + 1$ → $x_B = \frac{p - 1}{2}$ für $p \geq 1$</li>
          </ul>

          <p>Schritt 2: Aggregation in Preissegmenten</p>

          <p><strong>Für $1 \leq p < 3$:</strong> Nur Bauer B bietet an</p>
          <div class="math-block">
            $$X = \frac{p - 1}{2}$$
          </div>

          <p><strong>Für $p \geq 3$:</strong> Beide bieten an</p>
          <div class="math-block">
            $$X = (p - 3) + \frac{p - 1}{2} = \frac{2(p-3) + (p-1)}{2} = \frac{2p - 6 + p - 1}{2} = \frac{3p - 7}{2}$$
          </div>

          <p><strong>Gesamtes Marktangebot:</strong></p>
          <div class="math-block">
            X(p) = \begin{cases}
            \frac{p - 1}{2} & \text{für } 1 \leq p < 3 \\
            \frac{3p - 7}{2} & \text{für } p \geq 3
            \end{cases}
          </div>

          <p><strong>Frage 2: Menge bei p = 5€</strong></p>
          <p>Da $5 \geq 3$, verwenden wir die zweite Formel:</p>
          <div class="math-block">
            $$X(5) = \frac{3 \cdot 5 - 7}{2} = \frac{15 - 7}{2} = \frac{8}{2} = 4 \text{ Einheiten}$$
          </div>

          <p><strong>Frage 3: Skizze der Marktangebotskurve</strong></p>
          <p>Die Kurve besteht aus zwei Segmenten:</p>
          <ul>
            <li>Von $p=1$ bis $p=3$: Steigung 0,5 (nur Bauer B)</li>
            <li>Ab $p=3$: Steigung 1,5 (beide Bauern)</li>
            <li>Bei $p=3$ befindet sich ein Knickpunkt, die Kurve wird steiler</li>
          </ul>
        </div>

        <h3>Aufgabe 3: Solarmodule – Verschiebungen der Angebotskurve</h3>

        <p>Die Angebotskurve für Solarmodule ist gegeben durch $p(x) = 0,5x + 10$.</p>

        <p><strong>Frage:</strong> Erklären Sie anhand dieser Beispiele, wie sich die Angebotskurve verschiebt, wenn folgende Änderungen eintreten:</p>
        <ol>
          <li>Der Preis für Silizium (ein wichtiger Rohstoff) steigt deutlich</li>
          <li>Eine neue, effizientere Produktionstechnologie wird eingeführt</li>
          <li>Die Regierung gewährt Subventionen für die Solarmodulproduktion</li>
          <li>Die Anzahl der Solarmodulhersteller sinkt, da einige Unternehmen den Markt verlassen</li>
        </ol>

        <div class="cb cb-ex">
          <div class="cb-label">Lösung</div>

          <p><strong>Ausgangssituation:</strong> $p(x) = 0,5x + 10$</p>

          <p><strong>1. Preis für Silizium steigt</strong></p>
          <p><strong>Effekt:</strong> Verschiebung nach <strong>links</strong> (Angebotsrückgang)</p>
          <p><strong>Begründung:</strong> Höhere Rohstoffkosten erhöhen die Produktionskosten. Der Mindestpreis (y-Achsenabschnitt) steigt. Beispiel: $p(x) = 0,5x + 15$</p>

          <p><strong>2. Neue, effizientere Produktionstechnologie</strong></p>
          <p><strong>Effekt:</strong> Verschiebung nach <strong>rechts</strong> (Angebotsanstieg)</p>
          <p><strong>Begründung:</strong> Bessere Technologie reduziert die Produktionskosten. Der Mindestpreis sinkt, oder bei gleichem Preis können mehr Einheiten produziert werden. Die Steigung wird flacher. Beispiel: $p(x) = 0,3x + 5$</p>

          <p><strong>3. Regierung gewährt Subventionen</strong></p>
          <p><strong>Effekt:</strong> Verschiebung nach <strong>rechts</strong> (Angebotsanstieg)</p>
          <p><strong>Begründung:</strong> Subventionen senken die effektiven Kosten für Produzenten. Sie können bei jedem Preis mehr anbieten. Beispiel: $p(x) = 0,5x + 8$</p>

          <p><strong>4. Anzahl der Hersteller sinkt</strong></p>
          <p><strong>Effekt:</strong> Verschiebung nach <strong>links</strong> (Angebotsrückgang)</p>
          <p><strong>Begründung:</strong> Weniger Anbieter bedeutet weniger Gesamtangebot auf dem Markt. Das aggregierte Angebot sinkt. Das Marktangebot würde sich vom aggregierten Angebot aller Hersteller nach links verschieben.</p>

          <p><strong>Zusammenfassung:</strong></p>
          <table class="data-table">
            <thead>
              <tr>
                <th>Änderung</th>
                <th>Verschiebung</th>
                <th>Grund</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td>Rohstoffpreis ↑</td>
                <td>← Links</td>
                <td>Kosten ↑, weniger profitable Produktion</td>
              </tr>
              <tr>
                <td>Technologie ↑</td>
                <td>Rechts →</td>
                <td>Kosten ↓, effizienter produzieren</td>
              </tr>
              <tr>
                <td>Subventionen ↑</td>
                <td>Rechts →</td>
                <td>Effektive Kosten ↓</td>
              </tr>
              <tr>
                <td>Anzahl Anbieter ↓</td>
                <td>← Links</td>
                <td>Weniger Gesamtangebot</td>
              </tr>
            </tbody>
          </table>
        </div>
      </section>

    </div>

    <!-- Navigation -->
    <div class="ch-nav">
      <a href="/learn/gueterarten/">← Güterarten</a>
      <a href="/learn/nachfragekurve/" class="primary">Nachfragekurve →</a>
    </div>
  </div>

  <!-- TOC Sidebar -->
  <aside class="ch-toc">
    <div class="ch-toc-title">Kapitel</div>
    <ul>
      <li><a href="#sec-ueberblick">Überblick</a></li>
      <li><a href="#sec-gesetz">Gesetz des Angebots</a></li>
      <li><a href="#sec-angebotsfunktion">Angebotsfunktion</a></li>
      <li><a href="#sec-aggregiert">Aggregiertes Angebot</a></li>
      <li><a href="#sec-verschiebung">Verschiebung vs. Bewegung</a></li>
      <li><a href="#sec-zusammenfassung">Zusammenfassung</a></li>
      <li><a href="#sec-aufgaben">Übungsaufgaben</a></li>
    </ul>
  </aside>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const sections = document.querySelectorAll('[id^="sec-"]');
  const tocLinks = document.querySelectorAll('.ch-toc a');

  function updateActiveLink() {
    let current = '';

    sections.forEach(section => {
      const sectionTop = section.offsetTop;
      if (window.pageYOffset >= sectionTop - 200) {
        current = section.getAttribute('id');
      }
    });

    tocLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href') === '#' + current) {
        link.classList.add('active');
      }
    });
  }

  window.addEventListener('scroll', updateActiveLink);
  updateActiveLink();
});
</script>
