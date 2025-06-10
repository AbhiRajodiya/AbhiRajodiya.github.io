<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Abhi Rajodiya | Portfolio</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet" />
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: #f5f7fa;
      color: #333;
    }
    header {
      background: #1f2937;
      color: #fff;
      padding: 1rem 3rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    header h1 {
      font-weight: 700;
    }
    nav a {
      color: #fff;
      margin-left: 2rem;
      text-decoration: none;
      font-weight: 500;
    }
    section {
      padding: 5rem 3rem;
    }
    .hero {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 90vh;
      text-align: center;
    }
    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.2rem;
      color: #555;
    }

    .about, .skills, .portfolio, .contact {
      max-width: 1000px;
      margin: auto;
    }
    .section-title {
      text-align: center;
      font-size: 2rem;
      margin-bottom: 2rem;
      color: #1f2937;
    }

    .skills-bar {
      background: #e5e7eb;
      border-radius: 20px;
      overflow: hidden;
      margin: 1rem 0;
    }
    .skills-bar span {
      display: block;
      padding: 0.5rem;
      color: white;
      background: #3b82f6;
      animation: fillBar 2s ease-in-out forwards;
    }
    @keyframes fillBar {
      from {
        width: 0%;
      }
    }

    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }
    .portfolio-grid div {
      background: #fff;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
      padding: 1rem;
      border-radius: 10px;
      transition: transform 0.3s;
    }
    .portfolio-grid div:hover {
      transform: translateY(-5px);
    }

    form {
      display: flex;
      flex-direction: column;
    }
    input, textarea {
      padding: 1rem;
      margin-bottom: 1rem;
      border: 1px solid #d1d5db;
      border-radius: 8px;
      font-size: 1rem;
    }
    button {
      padding: 1rem;
      background: #2563eb;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1rem;
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
    <h1>Abhi Rajodiya</h1>
    <nav>
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#portfolio">Portfolio</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero" data-aos="fade-up">
    <h2>Hello, I'm Abhi 👋</h2>
    <p>.NET Developer | Azure Enthusiast | LogIngestor Creator</p>
  </section>

  <section id="about" class="about" data-aos="fade-right">
    <h2 class="section-title">About Me</h2>
    <p>I am a passionate software developer specializing in ASP.NET Core, SignalR, and real-time monitoring systems. I build scalable, secure, and modern web applications.</p>
  </section>

  <section id="skills" class="skills" data-aos="fade-left">
    <h2 class="section-title">Skills</h2>
    <div>
      <label>.NET Core</label>
      <div class="skills-bar"><span style="width: 90%">90%</span></div>
      <label>SignalR</label>
      <div class="skills-bar"><span style="width: 85%">85%</span></div>
      <label>Azure</label>
      <div class="skills-bar"><span style="width: 75%">75%</span></div>
      <label>JavaScript & Angular</label>
      <div class="skills-bar"><span style="width: 70%">70%</span></div>
    </div>
  </section>

  <section id="portfolio" class="portfolio" data-aos="zoom-in">
    <h2 class="section-title">Projects</h2>
    <div class="portfolio-grid">
      <div>
        <h4>LogIngestor</h4>
        <p>Real-time log monitoring system using SignalR, Chart.js, and .NET APIs.</p>
      </div>
      <div>
        <h4>Azure Blob Storage Uploader</h4>
        <p>ASP.NET Core app for uploading and viewing files stored in Azure Blob Storage.</p>
      </div>
      <div>
        <h4>Remote Script Execution</h4>
        <p>Custom .NET tool for running batch files across multiple devices remotely.</p>
      </div>
    </div>
  </section>

  <section id="contact" class="contact" data-aos="fade-up">
    <h2 class="section-title">Contact Me</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    &copy; 2025 Abhi Rajodiya. All rights reserved.
  </footer>

  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init({
      duration: 1000,
      once: true,
    });
  </script>
</body>
</html>
