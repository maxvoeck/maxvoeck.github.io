---
layout: page
title: 
permalink: /teaching/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Space+Grotesk:wght@400;500;600&display=swap');

:root {
  --bg-deep: #0a0a0f;
  --bg-card: rgba(255,255,255,0.06);
  --bg-card-hover: rgba(255,255,255,0.09);
  --border: rgba(255,255,255,0.08);
  --border-hover: rgba(255,255,255,0.14);
  --text-primary: rgba(255,255,255,0.92);
  --text-secondary: rgba(255,255,255,0.55);
  --text-muted: rgba(255,255,255,0.32);
  --accent-1: #6366f1;
  --accent-2: #8b5cf6;
  --accent-3: #a78bfa;
  --math: #ec4899;
  --math-soft: rgba(236, 72, 153, 0.12);
  --econ: #f59e0b;
  --econ-soft: rgba(245, 158, 11, 0.12);
  --cs: #3b82f6;
  --cs-soft: rgba(59, 130, 246, 0.12);
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-deep) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }
a { color: var(--text-secondary); }
a:hover { color: var(--text-primary); text-decoration: none; }

/* ═══ AMBIENT ═══ */
.te-ambient {
  position: fixed; top: 0; left: 0; right: 0; bottom: 0;
  z-index: 0; overflow: hidden; pointer-events: none;
}
.te-ambient-orb {
  position: absolute; border-radius: 50%;
  filter: blur(120px); opacity: 0.4;
  animation: te-drift 20s ease-in-out infinite;
}
.te-ambient-orb:nth-child(1) {
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(236, 72, 153, 0.18) 0%, transparent 70%);
  top: -10%; left: -8%;
}
.te-ambient-orb:nth-child(2) {
  width: 450px; height: 450px;
  background: radial-gradient(circle, rgba(245, 158, 11, 0.14) 0%, transparent 70%);
  top: 50%; right: -10%;
  animation-delay: -8s; animation-duration: 24s;
}
.te-ambient-orb:nth-child(3) {
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.14) 0%, transparent 70%);
  bottom: -8%; left: 30%;
  animation-delay: -14s; animation-duration: 22s;
}
@keyframes te-drift {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(25px, -18px) scale(1.04); }
  50% { transform: translate(-18px, 25px) scale(0.96); }
  75% { transform: translate(12px, 12px) scale(1.02); }
}
.te-ambient::after {
  content: ''; position: absolute; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  opacity: 0.4; pointer-events: none;
}

/* ═══ CONTENT ═══ */
.te-content {
  position: relative; z-index: 1;
  max-width: 780px; margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  font-family: 'Inter', -apple-system, sans-serif;
}

/* ═══ HERO ═══ */
.te-hero {
  background: var(--bg-card);
  backdrop-filter: blur(40px); -webkit-backdrop-filter: blur(40px);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.5rem 2.25rem 2rem;
  margin-bottom: 3rem;
  position: relative; overflow: hidden;
}
.te-hero::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
}
.te-hero-eyebrow {
  font-size: 0.72rem; font-weight: 500;
  letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--accent-3); margin-bottom: 0.75rem;
}
.te-hero h1 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 2.5rem; font-weight: 600;
  letter-spacing: -0.03em; line-height: 1.1;
  margin-bottom: 0.5rem;
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.te-hero-sub {
  font-size: 0.92rem; color: var(--text-secondary);
  font-weight: 300; line-height: 1.8;
}

/* ═══ CARDS GRID ═══ */
.te-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
  margin-bottom: 2rem;
}

.te-card {
  background: var(--bg-card);
  backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 2rem 2rem 1.75rem;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative; overflow: hidden;
  text-decoration: none !important;
  display: block;
}
.te-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
  opacity: 0; transition: opacity 0.3s ease;
}
.te-card:hover {
  background: var(--bg-card-hover); border-color: var(--border-hover);
  transform: translateY(-3px);
  box-shadow: 0 12px 40px rgba(0,0,0,0.3);
  text-decoration: none !important;
}
.te-card:hover::before { opacity: 1; }

/* Card accent border */
.te-card--math { border-left: 2px solid var(--math); }
.te-card--econ { border-left: 2px solid var(--econ); }
.te-card--cs { border-left: 2px solid var(--cs); }

.te-card--math:hover { box-shadow: 0 12px 40px rgba(236,72,153,0.08); }
.te-card--econ:hover { box-shadow: 0 12px 40px rgba(245,158,11,0.08); }
.te-card--cs:hover { box-shadow: 0 12px 40px rgba(59,130,246,0.08); }

/* Card header */
.te-card-head {
  display: flex; align-items: center; gap: 1rem;
  margin-bottom: 1rem;
}

.te-card-icon {
  width: 44px; height: 44px; border-radius: 12px;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0; transition: all 0.3s ease;
}
.te-card--math .te-card-icon { background: var(--math-soft); border: 1px solid rgba(236,72,153,0.2); }
.te-card--econ .te-card-icon { background: var(--econ-soft); border: 1px solid rgba(245,158,11,0.2); }
.te-card--cs .te-card-icon { background: var(--cs-soft); border: 1px solid rgba(59,130,246,0.2); }

