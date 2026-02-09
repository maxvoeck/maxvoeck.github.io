---
layout: page
title: 
permalink: /teaching/mathematik/
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
  
  --vektor: #f59e0b;
  --vektor-soft: rgba(245, 158, 11, 0.12);
  --algebra: #06b6d4;
  --algebra-soft: rgba(6, 182, 212, 0.12);
  --diff: #ec4899;
  --diff-soft: rgba(236, 72, 153, 0.12);
  --integral: #10b981;
  --integral-soft: rgba(16, 185, 129, 0.12);
  --tools: #f97316;
  --tools-soft: rgba(249, 115, 22, 0.12);
  
  --success: #34d399;
  --success-soft: rgba(52, 211, 153, 0.12);
  
  --radius: 16px;
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-deep) !important;
  color: var(--text-primary);
}

.post-header, .page-heading, header.post-header { display: none !important; }
a { color: var(--text-secondary); }
a:hover { color: var(--text-primary); }

/* ═══════════════════════════════════════
   AMBIENT
   ═══════════════════════════════════════ */

.ma-ambient {
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  z-index: 0;
  overflow: hidden;
  pointer-events: none;
}

.ma-ambient-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(120px);
  opacity: 0.45;
  animation: ma-drift 20s ease-in-out infinite;
}

.ma-ambient-orb:nth-child(1) {
  width: 550px; height: 550px;
  background: radial-gradient(circle, rgba(236, 72, 153, 0.2) 0%, transparent 70%);
  top: -12%; left: -8%;
  animation-delay: 0s;
}

.ma-ambient-orb:nth-child(2) {
  width: 450px; height: 450px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.18) 0%, transparent 70%);
  top: 35%; right: -12%;
  animation-delay: -8s; animation-duration: 24s;
}

.ma-ambient-orb:nth-child(3) {
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(16, 185, 129, 0.12) 0%, transparent 70%);
  bottom: -8%; left: 15%;
  animation-delay: -14s; animation-duration: 22s;
}

.ma-ambient-orb:nth-child(4) {
  width: 350px; height: 350px;
  background: radial-gradient(circle, rgba(245, 158, 11, 0.1) 0%, transparent 70%);
  top: 55%; left: -5%;
  animation-delay: -4s; animation-duration: 19s;
}

@keyframes ma-drift {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(25px, -18px) scale(1.04); }
  50% { transform: translate(-18px, 25px) scale(0.96); }
  75% { transform: translate(12px, 12px) scale(1.02); }
}

.ma-ambient::after {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  opacity: 0.4;
  pointer-events: none;
}

/* ═══════════════════════════════════════
   CONTENT
   ═══════════════════════════════════════ */

.ma-content {
  position: relative;
  z-index: 1;
  max-width: 780px;
  margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  font-family: 'Inter', -apple-system, sans-serif;
}

/* ═══════════════════════════════════════
   HERO
   ═══════════════════════════════════════ */

.ma-hero {
  background: var(--bg-card);
  backdrop-filter: blur(40px);
  -webkit-backdrop-filter: blur(40px);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.5rem 2.25rem 2rem;
  margin-bottom: 3rem;
  position: relative;
  overflow: hidden;
}

.ma-hero::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
}

.ma-hero-eyebrow {
  font-size: 0.72rem;
  font-weight: 500;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--accent-3);
  margin-bottom: 0.75rem;
}

.ma-hero h1 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 2.5rem;
  font-weight: 600;
  letter-spacing: -0.03em;
  line-height: 1.1;
  margin-bottom: 0.4rem;
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.ma-hero-sub {
  font-size: 0.92rem;
  color: var(--text-secondary);
  font-weight: 300;
  margin-bottom: 2rem;
}

.ma-progress-track {
  background: rgba(255,255,255,0.06);
  border-radius: 100px;
  height: 4px;
  overflow: hidden;
  margin-bottom: 0.75rem;
}

.ma-progress-fill {
  height: 100%;
  border-radius: 100px;
  background: linear-gradient(90deg, var(--diff), var(--accent-2), var(--accent-3));
  width: 0%;
  transition: width 0.8s cubic-bezier(0.23, 1, 0.32, 1);
  box-shadow: 0 0 12px rgba(236, 72, 153, 0.3);
}

