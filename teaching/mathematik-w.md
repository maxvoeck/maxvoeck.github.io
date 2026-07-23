---
layout: page
title: 
permalink: /teaching/mathematik-w/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
/* ═══════════════════════════════════════════════════════
   NACHTPROGRAMM — Mathematik (W-Kurs) für das Studienkolleg
   Konzertprogramm-Ästhetik: Tinte, Elfenbein, Messing
   ═══════════════════════════════════════════════════════ */
:root {
  --ink:      #101014;
  --graphit:  #17171d;
  --graphit2: #1e1e26;
  --linie:    rgba(236, 231, 220, 0.09);
  --linie2:   rgba(236, 231, 220, 0.18);
  --elfenbein:#ece7dc;
  --nebel:    #8f8e97;
  --messing:  #c2a15c;
  --messing2: #dfc48a;
  --gruen:    #8fa284;

  --display: 'Fraunces', Georgia, serif;
  --body:    'Inter', system-ui, sans-serif;
  --mono:    'JetBrains Mono', monospace;
}

body, html, .page-content, .wrapper, main {
  background: #101014 !important;
}
.post-header, .page-heading, header.post-header {
  display: none !important;
}

.mw-page * { box-sizing: border-box; margin: 0; padding: 0; }

.mw-page {
  background: var(--ink);
  color: var(--elfenbein);
  font-family: var(--body);
  font-size: 15px;
  line-height: 1.55;
  -webkit-font-smoothing: antialiased;
  padding-bottom: 120px;
}
.mw-page h1, .mw-page h2, .mw-page h3, .mw-page h4, .mw-page h5, .mw-page h6 {
  color: var(--elfenbein);
}

.mw-wrap { max-width: 1060px; margin: 0 auto; padding: 0 28px; }

/* ─── Hero ─── */
.mw-hero {
  padding: 96px 0 72px;
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 48px;
  align-items: end;
  border-bottom: 1px solid var(--linie2);
}
.mw-eyebrow {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.28em;
  text-transform: uppercase;
  color: var(--messing);
  margin-bottom: 20px;
}
.mw-hero h1 {
  font-family: var(--display);
  font-weight: 300;
  font-size: clamp(52px, 8vw, 92px);
  line-height: 0.98;
  letter-spacing: -0.02em;
}
.mw-hero h1 em {
  font-style: italic;
  font-weight: 300;
  color: var(--messing2);
}
.mw-hero-sub {
  margin-top: 22px;
  max-width: 46ch;
  color: var(--nebel);
  font-size: 16px;
}

.mw-status {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--nebel);
  border: 1px solid var(--linie2);
  border-radius: 999px;
  padding: 9px 18px;
  white-space: nowrap;
}

/* ─── Kapitel ─── */
.mw-kapitel { padding: 72px 0 12px; }
.mw-kapitel-kopf {
  display: flex;
  align-items: baseline;
  gap: 22px;
  margin-bottom: 34px;
}
.mw-numeral {
  font-family: var(--display);
  font-style: italic;
  font-weight: 300;
  font-size: 44px;
  color: var(--messing);
  min-width: 64px;
}
.mw-kapitel-kopf h2 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 32px;
  letter-spacing: -0.01em;
}
.mw-kapitel-kopf .mw-meta {
  font-family: var(--mono);
  font-size: 11px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--nebel);
  margin-left: auto;
  white-space: nowrap;
}

/* ─── Leerer Zustand ─── */
.mw-leer {
  padding: 20px 8px 8px;
  border-top: 1px solid var(--linie);
  color: var(--nebel);
  font-size: 14px;
  font-style: italic;
}

/* ─── Modulzeilen (Tracklist, für später) ─── */
.mw-liste { border-top: 1px solid var(--linie); }
.mw-modul {
  display: grid;
  grid-template-columns: 56px 1fr auto;
  gap: 20px;
  align-items: center;
  padding: 20px 8px;
  border-bottom: 1px solid var(--linie);
  transition: background 180ms ease, padding 180ms ease;
}
.mw-modul:hover { background: rgba(236,231,220,0.025); padding-left: 16px; }
.mw-nr {
  font-family: var(--mono);
  font-size: 13px;
  color: var(--nebel);
  transition: color 180ms;
}
.mw-modul:hover .mw-nr { color: var(--messing); }
.mw-modul h4 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 19px;
  letter-spacing: 0.005em;
}
.mw-desc { color: var(--nebel); font-size: 13.5px; margin-top: 3px; }

