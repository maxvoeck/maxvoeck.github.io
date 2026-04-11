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

/* ─── Aufgabe des Tages Teaser ─── */
.adt-teaser {
  margin-bottom: var(--s16);
}

.adt-teaser-eyebrow {
  font-family: var(--font-body);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--text-tertiary);
  margin-bottom: var(--s6);
}

.adt-teaser-grid {
  display: flex;
  flex-direction: column;
  gap: var(--s3);
}

.adt-teaser-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: var(--s4);
  padding: var(--s5) var(--s6);
  border: 1px solid var(--border);
  border-radius: var(--r-md);
  text-decoration: none;
  color: inherit;
  transition: all 200ms var(--ease-out);
  background: var(--bg-elevated, rgba(255,255,255,0.03));
}

.adt-teaser-card:hover {
  border-color: var(--border-hover, var(--border-strong));
  padding-left: calc(var(--s6) + 4px);
}

.adt-teaser-left {
  display: flex;
  align-items: center;
  gap: var(--s4);
  min-width: 0;
}

.adt-teaser-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  flex-shrink: 0;
}

.adt-teaser-dot--mathe { background: var(--beni); }
.adt-teaser-dot--vwl { background: var(--kitsune); }
.adt-teaser-dot--info { background: var(--ai); }

.adt-teaser-fach {
  font-size: 15px;
  font-weight: 400;
  color: var(--text-primary);
  white-space: nowrap;
}

.adt-teaser-arrow {
  font-size: 13px;
  color: var(--text-tertiary);
  flex-shrink: 0;
  transition: color 200ms;
}

.adt-teaser-card:hover .adt-teaser-arrow {
  color: var(--accent);
}

@media (max-width: 480px) {
  .home { padding: 3rem 1.25rem 3rem; }
  .home-nav-label { font-size: 20px; }
}
</style>

<div class="home">

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