.ma-progress-meta {
  display: flex;
  justify-content: space-between;
}

.ma-progress-meta span {
  font-size: 0.75rem;
  color: var(--text-muted);
  font-weight: 400;
}

.ma-progress-meta .ma-pct {
  color: var(--accent-3);
  font-weight: 500;
}

/* ═══════════════════════════════════════
   SECTIONS
   ═══════════════════════════════════════ */

.ma-section { margin-bottom: 3rem; }

.ma-section-head {
  display: flex;
  align-items: center;
  gap: 0.85rem;
  margin-bottom: 0.4rem;
  padding: 0 0.25rem;
}

.ma-section-badge {
  width: 36px; height: 36px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.ma-section--vektor .ma-section-badge { background: var(--vektor-soft); color: var(--vektor); border: 1px solid rgba(245,158,11,0.2); }
.ma-section--algebra .ma-section-badge { background: var(--algebra-soft); color: var(--algebra); border: 1px solid rgba(6,182,212,0.2); }
.ma-section--diff .ma-section-badge { background: var(--diff-soft); color: var(--diff); border: 1px solid rgba(236,72,153,0.2); }
.ma-section--integral .ma-section-badge { background: var(--integral-soft); color: var(--integral); border: 1px solid rgba(16,185,129,0.2); }
.ma-section--tools .ma-section-badge { background: var(--tools-soft); color: var(--tools); border: 1px solid rgba(249,115,22,0.2); }

.ma-section-title {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.35rem;
  font-weight: 500;
  letter-spacing: -0.01em;
  color: var(--text-primary);
  margin: 0;
}

.ma-section-meta {
  font-size: 0.78rem;
  color: var(--text-muted);
  padding-left: calc(36px + 0.85rem + 0.25rem);
  margin-bottom: 1.5rem;
}

/* ═══════════════════════════════════════
   TIMELINE
   ═══════════════════════════════════════ */

.ma-path {
  position: relative;
  padding-left: 2.5rem;
}

.ma-path::before {
  content: '';
  position: absolute;
  left: 17px;
  top: 20px; bottom: 20px;
  width: 1px;
  background: linear-gradient(180deg, var(--border) 0%, rgba(255,255,255,0.03) 100%);
}

.ma-module {
  position: relative;
  margin-bottom: 0.75rem;
}

.ma-module-dot {
  position: absolute;
  left: -2.5rem;
  top: 50%;
  transform: translateY(-50%);
  width: 11px; height: 11px;
  border-radius: 50%;
  background: var(--bg-deep);
  border: 2px solid var(--border);
  z-index: 2;
  transition: all 0.3s ease;
}

.ma-module.is-complete .ma-module-dot {
  background: var(--success);
  border-color: var(--success);
  box-shadow: 0 0 8px rgba(52,211,153,0.3);
}

/* ═══════════════════════════════════════
   CARD
   ═══════════════════════════════════════ */

.ma-card {
  background: var(--bg-card);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 1.35rem 1.5rem;
  transition: all 0.35s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative;
  overflow: hidden;
}

.ma-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.ma-card:hover {
  background: var(--bg-card-hover);
  border-color: var(--border-hover);
  transform: translateY(-2px);
  box-shadow: 0 8px 32px rgba(0,0,0,0.3);
}

.ma-card:hover::before { opacity: 1; }

.ma-module.is-complete .ma-card {
  border-left: 2px solid var(--success);
}

.ma-card-top {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  margin-bottom: 0.3rem;
}

.ma-step-num {
  font-size: 0.65rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 0.15rem 0.55rem;
  border-radius: 6px;
  flex-shrink: 0;
}

.ma-section--vektor .ma-step-num { color: var(--vektor); background: var(--vektor-soft); }
.ma-section--algebra .ma-step-num { color: var(--algebra); background: var(--algebra-soft); }
.ma-section--diff .ma-step-num { color: var(--diff); background: var(--diff-soft); }
.ma-section--integral .ma-step-num { color: var(--integral); background: var(--integral-soft); }
.ma-section--tools .ma-step-num { color: var(--tools); background: var(--tools-soft); }

.ma-module.is-complete .ma-step-num { color: var(--success); background: var(--success-soft); }

.ma-card h4 {
  font-size: 0.95rem;
  font-weight: 500;
  color: var(--text-primary);
  margin: 0;
  line-height: 1.45;
}

.ma-card-desc {
  font-size: 0.82rem;
  color: var(--text-secondary);
  font-weight: 300;
  line-height: 1.7;
  margin: 0.25rem 0 1.1rem 0;
}

/* Actions */
.ma-actions {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  flex-wrap: wrap;
}

.ma-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.55rem 1rem;
  border-radius: 10px;
  font-size: 0.76rem;
  font-weight: 500;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  text-decoration: none;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.03);
  color: var(--text-secondary) !important;
  transition: all 0.25s ease;
  cursor: pointer;
  font-family: 'Inter', -apple-system, sans-serif;
}

