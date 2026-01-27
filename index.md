---
layout: default
---

<style>
/* Japandi Design mit Apple-Style Rounded Corners */

body {
  background: linear-gradient(135deg, #f7f5f2 0%, #f0ede8 25%, #e8e5e0 50%, #f0ede8 75%, #f7f5f2 100%);
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Inter", "Segoe UI", sans-serif;
  line-height: 1.7;
  color: #3d3d3d;
  min-height: 100vh;
  background-attachment: fixed;
}

.home {
  position: relative;
}

/* Hero Header */
.hero-header {
  background: #ffffff;
  padding: 4rem 2.5rem;
  margin: -2rem -2rem 4rem -2rem;
  position: relative;
  overflow: hidden;
  border-bottom: 1px solid #e8e5e0;
  border-radius: 0 0 32px 32px;
}

/* Zen-inspirierte Dekoration */
.hero-header::before {
  content: '';
  position: absolute;
  top: 50%;
  right: 60px;
  width: 200px;
  height: 200px;
  background: radial-gradient(circle, rgba(139, 158, 159, 0.06) 0%, transparent 60%);
  border-radius: 50%;
  transform: translateY(-50%);
}

.hero-header::after {
  content: '';
  position: absolute;
  top: 50%;
  right: 180px;
  width: 120px;
  height: 120px;
  background: radial-gradient(circle, rgba(184, 168, 154, 0.04) 0%, transparent 60%);
  border-radius: 50%;
  transform: translateY(-50%);
}

.hero-header h1 {
  margin: 0 0 1rem 0;
  font-size: 2.5rem;
  font-weight: 400;
  letter-spacing: 0.02em;
  color: #3d3d3d;
  position: relative;
  z-index: 1;
}

.intro {
  font-size: 1.05rem;
  color: #6b6b6b;
  font-weight: 400;
  margin: 0;
  letter-spacing: 0.02em;
  line-height: 1.8;
  position: relative;
  z-index: 1;
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
  border-radius: 20px;
  padding: 0;
  transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.03);
}

/* Dezente, natürliche Farbpalette */
.section-card.about {
  border-top: 2px solid #b8a89a;
}

.section-card.analyses {
  border-top: 2px solid #8b9e9f;
}

