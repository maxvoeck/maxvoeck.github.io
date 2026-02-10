---
layout: page
title: 
permalink: /analysen/
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
  --analysen: #f97316;
  --analysen-soft: rgba(249, 115, 22, 0.12);
}

body, html, .page-content, .wrapper, main, .post-content {
  background: var(--bg-deep) !important;
  color: var(--text-primary);
}
.post-header, .page-heading, header.post-header { display: none !important; }
a { color: var(--accent-3); }
a:hover { color: #c4b5fd; text-decoration: none; }

/* ═══ AMBIENT ═══ */
.an-ambient {
  position: fixed; top: 0; left: 0; right: 0; bottom: 0;
  z-index: 0; overflow: hidden; pointer-events: none;
}
.an-ambient-orb {
  position: absolute; border-radius: 50%;
  filter: blur(120px); opacity: 0.4;
  animation: an-drift 20s ease-in-out infinite;
}
.an-ambient-orb:nth-child(1) {
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(249, 115, 22, 0.18) 0%, transparent 70%);
  top: -10%; left: -5%;
}
.an-ambient-orb:nth-child(2) {
  width: 420px; height: 420px;
  background: radial-gradient(circle, rgba(139, 92, 246, 0.14) 0%, transparent 70%);
  top: 45%; right: -10%;
  animation-delay: -8s; animation-duration: 24s;
}
.an-ambient-orb:nth-child(3) {
  width: 350px; height: 350px;
  background: radial-gradient(circle, rgba(99, 102, 241, 0.1) 0%, transparent 70%);
  bottom: -5%; left: 30%;
  animation-delay: -14s; animation-duration: 22s;
}
@keyframes an-drift {
  0%, 100% { transform: translate(0, 0) scale(1); }
  25% { transform: translate(25px, -18px) scale(1.04); }
  50% { transform: translate(-18px, 25px) scale(0.96); }
  75% { transform: translate(12px, 12px) scale(1.02); }
}
.an-ambient::after {
  content: ''; position: absolute; inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
  opacity: 0.4; pointer-events: none;
}

/* ═══ CONTENT ═══ */
.an-content {
  position: relative; z-index: 1;
  max-width: 780px; margin: 0 auto;
  padding: 2rem 1.5rem 5rem;
  font-family: 'Inter', -apple-system, sans-serif;
}

/* ═══ HERO ═══ */
.an-hero {
  background: var(--bg-card);
  backdrop-filter: blur(40px); -webkit-backdrop-filter: blur(40px);
  border: 1px solid var(--border);
  border-radius: 24px;
  padding: 2.5rem 2.25rem 2rem;
  margin-bottom: 2.5rem;
  position: relative; overflow: hidden;
}
.an-hero::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
}
.an-hero-eyebrow {
  font-size: 0.72rem; font-weight: 500;
  letter-spacing: 0.12em; text-transform: uppercase;
  color: var(--analysen); margin-bottom: 0.75rem;
}
.an-hero h1 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 2.5rem; font-weight: 600;
  letter-spacing: -0.03em; line-height: 1.1;
  margin-bottom: 0.5rem;
  background: linear-gradient(135deg, #fff 0%, rgba(255,255,255,0.7) 100%);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
}
.an-hero-sub {
  font-size: 0.92rem; color: var(--text-secondary);
  font-weight: 300; line-height: 1.8;
}

/* ═══ POST LIST ═══ */
.an-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.an-post {
  background: var(--bg-card);
  backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-left: 2px solid var(--analysen);
  border-radius: 16px;
  padding: 1.75rem 2rem;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease, background 0.15s ease;
  position: relative; overflow: hidden;
}
.an-post::before {
  content: ''; position: absolute; top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
  opacity: 0; transition: opacity 0.15s ease;
}
.an-post:hover {
  background: var(--bg-card-hover); border-color: var(--border-hover);
  border-left-color: var(--analysen);
  transform: translateY(-2px);
  box-shadow: 0 8px 32px rgba(249, 115, 22, 0.06);
}
.an-post:hover::before { opacity: 1; }

.an-post-date {
  font-size: 0.7rem; font-weight: 500;
  letter-spacing: 0.08em; text-transform: uppercase;
  color: var(--text-muted); margin-bottom: 0.6rem;
}