.te-card-icon svg {
  width: 22px; height: 22px; transition: all 0.3s ease;
}
.te-card--math .te-card-icon svg { fill: var(--math); }
.te-card--econ .te-card-icon svg { fill: var(--econ); }
.te-card--cs .te-card-icon svg { fill: var(--cs); }

.te-card:hover .te-card-icon { transform: scale(1.08); }

.te-card-title-wrap { flex: 1; }

.te-card h2 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.25rem; font-weight: 500;
  letter-spacing: -0.01em; margin: 0;
  color: var(--text-primary) !important;
  transition: color 0.3s ease;
}
.te-card--math:hover h2 { color: var(--math) !important; }
.te-card--econ:hover h2 { color: var(--econ) !important; }
.te-card--cs:hover h2 { color: var(--cs) !important; }

.te-card-count {
  font-size: 0.72rem; color: var(--text-muted);
  font-weight: 400; margin-top: 0.15rem;
}

/* Card body */
.te-card-desc {
  font-size: 0.85rem; color: var(--text-secondary);
  font-weight: 300; line-height: 1.7;
  margin-bottom: 1.25rem;
}

/* Tags */
.te-tags { display: flex; flex-wrap: wrap; gap: 0.45rem; margin-bottom: 1.5rem; }

.te-tag {
  padding: 0.3rem 0.75rem; border-radius: 8px;
  font-size: 0.72rem; font-weight: 500;
  letter-spacing: 0.03em; transition: all 0.3s ease;
  border: 1px solid var(--border);
  color: var(--text-muted); background: transparent;
}
.te-card--math .te-tag { color: rgba(236,72,153,0.7); border-color: rgba(236,72,153,0.15); }
.te-card--econ .te-tag { color: rgba(245,158,11,0.7); border-color: rgba(245,158,11,0.15); }
.te-card--cs .te-tag { color: rgba(59,130,246,0.7); border-color: rgba(59,130,246,0.15); }

.te-card:hover .te-tag { border-color: var(--border-hover); }
.te-card--math:hover .te-tag { background: var(--math-soft); border-color: rgba(236,72,153,0.25); color: var(--math); }
.te-card--econ:hover .te-tag { background: var(--econ-soft); border-color: rgba(245,158,11,0.25); color: var(--econ); }
.te-card--cs:hover .te-tag { background: var(--cs-soft); border-color: rgba(59,130,246,0.25); color: var(--cs); }

/* Card actions */
.te-card-actions { display: flex; gap: 0.6rem; flex-wrap: wrap; }

.te-btn {
  display: inline-flex; align-items: center; gap: 0.4rem;
  padding: 0.6rem 1.15rem; border-radius: 10px;
  font-size: 0.78rem; font-weight: 500;
  letter-spacing: 0.04em; text-transform: uppercase;
  text-decoration: none !important;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.03);
  color: var(--text-secondary) !important;
  transition: all 0.25s ease;
}
.te-btn:hover {
  transform: translateY(-1px); border-color: var(--border-hover);
  background: rgba(255,255,255,0.08);
  color: var(--text-primary) !important;
  box-shadow: 0 4px 16px rgba(0,0,0,0.2);
}
.te-card--math .te-btn:first-child:hover { border-color: rgba(236,72,153,0.4); box-shadow: 0 4px 16px rgba(236,72,153,0.1); }
.te-card--econ .te-btn:first-child:hover { border-color: rgba(245,158,11,0.4); box-shadow: 0 4px 16px rgba(245,158,11,0.1); }
.te-card--cs .te-btn:first-child:hover { border-color: rgba(59,130,246,0.4); box-shadow: 0 4px 16px rgba(59,130,246,0.1); }

.te-btn--secondary:hover { border-color: var(--border-hover); }

/* Arrow on hover */
.te-btn-arrow {
  opacity: 0; transform: translateX(-4px);
  transition: all 0.25s ease;
  font-size: 0.85rem;
}
.te-btn:hover .te-btn-arrow {
  opacity: 1; transform: translateX(0);
}

/* ═══ FOOTER NOTE ═══ */
.te-footer {
  text-align: center; color: var(--text-muted);
  margin-top: 2rem; padding-top: 2rem;
  border-top: 1px solid var(--border);
  font-size: 0.82rem; font-weight: 300;
  letter-spacing: 0.01em; line-height: 1.7;
}

/* ═══ ANIMATIONS ═══ */
@keyframes te-fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}
.te-hero { animation: te-fadeUp 0.6s ease both; }
.te-card { animation: te-fadeUp 0.5s ease both; }
.te-card:nth-child(1) { animation-delay: 0.1s; }
.te-card:nth-child(2) { animation-delay: 0.2s; }
.te-card:nth-child(3) { animation-delay: 0.3s; }

