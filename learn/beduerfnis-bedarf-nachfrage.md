---
layout: page
title:
permalink: /learn/beduerfnis-bedarf-nachfrage/
---

<style>
:root{--math:#c45c3e;--econ:#c49a6c;--geo:#c49a6c;--sumi:#1a1a18;--kuro:#2c2c28;--hai:#3d3d38;--kinari:#f0ece4;--shiro:#f7f5f0;--kinu:#e8e3d8;--ishi:#b8b3a8;--sugi:#8a8578;--beni:#c45c3e;--matcha:#7a8c6e;--ai:#5b7a8c;--kitsune:#c49a6c;--sakura:#c4868a;--bg-primary:#f7f5f0;--bg-secondary:#f0ece4;--bg-tertiary:#e8e3d8;--text-primary:#1a1a18;--text-secondary:#8a8578;--text-tertiary:#b8b3a8;--separator:rgba(26,26,24,0.08);--font-stack:'DM Sans','Noto Sans JP',-apple-system,BlinkMacSystemFont,sans-serif;--space-1:4px;--space-2:8px;--space-3:12px;--space-4:16px;--space-5:20px;--space-6:24px;--space-8:32px;--space-10:40px;--space-12:48px;--space-16:64px;--radius-sm:8px;--radius-md:12px;--radius-lg:16px;--radius-xl:20px;--radius-2xl:24px;--radius-full:9999px;--transition-base:250ms cubic-bezier(0.4,0,0.2,1);}
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
.ch-eyebrow{display:inline-flex;align-items:center;gap:6px;font-size:12px;font-weight:600;text-transform:uppercase;letter-spacing:.08em;color:var(--econ);background:rgba(196,154,108,.1);border:1px solid rgba(196,154,108,.2);border-radius:var(--radius-full);padding:3px 10px;margin-bottom:var(--space-4);}
.ch-header h1{font-size:clamp(28px,4vw,42px);font-weight:300;font-family:'Cormorant Garamond','Noto Serif JP',Georgia,serif;letter-spacing:-.025em;line-height:1.08;margin-bottom:var(--space-3);}
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
.cb-def{background:rgba(91,122,140,.1);border-color:var(--ai);}.cb-def .cb-label{color:var(--ai);}
.cb-ex{background:rgba(122,140,110,.08);border-color:var(--matcha);}.cb-ex .cb-label{color:var(--matcha);}
.cb-task{background:rgba(196,154,108,.08);border-color:var(--kitsune);}.cb-task .cb-label{color:var(--kitsune);}
.cb-note{background:rgba(196,154,108,.08);border-color:var(--econ);}.cb-note .cb-label{color:var(--econ);}
.cb-tip{background:rgba(175,82,222,.08);border-color:var(--sakura);}.cb-tip .cb-label{color:var(--sakura);}
.math-block{background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-md);padding:var(--space-5) var(--space-6);margin:var(--space-4) 0;overflow-x:auto;text-align:center;font-size:1.05em;}
.steps{list-style:none;padding:0;margin:var(--space-3) 0;counter-reset:step;}
.steps li{counter-increment:step;display:flex;gap:var(--space-3);margin-bottom:var(--space-4);font-size:15px;color:var(--text-secondary);line-height:1.65;}
.steps li::before{content:counter(step);min-width:24px;height:24px;border-radius:50%;background:rgba(196,154,108,.15);color:var(--econ);font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px;}
.ch-toc{position:sticky;top:80px;background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-xl);padding:var(--space-5);}
.ch-toc-title{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--text-tertiary);margin-bottom:var(--space-4);}
.ch-toc ul{list-style:none;padding:0;}.ch-toc li{margin-bottom:var(--space-1);}
.ch-toc a{font-size:13px;color:var(--text-tertiary);text-decoration:none;display:block;padding:4px 8px;border-radius:var(--radius-sm);transition:all var(--transition-base);}
.ch-toc a:hover{color:var(--text-primary);background:var(--bg-tertiary);}.ch-toc a.active{color:var(--econ);background:rgba(196,154,108,.1);}
.ch-nav{margin-top:var(--space-12);padding-top:var(--space-8);border-top:1px solid var(--separator);display:flex;justify-content:space-between;align-items:center;gap:var(--space-4);flex-wrap:wrap;}
.ch-nav a{display:inline-flex;align-items:center;gap:var(--space-2);font-size:14px;font-weight:500;color:var(--text-tertiary);text-decoration:none;padding:var(--space-3) var(--space-4);border:1px solid var(--separator);border-radius:var(--radius-md);transition:all var(--transition-base);}
.ch-nav a:hover{color:var(--text-primary);border-color:rgba(var(--text-rgb),0.15);background:var(--bg-secondary);}
.ch-nav a.primary{color:var(--econ);border-color:rgba(196,154,108,.3);background:rgba(196,154,108,.05);}
.ch-nav a.primary:hover{background:rgba(196,154,108,.12);}
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
    <a href="/learn/vwl/">VWL</a><span class="ch-breadcrumb-sep">›</span>
    <span>Bedürfnis, Bedarf & Nachfrage</span>
  </div>

  <div class="ch-header">
    <div class="ch-eyebrow">VWL · Kapitel 1</div>
    <h1>Bedürfnis, Bedarf und Nachfrage in der Wirtschaft</h1>
    <div class="ch-header-meta">
      <span>ca. 15 min</span><span>·</span>
      <span>Grundlagen · Bedürfnisarten · Maslowsche Pyramide</span>
    </div>
  </div>

  <div class="ch-section" id="sec-ueberblick">
    <h2>Überblick – Die drei Grundkonzepte</h2>
    <p>Die Volkswirtschaftslehre (VWL) befasst sich mit der Frage, wie knappe Ressourcen optimal genutzt werden. Um diese Problematik zu verstehen, müssen wir zunächst drei zentrale Begriffe klären, die eng miteinander verflochten sind: <strong>Bedürfnis</strong>, <strong>Bedarf</strong> und <strong>Nachfrage</strong>. Diese drei Konzepte bilden eine logische Kette, die von der inneren Empfindung bis zur tatsächlichen Marktentscheidung führt.</p>

    <p>Jedes wirtschaftliche Handeln beginnt mit einem Bedürfnis. Menschen haben unbegrenzte Wünsche und Verlangen, die ihr Verhalten prägen. Doch nicht jedes Bedürfnis kann in einen konkreten Kauf umgewandelt werden – hier kommt die finanzielle Leistungsfähigkeit ins Spiel. Der Übergang von einem Wunsch zu einem realistischen Plan und schließlich zu einer konkreten Kaufentscheidung wird durch diese drei Begriffe beschrieben.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Die Kette: Bedürfnis → Bedarf → Nachfrage</div>
      <ul style="margin:var(--space-3) 0 0 var(--space-5);list-style:none;padding:0;">
        <li style="margin-bottom:var(--space-3);"><strong>Bedürfnis:</strong> Ein empfundener Mangel, der das Verlangen weckt, ihn zu beseitigen. Bedürfnisse sind universal und subjektiv.</li>
        <li style="margin-bottom:var(--space-3);"><strong>Bedarf:</strong> Ein konkretes Bedürfnis, das durch verfügbare finanzielle Mittel (Kaufkraft) realisierbar ist. Bedarf ist das „finanzierbare Bedürfnis".</li>
        <li><strong>Nachfrage:</strong> Die tatsächliche Kaufabsicht auf dem Markt. Sie ist das konkrete Angebot, das ein Käufer an einen Verkäufer richtet und ist beobachtbar, messbar und statistisch erfassbar.</li>
      </ul>
    </div>

    <p>Diese drei Konzepte zu unterscheiden ist für das Verständnis der Marktwirtschaft entscheidend. Ein Person kann unbegrenzte Bedürfnisse haben, aber nur ein begrenztes Einkommen. Daher wird nur ein Teil der Bedürfnisse zu Bedarf, und wiederum nur ein Teil des Bedarfs wird tatsächlich in Nachfrage umgewandelt.</p>
  </div>

  <div class="ch-section" id="sec-beduerfnis">
    <h2>Was ist ein Bedürfnis?</h2>
    <p>Ein <strong>Bedürfnis</strong> ist das Gefühl eines Mangels und der daraus resultierende Wunsch, diesen Mangel zu beheben. Es ist eine subjektive, emotionale Empfindung, die jeder Mensch unterschiedlich wahrnimmt. Bedürfnisse entstehen aus physischen oder psychologischen Zuständen heraus und motivieren Menschen zu handeln.</p>

    <p>Bedürfnisse sind von Natur aus <strong>unbegrenzt</strong>. Ein Mensch kann niemals alle möglichen Bedürfnisse befriedigen – wenn eine Bedürfnis erfüllt ist, entsteht unmittelbar das nächste. Dies ist ein zentrales Problem der Wirtschaft: Während Bedürfnisse endlos sind, sind Güter und Ressourcen begrenzt. Diese grundlegende Knappheit ist die Motivation für wirtschaftliches Handeln.</p>

    <h3>Entstehung von Bedürfnissen</h3>
    <p>Bedürfnisse entstehen durch verschiedene innere und äußere Einflussfaktoren:</p>
    <ul>
      <li><strong>Physische Zustände:</strong> Hunger, Durst, Müdigkeit, Kälte – diese sind biologische Signale des Körpers</li>
      <li><strong>Psychologische Zustände:</strong> Das Verlangen nach Sicherheit, Anerkennung, Zugehörigkeit oder Selbstverwirklichung</li>
      <li><strong>Soziale Einflüsse:</strong> Modetrends, kulturelle Normen und der Druck, im sozialen Umfeld mithalten zu können</li>
      <li><strong>Werbung und Marketing:</strong> Geschickte Vermarktung kann Bedürfnisse wecken oder verstärken, die vorher nicht bewusst waren</li>
    </ul>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiele</div>
      <div class="cb-title">Entstehung von Bedürfnissen</div>
      <p><strong>Physisches Bedürfnis:</strong> Nach einem anstrengenden Trainingstag verspürt eine Person Müdigkeit und Durst. Das Bedürfnis nach Schlaf und Flüssigkeit wird unmittelbar bewusst.</p>
      <p><strong>Soziales Bedürfnis:</strong> Ein Jugendlicher sieht, dass Klassenkameraden ein bestimmtes Smartphone-Modell haben. Obwohl das alte Telefon noch funktioniert, entsteht das Bedürfnis nach demselben Modell aus sozialen Gründen.</p>
      <p><strong>Durch Werbung gewecktes Bedürfnis:</strong> Eine Person sieht eine Anzeige für einen neuen Sportwagen mit eleganten Features. Plötzlich entwickelt sich der Wunsch nach diesem Auto, obwohl vorher kein bewusster Mangel empfunden wurde.</p>
    </div>

    <h3>Merkmale von Bedürfnissen</h3>
    <p>Bedürfnisse haben mehrere charakteristische Merkmale, die sie prägen:</p>
    <ul>
      <li><strong>Subjektivität:</strong> Jeder Mensch empfindet Bedürfnisse unterschiedlich – was für eine Person wichtig ist, kann für eine andere unwichtig sein</li>
      <li><strong>Unbegrenztheit:</strong> Menschliche Bedürfnisse sind praktisch unbegrenzt; es gibt immer noch ein weiteres Bedürfnis zu befriedigen</li>
      <li><strong>Wiederholbarkeit:</strong> Viele Bedürfnisse treten regelmäßig auf (täglich Hunger, wöchentlich Unterhaltung)</li>
      <li><strong>Entwicklung:</strong> Bedürfnisse verändern sich mit dem Alter, der Lebenssituation und den Erfahrungen</li>
    </ul>
  </div>

  <div class="ch-section" id="sec-beduerfnisarten">
    <h2>Arten von Bedürfnissen</h2>
    <p>Bedürfnisse lassen sich nach verschiedenen Kriterien kategorisieren. Diese Unterscheidungen helfen, die Vielfalt menschlicher Wünsche besser zu verstehen und zu analysieren.</p>

    <h3>Existenzbedürfnisse, Kulturbedürfnisse und Luxusbedürfnisse</h3>
    <p>Eine häufige Klassifizierung unterscheidet Bedürfnisse nach ihrer Notwendigkeit für die menschliche Existenz:</p>

    <div class="cb cb-def">
      <div class="cb-label">Klassifizierung</div>
      <p><strong>Existenzbedürfnisse (notwendige Bedürfnisse):</strong> Dies sind die absolut notwendigen Güter und Dienstleistungen für das Überleben und die grundlegendste Gesundheit. Dazu gehören Nahrung, Wasser, Wohnraum, Kleidung und medizinische Grundversorgung. Ein Mensch kann ohne die Befriedigung dieser Bedürfnisse nicht überleben.</p>
      <p><strong>Kulturbedürfnisse (Wahlbedürfnisse):</strong> Diese sind nicht lebensnotwendig, aber gehören zu einer anständigen und würdevollen Lebensweise in einer Gesellschaft. Sie umfassen Bildung, Kultur, Unterhaltung, soziale Kontakte und persönliche Hygiene über das Minimum hinaus. Die genaue Definition ist kulturabhängig und variiert zwischen Gesellschaften.</p>
      <p><strong>Luxusbedürfnisse:</strong> Dies sind Güter und Dienstleistungen, die über das notwendige und gewöhnliche Maß hinausgehen. Sie dienen der Repräsentation, dem Vergnügen und der Befriedigung von Status-Wünschen. Beispiele: Schmuck, teure Sportautos, Luxusreisen oder exklusive Clubs. Diese Bedürfnisse treten erst bei höherem Einkommen auf.</p>
    </div>

    <h3>Individualbedürfnisse und Kollektivbedürfnisse</h3>
    <p>Bedürfnisse können auch danach unterschieden werden, ob sie von Einzelpersonen oder von Gruppen ausgehen:</p>

    <ul>
      <li><strong>Individualbedürfnisse:</strong> Bedürfnisse einer einzelnen Person, die sie privat befriedigen möchte (z.B. Essen, Kleidung, Hobby). Diese werden typischerweise auf dem privaten Markt gekauft.</li>
      <li><strong>Kollektivbedürfnisse (Gemeinschaftsbedürfnisse):</strong> Bedürfnisse, die von einer Gemeinschaft gemeinsam befriedigt werden müssen oder können. Beispiele sind öffentliche Sicherheit (Polizei), Verteidigung, Infrastruktur (Straßen, öffentliche Verkehrsmittel) oder Bildung. Diese werden oft vom Staat bereitgestellt und über Steuern finanziert.</li>
    </ul>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Unterscheidung der Bedürfnisarten</div>
      <p><strong>Ein Student betrachtet sein Leben:</strong></p>
      <ul style="margin:var(--space-3) 0 0 var(--space-5);">
        <li><strong>Existenzbedürfnis:</strong> Nahrung, Unterkunft in einem Studentenwohnheim</li>
        <li><strong>Kulturbedürfnis:</strong> Universität und Vorlesungen (Bildung), Kino oder Konzerte mit Freunden</li>
        <li><strong>Luxusbedürfnis:</strong> Ein neues High-End-Gaming-Notebook mit RTX 4090 Grafikkarte</li>
        <li><strong>Individualbedürfnis:</strong> Der Student möchte ein eigenes Buch zum Lernen kaufen</li>
        <li><strong>Kollektivbedürfnis:</strong> Der Student nutzt öffentliche Straßen, öffentliche Bibliotheken und öffentliche Verkehrsmittel</li>
      </ul>
    </div>
  </div>

  <div class="ch-section" id="sec-maslow">
    <h2>Die Maslowsche Bedürfnispyramide</h2>
    <p>Der amerikanische Psychologe Abraham Maslow entwickelte 1943 die berühmte <strong>Bedürfnispyramide</strong>, die menschliche Bedürfnisse hierarchisch ordnet. Sein Modell besagt, dass Menschen ihre Bedürfnisse in einer bestimmten Reihenfolge befriedigen: Erst wenn eine Kategorie von Bedürfnissen weitgehend erfüllt ist, wendet man sich der nächsthöheren Stufe zu. Dieses Modell ist auch für die Ökonomie wertvoll, da es erklärt, warum Menschen ihre Ausgaben unterschiedlich priorisieren.</p>

    <h3>Die fünf Stufen nach Maslow</h3>

    <div class="cb cb-def">
      <div class="cb-label">Pyramide</div>
      <p><strong>1. Physiologische Bedürfnisse (Basis):</strong> Die fundamentalsten biologischen Bedürfnisse wie Hunger, Durst, Schlaf, Atemluft und Fortpflanzung. Ohne diese zu befriedigen, kann ein Mensch nicht leben. Menschen konzentrieren all ihre Energie auf diese Bedürfnisse, wenn sie nicht erfüllt sind (z.B. in Krisenzeiten oder extremer Armut).</p>

      <p><strong>2. Sicherheitsbedürfnisse:</strong> Das Verlangen nach Schutz, Stabilität, Ordnung und Sicherheit. Dazu gehören Schutz vor Gefahren, finanzielle Sicherheit (stabiles Einkommen), Versicherungen und ein stabiles Zuhause. Menschen mit ungefestigtem Einkommen oder unsicherer Wohnlage konzentrieren ihre Ausgaben stark auf diese Kategorie.</p>

      <p><strong>3. Soziale Bedürfnisse (Zugehörigkeit):</strong> Das Bedürfnis nach Zugehörigkeit, Liebe, Freundschaft und sozialer Anerkennung. Menschen wollen Teil einer Gruppe sein, sich verstanden fühlen und sich von anderen Menschen wertgeschätzt wissen. Dies erklärt viele Konsumentscheidungen (trendige Kleidung, bestimmte Clubs beitreten).</p>

      <p><strong>4. Wertschätzungs- und Anerkennungsbedürfnisse:</strong> Das Streben nach Anerkennung, Status, Prestige und Selbstvertrauen. Menschen möchten von anderen respektiert werden und selbst ein positives Selbstbild haben. Dies führt zu Ausgaben für Statussymbole, teure Marken und repräsentative Güter.</p>

      <p><strong>5. Selbstverwirklichungsbedürfnisse (Spitze):</strong> Das Streben, das volle Potenzial auszuschöpfen und persönliche Ziele zu erreichen. Dies könnte bedeuten, eine Karriere im Traumberuf zu verfolgen, kreativ zu sein oder persönliche Fähigkeiten zu entwickeln. Dies tritt typically erst bei höherem Einkommen auf.</p>
    </div>

    <h3>Bedeutung für die Wirtschaft</h3>
    <p>Maslows Pyramide erklärt wichtige wirtschaftliche Phänomene:</p>
    <ul>
      <li><strong>Unterschiedliche Konsummuster:</strong> Arme Menschen geben die meisten Ausgaben für Nahrung und Wohnung aus (Stufe 1-2), während wohlhabende Menschen auch in Luxus und persönliche Entwicklung investieren (Stufe 4-5).</li>
      <li><strong>Elastizität der Nachfrage:</strong> Bedürfnisse der unteren Stufen sind relativ unelastisch (man kann Essen nicht einfach reduzieren), während Luxusbedürfnisse sehr elastisch sind (bei Rezession wird zuerst an Luxus gespart).</li>
      <li><strong>Marketingpsychologie:</strong> Unternehmen versuchen, ihre Produkte mit höheren Bedürfnisstufen zu verbinden (z.B. wird ein Auto nicht nur als Transportmittel verkauft, sondern auch als Statussymbol und Ausdruck von Freiheit).</li>
    </ul>

    <div class="cb cb-note">
      <div class="cb-label">Wichtig</div>
      <p>Maslows Modell ist zwar hilfreich, aber nicht absolut. Menschen verhalten sich nicht immer streng nach dieser Hierarchie – manchmal opfern Menschen Sicherheit für Liebe oder soziale Anerkennung für kreative Selbstverwirklichung. Kulturelle Unterschiede spielen auch eine Rolle.</p>
    </div>
  </div>

  <div class="ch-section" id="sec-bedarf">
    <h2>Bedarf – Das finanzierbare Bedürfnis</h2>
    <p><strong>Bedarf</strong> ist das Bindeglied zwischen dem inneren Wunsch (Bedürfnis) und der tatsächlichen Marktentscheidung (Nachfrage). Während ein Bedürfnis universell und unbegrenzt ist, wird es zum Bedarf, wenn folgende zwei Bedingungen erfüllt sind:</p>

    <ol style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
      <li><strong>Ein konkretes Bedürfnis existiert:</strong> Es muss ein empfundener Mangel vorhanden sein.</li>
      <li><strong>Finanzielle Mittel sind verfügbar:</strong> Die Person muss das Geld haben oder aufbringen können, um das Bedürfnis zu befriedigen.</li>
    </ol>

    <p>Der Begriff <strong>Kaufkraft</strong> ist zentral für das Verständnis von Bedarf. Kaufkraft ist das verfügbare Einkommen (oder verfügbare finanzielle Mittel) einer Person, die sie für Konsumausgaben verwenden kann. Bedarf ist daher nicht nur abhängig von Wünschen, sondern auch von der wirtschaftlichen Leistungsfähigkeit einer Person.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Bedarf und Kaufkraft</div>
      <p><strong>Bedarf = Bedürfnis + Kaufkraft</strong></p>
      <p>Ein Teenager hat vielleicht das Bedürfnis nach einem iPhone 15 Pro Max (1.500 €), aber ohne Ersparnisse oder Taschengeld hat er keinen Bedarf. Eine wohlhabende Person hat hingegen sowohl das Bedürfnis als auch die Kaufkraft – sie hat also Bedarf.</p>
      <p><strong>Kaufkraft</strong> ist das verfügbare Einkommen oder Vermögen, das eine Person für Konsum ausgeben kann. Sie wird durch Faktoren wie Löhne, Gehälter, Renteneinkommen, Ersparnisse und verfügbare Kredite bestimmt.</p>
    </div>

    <h3>Wie Bedarf entsteht</h3>
    <p>Das Verfahren ist relativ einfach: Eine Person verspürt zunächst ein Bedürfnis. Sie denkt dann: „Kann ich mir das leisten?" Wenn die Antwort „Ja" ist und die finanzielle Situation dies erlaubt, verwandelt sich das Bedürfnis in Bedarf. Die Person wird sich auf dem Markt umsehen, um diese Bedürfnis zu erfüllen.</p>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Vom Bedürfnis zum Bedarf</div>
      <p><strong>Szenario 1 – Schüler:</strong> Ein Schüler sieht die neue Gaming-Konsole PlayStation 5 (500 €). Das Bedürfnis ist da – jeder in der Klasse hat eine! Aber Taschengeld ist nur 20 € monatlich. Der Bedarf existiert nicht, da die Kaufkraft fehlt. Das Bedürfnis bleibt ein Wunsch.</p>
      <p><strong>Szenario 2 – Berufstätige:</strong> Eine Person arbeitet als Manager und verdient monatlich 4.000 €. Sie hat das Bedürfnis nach einem neuen Laptop (1.200 €). Da sie ein stabiles Einkommen hat und sich das Gerät leisten kann, existiert hier ein Bedarf. Sie werden vermutlich nach Angeboten suchen und einen kaufen.</p>
      <p><strong>Szenario 3 – Konjunkturkrise:</strong> Ein Arbeiter hatte zuvor ein Einkommen von 3.000 € und war in der Lage, sich regelmäßig neue Kleidung zu kaufen (Bedarf). Nach Jobverlust beträgt sein Einkommen jetzt 400 € Arbeitslosengeld. Der Bedarf nach neuer Kleidung verschwindet, obwohl das Bedürfnis eventuell noch vorhanden ist. Jetzt kann er sich nur noch das Notwendigste leisten.</p>
    </div>

    <h3>Bedarf und wirtschaftliche Stabilität</h3>
    <p>Die Menge des Bedarfs in einer Volkswirtschaft hängt stark von der wirtschaftlichen Situation ab. In Zeiten wirtschaftlichen Wachstums und hoher Beschäftigung steigt die durchschnittliche Kaufkraft der Bevölkerung, was zu höherem Bedarf führt. In Rezessionen oder Krisenzeiten sinkt die Kaufkraft, und der Bedarf konzentriert sich wieder auf Existenzbedürfnisse.</p>
  </div>

  <div class="ch-section" id="sec-nachfrage">
    <h2>Nachfrage – Die Marktentscheidung</h2>
    <p><strong>Nachfrage</strong> ist der letzte Schritt in der Kette Bedürfnis → Bedarf → Nachfrage. Sie beschreibt die tatsächliche <strong>Kaufabsicht</strong> eines Konsumenten gegenüber einem Anbieter – also wie viel von einem bestimmten Gut eine Person zu einem bestimmten Preis kaufen möchte oder auch tatsächlich kauft.</p>

    <p>Im Gegensatz zu Bedürfnis (subjektiv und oft verborgen) und Bedarf (theoretisch berechenbar), ist Nachfrage <strong>beobachtbar, messbar und statistisch erfassbar</strong>. Wirtschaftswissenschaftler können Nachfragestatistiken erheben, Trends analysieren und Vorhersagen treffen. Dies macht die Nachfrage zu einem der wichtigsten Konzepte in der VWL.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Nachfrage im ökonomischen Sinne</div>
      <p>Nachfrage ist die Bereitschaft und Fähigkeit eines Käufers, eine bestimmte Menge eines Gutes zu einem bestimmten Preis in einem definierten Zeitraum zu kaufen.</p>
      <p><strong>Nachfrage ≠ Bedarf:</strong> Eine Person kann Bedarf haben (finanzielle Mittel + Bedürfnis), entscheidet sich aber bewusst gegen den Kauf (zu teuer, bessere Alternative gefunden, impulsiv gekauft). Das ist kein Nachfrage.</p>
    </div>

    <h3>Von Bedarf zur Nachfrage</h3>
    <p>Nicht jeder Bedarf führt automatisch zu Nachfrage. Folgende Faktoren spielen eine Rolle:</p>

    <ul>
      <li><strong>Preis:</strong> Ein Produkt mag begehrt sein, aber wenn der Preis zu hoch ist, wird die Person es nicht kaufen (z.B. ein Auto für 100.000 €, das sich nur wenige leisten können).</li>
      <li><strong>Verfügbarkeit:</strong> Wenn das gewünschte Produkt nicht verfügbar ist (ausverkauft, nicht in der Nähe), kann Nachfrage nicht entstehen.</li>
      <li><strong>Substitutionsprodukte:</strong> Es gibt möglicherweise günstigere Alternativen, die den gleichen Zweck erfüllen. Ein Konsument kann Bedarf nach einem teuren Sportwagen haben, entscheidet sich aber für einen günstigen Honda.</li>
      <li><strong>Konsumentenpräferenzen:</strong> Persönliche Geschmäcker und Überzeugungen spielen eine Rolle. Jemand mit ethischen Bedenken mag Bedarf nach Produkten haben, die unter fragwürdigen Bedingungen hergestellt wurden, kauft aber bewusst nicht.</li>
      <li><strong>Dispositioneinkommen:</strong> Das verfügbare Einkommen nach Steuern und fixen Ausgaben. Wenn nach Miete und Lebensmitteln kein Geld mehr übrig ist, kann keine Nachfrage entstehen.</li>
    </ul>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Bedarf führt nicht immer zu Nachfrage</div>
      <p><strong>Familie mit 40.000 € Jahreseinkommen:</strong> Die Familie hat ein echtes Bedürfnis und Bedarf nach einem Auto (für Pendeln zur Arbeit). Allerdings:</p>
      <ul style="margin:var(--space-3) 0 0 var(--space-5);">
        <li>Der neue BMW 7er kostet 90.000 €. Das ist nicht leistbar → keine Nachfrage</li>
        <li>Ein 5 Jahre altes Hyundai i30 kostet 10.000 €. Das ist leistbar → Nachfrage entsteht</li>
        <li>Allerdings: Die Familie hat nur 8.000 € Ersparnisse. Sie können sich den Hyundai nicht leisten → keine aktuelle Nachfrage</li>
        <li>Wenn die Familie einen Kredit aufnimmt, kann die Nachfrage entstehen</li>
      </ul>
    </div>

    <h3>Die Nachfragekurve</h3>
    <p>In der Ökonomie wird Nachfrage oft als <strong>Nachfragekurve</strong> dargestellt, die die Beziehung zwischen Preis und Menge zeigt. Generell gilt das Gesetz der Nachfrage: <strong>Je höher der Preis, desto geringer die nachgefragte Menge</strong>, und umgekehrt. Dies ist intuitiv verständlich – bei höheren Preisen kaufen weniger Menschen das Produkt.</p>

    <div class="cb cb-note">
      <div class="cb-label">Hinweis</div>
      <p>Die Nachfragekurve und ihre Bewegungen (durch Preisänderungen vs. durch Änderung anderer Faktoren) werden in den nächsten Kapiteln detailliert behandelt.</p>
    </div>
  </div>

  <div class="ch-section" id="sec-oekonomisches-prinzip">
    <h2>Das ökonomische Prinzip</h2>
    <p>Das ökonomische Handeln basiert auf einem fundamentalen Konzept: <strong>Das ökonomische Prinzip</strong> (oder Rationalprinzip). Es beschreibt, wie Menschen und Unternehmen mit knappen Ressourcen unter Bedingungen der Knappheit umgehen.</p>

    <h3>Das Grundproblem: Knappheit</h3>
    <p>Die zentrale Erkenntnis der Ökonomie ist, dass die Ressourcen und Güter auf dieser Welt begrenzt sind, während die Bedürfnisse der Menschen unbegrenzt sind. Dies führt zu <strong>Knappheit</strong> – ein Zustand, in dem nicht genug Güter vorhanden sind, um alle Bedürfnisse zu befriedigen. Knappheit ist nicht subjektiv („Ich möchte mehr"), sondern objektiv und mathematisch:</p>

    <div class="cb cb-def">
      <div class="cb-label">Knappheit</div>
      <p>Knappheit existiert, wenn die verfügbare Menge eines Gutes kleiner ist als die nachgefragte Menge zum Preis von null (also wenn das Gut kostenlos wäre, würde man sich davon mehr nehmen).</p>
      <p><strong>Beispiel:</strong> Es gibt nur eine begrenzte Menge an Treibstoffen, Mineralien oder bebaubarem Land auf der Erde. Obwohl die Technologie sich verbessert, ändern sich die Grundlagen der Knappheit nicht.</p>
    </div>

    <h3>Minimalprinzip und Maximalprinzip</h3>
    <p>Um mit dieser Knappheit umzugehen, hat die Ökonomie zwei Ansätze identifiziert: das Minimalprinzip und das Maximalprinzip.</p>

    <div class="cb cb-def">
      <div class="cb-label">Definition</div>
      <div class="cb-title">Die zwei Formen des ökonomischen Prinzips</div>

      <p><strong>Minimalprinzip:</strong> Mit einem <strong>gegebenen Aufwand</strong> oder einer bestimmten Ressourcenmenge den <strong>maximalen Nutzen oder Ertrag</strong> erzielen.</p>
      <ul style="margin:var(--space-3) 0 var(--space-4) var(--space-5);list-style:none;padding:0;">
        <li><strong>Für Konsumenten:</strong> Mit dem verfügbaren Einkommen (z.B. 50 € Budget) möglichst viel Wert oder Nutzen bekommen.</li>
        <li><strong>Für Unternehmen:</strong> Mit gegebenen Produktionsmitteln (z.B. 100 Arbeitsstunden) möglichst viel produzieren oder verkaufen.</li>
      </ul>

      <p><strong>Maximalprinzip:</strong> Ein bestimmtes Ziel oder eine bestimmte Menge mit <strong>minimalem Aufwand oder Ressourceneinsatz</strong> erreichen.</p>
      <ul style="margin:var(--space-3) 0 0 var(--space-5);list-style:none;padding:0;">
        <li><strong>Für Konsumenten:</strong> Ein bestimmtes Produkt (z.B. ein spezifisches Buch) mit möglichst wenig Geld kaufen.</li>
        <li><strong>Für Unternehmen:</strong> Ein Produktionsziel (z.B. 1.000 Einheiten) mit möglichst wenigen Ressourcen oder Arbeitsstunden erreichen.</li>
      </ul>
    </div>

    <div class="cb cb-ex">
      <div class="cb-label">Beispiel</div>
      <div class="cb-title">Minimalprinzip vs. Maximalprinzip</div>
      <p><strong>Szenario: Ein Student plant eine Party.</strong></p>
      <p><strong>Minimalprinzip:</strong> Der Student hat 100 € Budget. Er möchte damit möglichst viel Spaß für sich und seine Gäste generieren. Er muss überlegen: Soll er teure Getränke kaufen oder eher günstige? Viele billige Snacks oder wenige hochwertige?</p>
      <p><strong>Maximalprinzip:</strong> Der Student hat das Ziel, 50 Leute auf die Party einzuladen. Er will dieses Ziel mit möglichst geringen Kosten erreichen. Er sucht nach Rabatten, günstigen Lokalen oder überredet einen Freund, Musik DJ zu spielen.</p>
    </div>

    <h3>Rationalität in der Ökonomie</h3>
    <p>Das ökonomische Prinzip setzt voraus, dass Menschen <strong>rational</strong> handeln – also ihr Verhalten bewusst optimieren. In der klassischen Ökonomie wird angenommen, dass Menschen perfekt informiert sind und logisch entscheiden. In der Realität trifft dies nicht immer zu (Menschen treffen emotionale Entscheidungen, sind unvollkommen informiert, unterliegen kognitiven Verzerrungen). Dies ist ein wichtiger Grund, warum moderne Ökonomie sich zunehmend mit der Verhaltensökonomie beschäftigt.</p>
  </div>

  <div class="ch-section" id="sec-zusammenfassung">
    <h2>Zusammenfassung – Die Kette der Konzepte</h2>
    <p>Lassen Sie uns die gesamte Kette von Bedürfnis über Bedarf bis zur Nachfrage zusammenfassen:</p>

    <div style="background:var(--bg-secondary);border:1px solid var(--separator);border-radius:var(--radius-lg);padding:var(--space-6);margin:var(--space-6) 0;">
      <p style="text-align:center;margin-bottom:var(--space-4);font-size:18px;font-weight:600;">
        <span style="color:var(--econ);">Bedürfnis</span>
        <span style="color:var(--text-tertiary);"> → </span>
        <span style="color:var(--econ);">Bedarf</span>
        <span style="color:var(--text-tertiary);"> → </span>
        <span style="color:var(--econ);">Nachfrage</span>
      </p>

      <div style="margin-top:var(--space-6);">
        <p style="margin-bottom:var(--space-5);"><strong style="color:var(--econ);">1. Bedürfnis</strong> – Ein empfundener Mangel; subjektiv, unbegrenzt, universell menschlich. Beispiel: „Ich bin hungrig"</p>

        <p style="margin-bottom:var(--space-5);"><strong style="color:var(--econ);">2. Bedarf</strong> – Ein konkretes, finanzierbares Bedürfnis (Bedürfnis + Kaufkraft). Beispiel: „Ich bin hungrig UND ich habe 10 € in der Tasche"</p>

        <p><strong style="color:var(--econ);">3. Nachfrage</strong> – Die tatsächliche Kaufabsicht auf dem Markt; beobachtbar und messbar. Beispiel: „Ich kaufe mir jetzt einen Burger für 7 €"</p>
      </div>
    </div>

    <h3>Schlüsselerkenntnisse</h3>
    <ul>
      <li>Bedürfnisse sind das <strong>Fundament</strong> der Ökonomie – sie treiben alle wirtschaftliche Aktivität an.</li>
      <li>Die <strong>Kaufkraft</strong> entscheidet darüber, welche Bedürfnisse zu Bedarf werden – daher haben arme Menschen einen anderen Bedarf als reiche Menschen.</li>
      <li>Nachfrage ist das, was <strong>Wirtschaftswissenschaftler messen und analysieren können</strong> – daher ist sie für die Prognose von Märkten so wichtig.</li>
      <li>Das ökonomische Prinzip (Minimalprinzip und Maximalprinzip) beschreibt, wie Menschen unter Bedingungen der Knappheit rationales Verhalten zeigen.</li>
      <li>In einer Marktwirtschaft entsteht der Preis durch die Schnittmenge von Angebot und Nachfrage – dadurch werden knappe Ressourcen verteilt.</li>
    </ul>
  </div>

  <div class="ch-section" id="sec-aufgaben">
    <h2>Übungsaufgaben</h2>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 1</div>
      <div class="cb-title">Begriffe unterscheiden</div>
      <p><strong>Aufgabenstellung:</strong> Ordnen Sie folgende Aussagen den Begriffen „Bedürfnis", „Bedarf" oder „Nachfrage" zu und begründen Sie Ihre Antwort:</p>
      <ol style="margin:var(--space-3) 0 0 var(--space-5);">
        <li>Ein 16-jähriger Schüler träumt von einem neuen iPhone 15 Pro, das 1.200 € kostet. Sein monatliches Taschengeld beträgt 30 €.</li>
        <li>Eine berufstätige Mutter mit 3.000 € Monatsgehalt kauft sich wöchentlich neue Kleidung im Einzelhandel.</li>
        <li>Ein Obdachloser verspürt das Verlangen nach einem warmen Dach über dem Kopf.</li>
        <li>Ein Rentner mit 1.500 € Rente sucht aktiv nach Angeboten für einen günstigen Tablet-Computer, um seine Enkel zu kontaktieren.</li>
      </ol>
      <p><strong>Lösung:</strong></p>
      <ol style="margin:var(--space-3) 0 0 var(--space-5);">
        <li><strong>Bedürfnis</strong> – Der Schüler hat das Bedürfnis nach dem iPhone, aber nicht die finanzielle Kaufkraft, um es zu einem Bedarf zu machen.</li>
        <li><strong>Nachfrage</strong> – Die Mutter hat sowohl das Bedürfnis als auch die Kaufkraft (Bedarf), und führt die Kaufabsicht aktiv aus (Nachfrage).</li>
        <li><strong>Bedürfnis</strong> – Ein fundamentales Bedürfnis nach Unterkunft/Sicherheit, aber ohne Kaufkraft ist es kein Bedarf.</li>
        <li><strong>Nachfrage</strong> – Der Rentner hat ein Bedürfnis nach Kontakt zu Enkelkindern, die Kaufkraft (Bedarf), und sucht konkret nach Produkten (Nachfrage).</li>
      </ol>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 2</div>
      <div class="cb-title">Maslowsche Pyramide anwenden</div>
      <p><strong>Aufgabenstellung:</strong> Ein Arbeiter verliert seinen Job und muss von Arbeitslosengeld leben (600 € monatlich). Seine Ausgaben pro Monat sehen folgt aus:</p>
      <ul style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
        <li>Miete: 400 €</li>
        <li>Lebensmittel: 150 €</li>
        <li>Nebenkosten: 50 €</li>
      </ul>
      <p><strong>Fragen:</strong></p>
      <ol style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
        <li>Welche Bedürfnisstufen nach Maslow kann der Arbeiter mit seinem Einkommen abdecken?</li>
        <li>Auf welche Konsumausgaben muss der Arbeiter verzichten?</li>
        <li>Was ändert sich, wenn der Arbeiter einen neuen Job mit 2.500 € Gehalt findet?</li>
      </ol>
      <p><strong>Lösung:</strong></p>
      <ol style="margin:var(--space-3) 0 0 var(--space-5);">
        <li>Der Arbeiter deckt gerade noch <strong>Stufe 1 (Physiologische Bedürfnisse)</strong> mit Nahrung und Wärme ab. Stufe 2 (Sicherheit) ist gefährdet, da das Budget sehr knapp ist. Stufen 3-5 sind nicht abgedeckt.</li>
        <li>Der Arbeiter muss auf <strong>Stufe 3 (soziale Kontakte, Unterhaltung)</strong>, <strong>Stufe 4 (Kleidung, Schönheit, Status)</strong> und <strong>Stufe 5 (persönliche Entwicklung, Bildung)</strong> verzichten. Das verfügbare Einkommen (0 €) ermöglicht kein diskretionäres Spending.</li>
        <li>Mit 2.500 € kann der Arbeiter komfortabel Stufe 1 und 2 abdecken und hat bedeutende Mittel für Stufe 3 und 4. Dies führt zu einem deutlich besseren Lebensstil und psychisches Wohlbefinden. Der Konsumentenschaff würde sich dramatisch verändern.</li>
      </ol>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 3</div>
      <div class="cb-title">Minimalprinzip und Maximalprinzip</div>
      <p><strong>Aufgabenstellung:</strong> Ein Unternehmen muss 1.000 Stühle herstellen. Es hat zwei Möglichkeiten:</p>
      <ul style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
        <li><strong>Methode A:</strong> Mit 10 Arbeitern arbeitet das Unternehmen 100 Stunden pro Woche und benötigt 2 Wochen.</li>
        <li><strong>Methode B:</strong> Mit 5 Arbeitern arbeitet das Unternehmen 40 Stunden pro Woche und benötigt 4 Wochen.</li>
      </ul>
      <p><strong>Fragen:</strong></p>
      <ol style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
        <li>Welche Methode folgt dem <strong>Minimalprinzip</strong> und welche dem <strong>Maximalprinzip</strong>?</li>
        <li>Welche Methode kostet weniger an Lohnkosten? (Annahme: Arbeiterstundensatz 15 €)</li>
      </ol>
      <p><strong>Lösung:</strong></p>
      <ol style="margin:var(--space-3) 0 0 var(--space-5);">
        <li><strong>Methode A:</strong> Maximalprinzip – mit gegebenen Mitteln (10 Arbeiter) das maximale Ziel (1.000 Stühle in 2 Wochen) erreichen. <strong>Methode B:</strong> Minimalprinzip – ein Ziel (1.000 Stühle) mit minimalem Aufwand (5 Arbeiter) erreichen.</li>
        <li><strong>Methode A:</strong> 10 Arbeiter × 100 Stunden × 15 € = 15.000 €. <strong>Methode B:</strong> 5 Arbeiter × 160 Stunden × 15 € = 12.000 €. Methode B kostet weniger, benötigt aber mehr Zeit. Die Wahl hängt von Prioritäten ab.</li>
      </ol>
    </div>

    <div class="cb cb-task">
      <div class="cb-label">Aufgabe 4</div>
      <div class="cb-title">Bedarf vs. Nachfrage – Die Rolle des Preises</div>
      <p><strong>Aufgabenstellung:</strong> Eine Person möchte einen Computer kaufen. Sie hat 1.500 € verfügbar. Im Elektronikladen gibt es folgende Optionen:</p>
      <ul style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
        <li><strong>Gaming-Laptop:</strong> 2.000 € (leistungsstark, aber zu teuer)</li>
        <li><strong>Standard-Laptop:</strong> 1.200 € (erfüllt alle Anforderungen)</li>
        <li><strong>Budget-Tablet:</strong> 400 € (funktioniert, aber limitiert)</li>
      </ul>
      <p><strong>Fragen:</strong></p>
      <ol style="margin:var(--space-3) 0 var(--space-4) var(--space-5);">
        <li>Welche Geräte entsprechen einem „Bedarf" nach der Person? Begründen Sie!</li>
        <li>Welches Gerät wird die Person wahrscheinlich kaufen (= Nachfrage)?</li>
        <li>Was würde sich ändern, wenn der Standard-Laptop plötzlich 600 € kostet?</li>
      </ol>
      <p><strong>Lösung:</strong></p>
      <ol style="margin:var(--space-3) 0 0 var(--space-5);">
        <li>Der Standard-Laptop (1.200 €) und das Budget-Tablet (400 €) entsprechen einem Bedarf, da beide innerhalb des verfügbaren Budgets liegen. Der Gaming-Laptop überschreitet das Budget und ist daher kein Bedarf.</li>
        <li>Die Person wird wahrscheinlich den Standard-Laptop kaufen (Nachfrage), da er das beste Preis-Leistungs-Verhältnis bietet. Das ist eine bewusste Marktentscheidung.</li>
        <li>Mit einem reduzierten Preis von 600 € würde der Standard-Laptop deutlich attraktiver. Die Nachfrage könnte sogar steigen, da mehr Verbraucher das verbesserte Preis-Leistungs-Verhältnis erkennen.</li>
      </ol>
    </div>
  </div>

</div>

<aside class="ch-toc">
  <div class="ch-toc-title">Inhaltsverzeichnis</div>
  <ul>
    <li><a href="#sec-ueberblick" class="active">Überblick</a></li>
    <li><a href="#sec-beduerfnis">Bedürfnis</a></li>
    <li><a href="#sec-beduerfnisarten">Bedürfnisarten</a></li>
    <li><a href="#sec-maslow">Maslowsche Pyramide</a></li>
    <li><a href="#sec-bedarf">Bedarf</a></li>
    <li><a href="#sec-nachfrage">Nachfrage</a></li>
    <li><a href="#sec-oekonomisches-prinzip">Ökonomisches Prinzip</a></li>
    <li><a href="#sec-zusammenfassung">Zusammenfassung</a></li>
    <li><a href="#sec-aufgaben">Übungsaufgaben</a></li>
  </ul>
</aside>

</div>

<nav class="ch-nav">
  <a href="/learn/vwl/">← Zurück zur VWL-Übersicht</a>
  <a href="/learn/gueterarten/" class="primary">Güterarten →</a>
</nav>

<script>
(function() {
  const headings = document.querySelectorAll('.ch-section[id]');
  const tocLinks = document.querySelectorAll('.ch-toc a[href^="#"]');

  const updateActiveLink = () => {
    let current = '';
    for (let heading of headings) {
      const top = heading.getBoundingClientRect().top;
      if (top < 200) current = heading.getAttribute('id');
    }
    tocLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href') === '#' + current) {
        link.classList.add('active');
      }
    });
  };

  window.addEventListener('scroll', updateActiveLink);
  updateActiveLink();
})();
</script>
