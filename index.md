---
layout: default
---

<style>
.home {
  max-width: 920px;
  margin: 0 auto;
  padding: 5rem 1.5rem 4rem;
}

.home-eyebrow {
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: var(--s12);
}

.home-nav {
  display: flex;
  flex-direction: column;
  border-top: 1px solid var(--border-strong);
}

.home-nav a {
  display: block;
  padding: 1.5rem 0;
  border-bottom: 1px solid var(--border);
  text-decoration: none;
  transition: padding-left 0.2s var(--ease-out);
}

.home-nav a:hover {
  padding-left: 0.75rem;
}

.home-nav-label {
  display: block;
  font-family: var(--font-display);
  font-size: 24px;
  font-weight: 400;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  margin-bottom: 0.2rem;
  transition: color var(--t-fast);
}

.home-nav a:hover .home-nav-label {
  color: var(--accent);
}

.home-nav-desc {
  display: block;
  font-size: 14px;
  font-weight: 300;
  color: var(--text-tertiary);
  line-height: 1.6;
}

/* ─── Aufgabe des Tages ─── */
.adt {
  margin-bottom: var(--s16);
}

.adt-eyebrow {
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: var(--s4);
}

.adt-card {
  border: 1px solid var(--border-strong);
  border-radius: var(--r-lg);
  padding: var(--s8);
  background: var(--bg-elevated, rgba(255,255,255,0.03));
  transition: border-color 250ms var(--ease-out);
}

.adt-card:hover {
  border-color: var(--border-hover, var(--border-strong));
}

.adt-meta {
  display: flex;
  align-items: center;
  gap: var(--s3);
  margin-bottom: var(--s5);
  flex-wrap: wrap;
}

.adt-tag {
  display: inline-block;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  padding: 3px 10px;
  border-radius: var(--r-sm);
  line-height: 1.4;
}

.adt-tag--mathe { background: rgba(196, 92, 62, 0.12); color: var(--beni); }
.adt-tag--vwl { background: rgba(196, 154, 108, 0.12); color: var(--kitsune); }
.adt-tag--info { background: rgba(91, 122, 140, 0.12); color: var(--ai); }

.adt-difficulty {
  font-size: 11px;
  color: var(--text-tertiary);
  font-weight: 400;
}

.adt-question {
  font-family: var(--font-display);
  font-size: 22px;
  font-weight: 400;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  line-height: 1.45;
  margin-bottom: var(--s3);
}

.adt-question .katex-display {
  margin: var(--s4) 0;
}

.adt-hint {
  font-size: 13px;
  color: var(--text-tertiary);
  font-weight: 300;
  line-height: 1.6;
  margin-bottom: var(--s6);
  font-style: italic;
}

.adt-code {
  display: block;
  background: var(--bg-secondary, #3d3d38);
  border: 1px solid var(--border);
  border-radius: var(--r-sm);
  padding: var(--s4);
  font-family: var(--font-mono);
  font-size: 13px;
  color: var(--text-primary);
  white-space: pre;
  overflow-x: auto;
  margin: var(--s4) 0 var(--s5);
  line-height: 1.6;
}

.adt-actions {
  display: flex;
  align-items: center;
  gap: var(--s3);
  flex-wrap: wrap;
}

.adt-btn {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  font-weight: 500;
  padding: 8px 16px;
  border-radius: var(--r-sm);
  border: 1px solid var(--border-strong);
  background: transparent;
  color: var(--text-primary);
  cursor: pointer;
  transition: all 200ms var(--ease-out);
  text-decoration: none;
  font-family: var(--font-body);
}

.adt-btn:hover {
  background: var(--bg-elevated, rgba(255,255,255,0.06));
  border-color: var(--accent);
  color: var(--accent);
}

.adt-btn--accent {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
}

.adt-btn--accent:hover {
  opacity: 0.88;
  color: #fff;
}

.adt-solution {
  display: none;
  margin-top: var(--s5);
  padding-top: var(--s5);
  border-top: 1px solid var(--border);
}

.adt-solution.visible {
  display: block;
  animation: adtFadeIn 300ms var(--ease-out);
}

@keyframes adtFadeIn {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}

.adt-solution-label {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--matcha);
  margin-bottom: var(--s3);
}

