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

@media (max-width: 480px) {
  .home { padding: 3rem 1.25rem 3rem; }
  .home-nav-label { font-size: 20px; }
}
</style>

<div class="home">

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