.section-card.teaching {
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

.section-card.about::before {
  background: linear-gradient(to bottom, #b8a89a, transparent);
}

.section-card.analyses::before {
  background: linear-gradient(to bottom, #8b9e9f, transparent);
}

.section-card.teaching::before {
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
  border-radius: 20px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.4s ease;
  z-index: 0;
}

.section-card.about::after {
  background: linear-gradient(180deg, rgba(184, 168, 154, 0.04) 0%, rgba(184, 168, 154, 0.02) 100%);
}

.section-card.analyses::after {
  background: linear-gradient(180deg, rgba(139, 158, 159, 0.04) 0%, rgba(139, 158, 159, 0.02) 100%);
}

.section-card.teaching::after {
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

.card-header {
  padding: 2rem 2rem 1.5rem 2rem;
  position: relative;
  z-index: 2;
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
}

.icon-wrapper {
  width: 48px;
  height: 48px;
  background: transparent;
  border: 1px solid #e8e5e0;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  transition: all 0.3s ease;
  position: relative;
  z-index: 3;
}

.section-card.about:hover .icon-wrapper {
  background: #b8a89a;
  border-color: #b8a89a;
}

.section-card.analyses:hover .icon-wrapper {
  background: #8b9e9f;
  border-color: #8b9e9f;
}

.section-card.teaching:hover .icon-wrapper {
  background: #c9a690;
  border-color: #c9a690;
}

.icon-wrapper svg {
  width: 24px;
  height: 24px;
  fill: #6b6b6b;
  transition: fill 0.3s ease;
}

.section-card:hover .icon-wrapper svg {
  fill: #ffffff;
}

.card-title-wrapper {
  flex-grow: 1;
}

.section-card h2 {
  margin: 0;
  color: #3d3d3d;
  font-size: 1.15rem;
  font-weight: 500;
  letter-spacing: 0.01em;
  line-height: 1.4;
  transition: color 0.3s ease;
}

.section-card.about:hover h2 {
  color: #b8a89a;
}

.section-card.analyses:hover h2 {
  color: #8b9e9f;
}

.section-card.teaching:hover h2 {
  color: #c9a690;
}

.card-content {
  padding: 0 2rem 2rem 2rem;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  position: relative;
  z-index: 2;
}

.section-card p {
  color: #6b6b6b;
  line-height: 1.8;
  margin: 0 0 1.5rem 0;
  font-size: 0.88rem;
  font-weight: 400;
  letter-spacing: 0.01em;
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
  border-radius: 12px;
  font-size: 0.85rem;
  font-weight: 500;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
  margin-top: auto;
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

.section-card.about .btn::before {
  background: linear-gradient(180deg, #b8a89a 0%, #cbbfb3 100%);
}

.section-card.analyses .btn::before {
  background: linear-gradient(180deg, #8b9e9f 0%, #a5b5b6 100%);
}

.section-card.teaching .btn::before {
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

.btn span {
  position: relative;
  z-index: 2;
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
    radial-gradient(circle at 15% 25%, rgba(184, 168, 154, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 85% 75%, rgba(139, 158, 159, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 50% 50%, rgba(201, 184, 150, 0.02) 0%, transparent 60%);
  pointer-events: none;
  z-index: -1;
  opacity: 0.8;
}

@media (max-width: 768px) {
  .sections {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .hero-header {
    margin: -1rem -1rem 2.5rem -1rem;
    padding: 2.5rem 1.75rem;
    border-radius: 0 0 24px 24px;
  }

  .hero-header h1 {
    font-size: 2rem;
  }

  .intro {
    font-size: 0.95rem;
  }

  .hero-header::before,
  .hero-header::after {
    display: none;
  }

  .card-header {
    padding: 1.75rem 1.5rem 1.25rem 1.5rem;
  }

  .card-content {
    padding: 0 1.5rem 1.75rem 1.5rem;
  }

  .icon-wrapper {
    width: 40px;
    height: 40px;
    border-radius: 10px;
  }

  .icon-wrapper svg {
    width: 20px;
    height: 20px;
  }

  .section-card h2 {
    font-size: 1.05rem;
  }
  
  .section-card {
    border-radius: 16px;
  }
  
  .section-card::after {
    border-radius: 16px;
  }
  
  .btn {
    border-radius: 10px;
  }
}
</style>

<div class="home">
  <div class="hero-header">
    <h1>Maximilian Vöck</h1>
    <p class="intro">Mathematik, Wirtschaft & Datenanalyse</p>
  </div>
  
  <div class="sections">
    <div class="section-card about">
      <div class="card-header">
        <div class="icon-wrapper">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM12 5C13.66 5 15 6.34 15 8C15 9.66 13.66 11 12 11C10.34 11 9 9.66 9 8C9 6.34 10.34 5 12 5ZM12 19.2C9.5 19.2 7.29 17.92 6 15.98C6.03 13.99 10 12.9 12 12.9C13.99 12.9 17.97 13.99 18 15.98C16.71 17.92 14.5 19.2 12 19.2Z"/>
          </svg>
        </div>
        <div class="card-title-wrapper">
          <h2>Über mich</h2>
        </div>
      </div>
      <div class="card-content">
        <p>Hintergrund, Ausbildung und Schwerpunkte</p>
        <a href="/about/" class="btn"><span>Mehr erfahren</span></a>
      </div>
    </div>
    
    <div class="section-card analyses">
      <div class="card-header">
        <div class="icon-wrapper">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M19 3H5C3.9 3 3 3.9 3 5V19C3 20.1 3.9 21 5 21H19C20.1 21 21 20.1 21 19V5C21 3.9 20.1 3 19 3ZM9 17H7V10H9V17ZM13 17H11V7H13V17ZM17 17H15V13H17V17Z"/>
          </svg>
        </div>
        <div class="card-title-wrapper">
          <h2>Analysen</h2>
        </div>
      </div>
      <div class="card-content">
        <p>Wirtschaftliche Betrachtungen und datengestützte Untersuchungen</p>
        <a href="/analysen/" class="btn"><span>Analysen lesen</span></a>
      </div>
    </div>
    
    <div class="section-card teaching">
      <div class="card-header">
        <div class="icon-wrapper">
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M5 13.18V17.18L12 21L19 17.18V13.18L12 17L5 13.18ZM12 3L1 9L12 15L21 10.09V17H23V9L12 3Z"/>
          </svg>
        </div>
        <div class="card-title-wrapper">
          <h2>Unterrichtsmaterialien</h2>
        </div>
      </div>
      <div class="card-content">
        <p>Mathematik, Volkswirtschaftslehre und Informatik</p>
        <a href="/teaching/" class="btn"><span>Materialien</span></a>
      </div>
    </div>
  </div>
</div>