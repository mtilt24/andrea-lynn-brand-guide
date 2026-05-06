<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Andrea Lynn — Brand Guide</title>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --linen:       #F2EDE4;
      --linen-alt:   #EAE4DA;
      --linen-deep:  #E0D8CC;
      --charcoal:    #2C2825;
      --gold:        #C49A3C;
      --gold-dark:   #A07B28;
      --sage:        #7A8C6E;
      --taupe:       #5C5650;
      --warm-white:  #FDFAF6;
      --near-black:  #1C1714;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }

    body {
      background: var(--linen);
      color: var(--taupe);
      font-family: 'Jost', sans-serif;
      font-size: 15px;
      line-height: 1.85;
    }

    /* ── SIDEBAR NAV ── */
    .sidebar {
      position: fixed;
      top: 0; left: 0; bottom: 0;
      width: 220px;
      background: var(--near-black);
      padding: 48px 0;
      z-index: 50;
      display: flex;
      flex-direction: column;
    }
    .sidebar-logo {
      padding: 0 32px 40px;
      border-bottom: 1px solid rgba(255,255,255,0.07);
      margin-bottom: 32px;
    }
    .sidebar-logo h1 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      font-weight: 400;
      color: var(--warm-white);
      line-height: 1.2;
    }
    .sidebar-logo h1 em { font-style: italic; color: var(--gold); }
    .sidebar-logo p {
      font-size: 9px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: rgba(253,250,246,0.35);
      margin-top: 6px;
    }
    .sidebar nav { flex: 1; padding: 0 24px; }
    .sidebar nav a {
      display: block;
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: rgba(253,250,246,0.4);
      text-decoration: none;
      padding: 10px 8px;
      border-left: 2px solid transparent;
      transition: color 0.2s, border-color 0.2s;
    }
    .sidebar nav a:hover,
    .sidebar nav a.active {
      color: var(--gold);
      border-left-color: var(--gold);
    }
    .sidebar-version {
      padding: 24px 32px 0;
      border-top: 1px solid rgba(255,255,255,0.07);
      font-size: 10px;
      color: rgba(253,250,246,0.2);
      letter-spacing: 1px;
    }

    /* ── MAIN CONTENT ── */
    .main {
      margin-left: 220px;
    }

    /* ── COVER ── */
    .cover {
      min-height: 100vh;
      background: var(--charcoal);
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      padding: 80px;
      position: relative;
      overflow: hidden;
    }
    .cover::before {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(ellipse at 80% 20%, rgba(196,154,60,0.12) 0%, transparent 60%);
    }
    .cover-watermark {
      position: absolute;
      top: 50%;
      right: -40px;
      transform: translateY(-50%);
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(180px, 20vw, 320px);
      font-weight: 300;
      font-style: italic;
      color: rgba(255,255,255,0.03);
      line-height: 1;
      white-space: nowrap;
      pointer-events: none;
      user-select: none;
    }
    .cover-eyebrow {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 4px;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 24px;
      display: flex;
      align-items: center;
      gap: 16px;
    }
    .cover-eyebrow::before {
      content: '';
      display: inline-block;
      width: 40px;
      height: 1px;
      background: var(--gold);
    }
    .cover h2 {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(52px, 8vw, 110px);
      font-weight: 300;
      color: var(--warm-white);
      line-height: 0.95;
      margin-bottom: 40px;
    }
    .cover h2 em { font-style: italic; color: var(--gold); }
    .cover-meta {
      display: flex;
      align-items: center;
      gap: 48px;
      border-top: 1px solid rgba(255,255,255,0.1);
      padding-top: 32px;
    }
    .cover-meta-item p:first-child {
      font-size: 9px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: rgba(253,250,246,0.35);
      margin-bottom: 4px;
    }
    .cover-meta-item p:last-child {
      font-size: 13px;
      color: rgba(253,250,246,0.7);
    }

    /* ── SECTION SHELL ── */
    .section {
      padding: 100px 80px;
      border-bottom: 1px solid var(--linen-deep);
    }
    .section:nth-child(even) { background: var(--linen-alt); }
    .section:nth-child(odd)  { background: var(--linen); }

    .section-header {
      display: flex;
      align-items: flex-start;
      gap: 48px;
      margin-bottom: 64px;
    }
    .section-num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 80px;
      font-weight: 300;
      color: var(--linen-deep);
      line-height: 0.9;
      flex-shrink: 0;
      margin-top: -8px;
    }
    .section-title-block .eyebrow {
      font-size: 10px;
      font-weight: 500;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--gold);
      display: block;
      margin-bottom: 12px;
    }
    .section-title-block h2 {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(32px, 4vw, 52px);
      font-weight: 400;
      color: var(--charcoal);
      line-height: 1.05;
    }
    .section-title-block h2 em { font-style: italic; }

    /* ── COLOUR PALETTE ── */
    .palette-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 2px;
      background: var(--linen-deep);
      margin-bottom: 48px;
    }
    .swatch {
      display: flex;
      flex-direction: column;
    }
    .swatch-color {
      height: 140px;
    }
    .swatch-info {
      background: var(--warm-white);
      padding: 16px;
    }
    .swatch-name {
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: var(--charcoal);
      margin-bottom: 4px;
    }
    .swatch-hex {
      font-family: 'Cormorant Garamond', serif;
      font-size: 16px;
      color: var(--taupe);
      margin-bottom: 6px;
    }
    .swatch-use {
      font-size: 10px;
      color: rgba(92,86,80,0.6);
      line-height: 1.5;
      letter-spacing: 0.3px;
    }
    .palette-row2 {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 2px;
      background: var(--linen-deep);
    }

    /* ── USAGE RULES ── */
    .usage-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2px;
      background: var(--linen-deep);
      margin-top: 40px;
    }
    .usage-card {
      background: var(--warm-white);
      padding: 36px;
    }
    .usage-card h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      font-weight: 400;
      color: var(--charcoal);
      margin-bottom: 16px;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .usage-card h4 .tag {
      font-family: 'Jost', sans-serif;
      font-size: 9px;
      letter-spacing: 2px;
      text-transform: uppercase;
      padding: 4px 10px;
      border-radius: 0;
    }
    .tag-do   { background: rgba(122,140,110,0.15); color: var(--sage); }
    .tag-dont { background: rgba(180,80,60,0.08);   color: #a04030; }
    .usage-card ul { list-style: none; }
    .usage-card ul li {
      font-size: 13px;
      color: var(--taupe);
      padding: 10px 0;
      border-bottom: 1px solid var(--linen-deep);
      display: flex;
      align-items: flex-start;
      gap: 10px;
      line-height: 1.55;
    }
    .usage-card ul li:last-child { border-bottom: none; }
    .li-icon { font-size: 12px; margin-top: 2px; flex-shrink: 0; }
    .li-icon.yes { color: var(--sage); }
    .li-icon.no  { color: #a04030; }

    /* ── TYPOGRAPHY ── */
    .type-specimen {
      background: var(--warm-white);
      border: 1px solid var(--linen-deep);
      margin-bottom: 32px;
      overflow: hidden;
    }
    .type-label {
      background: var(--linen-alt);
      padding: 14px 28px;
      border-bottom: 1px solid var(--linen-deep);
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .type-label-name {
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--charcoal);
    }
    .type-label-spec {
      font-size: 11px;
      color: rgba(92,86,80,0.5);
    }
    .type-preview { padding: 36px 28px; }
    .type-meta {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 0;
      background: var(--linen-deep);
      border-top: 1px solid var(--linen-deep);
    }
    .type-meta-item {
      background: var(--warm-white);
      padding: 14px 20px;
      border-right: 1px solid var(--linen-deep);
    }
    .type-meta-item:last-child { border-right: none; }
    .type-meta-item p:first-child {
      font-size: 9px;
      letter-spacing: 2.5px;
      text-transform: uppercase;
      color: rgba(92,86,80,0.45);
      margin-bottom: 4px;
    }
    .type-meta-item p:last-child {
      font-size: 12px;
      color: var(--charcoal);
      font-weight: 500;
    }

    /* ── BRAND VOICE ── */
    .voice-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
      margin-bottom: 48px;
    }
    .voice-card {
      background: var(--warm-white);
      border: 1px solid var(--linen-deep);
      padding: 36px;
      position: relative;
    }
    .voice-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 3px;
      background: var(--gold);
    }
    .voice-card h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 24px;
      font-weight: 400;
      color: var(--charcoal);
      margin-bottom: 16px;
    }
    .voice-card p {
      font-size: 14px;
      color: var(--taupe);
      line-height: 1.8;
    }

    .words-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2px;
      background: var(--linen-deep);
      margin-bottom: 48px;
    }
    .words-card {
      background: var(--warm-white);
      padding: 36px;
    }
    .words-card h4 {
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 3px;
      text-transform: uppercase;
      margin-bottom: 24px;
    }
    .words-card.love h4 { color: var(--sage); }
    .words-card.never h4 { color: #a04030; }
    .words-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }
    .word-tag {
      font-family: 'Cormorant Garamond', serif;
      font-size: 18px;
      font-weight: 400;
      font-style: italic;
      padding: 6px 16px;
      border: 1px solid;
    }
    .love .word-tag {
      color: var(--charcoal);
      border-color: var(--linen-deep);
      background: var(--linen);
    }
    .never .word-tag {
      color: rgba(92,86,80,0.4);
      border-color: var(--linen-deep);
      background: var(--linen);
      text-decoration: line-through;
      text-decoration-color: rgba(160,64,48,0.4);
    }

    /* ── COPY EXAMPLES ── */
    .copy-example {
      background: var(--warm-white);
      border: 1px solid var(--linen-deep);
      margin-bottom: 24px;
      overflow: hidden;
    }
    .copy-example-header {
      background: var(--linen-alt);
      padding: 12px 24px;
      border-bottom: 1px solid var(--linen-deep);
      font-size: 9px;
      font-weight: 600;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--taupe);
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .copy-example-header .dot {
      width: 8px; height: 8px;
      border-radius: 50%;
      background: var(--gold);
    }
    .copy-example-body {
      padding: 32px;
    }
    .copy-example-body p {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      font-weight: 300;
      font-style: italic;
      color: var(--charcoal);
      line-height: 1.55;
    }

    /* ── LOGO ── */
    .logo-section-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2px;
      background: var(--linen-deep);
      margin-bottom: 40px;
    }
    .logo-card {
      padding: 60px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 8px;
      min-height: 200px;
    }
    .logo-card.light { background: var(--warm-white); }
    .logo-card.dark  { background: var(--charcoal); }
    .logo-card.gold  { background: var(--gold); }
    .logo-card.linen { background: var(--linen); }
    .logo-lockup {
      font-family: 'Cormorant Garamond', serif;
      font-size: 36px;
      font-weight: 400;
      line-height: 1;
      text-align: center;
    }
    .logo-lockup em { font-style: italic; }
    .logo-lockup .sub {
      display: block;
      font-family: 'Jost', sans-serif;
      font-size: 9px;
      font-weight: 500;
      letter-spacing: 4px;
      text-transform: uppercase;
      margin-top: 10px;
    }
    .logo-card-label {
      font-size: 9px;
      letter-spacing: 2px;
      text-transform: uppercase;
      opacity: 0.4;
      margin-top: 16px;
    }

    /* ── IMAGERY ── */
    .imagery-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2px;
      background: var(--linen-deep);
      margin-bottom: 40px;
    }
    .imagery-card {
      aspect-ratio: 3/4;
      position: relative;
      overflow: hidden;
      display: flex;
      align-items: flex-end;
      padding: 20px;
    }
    .imagery-card .img-label {
      font-size: 10px;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: rgba(255,255,255,0.7);
      background: rgba(0,0,0,0.3);
      padding: 6px 12px;
      backdrop-filter: blur(4px);
    }

    /* ── BRAND PILLARS ── */
    .pillars-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 2px;
      background: var(--linen-deep);
    }
    .pillar-card {
      background: var(--warm-white);
      padding: 40px 32px;
      border-top: 3px solid var(--gold);
    }
    .pillar-num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 48px;
      font-weight: 300;
      color: var(--linen-deep);
      line-height: 1;
      margin-bottom: 16px;
    }
    .pillar-card h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 22px;
      font-weight: 400;
      font-style: italic;
      color: var(--charcoal);
      margin-bottom: 12px;
    }
    .pillar-card p {
      font-size: 13px;
      color: var(--taupe);
      line-height: 1.7;
    }

    /* ── AUDIENCE ── */
    .audience-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
    }
    .audience-card {
      background: var(--warm-white);
      border: 1px solid var(--linen-deep);
      padding: 40px;
    }
    .audience-card h4 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 24px;
      font-weight: 400;
      color: var(--charcoal);
      margin-bottom: 20px;
      padding-bottom: 16px;
      border-bottom: 1px solid var(--linen-deep);
    }
    .audience-card h4 em { font-style: italic; color: var(--gold); }
    .audience-card ul { list-style: none; }
    .audience-card ul li {
      font-size: 13px;
      color: var(--taupe);
      padding: 9px 0;
      border-bottom: 1px solid var(--linen-deep);
      display: flex;
      align-items: flex-start;
      gap: 10px;
      line-height: 1.5;
    }
    .audience-card ul li:last-child { border-bottom: none; }

    /* ── BUTTONS & UI ── */
    .ui-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
      margin-bottom: 40px;
    }
    .ui-card {
      background: var(--warm-white);
      border: 1px solid var(--linen-deep);
      padding: 36px;
    }
    .ui-card h4 {
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--taupe);
      margin-bottom: 24px;
    }
    .btn-row {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .demo-btn {
      display: inline-block;
      font-family: 'Jost', sans-serif;
      font-size: 10px;
      font-weight: 600;
      letter-spacing: 2.5px;
      text-transform: uppercase;
      padding: 15px 32px;
      cursor: default;
      width: fit-content;
    }
    .demo-btn-primary   { background: var(--gold);     color: var(--warm-white); }
    .demo-btn-outline   { border: 1px solid var(--charcoal); color: var(--charcoal); }
    .demo-btn-ghost     { border: 1px solid rgba(44,40,37,0.3); color: var(--taupe); }
    .demo-btn-ghost-wht { border: 1px solid rgba(253,250,246,0.4); color: var(--warm-white); background: var(--charcoal); }
    .btn-spec {
      font-size: 11px;
      color: rgba(92,86,80,0.5);
      margin-top: 6px;
      letter-spacing: 0.3px;
    }
    .btn-demo-row {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    /* ── FOOTER ── */
    .guide-footer {
      background: var(--near-black);
      padding: 60px 80px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .guide-footer h3 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 28px;
      font-weight: 400;
      color: var(--warm-white);
    }
    .guide-footer h3 em { font-style: italic; color: var(--gold); }
    .guide-footer p {
      font-size: 11px;
      color: rgba(253,250,246,0.3);
      letter-spacing: 1px;
      margin-top: 6px;
    }
    .guide-footer .footer-right {
      text-align: right;
      font-size: 11px;
      color: rgba(253,250,246,0.25);
      letter-spacing: 1px;
      line-height: 2;
    }

    @media (max-width: 900px) {
      .sidebar { display: none; }
      .main { margin-left: 0; }
      .cover { padding: 60px 40px; }
      .section { padding: 72px 40px; }
      .palette-grid { grid-template-columns: repeat(3, 1fr); }
      .palette-row2 { grid-template-columns: repeat(2, 1fr); }
      .voice-grid, .words-grid, .usage-grid,
      .logo-section-grid, .ui-grid, .audience-grid { grid-template-columns: 1fr; }
      .pillars-grid { grid-template-columns: 1fr 1fr; }
      .imagery-grid { grid-template-columns: 1fr 1fr; }
      .type-meta { grid-template-columns: 1fr 1fr; }
      .guide-footer { flex-direction: column; gap: 24px; text-align: center; }
      .guide-footer .footer-right { text-align: center; }
    }
  </style>
</head>
<body>

<!-- ── SIDEBAR ── -->
<div class="sidebar">
  <div class="sidebar-logo">
    <svg width="60" height="40" viewBox="0 0 120 80" fill="none" xmlns="http://www.w3.org/2000/svg" style="margin-bottom:10px;">
      <circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/>
      <circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/>
      <circle cx="60" cy="40" r="3.2" fill="#C49A3C"/>
    </svg>
    <h1>Andrea <em>Lynn</em></h1>
    <p>Brand Guide</p>
  </div>
  <nav>
    <a href="#cover">Overview</a>
    <a href="#pillars">Brand Pillars</a>
    <a href="#audience">Audience</a>
    <a href="#colors">Color Palette</a>
    <a href="#typography">Typography</a>
    <a href="#logo">Logo</a>
    <a href="#voice">Brand Voice</a>
    <a href="#imagery">Imagery</a>
    <a href="#ui">Buttons & UI</a>
  </nav>
  <div class="sidebar-version">
    <p>Version 1.0 · 2025</p>
  </div>
</div>

<!-- ── MAIN ── -->
<div class="main">

  <!-- COVER -->
  <section class="cover" id="cover">
    <div class="cover-watermark">Lynn</div>
    <div class="cover-eyebrow">Brand Identity Guide</div>
    <h2>Andrea<br/><em>Lynn</em></h2>
    <div class="cover-meta">
      <div class="cover-meta-item">
        <p>Brand</p>
        <p>Andrea Lynn</p>
      </div>
      <div class="cover-meta-item">
        <p>Version</p>
        <p>1.0 — 2025</p>
      </div>
      <div class="cover-meta-item">
        <p>Category</p>
        <p>Transformational Coaching</p>
      </div>
      <div class="cover-meta-item">
        <p>Audience</p>
        <p>Midlife Women in Transition</p>
      </div>
    </div>
  </section>

  <!-- BRAND PILLARS -->
  <section class="section" id="pillars">
    <div class="section-header">
      <div class="section-num">01</div>
      <div class="section-title-block">
        <span class="eyebrow">Foundation</span>
        <h2>Brand <em>Pillars</em></h2>
      </div>
    </div>
    <div class="pillars-grid">
      <div class="pillar-card">
        <div class="pillar-num">01</div>
        <h4>Unlimited Potential</h4>
        <p>Every woman who comes to this work carries an unlived life inside her. The brand holds that possibility with total conviction.</p>
      </div>
      <div class="pillar-card">
        <div class="pillar-num">02</div>
        <h4>Connection</h4>
        <p>To self, to body, to others. This work restores the thread that gets lost in the noise of a life built for everyone else.</p>
      </div>
      <div class="pillar-card">
        <div class="pillar-num">03</div>
        <h4>Depth</h4>
        <p>Nothing surface. Nothing performative. This is real, felt, embodied transformation — not inspiration content.</p>
      </div>
      <div class="pillar-card">
        <div class="pillar-num">04</div>
        <h4>Your Body Is the Portal</h4>
        <p>The body holds the answers. Somatic wisdom is the through-line of everything — the method, the message, the medicine.</p>
      </div>
    </div>

    <!-- Brand in 3 words -->
    <div style="margin-top: 48px; background: var(--charcoal); padding: 56px; display: grid; grid-template-columns: repeat(3, 1fr); text-align: center;">
      <div style="border-right: 1px solid rgba(255,255,255,0.08); padding: 0 40px;">
        <p style="font-family:'Cormorant Garamond',serif; font-size:42px; font-weight:300; font-style:italic; color:var(--gold);">Mystical</p>
        <p style="font-size:10px; letter-spacing:2px; text-transform:uppercase; color:rgba(253,250,246,0.35); margin-top:8px;">Core Brand Word</p>
      </div>
      <div style="border-right: 1px solid rgba(255,255,255,0.08); padding: 0 40px;">
        <p style="font-family:'Cormorant Garamond',serif; font-size:42px; font-weight:300; font-style:italic; color:var(--gold);">Grounded</p>
        <p style="font-size:10px; letter-spacing:2px; text-transform:uppercase; color:rgba(253,250,246,0.35); margin-top:8px;">Core Brand Word</p>
      </div>
      <div style="padding: 0 40px;">
        <p style="font-family:'Cormorant Garamond',serif; font-size:42px; font-weight:300; font-style:italic; color:var(--gold);">Evolutionary</p>
        <p style="font-size:10px; letter-spacing:2px; text-transform:uppercase; color:rgba(253,250,246,0.35); margin-top:8px;">Core Brand Word</p>
      </div>
    </div>
  </section>

  <!-- AUDIENCE -->
  <section class="section" id="audience">
    <div class="section-header">
      <div class="section-num">02</div>
      <div class="section-title-block">
        <span class="eyebrow">Who We Speak To</span>
        <h2>The <em>Audience</em></h2>
      </div>
    </div>
    <div class="audience-grid">
      <div class="audience-card">
        <h4>She <em>is</em> our woman</h4>
        <ul>
          <li><span class="li-icon yes">✦</span> Midlife women in transition — career, relationship, identity, or spiritual</li>
          <li><span class="li-icon yes">✦</span> Feels stuck, stagnant, or like she's outgrown her life</li>
          <li><span class="li-icon yes">✦</span> Knows she's meant for more and is finally ready to claim it</li>
          <li><span class="li-icon yes">✦</span> Open to somatic, spiritual, and embodied approaches</li>
          <li><span class="li-icon yes">✦</span> Wants expansion, aliveness, depth, and real transformation</li>
          <li><span class="li-icon yes">✦</span> Values trust and personal connection over slick marketing</li>
          <li><span class="li-icon yes">✦</span> Willing to take responsibility for her own evolution</li>
        </ul>
      </div>
      <div class="audience-card">
        <h4>She is <em>not</em> our woman</h4>
        <ul>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Closed off spiritually or dismissive of embodied work</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Committed to a victim identity</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Unwilling to change or take action</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Looking for a quick fix or surface-level inspiration</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Not open to the body as a source of wisdom</li>
        </ul>
        <div style="margin-top:24px; padding:20px; background:var(--linen); border-left:3px solid var(--gold);">
          <p style="font-family:'Cormorant Garamond',serif; font-size:18px; font-style:italic; color:var(--charcoal); line-height:1.5;">
            "Write to the woman who is one decision away from everything changing — not the one still deciding whether change is possible."
          </p>
        </div>
      </div>
    </div>

    <!-- Common objections -->
    <div style="margin-top:32px; background:var(--warm-white); border:1px solid var(--linen-deep); padding:40px;">
      <p style="font-size:10px; font-weight:600; letter-spacing:3px; text-transform:uppercase; color:var(--gold); margin-bottom:24px;">Common Objections to Address in Copy</p>
      <div style="display:grid; grid-template-columns:repeat(3,1fr); gap:2px; background:var(--linen-deep);">
        <div style="background:var(--linen); padding:24px;">
          <p style="font-family:'Cormorant Garamond',serif; font-size:20px; font-style:italic; color:var(--charcoal); margin-bottom:8px;">"It's too expensive."</p>
          <p style="font-size:12px; color:var(--taupe); line-height:1.7;">Address with payment plans, ROI of transformation, and cost of staying stuck.</p>
        </div>
        <div style="background:var(--linen); padding:24px;">
          <p style="font-family:'Cormorant Garamond',serif; font-size:20px; font-style:italic; color:var(--charcoal); margin-bottom:8px;">"I don't have time."</p>
          <p style="font-size:12px; color:var(--taupe); line-height:1.7;">Address with commitment level clarity, flexible formats, and the cost of waiting.</p>
        </div>
        <div style="background:var(--linen); padding:24px;">
          <p style="font-family:'Cormorant Garamond',serif; font-size:20px; font-style:italic; color:var(--charcoal); margin-bottom:8px;">"I need to check with my husband."</p>
          <p style="font-size:12px; color:var(--taupe); line-height:1.7;">Address by centering her own authority and the discovery call as a no-pressure first step.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- COLOURS -->
  <section class="section" id="colors">
    <div class="section-header">
      <div class="section-num">03</div>
      <div class="section-title-block">
        <span class="eyebrow">Visual Identity</span>
        <h2>Color <em>Palette</em></h2>
      </div>
    </div>

    <div class="palette-grid">
      <div class="swatch">
        <div class="swatch-color" style="background:#F2EDE4;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Linen</p>
          <p class="swatch-hex">#F2EDE4</p>
          <p class="swatch-use">Primary background. The main canvas. Warm, not stark.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#EAE4DA;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Linen Alt</p>
          <p class="swatch-hex">#EAE4DA</p>
          <p class="swatch-use">Section breaks. Creates rhythm between sections.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#E0D8CC;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Linen Deep</p>
          <p class="swatch-hex">#E0D8CC</p>
          <p class="swatch-use">Borders, dividers, list separators.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#C49A3C;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Amber Gold</p>
          <p class="swatch-hex">#C49A3C</p>
          <p class="swatch-use">The soul color. CTAs, eyebrows, accents. Warm, rich, honey-toned.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#A07B28;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Gold Dark</p>
          <p class="swatch-hex">#A07B28</p>
          <p class="swatch-use">Hover states only. Never used as a primary color.</p>
        </div>
      </div>
    </div>

    <div class="palette-row2" style="margin-top:2px;">
      <div class="swatch">
        <div class="swatch-color" style="background:#2C2825;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Deep Charcoal</p>
          <p class="swatch-hex">#2C2825</p>
          <p class="swatch-use">Headlines, nav, dark sections. Warmer than pure black.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#5C5650;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Warm Taupe</p>
          <p class="swatch-hex">#5C5650</p>
          <p class="swatch-use">All body text. Warm enough to feel human, dark enough to read.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#7A8C6E; "></div>
        <div class="swatch-info">
          <p class="swatch-name">Sage</p>
          <p class="swatch-hex">#7A8C6E</p>
          <p class="swatch-use">Accent only. Eyebrow text and left-border accents. Never a fill.</p>
        </div>
      </div>
      <div class="swatch">
        <div class="swatch-color" style="background:#1C1714;"></div>
        <div class="swatch-info">
          <p class="swatch-name">Near Black</p>
          <p class="swatch-hex">#1C1714;</p>
          <p class="swatch-use">Footer background only. Warmer than pure black.</p>
        </div>
      </div>
    </div>

    <div class="usage-grid">
      <div class="usage-card">
        <h4>Color <span class="tag tag-do">Do</span></h4>
        <ul>
          <li><span class="li-icon yes">✦</span> Use Amber Gold sparingly as a true accent — it loses its power if overused</li>
          <li><span class="li-icon yes">✦</span> Let vibrant photography provide the color, not the backgrounds</li>
          <li><span class="li-icon yes">✦</span> Use Linen and Linen Alt to create natural section rhythm</li>
          <li><span class="li-icon yes">✦</span> Pair deep charcoal with warm white for high contrast text sections</li>
          <li><span class="li-icon yes">✦</span> Use Sage as a single accent detail — never as a fill color</li>
        </ul>
      </div>
      <div class="usage-card">
        <h4>Color <span class="tag tag-dont">Don't</span></h4>
        <ul>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never use pure black (#000000) or pure white (#FFFFFF)</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never use the gold as a large fill or background area</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never use Sage as a section background</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never add new colors outside this palette</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never use Gold Dark (#A07B28) except on button hover states</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- TYPOGRAPHY -->
  <section class="section" id="typography">
    <div class="section-header">
      <div class="section-num">04</div>
      <div class="section-title-block">
        <span class="eyebrow">Visual Identity</span>
        <h2>Typography <em>System</em></h2>
      </div>
    </div>

    <!-- Display -->
    <div class="type-specimen">
      <div class="type-label">
        <span class="type-label-name">Display — Cormorant Garamond</span>
        <span class="type-label-spec">Headlines, pull quotes, brand name</span>
      </div>
      <div class="type-preview">
        <p style="font-family:'Cormorant Garamond',serif; font-size:72px; font-weight:400; color:var(--charcoal); line-height:1.0; margin-bottom:16px;">You Were Not Made<br/>to Stay <em style="font-style:italic; color:var(--gold);">Small.</em></p>
        <p style="font-family:'Cormorant Garamond',serif; font-size:32px; font-weight:400; font-style:italic; color:var(--taupe);">Abcdefghijklmnopqrstuvwxyz 0123456789</p>
      </div>
      <div class="type-meta">
        <div class="type-meta-item"><p>Family</p><p>Cormorant Garamond</p></div>
        <div class="type-meta-item"><p>Weight</p><p>400 Regular</p></div>
        <div class="type-meta-item"><p>H1 Size</p><p>42–82px</p></div>
        <div class="type-meta-item"><p>Line Height</p><p>1.0</p></div>
      </div>
    </div>

    <!-- H2 -->
    <div class="type-specimen">
      <div class="type-label">
        <span class="type-label-name">H2 — Section Headlines</span>
        <span class="type-label-spec">Cormorant Garamond 400</span>
      </div>
      <div class="type-preview">
        <p style="font-family:'Cormorant Garamond',serif; font-size:48px; font-weight:400; color:var(--charcoal); line-height:1.08; margin-bottom:12px;">Women who leapt.<br/><em style="font-style:italic;">Women who landed.</em></p>
      </div>
      <div class="type-meta">
        <div class="type-meta-item"><p>Size</p><p>30–54px</p></div>
        <div class="type-meta-item"><p>Weight</p><p>400 Regular</p></div>
        <div class="type-meta-item"><p>Line Height</p><p>1.08</p></div>
        <div class="type-meta-item"><p>Italic</p><p>Used for emphasis</p></div>
      </div>
    </div>

    <!-- Body -->
    <div class="type-specimen">
      <div class="type-label">
        <span class="type-label-name">Body — Jost</span>
        <span class="type-label-spec">All paragraph copy, UI text, navigation</span>
      </div>
      <div class="type-preview">
        <p style="font-family:'Jost',sans-serif; font-size:15px; font-weight:400; color:var(--taupe); line-height:1.85; max-width:600px; margin-bottom:20px;">Maybe your marriage is shifting. Maybe your career no longer fits. Maybe something in you is waking up that you can't quite name — but you can feel it. I've been guiding women through exactly this for over 15 years.</p>
        <div style="display:flex; gap:40px; flex-wrap:wrap;">
          <div>
            <p style="font-family:'Jost',sans-serif; font-size:10px; font-weight:500; letter-spacing:3px; text-transform:uppercase; color:var(--gold);">Eyebrow Label · 10px · 500 · LS 3px</p>
          </div>
          <div>
            <p style="font-family:'Jost',sans-serif; font-size:11px; font-weight:400; letter-spacing:2px; text-transform:uppercase; color:var(--charcoal);">Nav Link · 11px · 400 · LS 2px</p>
          </div>
          <div>
            <p style="font-family:'Jost',sans-serif; font-size:10px; font-weight:600; letter-spacing:2.5px; text-transform:uppercase; color:var(--warm-white); background:var(--gold); padding:10px 20px;">CTA Button · 10px · 600 · LS 2.5px</p>
          </div>
        </div>
      </div>
      <div class="type-meta">
        <div class="type-meta-item"><p>Family</p><p>Jost</p></div>
        <div class="type-meta-item"><p>Body Size</p><p>15px</p></div>
        <div class="type-meta-item"><p>Weight</p><p>400 Regular</p></div>
        <div class="type-meta-item"><p>Line Height</p><p>1.85</p></div>
      </div>
    </div>
  </section>

  <!-- LOGO -->
  <section class="section" id="logo">
    <div class="section-header">
      <div class="section-num">05</div>
      <div class="section-title-block">
        <span class="eyebrow">Visual Identity</span>
        <h2>Logo <em>Usage</em></h2>
      </div>
    </div>

    <p style="font-size:13px; color:var(--taupe); max-width:640px; margin-bottom:12px; line-height:1.8;">The logo mark is a <strong style="color:var(--charcoal);">Vesica Piscis</strong> — two overlapping circles with a gold center dot. This sacred geometry represents the intersection of two worlds, the divine feminine, and the portal between realms. The wordmark "ANDREA LYNN" sits beneath in spaced caps.</p>
    <p style="font-size:13px; color:var(--taupe); max-width:640px; margin-bottom:40px; line-height:1.8;">Symbol: <strong style="color:var(--charcoal);">Amber Gold #C49A3C</strong> &nbsp;·&nbsp; Wordmark on light: <strong style="color:var(--charcoal);">Deep Charcoal #2C2825</strong> &nbsp;·&nbsp; Wordmark on dark: <strong style="color:var(--charcoal);">Warm White #FDFAF6</strong></p>

    <!-- SVG LOGO MARK -->
    <style>
      .logo-display { display:flex; flex-direction:column; align-items:center; justify-content:center; gap:18px; }
      .logo-wordmark-text { font-family:'Cormorant Garamond',serif; font-size:17px; font-weight:400; letter-spacing:7px; text-transform:uppercase; }
    </style>

    <div class="logo-section-grid">
      <div class="logo-card linen">
        <div class="logo-display">
          <svg width="120" height="80" viewBox="0 0 120 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="60" cy="40" r="3.2" fill="#C49A3C"/>
          </svg>
          <span class="logo-wordmark-text" style="color:#2C2825;">Andrea Lynn</span>
        </div>
        <p class="logo-card-label" style="color:var(--taupe); margin-top:20px;">On Linen — Primary Use</p>
      </div>
      <div class="logo-card light">
        <div class="logo-display">
          <svg width="120" height="80" viewBox="0 0 120 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="60" cy="40" r="3.2" fill="#C49A3C"/>
          </svg>
          <span class="logo-wordmark-text" style="color:#2C2825;">Andrea Lynn</span>
        </div>
        <p class="logo-card-label" style="color:var(--taupe); margin-top:20px;">On Warm White</p>
      </div>
      <div class="logo-card dark">
        <div class="logo-display">
          <svg width="120" height="80" viewBox="0 0 120 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="60" cy="40" r="3.2" fill="#C49A3C"/>
          </svg>
          <span class="logo-wordmark-text" style="color:#FDFAF6;">Andrea Lynn</span>
        </div>
        <p class="logo-card-label" style="color:rgba(253,250,246,0.3); margin-top:20px;">On Dark / Charcoal</p>
      </div>
      <div class="logo-card" style="background:#1C1714;">
        <div class="logo-display">
          <svg width="120" height="80" viewBox="0 0 120 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.1" fill="none"/>
            <circle cx="60" cy="40" r="3.2" fill="#C49A3C"/>
          </svg>
          <span class="logo-wordmark-text" style="color:#FDFAF6;">Andrea Lynn</span>
        </div>
        <p class="logo-card-label" style="color:rgba(253,250,246,0.25); margin-top:20px;">On Near Black / Footer</p>
      </div>
    </div>

    <!-- Symbol only row -->
    <p style="font-size:10px; font-weight:500; letter-spacing:3px; text-transform:uppercase; color:var(--gold); margin:40px 0 16px;">Symbol Only — Submark</p>
    <div style="display:grid; grid-template-columns:repeat(4,1fr); gap:2px; background:var(--linen-deep); margin-bottom:40px;">
      <div style="background:var(--linen); padding:36px; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:12px;">
        <svg width="70" height="48" viewBox="0 0 120 80" fill="none"><circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/><circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/><circle cx="60" cy="40" r="3.2" fill="#C49A3C"/></svg>
        <span style="font-size:9px; letter-spacing:2px; text-transform:uppercase; color:var(--taupe); opacity:0.5;">On Linen</span>
      </div>
      <div style="background:var(--warm-white); padding:36px; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:12px;">
        <svg width="70" height="48" viewBox="0 0 120 80" fill="none"><circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/><circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/><circle cx="60" cy="40" r="3.2" fill="#C49A3C"/></svg>
        <span style="font-size:9px; letter-spacing:2px; text-transform:uppercase; color:var(--taupe); opacity:0.5;">On White</span>
      </div>
      <div style="background:var(--charcoal); padding:36px; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:12px;">
        <svg width="70" height="48" viewBox="0 0 120 80" fill="none"><circle cx="46" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/><circle cx="74" cy="40" r="36" stroke="#C49A3C" stroke-width="1.4" fill="none"/><circle cx="60" cy="40" r="3.2" fill="#C49A3C"/></svg>
        <span style="font-size:9px; letter-spacing:2px; text-transform:uppercase; color:rgba(253,250,246,0.3);">On Dark</span>
      </div>
      <div style="background:var(--near-black); padding:36px; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:12px;">
        <svg width="70" height="48" viewBox="0 0 120 80" fill="none"><circle cx="46" cy="40" r="36" stroke="#FDFAF6" stroke-width="1.4" fill="none"/><circle cx="74" cy="40" r="36" stroke="#FDFAF6" stroke-width="1.4" fill="none"/><circle cx="60" cy="40" r="3.2" fill="#C49A3C"/></svg>
        <span style="font-size:9px; letter-spacing:2px; text-transform:uppercase; color:rgba(253,250,246,0.25);">White Mark</span>
      </div>
    </div>

    <div class="usage-grid">
      <div class="usage-card">
        <h4>Logo <span class="tag tag-do">Do</span></h4>
        <ul>
          <li><span class="li-icon yes">✦</span> Always maintain clear space around the logo equal to the height of the symbol</li>
          <li><span class="li-icon yes">✦</span> Use the gold symbol with charcoal wordmark on all light and linen backgrounds</li>
          <li><span class="li-icon yes">✦</span> Use the gold symbol with warm white wordmark on dark backgrounds</li>
          <li><span class="li-icon yes">✦</span> Use the submark (symbol only) for small contexts like favicons or social avatars</li>
          <li><span class="li-icon yes">✦</span> Scale proportionally — always maintain the symbol-to-wordmark ratio</li>
        </ul>
      </div>
      <div class="usage-card">
        <h4>Logo <span class="tag tag-dont">Don't</span></h4>
        <ul>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never recolor the symbol outside of gold or white</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never place the logo on a busy or patterned background</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never use the logo at a size smaller than 120px wide on screen</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never stretch, compress, or alter the spacing of the mark</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Never place the logo on a gold background — low contrast</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BRAND VOICE -->
  <section class="section" id="voice">
    <div class="section-header">
      <div class="section-num">06</div>
      <div class="section-title-block">
        <span class="eyebrow">Messaging</span>
        <h2>Brand <em>Voice</em></h2>
      </div>
    </div>

    <div class="voice-grid">
      <div class="voice-card">
        <h4>Tone</h4>
        <p>Bold and confident, but never aggressive. Warm and intimate, but never precious. Mystical, but always grounded enough that a first-time visitor understands what she does and how to begin.</p>
      </div>
      <div class="voice-card">
        <h4>Point of View</h4>
        <p>Always first person. "I" not "we." Andrea is the brand. The writing feels like a woman speaking directly to another woman — not a company talking at a customer.</p>
      </div>
      <div class="voice-card">
        <h4>Style</h4>
        <p>Short paragraphs. Intentional line breaks. Simple, vivid sentences. Occasional poetic repetition. Reflective questions. Embodied language — breath, body, nervous system, aliveness, desire, becoming.</p>
      </div>
      <div class="voice-card">
        <h4>Approach</h4>
        <p>Lead with transformation and felt sense, then add structure and clarity. Explain what it is, who it's for, how it works, and what to do next. Balance mystical language with clear, practical outcomes.</p>
      </div>
    </div>

    <div class="words-grid">
      <div class="words-card love">
        <h4>Words &amp; Phrases We Love</h4>
        <div class="words-tags">
          <span class="word-tag">Let's fucking go</span>
          <span class="word-tag">Leap and the net will appear</span>
          <span class="word-tag">Love over fear</span>
          <span class="word-tag">Your body is the portal</span>
          <span class="word-tag">Threshold</span>
          <span class="word-tag">Aliveness</span>
          <span class="word-tag">Becoming</span>
          <span class="word-tag">Devotion</span>
          <span class="word-tag">Embodied</span>
          <span class="word-tag">Sacred</span>
          <span class="word-tag">Unleash</span>
          <span class="word-tag">Expansion</span>
        </div>
      </div>
      <div class="words-card never">
        <h4>Words We Never Use</h4>
        <div class="words-tags">
          <span class="word-tag">It's not possible</span>
          <span class="word-tag">I can't</span>
          <span class="word-tag">Victim</span>
          <span class="word-tag">Just</span>
          <span class="word-tag">Simply</span>
          <span class="word-tag">Transformation journey</span>
          <span class="word-tag">Empower you to</span>
          <span class="word-tag">Unlock your potential</span>
          <span class="word-tag">Hustle</span>
          <span class="word-tag">Girl boss</span>
        </div>
      </div>
    </div>

    <!-- Copy examples -->
    <p style="font-size:10px; font-weight:600; letter-spacing:3px; text-transform:uppercase; color:var(--gold); margin-bottom:20px;">Copy Examples — Voice in Action</p>

    <div class="copy-example">
      <div class="copy-example-header"><div class="dot"></div>Hero Headline</div>
      <div class="copy-example-body">
        <p>You Were Not Made to Stay Small.</p>
      </div>
    </div>
    <div class="copy-example">
      <div class="copy-example-header"><div class="dot"></div>Opening Body Copy</div>
      <div class="copy-example-body">
        <p>"Maybe your marriage is shifting. Maybe your career no longer fits. Maybe something in you is waking up that you can't quite name — but you can feel it.<br/><br/>I've been guiding women through exactly this for over 15 years."</p>
      </div>
    </div>
    <div class="copy-example">
      <div class="copy-example-header"><div class="dot"></div>Call to Action Framing</div>
      <div class="copy-example-body">
        <p>"The question isn't whether you're ready. The question is — how much longer are you willing to wait?"</p>
      </div>
    </div>
  </section>

  <!-- IMAGERY -->
  <section class="section" id="imagery">
    <div class="section-header">
      <div class="section-num">07</div>
      <div class="section-title-block">
        <span class="eyebrow">Visual Identity</span>
        <h2>Imagery <em>Direction</em></h2>
      </div>
    </div>

    <div class="imagery-grid">
      <div class="imagery-card" style="background:linear-gradient(160deg,#c9b99a,#7a6550);">
        <span class="img-label">Embodied Movement</span>
      </div>
      <div class="imagery-card" style="background:linear-gradient(160deg,#b5a070,#5a4030);">
        <span class="img-label">Andrea — Present + Grounded</span>
      </div>
      <div class="imagery-card" style="background:linear-gradient(160deg,#c0b080,#806040);">
        <span class="img-label">Human Connection</span>
      </div>
      <div class="imagery-card" style="background:linear-gradient(180deg,#8a9070,#404530);">
        <span class="img-label">Nature + Earth</span>
      </div>
      <div class="imagery-card" style="background:linear-gradient(160deg,#c8b890,#806040);">
        <span class="img-label">Warmth + Light</span>
      </div>
      <div class="imagery-card" style="background:linear-gradient(160deg,#a09060,#5a3820);">
        <span class="img-label">Sacred Space</span>
      </div>
    </div>

    <div class="usage-grid">
      <div class="usage-card">
        <h4>Imagery <span class="tag tag-do">Do</span></h4>
        <ul>
          <li><span class="li-icon yes">✦</span> Use photography as the main source of color on the site</li>
          <li><span class="li-icon yes">✦</span> Choose images that feel warm, vibrant, alive, and human</li>
          <li><span class="li-icon yes">✦</span> Show real emotion — connection, joy, presence, depth</li>
          <li><span class="li-icon yes">✦</span> Use nature imagery that feels earthy, grounded, and feminine</li>
          <li><span class="li-icon yes">✦</span> Show Andrea — she is the brand, she must be seen</li>
        </ul>
      </div>
      <div class="usage-card">
        <h4>Imagery <span class="tag tag-dont">Don't</span></h4>
        <ul>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> No cold, clinical, or corporate stock photography</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> No flat, disconnected, or overly filtered images</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> No images that feel staged or performative</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> Avoid ultra-dark or ultra-desaturated photography</li>
          <li><span class="li-icon no" style="color:#a04030;">✕</span> No imagery that feels "wellness generic" or clichéd</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- BUTTONS & UI -->
  <section class="section" id="ui">
    <div class="section-header">
      <div class="section-num">08</div>
      <div class="section-title-block">
        <span class="eyebrow">UI Components</span>
        <h2>Buttons <em>&amp; UI</em></h2>
      </div>
    </div>

    <div class="ui-grid">
      <div class="ui-card">
        <h4>Button Styles</h4>
        <div class="btn-demo-row">
          <div>
            <div class="demo-btn demo-btn-primary">Book a Free Call</div>
            <p class="btn-spec">Primary — Gold fill. Main CTA. Used once per section maximum.</p>
          </div>
          <div>
            <div class="demo-btn demo-btn-outline">Explore the Work</div>
            <p class="btn-spec">Outline — Charcoal border. Secondary CTA on light backgrounds.</p>
          </div>
          <div>
            <div class="demo-btn demo-btn-ghost-wht">Read More Stories</div>
            <p class="btn-spec">Ghost — White border on dark sections only.</p>
          </div>
        </div>
      </div>
      <div class="ui-card">
        <h4>Text Links &amp; Labels</h4>
        <div class="btn-demo-row">
          <div>
            <p style="font-family:'Jost',sans-serif; font-size:11px; font-weight:500; letter-spacing:2px; text-transform:uppercase; color:var(--gold); border-bottom:1px solid var(--gold); display:inline-block; padding-bottom:2px;">Full Details →</p>
            <p class="btn-spec">Text link — Gold with underline. Used alongside a primary CTA.</p>
          </div>
          <div>
            <p style="font-size:10px; font-weight:500; letter-spacing:3px; text-transform:uppercase; color:var(--gold);">Eyebrow Label</p>
            <p class="btn-spec">Eyebrow — Gold, 10px, weight 500, LS 3px. Opens every section.</p>
          </div>
          <div>
            <p style="font-size:10px; font-weight:500; letter-spacing:3px; text-transform:uppercase; color:var(--sage);">Event Tag · Sage</p>
            <p class="btn-spec">Sage label — Used on cards and event tags only. Never as a fill.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Spacing note -->
    <div style="background:var(--warm-white); border:1px solid var(--linen-deep); padding:40px;">
      <p style="font-size:10px; font-weight:600; letter-spacing:3px; text-transform:uppercase; color:var(--gold); margin-bottom:20px;">Spacing &amp; Structure</p>
      <div style="display:grid; grid-template-columns:repeat(3,1fr); gap:24px;">
        <div>
          <p style="font-size:22px; font-family:'Cormorant Garamond',serif; color:var(--charcoal); margin-bottom:8px;">Section Padding</p>
          <p style="font-size:13px; color:var(--taupe); line-height:1.7;">100–120px top and bottom on desktop. 72px on mobile. Generous space signals luxury and intention.</p>
        </div>
        <div>
          <p style="font-size:22px; font-family:'Cormorant Garamond',serif; color:var(--charcoal); margin-bottom:8px;">Grid Gutters</p>
          <p style="font-size:13px; color:var(--taupe); line-height:1.7;">2px gap between cards with a linen-deep background creates clean separation without heavy borders.</p>
        </div>
        <div>
          <p style="font-size:22px; font-family:'Cormorant Garamond',serif; color:var(--charcoal); margin-bottom:8px;">Gold Line Element</p>
          <p style="font-size:13px; color:var(--taupe); line-height:1.7;">48px × 1px horizontal gold line used as a decorative separator before eyebrow labels in hero sections.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <div class="guide-footer">
    <div>
      <h3>Andrea <em>Lynn</em></h3>
      <p>Brand Guide · Version 1.0 · 2025</p>
    </div>
    <div class="footer-right">
      <p>andreaspacek@gmail.com</p>
      <p>instagram.com/andrealynnalchemy</p>
      <p>andreaspacek.com</p>
    </div>
  </div>

</div><!-- /main -->

<script>
  // Active sidebar link on scroll
  const sections = document.querySelectorAll('[id]');
  const navLinks = document.querySelectorAll('.sidebar nav a');

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        navLinks.forEach(link => {
          link.classList.toggle('active', link.getAttribute('href') === '#' + entry.target.id);
        });
      }
    });
  }, { threshold: 0.3 });

  sections.forEach(s => observer.observe(s));
</script>

</body>
</html>