.adt-solution-text {
  font-size: 15px;
  color: var(--text-primary);
  line-height: 1.7;
  font-weight: 300;
}

.adt-solution-text code {
  font-family: var(--font-mono);
  font-size: 13px;
  background: var(--bg-secondary, #3d3d38);
  padding: 2px 6px;
  border-radius: 4px;
}

.adt-link {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  font-size: 13px;
  color: var(--text-tertiary);
  text-decoration: none;
  margin-top: var(--s4);
  transition: color 200ms;
}

.adt-link:hover {
  color: var(--accent);
}

@media (max-width: 480px) {
  .home { padding: 3rem 1.25rem 3rem; }
  .home-nav-label { font-size: 20px; }
  .adt-question { font-size: 18px; }
  .adt-card { padding: var(--s5); }
}
</style>

<!-- KaTeX for math rendering -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.js"></script>

<div class="home">

  <!-- ═══ Aufgabe des Tages ═══ -->
  <div class="adt">
    <div class="adt-eyebrow">Aufgabe des Tages</div>
    <div class="adt-card" id="adt-card">
      <div class="adt-meta">
        <span class="adt-tag" id="adt-tag"></span>
        <span class="adt-difficulty" id="adt-diff"></span>
      </div>
      <div class="adt-question" id="adt-question"></div>
      <div class="adt-hint" id="adt-hint"></div>
      <div id="adt-code-wrap"></div>
      <div class="adt-actions">
        <button class="adt-btn adt-btn--accent" onclick="toggleSolution()">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></svg>
          Antwort zeigen
        </button>
        <a class="adt-btn" id="adt-quiz-link" style="display:none">
          Quiz starten &rarr;
        </a>
      </div>
      <div class="adt-solution" id="adt-solution">
        <div class="adt-solution-label">Antwort</div>
        <div class="adt-solution-text" id="adt-answer"></div>
        <a class="adt-link" id="adt-module-link">Zum Thema &rarr;</a>
      </div>
    </div>
  </div>

  <!-- ═══ Navigation ═══ -->
  <div class="home-eyebrow">Studienkolleg Leipzig</div>

  <nav class="home-nav">
    <a href="/about/">
      <span class="home-nav-label">Hinweise zum Studium</span>
      <span class="home-nav-desc">Wie das Studienkolleg funktioniert, wie viel ihr lernen müsst, wie ihr die Materialien nutzt</span>
    </a>
    <a href="/teaching/">
      <span class="home-nav-label">Materialien</span>
      <span class="home-nav-desc">Mathematik, Volkswirtschaftslehre und Informatik</span>
    </a>
    <a href="/termine/">
      <span class="home-nav-label">Termine</span>
      <span class="home-nav-desc">Klausurtermine und organisatorische Hinweise</span>
    </a>
  </nav>

</div>

<script>
(function() {
  // ═══ AUFGABEN-POOL ═══
  // Jede Aufgabe: { fach, tag, diff, frage, hint?, code?, antwort, quiz?, modul }
  var pool = [
    // ─── MATHEMATIK: Algebra ───
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Berechne die Determinante: $\\det\\begin{pmatrix} 3 & 1 \\\\ 5 & 2 \\end{pmatrix}$",
      hint: "Denk an die Formel ad - bc.",
      antwort: "$\\det = 3 \\cdot 2 - 1 \\cdot 5 = 6 - 5 = 1$",
      quiz: "/assets/quizzes/quiz_determinanten.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Löse das Gleichungssystem: $2x + y = 7$ und $x - y = 2$",
      hint: "Addiere beide Gleichungen, um y zu eliminieren.",
      antwort: "Addition ergibt $3x = 9$, also $x = 3$. Einsetzen: $3 - y = 2$, also $y = 1$. Lösung: $(3, 1)$.",
      quiz: "/assets/quizzes/quiz_lgs_grundlagen.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Gegeben ist $A = \\begin{pmatrix} 1 & 2 \\\\ 3 & 4 \\end{pmatrix}$. Berechne $A^2$.",
      antwort: "$A^2 = \\begin{pmatrix} 1{\\cdot}1+2{\\cdot}3 & 1{\\cdot}2+2{\\cdot}4 \\\\ 3{\\cdot}1+4{\\cdot}3 & 3{\\cdot}2+4{\\cdot}4 \\end{pmatrix} = \\begin{pmatrix} 7 & 10 \\\\ 15 & 22 \\end{pmatrix}$",
      quiz: "/assets/quizzes/quiz_matrizen_grundlagen.html",
      modul: "/teaching/mathematik/"
    },
    // ─── MATHEMATIK: Vektoren ───
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Berechne das Skalarprodukt von $\\vec{a} = \\begin{pmatrix} 2 \\\\ -1 \\\\ 3 \\end{pmatrix}$ und $\\vec{b} = \\begin{pmatrix} 1 \\\\ 4 \\\\ -2 \\end{pmatrix}$.",
      antwort: "$\\vec{a} \\cdot \\vec{b} = 2{\\cdot}1 + (-1){\\cdot}4 + 3{\\cdot}(-2) = 2 - 4 - 6 = -8$",
      quiz: "/assets/quizzes/quiz_vektorprodukt.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Bestimme den Abstand des Punktes $P(1, 2, 3)$ vom Ursprung.",
      antwort: "$d = \\sqrt{1^2 + 2^2 + 3^2} = \\sqrt{14} \\approx 3{,}74$",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Klausurniveau",
      frage: "Zeige, dass die Vektoren $\\vec{a} = \\begin{pmatrix} 1 \\\\ 0 \\\\ -1 \\end{pmatrix}$ und $\\vec{b} = \\begin{pmatrix} 2 \\\\ 1 \\\\ 2 \\end{pmatrix}$ senkrecht zueinander stehen.",
      antwort: "Skalarprodukt: $\\vec{a} \\cdot \\vec{b} = 1{\\cdot}2 + 0{\\cdot}1 + (-1){\\cdot}2 = 2 + 0 - 2 = 0$. Da das Skalarprodukt $= 0$ ist, stehen die Vektoren senkrecht aufeinander.",
      quiz: "/assets/quizzes/quiz_vektorprodukt.html",
      modul: "/teaching/mathematik/"
    },
    // ─── MATHEMATIK: Differentialrechnung ───
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Bestimme die Ableitung von $f(x) = 3x^4 - 2x^2 + 5x - 1$.",
      antwort: "$f'(x) = 12x^3 - 4x + 5$",
      quiz: "/assets/quizzes/quiz_ableitung_grundlagen.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Bestimme die Ableitung von $f(x) = \\sin(x) \\cdot e^x$ mit der Produktregel.",
      antwort: "$f'(x) = \\cos(x) \\cdot e^x + \\sin(x) \\cdot e^x = e^x(\\cos x + \\sin x)$",
      quiz: "/assets/quizzes/quiz_ableitungsregeln.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Finde die Extrempunkte von $f(x) = x^3 - 3x + 2$.",
      hint: "Setze f'(x) = 0 und prüfe mit f''(x).",
      antwort: "$f'(x) = 3x^2 - 3 = 0 \\Rightarrow x = \\pm 1$. $f''(x) = 6x$. Bei $x=1$: $f''(1) = 6 > 0$ (Minimum, $f(1)=0$). Bei $x=-1$: $f''(-1) = -6 < 0$ (Maximum, $f(-1)=4$).",
      quiz: "/assets/quizzes/quiz_extrempunkte.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Klausurniveau",
      frage: "Bestimme die Wendepunkte von $f(x) = x^4 - 6x^2 + 8x + 1$.",
      antwort: "$f''(x) = 12x^2 - 12 = 0 \\Rightarrow x^2 = 1 \\Rightarrow x = \\pm 1$. $f'''(x) = 24x$. Bei $x=1$: $f'''(1) = 24 \\neq 0$ und bei $x=-1$: $f'''(-1) = -24 \\neq 0$. Beide sind Wendepunkte: $W_1(1, 4)$ und $W_2(-1, -12)$.",
      quiz: "/assets/quizzes/quiz_wendepunkte.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Berechne $\\lim_{n \\to \\infty} \\frac{3n^2 + 2n}{n^2 - 1}$.",
      hint: "Teile Zähler und Nenner durch die höchste Potenz von n.",
      antwort: "Teile durch $n^2$: $\\lim_{n \\to \\infty} \\frac{3 + \\frac{2}{n}}{1 - \\frac{1}{n^2}} = \\frac{3+0}{1-0} = 3$",
      quiz: "/assets/quizzes/quiz_grenzwerte_folgen.html",
      modul: "/teaching/mathematik/"
    },
    // ─── MATHEMATIK: Integralrechnung ───
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Berechne $\\int (4x^3 - 6x + 1)\\,dx$.",
      antwort: "$\\int (4x^3 - 6x + 1)\\,dx = x^4 - 3x^2 + x + C$",
      quiz: "/assets/quizzes/quiz_integral_einfuehrung.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Berechne die Fläche zwischen $f(x) = x^2$ und der x-Achse auf dem Intervall $[0, 3]$.",
      antwort: "$A = \\int_0^3 x^2\\,dx = \\left[\\frac{x^3}{3}\\right]_0^3 = \\frac{27}{3} - 0 = 9$ FE",
      quiz: "/assets/quizzes/quiz_hauptsatz_flaechen.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Klausurniveau",
      frage: "Berechne $\\int x \\cdot e^x \\, dx$ mit partieller Integration.",
      hint: "Wähle u = x und v' = e^x.",
      antwort: "Mit $u = x$, $v' = e^x$: $u' = 1$, $v = e^x$. Also: $\\int x \\cdot e^x \\, dx = x \\cdot e^x - \\int e^x \\, dx = x \\cdot e^x - e^x + C = e^x(x-1) + C$.",
      quiz: "/assets/quizzes/quiz_integrationsmethoden.html",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Bestimme mit der Regel von L'Hôpital: $\\lim_{x \\to 0} \\frac{\\sin x}{x}$",
      antwort: "Typ $\\frac{0}{0}$. L'Hôpital: $\\lim_{x \\to 0} \\frac{\\cos x}{1} = \\cos(0) = 1$.",
      quiz: "/assets/quizzes/quiz_hospital.html",
      modul: "/teaching/mathematik/"
    },
    // ─── MATHEMATIK: Kurvendiskussion ───
    {
      fach: "mathe", tag: "Mathematik", diff: "Klausurniveau",
      frage: "Bestimme die Asymptoten von $f(x) = \\frac{2x^2 + 1}{x - 1}$.",
      hint: "Prüfe senkrechte und schräge Asymptoten.",
      antwort: "Senkrechte Asymptote bei $x = 1$ (Nenner = 0). Polynomdivision: $f(x) = 2x + 2 + \\frac{3}{x-1}$, also schräge Asymptote: $y = 2x + 2$.",
      quiz: "/assets/quizzes/quiz_asymptoten.html",
      modul: "/teaching/mathematik/"
    },
    // ─── VWL: Mikroökonomie ───
    {
      fach: "vwl", tag: "VWL", diff: "Grundlagen",
      frage: "Was ist der Unterschied zwischen einem Bedürfnis, einem Bedarf und der Nachfrage?",
      antwort: "Ein Bedürfnis ist ein Mangelempfinden (z.B. Hunger). Bedarf entsteht, wenn das Bedürfnis auf ein konkretes Gut gerichtet ist (z.B. Pizza). Nachfrage entsteht, wenn der Bedarf mit Kaufkraft am Markt auftritt (z.B. Pizza kaufen).",
      quiz: "/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html",
      modul: "/teaching/vwl/"
    },
    {
      fach: "vwl", tag: "VWL", diff: "Grundlagen",
      frage: "Nenne drei Merkmale eines vollkommenen Marktes.",
      antwort: "Homogene Güter (alle Güter sind gleichartig), vollständige Markttransparenz (alle Teilnehmer kennen Preise und Qualitäten), keine persönlichen, zeitlichen oder räumlichen Präferenzen.",
      quiz: "/assets/quizzes/quiz_marktformen.html",
      modul: "/teaching/vwl/"
    },
    {
      fach: "vwl", tag: "VWL", diff: "Mittel",
      frage: "Die Nachfragefunktion ist $p = 100 - 2q$ und die Angebotsfunktion $p = 20 + 3q$. Bestimme den Gleichgewichtspreis und die Gleichgewichtsmenge.",
      antwort: "Gleichsetzen: $100 - 2q = 20 + 3q \\Rightarrow 80 = 5q \\Rightarrow q^* = 16$. Einsetzen: $p^* = 100 - 2 \\cdot 16 = 68$. Gleichgewicht: Menge 16, Preis 68.",
      quiz: "/assets/quizzes/quiz_marktgleichgewicht.html",
      modul: "/teaching/vwl/"
    },
    {
      fach: "vwl", tag: "VWL", diff: "Grundlagen",
      frage: "Was versteht man unter einem öffentlichen Gut? Nenne ein Beispiel.",
      antwort: "Ein öffentliches Gut ist nicht-rivalisierend (der Konsum durch eine Person schließt andere nicht aus) und nicht-ausschließbar (niemand kann vom Konsum ausgeschlossen werden). Beispiel: Straßenbeleuchtung, Landesverteidigung.",
      quiz: "/assets/quizzes/quiz_gueterarten.html",
      modul: "/teaching/vwl/"
    },
    {
      fach: "vwl", tag: "VWL", diff: "Mittel",
      frage: "Erkläre das Gesetz der Nachfrage und warum die Nachfragekurve in der Regel fallend verläuft.",
      antwort: "Das Gesetz der Nachfrage besagt: Steigt der Preis eines Gutes, sinkt die nachgefragte Menge (ceteris paribus) und umgekehrt. Die Kurve fällt wegen des Substitutionseffekts (Konsumenten weichen auf günstigere Alternativen aus) und des Einkommenseffekts (bei höherem Preis sinkt die reale Kaufkraft).",
      quiz: "/assets/quizzes/quiz_nachfrage.html",
      modul: "/teaching/vwl/"
    },
    // ─── VWL: Makroökonomie ───
    {
      fach: "vwl", tag: "VWL", diff: "Mittel",
      frage: "Nenne die vier Phasen eines Konjunkturzyklus.",
      antwort: "Aufschwung (Expansion), Hochkonjunktur (Boom), Abschwung (Rezession), Tiefstand (Depression). Danach beginnt der Zyklus erneut.",
      quiz: "/assets/quizzes/quiz_konjunktur.html",
      modul: "/teaching/vwl/"
    },
    {
      fach: "vwl", tag: "VWL", diff: "Klausurniveau",
      frage: "Erkläre den Unterschied zwischen dem BIP nach Entstehungs-, Verwendungs- und Verteilungsrechnung.",
      antwort: "Entstehung: Summe der Bruttowertschöpfung aller Wirtschaftsbereiche. Verwendung: $BIP = C + I + G + (Ex - Im)$ (Konsum + Investitionen + Staatsausgaben + Nettoexporte). Verteilung: Summe der Arbeitnehmerentgelte, Unternehmensgewinne, Abschreibungen und Produktionsabgaben.",
      quiz: "/assets/quizzes/quiz_vgr.html",
      modul: "/teaching/vwl/"
    },
    {
      fach: "vwl", tag: "VWL", diff: "Grundlagen",
      frage: "Was ist Inflation und wie wird sie gemessen?",
      antwort: "Inflation ist ein anhaltender Anstieg des allgemeinen Preisniveaus. Sie wird typischerweise über den Verbraucherpreisindex (VPI) gemessen, der die Preisentwicklung eines repräsentativen Warenkorbs abbildet.",
      quiz: "/assets/quizzes/quiz_preisniveau.html",
      modul: "/teaching/vwl/"
    },
    // ─── INFORMATIK ───
    {
      fach: "info", tag: "Informatik", diff: "Grundlagen",
      frage: "Was ist der Unterschied zwischen einer Liste und einem Tupel in Python?",
      antwort: "Listen sind veränderbar (mutable): Elemente können hinzugefügt, entfernt oder geändert werden. Tupel sind unveränderbar (immutable): Nach der Erstellung können sie nicht mehr verändert werden. Listen verwenden eckige Klammern <code>[ ]</code>, Tupel runde Klammern <code>( )</code>.",
      quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html",
      modul: "/teaching/informatik/"
    },
    {
      fach: "info", tag: "Informatik", diff: "Grundlagen",
      frage: "Was gibt dieser Python-Code aus?",
      code: "x = [1, 2, 3, 4, 5]\nprint(x[1:4])",
      antwort: "<code>[2, 3, 4]</code> — Slicing in Python geht von Index 1 (inklusive) bis Index 4 (exklusive).",
      quiz: "/assets/quizzes/quiz_listen_datenstrukturen.html",
      modul: "/teaching/informatik/"
    },
    {
      fach: "info", tag: "Informatik", diff: "Mittel",
      frage: "Schreibe eine Python-Funktion, die prüft, ob eine Zahl eine Primzahl ist.",
      hint: "Du brauchst nur bis zur Wurzel der Zahl zu prüfen.",
      code: "def ist_primzahl(n):\n    # Dein Code hier\n    pass",
      antwort: "<code>def ist_primzahl(n):</code><br><code>&nbsp;&nbsp;if n < 2: return False</code><br><code>&nbsp;&nbsp;for i in range(2, int(n**0.5)+1):</code><br><code>&nbsp;&nbsp;&nbsp;&nbsp;if n % i == 0: return False</code><br><code>&nbsp;&nbsp;return True</code>",
      quiz: "/assets/quizzes/quiz_kontrollstrukturen.html",
      modul: "/teaching/informatik/"
    },
    {
      fach: "info", tag: "Informatik", diff: "Grundlagen",
      frage: "Was ist der Unterschied zwischen <code>=</code> und <code>==</code> in Python?",
      antwort: "<code>=</code> ist der Zuweisungsoperator (speichert einen Wert in einer Variable, z.B. <code>x = 5</code>). <code>==</code> ist der Vergleichsoperator (prüft, ob zwei Werte gleich sind, z.B. <code>x == 5</code> ergibt <code>True</code> oder <code>False</code>).",
      quiz: "/assets/quizzes/quiz_variablen_datentypen.html",
      modul: "/teaching/informatik/"
    },
    {
      fach: "info", tag: "Informatik", diff: "Mittel",
      frage: "Was gibt dieser Code aus?",
      code: "for i in range(5):\n    if i % 2 == 0:\n        print(i, end=\" \")",
      antwort: "<code>0 2 4</code> — Die Schleife geht von 0 bis 4. Die Bedingung <code>i % 2 == 0</code> filtert gerade Zahlen.",
      quiz: "/assets/quizzes/quiz_kontrollstrukturen.html",
      modul: "/teaching/informatik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Grundlagen",
      frage: "Berechne: $\\frac{2}{3} + \\frac{3}{4}$",
      hint: "Finde den gemeinsamen Nenner.",
      antwort: "Gemeinsamer Nenner ist 12: $\\frac{8}{12} + \\frac{9}{12} = \\frac{17}{12}$",
      modul: "/teaching/mathematik/"
    },
    {
      fach: "mathe", tag: "Mathematik", diff: "Mittel",
      frage: "Berechne das Rotationsvolumen, das entsteht, wenn $f(x) = \\sqrt{x}$ auf $[0, 4]$ um die x-Achse rotiert.",
      antwort: "$V = \\pi \\int_0^4 (\\sqrt{x})^2 \\, dx = \\pi \\int_0^4 x \\, dx = \\pi \\left[\\frac{x^2}{2}\\right]_0^4 = \\pi \\cdot 8 = 8\\pi$ VE",
      quiz: "/assets/quizzes/quiz_rotationsvolumen.html",
      modul: "/teaching/mathematik/"
    }
  ];

  // ─── Tagesbasierte Auswahl ───
  function getDayIndex() {
    var now = new Date();
    var start = new Date(now.getFullYear(), 0, 0);
    var diff = now - start;
    var dayOfYear = Math.floor(diff / 86400000);
    return dayOfYear % pool.length;
  }

  // ─── Render mit KaTeX ───
  function renderMath(el) {
    var html = el.innerHTML;
    // Display math: $$...$$
    html = html.replace(/\$\$([\s\S]+?)\$\$/g, function(m, tex) {
      var span = document.createElement('span');
      try { katex.render(tex.trim(), span, { displayMode: true, throwOnError: false }); }
      catch(e) { span.textContent = tex; }
      return span.outerHTML;
    });
    // Inline math: $...$
    html = html.replace(/\$([^\$]+?)\$/g, function(m, tex) {
      var span = document.createElement('span');
      try { katex.render(tex.trim(), span, { displayMode: false, throwOnError: false }); }
      catch(e) { span.textContent = tex; }
      return span.outerHTML;
    });
    el.innerHTML = html;
  }

  // ─── Init ───
  var task = pool[getDayIndex()];
  var tagEl = document.getElementById('adt-tag');
  var diffEl = document.getElementById('adt-diff');
  var questionEl = document.getElementById('adt-question');
  var hintEl = document.getElementById('adt-hint');
  var codeWrap = document.getElementById('adt-code-wrap');
  var answerEl = document.getElementById('adt-answer');
  var quizLink = document.getElementById('adt-quiz-link');
  var modulLink = document.getElementById('adt-module-link');

  // Tag
  tagEl.textContent = task.tag;
  tagEl.className = 'adt-tag adt-tag--' + task.fach;

  // Difficulty
  var diffIcons = { "Grundlagen": "I", "Mittel": "II", "Klausurniveau": "III" };
  diffEl.textContent = (diffIcons[task.diff] || "") + " " + task.diff;

  // Question
  questionEl.innerHTML = task.frage;
  renderMath(questionEl);

  // Hint
  if (task.hint) {
    hintEl.textContent = task.hint;
    hintEl.style.display = 'block';
  } else {
    hintEl.style.display = 'none';
  }

  // Code block
  if (task.code) {
    var pre = document.createElement('code');
    pre.className = 'adt-code';
    pre.textContent = task.code;
    codeWrap.appendChild(pre);
  }

  // Answer
  answerEl.innerHTML = task.antwort;
  renderMath(answerEl);

  // Links
  if (task.quiz) {
    quizLink.href = task.quiz;
    quizLink.style.display = 'inline-flex';
  }
  if (task.modul) {
    modulLink.href = task.modul;
  }

  // Toggle solution
  window.toggleSolution = function() {
    var sol = document.getElementById('adt-solution');
    sol.classList.toggle('visible');
    var btn = document.querySelector('.adt-btn--accent');
    if (sol.classList.contains('visible')) {
      btn.innerHTML = '<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M17.94 17.94A10.07 10.07 0 0112 20c-7 0-11-8-11-8a18.45 18.45 0 015.06-5.94M9.9 4.24A9.12 9.12 0 0112 4c7 0 11 8 11 8a18.5 18.5 0 01-2.16 3.19m-6.72-1.07a3 3 0 11-4.24-4.24"/><line x1="1" y1="1" x2="23" y2="23"/></svg> Antwort verbergen';
    } else {
      btn.innerHTML = '<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"/><circle cx="12" cy="12" r="3"/></svg> Antwort zeigen';
    }
  };
})();
</script>
