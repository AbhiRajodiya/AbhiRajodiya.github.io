<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Abhi Rajodiya — .NET Full Stack Developer</title>
  <meta name="description"
    content="Abhi Rajodiya — .NET Full Stack Developer crafting enterprise-grade web applications with ASP.NET Core, Angular, and Microsoft Azure." />
  <meta name="theme-color" content="#0a0a0f" />
  <!-- FAVICON — AR gradient monogram matching dark luxe theme -->
  <link rel="icon" type="image/png" sizes="512x512" href="favicon.png" />
  <link rel="icon" type="image/png" sizes="32x32" href="favicon.png" />
  <link rel="icon" type="image/png" sizes="16x16" href="favicon.png" />
  <link rel="apple-touch-icon" sizes="180x180" href="favicon.png" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Space+Grotesk:wght@400;500;600;700&display=swap"
    rel="stylesheet" />
  <style>
    /* ═══════════════════════════════════════════════════
   DESIGN SYSTEM — Dark Luxe Theme
   ═══════════════════════════════════════════════════ */
    :root {
      --bg-primary: #0a0a0f;
      --bg-secondary: #111118;
      --bg-card: rgba(255, 255, 255, 0.03);
      --bg-glass: rgba(255, 255, 255, 0.05);
      --border: rgba(255, 255, 255, 0.06);
      --border-hover: rgba(255, 255, 255, 0.12);
      --text-primary: #f0f0f5;
      --text-secondary: #8888a0;
      --text-muted: #55556a;
      --accent: #6c5ce7;
      --accent-glow: rgba(108, 92, 231, 0.35);
      --accent2: #00cec9;
      --accent2-glow: rgba(0, 206, 201, 0.3);
      --gradient-1: linear-gradient(135deg, #6c5ce7, #a29bfe);
      --gradient-2: linear-gradient(135deg, #00cec9, #81ecec);
      --gradient-3: linear-gradient(135deg, #fd79a8, #e84393);
      --gradient-hero: linear-gradient(135deg, #6c5ce7 0%, #00cec9 50%, #fd79a8 100%);
      --font-display: 'Space Grotesk', sans-serif;
      --font-body: 'Inter', sans-serif;
      --radius-sm: 8px;
      --radius-md: 16px;
      --radius-lg: 24px;
      --radius-xl: 32px;
    }

    *,
    *::before,
    *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: var(--font-body);
      background: var(--bg-primary);
      color: var(--text-primary);
      overflow-x: hidden;
      line-height: 1.6;
    }

    ::selection {
      background: var(--accent);
      color: #fff;
    }

    /* ── PARTICLE CANVAS ── */
    #particles-canvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
    }

    /* ── AMBIENT GLOW ORBS ── */
    .glow-orb {
      position: fixed;
      border-radius: 50%;
      filter: blur(120px);
      pointer-events: none;
      z-index: 0;
      opacity: 0.4;
    }

    .glow-orb-1 {
      width: 600px;
      height: 600px;
      background: var(--accent);
      top: -200px;
      left: -200px;
      animation: orbFloat1 18s ease-in-out infinite;
    }

    .glow-orb-2 {
      width: 500px;
      height: 500px;
      background: var(--accent2);
      bottom: -150px;
      right: -150px;
      animation: orbFloat2 22s ease-in-out infinite;
    }

    .glow-orb-3 {
      width: 400px;
      height: 400px;
      background: #fd79a8;
      top: 50%;
      left: 60%;
      animation: orbFloat3 15s ease-in-out infinite;
      opacity: 0.2;
    }

    @keyframes orbFloat1 {

      0%,
      100% {
        transform: translate(0, 0);
      }

      33% {
        transform: translate(80px, 120px);
      }

      66% {
        transform: translate(-40px, 60px);
      }
    }

    @keyframes orbFloat2 {

      0%,
      100% {
        transform: translate(0, 0);
      }

      33% {
        transform: translate(-100px, -80px);
      }

      66% {
        transform: translate(60px, -120px);
      }
    }

    @keyframes orbFloat3 {

      0%,
      100% {
        transform: translate(0, 0);
      }

      50% {
        transform: translate(-120px, 80px);
      }
    }

    /* ── NAVIGATION ── */
    nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 3rem;
      background: rgba(10, 10, 15, 0.6);
      backdrop-filter: blur(20px) saturate(180%);
      -webkit-backdrop-filter: blur(20px) saturate(180%);
      border-bottom: 1px solid var(--border);
      transition: all 0.4s cubic-bezier(0.22, 1, 0.36, 1);
    }

    nav.scrolled {
      padding: 0.7rem 3rem;
      background: rgba(10, 10, 15, 0.85);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
    }

    .nav-logo {
      font-family: var(--font-display);
      font-weight: 700;
      font-size: 1.5rem;
      color: var(--text-primary);
      text-decoration: none;
      position: relative;
    }

    .nav-logo span {
      background: var(--gradient-hero);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .nav-links {
      display: flex;
      gap: 0.5rem;
      list-style: none;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--text-secondary);
      font-size: 0.88rem;
      font-weight: 500;
      padding: 0.5rem 1rem;
      border-radius: var(--radius-sm);
      transition: all 0.3s;
      position: relative;
    }

    .nav-links a:hover {
      color: var(--text-primary);
      background: var(--bg-glass);
    }

    .nav-links a.active {
      color: var(--accent);
      background: rgba(108, 92, 231, 0.1);
    }

    /* ── HAMBURGER ── */
    .ham {
      display: none;
      flex-direction: column;
      gap: 5px;
      cursor: pointer;
      padding: 8px;
      border-radius: var(--radius-sm);
      transition: background 0.3s;
    }

    .ham:hover {
      background: var(--bg-glass);
    }

    .ham span {
      width: 22px;
      height: 2px;
      background: var(--text-primary);
      border-radius: 2px;
      transition: all 0.3s;
      display: block;
    }

    /* ── MOBILE NAV ── */
    .mobile-nav {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(10, 10, 15, 0.95);
      backdrop-filter: blur(30px);
      z-index: 999;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 1.5rem;
    }

    .mobile-nav.open {
      display: flex;
    }

    .mobile-nav a {
      text-decoration: none;
      color: var(--text-primary);
      font-family: var(--font-display);
      font-size: 1.8rem;
      font-weight: 600;
      transition: color 0.3s;
    }

    .mobile-nav a:hover {
      color: var(--accent);
    }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 5rem 3rem 3rem;
      position: relative;
      overflow: hidden;
    }

    .hero-grid-bg {
      position: absolute;
      inset: 0;
      background-image:
        linear-gradient(rgba(108, 92, 231, 0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(108, 92, 231, 0.03) 1px, transparent 1px);
      background-size: 60px 60px;
      mask-image: radial-gradient(ellipse 70% 60% at 50% 40%, black 30%, transparent 100%);
      -webkit-mask-image: radial-gradient(ellipse 70% 60% at 50% 40%, black 30%, transparent 100%);
    }

    .hero-inner {
      position: relative;
      z-index: 2;
      max-width: 900px;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      background: var(--bg-glass);
      border: 1px solid var(--border);
      color: var(--text-secondary);
      padding: 0.45rem 1.2rem;
      border-radius: 100px;
      font-size: 0.8rem;
      font-weight: 500;
      letter-spacing: 0.5px;
      margin-bottom: 2rem;
      backdrop-filter: blur(10px);
      animation: fadeSlideUp 0.8s cubic-bezier(0.22, 1, 0.36, 1) both;
    }

    .hero-badge .pulse-dot {
      width: 8px;
      height: 8px;
      background: #00b894;
      border-radius: 50%;
      position: relative;
    }

    .hero-badge .pulse-dot::after {
      content: '';
      position: absolute;
      inset: -3px;
      border-radius: 50%;
      border: 1px solid #00b894;
      animation: pulseRing 2s ease-out infinite;
    }

    @keyframes pulseRing {
      0% {
        transform: scale(1);
        opacity: 0.8;
      }

      100% {
        transform: scale(2.2);
        opacity: 0;
      }
    }

    .hero h1 {
      font-family: var(--font-display);
      font-weight: 700;
      font-size: clamp(3.5rem, 8vw, 7rem);
      line-height: 1.05;
      letter-spacing: -3px;
      animation: fadeSlideUp 0.8s 0.1s cubic-bezier(0.22, 1, 0.36, 1) both;
    }

    .hero h1 .gradient-text {
      background: var(--gradient-hero);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      background-size: 200% 200%;
      animation: gradientShift 6s ease infinite;
    }

    @keyframes gradientShift {

      0%,
      100% {
        background-position: 0% 50%;
      }

      50% {
        background-position: 100% 50%;
      }
    }

    .hero-sub {
      margin-top: 1.8rem;
      font-size: 1.15rem;
      color: var(--text-secondary);
      font-weight: 300;
      max-width: 560px;
      line-height: 1.8;
      animation: fadeSlideUp 0.8s 0.2s cubic-bezier(0.22, 1, 0.36, 1) both;
    }

    .hero-actions {
      margin-top: 2.5rem;
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      animation: fadeSlideUp 0.8s 0.3s cubic-bezier(0.22, 1, 0.36, 1) both;
    }

    /* ── BUTTONS ── */
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.85rem 2rem;
      border-radius: 100px;
      font-size: 0.92rem;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.35s cubic-bezier(0.22, 1, 0.36, 1);
      cursor: pointer;
      border: none;
      font-family: var(--font-body);
      position: relative;
      overflow: hidden;
    }

    .btn::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: inherit;
      opacity: 0;
      transition: opacity 0.35s;
    }

    .btn-primary {
      background: var(--gradient-1);
      color: #fff;
      box-shadow: 0 4px 20px var(--accent-glow);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 40px var(--accent-glow);
    }

    .btn-outline {
      background: transparent;
      color: var(--text-primary);
      border: 1.5px solid var(--border-hover);
    }

    .btn-outline:hover {
      background: var(--bg-glass);
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-3px);
    }

    /* ── HERO STATS ── */
    .hero-stats {
      margin-top: 3.5rem;
      display: flex;
      gap: 3rem;
      animation: fadeSlideUp 0.8s 0.4s cubic-bezier(0.22, 1, 0.36, 1) both;
    }

    .stat-num {
      font-family: var(--font-display);
      font-size: 2.5rem;
      font-weight: 700;
      line-height: 1;
      background: var(--gradient-1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .stat-label {
      font-size: 0.82rem;
      color: var(--text-muted);
      letter-spacing: 0.5px;
      margin-top: 0.3rem;
    }

    /* ── SCROLL INDICATOR ── */
    .scroll-hint {
      position: absolute;
      bottom: 2.5rem;
      right: 3rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.5rem;
      color: var(--text-muted);
      font-size: 0.7rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      animation: fadeSlideUp 1s 0.8s both;
    }

    .scroll-line {
      width: 1px;
      height: 60px;
      background: linear-gradient(to bottom, var(--accent), transparent);
      animation: scrollPulse 2s ease-in-out infinite;
    }

    @keyframes scrollPulse {

      0%,
      100% {
        opacity: 1;
        transform: scaleY(1);
      }

      50% {
        opacity: 0.3;
        transform: scaleY(0.5);
      }
    }

    /* ── SECTIONS ── */
    .section-wrapper {
      padding: 6rem 3rem;
      max-width: 1200px;
      margin: 0 auto;
      position: relative;
      z-index: 2;
    }

    .section-header {
      display: flex;
      align-items: center;
      gap: 1rem;
      margin-bottom: 3.5rem;
    }

    .section-num {
      font-family: var(--font-display);
      font-size: 0.8rem;
      font-weight: 600;
      background: var(--gradient-1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: 2px;
    }

    .section-title {
      font-family: var(--font-display);
      font-weight: 700;
      font-size: clamp(2rem, 4vw, 3rem);
      letter-spacing: -1.5px;
    }

    .section-line {
      flex: 1;
      height: 1px;
      background: linear-gradient(90deg, var(--border-hover), transparent);
    }

    /* ── SKILLS ── */
    .skills-section {
      background: var(--bg-secondary);
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      padding: 4rem;
      margin: 0 2rem;
      position: relative;
      overflow: hidden;
      z-index: 2;
    }

    .skills-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 200px;
      height: 1px;
      background: var(--gradient-1);
    }

    .skills-clusters {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.2rem;
    }

    .skill-cluster {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 1.8rem;
      transition: all 0.4s cubic-bezier(0.22, 1, 0.36, 1);
      position: relative;
      overflow: hidden;
    }

    .skill-cluster::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: inherit;
      background: radial-gradient(circle at 50% 0%, rgba(108, 92, 231, 0.08), transparent 70%);
      opacity: 0;
      transition: opacity 0.4s;
    }

    .skill-cluster:hover {
      border-color: var(--border-hover);
      transform: translateY(-4px);
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
    }

    .skill-cluster:hover::before {
      opacity: 1;
    }

    .skill-icon {
      width: 48px;
      height: 48px;
      border-radius: var(--radius-md);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.4rem;
      margin-bottom: 1.2rem;
    }

    .skill-cluster h4 {
      font-family: var(--font-display);
      font-size: 0.78rem;
      font-weight: 600;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--text-muted);
      margin-bottom: 1rem;
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.45rem;
    }

    .skill-tag {
      background: rgba(108, 92, 231, 0.1);
      color: var(--text-secondary);
      padding: 0.35rem 0.85rem;
      border-radius: 100px;
      font-size: 0.8rem;
      font-weight: 500;
      border: 1px solid rgba(108, 92, 231, 0.15);
      transition: all 0.3s;
    }

    .skill-tag:hover {
      background: rgba(108, 92, 231, 0.2);
      color: var(--text-primary);
      border-color: var(--accent);
      transform: translateY(-1px);
    }

    /* ── DIVIDER ── */
    .divider {
      border: none;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--border-hover), transparent);
      margin: 0 3rem;
    }

    /* ── EXPERIENCE ── */
    .exp-timeline {
      position: relative;
    }

    .exp-timeline::before {
      content: '';
      position: absolute;
      left: 0;
      top: 0;
      bottom: 0;
      width: 1px;
      background: linear-gradient(to bottom, var(--accent), var(--accent2), transparent);
    }

    .exp-item {
      padding-left: 2.5rem;
      padding-bottom: 3.5rem;
      position: relative;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .exp-item.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .exp-item::before {
      content: '';
      position: absolute;
      left: -5px;
      top: 6px;
      width: 11px;
      height: 11px;
      border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 0 3px var(--bg-primary), 0 0 0 5px var(--accent), 0 0 20px var(--accent-glow);
    }

    .exp-date {
      font-size: 0.78rem;
      font-weight: 600;
      background: var(--gradient-1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      margin-bottom: 0.5rem;
    }

    .exp-role {
      font-family: var(--font-display);
      font-size: 1.4rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      margin-bottom: 0.3rem;
    }

    .exp-company {
      font-size: 0.92rem;
      color: var(--text-muted);
      margin-bottom: 1.2rem;
    }

    .exp-company strong {
      color: var(--text-secondary);
      font-weight: 600;
    }

    .exp-bullets {
      list-style: none;
    }

    .exp-bullets li {
      position: relative;
      padding-left: 1.5rem;
      margin-bottom: 0.65rem;
      font-size: 0.92rem;
      color: var(--text-secondary);
      line-height: 1.7;
    }

    .exp-bullets li::before {
      content: '→';
      position: absolute;
      left: 0;
      color: var(--accent);
      font-weight: 600;
    }

    /* ── PROJECTS ── */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
      gap: 1.5rem;
    }

    .project-card {
      background: var(--bg-card);
      border-radius: var(--radius-lg);
      padding: 2rem;
      border: 1px solid var(--border);
      position: relative;
      overflow: hidden;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .project-card.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .project-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 2px;
    }

    .project-card:nth-child(1)::before {
      background: var(--gradient-1);
    }

    .project-card:nth-child(2)::before {
      background: var(--gradient-2);
    }

    .project-card::after {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: inherit;
      background: radial-gradient(circle at 50% 0%, rgba(108, 92, 231, 0.06), transparent 60%);
      opacity: 0;
      transition: opacity 0.4s;
    }

    .project-card:hover {
      border-color: var(--border-hover);
      transform: translateY(-6px);
      box-shadow: 0 25px 60px rgba(0, 0, 0, 0.4);
    }

    .project-card:hover::after {
      opacity: 1;
    }

    .project-num {
      font-family: var(--font-display);
      font-size: 3.2rem;
      font-weight: 700;
      background: linear-gradient(135deg, var(--border-hover), transparent);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      line-height: 1;
      margin-bottom: 0.5rem;
    }

    .project-name {
      font-family: var(--font-display);
      font-size: 1.25rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      margin-bottom: 0.8rem;
      position: relative;
      z-index: 1;
    }

    .project-desc {
      font-size: 0.9rem;
      color: var(--text-muted);
      line-height: 1.7;
      margin-bottom: 1.5rem;
      position: relative;
      z-index: 1;
    }

    .project-highlights {
      list-style: none;
      margin-bottom: 1.5rem;
      position: relative;
      z-index: 1;
    }

    .project-highlights li {
      font-size: 0.88rem;
      color: var(--text-secondary);
      padding: 0.45rem 0;
      border-bottom: 1px solid var(--border);
      display: flex;
      align-items: flex-start;
      gap: 0.6rem;
      line-height: 1.55;
    }

    .project-highlights li::before {
      content: '◆';
      color: var(--accent);
      font-size: 0.45rem;
      margin-top: 0.5rem;
      flex-shrink: 0;
    }

    .project-tech {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      position: relative;
      z-index: 1;
    }

    .tech-tag {
      background: var(--bg-glass);
      color: var(--text-secondary);
      padding: 0.3rem 0.75rem;
      border-radius: 100px;
      font-size: 0.75rem;
      font-weight: 500;
      border: 1px solid var(--border);
      transition: all 0.3s;
    }

    .tech-tag:hover {
      border-color: var(--accent);
      color: var(--accent);
    }

    /* ── HIGHLIGHT STRIP ── */
    .highlight-strip {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 2.5rem;
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
      min-width: 220px;
    }

    .highlight-icon {
      width: 42px;
      height: 42px;
      border-radius: var(--radius-sm);
      background: rgba(108, 92, 231, 0.1);
      border: 1px solid rgba(108, 92, 231, 0.15);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.2rem;
      flex-shrink: 0;
    }

    .highlight-text {
      font-size: 0.85rem;
      color: var(--text-secondary);
      line-height: 1.6;
    }

    .highlight-text strong {
      display: block;
      font-weight: 600;
      margin-bottom: 0.2rem;
      font-family: var(--font-display);
      color: var(--text-primary);
    }

    /* ── EDUCATION ── */
    .edu-card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 2.5rem;
      display: flex;
      gap: 2rem;
      align-items: center;
      flex-wrap: wrap;
      transition: all 0.4s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .edu-card:hover {
      border-color: var(--border-hover);
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
    }

    .edu-badge {
      width: 80px;
      height: 80px;
      background: var(--gradient-1);
      border-radius: var(--radius-md);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2rem;
      flex-shrink: 0;
      box-shadow: 0 8px 30px var(--accent-glow);
    }

    .edu-info {
      flex: 1;
    }

    .edu-degree {
      font-family: var(--font-display);
      font-size: 1.35rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      margin-bottom: 0.3rem;
    }

    .edu-school {
      color: var(--text-muted);
      font-size: 0.92rem;
      margin-bottom: 0.6rem;
    }

    .edu-meta {
      display: flex;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .edu-meta-item {
      font-size: 0.85rem;
      color: var(--text-secondary);
      font-weight: 500;
    }

    .edu-meta-item span {
      color: var(--text-muted);
      font-weight: 400;
    }

    .edu-cgpa {
      font-family: var(--font-display);
      font-size: 2.5rem;
      font-weight: 700;
      background: var(--gradient-1);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-align: right;
    }

    .edu-cgpa-label {
      font-size: 0.72rem;
      color: var(--text-muted);
      letter-spacing: 1.5px;
      text-transform: uppercase;
      text-align: right;
    }

    /* ── CONTACT ── */
    .contact-section {
      background: var(--bg-secondary);
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      margin: 0 2rem 4rem;
      padding: 5rem 4rem;
      text-align: center;
      position: relative;
      overflow: hidden;
      z-index: 2;
    }

    .contact-section::before {
      content: '';
      position: absolute;
      width: 500px;
      height: 500px;
      background: radial-gradient(circle, rgba(108, 92, 231, 0.15), transparent 70%);
      top: -200px;
      right: -100px;
      pointer-events: none;
    }

    .contact-section::after {
      content: '';
      position: absolute;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(0, 206, 201, 0.1), transparent 70%);
      bottom: -200px;
      left: -100px;
      pointer-events: none;
    }

    .contact-section h2 {
      font-family: var(--font-display);
      font-size: clamp(2.5rem, 5vw, 4.5rem);
      font-weight: 700;
      letter-spacing: -2px;
      margin-bottom: 1rem;
      position: relative;
      z-index: 1;
    }

    .contact-section h2 .gradient-text {
      background: var(--gradient-hero);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .contact-section p {
      color: var(--text-muted);
      font-size: 1.1rem;
      margin-bottom: 2.5rem;
      position: relative;
      z-index: 1;
    }

    .contact-links {
      display: flex;
      gap: 0.8rem;
      justify-content: center;
      flex-wrap: wrap;
      position: relative;
      z-index: 1;
    }

    .contact-link {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.8rem 1.6rem;
      border-radius: 100px;
      font-size: 0.88rem;
      font-weight: 500;
      text-decoration: none;
      transition: all 0.35s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .contact-link-primary {
      background: var(--gradient-1);
      color: #fff;
      box-shadow: 0 4px 20px var(--accent-glow);
    }

    .contact-link-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 40px var(--accent-glow);
    }

    .contact-link-outline {
      background: transparent;
      color: var(--text-secondary);
      border: 1.5px solid var(--border-hover);
    }

    .contact-link-outline:hover {
      background: var(--bg-glass);
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-3px);
    }

    /* ── FOOTER ── */
    footer {
      text-align: center;
      padding: 2rem;
      color: var(--text-muted);
      font-size: 0.82rem;
      letter-spacing: 0.5px;
      position: relative;
      z-index: 2;
    }

    /* ── ANIMATIONS ── */
    @keyframes fadeSlideUp {
      from {
        opacity: 0;
        transform: translateY(40px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* ── REVEAL ON SCROLL ── */
    .reveal {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.7s cubic-bezier(0.22, 1, 0.36, 1);
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      nav {
        padding: 0.8rem 1.5rem;
      }

      nav.scrolled {
        padding: 0.6rem 1.5rem;
      }

      .nav-links {
        display: none;
      }

      .ham {
        display: flex;
      }

      .hero {
        padding: 6rem 1.5rem 3rem;
      }

      .hero h1 {
        letter-spacing: -1.5px;
      }

      .hero-stats {
        gap: 2rem;
        flex-wrap: wrap;
      }

      .section-wrapper {
        padding: 4rem 1.5rem;
      }

      .skills-section {
        margin: 0 1rem;
        padding: 2.5rem 1.5rem;
      }

      .skills-clusters {
        grid-template-columns: 1fr;
      }

      .projects-grid {
        grid-template-columns: 1fr;
      }

      .contact-section {
        margin: 0 1rem 2rem;
        padding: 3rem 1.5rem;
      }

      .divider {
        margin: 0 1.5rem;
      }

      .edu-card {
        flex-direction: column;
        align-items: flex-start;
      }

      .edu-cgpa,
      .edu-cgpa-label {
        text-align: left;
      }

      .scroll-hint {
        display: none;
      }

      .highlight-strip {
        flex-direction: column;
      }
    }
    /* ===== CAT ASSISTANT ===== */

#catAssistant {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 99999;
  cursor: pointer;
  user-select: none;
}

#catEmoji {
  font-size: 70px;
  animation: catBounce 2s infinite ease-in-out;
  filter: drop-shadow(0 0 15px rgba(255,255,255,0.2));
}

#catBubble {
  position: absolute;
  bottom: 90px;
  right: 0;
  width: 260px;
  background: rgba(17,17,24,.95);
  color: white;
  border: 1px solid rgba(255,255,255,.1);
  border-radius: 16px;
  padding: 12px;
  font-size: 14px;
  display: none;
  backdrop-filter: blur(20px);
  box-shadow: 0 10px 30px rgba(0,0,0,.4);
}

#catBubble.show {
  display: block;
  animation: catPop .3s ease;
}

