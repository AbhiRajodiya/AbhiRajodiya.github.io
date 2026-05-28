<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Abhi Rajodiya — .NET Full Stack Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet"/>
  <!-- Standard browser tab icon -->
<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,..."/>

<!-- Fallback for older browsers -->
<link rel="shortcut icon" type="image/svg+xml" href="data:image/svg+xml,..."/>

<!-- iOS home screen icon -->
<link rel="apple-touch-icon" href="data:image/svg+xml,..."/>

<!-- Mobile browser chrome color -->
<meta name="theme-color" content="#1a1a2e"/>
<style>
:root {
  --ink: #0d0f14;
  --paper: #f7f6f1;
  --mid: #e8e4d9;
  --accent: #1a56ff;
  --accent2: #ff4d1c;
  --muted: #8a8880;
  --card-bg: #ffffff;
  --tag-bg: #edeae0;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--paper);
  color: var(--ink);
  overflow-x: hidden;
}

/* ── NOISE OVERLAY ── */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
  pointer-events: none;
  z-index: 9999;
  opacity: 0.6;
}

/* ── NAV ── */
nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.2rem 4rem;
  backdrop-filter: blur(14px);
  background: rgba(247,246,241,0.82);
  border-bottom: 1px solid var(--mid);
}

.nav-logo {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: 1.25rem;
  letter-spacing: -0.5px;
  color: var(--ink);
  text-decoration: none;
}

.nav-logo span { color: var(--accent); }

.nav-links { display: flex; gap: 2.2rem; list-style: none; }

.nav-links a {
  text-decoration: none;
  color: var(--muted);
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 0.3px;
  transition: color 0.2s;
  position: relative;
}

.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -3px; left: 0;
  width: 0; height: 1.5px;
  background: var(--accent);
  transition: width 0.25s;
}

.nav-links a:hover { color: var(--ink); }
.nav-links a:hover::after { width: 100%; }

/* ── HERO ── */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: 8rem 4rem 4rem;
  position: relative;
  overflow: hidden;
}

.hero-bg-text {
  position: absolute;
  top: 50%;
  left: -2rem;
  transform: translateY(-50%);
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: clamp(7rem, 18vw, 18rem);
  color: transparent;
  -webkit-text-stroke: 1.5px var(--mid);
  white-space: nowrap;
  pointer-events: none;
  user-select: none;
  z-index: 0;
  animation: slideText 25s linear infinite;
}

@keyframes slideText {
  0% { transform: translateY(-50%) translateX(0); }
  100% { transform: translateY(-50%) translateX(-40%); }
}

.hero-inner {
  position: relative;
  z-index: 1;
  max-width: 900px;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: var(--ink);
  color: var(--paper);
  padding: 0.35rem 1rem;
  border-radius: 100px;
  font-size: 0.78rem;
  font-weight: 500;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 1.8rem;
  animation: fadeUp 0.8s both;
}

.hero-badge::before {
  content: '';
  width: 7px; height: 7px;
  background: #22c55e;
  border-radius: 50%;
  animation: pulse 1.8s ease-in-out infinite;
}

@keyframes pulse {
  0%,100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.5; transform: scale(0.7); }
}

.hero h1 {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: clamp(3.2rem, 7vw, 6.5rem);
  line-height: 1.0;
  letter-spacing: -2px;
  color: var(--ink);
  animation: fadeUp 0.8s 0.1s both;
}

.hero h1 em {
  font-style: normal;
  color: var(--accent);
  position: relative;
}

.hero h1 em::after {
  content: '';
  position: absolute;
  bottom: 6px; left: 0; right: 0;
  height: 4px;
  background: var(--accent2);
  border-radius: 2px;
  transform: scaleX(0);
  transform-origin: left;
  animation: lineIn 0.6s 0.9s forwards;
}

@keyframes lineIn {
  to { transform: scaleX(1); }
}

.hero-sub {
  margin-top: 1.6rem;
  font-size: 1.18rem;
  color: var(--muted);
  font-weight: 300;
  max-width: 560px;
  line-height: 1.7;
  animation: fadeUp 0.8s 0.2s both;
}

.hero-actions {
  margin-top: 2.5rem;
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  animation: fadeUp 0.8s 0.3s both;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.85rem 2rem;
  border-radius: 100px;
  font-size: 0.95rem;
  font-weight: 500;
  text-decoration: none;
  transition: all 0.25s;
  cursor: pointer;
  border: none;
}

