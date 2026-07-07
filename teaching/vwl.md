---
layout: page
title:
permalink: /teaching/vwl/
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;1,9..144,300;1,9..144,400&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
/* ═══════════════════════════════════════════════════════
   NACHTPROGRAMM — Volkswirtschaftslehre für das Studienkolleg
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
.mw-hero-sub {
  margin-top: 22px;
  max-width: 46ch;
  color: var(--nebel);
  font-size: 16px;
}

/* Fortschrittsbogen */
.mw-progress { text-align: center; }
.mw-ring { width: 120px; height: 120px; }
.mw-ring circle { fill: none; stroke-width: 3; }
.mw-ring .bg { stroke: var(--linie2); }
.mw-ring .fg {
  stroke: var(--messing);
  stroke-linecap: round;
  transform: rotate(-90deg);
  transform-origin: 50% 50%;
  transition: stroke-dashoffset 600ms cubic-bezier(0.4,0,0.2,1);
}
.mw-ring-label {
  font-family: var(--display);
  font-size: 30px;
  font-weight: 300;
  fill: var(--elfenbein);
}
.mw-ring-caption {
  margin-top: 10px;
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--nebel);
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

/* ─── Modulzeilen (Tracklist) ─── */
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
.mw-modul.done .mw-nr { color: var(--gruen); }
.mw-modul h4 {
  font-family: var(--display);
  font-weight: 400;
  font-size: 19px;
  letter-spacing: 0.005em;
}
.mw-modul.done h4 { color: var(--nebel); }
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

