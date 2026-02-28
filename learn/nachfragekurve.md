---
layout: page
title:
permalink: /learn/nachfragekurve/
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
</style>

<div class="ch-wrap">
  <div id="chapter-content">
    <div class="ch-breadcrumb">
      <a href="/learn/">Learn</a>
      <span class="ch-breadcrumb-sep">›</span>
      <a href="/learn/vwl/">VWL</a>
      <span class="ch-breadcrumb-sep">›</span>
      <span>Nachfragekurve</span>
    </div>

    <div class="ch-header">
      <div class="ch-eyebrow">VWL · Kapitel 4</div>
      <h1>Die Nachfragekurve</h1>
      <div class="ch-header-meta">
        <span>ca. 25 min</span>
        <span>·</span>
        <span>Gesetz der Nachfrage</span>
        <span>·</span>
        <span>Nachfragefunktion</span>
        <span>·</span>
        <span>Aggregierte Nachfrage</span>
        <span>·</span>
        <span>Verschiebungen</span>
      </div>
    </div>

    <div class="ch-sections">
      <!-- ÜBERBLICK -->
      <section class="ch-section" id="sec-ueberblick">
        <h2>Überblick – Grundlagen der Nachfrage</h2>
        <p>Nachfrage ist eine der zentralsten Größen in der Volkswirtschaftslehre. Sie beschreibt, welche Menge eines Gutes Käufer bereit und in der Lage sind, zu einem bestimmten Preis zu kaufen. Im Gegensatz zu theoretischen Wünschen oder Bedürfnissen ist die Nachfrage durch zwei Bedingungen gekennzeichnet:</p>
        <ul>
          <li><strong>Bereitschaft</strong> – der Käufer möchte das Gut erwerben</li>
          <li><strong>Fähigkeit</strong> – der Käufer verfügt über die notwendigen Mittel (Einkommen)</li>
        </ul>
        <p>In unserem Marktmodell bildet die Nachfrage eine der beiden Seiten des Marktes. Während die Angebotsseite beschreibt, welche Menge Produzenten zu verschiedenen Preisen bereitzustellen bereit sind, zeigt die Nachfrageseite das Verhalten der Konsumenten. Das Zusammenspiel von Angebot und Nachfrage bestimmt letztlich den Marktpreis und die Gleichgewichtsmenge.</p>
        <p>In diesem Kapitel werden wir die Nachfragekurve detailliert analysieren: wie sie aussieht, welche Faktoren sie beeinflussen, und wie man sie mathematisch darstellt. Dieses Verständnis ist fundamental für alle weiteren ökonomischen Analysen.</p>
      </section>

      <!-- GESETZ DER NACHFRAGE -->
      <section class="ch-section" id="sec-gesetz">
        <h2>Das Gesetz der Nachfrage</h2>
        <p>Das Gesetz der Nachfrage ist eines der robustesten und intuitivsten Gesetze der Ökonomie. Es besagt, dass die nachgefragte Menge eines Gutes sinkt, wenn der Preis steigt – und umgekehrt. Diese Beziehung gilt unter der Bedingung ceteris paribus (alle anderen Faktoren bleiben konstant).</p>
        <p>Intuitiv macht das Sinn: Wenn ein Produkt teurer wird, können sich weniger Menschen leisten, es zu kaufen. Gleichzeitig sind diejenigen, die es sich leisten könnten, eher geneigt, nach Alternativen zu suchen. Umgekehrt führt ein niedrigerer Preis dazu, dass mehr Menschen das Gut kaufen können und möchten.</p>
        <p>Grafisch stellt sich das Gesetz der Nachfrage als eine fallende Kurve dar. Die x-Achse zeigt die Menge (Quantität), die y-Achse zeigt den Preis. Da Preis und Menge in entgegengesetzter Richtung sich bewegen, hat die Nachfragekurve eine negative Steigung.</p>

        <div class="cb cb-def">
          <div class="cb-label">Definition</div>
          <div class="cb-title">Das Gesetz der Nachfrage</div>
          <p>Das Gesetz der Nachfrage besagt, dass zwischen dem Preis eines Gutes und der nachgefragten Menge dieses Gutes ein inverses Verhältnis besteht. Je höher der Preis, desto geringer die nachgefragte Menge (ceteris paribus). Je niedriger der Preis, desto höher die nachgefragte Menge.</p>
        </div>

        <div class="cb cb-note">
          <div class="cb-label">Wichtige Begriffe</div>
          <p><strong>Prohibitivpreis:</strong> Der Preis, bei dem die nachgefragte Menge genau null ist. Oberhalb dieses Preises kauft niemand das Gut mehr. Dies ist der y-Achsenabschnitt der Nachfragekurve.</p>
          <p><strong>Marktsättigung (oder Sättigungsmenge):</strong> Die Menge, die bei einem Preis von null nachgefragt würde – also die maximale Nachfrage, wenn das Gut kostenlos wäre. Dies ist der x-Achsenabschnitt der Nachfragekurve.</p>
        </div>
      </section>

      <!-- NACHFRAGEFUNKTION -->
      <section class="ch-section" id="sec-nachfragefunktion">
        <h2>Die Nachfragefunktion</h2>
        <p>Um die Nachfrage mathematisch zu erfassen, stellen wir sie als Funktion dar. Die einfachste und häufig verwendete Form ist die lineare Nachfragefunktion:</p>

        <div class="math-block">
          $$p = a - b \cdot x$$
        </div>

        <p>Hierbei gilt:</p>
        <ul>
          <li>$p$ = Preis des Gutes</li>
          <li>$x$ = nachgefragte Menge</li>
          <li>$a$ = y-Achsenabschnitt (Prohibitivpreis)</li>
          <li>$b$ = Steigung (absolute Wert der Steigung ist positiv, die Kurve fällt aber nach rechts)</li>
        </ul>

        <p>Die negative Steigung zeigt das Gesetz der Nachfrage: Mit jeder zusätzlichen Einheit, die nachgefragt wird, sinkt der Preis, den Konsumenten bereit sind zu zahlen, um $b$ Euro.</p>

        <div class="cb cb-ex">
          <div class="cb-label">Beispiel</div>
          <div class="cb-title">Buchmarkt</div>
          <p>Betrachten wir den Markt für ein populäres Buch. Die Nachfragefunktion lautet:</p>
          <div class="math-block">$$f(x) = -\frac{1}{2}x + 10$$</div>
          <p><strong>Prohibitivpreis:</strong> Bei $x = 0$ ist $p = 10€$. Niemand würde das Buch kaufen, wenn es 10 Euro kostet (dies ist ein hypothetisches Beispiel).</p>
          <p><strong>Marktsättigung:</strong> Bei $p = 0$ erhalten wir: $0 = -\frac{1}{2}x + 10$, also $x = 20$ Bücher. Wenn das Buch kostenlos wäre, würden 20 Menschen es haben wollen.</p>
          <p><strong>Nachfrage bei p = 6€:</strong> Setzen wir $p = 6$ ein:</p>
          <div class="math-block">$$6 = -\frac{1}{2}x + 10$$</div>
          <div class="math-block">$$-4 = -\frac{1}{2}x$$</div>
          <div class="math-block">$$x = 8$$</div>
          <p>Bei einem Preis von 6 Euro werden 8 Bücher nachgefragt.</p>
        </div>

        <h3>Umstellen der Nachfragefunktion</h3>
        <p>Oft ist es praktisch, die Nachfragefunktion nach $x$ umzustellen, um direkt zu sehen, wie viel bei einem gegebenen Preis nachgefragt wird:</p>

        <div class="math-block">
          $$p = a - b \cdot x \quad \Rightarrow \quad x = \frac{a - p}{b}$$
        </div>

        <p>Im Buchbeispiel:</p>
        <div class="math-block">
          $$x = \frac{10 - p}{0{,}5} = 20 - 2p$$
        </div>

        <p>Das bedeutet: Bei jeden Euro Preiserhöhung sinkt die nachgefragte Menge um 2 Bücher.</p>
      </section>

      <!-- AGGREGIERTE NACHFRAGE -->
      <section class="ch-section" id="sec-aggregiert">
        <h2>Aggregierte Marktnachfrage</h2>
        <p>Bisher haben wir die Nachfrage eines einzelnen Konsumenten betrachtet. In der Realität besteht der Markt aus vielen Konsumenten mit unterschiedlichen Nachfragefunktionen. Die <strong>aggregierte Marktnachfrage</strong> ist die Summe aller individuellen Nachfragemengen bei jedem gegebenen Preis – mit anderen Worten, die <strong>horizontale Summe</strong> aller individuellen Nachfragekurven.</p>

        <p>Um die aggregierte Nachfrage zu berechnen, gehen wir nach folgendem Verfahren vor:</p>

        <ul class="steps">
          <li>Stellen Sie jede individuelle Nachfragefunktion nach $x$ um (von $p = a - bx$ zu $x = \frac{a-p}{b}$)</li>
          <li>Addieren Sie die Mengen für jeden Preis, aber beachten Sie den Prohibitivpreis: Ist der Preis höher als der Prohibitivpreis eines Konsumenten, kauft dieser Konsument nichts</li>
          <li>Schreiben Sie die aggregierte Nachfragefunktion in Abschnitten auf, falls verschiedene Konsumenten unterschiedliche Prohibitivpreise haben</li>
        </ul>

        <div class="cb cb-ex">
          <div class="cb-label">Beispiel</div>
          <div class="cb-title">Aggregierte Nachfrage: Zwei Konsumenten</div>
          <p>Betrachten wir zwei Konsumenten auf dem Energydrink-Markt:</p>
          <p><strong>Konsument 1:</strong> $p_1 = -2x_1 + 12$, also $x_1 = \frac{12-p}{2}$ (Prohibitivpreis: 12€)</p>
          <p><strong>Konsument 2:</strong> $p_2 = -x_2 + 8$, also $x_2 = 8-p$ (Prohibitivpreis: 8€)</p>

          <p><strong>Für $8 < p \leq 12$ (nur Konsument 1 kauft):</strong></p>
          <div class="math-block">
            $$X = \frac{12-p}{2}$$
          </div>

          <p><strong>Für $p \leq 8$ (beide kaufen):</strong></p>
          <div class="math-block">
            $$X = \frac{12-p}{2} + (8-p) = \frac{12-p}{2} + \frac{2(8-p)}{2} = \frac{12-p+16-2p}{2} = \frac{28-3p}{2}$$
          </div>

          <p><strong>Konkrete Werte:</strong></p>
          <ul>
            <li>Bei $p = 2€$: $X = \frac{28-6}{2} = 11$ Dosen</li>
            <li>Bei $p = 6€$: $X = \frac{28-18}{2} = 5$ Dosen</li>
            <li>Bei $p = 10€$: $X = \frac{12-10}{2} = 1$ Dose (nur Konsument 1)</li>
          </ul>
        </div>
      </section>

      <!-- VERSCHIEBUNG DER NACHFRAGEKURVE -->
      <section class="ch-section" id="sec-verschiebung">
        <h2>Verschiebung der Nachfragekurve</h2>
        <p>Es ist wichtig, zwischen zwei verschiedenen Konzepten zu unterscheiden:</p>
        <ul>
          <li><strong>Bewegung entlang der Kurve:</strong> Dies tritt auf, wenn sich der Preis des Gutes selbst ändert. Die nachgefragte Menge ändert sich, aber die Nachfragekurve selbst bleibt gleich.</li>
          <li><strong>Verschiebung der Kurve:</strong> Dies tritt auf, wenn sich die gesamte Nachfragekurve verändert – also wenn die Nachfragemenge bei jedem gegebenen Preis anders ist. Dies geschieht durch externe Faktoren, nicht durch Preisänderungen des Gutes selbst.</li>
        </ul>

        <p>Diese Unterscheidung ist fundamental für ökonomische Analysen. Nur Preisänderungen des Gutes führen zu Bewegungen entlang der Kurve. Alles andere führt zu Verschiebungen.</p>

        <div class="cb cb-def">
          <div class="cb-label">Definition</div>
          <div class="cb-title">Fünf Faktoren der Nachfrageverschiebung</div>
          <p><strong>1. Einkommen:</strong> Ein Anstieg des Einkommens führt normalerweise zu einer erhöhten Nachfrage nach normalen Gütern und einer geringeren Nachfrage nach inferioren Gütern. Die Kurve verschiebt sich nach rechts (für normale Güter).</p>
          <p><strong>2. Präferenzen:</strong> Veränderte Vorlieben und Geschmäcke der Konsumenten verschieben die Nachfragekurve. Beispiele sind Mode, Trends, kulturelle Entwicklungen oder gesundheitliche Trends (z.B. wachsendes Bewusstsein für Nachhaltigkeit).</p>
          <p><strong>3. Verwandte Güter:</strong> Der Preis anderer Güter beeinflusst die Nachfrage nach dem betrachteten Gut. Es gibt zwei Arten: <strong>Substitutionsgüter</strong> (Güter, die sich gegenseitig ersetzen) und <strong>Komplementärgüter</strong> (Güter, die zusammen verwendet werden).</p>
          <p><strong>4. Bevölkerung:</strong> Ein Anstieg der Bevölkerung führt zu einer erhöhten Marktnachfrage. Die Nachfragekurve verschiebt sich nach rechts.</p>
          <p><strong>5. Erwartungen:</strong> Erwartungen über zukünftige Preise, Einkommen oder Verfügbarkeit beeinflussen heutige Nachfragentscheidungen. Wenn Konsumenten eine Preiserhöhung erwarten, kaufen sie heute mehr und verschieben die Nachfrage nach rechts.</p>
        </div>

        <h3>Substitutions- und Komplementärgüter</h3>
        <p><strong>Substitutionsgüter</strong> sind Güter, die sich gegenseitig ersetzen können. Sie erfüllen einen ähnlichen Zweck oder erfüllen dasselbe Bedürfnis. Beispiele:</p>
        <ul>
          <li>Butter und Margarine</li>
          <li>Cola und Pepsi</li>
          <li>Auto und öffentliche Verkehrsmittel</li>
          <li>Kaffee und Tee</li>
        </ul>
        <p>Wenn der Preis für Cola steigt, switchen Konsumenten zu Pepsi, und die Nachfrage nach Pepsi steigt (nach rechts). Die Nachfragekurve für Pepsi verschiebt sich nach rechts.</p>

        <p><strong>Komplementärgüter</strong> sind Güter, die zusammen verwendet werden oder sich gegenseitig ergänzen. Das Konsum eines Gutes erhöht die Nachfrage nach dem anderen. Beispiele:</p>
        <ul>
          <li>Auto und Benzin</li>
          <li>Drucker und Druckerpatronen</li>
          <li>Kaffee und Zucker</li>
          <li>Ski und Skistiefel</li>
        </ul>
        <p>Wenn der Preis für Drucker sinkt, kaufen mehr Menschen Drucker, und daher steigt auch die Nachfrage nach Druckerpatronen (nach rechts). Die Nachfragekurve für Druckerpatronen verschiebt sich nach rechts.</p>
      </section>

      <!-- ZUSAMMENFASSUNG -->
      <section class="ch-section" id="sec-zusammenfassung">
        <h2>Zusammenfassung</h2>
        <div class="cb cb-note">
          <div class="cb-label">Kernpunkte</div>
          <p><strong>Die Nachfragekurve</strong> zeigt das inverse Verhältnis zwischen Preis und nachgefragter Menge. Sie fällt nach rechts mit negativer Steigung.</p>
          <p><strong>Das Gesetz der Nachfrage</strong> besagt, dass höhere Preise zu niedrigerer Nachfrage führen und umgekehrt.</p>
          <p><strong>Die Nachfragefunktion</strong> lautet in linearer Form $p = a - bx$, wobei $a$ der Prohibitivpreis und $b$ die (absolute) Steigung ist.</p>
          <p><strong>Der Prohibitivpreis</strong> ist der Preis, bei dem die Nachfrage auf null sinkt. Die <strong>Marktsättigung</strong> ist die Menge, die bei Preis null nachgefragt wird.</p>
          <p><strong>Aggregierte Nachfrage</strong> ist die Summe aller individuellen Nachfragen. Man summiert die Mengen horizontal für jeden Preis.</p>
          <p><strong>Bewegung entlang der Kurve</strong> entsteht durch Preisänderungen des Gutes selbst. <strong>Verschiebung der Kurve</strong> entsteht durch externe Faktoren: Einkommen, Präferenzen, verwandte Güter, Bevölkerung, Erwartungen.</p>
          <p><strong>Substitutionsgüter</strong> ersetzen sich gegenseitig, daher steigt ihre Nachfrage, wenn der Konkurrenzpreis steigt. <strong>Komplementärgüter</strong> werden zusammen verwendet, daher sinkt ihre Nachfrage, wenn der Preis des Komplementärsgutes steigt.</p>
        </div>
      </section>

      <!-- ÜBUNGSAUFGABEN -->
      <section class="ch-section" id="sec-aufgaben">
        <h2>Übungsaufgaben</h2>

        <h3>Aufgabe 1: Nachfragefunktion für Kopfhörer</h3>
        <p>Der Prohibitivpreis für Kopfhörer liegt bei 80€. Bei einem Preis von 0€ würden 160 Stück nachgefragt.</p>
        <p><strong>Fragen:</strong></p>
        <ol>
          <li>Stellen Sie die Nachfragefunktion auf.</li>
          <li>Wie viele Kopfhörer werden bei p = 30€ nachgefragt?</li>
        </ol>
        <p><strong>Lösung:</strong></p>
        <p>Wir haben zwei Punkte: (0, 80) und (160, 0).</p>
        <p>Steigung: $b = \frac{\Delta p}{\Delta x} = \frac{0 - 80}{160 - 0} = \frac{-80}{160} = -\frac{1}{2}$</p>
        <p>Nachfragefunktion:</p>
        <div class="math-block">
          $$p = 80 - \frac{1}{2}x \quad \text{oder} \quad f(x) = -\frac{1}{2}x + 80$$
        </div>
        <p>Bei p = 30€:</p>
        <div class="math-block">
          $$30 = -\frac{1}{2}x + 80$$
        </div>
        <div class="math-block">
          $$-50 = -\frac{1}{2}x$$
        </div>
        <div class="math-block">
          $$x = 100 \text{ Stück}$$
        </div>
        <p>Bei einem Preis von 30€ werden 100 Kopfhörer nachgefragt.</p>

        <h3>Aufgabe 2: Aggregierte Nachfrage für Energydrinks</h3>
        <p>Auf dem Markt für Energydrinks gibt es zwei Studenten mit folgenden Nachfragefunktionen:</p>
        <ul>
          <li>Student A: $p_A = -x_A + 5$</li>
          <li>Student B: $p_B = -2x_B + 6$</li>
        </ul>
        <p><strong>Fragen:</strong></p>
        <ol>
          <li>Berechnen Sie die aggregierte Marktnachfrage als Funktion vom Preis.</li>
          <li>Wie viel wird insgesamt bei p = 3€ nachgefragt?</li>
        </ol>
        <p><strong>Lösung:</strong></p>
        <p>Zunächst stellen wir nach x um:</p>
        <p>$x_A = 5 - p$ für $p \leq 5$ (Prohibitivpreis: 5€)</p>
        <p>$x_B = \frac{6-p}{2}$ für $p \leq 6$ (Prohibitivpreis: 6€)</p>

        <p><strong>Für $5 < p \leq 6$:</strong> Nur Student B kauft</p>
        <div class="math-block">
          $$X = \frac{6-p}{2}$$
        </div>

        <p><strong>Für $p \leq 5$:</strong> Beide Studenten kaufen</p>
        <div class="math-block">
          $$X = (5-p) + \frac{6-p}{2} = \frac{2(5-p)}{2} + \frac{6-p}{2} = \frac{10-2p+6-p}{2} = \frac{16-3p}{2}$$
        </div>

        <p>Bei p = 3€ (liegt im Bereich $p \leq 5$):</p>
        <div class="math-block">
          $$X = \frac{16-3(3)}{2} = \frac{16-9}{2} = \frac{7}{2} = 3{,}5 \text{ Einheiten}$$
        </div>

        <h3>Aufgabe 3: Verschiebung der Nachfragekurve für E-Bikes</h3>
        <p>Erklären Sie, in welche Richtung sich die Nachfragekurve für E-Bikes verschiebt, wenn:</p>
        <ol>
          <li>Das Einkommen der Bevölkerung steigt</li>
          <li>Der Preis für Benzin stark steigt</li>
          <li>Ein neuer Trend zu Fitness und Umweltbewusstsein entsteht</li>
        </ol>
        <p><strong>Lösung:</strong></p>
        <ol>
          <li><strong>Einkommen steigt:</strong> E-Bikes sind für viele Menschen ein superiores Gut – sie kaufen mehr davon, wenn sie mehr Geld haben. Die Nachfragekurve verschiebt sich nach <strong>rechts</strong>.</li>
          <li><strong>Benzinpreis steigt:</strong> Auto fahren wird teurer. E-Bikes sind ein Substitutionsgut zu Autos (beides sind Transportmittel). Wenn das Substitut (Auto) teurer wird, steigt die Nachfrage nach E-Bikes. Die Kurve verschiebt sich nach <strong>rechts</strong>.</li>
          <li><strong>Neuer Trend:</strong> Ein Trend zu Fitness und Nachhaltigkeit verändert die Präferenzen der Menschen. Sie präferieren E-Bikes nun stärker als vorher. Die Nachfragekurve verschiebt sich nach <strong>rechts</strong>.</li>
        </ol>

        <h3>Aufgabe 4: Smartphone-Markt (komplexes Anwendungsbeispiel)</h3>
        <p>Der Smartphone-Markt in einem Land weist folgende Eigenschaften auf: Der Prohibitivpreis liegt bei 1.200€ und die Sättigungsmenge beträgt 600 Einheiten.</p>
        <p><strong>Fragen:</strong></p>
        <ol>
          <li>Stellen Sie die Nachfragefunktion auf.</li>
          <li>Bei welchem Preis werden 300 Smartphones nachgefragt?</li>
          <li>Wie verändert sich die Nachfrage, wenn ein neues, günstiges Konkurrenzprodukt auf den Markt kommt?</li>
        </ol>
        <p><strong>Lösung:</strong></p>
        <p>Gegeben: Prohibitivpreis = 1.200€ (Punkt (0, 1200)), Sättigungsmenge = 600 (Punkt (600, 0))</p>
        <p>Steigung: $b = \frac{0 - 1200}{600 - 0} = \frac{-1200}{600} = -2$</p>
        <p><strong>1. Nachfragefunktion:</strong></p>
        <div class="math-block">
          $$p = -2x + 1200 \quad \text{oder} \quad f(x) = -2x + 1200$$
        </div>

        <p><strong>2. Preis bei x = 300:</strong></p>
        <div class="math-block">
          $$p = -2(300) + 1200 = -600 + 1200 = 600€$$
        </div>
        <p>Bei einem Preis von 600€ werden 300 Smartphones nachgefragt.</p>

        <p><strong>3. Konkurrenzprodukt günstiger:</strong> Ein günstiges Konkurrenzprodukt ist ein Substitutionsgut. Wenn sein Preis sinkt (und damit Smartphones teurer erscheinen im Vergleich), sinkt die Nachfrage nach Smartphones. Die Nachfragekurve verschiebt sich nach <strong>links</strong>. Bei jedem gegebenen Preis werden nun weniger Smartphones nachgefragt als vorher.</p>
      </section>
    </div>

    <!-- NAVIGATION -->
    <div class="ch-nav">
      <a href="/learn/angebotskurve/">← Angebotskurve</a>
      <a href="/learn/vwl/" class="primary">Zurück zur VWL-Übersicht →</a>
    </div>
  </div>

  <!-- SIDEBAR TABLE OF CONTENTS -->
  <aside class="ch-toc">
    <div class="ch-toc-title">In diesem Kapitel</div>
    <ul>
      <li><a href="#sec-ueberblick">Überblick</a></li>
      <li><a href="#sec-gesetz">Gesetz der Nachfrage</a></li>
      <li><a href="#sec-nachfragefunktion">Nachfragefunktion</a></li>
      <li><a href="#sec-aggregiert">Aggregierte Nachfrage</a></li>
      <li><a href="#sec-verschiebung">Verschiebung der Kurve</a></li>
      <li><a href="#sec-zusammenfassung">Zusammenfassung</a></li>
      <li><a href="#sec-aufgaben">Übungsaufgaben</a></li>
    </ul>
  </aside>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const tocLinks = document.querySelectorAll('.ch-toc a');
  const sections = document.querySelectorAll('.ch-section');

  function updateActiveLink() {
    let currentSection = '';

    sections.forEach(section => {
      const sectionTop = section.offsetTop;
      const sectionHeight = section.offsetHeight;
      if (window.scrollY >= sectionTop - 150 && window.scrollY < sectionTop + sectionHeight) {
        currentSection = section.getAttribute('id');
      }
    });

    tocLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href') === `#${currentSection}`) {
        link.classList.add('active');
      }
    });
  }

  window.addEventListener('scroll', updateActiveLink);
  updateActiveLink();
});
</script>