.ma-btn:hover {
  transform: translateY(-1px);
  border-color: var(--border-hover);
  background: rgba(255,255,255,0.08);
  color: var(--text-primary) !important;
  box-shadow: 0 4px 16px rgba(0,0,0,0.2);
  text-decoration: none;
}

.ma-section--vektor .ma-btn--pdf:hover { border-color: rgba(245,158,11,0.4); box-shadow: 0 4px 16px rgba(245,158,11,0.1); }
.ma-section--algebra .ma-btn--pdf:hover { border-color: rgba(6,182,212,0.4); box-shadow: 0 4px 16px rgba(6,182,212,0.1); }
.ma-section--diff .ma-btn--pdf:hover { border-color: rgba(236,72,153,0.4); box-shadow: 0 4px 16px rgba(236,72,153,0.1); }
.ma-section--integral .ma-btn--pdf:hover { border-color: rgba(16,185,129,0.4); box-shadow: 0 4px 16px rgba(16,185,129,0.1); }
.ma-section--tools .ma-btn--open:hover { border-color: rgba(249,115,22,0.4); box-shadow: 0 4px 16px rgba(249,115,22,0.1); }

.ma-btn--quiz:hover { border-color: rgba(99,102,241,0.4); box-shadow: 0 4px 16px rgba(99,102,241,0.1); }

.ma-check {
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 0.4rem;
  font-size: 0.72rem;
  color: var(--text-muted);
  cursor: pointer;
  padding: 0.35rem 0.55rem;
  border-radius: 8px;
  transition: all 0.2s ease;
  user-select: none;
}

.ma-check:hover { background: var(--success-soft); color: var(--success); }

.ma-check-box {
  width: 18px; height: 18px;
  border-radius: 6px;
  border: 1.5px solid var(--border);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s ease;
  flex-shrink: 0;
}

.ma-check-box svg { opacity: 0; transition: opacity 0.2s ease; width: 11px; height: 11px; }

.ma-module.is-complete .ma-check-box {
  background: var(--success);
  border-color: var(--success);
  box-shadow: 0 0 8px rgba(52,211,153,0.2);
}

.ma-module.is-complete .ma-check-box svg { opacity: 1; }
.ma-module.is-complete .ma-check { color: var(--success); }

/* ═══════════════════════════════════════
   FOOTER
   ═══════════════════════════════════════ */

.ma-footer {
  margin-top: 2rem;
  padding: 1.5rem 1.75rem;
  background: var(--bg-card);
  backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
}

.ma-footer-text { font-size: 0.8rem; color: var(--text-muted); font-weight: 300; }
.ma-footer-text strong { color: var(--text-secondary); font-weight: 500; }

.ma-footer-actions { display: flex; gap: 0.6rem; }

.ma-btn-reset {
  display: inline-flex;
  align-items: center;
  padding: 0.55rem 1rem;
  border-radius: 10px;
  font-size: 0.72rem;
  font-weight: 400;
  letter-spacing: 0.04em;
  border: 1px solid transparent;
  background: transparent;
  color: var(--text-muted) !important;
  transition: all 0.25s ease;
  cursor: pointer;
  font-family: 'Inter', -apple-system, sans-serif;
}

.ma-btn-reset:hover { border-color: var(--border); color: var(--text-secondary) !important; }

/* ═══════════════════════════════════════
   ANIMATIONS
   ═══════════════════════════════════════ */

@keyframes ma-fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}

.ma-hero { animation: ma-fadeUp 0.6s ease both; }
.ma-section { animation: ma-fadeUp 0.6s ease both; }