/* Haken */
.mw-check {
  width: 30px; height: 30px;
  border-radius: 50%;
  border: 1px solid var(--linie2);
  background: transparent;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  transition: all 200ms ease;
  margin-left: 6px;
  flex-shrink: 0;
}
.mw-check svg { width: 13px; height: 13px; stroke: var(--ink); opacity: 0; transform: scale(0.4); transition: all 260ms cubic-bezier(0.34,1.56,0.64,1); }
.mw-check:hover { border-color: var(--gruen); }
.mw-modul.done .mw-check { background: var(--gruen); border-color: var(--gruen); }
.mw-modul.done .mw-check svg { opacity: 1; transform: scale(1); }

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
  .mw-hero { grid-template-columns: 1fr; gap: 36px; padding: 64px 0 48px; }
  .mw-progress { text-align: left; }
  .mw-modul { grid-template-columns: 40px 1fr; }
  .mw-actions { grid-column: 1 / -1; padding-left: 60px; flex-wrap: wrap; justify-content: flex-start; }
  .mw-kapitel-kopf .mw-meta { display: none; }
}
@media (max-width: 760px) { .mw-actions { padding-left: 0; } }

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
      <div class="mw-eyebrow">Studienkolleg Leipzig · Feststellungsprüfung</div>
      <h1>Volkswirtschaftslehre</h1>
      <p class="mw-hero-sub">17 Module in zwei Kapiteln — Mikro- und Makroökonomie, jedes Modul mit Skript, Quiz, Podcast zum Hören und vertiefendem Text.</p>
    </div>
    <div class="mw-progress">
      <svg class="mw-ring" viewBox="0 0 120 120">
        <circle class="bg" cx="60" cy="60" r="52"/>
        <circle class="fg" cx="60" cy="60" r="52" id="ringFg"/>
        <text class="mw-ring-label" x="60" y="60" text-anchor="middle" dominant-baseline="central" id="ringLabel">0</text>
      </svg>
      <div class="mw-ring-caption">von <span id="ringTotal">0</span> Modulen</div>
    </div>
  </header>

  <div id="kapitel"></div>

  <!-- Fußzeile -->
  <footer class="mw-fuss">
    <div><strong style="color:var(--elfenbein)">17 Module</strong> · Mikroökonomie &amp; Makroökonomie</div>
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
/* ─── Daten: hier neue Module, PDFs & Quiz eintragen ─── */
const KAPITEL = [
  {
    numeral: 'I', titel: 'Mikroökonomie', meta: '9 Module',
    module: [
      { id:'m1', nr:'01', titel:'Bedürfnis, Bedarf und Nachfrage', pdf:'/assets/pdfs/WS_VWL_1-3.pdf', quiz:'/assets/quizzes/quiz_beduerfnis_bedarf_nachfrage.html', podcast:'/assets/audio/beduerfnis-bedarf-nachfrage.mp3', text:'/assets/texte/beduerfnis-bedarf-nachfrage.pdf' },
      { id:'m2', nr:'02', titel:'Güterarten in der Wirtschaft', pdf:'/assets/pdfs/WS_VWL_2-2.pdf', quiz:'/assets/quizzes/quiz_gueterarten.html', podcast:'/assets/audio/gueterarten.mp3', text:'/assets/texte/gueterarten.pdf' },
      { id:'m3', nr:'03', titel:'Angebot und Angebotskurve', pdf:'/assets/pdfs/WS_VWL_3-4.pdf', quiz:'/assets/quizzes/quiz_angebot.html', podcast:'/assets/audio/angebot.mp3', text:'/assets/texte/angebot.pdf' },
      { id:'m4', nr:'04', titel:'Nachfrage und Nachfragekurve', pdf:'/assets/pdfs/WS_VWL_4-2.pdf', quiz:'/assets/quizzes/quiz_nachfrage.html', podcast:'/assets/audio/nachfrage.mp3', text:'/assets/texte/nachfrage.pdf' },
      { id:'m5', nr:'05', titel:'Marktgleichgewicht', pdf:'/assets/pdfs/WS_VWL_5-2.pdf', quiz:'/assets/quizzes/quiz_marktgleichgewicht.html', podcast:'/assets/audio/marktgleichgewicht.mp3', text:'/assets/texte/marktgleichgewicht.pdf' },
      { id:'m6', nr:'06', titel:'Konsumenten- und Produzentenrente', pdf:'/assets/pdfs/WS_VWL_6.pdf', quiz:'/assets/quizzes/quiz_renten.html', podcast:'/assets/audio/renten.mp3', text:'/assets/texte/renten.pdf' },
      { id:'m7', nr:'07', titel:'Marktformen', pdf:'/assets/pdfs/WS_VWL_7.pdf', quiz:'/assets/quizzes/quiz_marktformen.html', podcast:'/assets/audio/marktformen.mp3', text:'/assets/texte/marktformen.pdf' },
      { id:'m8', nr:'08', titel:'Budgetgerade', pdf:'/assets/pdfs/WS_VWL_8-3.pdf', quiz:'/assets/quizzes/quiz_budgetgerade.html', podcast:'/assets/audio/budgetgerade.mp3', text:'/assets/texte/budgetgerade.pdf' },
      { id:'klausur-mikro', nr:'★', titel:'Klausur Mikroökonomie', desc:'Übungsklausur zu allen Mikrothemen', pdf:'/assets/pdfs/Übungsheft_W_1.pdf', podcast:'/assets/audio/klausur-mikro.mp3', text:'/assets/texte/klausur-mikro.pdf' },
    ]
  },
  {
    numeral: 'II', titel: 'Makroökonomie', meta: '8 Module',
    module: [
      { id:'m9', nr:'09', titel:'Volkswirtschaftliche Gesamtrechnung', pdf:'/assets/pdfs/VWL_11.pdf', quiz:'/assets/quizzes/quiz_vgr.html', podcast:'/assets/audio/vgr.mp3', text:'/assets/texte/vgr.pdf' },
      { id:'m10', nr:'10', titel:'Nominales vs. reales BIP', pdf:'/assets/pdfs/VWL_12.pdf', quiz:'/assets/quizzes/quiz_vgr2.html', podcast:'/assets/audio/nominales-reales-bip.mp3', text:'/assets/texte/nominales-reales-bip.pdf' },
      { id:'m11', nr:'11', titel:'Konjunktur & Konjunkturzyklen', pdf:'/assets/pdfs/VWL_11_Konjunktur.pdf', quiz:'/assets/quizzes/quiz_konjunktur.html', podcast:'/assets/audio/konjunktur.mp3', text:'/assets/texte/konjunktur.pdf' },
      { id:'m12', nr:'12', titel:'Antizyklische Konjunkturpolitik', pdf:'/assets/pdfs/VWL_12_Konjunkturpolitik.pdf', quiz:'/assets/quizzes/quiz_konjunkturpolitik.html', podcast:'/assets/audio/konjunkturpolitik.mp3', text:'/assets/texte/konjunkturpolitik.pdf' },
      { id:'m13', nr:'13', titel:'Arbeitslosigkeit & Arbeitsmarktpolitik', pdf:'/assets/pdfs/Vwl_13_Arbeitslosigkeit.pdf', quiz:'/assets/quizzes/quiz_arbeitslosigkeit.html', podcast:'/assets/audio/arbeitslosigkeit.mp3', text:'/assets/texte/arbeitslosigkeit.pdf' },
      { id:'m14', nr:'14', titel:'Inflation & Preisniveaustabilität', pdf:'/assets/pdfs/VWL_14_Preisniveau.pdf', quiz:'/assets/quizzes/quiz_preisniveau.html', podcast:'/assets/audio/preisniveau.mp3', text:'/assets/texte/preisniveau.pdf' },
      { id:'m15', nr:'15', titel:'Magisches Viereck', pdf:'/assets/pdfs/VWL_15.pdf', quiz:'/assets/quizzes/quiz_magisches_viereck.html', podcast:'/assets/audio/magisches-viereck.mp3', text:'/assets/texte/magisches-viereck.pdf' },
      { id:'klausur-makro', nr:'★', titel:'Klausur Makroökonomie', desc:'Übungsklausur zu allen Makrothemen', pdf:'/assets/pdfs/Übungsheft_W_2.pdf', podcast:'/assets/audio/klausur-makro.mp3', text:'/assets/texte/klausur-makro.pdf' },
    ]
  }
];

