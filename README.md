
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Abhi Rajodiya | .NET Developer</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet" />
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet" />
  <style>
    :root {
      --accent: #6366f1;
      --accent-light: #a5b4fc;
      --accent-gradient: linear-gradient(90deg,#6366f1 0%,#3b82f6 100%);
      --bg: #f3f4f6;
      --bg-card: #fff;
      --shadow: 0 6px 24px 0 rgba(99,102,241,0.09);
      --radius: 16px;
      --header-bg: #18181b;
      --header-txt: #fff;
      --footer-bg: #18181b;
      --footer-txt: #fff;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: var(--bg);
      color: #1f2937;
      transition: background 0.3s;
    }
    header {
      background: var(--header-bg);
      color: var(--header-txt);
      padding: 1.5rem 3rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 2px 18px rgba(99,102,241,0.07);
    }
    header strong {
      letter-spacing: 1px;
      font-size: 1.4rem;
      background: var(--accent-gradient);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-fill-color: transparent;
    }
    nav {
      display: flex;
      align-items: center;
    }
    nav a {
      color: var(--header-txt);
      margin-left: 1.5rem;
      text-decoration: none;
      font-weight: 500;
      letter-spacing: .5px;
      transition: color 0.2s;
      position: relative;
    }
    nav a::after {
      content: "";
      display: block;
      width: 0;
      height: 2px;
      background: var(--accent-gradient);
      transition: width .3s;
      border-radius: 2px;
      margin: 2px 0 0 0;
    }
    nav a:hover, nav a.active {
      color: var(--accent);
    }
    nav a:hover::after, nav a.active::after {
      width: 100%;
    }
    @media (max-width: 900px) {
      header, section {
        padding-left: 1.5rem;
        padding-right: 1.5rem;
      }
      nav a { margin-left: 1rem; }
    }
    @media (max-width: 600px) {
      header {
        flex-direction: column;
        align-items: flex-start;
        padding: 1rem 1rem;
      }
      nav { margin-top: 0.5rem; flex-wrap: wrap; }
      nav a { margin: 0 0.7rem 0.5rem 0; }
    }
    section {
      padding: 4rem 3rem;
      max-width: 1000px;
      margin: auto;
      animation: fadeInUp 0.7s;
    }
    @media (max-width: 700px) {
      section {
        padding: 2rem 0.5rem;
      }
    }
    h2.section-title {
      font-size: 2.3rem;
      text-align: center;
      margin-bottom: 2.2rem;
      background: var(--accent-gradient);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-fill-color: transparent;
      letter-spacing: 1.2px;
      font-weight: 700;
    }
    .intro {
      text-align: center;
      background: var(--accent-gradient);
      color: #fff;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      margin-bottom: 2.5rem;
      padding: 2.5rem 1.5rem 2rem 1.5rem;
      position: relative;
      overflow: hidden;
    }
    .intro::before {
      content: "";
      background: url('https://www.transparenttextures.com/patterns/cubes.png') repeat;
      opacity: .13;
      position: absolute; inset: 0;
      z-index: 0;
    }
    .intro h1 {
      font-size: 2.8rem;
      margin-bottom: 0.7rem;
      position: relative;
      z-index: 1;
      font-weight: 700;
    }
    .intro p {
      font-size: 1.2rem;
      font-weight: 400;
      letter-spacing: .2px;
      margin: 0;
      position: relative;
      z-index: 1;
    }

    .skills-grid, .exp-grid, .project-grid, .edu-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.5rem;
    }
    .card {
      background: var(--bg-card);
      padding: 1.6rem 1.3rem;
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      transition: transform 0.3s, box-shadow 0.3s;
      position: relative;
      z-index: 1;
      overflow: hidden;
      border-left: 5px solid var(--accent-light);
    }
    .card:hover {
      transform: translateY(-7px) scale(1.03) rotate(-0.5deg);
      box-shadow: 0 10px 32px 0 rgba(99,102,241,0.13);
      border-left: 7px solid var(--accent);
    }
    .skills-grid .card {
      font-size: 1.1rem;
      font-weight: 500;
      text-align: center;
      background: linear-gradient(135deg,#e0e7ff 0%,#f0f9ff 100%);
      color: #4338ca;
      border: none;
      box-shadow: 0 2px 12px 0 rgba(99,102,241,0.08);
      letter-spacing: .5px;
      border-radius: 12px;
      padding: 1rem 0.5rem;
    }
    .project-grid .card {
      background: linear-gradient(120deg,#f1f5f9 70%,#e0e7ff 100%);
      border-left: 5px solid #818cf8;
    }
    .exp-grid .card {
      border-left: 5px solid #60a5fa;
      background: linear-gradient(120deg,#f0f9ff 85%,#e0e7ff 100%);
    }
    .edu-grid .card {
      border-left: 5px solid #f87171;
      background: linear-gradient(120deg,#fef2f2 85%,#f3f4f6 100%);
    }
    .card h4 {
      margin-top: 0;
      margin-bottom: .7rem;
      color: var(--accent);
      font-weight: 600;
      font-size: 1.12rem;
      letter-spacing: .7px;
    }
    .card p {
      margin: .5rem 0 0.3rem 0;
      color: #374151;
      font-size: 1rem;
      line-height: 1.5;
    }
    .card em {
      color: #6366f1;
      font-style: normal;
      font-weight: 500;
      font-size: .98rem;
    }
    .contact {
      text-align: center;
      margin-top: 2.5rem;
    }
    .contact a {
      display: inline-block;
      margin: 0.5rem 0.8rem;
      color: var(--accent);
      background: #fff;
      border-radius: 24px;
      padding: 0.45rem 1.1rem;
      text-decoration: none;
      font-size: 1.12rem;
      font-weight: 500;
      letter-spacing: .5px;
      box-shadow: 0 2px 8px 0 rgba(99,102,241,0.09);
      transition: background 0.2s, color 0.2s, transform 0.2s;
      border: 1.5px solid var(--accent-light);
      position: relative;
      top: 0;
    }
    .contact a:hover {
      background: var(--accent-gradient);
      color: #fff;
      transform: translateY(-2px) scale(1.04);
      border: 1.5px solid #6366f1;
    }
    .contact i {
      margin-right: 0.5rem;
      color: var(--accent);
    }
    .contact p {
      margin: 0.5rem 0;
    }
    footer {
      text-align: center;
      padding: 2rem;
      background: var(--footer-bg);
      color: var(--footer-txt);
      font-size: 1.1rem;
      letter-spacing: 1px;
      margin-top: 2.5rem;
    }
    /* Animations */
    @keyframes fadeInUp {
      from { opacity:0; transform:translateY(40px);}
      to { opacity:1; transform:translateY(0);}
    }
    /* Mobile improvements */
    @media (max-width: 480px) {
      .intro h1 { font-size: 2.1rem; }
      h2.section-title { font-size: 1.35rem; }
      .skills-grid, .exp-grid, .project-grid, .edu-grid {
        grid-template-columns: 1fr;
      }
      .card { padding: 1.2rem 0.7rem;}
      section { padding: 1.3rem 0.2rem;}
    }
    /* Scrollbar styling */
    ::-webkit-scrollbar {
      width: 8px;
      background: #e0e7ff;
    }
    ::-webkit-scrollbar-thumb {
      background: #a5b4fc;
      border-radius: 8px;
    }
  </style>
</head>
<body>

  <header>
    <div><strong>Abhi Rajodiya</strong></div>
    <nav>
      <a href="#profile">Profile</a>
      <a href="#skills">Skills</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="intro" data-aos="fade-up">
    <h1>Hello! I'm Abhi Rajodiya 👋</h1>
    <p>A passionate <b>.NET Developer</b> with experience in full-stack web development and real-time applications.</p>
  </section>

  <section id="profile" data-aos="fade-right">
    <h2 class="section-title">Profile</h2>
    <p>I am a dedicated <b>.NET Developer</b> specializing in building and maintaining web applications using <b>ASP.NET Core MVC</b> and <b>SQL Server</b>. Skilled in efficient coding, debugging, and effective database management.</p>
  </section>

  <section id="skills" data-aos="fade-left">
    <h2 class="section-title">Skills</h2>
    <div class="skills-grid">
      <div class="card"><i class="fab fa-cuttlefish"></i> C#</div>
      <div class="card"><i class="fa-solid fa-code"></i> ASP.NET Core MVC</div>
      <div class="card"><i class="fas fa-database"></i> SQL Server</div>
      <div class="card"><i class="fas fa-plug"></i> REST API</div>
      <div class="card"><i class="fab fa-js"></i> JavaScript</div>
      <div class="card"><i class="fab fa-js-square"></i> JQuery</div>
      <div class="card"><i class="fab fa-html5"></i> HTML5 & CSS3</div>
      <div class="card"><i class="fab fa-python"></i> Python</div>
    </div>
  </section>

  <section id="experience" data-aos="zoom-in-up">
    <h2 class="section-title">Experience</h2>
    <div class="exp-grid">
      <div class="card">
        <h4>Rushkar Technology</h4>
        <p><em>.NET Developer Trainee</em> | Sep 2024 – Nov 2024</p>
        <p>Worked on <b>ASP.NET Core</b>, database integration, debugging, and collaborated on building enterprise-grade web apps.</p>
      </div>
      <div class="card">
        <h4>Felix IT Systems</h4>
        <p><em>Full Stack Web Developer Intern</em> | Oct 2022 – Mar 2023</p>
        <p>Built full-stack projects with both frontend and backend technologies; enhanced deployment & team collaboration skills.</p>
      </div>
    </div>
  </section>

  <section id="projects" data-aos="fade-up">
    <h2 class="section-title">Projects</h2>
    <div class="project-grid">
      <div class="card">
        <h4>Fitness Tracker</h4>
        <p>ASP.NET MVC app with user authentication, goal tracking, and data visualization via <b>Chart.js/D3.js</b>.</p>
      </div>
      <div class="card">
        <h4>Hospital Admin System</h4>
        <p>ASP.NET MVC-based system with patient registration, appointment scheduling, medical record handling using <b>EF</b>.</p>
      </div>
      <div class="card">
        <h4>Weather Application</h4>
        <p>Weather API integration with <b>OpenWeatherMap</b> using async calls, responsive UI with <b>Bootstrap</b>.</p>
      </div>
    </div>
  </section>

  <section id="education" data-aos="fade-right">
    <h2 class="section-title">Education</h2>
    <div class="edu-grid">
      <div class="card">
        <h4>Indus University</h4>
        <p><em>B.Tech in Computer Science</em></p>
        <p>Jun 2019 – May 2023 | Ahmedabad, India</p>
      </div>
    </div>
  </section>

  <section id="contact" class="contact" data-aos="zoom-in">
    <h2 class="section-title">Contact Me</h2>
    <p>
      <a href="mailto:abhipatel1646@gmail.com"><i class="fas fa-envelope"></i> abhipatel1646@gmail.com</a>
      <a href="tel:8401804226"><i class="fas fa-phone"></i> +91 8401804226</a>
    </p>
    <p>
      <a href="https://linkedin.com/in/abhi-rajodiya" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
      <a href="https://github.com/AbhiRajodiya" target="_blank"><i class="fab fa-github"></i> GitHub</a>
    </p>
  </section>

  <footer>
    &copy; 2025 Abhi Rajodiya. All rights reserved.
  </footer>

  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init({
      duration: 1000,
      once: true
    });

    // Active navigation on scroll
    const sections = document.querySelectorAll("section[id]");
    const navLinks = document.querySelectorAll('nav a');
    window.addEventListener("scroll", () => {
      let scrollY = window.scrollY + 150;
      sections.forEach(sec => {
        if (scrollY > sec.offsetTop && scrollY < sec.offsetTop + sec.offsetHeight) {
          navLinks.forEach(link => link.classList.remove('active'));
          const active = document.querySelector('nav a[href="#' + sec.id + '"]');
          if(active) active.classList.add('active');
        }
      });
    });
  </script>
</body>
</html>
