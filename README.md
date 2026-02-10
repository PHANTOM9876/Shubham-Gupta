
[index.html](https://github.com/user-attachments/files/25203233/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Shubham Gupta — Content & Social Media Strategist</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --ink: #0d0d0d;
      --paper: #f4f0e8;
      --cream: #ede8dc;
      --gold: #b8924a;
      --gold-light: #d4a85a;
      --rust: #a34a2a;
      --mid: #5a5248;
      --soft: #9c9285;
      --border: #d0c9bb;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--paper);
      color: var(--ink);
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      overflow-x: hidden;
    }

    /* ── NOISE TEXTURE OVERLAY ── */
    body::before {
      content: '';
      position: fixed; inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 999;
    }

    /* ── MASTHEAD / HEADER ── */
    header {
      padding: 0;
      border-bottom: 2px solid var(--ink);
      position: relative;
    }

    .masthead-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 18px 56px;
      border-bottom: 1px solid var(--border);
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--mid);
    }

    .masthead-date { }
    .masthead-tagline { 
      background: var(--ink);
      color: var(--paper);
      padding: 4px 12px;
      letter-spacing: 0.1em;
    }

    .masthead-hero {
      padding: 60px 56px 48px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0;
      align-items: end;
    }

    .hero-name {
      font-family: 'Playfair Display', serif;
      font-size: clamp(64px, 8vw, 108px);
      font-weight: 900;
      line-height: 0.92;
      letter-spacing: -0.02em;
      color: var(--ink);
    }

    .hero-name span {
      display: block;
      color: var(--gold);
    }

    .hero-right {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 24px;
      padding-bottom: 8px;
    }

    .hero-role {
      font-family: 'Playfair Display', serif;
      font-style: italic;
      font-size: 22px;
      color: var(--mid);
      text-align: right;
      line-height: 1.4;
    }

    .hero-contact {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 6px;
    }

    .hero-contact a {
      font-family: 'DM Mono', monospace;
      font-size: 11.5px;
      color: var(--mid);
      text-decoration: none;
      letter-spacing: 0.05em;
      transition: color 0.2s;
    }
    .hero-contact a:hover { color: var(--gold); }

    .divider-rule {
      height: 1px;
      background: linear-gradient(90deg, var(--ink) 60%, transparent);
      margin: 0 56px;
    }

    .masthead-kicker {
      padding: 14px 56px;
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--rust);
      border-top: 1px solid var(--border);
      display: flex;
      gap: 48px;
    }

    .kicker-tag::before { content: '◆ '; }

    /* ── NAV ── */
    nav {
      background: var(--ink);
      padding: 0 56px;
      display: flex;
      gap: 0;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    nav a {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--soft);
      text-decoration: none;
      padding: 16px 20px;
      border-right: 1px solid #2a2522;
      transition: color 0.2s, background 0.2s;
    }

    nav a:first-child { border-left: 1px solid #2a2522; }
    nav a:hover { color: var(--gold); background: #1a1714; }

    /* ── MAIN LAYOUT ── */
    main {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 56px;
    }

    section { padding: 72px 0; border-bottom: 1px solid var(--border); }
    section:last-child { border-bottom: none; }

    /* ── SECTION HEADERS ── */
    .section-label {
      font-family: 'DM Mono', monospace;
      font-size: 10.5px;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--rust);
      margin-bottom: 8px;
    }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(32px, 4vw, 48px);
      font-weight: 700;
      line-height: 1.1;
      margin-bottom: 40px;
      color: var(--ink);
    }

    /* ── ABOUT ── */
    .about-grid {
      display: grid;
      grid-template-columns: 5fr 3fr;
      gap: 64px;
      align-items: start;
    }

    .about-lead {
      font-family: 'Playfair Display', serif;
      font-size: 22px;
      line-height: 1.65;
      color: var(--ink);
      margin-bottom: 24px;
    }

    .about-lead em { color: var(--gold); font-style: italic; }

    .about-body {
      font-size: 15.5px;
      line-height: 1.8;
      color: var(--mid);
    }

    .about-stats {
      display: flex;
      flex-direction: column;
      gap: 0;
      border: 1px solid var(--border);
    }

    .stat-item {
      padding: 24px 28px;
      border-bottom: 1px solid var(--border);
    }
    .stat-item:last-child { border-bottom: none; }

    .stat-number {
      font-family: 'Playfair Display', serif;
      font-size: 48px;
      font-weight: 900;
      color: var(--gold);
      line-height: 1;
    }

    .stat-label {
      font-family: 'DM Mono', monospace;
      font-size: 10.5px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--mid);
      margin-top: 4px;
    }

    /* ── EXPERIENCE ── */
    .experience-list {
      display: flex;
      flex-direction: column;
      gap: 0;
    }

    .exp-item {
      display: grid;
      grid-template-columns: 200px 1fr;
      gap: 48px;
      padding: 40px 0;
      border-bottom: 1px solid var(--border);
      position: relative;
    }
    .exp-item:last-child { border-bottom: none; }

    .exp-meta {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .exp-date {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      letter-spacing: 0.1em;
      color: var(--soft);
    }

    .exp-company {
      font-family: 'Playfair Display', serif;
      font-size: 13px;
      font-weight: 700;
      color: var(--gold);
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .exp-badge {
      display: inline-block;
      background: var(--rust);
      color: #fff;
      font-family: 'DM Mono', monospace;
      font-size: 9px;
      letter-spacing: 0.1em;
      padding: 3px 8px;
      text-transform: uppercase;
      margin-top: 4px;
      width: fit-content;
    }

    .exp-content {}

    .exp-title {
      font-family: 'Playfair Display', serif;
      font-size: 26px;
      font-weight: 700;
      margin-bottom: 12px;
      line-height: 1.2;
    }

    .exp-desc {
      font-size: 15px;
      line-height: 1.75;
      color: var(--mid);
    }

    .exp-highlights {
      margin-top: 20px;
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .highlight-pill {
      border: 1px solid var(--border);
      background: var(--cream);
      font-family: 'DM Mono', monospace;
      font-size: 10.5px;
      letter-spacing: 0.08em;
      padding: 5px 12px;
      color: var(--mid);
    }

    /* ── SKILLS ── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 0;
      border: 1px solid var(--border);
    }

    .skill-block {
      padding: 36px 32px;
      border-right: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .skill-block:nth-child(3n) { border-right: none; }
    .skill-block:nth-last-child(-n+3) { border-bottom: none; }

    .skill-block-icon {
      font-size: 28px;
      margin-bottom: 16px;
    }

    .skill-block-title {
      font-family: 'Playfair Display', serif;
      font-size: 18px;
      font-weight: 700;
      margin-bottom: 12px;
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 12px;
    }

    .skill-tag {
      background: var(--ink);
      color: var(--paper);
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.08em;
      padding: 4px 10px;
    }

    .skill-tag.outline {
      background: transparent;
      color: var(--ink);
      border: 1px solid var(--ink);
    }

    /* ── CERTIFICATIONS ── */
    .cert-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .cert-card {
      background: var(--cream);
      border: 1px solid var(--border);
      padding: 28px 32px;
      position: relative;
      overflow: hidden;
      transition: transform 0.2s;
    }

    .cert-card:hover { transform: translateY(-2px); }

    .cert-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 4px; height: 100%;
      background: var(--gold);
    }

    .cert-title {
      font-family: 'Playfair Display', serif;
      font-size: 17px;
      font-weight: 700;
      margin-bottom: 6px;
      padding-left: 8px;
    }

    .cert-detail {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      color: var(--soft);
      letter-spacing: 0.06em;
      padding-left: 8px;
    }

    /* ── FEATURED WORK ── */
    .work-pullquote {
      border-left: 5px solid var(--gold);
      padding: 20px 40px;
      margin: 0 0 40px;
      background: var(--cream);
    }

    .work-pullquote p {
      font-family: 'Playfair Display', serif;
      font-style: italic;
      font-size: 22px;
      line-height: 1.6;
      color: var(--ink);
    }

    .work-items {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1px;
      background: var(--border);
      border: 1px solid var(--border);
    }

    .work-item {
      background: var(--paper);
      padding: 32px 28px;
      position: relative;
      overflow: hidden;
    }

    .work-item-num {
      font-family: 'Playfair Display', serif;
      font-size: 80px;
      font-weight: 900;
      color: var(--cream);
      position: absolute;
      top: -10px; right: 16px;
      line-height: 1;
      pointer-events: none;
    }

    .work-item-cat {
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--rust);
      margin-bottom: 10px;
    }

    .work-item-title {
      font-family: 'Playfair Display', serif;
      font-size: 18px;
      font-weight: 700;
      margin-bottom: 10px;
      line-height: 1.3;
    }

    .work-item-desc {
      font-size: 13.5px;
      line-height: 1.65;
      color: var(--mid);
    }

    /* ── FOOTER ── */
    footer {
      background: var(--ink);
      color: var(--paper);
      padding: 64px 56px;
      margin-top: 0;
    }

    .footer-inner {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 64px;
      align-items: center;
    }

    .footer-name {
      font-family: 'Playfair Display', serif;
      font-size: 48px;
      font-weight: 900;
      line-height: 0.95;
      margin-bottom: 16px;
    }

    .footer-name span { color: var(--gold); }

    .footer-tagline {
      font-family: 'Playfair Display', serif;
      font-style: italic;
      color: var(--soft);
      font-size: 16px;
    }

    .footer-links {
      display: flex;
      flex-direction: column;
      gap: 16px;
      align-items: flex-end;
    }

    .footer-link-item {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .footer-link-label {
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--soft);
    }

    .footer-link-val {
      font-family: 'DM Mono', monospace;
      font-size: 13px;
      color: var(--gold);
      text-decoration: none;
    }

    .footer-link-val:hover { color: #fff; }

    .footer-bottom {
      max-width: 1200px;
      margin: 40px auto 0;
      padding-top: 24px;
      border-top: 1px solid #2a2522;
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: #4a4540;
      display: flex;
      justify-content: space-between;
    }

    /* ── ANIMATIONS ── */
    @keyframes fadeSlide {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .hero-name, .hero-role { animation: fadeSlide 0.9s ease both; }
    .hero-role { animation-delay: 0.15s; }
    .hero-contact { animation: fadeSlide 0.9s ease 0.3s both; }
    .masthead-kicker { animation: fadeSlide 0.9s ease 0.4s both; }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      header, nav, main, footer { padding-left: 24px; padding-right: 24px; }
      .masthead-hero { grid-template-columns: 1fr; gap: 32px; }
      .hero-right { align-items: flex-start; }
      .hero-role, .hero-contact { text-align: left; align-items: flex-start; }
      .about-grid { grid-template-columns: 1fr; }
      .skills-grid { grid-template-columns: 1fr; }
      .cert-grid { grid-template-columns: 1fr; }
      .work-items { grid-template-columns: 1fr; }
      .footer-inner { grid-template-columns: 1fr; }
      .footer-links { align-items: flex-start; }
      .exp-item { grid-template-columns: 1fr; gap: 16px; }
      .masthead-top { flex-direction: column; gap: 8px; }
    }
  </style>
</head>
<body>

<!-- ══════════ HEADER / MASTHEAD ══════════ -->
<header>
  <div class="masthead-top">
    <span class="masthead-date">Panipat, Haryana · India</span>
    <span class="masthead-tagline">Content · Social Media · Digital Strategy</span>
    <span>Open to Remote &amp; On-site</span>
  </div>

  <div class="masthead-hero">
    <div class="hero-name">
      Shubham<span>Gupta.</span>
    </div>
    <div class="hero-right">
      <div class="hero-role">
        Content Writer &amp; Social<br/>Media Strategist
      </div>
      <div class="hero-contact">
        <a href="/cdn-cgi/l/email-protection#066173767267756e73646e676b333f3e313046616b676f6a2865696b"><span class="__cf_email__" data-cfemail="caadbfbabeabb9a2bfa8a2aba7fff3f2fdfc8aada7aba3a6e4a9a5a7">[email&#160;protected]</span></a>
        <a href="https://www.linkedin.com/in/shubham-gupta-24785a217" target="_blank">linkedin.com/in/shubham-gupta-24785a217</a>
        <a href="#">Panipat, Haryana — 132103</a>
      </div>
    </div>
  </div>

  <div class="divider-rule"></div>

  <div class="masthead-kicker">
    <span class="kicker-tag">5+ Years Writing Experience</span>
    <span class="kicker-tag">Employee of the Month — Jan 2025</span>
    <span class="kicker-tag">50 WPM Certified Typist</span>
  </div>
</header>

<!-- ══════════ NAV ══════════ -->
<nav>
  <a href="#about">About</a>
  <a href="#experience">Experience</a>
  <a href="#work">Work</a>
  <a href="#skills">Skills</a>
  <a href="#certifications">Certifications</a>
  <a href="#contact">Contact</a>
</nav>

<!-- ══════════ MAIN ══════════ -->
<main>

  <!-- ABOUT -->
  <section id="about">
    <div class="section-label">§ 01 — Profile</div>
    <div class="section-title">Who I Am</div>
    <div class="about-grid">
      <div>
        <p class="about-lead">
          A self-driven content professional with over <em>5 years</em> of hands-on experience turning ideas into compelling digital narratives — from long-form articles to high-performing YouTube scripts.
        </p>
        <p class="about-body">
          I specialise in content writing, social media management, and digital marketing strategy. Having written extensively in the fitness and lifestyle niche — including detailed biographies of female fitness personalities — I understand how to research deeply, write authentically, and engage audiences who care about quality. I am currently working as a Social &amp; Multimedia Handler at Taggify, where I hit my first performance goal ahead of schedule and earned Employee of the Month recognition in my very first month.
          <br/><br/>
          I bring a cooperative, deadline-driven work ethic and am fully comfortable working beyond standard hours when the project demands it. Whether remote or on-site, I show up with full commitment and a bias for action.
        </p>
      </div>
      <div class="about-stats">
        <div class="stat-item">
          <div class="stat-number">5+</div>
          <div class="stat-label">Years of Content Experience</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">50</div>
          <div class="stat-label">WPM Typing Speed (Certified)</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">1st</div>
          <div class="stat-label">Month — Employee of the Month</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">2</div>
          <div class="stat-label">Offline Hackathons Participated</div>
        </div>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE -->
  <section id="experience">
    <div class="section-label">§ 02 — Career</div>
    <div class="section-title">Work Experience</div>
    <div class="experience-list">

      <div class="exp-item">
        <div class="exp-meta">
          <span class="exp-date">Dec 2024 — Present</span>
          <span class="exp-company">Taggify</span>
          <span class="exp-badge">★ Employee of the Month</span>
        </div>
        <div class="exp-content">
          <div class="exp-title">Social Media &amp; Multimedia Handler</div>
          <p class="exp-desc">
            Joined Taggify as a full-spectrum digital content handler, responsible for planning, creating, and distributing multimedia content across social media channels. Achieved all first-month targets within the assigned deadline and was recognised with the Employee of the Month award — a milestone reflecting both performance quality and team collaboration. Work spans content strategy, post scheduling, visual briefing, and cross-platform audience engagement.
          </p>
          <div class="exp-highlights">
            <span class="highlight-pill">Social Media Strategy</span>
            <span class="highlight-pill">Multimedia Content</span>
            <span class="highlight-pill">Content Planning</span>
            <span class="highlight-pill">Platform Management</span>
            <span class="highlight-pill">Deadline Delivery</span>
          </div>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-meta">
          <span class="exp-date">2019 — 2024</span>
          <span class="exp-company">Freelance / Digital Clients</span>
        </div>
        <div class="exp-content">
          <div class="exp-title">Freelance Content Writer &amp; YouTube Scriptwriter</div>
          <p class="exp-desc">
            Over five years of independent writing work across two core verticals: in-depth biographical articles on female fitness models published to niche wellness and lifestyle websites, and engaging YouTube video scripts crafted to maximise watch-time and viewer retention. Developed a disciplined research and writing process, consistently delivering SEO-optimised content with strong on-page structure, naturally integrated keywords, and targeted audience tone.
          </p>
          <div class="exp-highlights">
            <span class="highlight-pill">Long-form Articles</span>
            <span class="highlight-pill">YouTube Scripting</span>
            <span class="highlight-pill">Fitness &amp; Lifestyle Niche</span>
            <span class="highlight-pill">On-Page SEO</span>
            <span class="highlight-pill">Keyword Research</span>
            <span class="highlight-pill">Content Research</span>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- FEATURED WORK -->
  <section id="work">
    <div class="section-label">§ 03 — Portfolio</div>
    <div class="section-title">What I Create</div>

    <div class="work-pullquote">
      <p>"Good content isn't just written — it's engineered for the right audience, at the right time, on the right platform."</p>
    </div>

    <div class="work-items">
      <div class="work-item">
        <div class="work-item-num">01</div>
        <div class="work-item-cat">Web Content</div>
        <div class="work-item-title">Fitness Model Biographies</div>
        <p class="work-item-desc">Long-form, well-researched biographical articles on fitness personalities, crafted for engagement, SEO discoverability, and reader trust. Published across multiple niche wellness websites.</p>
      </div>
      <div class="work-item">
        <div class="work-item-num">02</div>
        <div class="work-item-cat">Video Production</div>
        <div class="work-item-title">YouTube Scripts</div>
        <p class="work-item-desc">High-retention video scripts with strong hooks, structured narrative arcs, and clear calls-to-action. Written for channels in the fitness, lifestyle, and informational content space over 5+ years.</p>
      </div>
      <div class="work-item">
        <div class="work-item-num">03</div>
        <div class="work-item-cat">Social Media</div>
        <div class="work-item-title">Multi-Platform Content</div>
        <p class="work-item-desc">Day-to-day social media handling at Taggify — content research, post creation, caption writing, and platform-specific strategy for brand visibility and audience growth.</p>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <div class="section-label">§ 04 — Competencies</div>
    <div class="section-title">Skills &amp; Tools</div>
    <div class="skills-grid">
      <div class="skill-block">
        <div class="skill-block-icon">✍️</div>
        <div class="skill-block-title">Content Writing</div>
        <p style="font-size:14px; color:var(--mid); line-height:1.6;">From short-form social captions to long-form editorial articles and detailed video scripts, I write content that informs, entertains, and converts.</p>
        <div class="skill-tags">
          <span class="skill-tag">Article Writing</span>
          <span class="skill-tag">Scriptwriting</span>
          <span class="skill-tag">Copywriting</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-icon">🔍</div>
        <div class="skill-block-title">SEO &amp; Research</div>
        <p style="font-size:14px; color:var(--mid); line-height:1.6;">Skilled in on-page SEO best practices, keyword identification, SERP analysis, and content structuring for organic discoverability.</p>
        <div class="skill-tags">
          <span class="skill-tag">On-Page SEO</span>
          <span class="skill-tag">Keyword Research</span>
          <span class="skill-tag">Content Research</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-icon">📱</div>
        <div class="skill-block-title">Social Media</div>
        <p style="font-size:14px; color:var(--mid); line-height:1.6;">End-to-end social media handling — strategy, scheduling, content creation, audience research, and performance analysis.</p>
        <div class="skill-tags">
          <span class="skill-tag">Social Strategy</span>
          <span class="skill-tag">Content Calendar</span>
          <span class="skill-tag">Audience Research</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-icon">📊</div>
        <div class="skill-block-title">Data &amp; Productivity</div>
        <p style="font-size:14px; color:var(--mid); line-height:1.6;">Comfortable with data entry, organisation, and management using Excel and Google Sheets for reporting and content tracking.</p>
        <div class="skill-tags">
          <span class="skill-tag">Microsoft Excel</span>
          <span class="skill-tag">Google Sheets</span>
          <span class="skill-tag">Data Entry</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-icon">⌨️</div>
        <div class="skill-block-title">Typing &amp; Speed</div>
        <p style="font-size:14px; color:var(--mid); line-height:1.6;">Certified ghost typist with a documented speed of 50 WPM — an asset for high-volume content production and quick turnarounds.</p>
        <div class="skill-tags">
          <span class="skill-tag">Ghost Typing</span>
          <span class="skill-tag">50 WPM Certified</span>
          <span class="skill-tag">Fast Delivery</span>
        </div>
      </div>
      <div class="skill-block">
        <div class="skill-block-icon">💻</div>
        <div class="skill-block-title">Tech &amp; Digital</div>
        <p style="font-size:14px; color:var(--mid); line-height:1.6;">ADCA certified with working knowledge of digital tools, basic Linux operations (Kali), and technical workshop participation.</p>
        <div class="skill-tags">
          <span class="skill-tag">ADCA</span>
          <span class="skill-tag">Kali Linux (Basic)</span>
          <span class="skill-tag">Computer Applications</span>
        </div>
      </div>
    </div>
  </section>

  <!-- CERTIFICATIONS -->
  <section id="certifications">
    <div class="section-label">§ 05 — Credentials</div>
    <div class="section-title">Education &amp; Certifications</div>
    <div class="cert-grid">
      <div class="cert-card">
        <div class="cert-title">Senior Secondary — Medical Stream</div>
        <div class="cert-detail">12th Standard · Passed 2020 · Science (Medical)</div>
      </div>
      <div class="cert-card">
        <div class="cert-title">Advanced Diploma in Computer Applications</div>
        <div class="cert-detail">ADCA · Completed · Computer Operations &amp; Applications</div>
      </div>
      <div class="cert-card">
        <div class="cert-title">Ghost Typing Certificate — 50 WPM</div>
        <div class="cert-detail">Certified Typing Speed · Professional Level</div>
      </div>
      <div class="cert-card">
        <div class="cert-title">Technical Workshop Certificates</div>
        <div class="cert-detail">Online &amp; Offline Workshops · Technical Skills Development</div>
      </div>
      <div class="cert-card">
        <div class="cert-title">Hackathon Participation × 2</div>
        <div class="cert-detail">Offline Hackathons · Problem Solving &amp; Tech Collaboration</div>
      </div>
      <div class="cert-card">
        <div class="cert-title">BCA — Computer Applications</div>
        <div class="cert-detail">PIET College · Affiliated to KUK · 2022–2023 (Studied)</div>
      </div>
    </div>
  </section>

</main>

<!-- ══════════ FOOTER ══════════ -->
<footer id="contact">
  <div class="footer-inner">
    <div>
      <div class="footer-name">Shubham<br/><span>Gupta.</span></div>
      <div class="footer-tagline">Available for content writing, social media &amp; digital marketing roles — remote or on-site.</div>
    </div>
    <div class="footer-links">
      <div class="footer-link-item">
        <span class="footer-link-label">Email</span>
        <a class="footer-link-val" href="/cdn-cgi/l/email-protection#452230353124362d30272d2428707c7d7273052228242c296b262a28"><span class="__cf_email__" data-cfemail="bfd8cacfcbdeccd7caddd7ded28a86878889ffd8d2ded6d391dcd0d2">[email&#160;protected]</span></a>
      </div>
      <div class="footer-link-item">
        <span class="footer-link-label">LinkedIn</span>
        <a class="footer-link-val" href="https://www.linkedin.com/in/shubham-gupta-24785a217" target="_blank">linkedin.com/in/shubham-gupta-24785a217</a>
      </div>
      <div class="footer-link-item">
        <span class="footer-link-label">Location</