.ma-module { animation: ma-fadeUp 0.4s ease both; }
.ma-module:nth-child(1) { animation-delay: 0.03s; }
.ma-module:nth-child(2) { animation-delay: 0.06s; }
.ma-module:nth-child(3) { animation-delay: 0.09s; }
.ma-module:nth-child(4) { animation-delay: 0.12s; }
.ma-module:nth-child(5) { animation-delay: 0.15s; }
.ma-module:nth-child(6) { animation-delay: 0.18s; }
.ma-module:nth-child(7) { animation-delay: 0.21s; }
.ma-module:nth-child(8) { animation-delay: 0.24s; }
.ma-module:nth-child(9) { animation-delay: 0.27s; }
.ma-module:nth-child(10) { animation-delay: 0.30s; }
.ma-module:nth-child(11) { animation-delay: 0.33s; }
.ma-module:nth-child(12) { animation-delay: 0.36s; }

/* ═══════════════════════════════════════
   RESPONSIVE
   ═══════════════════════════════════════ */

@media (max-width: 768px) {
  .ma-content { padding: 1.5rem 1rem 4rem; }
  .ma-hero { padding: 2rem 1.5rem 1.5rem; border-radius: 20px; }
  .ma-hero h1 { font-size: 1.9rem; }
  .ma-path { padding-left: 2rem; }
  .ma-module-dot { left: -2rem; }
  .ma-card { padding: 1.1rem 1.2rem; }
  .ma-actions { flex-direction: column; align-items: stretch; }
  .ma-btn { justify-content: center; }
  .ma-check { margin-left: 0; justify-content: center; }
  .ma-footer { flex-direction: column; text-align: center; }
  .ma-footer-actions { width: 100%; flex-direction: column; }
  .ma-section-meta { padding-left: calc(36px + 0.85rem); }
}
</style>

<!-- AMBIENT -->
<div class="ma-ambient">
  <div class="ma-ambient-orb"></div>
  <div class="ma-ambient-orb"></div>
  <div class="ma-ambient-orb"></div>
  <div class="ma-ambient-orb"></div>
</div>

