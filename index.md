---
layout: default
---

<style>
.home {
  max-width: 920px;
  margin: 0 auto;
  padding: 5rem 1.5rem 4rem;
}

.home-name {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 6vw, 3.5rem);
  font-weight: 300;
  letter-spacing: -0.02em;
  line-height: 1.1;
  color: var(--text-primary);
  margin-bottom: 1rem;
}

.home-intro {
  font-size: 1.05rem;
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 3.5rem;
  max-width: 480px;
}

.home-nav {
  display: flex;
  flex-direction: column;
  border-top: 1px solid var(--separator-strong);
}

.home-nav a {
  display: block;
  padding: 1.25rem 0;
  border-bottom: 1px solid var(--separator);
  text-decoration: none;
  transition: padding-left 0.2s ease;
}

.home-nav a:hover {
  padding-left: 0.5rem;
}

.home-nav-label {
  display: block;
  font-size: 1.05rem;
  font-weight: 500;
  color: var(--text-primary);
  margin-bottom: 0.2rem;
  transition: color 0.15s ease;
}

.home-nav a:hover .home-nav-label {
  color: var(--accent, #b85c38);
}

.home-nav-desc {
  display: block;
  font-size: 0.88rem;
  color: var(--text-tertiary);
}

@media (max-width: 480px) {
  .home {
    padding: 3rem 1.25rem 3rem;
  }
}
</style>

<div class="home">

  <h1 class="home-name">Maximilian<br>Vöcklinghaus</h1>
  <p class="home-intro">Dozent am Studienkolleg der Rahn Education in Leipzig – Mathematik, Informatik & interaktives Lernen.</p>

  <nav class="home-nav">
    <a href="/about/">
      <span class="home-nav-label">Hinweise zum Studium</span>
      <span class="home-nav-desc">Wie das Studienkolleg funktioniert, wie viel ihr lernen müsst, wie ihr die Materialien nutzt</span>
    </a>
    <a href="/teaching/">
      <span class="home-nav-label">Unterrichtsmaterialien</span>
      <span class="home-nav-desc">Mathematik, Volkswirtschaftslehre und Informatik</span>
    </a>
  </nav>

</div>
