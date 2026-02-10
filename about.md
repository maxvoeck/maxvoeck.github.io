---
layout: page
title: 
permalink: /about/
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
  --edu: #f59e0b;
  --edu-soft: rgba(245, 158, 11, 0.12);
  --focus: #ec4899;
  --focus-soft: rgba(236, 72, 153, 0.12);
  --interests: #06b6d4;
  --interests-soft: rgba(6, 182, 212, 0.12);
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-deep) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }
a { color: var(--accent-3); }
a:hover { color: #c4b5fd; text-decoration: none; }

/* ═══ AMBIENT ═══ */
.ab-ambient {
  position: fixed; top: 0; left: 0; right: 0; bottom: 0;
  z-index: 0; overflow: hidden; pointer-events: none;
}
.ab-ambient-orb {
  position: absolute; border-radius: 50%;
  filter: blur(120px); opacity: 0.4;
  animation: ab-drift 20s ease-in-out infinite;
}
.ab-ambient-orb:nth-child(1) {
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.2) 0%, transparent 70%);
  top: -10%; right: -8%;
}
.ab-ambient-orb:nth-child(2) {
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(139, 92, 246, 0.15) 0%, transparent 70%);
  bottom: 10%; left: -8%;
  animation-delay: -9s; animation-duration: 24s;
}
.ab-ambient-orb:nth-child(3) {
  width: 350px; height: 350px;
  background: radial-gradient(circle, rgba(6, 182, 212, 0.1) 0%, transparent 70%);
  top: 40%; left: 50%;
  animation-delay: -14s; animation-duration: 22s;
}
@keyframes ab-drift {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(25px, -18px) scale(1.04); }
  50% { transform: translate(-18px, 25px) scale(0.96); }
  75% { transform: translate(12px, 12px) scale(1.02); }
}
.ab-ambient::after {
  content: ''; position: absolute; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  opacity: 0.4; pointer-events: none;
}

/* ═══ CONTENT ═══ */
.ab-content {
  position: relative; z-index: 1;
  max-width: 780px; margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  font-family: 'Inter', -apple-system, sans-serif;
}

/* ═══ HERO ═══ */
.ab-hero {
  background: var(--bg-card);
  backdrop-filter: blur(40px); -webkit-backdrop-filter: blur(40px);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.5rem 2.25rem 2rem;
  margin-bottom: 2rem;
  position: relative; overflow: hidden;
}
.ab-hero::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
}
.ab-hero-eyebrow {
  font-size: 0.72rem; font-weight: 500;
  letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--accent-3); margin-bottom: 0.75rem;
}
.ab-hero h1 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 2.5rem; font-weight: 600;
  letter-spacing: -0.03em; line-height: 1.1;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.ab-hero-text {
  font-size: 0.95rem; color: var(--text-secondary);
  font-weight: 300; line-height: 1.85;
}

/* ═══ CARDS ═══ */
.ab-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
}

.ab-card {
  background: var(--bg-card);
  backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 2rem 2rem 1.75rem;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative; overflow: hidden;
}
.ab-card::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
  opacity: 0; transition: opacity 0.3s ease;
}
.ab-card:hover {
  background: var(--bg-card-hover); border-color: var(--border-hover);
  transform: translateY(-3px);
  box-shadow: 0 12px 40px rgba(0,0,0,0.3);
}
.ab-card:hover::before { opacity: 1; }

.ab-card--edu { border-left: 2px solid var(--edu); }
.ab-card--focus { border-left: 2px solid var(--focus); }
.ab-card--interests { border-left: 2px solid var(--interests); }

.ab-card--edu:hover { box-shadow: 0 12px 40px rgba(245,158,11,0.06); }
.ab-card--focus:hover { box-shadow: 0 12px 40px rgba(236,72,153,0.06); }
.ab-card--interests:hover { box-shadow: 0 12px 40px rgba(6,182,212,0.06); }

/* Card header */
.ab-card-head {
  display: flex; align-items: center; gap: 0.85rem;
  margin-bottom: 1.25rem;
}

.ab-card-badge {
  width: 36px; height: 36px; border-radius: 10px;
  display: flex; align-items: center; justify-content: center;
  font-size: 0.9rem; flex-shrink: 0;
}
.ab-card--edu .ab-card-badge { background: var(--edu-soft); border: 1px solid rgba(245,158,11,0.2); }
.ab-card--focus .ab-card-badge { background: var(--focus-soft); border: 1px solid rgba(236,72,153,0.2); }
.ab-card--interests .ab-card-badge { background: var(--interests-soft); border: 1px solid rgba(6,182,212,0.2); }

.ab-card h2 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.2rem; font-weight: 500;
  letter-spacing: -0.01em; margin: 0;
  color: var(--text-primary);
}