<div class="ma-content">

  <!-- HERO -->
  <div class="ma-hero">
    <div class="ma-hero-eyebrow">Studienkolleg Leipzig</div>
    <h1>Mathematik</h1>
    <p class="ma-hero-sub">25 Module + 3 interaktive Tools · Vektoren, Algebra, Analysis & Integralrechnung</p>
    <div class="ma-progress-track">
      <div class="ma-progress-fill" id="maProgressBar"></div>
    </div>
    <div class="ma-progress-meta">
      <span><span id="maCompletedCount">0</span> von <span id="maTotalCount">28</span> Modulen</span>
      <span class="ma-pct" id="maProgressPercent">0 %</span>
    </div>
  </div>

  <!-- ═══════════════════════════════════════
       VEKTORRECHNUNG
       ═══════════════════════════════════════ -->
  <div class="ma-section ma-section--vektor">
    <div class="ma-section-head">
      <div class="ma-section-badge">Ve</div>
      <h2 class="ma-section-title">Vektorrechnung & Analytische Geometrie</h2>
    </div>
    <p class="ma-section-meta">4 Module · Vom Vektor zum Raum</p>
    <div class="ma-path">

      <div class="ma-module" data-module="v1">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">01</span><h4>Vektorrechnung – Grundlagen</h4></div>
          <p class="ma-card-desc">Einführung in Vektoren, Koordinatensysteme, Skalare vs. vektorielle Größen, Betrag, Einheitsvektoren, Basisvektoren und Grundoperationen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Geo_2_1-2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_vektorrechnung_grundlagen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('v1')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="v2">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">02</span><h4>Vektorprodukt und Spatprodukt</h4></div>
          <p class="ma-card-desc">Kreuzprodukt, geometrische Bedeutung, Flächenberechnung, Spatprodukt, Volumenberechnung und Anwendungen in der Raumgeometrie</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Geo_2_2-2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_vektorprodukt.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('v2')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="v3">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">03</span><h4>Geraden und Ebenen im Raum</h4></div>
          <p class="ma-card-desc">Parametergleichungen von Geraden und Ebenen, Normalenvektor, Koordinatenform, Lagebeziehungen und Schnittwinkelberechnung</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Geo_2_3.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_geraden_ebenen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('v3')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="v4">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">04</span><h4>Lagebeziehungen und Abstände</h4></div>
          <p class="ma-card-desc">Ebene-Ebene-Lagen, Abstandsberechnungen zwischen Punkten, Geraden und Ebenen, Hessesche Normalenform und praktische Anwendungen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Geo_2_4.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_lagebeziehungen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('v4')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- ═══════════════════════════════════════
       LINEARE ALGEBRA
       ═══════════════════════════════════════ -->
  <div class="ma-section ma-section--algebra">
    <div class="ma-section-head">
      <div class="ma-section-badge">Al</div>
      <h2 class="ma-section-title">Lineare Algebra</h2>
    </div>
    <p class="ma-section-meta">5 Module · Matrizen, Determinanten & LGS</p>
    <div class="ma-path">

      <div class="ma-module" data-module="a1">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">05</span><h4>Matrizen – Einführung und Rechenoperationen</h4></div>
          <p class="ma-card-desc">Grundlagen der Matrizenrechnung: Addition, Multiplikation, Transponieren, spezielle Matrizen und Rechenregeln mit praktischen Beispielen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Matrizen_2_1-5.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_matrizen_grundlagen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('a1')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="a2">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">06</span><h4>Determinanten – Grundlagen und Rechenregeln</h4></div>
          <p class="ma-card-desc">Determinantenberechnung, Laplace-Entwicklung, Sarrus-Regel, reguläre/singuläre Matrizen, geometrische Bedeutung und Inverse Matrizen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Matrizen_2_2-2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_determinanten.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('a2')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="a3">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">07</span><h4>Matrizengleichungen – Übungsaufgaben</h4></div>
          <p class="ma-card-desc">Umfangreiche Übungsaufgaben zu Matrizengleichungen, Rangbestimmung, Gauß-Elimination und Lösungsstrategien</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Matrizen_2_3-3.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <label class="ma-check" onclick="maToggle('a3')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="a4">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">08</span><h4>Lineare Gleichungssysteme – Grundlagen</h4></div>
          <p class="ma-card-desc">Einführung in LGS, Matrixschreibweise, Gauß-Algorithmus, Lösbarkeitskriterien und praktische Anwendungen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/LGS_2_1-5.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_lgs_grundlagen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('a4')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="a5">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">09</span><h4>LGS – Parameterabhängigkeit</h4></div>
          <p class="ma-card-desc">Untersuchung von LGS mit Parametern, Determinantentest, Fallunterscheidungen und Lösbarkeitsanalyse</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/LGS_2_2-2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <label class="ma-check" onclick="maToggle('a5')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- ═══════════════════════════════════════
       DIFFERENTIALRECHNUNG
       ═══════════════════════════════════════ -->
  <div class="ma-section ma-section--diff">
    <div class="ma-section-head">
      <div class="ma-section-badge">Di</div>
      <h2 class="ma-section-title">Differentialrechnung</h2>
    </div>
    <p class="ma-section-meta">12 Module · Von Folgen bis Kurvendiskussion</p>
    <div class="ma-path">

      <div class="ma-module" data-module="d1">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">10</span><h4>Zahlenfolgen – Grundlagen</h4></div>
          <p class="ma-card-desc">Explizite und rekursive Bildungsvorschriften, Beschränktheit, Monotonie, arithmetische und geometrische Folgen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Folgen_2_1-2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_zahlenfolgen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d1')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d2">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">11</span><h4>Grenzwerte von Zahlenfolgen</h4></div>
          <p class="ma-card-desc">Konvergenz und Divergenz, Nullfolgen, Grenzwertsätze, Eulersche Zahl e</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Grenzwerte_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_grenzwerte_folgen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d2')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d3">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">12</span><h4>Grenzwerte – Verhalten im Unendlichen</h4></div>
          <p class="ma-card-desc">Grenzwerte für x → ±∞, Dominanzprinzip, waagerechte Asymptoten und typische Aufgabentypen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Funktion_2_2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_grenzwerte_funktionen_1.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d3')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d4">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">13</span><h4>Grenzwerte an einer Stelle</h4></div>
          <p class="ma-card-desc">Einseitige Grenzwerte, Polstellen, hebbare Lücken, Unstetigkeitsarten und Asymptoten</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Grenzwerte_2_2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_grenzwerte_funktionen_2.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d4')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d5">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">14</span><h4>Asymptoten & Polynomdivision</h4></div>
          <p class="ma-card-desc">Waagerechte, senkrechte und schräge Asymptoten, Polynomdivision, vollständige Funktionsanalyse</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Grenzwerte_2_3.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_asymptoten.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d5')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d6">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">15</span><h4>Wie steil ist eine Funktion?</h4></div>
          <p class="ma-card-desc">Steigung linearer und nicht-linearer Funktionen, Sekanten und Tangenten, Definition der Ableitung, Differenzierbarkeit</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Funktion_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_ableitung_grundlagen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d6')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d7">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">16</span><h4>Ableitungsregeln</h4></div>
          <p class="ma-card-desc">Potenz-, Summen-, Produkt-, Quotienten- und Kettenregel mit Beispielen und typischen Prüfungsaufgaben</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Funktion_2_4.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_ableitungsregeln.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d7')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d8">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">17</span><h4>Die Regel von de L'Hôpital</h4></div>
          <p class="ma-card-desc">Systematische Methode für unbestimmte Ausdrücke: 0/0, ∞/∞, ∞·0, ∞-∞, 0⁰, ∞⁰, 1∞</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Hospital_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_hospital.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d8')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d9">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">18</span><h4>Extrempunkte</h4></div>
          <p class="ma-card-desc">Notwendige und hinreichende Bedingungen, zweite Ableitung, Hoch- und Tiefpunkte, Sattelpunkte</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Extremwert_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_extrempunkte.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d9')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d10">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">19</span><h4>Wendepunkte</h4></div>
          <p class="ma-card-desc">Krümmungswechsel, dritte Ableitung, Links-Rechts- und Rechts-Links-Wendepunkte</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Wendepunkt_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_wendepunkte.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d10')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d11">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">20</span><h4>Kurvendiskussion</h4></div>
          <p class="ma-card-desc">Systematische Funktionsanalyse: Definitionsbereich, Symmetrie, Grenzwerte, Asymptoten, Nullstellen, Extrempunkte, Wendepunkte</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Kurvendiskusion_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_kurvendiskussion.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d11')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="d12">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">21</span><h4>Extremwertaufgaben</h4></div>
          <p class="ma-card-desc">Optimierungsprobleme: Haupt- und Nebenbedingungen, Zielfunktionen, Beispiele aus Technik und Wirtschaft</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Extrem_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_extremwertaufgaben.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('d12')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- ═══════════════════════════════════════
       INTEGRALRECHNUNG
       ═══════════════════════════════════════ -->
  <div class="ma-section ma-section--integral">
    <div class="ma-section-head">
      <div class="ma-section-badge">In</div>
      <h2 class="ma-section-title">Integralrechnung</h2>
    </div>
    <p class="ma-section-meta">4 Module · Stammfunktionen bis Rotationsvolumen</p>
    <div class="ma-path">

      <div class="ma-module" data-module="i1">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">22</span><h4>Einführung</h4></div>
          <p class="ma-card-desc">Stammfunktionen, Grundintegrale, Faktor- und Summenregel, bestimmtes Integral</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Integral_2_1.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_integral_einfuehrung.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('i1')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="i2">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">23</span><h4>Integrationsmethoden</h4></div>
          <p class="ma-card-desc">Substitution, partielle Integration, LIATE-Regel, Partialbruchzerlegung</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Integral_2_2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_integrationsmethoden.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('i2')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="i3">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">24</span><h4>Hauptsatz & Flächen</h4></div>
          <p class="ma-card-desc">Hauptsatz der Differential- und Integralrechnung, bestimmte Integrale, Flächenberechnung zwischen Graphen</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Integral_2_3.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_hauptsatz_flaechen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('i3')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="i4">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">25</span><h4>Flächenberechnung & Rotationsvolumen</h4></div>
          <p class="ma-card-desc">Komplexere Flächenberechnung, Volumen von Rotationskörpern um x- und y-Achse</p>
          <div class="ma-actions">
            <a href="/assets/pdfs/Intergal_2_4-2.pdf" class="ma-btn ma-btn--pdf"><span>📄</span> PDF</a>
            <a href="/assets/quizzes/quiz_rotationsvolumen.html" class="ma-btn ma-btn--quiz"><span>✎</span> Quiz</a>
            <label class="ma-check" onclick="maToggle('i4')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- ═══════════════════════════════════════
       INTERAKTIVE TOOLS
       ═══════════════════════════════════════ -->
  <div class="ma-section ma-section--tools">
    <div class="ma-section-head">
      <div class="ma-section-badge">⚡</div>
      <h2 class="ma-section-title">Interaktive Tools</h2>
    </div>
    <p class="ma-section-meta">3 Tools · Hands-on erkunden</p>
    <div class="ma-path">

      <div class="ma-module" data-module="t1">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">📐</span><h4>Tangenten-Explorer</h4></div>
          <p class="ma-card-desc">Interaktive Visualisierung von Tangenten und Ableitungen. Bewege den Punkt auf verschiedenen Funktionen und beobachte live die Steigungsänderung</p>
          <div class="ma-actions">
            <a href="/assets/interactive/tangenten_explorer.html" class="ma-btn ma-btn--open"><span>🚀</span> Öffnen</a>
            <label class="ma-check" onclick="maToggle('t1')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="t2">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">📐</span><h4>3D-Vektor-Explorer</h4></div>
          <p class="ma-card-desc">Drehe und manipuliere Vektoren im 3D-Raum. Visualisiere Addition, Subtraktion, Skalar- und Kreuzprodukt interaktiv</p>
          <div class="ma-actions">
            <a href="/assets/interactive/vektor_explorer.html" class="ma-btn ma-btn--open"><span>🚀</span> Öffnen</a>
            <label class="ma-check" onclick="maToggle('t2')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

      <div class="ma-module" data-module="t3">
        <div class="ma-module-dot"></div>
        <div class="ma-card">
          <div class="ma-card-top"><span class="ma-step-num">🔷</span><h4>Geraden & Ebenen im Raum</h4></div>
          <p class="ma-card-desc">Erkunde alle Lagebeziehungen von Geraden und Ebenen im 3D-Raum – schneidend, parallel, windschief oder identisch</p>
          <div class="ma-actions">
            <a href="/assets/interactive/geraden_ebenen_explorer.html" class="ma-btn ma-btn--open"><span>🚀</span> Öffnen</a>
            <label class="ma-check" onclick="maToggle('t3')"><span class="ma-check-box"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round"><path d="M2.5 6.5L5 9L9.5 3.5"/></svg></span>Erledigt</label>
          </div>
        </div>
      </div>

    </div>
  </div>

  <!-- FOOTER -->
  <div class="ma-footer">
    <div class="ma-footer-text"><strong>28 Module</strong> · Materialien für Bildungszwecke · Frei verwendbar</div>
    <div class="ma-footer-actions">
      <a href="/teaching/" class="ma-btn">← Übersicht</a>
      <button class="ma-btn-reset" onclick="maReset()">Fortschritt zurücksetzen</button>
    </div>
  </div>