@keyframes catBounce {
  0%,100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes catPop {
  from {
    opacity: 0;
    transform: translateY(15px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
  </style>
</head>

<body>

  <!-- AMBIENT GLOW ORBS -->
  <div class="glow-orb glow-orb-1"></div>
  <div class="glow-orb glow-orb-2"></div>
  <div class="glow-orb glow-orb-3"></div>

  <!-- PARTICLE CANVAS -->
  <canvas id="particles-canvas"></canvas>

  <!-- MOBILE NAV OVERLAY -->
  <div class="mobile-nav" id="mobileNav">
    <a href="#about" onclick="closeMobileNav()">About</a>
    <a href="#skills" onclick="closeMobileNav()">Skills</a>
    <a href="#experience" onclick="closeMobileNav()">Experience</a>
    <a href="#projects" onclick="closeMobileNav()">Projects</a>
    <a href="#contact" onclick="closeMobileNav()">Contact</a>
  </div>

  <!-- NAV -->
  <nav id="mainNav">
    <a href="#" class="nav-logo">A<span>R</span></a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="ham" id="hamBtn" onclick="toggleMobileNav()">
      <span></span><span></span><span></span>
    </div>
  </nav>

  <!-- HERO -->
  <section class="hero" id="about">
    <div class="hero-grid-bg"></div>
    <div class="hero-inner">
      <div class="hero-badge"><span class="pulse-dot"></span> Available for opportunities</div>
      <h1>Abhi<br /><span class="gradient-text">Rajodiya</span></h1>
      <p class="hero-sub">.NET Full Stack Developer crafting enterprise-grade web applications with ASP.NET Core,
        Angular, and Microsoft Azure. Based in Ahmedabad, India.</p>
      <div class="hero-actions">
        <a href="mailto:abhipatel1646@gmail.com" class="btn btn-primary">✉ Get in Touch</a>
        <a href="https://github.com/AbhiRajodiya" target="_blank" class="btn btn-outline">↗ GitHub</a>
      </div>
      <div class="hero-stats">
        <div class="stat">
          <div class="stat-num">1.5+</div>
          <div class="stat-label">Years Experience</div>
        </div>
        <div class="stat">
          <div class="stat-num">2+</div>
          <div class="stat-label">Key Projects</div>
        </div>
        <div class="stat">
          <div class="stat-num">8.67</div>
          <div class="stat-label">CGPA / 10.0</div>
        </div>
      </div>
    </div>
    <div class="scroll-hint">
      <div class="scroll-line"></div><span>Scroll</span>
    </div>
  </section>

  <hr class="divider" />

  <!-- SKILLS -->
  <div class="skills-section" id="skills">
    <div class="section-header">
      <span class="section-num">01</span>
      <h2 class="section-title">Technical Skills</h2>
      <div class="section-line"></div>
    </div>
    <div class="skills-clusters">
      <div class="skill-cluster reveal">
        <div class="skill-icon" style="background:rgba(108,92,231,0.15);">⚙️</div>
        <h4>Backend</h4>
        <div class="skill-tags"><span class="skill-tag">ASP.NET Core MVC</span><span class="skill-tag">Web
            API</span><span class="skill-tag">C#</span><span class="skill-tag">Entity Framework Core</span><span
            class="skill-tag">Dapper</span><span class="skill-tag">SignalR</span><span
            class="skill-tag">Async/Await</span></div>
      </div>
      <div class="skill-cluster reveal">
        <div class="skill-icon" style="background:rgba(253,121,168,0.15);">🎨</div>
        <h4>Frontend</h4>
        <div class="skill-tags"><span class="skill-tag">Angular</span><span class="skill-tag">TypeScript</span><span
            class="skill-tag">JavaScript</span><span class="skill-tag">HTML5</span><span class="skill-tag">CSS3</span>
        </div>
      </div>
      <div class="skill-cluster reveal">
        <div class="skill-icon" style="background:rgba(0,206,201,0.15);">☁️</div>
        <h4>Cloud & DevOps</h4>
        <div class="skill-tags"><span class="skill-tag">Microsoft Azure</span><span class="skill-tag">Azure
            DevOps</span><span class="skill-tag">GitHub Actions</span><span class="skill-tag">CI/CD
            Pipelines</span><span class="skill-tag">Blob Storage</span><span class="skill-tag">Azure Functions</span>
        </div>
      </div>
      <div class="skill-cluster reveal">
        <div class="skill-icon" style="background:rgba(245,158,11,0.15);">🗄️</div>
        <h4>Database</h4>
        <div class="skill-tags"><span class="skill-tag">MS SQL Server</span><span class="skill-tag">Database
            Design</span><span class="skill-tag">Optimization</span><span class="skill-tag">Stored Procedures</span>
        </div>
      </div>
      <div class="skill-cluster reveal">
        <div class="skill-icon" style="background:rgba(162,155,254,0.15);">🏗️</div>
        <h4>Architecture</h4>
        <div class="skill-tags"><span class="skill-tag">Clean Architecture</span><span class="skill-tag">SOLID
            Principles</span><span class="skill-tag">Repository Pattern</span><span class="skill-tag">Dependency
            Injection</span><span class="skill-tag">Microservices</span><span class="skill-tag">MVC</span></div>
      </div>
      <div class="skill-cluster reveal">
        <div class="skill-icon" style="background:rgba(232,67,147,0.15);">🛠️</div>
        <h4>Tools & Practices</h4>
        <div class="skill-tags"><span class="skill-tag">Visual Studio</span><span class="skill-tag">Git /
            GitHub</span><span class="skill-tag">Postman</span><span class="skill-tag">Swagger</span><span
            class="skill-tag">Agile / Scrum</span><span class="skill-tag">JIRA</span></div>
      </div>
    </div>
  </div>

  <!-- EXPERIENCE -->
  <section class="section-wrapper" id="experience">
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
          <li>Built real-time communication features using SignalR, enabling live device monitoring dashboards with
            sub-second data refresh rates.</li>
          <li>Automated build and deployment workflows using Azure DevOps CI/CD pipelines and GitHub Actions, reducing
            manual deployment errors significantly.</li>
          <li>Deployed and managed cloud-hosted applications on Microsoft Azure — Web Apps, Blob Storage, Azure
            Functions — gaining hands-on cloud engineering experience.</li>
          <li>Collaborated cross-functionally with senior engineers and product teams in Agile sprints, consistently
            delivering features on schedule.</li>
          <li>Participated in code reviews and contributed to establishing best practices for API design, error
            handling, and logging standards.</li>
        </ul>
      </div>
      <div class="exp-item">
        <div class="exp-date">Oct 2022 — Mar 2023</div>
        <div class="exp-role">Full Stack Web Developer Intern</div>
        <div class="exp-company"><strong>Felix IT Systems</strong> · Ahmedabad, India</div>
        <ul class="exp-bullets">
          <li>Developed RESTful APIs in ASP.NET Core and consumed them via Angular front-end components, ensuring
            seamless data flow and responsive UI.</li>
          <li>Designed and implemented relational database schemas in SQL Server; wrote optimized stored procedures and
            queries for business-critical modules.</li>
          <li>Led full-stack development of an enterprise calibration management platform (Angular + .NET Core) for a
            US-based client (Antylia Scientific).</li>
          <li>Optimized MS SQL Server schemas and queries via Entity Framework Core, achieving measurable reduction in
            API response times.</li>
        </ul>
      </div>
    </div>
  </section>

  <hr class="divider" />

  <!-- PROJECTS -->
  <section class="section-wrapper" id="projects">
    <div class="section-header">
      <span class="section-num">03</span>
      <h2 class="section-title">Key Projects</h2>
      <div class="section-line"></div>
    </div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-num">01</div>
        <div class="project-name">LogIngestor — Real-Time Device Monitoring</div>
        <p class="project-desc">A full-stack real-time monitoring platform tracking CPU, GPU, Memory, Disk, and Network
          metrics with sub-second live updates via SignalR WebSockets.</p>
        <ul class="project-highlights">
          <li>High-throughput log ingestion pipeline with Dapper ORM and optimized SQL Server queries for large-scale
            telemetry data.</li>
          <li>GPS tracking and remote script execution modules enabling centralized fleet management — adopted in
            production.</li>
          <li>Clean code principles and modular architecture for long-term maintainability and scalability.</li>
        </ul>
        <div class="project-tech"><span class="tech-tag">.NET Core</span><span class="tech-tag">SignalR</span><span
            class="tech-tag">SQL Server</span><span class="tech-tag">Dapper</span><span class="tech-tag">REST API</span>
        </div>
      </div>
      <div class="project-card">
        <div class="project-num">02</div>
        <div class="project-name">Calibration Traceable Live — Enterprise Platform</div>
        <p class="project-desc">End-to-end enterprise calibration management system for Antylia Scientific (US-based),
          replacing a legacy WPF desktop application with a modern web stack.</p>
        <ul class="project-highlights">
          <li>RESTful APIs for full calibration lifecycle: LOT/Serial Number generation, data entry, certificate
            generation, Azure Blob auto-upload.</li>
          <li>Angular front-end with real-time data grids supporting 500+ batch lot processing.</li>
          <li>Role-Based Access Control with 4 user tiers, IP whitelisting, and audit trail logging for regulatory
            compliance.</li>
          <li>Third-party hardware SDK integration and NiceLabel for automated Zebra barcode printing.</li>
        </ul>
        <div class="project-tech"><span class="tech-tag">.NET Core Web API</span><span
            class="tech-tag">Angular</span><span class="tech-tag">EF Core</span><span class="tech-tag">Azure
            Blob</span><span class="tech-tag">Hardware SDK</span></div>
      </div>
    </div>

    <div class="highlight-strip reveal">
      <div class="highlight-item">
        <div class="highlight-icon">🤖</div>
        <div class="highlight-text"><strong>AI-Assisted Dev</strong>Proficient with Cursor, GitHub Copilot, ChatGPT, and
          Claude for faster, cleaner code.</div>
      </div>
      <div class="highlight-item">
        <div class="highlight-icon">📡</div>
        <div class="highlight-text"><strong>IoT Integration</strong>Hands-on experience with hardware-software
          interfaces and real-time data systems.</div>
      </div>
      <div class="highlight-item">
        <div class="highlight-icon">📈</div>
        <div class="highlight-text"><strong>Always Upskilling</strong>Actively learning Docker, microservices
          architecture, and unit testing with xUnit/NUnit.</div>
      </div>
    </div>
  </section>

  <hr class="divider" />

  <!-- EDUCATION -->
  <section class="section-wrapper" id="education">
    <div class="section-header">
      <span class="section-num">04</span>
      <h2 class="section-title">Education</h2>
      <div class="section-line"></div>
    </div>
    <div class="edu-card reveal">
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
    <h2>Let's <span class="gradient-text">Build</span> Something</h2>
    <p>Open to full-time roles, collaborations, and interesting conversations.</p>
    <div class="contact-links">
      <a href="mailto:abhipatel1646@gmail.com" class="contact-link contact-link-primary">✉ abhipatel1646@gmail.com</a>
      <a href="tel:+918401804226" class="contact-link contact-link-outline">📞 +91 8401804226</a>
      <a href="https://linkedin.com/in/abhi-rajodiya" target="_blank" class="contact-link contact-link-outline">in
        LinkedIn</a>
      <a href="https://github.com/AbhiRajodiya" target="_blank" class="contact-link contact-link-outline">⌥ GitHub</a>
    </div>
  </div>

  <footer>© 2025 Abhi Rajodiya · Ahmedabad, Gujarat, India · Designed & Coded with purpose.</footer>

  <script>
    // ── PARTICLE SYSTEM ──
    const canvas = document.getElementById('particles-canvas');
    const ctx = canvas.getContext('2d');
    let particles = [];
    const PARTICLE_COUNT = 60;

    function resizeCanvas() {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    }
    resizeCanvas();
    window.addEventListener('resize', resizeCanvas);

    class Particle {
      constructor() { this.reset(); }
      reset() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * canvas.height;
        this.size = Math.random() * 1.5 + 0.5;
        this.speedX = (Math.random() - 0.5) * 0.3;
        this.speedY = (Math.random() - 0.5) * 0.3;
        this.opacity = Math.random() * 0.4 + 0.1;
      }
      update() {
        this.x += this.speedX;
        this.y += this.speedY;
        if (this.x < 0 || this.x > canvas.width) this.speedX *= -1;
        if (this.y < 0 || this.y > canvas.height) this.speedY *= -1;
      }
      draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fillStyle = `rgba(108, 92, 231, ${this.opacity})`;
        ctx.fill();
      }
    }

    for (let i = 0; i < PARTICLE_COUNT; i++) particles.push(new Particle());

    function connectParticles() {
      for (let i = 0; i < particles.length; i++) {
        for (let j = i + 1; j < particles.length; j++) {
          const dx = particles[i].x - particles[j].x;
          const dy = particles[i].y - particles[j].y;
          const dist = Math.sqrt(dx * dx + dy * dy);
          if (dist < 150) {
            ctx.beginPath();
            ctx.strokeStyle = `rgba(108, 92, 231, ${0.06 * (1 - dist / 150)})`;
            ctx.lineWidth = 0.5;
            ctx.moveTo(particles[i].x, particles[i].y);
            ctx.lineTo(particles[j].x, particles[j].y);
            ctx.stroke();
          }
        }
      }
    }

    function animateParticles() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      particles.forEach(p => { p.update(); p.draw(); });
      connectParticles();
      requestAnimationFrame(animateParticles);
    }
    animateParticles();

    // ── SCROLL ANIMATIONS ──
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
    }, { threshold: 0.1 });
    document.querySelectorAll('.exp-item, .project-card, .reveal').forEach(el => observer.observe(el));

    // Stagger delays
    document.querySelectorAll('.project-card').forEach((c, i) => { c.style.transitionDelay = `${i * 0.15}s`; });
    document.querySelectorAll('.exp-item').forEach((c, i) => { c.style.transitionDelay = `${i * 0.15}s`; });
    document.querySelectorAll('.skill-cluster.reveal').forEach((c, i) => { c.style.transitionDelay = `${i * 0.08}s`; });

    // ── NAV SCROLL EFFECT ──
    window.addEventListener('scroll', () => {
      document.getElementById('mainNav').classList.toggle('scrolled', window.scrollY > 50);
    });

    // ── ACTIVE NAV HIGHLIGHT ──
    const sections = document.querySelectorAll('section[id], div[id]');
    const navLinks = document.querySelectorAll('.nav-links a');
    window.addEventListener('scroll', () => {
      let current = '';
      sections.forEach(s => {
        const top = s.offsetTop - 120;
        if (window.scrollY >= top) current = s.getAttribute('id');
      });
      navLinks.forEach(a => {
        a.classList.remove('active');
        if (a.getAttribute('href') === '#' + current) a.classList.add('active');
      });
    });

    // ── MOBILE NAV ──
    function toggleMobileNav() {
      const nav = document.getElementById('mobileNav');
      const btn = document.getElementById('hamBtn');
      const spans = btn.querySelectorAll('span');
      const isOpen = nav.classList.contains('open');
      nav.classList.toggle('open');
      document.body.style.overflow = isOpen ? '' : 'hidden';
      spans[0].style.transform = isOpen ? '' : 'rotate(45deg) translate(5px, 5px)';
      spans[1].style.opacity = isOpen ? '1' : '0';
      spans[2].style.transform = isOpen ? '' : 'rotate(-45deg) translate(5px, -5px)';
    }
    function closeMobileNav() {
      const nav = document.getElementById('mobileNav');
      const btn = document.getElementById('hamBtn');
      const spans = btn.querySelectorAll('span');
      nav.classList.remove('open');
      document.body.style.overflow = '';
      spans[0].style.transform = '';
      spans[1].style.opacity = '1';
      spans[2].style.transform = '';
    }

    // ── SMOOTH REVEAL ON LOAD ──
    document.addEventListener('DOMContentLoaded', () => {
      document.body.style.opacity = '0';
      document.body.style.transition = 'opacity 0.5s';
      requestAnimationFrame(() => { document.body.style.opacity = '1'; });
    });
    /* ===== CAT ASSISTANT ===== */