/* ═══ RESPONSIVE ═══ */
@media (max-width: 768px) {
  .te-content { padding: 1.5rem 1rem 4rem; }
  .te-hero { padding: 2rem 1.5rem 1.5rem; border-radius: 20px; }
  .te-hero h1 { font-size: 1.9rem; }
  .te-card { padding: 1.5rem 1.5rem 1.5rem; border-radius: 16px; }
  .te-card h2 { font-size: 1.1rem; }
  .te-card-actions { flex-direction: column; }
  .te-btn { justify-content: center; }
}
</style>

<!-- AMBIENT -->
<div class="te-ambient">
  <div class="te-ambient-orb"></div>
  <div class="te-ambient-orb"></div>
  <div class="te-ambient-orb"></div>
</div>

<div class="te-content">

  <!-- HERO -->
  <div class="te-hero">
    <div class="te-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Lehrmaterialien</h1>
    <p class="te-hero-sub">Ausgewählte Materialien aus meiner Lehrtätigkeit. Alle Unterlagen sind speziell auf die Anforderungen der Feststellungsprüfung (FSP) abgestimmt.</p>
  </div>

  <!-- CARDS -->
  <div class="te-grid">

    <!-- MATHEMATIK -->
    <div class="te-card te-card--math">
      <div class="te-card-head">
        <div class="te-card-icon">
          <svg viewBox="0 0 24 24"><path d="M18 4H8.5L14 12L8.5 20H18V18H11.5L16 12L11.5 6H18V4Z"/></svg>
        </div>
        <div class="te-card-title-wrap">
          <h2>Mathematik</h2>
          <div class="te-card-count">28 Module · 3 interaktive Tools</div>
        </div>
      </div>
      <p class="te-card-desc">Fundierte Vorbereitung auf Analysis und Lineare Algebra für technische Studiengänge – von Vektorrechnung bis Rotationsvolumen</p>
      <div class="te-tags">
        <span class="te-tag">Vektorrechnung</span>
        <span class="te-tag">Lineare Algebra</span>
        <span class="te-tag">Differentialrechnung</span>
        <span class="te-tag">Integralrechnung</span>
      </div>
      <div class="te-card-actions">
        <a href="/teaching/mathematik/" class="te-btn" onclick="event.stopPropagation()"><span>Lernpfad öffnen</span><span class="te-btn-arrow">→</span></a>
        <a href="/assets/pdfs/Mathematik_Skript.pdf" class="te-btn te-btn--secondary" onclick="event.stopPropagation()"><span>📄 Gesamtskript</span></a>
      </div>
    </div>

    <!-- VWL -->
    <div class="te-card te-card--econ">
      <div class="te-card-head">
        <div class="te-card-icon">
          <svg viewBox="0 0 24 24"><path d="M3 14L5 12L9 16L14 11L16 13L21 8V18C21 19.1 20.1 20 19 20H5C3.9 20 3 19.1 3 18V14ZM21 5V7L16 12L14 10L9 15L5 11L3 13V5C3 3.9 3.9 3 5 3H19C20.1 3 21 3.9 21 5Z"/></svg>
        </div>
        <div class="te-card-title-wrap">
          <h2>Volkswirtschaftslehre</h2>
          <div class="te-card-count">13 Module · Mikro & Makro</div>
        </div>
      </div>
      <p class="te-card-desc">Makro- und Mikroökonomie mit praxisnahen Beispielen – von Bedürfnissen bis zur Arbeitsmarktpolitik</p>
      <div class="te-tags">
        <span class="te-tag">Marktgleichgewicht</span>
        <span class="te-tag">Konsumentenrente</span>
        <span class="te-tag">BIP & Konjunktur</span>
        <span class="te-tag">Wirtschaftspolitik</span>
      </div>
      <div class="te-card-actions">
        <a href="/teaching/vwl/" class="te-btn" onclick="event.stopPropagation()"><span>Lernpfad öffnen</span><span class="te-btn-arrow">→</span></a>
      </div>
    </div>

    <!-- INFORMATIK -->
    <div class="te-card te-card--cs">
      <div class="te-card-head">
        <div class="te-card-icon">
          <svg viewBox="0 0 24 24"><path d="M8 3L4 7L8 11L9.4 9.6L6.8 7L9.4 4.4L8 3ZM16 3L14.6 4.4L17.2 7L14.6 9.6L16 11L20 7L16 3ZM10 13L12 21L14 20L12 12L10 13Z"/></svg>
        </div>
        <div class="te-card-title-wrap">
          <h2>Informatik</h2>
          <div class="te-card-count">5 Module · Python</div>
        </div>
      </div>
      <p class="te-card-desc">Grundlagen der Programmierung und algorithmisches Denken – von print() bis zu eigenen Funktionen</p>
      <div class="te-tags">
        <span class="te-tag">Python</span>
        <span class="te-tag">Kontrollstrukturen</span>
        <span class="te-tag">Listen</span>
        <span class="te-tag">Funktionen</span>
      </div>
      <div class="te-card-actions">
        <a href="/teaching/informatik/" class="te-btn" onclick="event.stopPropagation()"><span>Lernpfad öffnen</span><span class="te-btn-arrow">→</span></a>
      </div>
    </div>

  </div>

  <div class="te-footer">
    Alle Materialien frei verwendbar für Bildungszwecke
  </div>

</div>