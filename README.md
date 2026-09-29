<!doctype html>
<html lang="en" data-theme="dark">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="Omar Mohamed — Founder, growth and commercial operator, and AI product builder creating revenue operating systems.">
  <meta name="color-scheme" content="dark light">
  <meta name="theme-color" content="#08101f">
  <title>Omar Mohamed — Revenue Systems Builder</title>
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' rx='15' fill='%2308101f'/%3E%3Cpath d='M14 32c0-11 7-18 18-18s18 7 18 18-7 18-18 18-18-7-18-18Zm10 0c0 6 3 10 8 10s8-4 8-10-3-10-8-10-8 4-8 10Z' fill='%235b8cff'/%3E%3Ccircle cx='48' cy='16' r='5' fill='%23ffba69'/%3E%3C/svg%3E">
  <style>
    :root {
      --bg: #f4f6fa;
      --bg-2: #e8edf6;
      --panel: rgba(255,255,255,.76);
      --panel-solid: #ffffff;
      --text: #0b1425;
      --muted: #5b6576;
      --line: rgba(11,20,37,.13);
      --soft-line: rgba(11,20,37,.07);
      --accent: #245eea;
      --accent-2: #9458ff;
      --warm: #d97718;
      --nav: rgba(244,246,250,.78);
      --shadow: 0 22px 70px rgba(22,39,77,.12);
      --grid: rgba(11,20,37,.045);
      --orb: rgba(36,94,234,.16);
      --max: 1200px;
      --radius: 24px;
    }

    html[data-theme="dark"] {
      --bg: #070d18;
      --bg-2: #0a1323;
      --panel: rgba(13,25,45,.72);
      --panel-solid: #0f1b30;
      --text: #f4f7fc;
      --muted: #99a7bd;
      --line: rgba(199,216,242,.16);
      --soft-line: rgba(199,216,242,.08);
      --accent: #6d96ff;
      --accent-2: #ad82ff;
      --warm: #ffba69;
      --nav: rgba(7,13,24,.78);
      --shadow: 0 28px 90px rgba(0,0,0,.32);
      --grid: rgba(199,216,242,.042);
      --orb: rgba(68,111,224,.23);
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      color: var(--text);
      background:
        radial-gradient(circle at 74% 7%, var(--orb), transparent 26rem),
        linear-gradient(var(--grid) 1px, transparent 1px),
        linear-gradient(90deg, var(--grid) 1px, transparent 1px),
        var(--bg);
      background-size: auto, 46px 46px, 46px 46px, auto;
      font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      font-size: 16px;
      line-height: 1.65;
      overflow-x: hidden;
      transition: background-color .25s ease, color .25s ease;
    }

    ::selection { background: var(--accent); color: #fff; }
    a { color: inherit; text-decoration: none; }
    button, a { -webkit-tap-highlight-color: transparent; }
    button { font: inherit; }
    :focus-visible { outline: 3px solid var(--accent); outline-offset: 4px; }

    .skip-link {
      position: fixed; left: 1rem; top: -5rem; z-index: 100;
      padding: .7rem 1rem; background: var(--text); color: var(--bg); border-radius: 10px;
    }
    .skip-link:focus { top: 1rem; }

    .container { width: min(calc(100% - 2rem), var(--max)); margin-inline: auto; }
    .section { padding: clamp(5rem, 10vw, 9rem) 0; position: relative; }
    .section.compact { padding-block: clamp(3.6rem, 7vw, 6rem); }
    .rule { border-top: 1px solid var(--line); }

    .eyebrow {
      display: inline-flex; align-items: center; gap: .6rem;
      margin: 0 0 1.2rem; color: var(--accent); font-size: .76rem;
      font-weight: 800; letter-spacing: .16em; text-transform: uppercase;
    }
    .eyebrow::before { content: ""; width: 1.8rem; height: 2px; background: currentColor; }
    h1, h2, h3, p { margin-top: 0; }
    h1, h2, h3 { line-height: 1.04; letter-spacing: -.045em; }
    h1 { max-width: 1000px; margin-bottom: 1.6rem; font-size: clamp(3rem, 8.8vw, 8.2rem); font-weight: 760; }
    h2 { margin-bottom: 1.3rem; font-size: clamp(2.3rem, 5vw, 4.6rem); font-weight: 720; }
    h3 { margin-bottom: .85rem; font-size: clamp(1.35rem, 2.3vw, 2rem); }
    .lead { max-width: 760px; color: var(--muted); font-size: clamp(1.12rem, 2vw, 1.45rem); line-height: 1.58; }
    .section-head { display: grid; grid-template-columns: .8fr 1.2fr; gap: 3rem; align-items: end; margin-bottom: clamp(2.6rem, 6vw, 5rem); }
    .section-head p { max-width: 610px; margin: 0; color: var(--muted); }

    .nav-shell {
      position: fixed; inset: 0 0 auto; z-index: 50;
      background: var(--nav); border-bottom: 1px solid transparent;
      backdrop-filter: blur(18px); transition: border-color .2s ease;
    }
    .nav-shell.scrolled { border-color: var(--line); }
    nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 1.5rem; }
    .brand { display: inline-flex; align-items: center; gap: .8rem; font-weight: 780; letter-spacing: -.02em; }
    .brand-mark { width: 34px; aspect-ratio: 1; display: grid; place-items: center; border-radius: 10px; background: var(--text); color: var(--bg); font-size: .78rem; }
    .nav-links { display: flex; align-items: center; gap: 1.5rem; color: var(--muted); font-size: .88rem; font-weight: 650; }
    .nav-links a { transition: color .2s ease; }
    .nav-links a:hover { color: var(--text); }
    .nav-actions { display: flex; align-items: center; gap: .6rem; }
    .icon-btn, .menu-btn {
      width: 42px; height: 42px; display: grid; place-items: center;
      border: 1px solid var(--line); color: var(--text); background: var(--panel);
      border-radius: 50%; cursor: pointer;
    }
    .menu-btn { display: none; }

    .hero { min-height: 100svh; padding: 10.5rem 0 4rem; display: flex; align-items: center; }
    .hero-grid { width: 100%; display: grid; grid-template-columns: 1fr auto; gap: 2rem; align-items: end; }
    .hero h1 .outline { color: transparent; -webkit-text-stroke: 1.5px var(--muted); }
    .hero h1 .accent { color: var(--accent); }
    .hero-copy { max-width: 730px; color: var(--muted); font-size: clamp(1.12rem, 2vw, 1.4rem); }
    .hero-actions { display: flex; flex-wrap: wrap; gap: .8rem; margin-top: 2.2rem; }
    .button {
      min-height: 48px; display: inline-flex; align-items: center; justify-content: center; gap: .65rem;
      padding: .75rem 1.15rem; border: 1px solid var(--line); border-radius: 999px;
      background: var(--text); color: var(--bg); font-weight: 750; font-size: .9rem;
      transition: transform .2s ease, box-shadow .2s ease;
    }
    .button:hover { transform: translateY(-2px); box-shadow: 0 10px 30px rgba(0,0,0,.16); }
    .button.secondary { background: transparent; color: var(--text); }
    .hero-aside { width: 165px; padding-bottom: .2rem; }
    .hero-aside .index { display: block; color: var(--warm); font-size: 2.6rem; font-weight: 300; line-height: 1; }
    .hero-aside p { margin: .7rem 0 0; color: var(--muted); font-size: .78rem; text-transform: uppercase; letter-spacing: .12em; }
    .signal-line { height: 1px; margin: 5rem 0 1.8rem; background: linear-gradient(90deg, var(--accent), var(--line) 70%, transparent); }
    .hero-meta { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1rem; color: var(--muted); }
    .hero-meta span { border-left: 1px solid var(--line); padding-left: 1rem; font-size: .8rem; letter-spacing: .1em; text-transform: uppercase; }

    .about-grid { display: grid; grid-template-columns: .78fr 1.22fr; gap: clamp(3rem, 8vw, 8rem); align-items: start; }
    .about-note { position: sticky; top: 7rem; }
    .about-note .big-number { color: var(--accent); font-size: clamp(5rem, 10vw, 9rem); line-height: .8; letter-spacing: -.08em; font-weight: 250; }
    .about-copy p { color: var(--muted); font-size: clamp(1.08rem, 1.8vw, 1.3rem); }
    .about-copy p:first-child { color: var(--text); font-size: clamp(1.45rem, 2.4vw, 2rem); line-height: 1.45; letter-spacing: -.025em; }
    .inline-highlight { color: var(--accent); }

    .venture-list { border-top: 1px solid var(--line); }
    .venture {
      display: grid; grid-template-columns: 52px 1fr 1fr; gap: 2rem;
      padding: 2rem 0; border-bottom: 1px solid var(--line); align-items: start;
      transition: padding .25s ease, background .25s ease;
    }
    .venture:hover { padding-inline: 1rem; background: linear-gradient(90deg, var(--soft-line), transparent); }
    .venture-num { color: var(--warm); font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: .82rem; }
    .venture h3 { margin: 0; }
    .venture-type { display: block; margin-top: .55rem; color: var(--accent); font-size: .75rem; font-weight: 800; letter-spacing: .13em; text-transform: uppercase; }
    .venture p { margin: 0; color: var(--muted); }

    .expertise-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; }
    .expertise-card {
      min-height: 280px; display: flex; flex-direction: column; justify-content: space-between;
      padding: 1.6rem; border: 1px solid var(--line); border-radius: var(--radius); background: var(--panel);
      box-shadow: 0 1px 0 var(--soft-line); backdrop-filter: blur(10px);
    }
    .expertise-card .mono { color: var(--accent); font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: .75rem; }
    .expertise-card p { margin: 0; color: var(--muted); }

    .stack-wrap { display: grid; grid-template-columns: 1fr 2fr; gap: 4rem; }
    .stack-cloud { display: flex; flex-wrap: wrap; align-content: start; gap: .7rem; }
    .tag { padding: .64rem .88rem; border: 1px solid var(--line); border-radius: 999px; background: var(--panel); color: var(--muted); font-size: .84rem; font-weight: 650; }
    .tag.accent { color: var(--accent); border-color: color-mix(in srgb, var(--accent) 45%, transparent); }

    .thesis-shell {
      position: relative; overflow: hidden; padding: clamp(1.2rem, 4vw, 3.4rem);
      border: 1px solid var(--line); border-radius: 36px; background: var(--panel-solid); box-shadow: var(--shadow);
    }
    .thesis-intro { max-width: 650px; margin-bottom: 3rem; }
    .system-map { display: grid; grid-template-columns: repeat(5, 1fr); gap: .7rem; position: relative; }
    .system-node { position: relative; min-height: 170px; padding: 1.1rem; border: 1px solid var(--line); border-radius: 18px; background: var(--bg); }
    .system-node::after { content: ""; position: absolute; left: calc(100% + 1px); top: 50%; width: .7rem; height: 1px; background: var(--accent); }
    .system-node:last-child::after { display: none; }
    .system-node b { display: block; margin-bottom: .5rem; font-size: 1rem; }
    .system-node span { color: var(--muted); font-size: .78rem; line-height: 1.45; }
    .system-node strong { display: block; margin-top: 1.2rem; color: var(--accent); font-size: 1.5rem; font-weight: 400; }

    .markets { display: grid; grid-template-columns: repeat(3, 1fr); border-top: 1px solid var(--line); border-left: 1px solid var(--line); }
    .market { min-height: 220px; padding: 1.6rem; border-right: 1px solid var(--line); border-bottom: 1px solid var(--line); }
    .market .flag { display: inline-block; margin-bottom: 4rem; color: var(--warm); font-size: .75rem; letter-spacing: .14em; }
    .market p { color: var(--muted); margin-bottom: 0; }

    .work-grid { display: grid; grid-template-columns: repeat(12, 1fr); gap: 1rem; }
    .case { grid-column: span 6; min-height: 380px; padding: 1.8rem; display: flex; flex-direction: column; justify-content: space-between; border: 1px solid var(--line); border-radius: var(--radius); background: var(--panel); }
    .case.featured { grid-column: span 8; min-height: 440px; background: linear-gradient(140deg, color-mix(in srgb, var(--accent) 18%, var(--panel-solid)), var(--panel-solid)); }
    .case.narrow { grid-column: span 4; }
    .case-label { color: var(--accent); font-size: .75rem; font-weight: 800; letter-spacing: .12em; text-transform: uppercase; }
    .case p { color: var(--muted); }
    .case-tags { display: flex; flex-wrap: wrap; gap: .5rem; }
    .case-tags span { padding: .35rem .55rem; border: 1px solid var(--line); border-radius: 99px; color: var(--muted); font-size: .72rem; }

    .teaching-grid { display: grid; grid-template-columns: 1.1fr .9fr; gap: 1rem; }
    .teaching-main, .teaching-side { padding: clamp(1.5rem, 4vw, 3rem); border-radius: var(--radius); }
    .teaching-main { background: var(--text); color: var(--bg); }
    .teaching-main p { max-width: 650px; color: color-mix(in srgb, var(--bg) 72%, transparent); }
    .teaching-side { border: 1px solid var(--line); background: var(--panel); }
    .teaching-side ul { margin: 1.5rem 0 0; padding: 0; list-style: none; }
    .teaching-side li { padding: .85rem 0; border-top: 1px solid var(--line); color: var(--muted); }

    .principles { counter-reset: principle; display: grid; grid-template-columns: repeat(2, 1fr); gap: 0 4rem; }
    .principle { counter-increment: principle; position: relative; padding: 1.6rem 0 1.6rem 3.3rem; border-top: 1px solid var(--line); }
    .principle::before { content: "0" counter(principle); position: absolute; left: 0; top: 1.8rem; color: var(--warm); font-family: ui-monospace, SFMono-Regular, Menlo, monospace; font-size: .76rem; }
    .principle b { display: block; margin-bottom: .35rem; }
    .principle p { margin: 0; color: var(--muted); }

    .contact-card {
      padding: clamp(2rem, 7vw, 6rem); border-radius: 36px;
      background: linear-gradient(135deg, var(--accent), var(--accent-2)); color: white;
      box-shadow: var(--shadow); text-align: center;
    }
    .contact-card h2 { max-width: 830px; margin-inline: auto; }
    .contact-card p { max-width: 620px; margin: 0 auto 2rem; color: rgba(255,255,255,.78); }
    .contact-links { display: flex; flex-wrap: wrap; justify-content: center; gap: .7rem; }
    .contact-links a, .contact-links button { padding: .75rem 1rem; border: 1px solid rgba(255,255,255,.35); border-radius: 999px; background: rgba(0,0,0,.12); color: #fff; cursor: pointer; font-weight: 720; }
    .contact-links a:hover, .contact-links button:hover { background: rgba(0,0,0,.24); }

    footer { padding: 2.3rem 0; border-top: 1px solid var(--line); color: var(--muted); font-size: .82rem; }
    .footer-grid { display: flex; justify-content: space-between; gap: 1rem; }
    .toast { position: fixed; left: 50%; bottom: 1.5rem; z-index: 80; transform: translate(-50%, 6rem); padding: .8rem 1rem; border: 1px solid var(--line); border-radius: 12px; background: var(--text); color: var(--bg); box-shadow: var(--shadow); opacity: 0; transition: .3s ease; }
    .toast.show { transform: translate(-50%, 0); opacity: 1; }

    .reveal { opacity: 0; transform: translateY(22px); transition: opacity .7s ease, transform .7s ease; }
    .reveal.visible { opacity: 1; transform: none; }

    @media (max-width: 900px) {
      .nav-links { position: fixed; inset: 77px 1rem auto; display: none; flex-direction: column; align-items: stretch; padding: 1rem; border: 1px solid var(--line); border-radius: 18px; background: var(--panel-solid); box-shadow: var(--shadow); }
      .nav-links.open { display: flex; }
      .nav-links a { padding: .7rem; }
      .menu-btn { display: grid; }
      .hero-grid, .section-head, .about-grid, .stack-wrap, .teaching-grid { grid-template-columns: 1fr; }
      .hero-aside { display: none; }
      .hero-meta { grid-template-columns: repeat(2, 1fr); }
      .about-note { position: static; }
      .expertise-grid { grid-template-columns: repeat(2, 1fr); }
      .system-map { grid-template-columns: 1fr; }
      .system-node { min-height: auto; }
      .system-node::after { left: 2rem; top: 100%; width: 1px; height: .7rem; }
      .markets { grid-template-columns: repeat(2, 1fr); }
      .case.featured, .case.narrow, .case { grid-column: span 12; min-height: 320px; }
    }

    @media (max-width: 620px) {
      .container { width: min(calc(100% - 1.25rem), var(--max)); }
      .section { padding-block: 4.5rem; }
      h1 { font-size: clamp(3rem, 15vw, 5rem); }
      .brand span:last-child { display: none; }
      .hero { padding-top: 8.5rem; }
      .hero-meta, .expertise-grid, .markets, .principles { grid-template-columns: 1fr; }
      .hero-meta { gap: .7rem; }
      .venture { grid-template-columns: 36px 1fr; gap: 1rem; }
      .venture p { grid-column: 2; }
      .expertise-card { min-height: 230px; }
      .market .flag { margin-bottom: 2rem; }
      .footer-grid { flex-direction: column; }
    }

    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      *, *::before, *::after { animation: none !important; transition: none !important; }
      .reveal { opacity: 1; transform: none; }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#main">Skip to content</a>
  <header class="nav-shell" id="navShell">
    <nav class="container" aria-label="Primary navigation">
      <a class="brand" href="#top" aria-label="Omar Mohamed, home">
        <span class="brand-mark">OM</span><span>Omar Mohamed</span>
      </a>
      <div class="nav-links" id="navLinks">
        <a href="#about">About</a><a href="#ventures">Ventures</a><a href="#work">Work</a><a href="#thesis">Thesis</a><a href="#contact">Contact</a>
      </div>
      <div class="nav-actions">
        <button class="icon-btn" id="themeToggle" aria-label="Switch color theme" title="Switch color theme">
          <span aria-hidden="true" id="themeIcon">☼</span>
        </button>
        <button class="menu-btn" id="menuToggle" aria-label="Open navigation" aria-expanded="false" aria-controls="navLinks">☰</button>
      </div>
    </nav>
  </header>

  <main id="main">
    <section class="hero" id="top">
      <div class="container">
        <div class="hero-grid">
          <div>
            <p class="eyebrow">Founder · Operator · Builder</p>
            <h1>Revenue is a <span class="outline">system.</span><br>I build the <span class="accent">operating layer.</span></h1>
            <p class="hero-copy">I’m Omar Mohamed—building at the intersection of growth, commercial strategy, revenue operations, automation, data, and AI.</p>
            <div class="hero-actions">
              <a class="button" href="#ventures">Explore the portfolio</a>
              <a class="button secondary" href="#contact">Start a conversation</a>
            </div>
          </div>
          <aside class="hero-aside" aria-label="Positioning summary">
            <span class="index">01</span>
            <p>Strategy translated into infrastructure</p>
          </aside>
        </div>
        <div class="signal-line"></div>
        <div class="hero-meta" aria-label="Areas of focus">
          <span>Growth systems</span><span>AI products</span><span>Revenue operations</span><span>GTM infrastructure</span>
        </div>
      </div>
    </section>

    <section class="section rule" id="about">
      <div class="container about-grid">
        <aside class="about-note reveal">
          <p class="eyebrow">About</p>
          <div class="big-number">∞</div>
          <p class="lead">One connected system, not a collection of disconnected tactics.</p>
        </aside>
        <div class="about-copy reveal">
          <p>I design <span class="inline-highlight">Revenue Operating Systems</span> that connect strategy, acquisition, sales, CRM, automation, analytics, and AI into one coherent commercial engine.</p>
          <p>My work is deliberately cross-functional. I move between board-level questions and system-level details: how a company should grow, what its funnel should measure, where automation creates leverage, and how intelligence can turn fragmented data into decisive action.</p>
          <p>The goal is not more software or more dashboards. It is a business that learns faster, operates with greater clarity, and compounds what works.</p>
        </div>
      </div>
    </section>

    <section class="section" id="ventures">
      <div class="container">
        <div class="section-head reveal">
          <div><p class="eyebrow">Venture portfolio</p><h2>Built for different moments of growth.</h2></div>
          <p>Products, services, and learning platforms organized around a single idea: commercial growth becomes more durable when its operating system is designed intentionally.</p>
        </div>
        <div class="venture-list reveal">
          <article class="venture"><span class="venture-num">01</span><div><h3>Rihan AI</h3><span class="venture-type">AI revenue intelligence</span></div><p>An intelligence layer for revenue teams—connecting commercial data, diagnosing what changed, explaining why, and helping teams decide what to do next.</p></article>
          <article class="venture"><span class="venture-num">02</span><div><h3>Growth Way</h3><span class="venture-type">Growth infrastructure</span></div><p>Strategy and implementation for companies building the systems behind sustainable acquisition, sales, CRM, RevOps, automation, and analytics.</p></article>
          <article class="venture"><span class="venture-num">03</span><div><h3>Launch Key</h3><span class="venture-type">Go-to-market architecture</span></div><p>A launch-focused operating model that turns market insight, positioning, offer design, channel planning, and execution into a coordinated path to market.</p></article>
          <article class="venture"><span class="venture-num">04</span><div><h3>Scale With Omar</h3><span class="venture-type">Operator education</span></div><p>Practical thinking for founders and growth leaders who want to move beyond isolated tactics and build repeatable systems for scale.</p></article>
          <article class="venture"><span class="venture-num">05</span><div><h3>Full Stack Funnel Builder</h3><span class="venture-type">Capability building</span></div><p>A structured way to develop end-to-end funnel fluency—from demand and conversion to retention, instrumentation, experimentation, and automation.</p></article>
        </div>
      </div>
    </section>

    <section class="section rule" id="expertise">
      <div class="container">
        <div class="section-head reveal">
          <div><p class="eyebrow">Expertise</p><h2>From commercial thesis to working system.</h2></div>
          <p>I work across the interfaces where ownership often breaks down—between marketing and sales, strategy and implementation, data and action.</p>
        </div>
        <div class="expertise-grid">
          <article class="expertise-card reveal"><span class="mono">01 / GROWTH</span><div><h3>Growth strategy</h3><p>Market choices, growth models, funnel architecture, experimentation, and the operating cadence required to learn.</p></div></article>
          <article class="expertise-card reveal"><span class="mono">02 / REVOPS</span><div><h3>Revenue operations</h3><p>Lifecycle design, CRM structure, pipeline logic, handoffs, measurement, and alignment around one revenue model.</p></div></article>
          <article class="expertise-card reveal"><span class="mono">03 / AI</span><div><h3>AI product building</h3><p>Agents and intelligence layers that summarize, diagnose, recommend, automate, and strengthen operator judgment.</p></div></article>
          <article class="expertise-card reveal"><span class="mono">04 / AUTOMATION</span><div><h3>Workflow automation</h3><p>Reliable workflows that connect tools, eliminate repetitive work, and keep data moving across the commercial stack.</p></div></article>
          <article class="expertise-card reveal"><span class="mono">05 / GTM</span><div><h3>Go-to-market systems</h3><p>Positioning, offers, channels, launch mechanics, sales enablement, and a route from attention to retained revenue.</p></div></article>
          <article class="expertise-card reveal"><span class="mono">06 / ANALYTICS</span><div><h3>Decision intelligence</h3><p>Instrumentation and analysis designed around the decisions teams need to make—not vanity dashboards.</p></div></article>
        </div>
      </div>
    </section>

    <section class="section compact" id="stack">
      <div class="container stack-wrap reveal">
        <div><p class="eyebrow">Working stack</p><h2>Tools serve the system.</h2><p class="lead">Platform-agnostic by design. The architecture starts with the business problem.</p></div>
        <div class="stack-cloud" aria-label="Tools and disciplines">
          <span class="tag accent">AI Agents</span><span class="tag accent">LLMs</span><span class="tag">CRM Architecture</span><span class="tag">Revenue Analytics</span><span class="tag">Meta Ads</span><span class="tag">Google Ads</span><span class="tag">GA4</span><span class="tag">Shopify</span><span class="tag">Zid</span><span class="tag">Salla</span><span class="tag">Sheets</span><span class="tag">APIs</span><span class="tag">Webhooks</span><span class="tag">Automation</span><span class="tag">SaaS Product Design</span><span class="tag">Data Modeling</span><span class="tag">Natural-language Analytics</span>
        </div>
      </div>
    </section>

    <section class="section" id="thesis">
      <div class="container">
        <div class="thesis-shell reveal">
          <div class="thesis-intro"><p class="eyebrow">Operating thesis</p><h2>Growth compounds when the loop closes.</h2><p class="lead">Every layer should make the next layer smarter. Insight becomes action; action creates better data; better data improves the next decision.</p></div>
          <div class="system-map" aria-label="Revenue operating system flow">
            <div class="system-node"><b>Signal</b><span>Market, customer, channel, and behavioral inputs.</span><strong>01</strong></div>
            <div class="system-node"><b>Sense</b><span>Unified data, context, patterns, and anomalies.</span><strong>02</strong></div>
            <div class="system-node"><b>Decide</b><span>Diagnosis, prioritization, and recommended action.</span><strong>03</strong></div>
            <div class="system-node"><b>Execute</b><span>Campaigns, sales motion, workflows, and automation.</span><strong>04</strong></div>
            <div class="system-node"><b>Learn</b><span>Measurement, feedback, and reusable commercial IP.</span><strong>05</strong></div>
          </div>
        </div>
      </div>
    </section>

    <section class="section rule" id="markets">
      <div class="container">
        <div class="section-head reveal"><div><p class="eyebrow">Markets</p><h2>Built around business models, not borders.</h2></div><p>The same operating principles adapt to different commercial realities: product-led journeys, complex pipelines, fast-moving commerce, and service businesses.</p></div>
        <div class="markets reveal">
          <article class="market"><span class="flag">B2B / 01</span><h3>SaaS</h3><p>Acquisition, activation, lifecycle, expansion, and product-informed revenue systems.</p></article>
          <article class="market"><span class="flag">B2C / 02</span><h3>Commerce</h3><p>Channel economics, conversion, retention, merchandising signals, and connected customer data.</p></article>
          <article class="market"><span class="flag">SERVICES / 03</span><h3>Expert businesses</h3><p>Offer architecture, demand generation, qualification, sales workflows, and delivery feedback loops.</p></article>
          <article class="market"><span class="flag">VENTURES / 04</span><h3>Early-stage</h3><p>Positioning, launch design, signal gathering, and a lightweight commercial operating cadence.</p></article>
          <article class="market"><span class="flag">SCALE / 05</span><h3>Growth-stage</h3><p>Cross-functional alignment, RevOps, data integrity, and automation that reduces operating drag.</p></article>
          <article class="market"><span class="flag">REGION / 06</span><h3>MENA + beyond</h3><p>Commercial systems designed with local platforms, market dynamics, and global ambition in mind.</p></article>
        </div>
      </div>
    </section>

    <section class="section" id="work">
      <div class="container">
        <div class="section-head reveal"><div><p class="eyebrow">Selected work</p><h2>Patterns of work, without the confidential details.</h2></div><p>Representative system-building themes across product, growth, automation, and commercial intelligence.</p></div>
        <div class="work-grid">
          <article class="case featured reveal"><div><span class="case-label">Product architecture</span><h3>Revenue intelligence layer</h3><p>Framing a product that connects fragmented revenue signals, makes performance explainable, and turns analysis into prioritized next actions.</p></div><div class="case-tags"><span>Unified analytics</span><span>Root-cause analysis</span><span>Anomaly detection</span><span>AI recommendations</span></div></article>
          <article class="case narrow reveal"><div><span class="case-label">Operating model</span><h3>Full-funnel system design</h3><p>Mapping the commercial journey from demand through pipeline, conversion, retention, and learning.</p></div><div class="case-tags"><span>Lifecycle</span><span>RevOps</span><span>Measurement</span></div></article>
          <article class="case reveal"><div><span class="case-label">Automation</span><h3>Commercial workflow orchestration</h3><p>Designing connected workflows that reduce manual handoffs, improve data consistency, and make the next best action visible.</p></div><div class="case-tags"><span>APIs</span><span>CRM</span><span>Agents</span><span>Automation</span></div></article>
          <article class="case reveal"><div><span class="case-label">Go-to-market</span><h3>Launch system</h3><p>Bringing positioning, offer, audience, channel, content, sales readiness, and feedback into one coordinated launch motion.</p></div><div class="case-tags"><span>Positioning</span><span>Launch</span><span>GTM</span><span>Learning loop</span></div></article>
        </div>
      </div>
    </section>

    <section class="section rule" id="teaching">
      <div class="container">
        <div class="section-head reveal"><div><p class="eyebrow">Teaching</p><h2>Turning operator knowledge into leverage.</h2></div><p>Frameworks matter when they help someone see the system, make a better decision, and execute with confidence.</p></div>
        <div class="teaching-grid reveal">
          <div class="teaching-main"><h3>Scale With Omar</h3><p>A platform for practical operator education: clearer models for growth, sharper commercial judgment, and a path from scattered tactics to a system that can be managed.</p></div>
          <div class="teaching-side"><h3>Full Stack Funnel Builder</h3><ul><li>Understand the whole customer journey</li><li>Connect channels to commercial outcomes</li><li>Instrument what matters</li><li>Build workflows that compound learning</li></ul></div>
        </div>
      </div>
    </section>

    <section class="section" id="principles">
      <div class="container">
        <div class="section-head reveal"><div><p class="eyebrow">Principles</p><h2>How I approach the work.</h2></div><p>A small set of operating beliefs guides decisions across products, ventures, and client systems.</p></div>
        <div class="principles reveal">
          <article class="principle"><b>Systems over tactics.</b><p>A tactic can create a spike. A system creates repeatability, feedback, and resilience.</p></article>
          <article class="principle"><b>Decisions over dashboards.</b><p>Analytics is useful when it changes what a team understands, prioritizes, or does.</p></article>
          <article class="principle"><b>Context before automation.</b><p>Automating a weak process only makes the weakness run faster.</p></article>
          <article class="principle"><b>Commercial and technical belong together.</b><p>The best solutions respect both business outcomes and implementation reality.</p></article>
          <article class="principle"><b>Clarity creates speed.</b><p>Clear ownership, definitions, and measures remove more friction than another tool.</p></article>
          <article class="principle"><b>Build reusable intelligence.</b><p>Every experiment should leave behind insight, structure, or IP that improves the next one.</p></article>
        </div>
      </div>
    </section>

    <section class="section" id="contact">
      <div class="container">
        <div class="contact-card reveal">
          <p class="eyebrow" style="color:white;justify-content:center">Connect</p>
          <h2>Building the next layer of intelligent revenue operations?</h2>
          <p>Let’s compare notes on growth systems, AI products, automation, and the infrastructure behind better commercial decisions.</p>
          <div class="contact-links">
            <button type="button" data-placeholder="Email address">Email placeholder</button>
            <a href="https://github.com/" target="_blank" rel="noreferrer" aria-label="GitHub placeholder link">GitHub</a>
            <a href="https://www.linkedin.com/" target="_blank" rel="noreferrer" aria-label="LinkedIn placeholder link">LinkedIn</a>
            <button type="button" data-placeholder="Booking link">Book a conversation</button>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer><div class="container footer-grid"><span>© <span id="year"></span> Omar Mohamed</span><span>Strategy × Systems × Intelligence</span></div></footer>
  <div class="toast" id="toast" role="status" aria-live="polite"></div>

  <script>
    const root = document.documentElement;
    const toggle = document.getElementById('themeToggle');
    const icon = document.getElementById('themeIcon');
    const storedTheme = localStorage.getItem('omar-theme');
    const preferredTheme = matchMedia('(prefers-color-scheme: light)').matches ? 'light' : 'dark';
    const setTheme = theme => {
      root.dataset.theme = theme;
      icon.textContent = theme === 'dark' ? '☼' : '☾';
      document.querySelector('meta[name="theme-color"]').content = theme === 'dark' ? '#08101f' : '#f4f6fa';
    };
    setTheme(storedTheme || preferredTheme);
    toggle.addEventListener('click', () => {
      const next = root.dataset.theme === 'dark' ? 'light' : 'dark';
      setTheme(next); localStorage.setItem('omar-theme', next);
    });

    const menuToggle = document.getElementById('menuToggle');
    const navLinks = document.getElementById('navLinks');
    menuToggle.addEventListener('click', () => {
      const open = navLinks.classList.toggle('open');
      menuToggle.setAttribute('aria-expanded', open); menuToggle.textContent = open ? '×' : '☰';
    });
    navLinks.querySelectorAll('a').forEach(link => link.addEventListener('click', () => {
      navLinks.classList.remove('open'); menuToggle.setAttribute('aria-expanded', 'false'); menuToggle.textContent = '☰';
    }));

    const navShell = document.getElementById('navShell');
    addEventListener('scroll', () => navShell.classList.toggle('scrolled', scrollY > 18), { passive: true });

    const reduced = matchMedia('(prefers-reduced-motion: reduce)').matches;
    if (!reduced && 'IntersectionObserver' in window) {
      const observer = new IntersectionObserver(entries => entries.forEach(entry => {
        if (entry.isIntersecting) { entry.target.classList.add('visible'); observer.unobserve(entry.target); }
      }), { threshold: .12 });
      document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
    } else document.querySelectorAll('.reveal').forEach(el => el.classList.add('visible'));

    const toast = document.getElementById('toast');
    let toastTimer;
    document.querySelectorAll('[data-placeholder]').forEach(button => button.addEventListener('click', () => {
      toast.textContent = `${button.dataset.placeholder} is ready for your real URL.`;
      toast.classList.add('show'); clearTimeout(toastTimer);
      toastTimer = setTimeout(() => toast.classList.remove('show'), 3000);
    }));
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