const catMessages = [
  "🐱 Welcome to Abhi's portfolio!",
  "☕ Coffee level: Critical",
  "🚀 Currently deploying awesomeness",
  "💻 It works on my machine",
  "🔍 Searching Stack Overflow...",
  "⚡ Debugging reality",
  "🎯 Check out the Projects section",
  "📞 Hire this human",
  "🗄️ The database did nothing wrong",
  "😎 Nice choice visiting this website",
  "🏆 Achievement Unlocked: Curious Visitor",
  "👀 I am watching your scroll position"
];

const catAssistant = document.getElementById("catAssistant");
const catBubble = document.getElementById("catBubble");

function showCatMessage(message) {

    catBubble.innerHTML = message;
    catBubble.classList.add("show");

    clearTimeout(window.catHideTimer);

    window.catHideTimer = setTimeout(() => {
        catBubble.classList.remove("show");
    }, 4000);
}

function randomCatMessage() {

    const random =
      catMessages[Math.floor(Math.random() * catMessages.length)];

    showCatMessage(random);
}

setInterval(randomCatMessage, 12000);

catAssistant.addEventListener("click", randomCatMessage);

/* Section based messages */

window.addEventListener("scroll", () => {

    const scroll = window.scrollY;

    if(scroll > 500 && scroll < 1200){
        showCatMessage("⚙️ Wow! That's a lot of skills.");
    }

    if(scroll > 1200 && scroll < 2200){
        showCatMessage("💼 Experience unlocked.");
    }

    if(scroll > 2200){
        showCatMessage("🚀 These projects are pretty cool.");
    }
});
  </script>
  <!-- CAT ASSISTANT -->

<div id="catAssistant">

    <div id="catBubble">
        Welcome Human 👋
    </div>

    <div id="catEmoji">
        🐱
    </div>

</div>
</body>

</html>
