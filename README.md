<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Abhi Rajodiya | .NET Developer</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet" />
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: #f3f4f6;
      color: #1f2937;
    }
    header {
      background: #1f2937;
      color: white;
      padding: 1.5rem 3rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    nav a {
      color: white;
      margin-left: 2rem;
      text-decoration: none;
      font-weight: 500;
    }
    section {
      padding: 4rem 3rem;
      max-width: 1000px;
      margin: auto;
    }
    h2.section-title {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 2rem;
      color: #2563eb;
    }
    .intro {
      text-align: center;
    }
    .intro h1 {
      font-size: 2.5rem;
    }
    .skills-grid, .exp-grid, .project-grid, .edu-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }
    .card {
      background: white;
      padding: 1.5rem;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }
    .card:hover {
      transform: translateY(-5px);
    }
    .contact {
      text-align: center;
    }
    .contact a {
      display: inline-block;
      margin: 0.5rem 1rem;
      color: #1f2937;
      text-decoration: none;
      font-size: 1.2rem;
    }
    footer {
      text-align: center;
      padding: 2rem;
      background: #1f2937;
      color: white;
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
    <p>A passionate .NET Developer with experience in full-stack web development and real-time applications.</p>
  </section>

  <section id="profile" data-aos="fade-right">
    <h2 class="section-title">Profile</h2>
    <p>I am a dedicated .NET Developer specializing in building and maintaining web applications using ASP.NET Core MVC and SQL Server. Skilled in efficient coding, debugging, and effective database management.</p>
  </section>

  <section id="skills" data-aos="fade-left">
    <h2 class="section-title">Skills</h2>
    <div class="skills-grid">
      <div class="card">C#</div>
      <div class="card">ASP.NET Core MVC</div>
      <div class="card">SQL Server</div>
      <div class="card">REST API</div>
      <div class="card">JavaScript</div>
      <div class="card">JQuery</div>
      <div class="card">HTML5 & CSS3</div>
      <div class="card">Python</div>
    </div>
  </section>

  <section id="experience" data-aos="zoom-in-up">
    <h2 class="section-title">Experience</h2>
    <div class="exp-grid">
      <div class="card">
        <h4>Rushkar Technology</h4>
        <p><em>.NET Developer Trainee</em> | Sep 2024 – Nov 2024</p>
        <p>Worked on ASP.NET Core, database integration, debugging, and collaborated on building enterprise-grade web apps.</p>
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
        <p>ASP.NET MVC app with user authentication, goal tracking, and data visualization via Chart.js/D3.js.</p>
      </div>
      <div class="card">
        <h4>Hospital Admin System</h4>
        <p>ASP.NET MVC-based system with patient registration, appointment scheduling, medical record handling using EF.</p>
      </div>
      <div class="card">
        <h4>Weather Application</h4>
        <p>Weather API integration with OpenWeatherMap using async calls, responsive UI with Bootstrap.</p>
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
    <p><i class="fas fa-envelope"></i> <a href="mailto:abhipatel1646@gmail.com">abhipatel1646@gmail.com</a></p>
    <p><i class="fas fa-phone"></i> <a href="tel:8401804226">+91 8401804226</a></p>
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
  </script>
</body>
</html>