/* ─── Fortschritt (localStorage mit Fallback) ─── */
const KEY = 'vwl-progress';
let memStore = {};
function getProgress() {
  try { return JSON.parse(localStorage.getItem(KEY)) || {}; }
  catch { return memStore; }
}
function saveProgress(p) {
  try { localStorage.setItem(KEY, JSON.stringify(p)); }
  catch { memStore = p; }
}

const iconPdf  = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6"/></svg>';
const iconQuiz = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 9a3 3 0 1 1 4 2.83c-.7.26-1 .95-1 1.67v.5"/><path d="M12 17.5h.01"/></svg>';
const iconPod  = '<svg viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg>';
const iconText = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 6h16M4 12h16M4 18h10"/></svg>';
const iconCheck= '<svg viewBox="0 0 12 12" fill="none" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg>';

/* ─── Rendern ─── */
function actionsFor(m) {
  let html = `<a href="${m.pdf}" class="mw-btn">${iconPdf} Folien</a>`;
  if (m.quiz) html += `<a href="${m.quiz}" class="mw-btn">${iconQuiz} Quiz</a>`;
  if (m.podcast) html += `<button class="mw-btn" onclick="startPodcast('${m.nr}', '${m.titel.replace(/'/g, "\\'")}', '${m.podcast}')">${iconPod} Podcast</button>`;
  if (m.text) html += `<a href="${m.text}" class="mw-btn">${iconText} Text</a>`;
  return html;
}

function render() {
  const wrap = document.getElementById('kapitel');
  let total = 0;
  wrap.innerHTML = KAPITEL.map(k => {
    total += k.module.length;
    return `
    <section class="mw-kapitel">
      <div class="mw-kapitel-kopf">
        <span class="mw-numeral">${k.numeral}</span>
        <h2>${k.titel}</h2>
        <span class="mw-meta">${k.meta}</span>
      </div>
      <div class="mw-liste">
        ${k.module.map(m => `
          <div class="mw-modul" data-module="${m.id}">
            <span class="mw-nr">${m.nr}</span>
            <div>
              <h4>${m.titel}</h4>
              ${m.desc ? `<p class="mw-desc">${m.desc}</p>` : ''}
            </div>
            <div class="mw-actions">
              ${actionsFor(m)}
              <button class="mw-check" onclick="toggleModule('${m.id}')" aria-label="Als erledigt markieren">${iconCheck}</button>
            </div>
          </div>
        `).join('')}
      </div>
    </section>
  `;
  }).join('');
  document.getElementById('ringTotal').textContent = total;
  updateUI();
}

function updateUI() {
  const p = getProgress();
  const total = KAPITEL.reduce((sum, k) => sum + k.module.length, 0);
  let done = 0;
  document.querySelectorAll('.mw-modul').forEach(el => {
    const on = !!p[el.dataset.module];
    el.classList.toggle('done', on);
    if (on) done++;
  });
  const r = 52, umfang = 2 * Math.PI * r;
  const fg = document.getElementById('ringFg');
  fg.style.strokeDasharray = umfang;
  fg.style.strokeDashoffset = umfang * (1 - (total ? done / total : 0));
  document.getElementById('ringLabel').textContent = done;
}

function toggleModule(id) {
  const p = getProgress();
  if (p[id]) delete p[id]; else p[id] = Date.now();
  saveProgress(p);
  updateUI();
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