.btn-primary {
  background: var(--ink);
  color: var(--paper);
}

.btn-primary:hover {
  background: var(--accent);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(26,86,255,0.3);
}

.btn-outline {
  background: transparent;
  color: var(--ink);
  border: 1.5px solid var(--ink);
}

.btn-outline:hover {
  background: var(--ink);
  color: var(--paper);
  transform: translateY(-2px);
}

.hero-stats {
  margin-top: 3.5rem;
  display: flex;
  gap: 3rem;
  animation: fadeUp 0.8s 0.4s both;
}

.stat { }

.stat-num {
  font-family: 'Syne', sans-serif;
  font-size: 2.4rem;
  font-weight: 800;
  color: var(--ink);
  line-height: 1;
}

.stat-num span { color: var(--accent); }

.stat-label {
  font-size: 0.82rem;
  color: var(--muted);
  letter-spacing: 0.5px;
  margin-top: 0.25rem;
}

/* ── SCROLL INDICATOR ── */
.scroll-hint {
  position: absolute;
  bottom: 2.5rem;
  right: 4rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  color: var(--muted);
  font-size: 0.75rem;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  animation: fadeUp 1s 0.8s both;
}

.scroll-line {
  width: 1px;
  height: 60px;
  background: linear-gradient(to bottom, var(--muted), transparent);
  animation: scrollAnim 1.5s ease-in-out infinite;
}

@keyframes scrollAnim {
  0%,100% { opacity: 1; transform: scaleY(1); }
  50% { opacity: 0.3; transform: scaleY(0.5); }
}

/* ── SECTIONS ── */
section {
  padding: 6rem 4rem;
  max-width: 1200px;
  margin: 0 auto;
}

.section-header {
  display: flex;
  align-items: baseline;
  gap: 1rem;
  margin-bottom: 3.5rem;
}

.section-num {
  font-family: 'Syne', sans-serif;
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--accent);
  letter-spacing: 2px;
  text-transform: uppercase;
}

.section-title {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: clamp(2rem, 4vw, 3.2rem);
  letter-spacing: -1.5px;
  color: var(--ink);
}

.section-line {
  flex: 1;
  height: 1px;
  background: var(--mid);
  margin-left: 1rem;
}

/* ── SKILLS ── */
.skills-section { background: var(--ink); border-radius: 2rem; padding: 4rem; max-width: none; margin: 0 2rem 0; }
.skills-section .section-title { color: var(--paper); }
.skills-section .section-num { color: #5b9dff; }
.skills-section .section-line { background: rgba(255,255,255,0.1); }

.skills-clusters {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.skill-cluster {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 1.2rem;
  padding: 1.8rem;
  transition: background 0.25s, transform 0.25s;
}

.skill-cluster:hover {
  background: rgba(255,255,255,0.08);
  transform: translateY(-4px);
}

.skill-cluster-icon {
  width: 44px; height: 44px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.3rem;
  margin-bottom: 1rem;
}

.skill-cluster h4 {
  font-family: 'Syne', sans-serif;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.5);
  margin-bottom: 1rem;
}

.skill-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }

.skill-tag {
  background: rgba(255,255,255,0.1);
  color: rgba(255,255,255,0.85);
  padding: 0.3rem 0.8rem;
  border-radius: 100px;
  font-size: 0.82rem;
  font-weight: 400;
  letter-spacing: 0.2px;
}

/* ── EXPERIENCE ── */
.exp-timeline { position: relative; }

.exp-timeline::before {
  content: '';
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 1px;
  background: var(--mid);
}

.exp-item {
  padding-left: 2.5rem;
  padding-bottom: 3.5rem;
  position: relative;
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.5s, transform 0.5s;
}

.exp-item.visible { opacity: 1; transform: translateY(0); }

.exp-item::before {
  content: '';
  position: absolute;
  left: -5px; top: 6px;
  width: 11px; height: 11px;
  border-radius: 50%;
  background: var(--accent);
  border: 2px solid var(--paper);
  box-shadow: 0 0 0 3px var(--accent);
}