.an-post h2 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 1.15rem; font-weight: 500;
  letter-spacing: -0.01em; line-height: 1.45;
  margin: 0 0 0.5rem 0;
}
.an-post h2 a {
  color: var(--text-primary) !important;
  text-decoration: none !important;
  transition: color 0.15s ease;
}
.an-post:hover h2 a { color: var(--analysen) !important; }

.an-post-excerpt {
  font-size: 0.85rem; color: var(--text-secondary);
  font-weight: 300; line-height: 1.75;
  margin: 0 0 1.25rem 0;
}

.an-btn {
  display: inline-flex; align-items: center; gap: 0.4rem;
  padding: 0.55rem 1.1rem; border-radius: 10px;
  font-size: 0.76rem; font-weight: 500;
  letter-spacing: 0.04em; text-transform: uppercase;
  text-decoration: none !important;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.03);
  color: var(--text-secondary) !important;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease, background 0.15s ease, color 0.15s ease;
  font-family: 'Inter', -apple-system, sans-serif;
}
.an-btn:hover {
  transform: translateY(-1px);
  border-color: rgba(249, 115, 22, 0.4);
  background: rgba(255,255,255,0.08);
  color: var(--text-primary) !important;
  box-shadow: 0 4px 16px rgba(249, 115, 22, 0.1);
}

.an-btn-arrow {
  opacity: 0; transform: translateX(-4px);
  transition: opacity 0.15s ease, transform 0.15s ease;
  font-size: 0.85rem;
}
.an-btn:hover .an-btn-arrow {
  opacity: 1; transform: translateX(0);
}

/* ═══ EMPTY STATE ═══ */
.an-empty {
  text-align: center;
  padding: 4rem 2rem;
  background: var(--bg-card);
  backdrop-filter: blur(20px);
  border: 1px solid var(--border);
  border-radius: 20px;
}
.an-empty p {
  color: var(--text-muted);
  font-size: 0.9rem; font-weight: 300;
  font-style: italic; margin: 0;
}

/* ═══ ANIMATIONS ═══ */
@keyframes an-fadeUp {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}
.an-hero { animation: an-fadeUp 0.6s ease both; }
.an-post { animation: an-fadeUp 0.4s ease both; }
.an-post:nth-child(1) { animation-delay: 0.08s; }
.an-post:nth-child(2) { animation-delay: 0.14s; }
.an-post:nth-child(3) { animation-delay: 0.2s; }
.an-post:nth-child(4) { animation-delay: 0.26s; }
.an-post:nth-child(5) { animation-delay: 0.32s; }
.an-empty { animation: an-fadeUp 0.5s ease both; animation-delay: 0.1s; }

/* ═══ RESPONSIVE ═══ */
@media (max-width: 768px) {
  .an-content { padding: 1.5rem 1rem 4rem; }
  .an-hero { padding: 2rem 1.5rem 1.5rem; border-radius: 20px; }
  .an-hero h1 { font-size: 1.9rem; }
  .an-post { padding: 1.5rem; border-radius: 14px; }
  .an-post h2 { font-size: 1.05rem; }
}
</style>

<!-- AMBIENT -->
<div class="an-ambient">
  <div class="an-ambient-orb"></div>
  <div class="an-ambient-orb"></div>
  <div class="an-ambient-orb"></div>
</div>

<div class="an-content">

  <!-- HERO -->
  <div class="an-hero">
    <div class="an-hero-eyebrow">Wirtschaftsanalysen</div>
    <h1>Analysen</h1>
    <p class="an-hero-sub">Analysen zu wirtschaftlichen Themen, Marktentwicklungen und wirtschaftspolitischen Fragestellungen.</p>
  </div>

  <!-- POST LIST -->
  <div class="an-list">
    {% for analyse in site.analysen %}
    <article class="an-post">
      <p class="an-post-date">{{ analyse.date | date: "%d. %B %Y" }}</p>
      <h2><a href="{{ analyse.url | relative_url }}">{{ analyse.title }}</a></h2>
      <p class="an-post-excerpt">{{ analyse.excerpt | strip_html | truncatewords: 40 }}</p>
      <a href="{{ analyse.url | relative_url }}" class="an-btn"><span>Weiterlesen</span><span class="an-btn-arrow">→</span></a>
    </article>
    {% endfor %}
  </div>

  {% if site.analysen.size == 0 %}
  <div class="an-empty">
    <p>Bald erscheinen hier die ersten Analysen...</p>
  </div>
  {% endif %}

</div>