/* Aktionen */
.mw-actions { display: flex; align-items: center; gap: 8px; flex-wrap: wrap; justify-content: flex-end; }
.mw-btn {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  font-family: var(--body);
  font-size: 12.5px;
  font-weight: 500;
  letter-spacing: 0.02em;
  color: var(--elfenbein);
  background: transparent;
  border: 1px solid var(--linie2);
  border-radius: 999px;
  padding: 7px 15px;
  cursor: pointer;
  text-decoration: none;
  transition: all 160ms ease;
  white-space: nowrap;
}
.mw-btn:hover { border-color: var(--messing); color: var(--messing2); }
.mw-btn svg { width: 13px; height: 13px; flex-shrink: 0; }

/* ─── Mini-Player ─── */
.mw-player {
  position: fixed;
  left: 50%;
  bottom: 20px;
  transform: translate(-50%, 140%);
  width: min(680px, calc(100% - 32px));
  background: rgba(30, 30, 38, 0.92);
  backdrop-filter: blur(18px);
  -webkit-backdrop-filter: blur(18px);
  border: 1px solid var(--linie2);
  border-radius: 14px;
  padding: 14px 20px;
  display: flex;
  align-items: center;
  gap: 16px;
  box-shadow: 0 20px 50px rgba(0,0,0,0.5);
  transition: transform 420ms cubic-bezier(0.22, 1, 0.36, 1);
  z-index: 50;
}
.mw-player.offen { transform: translate(-50%, 0); }
.mw-play {
  width: 42px; height: 42px;
  border-radius: 50%;
  background: var(--messing);
  border: none;
  cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
  transition: background 160ms;
}
.mw-play:hover { background: var(--messing2); }
.mw-play svg { width: 15px; height: 15px; fill: var(--ink); }
.mw-player-info { flex: 1; min-width: 0; }
.mw-player-info .laeuft {
  font-family: var(--mono);
  font-size: 9.5px;
  letter-spacing: 0.24em;
  text-transform: uppercase;
  color: var(--messing);
}
.mw-player-info .titel {
  font-family: var(--display);
  font-size: 16px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  margin-top: 2px;
}
.mw-player-bar {
  height: 3px;
  background: var(--linie2);
  border-radius: 2px;
  margin-top: 8px;
  overflow: hidden;
}
.mw-player-bar > div {
  height: 100%;
  width: 0%;
  background: var(--messing);
  border-radius: 2px;
}
.mw-player-close {
  background: none; border: none;
  color: var(--nebel);
  font-size: 20px;
  cursor: pointer;
  line-height: 1;
  padding: 6px;
  transition: color 160ms;
}
.mw-player-close:hover { color: var(--elfenbein); }

/* ─── Fußzeile ─── */
.mw-fuss {
  margin-top: 88px;
  padding: 36px 0;
  border-top: 1px solid var(--linie2);
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  flex-wrap: wrap;
  color: var(--nebel);
  font-size: 13px;
}
.mw-fuss-links { display: flex; gap: 10px; }

/* ─── Responsiv ─── */
@media (max-width: 760px) {
  .mw-hero { grid-template-columns: 1fr; gap: 24px; padding: 64px 0 48px; }
  .mw-modul { grid-template-columns: 40px 1fr; }
  .mw-actions { grid-column: 1 / -1; padding-left: 60px; flex-wrap: wrap; justify-content: flex-start; }
  .mw-kapitel-kopf .mw-meta { display: none; }
}

@media (prefers-reduced-motion: reduce) {
  * { transition-duration: 1ms !important; animation: none !important; }
  html { scroll-behavior: auto; }
}
</style>

<div class="mw-page">
<div class="mw-wrap">

  <!-- Hero -->
  <header class="mw-hero">
    <div>
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung · W-Kurs</div>
      <h1>Mathematik,<br><em>2. Semester.</em></h1>
      <p class="mw-hero-sub">Module, Skripte und Übungen für den W-Kurs im zweiten Semester. Die Inhalte werden nach und nach ergänzt.</p>
    </div>
    <div class="mw-status">In Vorbereitung</div>
  </header>

  <div id="kapitel"></div>

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div>Materialien folgen Kapitel für Kapitel — hier lohnt sich regelmäßiges Vorbeischauen.</div>
    <div class="mw-fuss-links">
      <a href="/teaching/" class="mw-btn">← Übersicht</a>
    </div>
  </footer>

</div>

<!-- Mini-Player -->
<div class="mw-player" id="player">
  <button class="mw-play" id="playBtn" aria-label="Abspielen / Pausieren">
    <svg id="playIcon" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
  </button>
  <div class="mw-player-info">
    <div class="laeuft">Jetzt läuft</div>
    <div class="titel" id="playerTitel">—</div>
    <div class="mw-player-bar"><div id="playerBar"></div></div>
  </div>
  <button class="mw-player-close" id="playerClose" aria-label="Player schließen">×</button>