/* Education items */
.ab-edu-item {
  margin-bottom: 1.25rem;
  padding-left: 0.25rem;
}
.ab-edu-item:last-child { margin-bottom: 0; }

.ab-edu-title {
  display: block;
  font-size: 0.92rem; font-weight: 500;
  color: var(--text-primary);
  margin-bottom: 0.15rem;
}
.ab-edu-place {
  font-size: 0.8rem; color: var(--text-muted);
  font-weight: 400; letter-spacing: 0.02em;
}

/* List items */
.ab-list {
  list-style: none; padding: 0; margin: 0;
}
.ab-list li {
  position: relative;
  padding-left: 1.4rem;
  margin-bottom: 1.1rem;
  font-size: 0.88rem;
  color: var(--text-secondary);
  font-weight: 300;
  line-height: 1.8;
}
.ab-list li:last-child { margin-bottom: 0; }

.ab-list li::before {
  content: '';
  position: absolute;
  left: 0; top: 0.6rem;
  width: 6px; height: 6px;
  border-radius: 50%;
}

.ab-card--focus .ab-list li::before { background: var(--focus); opacity: 0.6; }
.ab-card--interests .ab-list li::before { background: var(--interests); opacity: 0.6; }

.ab-list li strong {
  color: var(--text-primary);
  font-weight: 500;
}

/* ═══ ANIMATIONS ═══ */
@keyframes ab-fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}
.ab-hero { animation: ab-fadeUp 0.6s ease both; }
.ab-card { animation: ab-fadeUp 0.5s ease both; }
.ab-card:nth-child(1) { animation-delay: 0.1s; }
.ab-card:nth-child(2) { animation-delay: 0.2s; }
.ab-card:nth-child(3) { animation-delay: 0.3s; }

/* ═══ RESPONSIVE ═══ */
@media (max-width: 768px) {
  .ab-content { padding: 1.5rem 1rem 4rem; }
  .ab-hero { padding: 2rem 1.5rem 1.5rem; border-radius: 20px; }
  .ab-hero h1 { font-size: 1.9rem; }
  .ab-card { padding: 1.5rem; border-radius: 16px; }
  .ab-card h2 { font-size: 1.1rem; }
}
</style>

<!-- AMBIENT -->
<div class="ab-ambient">
  <div class="ab-ambient-orb"></div>
  <div class="ab-ambient-orb"></div>
  <div class="ab-ambient-orb"></div>
</div>

<div class="ab-content">

  <!-- HERO -->
  <div class="ab-hero">
    <div class="ab-hero-eyebrow">Über mich</div>
    <h1>Maximilian Vöcklinghaus</h1>
    <p class="ab-hero-text">Dozent am Studienkolleg der Rahn Education in Leipzig. Ich begleite internationale Studierende auf ihrem Weg ins deutsche Hochschulstudium und unterrichte Mathematik, Informatik und Volkswirtschaftslehre.</p>
  </div>

  <!-- CARDS -->
  <div class="ab-grid">

    <div class="ab-card ab-card--edu">
      <div class="ab-card-head">
        <div class="ab-card-badge">🎓</div>
        <h2>Ausbildung</h2>
      </div>
      <div class="ab-edu-item">
        <span class="ab-edu-title">Bachelor in Mathematik</span>
        <span class="ab-edu-place">Heinrich-Heine-Universität Düsseldorf</span>
      </div>
      <div class="ab-edu-item">
        <span class="ab-edu-title">Data Science Master</span>
        <span class="ab-edu-place">RWTH Aachen</span>
      </div>
    </div>

    <div class="ab-card ab-card--focus">
      <div class="ab-card-head">
        <div class="ab-card-badge">◎</div>
        <h2>Schwerpunkte</h2>
      </div>
      <ul class="ab-list">
        <li><strong>Mathematik & Data Science:</strong> Von Analysis und linearer Algebra bis zu praktischer Datenanalyse</li>
        <li><strong>Wirtschaftswissenschaften:</strong> Volkswirtschaftslehre, Marktanalysen, kritische Wirtschaftstheorie</li>
        <li><strong>Didaktik & Bildung:</strong> Entwicklung interaktiver Lernmaterialien und digitaler Bildungsressourcen</li>
      </ul>
    </div>

    <div class="ab-card ab-card--interests">
      <div class="ab-card-head">
        <div class="ab-card-badge">✦</div>
        <h2>Interessen</h2>
      </div>
      <ul class="ab-list">
        <li>Kritische Theorie und Kulturanalyse</li>
        <li>Wirtschaftsphilosophie</li>
        <li>Schnittstelle zwischen quantitativen Methoden und gesellschaftlicher Analyse</li>
      </ul>
    </div>

  </div>

</div>