</div>

<!-- PROGRESS TRACKING -->
<script>
const MA_KEY = 'math-progress';
const MA_TOTAL = 28;

function maGetProgress() {
  try { return JSON.parse(localStorage.getItem(MA_KEY)) || {}; }
  catch(e) { return {}; }
}

function maSaveProgress(p) { localStorage.setItem(MA_KEY, JSON.stringify(p)); }

function maToggle(id) {
  const p = maGetProgress();
  if (p[id]) { delete p[id]; } else { p[id] = Date.now(); }
  maSaveProgress(p);
  maRender();
}

function maReset() {
  if (confirm('Fortschritt wirklich zurücksetzen?')) {
    localStorage.removeItem(MA_KEY);
    maRender();
  }
}

function maRender() {
  const p = maGetProgress();
  const c = Object.keys(p).length;
  const pct = Math.round((c / MA_TOTAL) * 100);
  
  document.getElementById('maProgressBar').style.width = pct + '%';
  document.getElementById('maCompletedCount').textContent = c;
  document.getElementById('maProgressPercent').textContent = pct + ' %';
  
  document.querySelectorAll('.ma-module').forEach(el => {
    const id = el.dataset.module;
    if (p[id]) { el.classList.add('is-complete'); }
    else { el.classList.remove('is-complete'); }
  });
}

document.addEventListener('DOMContentLoaded', maRender);
if (document.readyState !== 'loading') maRender();
</script>