.exp-date {
  font-size: 0.78rem;
  font-weight: 500;
  color: var(--accent);
  letter-spacing: 1px;
  text-transform: uppercase;
  margin-bottom: 0.5rem;
}

.exp-role {
  font-family: 'Syne', sans-serif;
  font-size: 1.4rem;
  font-weight: 700;
  letter-spacing: -0.5px;
  color: var(--ink);
  margin-bottom: 0.3rem;
}

.exp-company {
  font-size: 0.95rem;
  color: var(--muted);
  margin-bottom: 1.2rem;
}

.exp-company strong { color: var(--ink); font-weight: 500; }

.exp-bullets { list-style: none; }

.exp-bullets li {
  position: relative;
  padding-left: 1.3rem;
  margin-bottom: 0.65rem;
  font-size: 0.95rem;
  color: #3a3a3a;
  line-height: 1.6;
}

.exp-bullets li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: var(--accent);
  font-size: 0.9rem;
}

/* ── PROJECTS ── */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 1.8rem;
}

.project-card {
  background: var(--card-bg);
  border-radius: 1.5rem;
  padding: 2rem;
  border: 1px solid var(--mid);
  position: relative;
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s;
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.5s, transform 0.5s, box-shadow 0.3s;
}

.project-card.visible { opacity: 1; transform: translateY(0); }

.project-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 20px 50px rgba(0,0,0,0.1);
}

.project-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
}