</div>
<audio id="audio"></audio>
</div>

<script>
/* ─── Daten: hier Kapitel und Module eintragen, sobald Materialien vorliegen ─── */
const KAPITEL = [
  {
    numeral: 'I', titel: 'Lineare Algebra', meta: '1 Modul',
    module: [
      { id:'a1', nr:'01', titel:'Matrizen — Grundbegriffe', desc:'Definition, Typ, spezielle Matrizen (Diagonal-, Dreiecks-, symmetrische Matrix), Gleichheit, Addition, Skalarmultiplikation, Matrizenmultiplikation, Transponierte, Inverse und Spur', pdf:'/assets/pdfs/W_Matrizen_1.pdf', quiz:'/assets/quizzes/quiz_matrizen_w_grundbegriffe.html', text:'/assets/texte/w-matrizen-1.pdf', podcast:'/assets/audio/w-matrizen-1.m4a' },
    ]
  },
  { numeral: 'II',  titel: 'Finanzmathematik',      meta: 'folgt', module: [] },
  { numeral: 'III', titel: 'Differentialrechnung',  meta: 'folgt', module: [] },
  { numeral: 'IV',  titel: 'Integralrechnung',      meta: 'folgt', module: [] },
];

const iconPdf  = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6"/></svg>';
const iconQuiz = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 9a3 3 0 1 1 4 2.83c-.7.26-1 .95-1 1.67v.5"/><path d="M12 17.5h.01"/></svg>';
const iconText = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 6h16M4 12h16M4 18h10"/></svg>';
const iconPod  = '<svg viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg>';

function actionsFor(m) {
  let html = `<a href="${m.pdf}" class="mw-btn">${iconPdf} Folien</a>`;
  if (m.quiz) html += `<a href="${m.quiz}" class="mw-btn">${iconQuiz} Quiz</a>`;
  if (m.podcast) html += `<button class="mw-btn" onclick="startPodcast('${m.nr}', '${m.titel.replace(/'/g, "\\'")}', '${m.podcast}')">${iconPod} Podcast</button>`;
  if (m.text) html += `<a href="${m.text}" class="mw-btn">${iconText} Text</a>`;
  return html;
}

function render() {
  const wrap = document.getElementById('kapitel');
  wrap.innerHTML = KAPITEL.map(k => `
    <section class="mw-kapitel">
      <div class="mw-kapitel-kopf">
        <span class="mw-numeral">${k.numeral}</span>
        <h2>${k.titel}</h2>
        <span class="mw-meta">${k.meta}</span>
      </div>
      ${k.module.length
        ? `<div class="mw-liste">${k.module.map(m => `
            <div class="mw-modul">
              <span class="mw-nr">${m.nr}</span>
              <div>
                <h4>${m.titel}</h4>
                <p class="mw-desc">${m.desc}</p>
              </div>
              <div class="mw-actions">${actionsFor(m)}</div>
            </div>
          `).join('')}</div>`
        : `<div class="mw-leer">Materialien für dieses Kapitel folgen in Kürze.</div>`
      }
    </section>
  `).join('');
}

/* ─── Mini-Player ─── */
const audio = document.getElementById('audio');
const player = document.getElementById('player');
const playBtn = document.getElementById('playBtn');
const playIcon = document.getElementById('playIcon');

function startPodcast(nr, titel, src) {
  document.getElementById('playerTitel').textContent = `Modul ${nr} · ${titel}`;
  player.classList.add('offen');
  audio.src = src;
  audio.play().catch(() => { /* Datei noch nicht vorhanden — Player bleibt als Vorschau sichtbar */ });
  setIcon();
}
playBtn.addEventListener('click', () => {
  if (audio.paused) audio.play().catch(()=>{}); else audio.pause();
  setIcon();
});
audio.addEventListener('play', setIcon);
audio.addEventListener('pause', setIcon);
audio.addEventListener('timeupdate', () => {
  const pct = audio.duration ? (audio.currentTime / audio.duration) * 100 : 0;
  document.getElementById('playerBar').style.width = pct + '%';
});
function setIcon() {
  playIcon.innerHTML = audio.paused
    ? '<path d="M8 5v14l11-7z"/>'
    : '<path d="M6 5h4v14H6zM14 5h4v14h-4z"/>';
}
document.getElementById('playerClose').addEventListener('click', () => {
  audio.pause();
  player.classList.remove('offen');
});

render();
</script>
