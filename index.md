---
layout: default
---

<style>
/* Japandi Design - Japanisch-Skandinavische Fusion */

.home {
  background: #f7f5f2;
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Inter", "Segoe UI", sans-serif;
  line-height: 1.7;
  color: #3d3d3d;
}

.home h1 {
  margin: 0 0 1rem 0;
  font-size: 2.5rem;
  font-weight: 400;
  letter-spacing: 0.02em;
  color: #3d3d3d;
  position: relative;
}

.intro {
  font-size: 1.1rem;
  color: #6b6b6b;
  font-weight: 400;
  margin-bottom: 4rem;
  letter-spacing: 0.02em;
  line-height: 1.8;
}

.sections {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2.5rem 0;
}

.section-card {
  background: #ffffff;
  border: 1px solid #e8e5e0;
  border-radius: 2px;
  padding: 2.5rem 2rem;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
  min-height: 240px;
}

/* Dezente, natürliche Farbpalette für verschiedene Karten */
.section-card:nth-child(1) {
  border-top: 2px solid #b8a89a;
}

.section-card:nth-child(2) {
  border-top: 2px solid #8b9e9f;
}

.section-card:nth-child(3) {
  border-top: 2px solid #c9a690;
}

/* Minimalistischer Akzent */
.section-card::before {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 1px;
  height: 60px;
  opacity: 0.15;
  transition: all 0.4s ease;
}

.section-card:nth-child(1)::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.section-card:nth-child(2)::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

.section-card:nth-child(3)::before {
  background: linear-gradient(to bottom, #c9a690, transparent);
}

/* Dezenter Cover-Effekt */
.section-card::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 2px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.4s ease;
  z-index: 0;
}

.section-card:nth-child(1)::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.section-card:nth-child(2)::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
}

.section-card:nth-child(3)::after {
  background: linear-gradient(180deg, rgba(201, 166, 144, 0.04) 0%, rgba(201, 166, 144, 0.02) 100%);
}

.section-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  border-color: #d5d0ca;
}

.section-card:hover::after {
  opacity: 1;
}

.section-card:hover::before {
  height: 100%;
  width: 3px;
  opacity: 0.4;
}

.section-card h2 {
  margin: 0 0 1rem 0;
  color: #3d3d3d;
  font-size: 1.25rem;
  font-weight: 500;
  letter-spacing: 0.01em;
  line-height: 1.4;
  transition: color 0.3s ease;
  position: relative;
  z-index: 2;
}

.section-card:nth-child(1):hover h2 {
  color: #b8a89a;
}

.section-card:nth-child(2):hover h2 {
  color: #8b9e9f;
}

.section-card:nth-child(3):hover h2 {
  color: #c9a690;
}

.section-card p {
  color: #6b6b6b;
  line-height: 1.8;
  margin: 0 0 2rem 0;
  font-size: 0.9rem;
  font-weight: 400;
  letter-spacing: 0.01em;
  flex-grow: 1;
  position: relative;
  z-index: 2;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.9rem 1.5rem;
  background: #fafaf9;
  color: #5a5a5a !important;
  text-decoration: none;
  border: 1px solid #e8e5e0;
  border-radius: 1px;
  font-size: 0.85rem;
  font-weight: 500;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
  margin-top: auto;
  align-self: flex-start;
  z-index: 2;
}

.btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.section-card:nth-child(1) .btn::before {
  background: linear-gradient(180deg, #b8a89a 0%, #cbbfb3 100%);
}

.section-card:nth-child(2) .btn::before {
  background: linear-gradient(180deg, #8b9e9f 0%, #a5b5b6 100%);
}

.section-card:nth-child(3) .btn::before {
  background: linear-gradient(180deg, #c9a690 0%, #dbc0af 100%);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.12);
  border-color: transparent;
  color: #ffffff !important;
}

.btn:hover::before {
  opacity: 1;
}

.btn:hover::after {
  opacity: 1;
  transform: translateX(0);
}

.btn::after {
  content: '→';
  position: absolute;
  right: 1.5rem;
  opacity: 0;
  transform: translateX(-10px);
  transition: all 0.3s ease;
  z-index: 3;
  color: #ffffff;
  font-size: 1rem;
}

.btn span {
  position: relative;
  z-index: 2;
}

/* Hero-Bereich mit dezenter Dekoration */
.home::before {
  content: '';
  position: absolute;
  top: 20%;
  right: -100px;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(139, 158, 159, 0.04) 0%, transparent 60%);
  border-radius: 50%;
  pointer-events: none;
}

.home::after {
  content: '';
  position: absolute;
  top: 15%;
  right: 50px;
  width: 180px;
  height: 180px;
  background: radial-gradient(circle, rgba(184, 168, 154, 0.03) 0%, transparent 60%);
  border-radius: 50%;
  pointer-events: none;
}

/* Wabi-Sabi Textur-Effekt */
body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(circle at 20% 30%, rgba(184, 168, 154, 0.02) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(139, 158, 159, 0.02) 0%, transparent 50%);
  pointer-events: none;
  z-index: -1;
}

@media (max-width: 768px) {
  .home h1 {
    font-size: 2rem;
  }

  .intro {
    font-size: 1rem;
    margin-bottom: 3rem;
  }

  .sections {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .section-card {
    padding: 2rem 1.5rem;
    min-height: 200px;
  }

  .section-card h2 {
    font-size: 1.15rem;
  }

  .section-card p {
    font-size: 0.88rem;
  }

  .home::before,
  .home::after {
    display: none;
  }
}
</style>

<div class="home">
  <h1>Max Vöcklinghaus</h1>
  <p class="intro">
    Mathematik, Wirtschaft & Datenanalyse
  </p>
  
  <div class="sections">
    <div class="section-card">
      <h2>Über mich</h2>
      <p>Hintergrund, Ausbildung und Schwerpunkte</p>
      <a href="/about/" class="btn">Mehr erfahren</a>
    </div>
    
    <div class="section-card">
      <h2>Analysen</h2>
      <p>Wirtschaftliche Betrachtungen und datengestützte Untersuchungen</p>
      <a href="/analysen/" class="btn">Analysen lesen</a>
    </div>
    
    <div class="section-card">
      <h2>Unterrichtsmaterialien</h2>
      <p>Mathematik, Volkswirtschaftslehre und Informatik</p>
      <a href="/teaching/" class="btn">Materialien</a>
    </div>
  </div>
</div>