.project-card:nth-child(1)::before { background: linear-gradient(90deg, var(--accent), #7c3aed); }
.project-card:nth-child(2)::before { background: linear-gradient(90deg, var(--accent2), #f59e0b); }

.project-num {
  font-family: 'Syne', sans-serif;
  font-size: 3.5rem;
  font-weight: 800;
  color: var(--mid);
  line-height: 1;
  margin-bottom: 0.5rem;
}

.project-name {
  font-family: 'Syne', sans-serif;
  font-size: 1.3rem;
  font-weight: 700;
  letter-spacing: -0.5px;
  color: var(--ink);
  margin-bottom: 0.8rem;
}

.project-desc {
  font-size: 0.9rem;
  color: var(--muted);
  line-height: 1.65;
  margin-bottom: 1.5rem;
}

.project-highlights {
  list-style: none;
  margin-bottom: 1.5rem;
}

.project-highlights li {
  font-size: 0.88rem;
  color: #3a3a3a;
  padding: 0.4rem 0;
  border-bottom: 1px solid var(--mid);
  display: flex;
  align-items: flex-start;
  gap: 0.6rem;
  line-height: 1.5;
}

.project-highlights li::before {
  content: '◆';
  color: var(--accent);
  font-size: 0.5rem;
  margin-top: 0.4rem;
  flex-shrink: 0;
}

.project-tech { display: flex; flex-wrap: wrap; gap: 0.4rem; }

.tech-tag {
  background: var(--tag-bg);
  color: var(--ink);
  padding: 0.25rem 0.7rem;
  border-radius: 100px;
  font-size: 0.77rem;
  font-weight: 500;
  letter-spacing: 0.3px;
}

/* ── EDUCATION ── */
.edu-card {
  background: var(--card-bg);
  border-radius: 1.5rem;
  padding: 2.5rem;
  border: 1px solid var(--mid);
  display: flex;
  gap: 2rem;
  align-items: center;
  flex-wrap: wrap;
}

.edu-badge {
  width: 80px; height: 80px;
  background: linear-gradient(135deg, var(--accent), #7c3aed);
  border-radius: 1.2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  flex-shrink: 0;
}

.edu-info { flex: 1; }

.edu-degree {
  font-family: 'Syne', sans-serif;
  font-size: 1.4rem;
  font-weight: 700;
  letter-spacing: -0.5px;
  margin-bottom: 0.3rem;
}

.edu-school {
  color: var(--muted);
  font-size: 0.95rem;
  margin-bottom: 0.6rem;
}

.edu-meta {
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.edu-meta-item {
  font-size: 0.85rem;
  color: var(--ink);
  font-weight: 500;
}

.edu-meta-item span {
  color: var(--muted);
  font-weight: 400;
}

.edu-cgpa {
  font-family: 'Syne', sans-serif;
  font-size: 2.5rem;
  font-weight: 800;
  color: var(--accent);
  text-align: right;
}

.edu-cgpa-label {
  font-size: 0.75rem;
  color: var(--muted);
  letter-spacing: 1px;
  text-transform: uppercase;
  text-align: right;
}

/* ── CONTACT / FOOTER ── */
.contact-section {
  background: var(--ink);
  border-radius: 2rem;
  margin: 0 2rem 4rem;
  padding: 5rem 4rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.contact-section::before {
  content: '';
  position: absolute;
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(26,86,255,0.2) 0%, transparent 70%);
  top: -100px; right: -100px;
  pointer-events: none;
}

.contact-section::after {
  content: '';
  position: absolute;
  width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(255,77,28,0.15) 0%, transparent 70%);
  bottom: -100px; left: -50px;
  pointer-events: none;
}

.contact-section h2 {
  font-family: 'Syne', sans-serif;
  font-size: clamp(2.5rem, 6vw, 5rem);
  font-weight: 800;
  letter-spacing: -2px;
  color: var(--paper);
  margin-bottom: 1rem;
  position: relative;
  z-index: 1;
}

.contact-section p {
  color: rgba(255,255,255,0.5);
  font-size: 1.1rem;
  margin-bottom: 3rem;
  position: relative;
  z-index: 1;
}

.contact-links {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
  position: relative;
  z-index: 1;
}

.contact-link {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  padding: 0.85rem 1.8rem;
  border-radius: 100px;
  font-size: 0.9rem;
  font-weight: 500;
  text-decoration: none;
  transition: all 0.25s;
  letter-spacing: 0.2px;
}

.contact-link-light {
  background: var(--paper);
  color: var(--ink);
}

.contact-link-light:hover {
  background: var(--accent);
  color: #fff;
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(26,86,255,0.4);
}

.contact-link-outline {
  background: transparent;
  color: var(--paper);
  border: 1.5px solid rgba(255,255,255,0.25);
}

.contact-link-outline:hover {
  background: rgba(255,255,255,0.1);
  border-color: rgba(255,255,255,0.5);
  transform: translateY(-2px);
}

footer {
  text-align: center;
  padding: 2rem;
  color: var(--muted);
  font-size: 0.85rem;
  letter-spacing: 0.5px;
}

/* ── ANIMATIONS ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

/* ── DIVIDER ── */
.divider {
  border: none;
  border-top: 1px solid var(--mid);
  margin: 0 4rem;
}

/* ── HAMBURGER ── */
.ham { display: none; flex-direction: column; gap: 5px; cursor: pointer; padding: 4px; }
.ham span { width: 24px; height: 2px; background: var(--ink); border-radius: 2px; transition: all 0.3s; }

/* ── RESPONSIVE ── */
@media (max-width: 768px) {
  nav { padding: 1rem 1.5rem; }
  .nav-links { display: none; }
  .ham { display: flex; }

  .hero { padding: 6rem 1.5rem 3rem; }
  section { padding: 4rem 1.5rem; }
  .skills-section, .contact-section { margin: 0 1rem; padding: 3rem 1.5rem; }
  .contact-section { margin-bottom: 2rem; }
  .divider { margin: 0 1.5rem; }

  .hero h1 { letter-spacing: -1.5px; }
  .hero-stats { gap: 1.8rem; }
  .skills-clusters { grid-template-columns: 1fr; }
  .projects-grid { grid-template-columns: 1fr; }

  .edu-card { flex-direction: column; align-items: flex-start; }
  .edu-cgpa { text-align: left; }
  .edu-cgpa-label { text-align: left; }

  .scroll-hint { display: none; }
}

/* ── HIGHLIGHT EXTRAS ── */
.highlight-strip {
  background: var(--mid);
  border-radius: 1.5rem;
  padding: 2.5rem 3rem;
  margin-top: 2.5rem;
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
}

.highlight-item {
  display: flex;
  align-items: flex-start;
  gap: 0.8rem;
  flex: 1;
  min-width: 200px;
}

.highlight-icon {
  width: 38px; height: 38px;
  border-radius: 10px;
  background: var(--card-bg);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.1rem;
  flex-shrink: 0;
}

.highlight-text {
  font-size: 0.88rem;
  color: var(--ink);
  line-height: 1.55;
}

.highlight-text strong {
  display: block;
  font-weight: 600;
  margin-bottom: 0.2rem;
  font-family: 'Syne', sans-serif;
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">AR<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="ham" onclick="toggleMenu(this)">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="about">
  <div class="hero-bg-text">DEVELOPER</div>
  <div class="hero-inner">
    <div class="hero-badge">Available for opportunities</div>
    <h1>Abhi<br/><em>Rajodiya</em></h1>
    <p class="hero-sub">.NET Full Stack Developer crafting enterprise-grade web applications with ASP.NET Core, Angular, and Microsoft Azure. Based in Ahmedabad, India.</p>
    <div class="hero-actions">
      <a href="mailto:abhipatel1646@gmail.com" class="btn btn-primary">
        ✉ Get in Touch
      </a>
      <a href="https://github.com/AbhiRajodiya" target="_blank" class="btn btn-outline">
        ↗ GitHub
      </a>
    </div>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-num">1.5<span>+</span></div>
        <div class="stat-label">Years Experience</div>
      </div>
      <div class="stat">
        <div class="stat-num">2<span>+</span></div>
        <div class="stat-label">Key Projects</div>
      </div>
      <div class="stat">
        <div class="stat-num">8.67</div>
        <div class="stat-label">CGPA / 10.0</div>
      </div>
    </div>
  </div>
  <div class="scroll-hint">
    <div class="scroll-line"></div>
    <span>Scroll</span>
  </div>
</section>

<hr class="divider"/>

<!-- SKILLS -->
<div class="skills-section" id="skills">
  <div class="section-header">
    <span class="section-num">01</span>
    <h2 class="section-title">Technical Skills</h2>
    <div class="section-line"></div>
  </div>
  <div class="skills-clusters">
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(26,86,255,0.15);">⚙️</div>
      <h4>Backend</h4>
      <div class="skill-tags">
        <span class="skill-tag">ASP.NET Core MVC</span>
        <span class="skill-tag">Web API</span>
        <span class="skill-tag">C#</span>
        <span class="skill-tag">Entity Framework Core</span>
        <span class="skill-tag">Dapper</span>
        <span class="skill-tag">SignalR</span>
        <span class="skill-tag">Async/Await</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(255,77,28,0.15);">🎨</div>
      <h4>Frontend</h4>
      <div class="skill-tags">
        <span class="skill-tag">Angular</span>
        <span class="skill-tag">TypeScript</span>
        <span class="skill-tag">JavaScript</span>
        <span class="skill-tag">HTML5</span>
        <span class="skill-tag">CSS3</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(34,197,94,0.15);">☁️</div>
      <h4>Cloud & DevOps</h4>
      <div class="skill-tags">
        <span class="skill-tag">Microsoft Azure</span>
        <span class="skill-tag">Azure DevOps</span>
        <span class="skill-tag">GitHub Actions</span>
        <span class="skill-tag">CI/CD Pipelines</span>
        <span class="skill-tag">Blob Storage</span>
        <span class="skill-tag">Azure Functions</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(245,158,11,0.15);">🗄️</div>
      <h4>Database</h4>
      <div class="skill-tags">
        <span class="skill-tag">MS SQL Server</span>
        <span class="skill-tag">Database Design</span>
        <span class="skill-tag">Optimization</span>
        <span class="skill-tag">Stored Procedures</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(124,58,237,0.15);">🏗️</div>
      <h4>Architecture</h4>
      <div class="skill-tags">
        <span class="skill-tag">Clean Architecture</span>
        <span class="skill-tag">SOLID Principles</span>
        <span class="skill-tag">Repository Pattern</span>
        <span class="skill-tag">Dependency Injection</span>
        <span class="skill-tag">Microservices</span>
        <span class="skill-tag">MVC</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(236,72,153,0.15);">🛠️</div>
      <h4>Tools & Practices</h4>
      <div class="skill-tags">
        <span class="skill-tag">Visual Studio</span>
        <span class="skill-tag">Git / GitHub</span>
        <span class="skill-tag">Postman</span>
        <span class="skill-tag">Swagger</span>
        <span class="skill-tag">Agile / Scrum</span>
        <span class="skill-tag">JIRA</span>
      </div>
    </div>
  </div>
</div>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-header">
    <span class="section-num">02</span>
    <h2 class="section-title">Experience</h2>
    <div class="section-line"></div>
  </div>
  <div class="exp-timeline">

    <div class="exp-item">
      <div class="exp-date">Aug 2024 — Present</div>
      <div class="exp-role">.NET Developer</div>
      <div class="exp-company"><strong>Rushkar Technology</strong> · Ahmedabad, India</div>
      <ul class="exp-bullets">
        <li>Built real-time communication features using SignalR, enabling live device monitoring dashboards with sub-second data refresh rates.</li>
        <li>Automated build and deployment workflows using Azure DevOps CI/CD pipelines and GitHub Actions, reducing manual deployment errors significantly.</li>
        <li>Deployed and managed cloud-hosted applications on Microsoft Azure — Web Apps, Blob Storage, Azure Functions — gaining hands-on cloud engineering experience.</li>
        <li>Collaborated cross-functionally with senior engineers and product teams in Agile sprints, consistently delivering features on schedule.</li>
        <li>Participated in code reviews and contributed to establishing best practices for API design, error handling, and logging standards.</li>
      </ul>
    </div>

    <div class="exp-item">
      <div class="exp-date">Oct 2022 — Mar 2023</div>
      <div class="exp-role">Full Stack Web Developer Intern</div>
      <div class="exp-company"><strong>Felix IT Systems</strong> · Ahmedabad, India</div>
      <ul class="exp-bullets">
        <li>Developed RESTful APIs in ASP.NET Core and consumed them via Angular front-end components, ensuring seamless data flow and responsive UI.</li>
        <li>Designed and implemented relational database schemas in SQL Server; wrote optimized stored procedures and queries for business-critical modules.</li>
        <li>Led full-stack development of an enterprise calibration management platform (Angular + .NET Core) for a US-based client (Antylia Scientific).</li>
        <li>Optimized MS SQL Server schemas and queries via Entity Framework Core, achieving measurable reduction in API response times.</li>
      </ul>
    </div>

  </div>
</section>

<hr class="divider"/>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-header">
    <span class="section-num">03</span>
    <h2 class="section-title">Key Projects</h2>
    <div class="section-line"></div>
  </div>
  <div class="projects-grid">

    <div class="project-card">
      <div class="project-num">01</div>
      <div class="project-name">LogIngestor — Real-Time Device Monitoring</div>
      <p class="project-desc">A full-stack real-time monitoring platform tracking CPU, GPU, Memory, Disk, and Network metrics with sub-second live updates via SignalR WebSockets.</p>
      <ul class="project-highlights">
        <li>High-throughput log ingestion pipeline with Dapper ORM and optimized SQL Server queries for large-scale telemetry data.</li>
        <li>GPS tracking and remote script execution modules enabling centralized fleet management — adopted in production.</li>
        <li>Clean code principles and modular architecture for long-term maintainability and scalability.</li>
      </ul>
      <div class="project-tech">
        <span class="tech-tag">.NET Core</span>
        <span class="tech-tag">SignalR</span>
        <span class="tech-tag">SQL Server</span>
        <span class="tech-tag">Dapper</span>
        <span class="tech-tag">REST API</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-num">02</div>
      <div class="project-name">Calibration Traceable Live — Enterprise Platform</div>
      <p class="project-desc">End-to-end enterprise calibration management system for Antylia Scientific (US-based), replacing a legacy WPF desktop application with a modern web stack.</p>
      <ul class="project-highlights">
        <li>RESTful APIs for full calibration lifecycle: LOT/Serial Number generation, data entry, certificate generation, Azure Blob auto-upload.</li>
        <li>Angular front-end with real-time data grids supporting 500+ batch lot processing.</li>
        <li>Role-Based Access Control with 4 user tiers, IP whitelisting, and audit trail logging for regulatory compliance.</li>
        <li>Third-party hardware SDK integration and NiceLabel for automated Zebra barcode printing.</li>
      </ul>
      <div class="project-tech">
        <span class="tech-tag">.NET Core Web API</span>
        <span class="tech-tag">Angular</span>
        <span class="tech-tag">EF Core</span>
        <span class="tech-tag">Azure Blob</span>
        <span class="tech-tag">Hardware SDK</span>
      </div>
    </div>

  </div>

  <!-- Highlights -->
  <div class="highlight-strip">
    <div class="highlight-item">
      <div class="highlight-icon">🤖</div>
      <div class="highlight-text">
        <strong>AI-Assisted Dev</strong>
        Proficient with Cursor, GitHub Copilot, ChatGPT, and Claude for faster, cleaner code.
      </div>
    </div>
    <div class="highlight-item">
      <div class="highlight-icon">📡</div>
      <div class="highlight-text">
        <strong>IoT Integration</strong>
        Hands-on experience with hardware-software interfaces and real-time data systems.
      </div>
    </div>
    <div class="highlight-item">
      <div class="highlight-icon">📈</div>
      <div class="highlight-text">
        <strong>Always Upskilling</strong>
        Actively learning Docker, microservices architecture, and unit testing with xUnit/NUnit.
      </div>
    </div>
  </div>
</section>

<hr class="divider"/>

<!-- EDUCATION -->
<section id="education">
  <div class="section-header">
    <span class="section-num">04</span>
    <h2 class="section-title">Education</h2>
    <div class="section-line"></div>
  </div>
  <div class="edu-card">
    <div class="edu-badge">🎓</div>
    <div class="edu-info">
      <div class="edu-degree">B.Tech — Computer Science Engineering</div>
      <div class="edu-school">Indus University, Ahmedabad, India</div>
      <div class="edu-meta">
        <div class="edu-meta-item">Graduated <span>May 2023</span></div>
        <div class="edu-meta-item">Duration <span>Jun 2019 – May 2023</span></div>
      </div>
    </div>
    <div>
      <div class="edu-cgpa">8.67</div>
      <div class="edu-cgpa-label">CGPA / 10.0</div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<div class="contact-section" id="contact">
  <h2>Let's Build Something</h2>
  <p>Open to full-time roles, collaborations, and interesting conversations.</p>
  <div class="contact-links">
    <a href="mailto:abhipatel1646@gmail.com" class="contact-link contact-link-light">✉ abhipatel1646@gmail.com</a>
    <a href="tel:+918401804226" class="contact-link contact-link-outline">📞 +91 8401804226</a>
    <a href="https://linkedin.com/in/abhi-rajodiya" target="_blank" class="contact-link contact-link-outline">in LinkedIn</a>
    <a href="https://github.com/AbhiRajodiya" target="_blank" class="contact-link contact-link-outline">⌥ GitHub</a>
  </div>
</div>

<footer>
  © 2025 Abhi Rajodiya · Ahmedabad, Gujarat, India · Designed & Coded with purpose.
</footer>

<script>
// Intersection Observer for scroll animations
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) { e.target.classList.add('visible'); }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.exp-item, .project-card').forEach(el => observer.observe(el));

// Stagger project cards
document.querySelectorAll('.project-card').forEach((card, i) => {
  card.style.transitionDelay = `${i * 0.12}s`;
});

document.querySelectorAll('.exp-item').forEach((item, i) => {
  item.style.transitionDelay = `${i * 0.15}s`;
});

// Mobile nav toggle
function toggleMenu(btn) {
  const nav = document.querySelector('.nav-links');
  const spans = btn.querySelectorAll('span');
  const isOpen = nav.style.display === 'flex';
  nav.style.display = isOpen ? 'none' : 'flex';
  nav.style.flexDirection = 'column';
  nav.style.position = 'absolute';
  nav.style.top = '70px';
  nav.style.left = '0';
  nav.style.right = '0';
  nav.style.background = 'rgba(247,246,241,0.97)';
  nav.style.padding = '1.5rem 2rem';
  nav.style.borderBottom = '1px solid #e8e4d9';
  spans[0].style.transform = isOpen ? '' : 'rotate(45deg) translate(5px, 5px)';
  spans[1].style.opacity = isOpen ? '1' : '0';
  spans[2].style.transform = isOpen ? '' : 'rotate(-45deg) translate(5px, -5px)';
}

// Close nav on link click
document.querySelectorAll('.nav-links a').forEach(a => {
  a.addEventListener('click', () => {
    const nav = document.querySelector('.nav-links');
    nav.style.display = 'none';
  });
});

// Nav active highlight on scroll
window.addEventListener('scroll', () => {
  const nav = document.querySelector('nav');
  if (window.scrollY > 50) {
    nav.style.boxShadow = '0 2px 20px rgba(0,0,0,0.06)';
  } else {
    nav.style.boxShadow = 'none';
  }
});
</script>

</body>
</html>
