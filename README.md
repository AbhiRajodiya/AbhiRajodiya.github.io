<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0"/>
<title>Abhi Rajodiya — .NET Full Stack Developer</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet"/>
<style>
:root{--ink:#0a0b0f;--paper:#f8f7f2;--mid:#e5e1d6;--accent:#1a56ff;--accent2:#ff4d1c;--muted:#8a8880;--card:#fff;--tag:#edeae0;--glow:rgba(26,86,255,0.18)}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:'DM Sans',sans-serif;background:var(--paper);color:var(--ink);overflow-x:hidden}
#progress-bar{position:fixed;top:0;left:0;height:3px;background:linear-gradient(90deg,var(--accent),var(--accent2));width:0%;z-index:9999;transition:width .1s}
body::before{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");pointer-events:none;z-index:9998;opacity:.5}
nav{position:fixed;top:0;left:0;right:0;z-index:200;display:flex;justify-content:space-between;align-items:center;padding:1.1rem 4rem;backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);background:rgba(248,247,242,.88);border-bottom:1px solid var(--mid);transition:box-shadow .3s}
nav.scrolled{box-shadow:0 4px 30px rgba(0,0,0,.07)}
.nav-logo{font-family:'Syne',sans-serif;font-weight:800;font-size:1.3rem;letter-spacing:-.5px;color:var(--ink);text-decoration:none;display:flex;align-items:center;gap:.3rem}
.nav-dot{width:8px;height:8px;background:var(--accent);border-radius:50%;display:inline-block;animation:pulse 2s ease-in-out infinite}
.nav-links{display:flex;gap:2.2rem;list-style:none}
.nav-links a{text-decoration:none;color:var(--muted);font-size:.88rem;font-weight:500;letter-spacing:.3px;transition:color .2s;position:relative}
.nav-links a::after{content:'';position:absolute;bottom:-3px;left:0;width:0;height:1.5px;background:var(--accent);transition:width .25s}
.nav-links a:hover{color:var(--ink)}
.nav-links a:hover::after{width:100%}
.ham{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:6px;border-radius:8px;transition:background .2s;background:none;border:none}
.ham:hover{background:var(--mid)}
.ham span{width:22px;height:2px;background:var(--ink);border-radius:2px;transition:all .3s;display:block}
.mob-nav{display:none;position:fixed;top:65px;left:0;right:0;background:rgba(248,247,242,.97);backdrop-filter:blur(20px);border-bottom:1px solid var(--mid);padding:1.2rem 2rem;z-index:199;flex-direction:column}
.mob-nav.open{display:flex;animation:slideDown .25s ease}
.mob-nav a{text-decoration:none;color:var(--ink);font-size:.98rem;font-weight:500;padding:.75rem 0;border-bottom:1px solid var(--mid);transition:color .2s,padding-left .2s;display:block}
.mob-nav a:hover{color:var(--accent);padding-left:.5rem}
@keyframes slideDown{from{opacity:0;transform:translateY(-8px)}to{opacity:1;transform:translateY(0)}}
.hero{min-height:100vh;display:flex;align-items:center;padding:8rem 4rem 4rem;position:relative;overflow:hidden;background:radial-gradient(ellipse 80% 60% at 60% 0%,rgba(26,86,255,.06) 0%,transparent 60%),radial-gradient(ellipse 50% 40% at 100% 80%,rgba(255,77,28,.05) 0%,transparent 50%)}
.hero-bg-text{position:absolute;top:50%;left:-2rem;transform:translateY(-50%);font-family:'Syne',sans-serif;font-weight:800;font-size:clamp(7rem,18vw,18rem);color:transparent;-webkit-text-stroke:1.5px var(--mid);white-space:nowrap;pointer-events:none;user-select:none;z-index:0;animation:slideText 30s linear infinite}
@keyframes slideText{0%{transform:translateY(-50%) translateX(0)}100%{transform:translateY(-50%) translateX(-40%)}}
.hero-inner{position:relative;z-index:1;max-width:860px}
.hero-badge{display:inline-flex;align-items:center;gap:.5rem;background:var(--ink);color:var(--paper);padding:.35rem 1rem;border-radius:100px;font-size:.75rem;font-weight:500;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:1.8rem;animation:fadeUp .8s both}
.hero-badge::before{content:'';width:7px;height:7px;background:#22c55e;border-radius:50%;animation:pulse 1.8s ease-in-out infinite}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.5;transform:scale(.7)}}
.hero h1{font-family:'Syne',sans-serif;font-weight:800;font-size:clamp(3rem,7vw,6.5rem);line-height:1.0;letter-spacing:-2px;animation:fadeUp .8s .1s both}
.hero h1 em{font-style:normal;color:var(--accent);position:relative;display:inline-block}
.hero h1 em::after{content:'';position:absolute;bottom:8px;left:0;right:0;height:4px;background:var(--accent2);border-radius:2px;transform:scaleX(0);transform-origin:left;animation:lineIn .6s .9s forwards}
@keyframes lineIn{to{transform:scaleX(1)}}
.hero-sub{margin-top:1.6rem;font-size:1.08rem;color:var(--muted);font-weight:300;max-width:540px;line-height:1.78;animation:fadeUp .8s .2s both}
.hero-actions{margin-top:2.5rem;display:flex;gap:1rem;flex-wrap:wrap;animation:fadeUp .8s .3s both}
.btn{display:inline-flex;align-items:center;gap:.5rem;padding:.85rem 2rem;border-radius:100px;font-size:.92rem;font-weight:500;text-decoration:none;transition:all .25s;cursor:pointer;border:none;font-family:'DM Sans',sans-serif}
.btn-primary{background:var(--ink);color:var(--paper)}
.btn-primary:hover{background:var(--accent);transform:translateY(-3px);box-shadow:0 12px 30px var(--glow)}
.btn-outline{background:transparent;color:var(--ink);border:1.5px solid currentColor}
.btn-outline:hover{background:var(--ink);color:var(--paper);transform:translateY(-3px)}
.hero-stats{margin-top:3.5rem;display:flex;gap:3rem;flex-wrap:wrap;animation:fadeUp .8s .4s both}
.stat-num{font-family:'Syne',sans-serif;font-size:2.4rem;font-weight:800;line-height:1}
.stat-num span{color:var(--accent)}
.stat-label{font-size:.8rem;color:var(--muted);letter-spacing:.5px;margin-top:.25rem}
.scroll-hint{position:absolute;bottom:2.5rem;right:4rem;display:flex;flex-direction:column;align-items:center;gap:.5rem;color:var(--muted);font-size:.72rem;letter-spacing:1.5px;text-transform:uppercase;animation:fadeUp 1s .8s both}
.scroll-line{width:1px;height:60px;background:linear-gradient(to bottom,var(--muted),transparent);animation:scrollAnim 1.5s ease-in-out infinite}
@keyframes scrollAnim{0%,100%{opacity:1;transform:scaleY(1)}50%{opacity:.3;transform:scaleY(.5)}}
section{padding:6rem 4rem;max-width:1200px;margin:0 auto}
.section-header{display:flex;align-items:baseline;gap:1rem;margin-bottom:3.5rem}
.section-num{font-family:'Syne',sans-serif;font-size:.78rem;font-weight:700;color:var(--accent);letter-spacing:2px;text-transform:uppercase}
.section-title{font-family:'Syne',sans-serif;font-weight:800;font-size:clamp(2rem,4vw,3rem);letter-spacing:-1.5px}
.section-line{flex:1;height:1px;background:var(--mid);margin-left:1rem}
.skills-section{background:linear-gradient(135deg,#0a0b0f 0%,#111827 100%);border-radius:2.5rem;padding:4rem;margin:0 2rem;position:relative;overflow:hidden}
.skills-section::before{content:'';position:absolute;width:600px;height:600px;background:radial-gradient(circle,rgba(26,86,255,.12) 0%,transparent 60%);top:-200px;right:-100px;pointer-events:none}
.skills-section .section-title{color:#f8f7f2}
.skills-section .section-num{color:#5b9dff}
.skills-section .section-line{background:rgba(255,255,255,.08)}
.skills-clusters{display:grid;grid-template-columns:repeat(auto-fit,minmax(255px,1fr));gap:1.2rem;margin-top:2rem}
.skill-cluster{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.07);border-radius:1.2rem;padding:1.8rem;transition:all .3s;position:relative;overflow:hidden}
.skill-cluster:hover{background:rgba(255,255,255,.07);transform:translateY(-5px);border-color:rgba(255,255,255,.12);box-shadow:0 20px 40px rgba(0,0,0,.3)}
.skill-cluster-icon{width:44px;height:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:1.3rem;margin-bottom:1rem}
.skill-cluster h4{font-family:'Syne',sans-serif;font-size:.82rem;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:rgba(255,255,255,.45);margin-bottom:1rem}
.skill-tags{display:flex;flex-wrap:wrap;gap:.45rem}
.skill-tag{background:rgba(255,255,255,.08);color:rgba(255,255,255,.82);padding:.28rem .75rem;border-radius:100px;font-size:.8rem;border:1px solid rgba(255,255,255,.05);transition:all .2s}
.skill-tag:hover{background:rgba(26,86,255,.25);border-color:rgba(26,86,255,.4);color:#fff}
.exp-timeline{position:relative}
.exp-timeline::before{content:'';position:absolute;left:0;top:0;bottom:0;width:1px;background:linear-gradient(to bottom,var(--accent),var(--mid))}
.exp-item{padding-left:2.5rem;padding-bottom:3.5rem;position:relative;opacity:0;transform:translateY(20px);transition:opacity .6s,transform .6s}
.exp-item.visible{opacity:1;transform:translateY(0)}
.exp-item::before{content:'';position:absolute;left:-5px;top:6px;width:11px;height:11px;border-radius:50%;background:var(--accent);border:2px solid var(--paper);box-shadow:0 0 0 3px var(--accent),0 0 16px var(--glow)}
.exp-date{font-size:.76rem;font-weight:500;color:var(--accent);letter-spacing:1px;text-transform:uppercase;margin-bottom:.5rem}
.exp-role{font-family:'Syne',sans-serif;font-size:1.4rem;font-weight:700;letter-spacing:-.5px;margin-bottom:.3rem}
.exp-company{font-size:.93rem;color:var(--muted);margin-bottom:1.2rem}
.exp-company strong{color:var(--ink);font-weight:500}
.exp-bullets{list-style:none}
.exp-bullets li{position:relative;padding-left:1.3rem;margin-bottom:.6rem;font-size:.93rem;color:#3a3a3a;line-height:1.65}
.exp-bullets li::before{content:'\2192';position:absolute;left:0;color:var(--accent);font-size:.88rem}
.projects-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(340px,1fr));gap:1.8rem}
.project-card{background:var(--card);border-radius:1.8rem;padding:2.2rem;border:1px solid var(--mid);position:relative;overflow:hidden;opacity:0;transform:translateY(20px);transition:opacity .5s,transform .5s,box-shadow .3s}
.project-card.visible{opacity:1;transform:translateY(0)}
.project-card:hover{transform:translateY(-8px);box-shadow:0 24px 60px rgba(0,0,0,.1)}
.project-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px}
.project-card:nth-child(1)::before{background:linear-gradient(90deg,var(--accent),#7c3aed)}
.project-card:nth-child(2)::before{background:linear-gradient(90deg,var(--accent2),#f59e0b)}
.project-num{font-family:'Syne',sans-serif;font-size:3.5rem;font-weight:800;color:var(--mid);line-height:1;margin-bottom:.5rem}
.project-name{font-family:'Syne',sans-serif;font-size:1.25rem;font-weight:700;letter-spacing:-.5px;margin-bottom:.8rem}
.project-desc{font-size:.88rem;color:var(--muted);line-height:1.68;margin-bottom:1.5rem}
.project-highlights{list-style:none;margin-bottom:1.5rem}
.project-highlights li{font-size:.87rem;color:#3a3a3a;padding:.4rem 0;border-bottom:1px solid var(--mid);display:flex;align-items:flex-start;gap:.6rem;line-height:1.5}
.project-highlights li::before{content:'\25C6';color:var(--accent);font-size:.45rem;margin-top:.4rem;flex-shrink:0}
.project-tech{display:flex;flex-wrap:wrap;gap:.4rem}
.tech-tag{background:var(--tag);color:var(--ink);padding:.25rem .7rem;border-radius:100px;font-size:.76rem;font-weight:500}
.highlight-strip{background:linear-gradient(135deg,var(--mid),#f0ede3);border-radius:1.8rem;padding:2.5rem 3rem;margin-top:2.5rem;display:flex;flex-wrap:wrap;gap:1.5rem}
.highlight-item{display:flex;align-items:flex-start;gap:.8rem;flex:1;min-width:180px}
.highlight-icon{width:40px;height:40px;border-radius:12px;background:var(--card);display:flex;align-items:center;justify-content:center;font-size:1.1rem;flex-shrink:0;box-shadow:0 2px 12px rgba(0,0,0,.06)}
.highlight-text{font-size:.87rem;line-height:1.55}
.highlight-text strong{display:block;font-weight:600;margin-bottom:.2rem;font-family:'Syne',sans-serif}
.edu-card{background:var(--card);border-radius:1.8rem;padding:2.5rem;border:1px solid var(--mid);display:flex;gap:2rem;align-items:center;flex-wrap:wrap;transition:box-shadow .3s}
.edu-card:hover{box-shadow:0 16px 48px rgba(0,0,0,.08)}
.edu-badge{width:80px;height:80px;background:linear-gradient(135deg,var(--accent),#7c3aed);border-radius:1.2rem;display:flex;align-items:center;justify-content:center;font-size:2rem;flex-shrink:0;box-shadow:0 8px 24px var(--glow)}
.edu-info{flex:1}
.edu-degree{font-family:'Syne',sans-serif;font-size:1.35rem;font-weight:700;letter-spacing:-.5px;margin-bottom:.3rem}
.edu-school{color:var(--muted);font-size:.93rem;margin-bottom:.6rem}
.edu-meta{display:flex;gap:1.5rem;flex-wrap:wrap}
.edu-meta-item{font-size:.84rem;font-weight:500}
.edu-meta-item span{color:var(--muted);font-weight:400}
.edu-cgpa{font-family:'Syne',sans-serif;font-size:2.5rem;font-weight:800;color:var(--accent);text-align:right}
.edu-cgpa-label{font-size:.72rem;color:var(--muted);letter-spacing:1px;text-transform:uppercase;text-align:right}
.contact-section{background:linear-gradient(135deg,#0a0b0f 0%,#111827 60%,#0f0f1a 100%);border-radius:2.5rem;margin:0 2rem 4rem;padding:5rem 4rem;text-align:center;position:relative;overflow:hidden}
.contact-section::before{content:'';position:absolute;width:600px;height:600px;background:radial-gradient(circle,rgba(26,86,255,.18) 0%,transparent 60%);top:-150px;right:-100px;pointer-events:none}
.contact-section::after{content:'';position:absolute;width:400px;height:400px;background:radial-gradient(circle,rgba(255,77,28,.12) 0%,transparent 60%);bottom:-100px;left:-50px;pointer-events:none}
.contact-section h2{font-family:'Syne',sans-serif;font-size:clamp(2.5rem,6vw,5rem);font-weight:800;letter-spacing:-2px;color:#f8f7f2;margin-bottom:1rem;position:relative;z-index:1}
.contact-section p{color:rgba(255,255,255,.45);font-size:1.05rem;margin-bottom:3rem;position:relative;z-index:1}
.contact-links{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;position:relative;z-index:1}
.contact-link{display:inline-flex;align-items:center;gap:.6rem;padding:.85rem 1.8rem;border-radius:100px;font-size:.88rem;font-weight:500;text-decoration:none;transition:all .25s;font-family:'DM Sans',sans-serif}
.contact-link-light{background:#f8f7f2;color:var(--ink)}
.contact-link-light:hover{background:var(--accent);color:#fff;transform:translateY(-3px);box-shadow:0 12px 30px rgba(26,86,255,.4)}
.contact-link-outline{background:transparent;color:#f8f7f2;border:1.5px solid rgba(255,255,255,.2)}
.contact-link-outline:hover{background:rgba(255,255,255,.08);border-color:rgba(255,255,255,.45);transform:translateY(-3px)}
footer{text-align:center;padding:2rem;color:var(--muted);font-size:.83rem;letter-spacing:.5px}
@keyframes fadeUp{from{opacity:0;transform:translateY(30px)}to{opacity:1;transform:translateY(0)}}
.divider{border:none;border-top:1px solid var(--mid);margin:0 4rem}
@media(max-width:900px){nav{padding:1rem 2rem}.hero{padding:7rem 2rem 3rem}section{padding:4.5rem 2rem}.skills-section,.contact-section{margin:0 1.5rem;padding:3.5rem 2rem}.contact-section{margin-bottom:2rem}.divider{margin:0 2rem}.highlight-strip{padding:2rem}}
@media(max-width:640px){nav{padding:1rem 1.25rem}.nav-links{display:none}.ham{display:flex}.hero{padding:6rem 1.25rem 3rem}.hero h1{letter-spacing:-1.5px}.hero-stats{gap:1.8rem}section{padding:3.5rem 1.25rem}.skills-section,.contact-section{margin:0 .75rem;padding:2.5rem 1.25rem;border-radius:1.5rem}.contact-section{margin-bottom:2rem}.divider{margin:0 1.25rem}.skills-clusters{grid-template-columns:1fr}.projects-grid{grid-template-columns:1fr}.edu-card{flex-direction:column;align-items:flex-start}.edu-cgpa,.edu-cgpa-label{text-align:left}.scroll-hint{display:none}.highlight-strip{padding:1.5rem;flex-direction:column}.highlight-item{min-width:100%}.contact-links{flex-direction:column;align-items:center}.hero-actions{flex-direction:column;align-items:flex-start}}
</style></head><body>
<div id="progress-bar"></div>
<nav id="navbar">
  <a href="#" class="nav-logo">AR<span class="nav-dot"></span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <button class="ham" id="ham-btn" aria-label="Toggle menu" onclick="toggleMenu()">
    <span id="h1"></span><span id="h2"></span><span id="h3"></span>
  </button>
</nav>
<nav class="mob-nav" id="mob-nav">
  <a href="#about" onclick="closeMob()">About</a>
  <a href="#skills" onclick="closeMob()">Skills</a>
  <a href="#experience" onclick="closeMob()">Experience</a>
  <a href="#projects" onclick="closeMob()">Projects</a>
  <a href="#contact" onclick="closeMob()">Contact</a>
</nav>

<section class="hero" id="about">
  <div class="hero-bg-text">DEVELOPER</div>
  <div class="hero-inner">
    <div class="hero-badge">Available for opportunities</div>
    <h1>Abhi<br/><em>Rajodiya</em></h1>
    <p class="hero-sub">.NET Full Stack Developer crafting enterprise-grade web applications with ASP.NET Core, Angular, and Microsoft Azure. Based in Ahmedabad, India.</p>
    <div class="hero-actions">
      <a href="mailto:abhipatel1646@gmail.com" class="btn btn-primary">&#9993; Get in Touch</a>
      <a href="https://github.com/AbhiRajodiya" target="_blank" class="btn btn-outline">&#8599; GitHub</a>
    </div>
    <div class="hero-stats">
      <div class="stat"><div class="stat-num">1.5<span>+</span></div><div class="stat-label">Years Experience</div></div>
      <div class="stat"><div class="stat-num">2<span>+</span></div><div class="stat-label">Key Projects</div></div>
      <div class="stat"><div class="stat-num">8.67</div><div class="stat-label">CGPA / 10.0</div></div>
    </div>
  </div>
  <div class="scroll-hint"><div class="scroll-line"></div><span>Scroll</span></div>
</section>

<hr class="divider"/>

<div class="skills-section" id="skills">
  <div class="section-header">
    <span class="section-num">01</span>
    <h2 class="section-title">Technical Skills</h2>
    <div class="section-line"></div>
  </div>
  <div class="skills-clusters">
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(26,86,255,.15)">&#9881;&#65039;</div>
      <h4>Backend</h4>
      <div class="skill-tags">
        <span class="skill-tag">ASP.NET Core MVC</span><span class="skill-tag">Web API</span><span class="skill-tag">C#</span><span class="skill-tag">Entity Framework Core</span><span class="skill-tag">Dapper</span><span class="skill-tag">SignalR</span><span class="skill-tag">Async/Await</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(255,77,28,.15)">&#127912;</div>
      <h4>Frontend</h4>
      <div class="skill-tags">
        <span class="skill-tag">Angular</span><span class="skill-tag">TypeScript</span><span class="skill-tag">JavaScript</span><span class="skill-tag">HTML5</span><span class="skill-tag">CSS3</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(34,197,94,.15)">&#9925;</div>
      <h4>Cloud &amp; DevOps</h4>
      <div class="skill-tags">
        <span class="skill-tag">Microsoft Azure</span><span class="skill-tag">Azure DevOps</span><span class="skill-tag">GitHub Actions</span><span class="skill-tag">CI/CD Pipelines</span><span class="skill-tag">Blob Storage</span><span class="skill-tag">Azure Functions</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(245,158,11,.15)">&#128452;&#65039;</div>
      <h4>Database</h4>
      <div class="skill-tags">
        <span class="skill-tag">MS SQL Server</span><span class="skill-tag">Database Design</span><span class="skill-tag">Optimization</span><span class="skill-tag">Stored Procedures</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(124,58,237,.15)">&#127959;</div>
      <h4>Architecture</h4>
      <div class="skill-tags">
        <span class="skill-tag">Clean Architecture</span><span class="skill-tag">SOLID Principles</span><span class="skill-tag">Repository Pattern</span><span class="skill-tag">Dependency Injection</span><span class="skill-tag">Microservices</span><span class="skill-tag">MVC</span>
      </div>
    </div>
    <div class="skill-cluster">
      <div class="skill-cluster-icon" style="background:rgba(236,72,153,.15)">&#128295;</div>
      <h4>Tools &amp; Practices</h4>
      <div class="skill-tags">
        <span class="skill-tag">Visual Studio</span><span class="skill-tag">Git / GitHub</span><span class="skill-tag">Postman</span><span class="skill-tag">Swagger</span><span class="skill-tag">Agile / Scrum</span><span class="skill-tag">JIRA</span>
      </div>
    </div>
  </div>
</div>

<section id="experience">
  <div class="section-header">
    <span class="section-num">02</span>
    <h2 class="section-title">Experience</h2>
    <div class="section-line"></div>
  </div>
  <div class="exp-timeline">
    <div class="exp-item">
      <div class="exp-date">Aug 2024 &mdash; Present</div>
      <div class="exp-role">.NET Developer</div>
      <div class="exp-company"><strong>Rushkar Technology</strong> &middot; Ahmedabad, India</div>
      <ul class="exp-bullets">
        <li>Built real-time communication features using SignalR, enabling live device monitoring dashboards with sub-second data refresh rates.</li>
        <li>Automated build and deployment workflows using Azure DevOps CI/CD pipelines and GitHub Actions, reducing manual deployment errors significantly.</li>
        <li>Deployed and managed cloud-hosted applications on Microsoft Azure &mdash; Web Apps, Blob Storage, Azure Functions.</li>
        <li>Collaborated cross-functionally with senior engineers in Agile sprints, consistently delivering features on schedule.</li>
        <li>Participated in code reviews and contributed to best practices for API design, error handling, and logging standards.</li>
      </ul>
    </div>
    <div class="exp-item">
      <div class="exp-date">Oct 2022 &mdash; Mar 2023</div>
      <div class="exp-role">Full Stack Web Developer Intern</div>
      <div class="exp-company"><strong>Felix IT Systems</strong> &middot; Ahmedabad, India</div>
      <ul class="exp-bullets">
        <li>Developed RESTful APIs in ASP.NET Core and consumed them via Angular front-end components, ensuring seamless data flow and responsive UI.</li>
        <li>Designed relational database schemas in SQL Server; wrote optimized stored procedures for business-critical modules.</li>
        <li>Led full-stack development of an enterprise calibration management platform (Angular + .NET Core) for a US-based client (Antylia Scientific).</li>
        <li>Optimized MS SQL Server schemas via Entity Framework Core, achieving measurable reduction in API response times.</li>
      </ul>
    </div>
  </div>
</section>

<hr class="divider"/>

<section id="projects">
  <div class="section-header">
    <span class="section-num">03</span>
    <h2 class="section-title">Key Projects</h2>
    <div class="section-line"></div>
  </div>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-num">01</div>
      <div class="project-name">LogIngestor &mdash; Real-Time Device Monitoring</div>
      <p class="project-desc">A full-stack real-time monitoring platform tracking CPU, GPU, Memory, Disk, and Network metrics with sub-second live updates via SignalR WebSockets.</p>
      <ul class="project-highlights">
        <li>High-throughput log ingestion pipeline with Dapper ORM and optimized SQL Server queries for large-scale telemetry data.</li>
        <li>GPS tracking and remote script execution modules enabling centralized fleet management &mdash; adopted in production.</li>
        <li>Clean code principles and modular architecture for long-term maintainability and scalability.</li>
      </ul>
      <div class="project-tech">
        <span class="tech-tag">.NET Core</span><span class="tech-tag">SignalR</span><span class="tech-tag">SQL Server</span><span class="tech-tag">Dapper</span><span class="tech-tag">REST API</span>
      </div>
    </div>
    <div class="project-card">
      <div class="project-num">02</div>
      <div class="project-name">Calibration Traceable Live &mdash; Enterprise Platform</div>
      <p class="project-desc">End-to-end enterprise calibration management system for Antylia Scientific (US-based), replacing a legacy WPF desktop application with a modern web stack.</p>
      <ul class="project-highlights">
        <li>RESTful APIs for full calibration lifecycle: LOT/Serial Number generation, data entry, certificate generation, Azure Blob auto-upload.</li>
        <li>Angular front-end with real-time data grids supporting 500+ batch lot processing.</li>
        <li>Role-Based Access Control with 4 user tiers, IP whitelisting, and audit trail logging for regulatory compliance.</li>
        <li>Third-party hardware SDK integration and NiceLabel for automated Zebra barcode printing.</li>
      </ul>
      <div class="project-tech">
        <span class="tech-tag">.NET Core Web API</span><span class="tech-tag">Angular</span><span class="tech-tag">EF Core</span><span class="tech-tag">Azure Blob</span><span class="tech-tag">Hardware SDK</span>
      </div>
    </div>
  </div>
  <div class="highlight-strip">
    <div class="highlight-item">
      <div class="highlight-icon">&#129302;</div>
      <div class="highlight-text"><strong>AI-Assisted Dev</strong>Proficient with Cursor, GitHub Copilot, ChatGPT, and Claude for faster, cleaner code.</div>
    </div>
    <div class="highlight-item">
      <div class="highlight-icon">&#128225;</div>
      <div class="highlight-text"><strong>IoT Integration</strong>Hands-on experience with hardware-software interfaces and real-time data systems.</div>
    </div>
    <div class="highlight-item">
      <div class="highlight-icon">&#128200;</div>
      <div class="highlight-text"><strong>Always Upskilling</strong>Actively learning Docker, microservices architecture, and unit testing with xUnit/NUnit.</div>
    </div>
  </div>
</section>

<hr class="divider"/>

<section id="education">
  <div class="section-header">
    <span class="section-num">04</span>
    <h2 class="section-title">Education</h2>
    <div class="section-line"></div>
  </div>
  <div class="edu-card">
    <div class="edu-badge">&#127891;</div>
    <div class="edu-info">
      <div class="edu-degree">B.Tech &mdash; Computer Science Engineering</div>
      <div class="edu-school">Indus University, Ahmedabad, India</div>
      <div class="edu-meta">
        <div class="edu-meta-item">Graduated <span>May 2023</span></div>
        <div class="edu-meta-item">Duration <span>Jun 2019 &ndash; May 2023</span></div>
      </div>
    </div>
    <div>
      <div class="edu-cgpa">8.67</div>
      <div class="edu-cgpa-label">CGPA / 10.0</div>
    </div>
  </div>
</section>

<div class="contact-section" id="contact">
  <h2>Let&rsquo;s Build Something</h2>
  <p>Open to full-time roles, collaborations, and interesting conversations.</p>
  <div class="contact-links">
    <a href="mailto:abhipatel1646@gmail.com" class="contact-link contact-link-light">&#9993; abhipatel1646@gmail.com</a>
    <a href="tel:+918401804226" class="contact-link contact-link-outline">&#128222; +91 8401804226</a>
    <a href="https://linkedin.com/in/abhi-rajodiya" target="_blank" class="contact-link contact-link-outline">in LinkedIn</a>
    <a href="https://github.com/AbhiRajodiya" target="_blank" class="contact-link contact-link-outline">&#9251; GitHub</a>
  </div>
</div>

<footer>&copy; 2025 Abhi Rajodiya &middot; Ahmedabad, Gujarat, India &middot; Designed &amp; Coded with purpose.</footer>

<script>
const obs = new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting)e.target.classList.add('visible')})},{threshold:0.1});
document.querySelectorAll('.exp-item,.project-card').forEach(el=>obs.observe(el));
document.querySelectorAll('.project-card').forEach((c,i)=>c.style.transitionDelay=i*0.12+'s');
document.querySelectorAll('.exp-item').forEach((el,i)=>el.style.transitionDelay=i*0.15+'s');
let mobOpen=false;
function toggleMenu(){
  mobOpen=!mobOpen;
  document.getElementById('mob-nav').classList.toggle('open',mobOpen);
  const s=document.querySelectorAll('#ham-btn span');
  s[0].style.transform=mobOpen?'rotate(45deg) translate(5px,5px)':'';
  s[1].style.opacity=mobOpen?'0':'1';
  s[2].style.transform=mobOpen?'rotate(-45deg) translate(5px,-5px)':'';
}
function closeMob(){
  mobOpen=false;
  document.getElementById('mob-nav').classList.remove('open');
  const s=document.querySelectorAll('#ham-btn span');
  s[0].style.transform='';s[1].style.opacity='1';s[2].style.transform='';
}
window.addEventListener('scroll',()=>{
  const pct=window.scrollY/(document.body.scrollHeight-window.innerHeight)*100;
  document.getElementById('progress-bar').style.width=pct+'%';
  document.getElementById('navbar').classList.toggle('scrolled',window.scrollY>50);
});
</script>
</body></html>
