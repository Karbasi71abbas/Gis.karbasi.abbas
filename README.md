# naghshebardari.kerman
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="مهندس عباس کرباسی - کارشناس نقشه‌برداری و کارشناس ارشد GIS | خدمات تخصصی نقشه‌برداری، سیستم اطلاعات جغرافیایی و سنجش از دور">
<meta name="keywords" content="نقشه برداری، GIS، سیستم اطلاعات جغرافیایی، عباس کرباسی، مهندس نقشه برداری">
<title>مهندس عباس کرباسی | کارشناس نقشه‌برداری و GIS</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --primary: #0B3D2E;
    --primary-light: #155C44;
    --accent: #1D9E75;
    --accent-light: #5DCAA5;
    --accent-pale: #E1F5EE;
    --gold: #C8963E;
    --gold-light: #F5D899;
    --dark: #0F1A15;
    --text: #1A2820;
    --text-muted: #4A6358;
    --text-light: #7A9A8A;
    --bg: #F7FAF8;
    --bg-card: #FFFFFF;
    --border: rgba(13, 80, 55, 0.12);
    --border-strong: rgba(13, 80, 55, 0.22);
    --shadow: 0 4px 24px rgba(11, 61, 46, 0.10);
    --shadow-lg: 0 12px 48px rgba(11, 61, 46, 0.14);
    --radius: 12px;
    --radius-lg: 20px;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'Vazirmatn', sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.75;
    direction: rtl;
    font-size: 15px;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; right: 0; left: 0; z-index: 1000;
    background: rgba(11, 61, 46, 0.97);
    backdrop-filter: blur(12px);
    padding: 0 6%;
    display: flex; align-items: center; justify-content: space-between;
    height: 68px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }
  .nav-brand {
    display: flex; align-items: center; gap: 12px;
    text-decoration: none; color: #fff;
  }
  .nav-logo {
    width: 42px; height: 42px;
    background: var(--accent);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px; font-weight: 700; color: #fff;
    letter-spacing: -0.5px;
  }
  .nav-title-wrap { display: flex; flex-direction: column; }
  .nav-name { font-size: 14px; font-weight: 600; color: #fff; }
  .nav-sub { font-size: 11px; color: rgba(255,255,255,0.6); }
  .nav-links { display: flex; gap: 6px; align-items: center; }
  .nav-links a {
    color: rgba(255,255,255,0.82);
    text-decoration: none;
    font-size: 13.5px;
    padding: 7px 14px;
    border-radius: 8px;
    transition: all 0.2s;
  }
  .nav-links a:hover { background: rgba(255,255,255,0.1); color: #fff; }
  .nav-cta {
    background: var(--accent) !important;
    color: #fff !important;
    font-weight: 500 !important;
  }
  .nav-cta:hover { background: var(--accent-light) !important; }
  .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; padding: 6px; }
  .hamburger span { display: block; width: 22px; height: 2px; background: #fff; border-radius: 2px; transition: 0.3s; }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    background: linear-gradient(155deg, #071F17 0%, #0B3D2E 45%, #0F5038 100%);
    display: flex; align-items: center; justify-content: center;
    position: relative; overflow: hidden;
    padding: 100px 6% 60px;
  }
  .hero-grid-bg {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(93,202,165,0.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(93,202,165,0.06) 1px, transparent 1px);
    background-size: 48px 48px;
  }
  .hero-circle {
    position: absolute;
    border-radius: 50%;
    border: 1px solid rgba(93,202,165,0.12);
  }
  .hero-circle-1 { width: 600px; height: 600px; top: -150px; left: -200px; }
  .hero-circle-2 { width: 400px; height: 400px; bottom: -100px; right: -100px; }
  .hero-circle-3 { width: 250px; height: 250px; top: 30%; right: 15%; border-color: rgba(93,202,165,0.18); }
  .hero-inner {
    max-width: 1100px; width: 100%; margin: 0 auto;
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 60px; align-items: center; position: relative; z-index: 2;
  }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(93,202,165,0.15);
    border: 1px solid rgba(93,202,165,0.3);
    color: var(--accent-light);
    font-size: 12.5px; padding: 7px 16px; border-radius: 100px;
    margin-bottom: 24px;
  }
  .hero-badge-dot { width: 6px; height: 6px; background: var(--accent-light); border-radius: 50%; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.5;transform:scale(1.4)} }
  .hero-h1 {
    font-size: clamp(32px, 4.5vw, 52px);
    font-weight: 700; color: #fff; line-height: 1.25;
    margin-bottom: 12px;
  }
  .hero-h1 span { color: var(--accent-light); }
  .hero-sub {
    font-size: 17px; color: rgba(255,255,255,0.65);
    margin-bottom: 32px; line-height: 1.8;
  }
  .hero-stats {
    display: flex; gap: 32px; margin-bottom: 40px;
  }
  .hero-stat-num {
    font-size: 30px; font-weight: 700; color: var(--accent-light); display: block;
  }
  .hero-stat-label { font-size: 12px; color: rgba(255,255,255,0.5); }
  .hero-btns { display: flex; gap: 14px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--accent); color: #fff;
    padding: 14px 28px; border-radius: 10px;
    text-decoration: none; font-weight: 600; font-size: 14.5px;
    transition: all 0.25s; border: none; cursor: pointer; display: inline-block;
  }
  .btn-primary:hover { background: #17825F; transform: translateY(-2px); box-shadow: 0 8px 20px rgba(29,158,117,0.35); }
  .btn-outline {
    background: transparent;
    border: 1px solid rgba(255,255,255,0.25); color: #fff;
    padding: 14px 28px; border-radius: 10px;
    text-decoration: none; font-weight: 500; font-size: 14.5px;
    transition: all 0.25s; display: inline-block;
  }
  .btn-outline:hover { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.45); }
  .hero-visual {
    position: relative; display: flex; align-items: center; justify-content: center;
  }
  .hero-map-wrap {
    width: 380px; height: 380px;
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(93,202,165,0.2);
    border-radius: 50%; display: flex; align-items: center; justify-content: center;
    position: relative;
  }
  .hero-map-inner {
    width: 280px; height: 280px;
    background: rgba(29,158,117,0.1);
    border: 1px solid rgba(93,202,165,0.35);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    flex-direction: column; gap: 8px;
  }
  .map-icon-svg { color: var(--accent-light); }
  .hero-map-label {
    font-size: 13px; color: rgba(255,255,255,0.75); font-weight: 500; text-align: center;
  }
  .hero-map-label span { color: var(--accent-light); display: block; font-size: 11px; margin-top: 2px; }
  .orbit-dot {
    position: absolute; width: 10px; height: 10px;
    background: var(--accent); border-radius: 50%;
    border: 2px solid var(--accent-light);
  }
  .od1 { top: 18px; right: 50%; transform: translateX(50%); }
  .od2 { bottom: 18px; right: 50%; transform: translateX(50%); }
  .od3 { right: 18px; top: 50%; transform: translateY(-50%); }
  .od4 { left: 18px; top: 50%; transform: translateY(-50%); }
  .floating-card {
    position: absolute;
    background: rgba(255,255,255,0.08);
    backdrop-filter: blur(8px);
    border: 1px solid rgba(255,255,255,0.12);
    border-radius: 12px; padding: 10px 16px;
    font-size: 12px; color: rgba(255,255,255,0.85);
    white-space: nowrap;
  }
  .fc1 { top: 10px; right: -30px; }
  .fc2 { bottom: 30px; left: -50px; }

  /* ── SECTION BASE ── */
  section { padding: 90px 6%; }
  .section-inner { max-width: 1100px; margin: 0 auto; }
  .section-eyebrow {
    display: inline-flex; align-items: center; gap: 8px;
    color: var(--accent); font-size: 12.5px; font-weight: 600;
    text-transform: uppercase; letter-spacing: 0.08em;
    margin-bottom: 12px;
  }
  .section-eyebrow::before {
    content: ''; width: 24px; height: 2px; background: var(--accent); border-radius: 2px;
  }
  .section-h2 { font-size: clamp(26px, 3vw, 36px); font-weight: 700; color: var(--text); margin-bottom: 16px; line-height: 1.3; }
  .section-desc { color: var(--text-muted); font-size: 16px; max-width: 600px; line-height: 1.85; }

  /* ── SERVICES ── */
  #services { background: #fff; }
  .services-grid {
    margin-top: 56px;
    display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 24px;
  }
  .service-card {
    background: var(--bg); border: 1px solid var(--border);
    border-radius: var(--radius-lg); padding: 32px 28px;
    transition: all 0.3s; cursor: default; position: relative; overflow: hidden;
  }
  .service-card::before {
    content: ''; position: absolute; top: 0; right: 0; left: 0;
    height: 3px; background: var(--accent); transform: scaleX(0);
    transform-origin: right; transition: transform 0.3s; border-radius: 0 0 0 0;
  }
  .service-card:hover { box-shadow: var(--shadow-lg); transform: translateY(-4px); border-color: var(--accent-light); }
  .service-card:hover::before { transform: scaleX(1); }
  .service-icon {
    width: 54px; height: 54px;
    background: var(--accent-pale);
    border-radius: 14px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 20px; font-size: 24px;
  }
  .service-title { font-size: 17px; font-weight: 600; color: var(--text); margin-bottom: 10px; }
  .service-desc { font-size: 14px; color: var(--text-muted); line-height: 1.8; }
  .service-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 16px; }
  .tag {
    background: var(--accent-pale); color: var(--primary-light);
    font-size: 11.5px; padding: 4px 10px; border-radius: 100px;
    font-weight: 500;
  }

  /* ── ABOUT ── */
  #about { background: var(--bg); }
  .about-grid {
    margin-top: 56px;
    display: grid; grid-template-columns: 1fr 1.3fr; gap: 80px; align-items: center;
  }
  .about-portrait {
    width: 100%; aspect-ratio: 1;
    max-width: 360px;
    background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
    border-radius: 28px;
    display: flex; align-items: center; justify-content: center;
    position: relative; overflow: hidden;
  }
  .portrait-initials {
    font-size: 72px; font-weight: 700; color: rgba(255,255,255,0.25); letter-spacing: -4px;
  }
  .portrait-badge {
    position: absolute; bottom: 20px; right: 20px;
    background: rgba(255,255,255,0.1);
    backdrop-filter: blur(8px);
    border: 1px solid rgba(255,255,255,0.2);
    border-radius: 12px; padding: 10px 16px;
    color: #fff; font-size: 13px; font-weight: 600;
  }
  .about-content {}
  .about-intro { font-size: 16px; color: var(--text); line-height: 1.9; margin-bottom: 28px; }
  .about-highlights { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 32px; }
  .highlight-item {
    display: flex; align-items: flex-start; gap: 12px;
    background: #fff; border: 1px solid var(--border);
    border-radius: var(--radius); padding: 16px;
  }
  .hi-icon {
    width: 36px; height: 36px; min-width: 36px;
    background: var(--accent-pale); border-radius: 8px;
    display: flex; align-items: center; justify-content: center; font-size: 16px;
  }
  .hi-label { font-size: 12px; color: var(--text-muted); margin-bottom: 2px; }
  .hi-val { font-size: 13.5px; font-weight: 600; color: var(--text); }
  .skills-section { margin-top: 8px; }
  .skills-title { font-size: 14px; font-weight: 600; color: var(--text); margin-bottom: 14px; }
  .skill-bar-item { margin-bottom: 12px; }
  .skill-bar-top { display: flex; justify-content: space-between; margin-bottom: 6px; font-size: 13px; }
  .skill-bar-name { color: var(--text); font-weight: 500; }
  .skill-bar-pct { color: var(--accent); font-weight: 600; }
  .skill-bar-bg { height: 6px; background: var(--accent-pale); border-radius: 100px; overflow: hidden; }
  .skill-bar-fill { height: 100%; background: var(--accent); border-radius: 100px; transition: width 1.2s ease; }

  /* ── PROJECTS ── */
  #projects { background: #fff; }
  .projects-grid {
    margin-top: 56px;
    display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 24px;
  }
  .project-card {
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: var(--radius-lg);
    overflow: hidden;
    transition: all 0.3s;
  }
  .project-card:hover { box-shadow: var(--shadow-lg); transform: translateY(-4px); }
  .project-img {
    height: 180px;
    display: flex; align-items: center; justify-content: center;
    font-size: 48px; position: relative; overflow: hidden;
  }
  .project-img-1 { background: linear-gradient(135deg, #0B3D2E 0%, #1D9E75 100%); }
  .project-img-2 { background: linear-gradient(135deg, #0C447C 0%, #378ADD 100%); }
  .project-img-3 { background: linear-gradient(135deg, #412402 0%, #BA7517 100%); }
  .project-img-4 { background: linear-gradient(135deg, #26215C 0%, #7F77DD 100%); }
  .project-img-5 { background: linear-gradient(135deg, #3B6D11 0%, #639922 100%); }
  .project-img-6 { background: linear-gradient(135deg, #4A1528 0%, #D4537E 100%); }
  .project-img-label {
    position: absolute; bottom: 12px; right: 12px;
    background: rgba(0,0,0,0.35); color: rgba(255,255,255,0.9);
    font-size: 11px; padding: 4px 10px; border-radius: 100px;
    backdrop-filter: blur(4px);
  }
  .project-body { padding: 24px; }
  .project-cat {
    font-size: 11px; font-weight: 600; color: var(--accent);
    text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 8px;
  }
  .project-name { font-size: 16px; font-weight: 600; color: var(--text); margin-bottom: 8px; }
  .project-desc { font-size: 13.5px; color: var(--text-muted); line-height: 1.75; }

  /* ── GIS ── */
  #gis {
    background: linear-gradient(155deg, var(--primary) 0%, #0F5038 100%);
    color: #fff;
  }
  #gis .section-eyebrow { color: var(--accent-light); }
  #gis .section-eyebrow::before { background: var(--accent-light); }
  #gis .section-h2 { color: #fff; }
  #gis .section-desc { color: rgba(255,255,255,0.68); }
  .gis-grid { margin-top: 56px; display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 20px; }
  .gis-card {
    background: rgba(255,255,255,0.07);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: var(--radius-lg); padding: 28px 24px;
    transition: all 0.3s;
  }
  .gis-card:hover { background: rgba(255,255,255,0.11); transform: translateY(-3px); }
  .gis-icon { font-size: 32px; margin-bottom: 16px; }
  .gis-title { font-size: 16px; font-weight: 600; color: #fff; margin-bottom: 8px; }
  .gis-desc { font-size: 13.5px; color: rgba(255,255,255,0.6); line-height: 1.75; }
  .gis-software {
    margin-top: 60px;
    border-top: 1px solid rgba(255,255,255,0.1); padding-top: 48px;
  }
  .gis-sw-title { font-size: 16px; font-weight: 600; color: #fff; margin-bottom: 24px; text-align: center; }
  .gis-sw-list { display: flex; flex-wrap: wrap; gap: 12px; justify-content: center; }
  .sw-pill {
    background: rgba(255,255,255,0.09);
    border: 1px solid rgba(255,255,255,0.16);
    color: rgba(255,255,255,0.82);
    font-size: 13px; padding: 8px 20px; border-radius: 100px;
    transition: all 0.2s;
  }
  .sw-pill:hover { background: rgba(29,158,117,0.25); border-color: var(--accent); color: var(--accent-light); }

  /* ── EDUCATION ── */
  #education { background: var(--bg); }
  .edu-timeline { margin-top: 56px; position: relative; }
  .edu-timeline::before {
    content: ''; position: absolute; right: 19px; top: 0; bottom: 0;
    width: 2px; background: var(--border-strong);
  }
  .edu-item {
    display: flex; gap: 28px; align-items: flex-start;
    margin-bottom: 40px; position: relative;
  }
  .edu-dot {
    width: 40px; height: 40px; min-width: 40px;
    background: var(--accent);
    border: 3px solid var(--bg);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 17px; color: #fff;
    position: relative; z-index: 1;
    box-shadow: 0 0 0 2px var(--accent);
  }
  .edu-dot-gray { background: var(--text-light); box-shadow: 0 0 0 2px var(--text-light); }
  .edu-body {
    background: #fff; border: 1px solid var(--border);
    border-radius: var(--radius-lg); padding: 22px 24px; flex: 1;
  }
  .edu-degree { font-size: 16px; font-weight: 600; color: var(--text); margin-bottom: 4px; }
  .edu-field { font-size: 14px; color: var(--accent); font-weight: 500; margin-bottom: 6px; }
  .edu-meta { font-size: 13px; color: var(--text-muted); }

  /* ── CONTACT ── */
  #contact { background: #fff; }
  .contact-grid {
    margin-top: 56px;
    display: grid; grid-template-columns: 1fr 1fr; gap: 60px;
  }
  .contact-info-list { display: flex; flex-direction: column; gap: 16px; }
  .contact-item {
    display: flex; align-items: center; gap: 16px;
    background: var(--bg); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 16px 20px;
    text-decoration: none; color: inherit; transition: all 0.25s;
  }
  .contact-item:hover { border-color: var(--accent); box-shadow: var(--shadow); }
  .ci-icon {
    width: 44px; height: 44px; min-width: 44px;
    background: var(--accent-pale); border-radius: 10px;
    display: flex; align-items: center; justify-content: center; font-size: 20px;
  }
  .ci-label { font-size: 12px; color: var(--text-muted); margin-bottom: 2px; }
  .ci-val { font-size: 14px; font-weight: 600; color: var(--text); }
  .contact-form { display: flex; flex-direction: column; gap: 16px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  .form-group { display: flex; flex-direction: column; gap: 6px; }
  .form-label { font-size: 13px; font-weight: 500; color: var(--text); }
  .form-input, .form-textarea {
    background: var(--bg); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 12px 16px;
    font-family: 'Vazirmatn', sans-serif;
    font-size: 14px; color: var(--text);
    transition: border-color 0.2s;
    direction: rtl;
  }
  .form-input:focus, .form-textarea:focus {
    outline: none; border-color: var(--accent);
    box-shadow: 0 0 0 3px rgba(29,158,117,0.1);
  }
  .form-textarea { min-height: 120px; resize: vertical; }
  .form-submit {
    background: var(--accent); color: #fff; border: none;
    padding: 14px 24px; border-radius: var(--radius);
    font-family: 'Vazirmatn', sans-serif; font-size: 15px; font-weight: 600;
    cursor: pointer; transition: all 0.25s;
  }
  .form-submit:hover { background: var(--primary-light); transform: translateY(-1px); box-shadow: 0 6px 18px rgba(29,158,117,0.3); }

  /* ── FOOTER ── */
  footer {
    background: var(--dark); color: rgba(255,255,255,0.65);
    padding: 48px 6%; text-align: center;
    font-size: 13.5px;
  }
  .footer-logo-row { display: flex; align-items: center; justify-content: center; gap: 10px; margin-bottom: 16px; }
  .footer-logo { width: 36px; height: 36px; background: var(--accent); border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 16px; font-weight: 700; color: #fff; }
  .footer-name { color: #fff; font-weight: 600; font-size: 15px; }
  .footer-links { display: flex; justify-content: center; gap: 24px; margin-bottom: 20px; flex-wrap: wrap; }
  .footer-links a { color: rgba(255,255,255,0.55); text-decoration: none; transition: color 0.2s; }
  .footer-links a:hover { color: var(--accent-light); }
  .footer-copy { color: rgba(255,255,255,0.35); font-size: 12px; }

  /* ── MOBILE ── */
  @media (max-width: 900px) {
    .hero-inner { grid-template-columns: 1fr; gap: 40px; }
    .hero-visual { display: none; }
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .about-portrait { max-width: 260px; aspect-ratio: 1; }
    .contact-grid { grid-template-columns: 1fr; gap: 40px; }
    .form-row { grid-template-columns: 1fr; }
    .nav-links { display: none; }
    .hamburger { display: flex; }
  }
  @media (max-width: 600px) {
    section { padding: 70px 5%; }
    .about-highlights { grid-template-columns: 1fr; }
    .hero-stats { gap: 20px; }
    .hero-stat-num { font-size: 24px; }
  }

  /* ── SCROLL ANIMATION ── */
  .fade-in { opacity: 0; transform: translateY(24px); transition: opacity 0.65s ease, transform 0.65s ease; }
  .fade-in.visible { opacity: 1; transform: translateY(0); }

  /* ── MOBILE MENU ── */
  .mobile-menu {
    display: none; position: fixed; top: 68px; right: 0; left: 0; z-index: 999;
    background: rgba(11, 61, 46, 0.98); backdrop-filter: blur(12px);
    padding: 16px 6%; flex-direction: column; gap: 4px;
    border-bottom: 1px solid rgba(255,255,255,0.08);
  }
  .mobile-menu.open { display: flex; }
  .mobile-menu a { color: rgba(255,255,255,0.85); text-decoration: none; padding: 12px 16px; border-radius: 8px; font-size: 14px; }
  .mobile-menu a:hover { background: rgba(255,255,255,0.08); }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-brand">
    <div class="nav-logo">ک</div>
    <div class="nav-title-wrap">
      <span class="nav-name">مهندس عباس کرباسی</span>
      <span class="nav-sub">کارشناس ارشد GIS | نقشه‌برداری</span>
    </div>
  </a>
  <div class="nav-links">
    <a href="#services">خدمات</a>
    <a href="#about">درباره من</a>
    <a href="#projects">پروژه‌ها</a>
    <a href="#gis">GIS</a>
    <a href="#education">تحصیلات</a>
    <a href="#contact" class="nav-cta">تماس با من</a>
  </div>
  <div class="hamburger" id="hamburger">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- MOBILE MENU -->
<div class="mobile-menu" id="mobileMenu">
  <a href="#services" onclick="closeMobile()">خدمات</a>
  <a href="#about" onclick="closeMobile()">درباره من</a>
  <a href="#projects" onclick="closeMobile()">پروژه‌ها</a>
  <a href="#gis" onclick="closeMobile()">GIS</a>
  <a href="#education" onclick="closeMobile()">تحصیلات</a>
  <a href="#contact" onclick="closeMobile()">تماس با من</a>
</div>

<!-- HERO -->
<section id="hero">
  <div class="hero-grid-bg"></div>
  <div class="hero-circle hero-circle-1"></div>
  <div class="hero-circle hero-circle-2"></div>
  <div class="hero-circle hero-circle-3"></div>
  <div class="hero-inner">
    <div class="hero-text">
      <div class="hero-badge">
        <span class="hero-badge-dot"></span>
        در دسترس برای پروژه‌های جدید
      </div>
      <h1 class="hero-h1">
        مهندس<br>
        <span>عباس کرباسی</span>
      </h1>
      <p class="hero-sub">
        کارشناس نقشه‌برداری و کارشناس ارشد سیستم اطلاعات جغرافیایی (GIS)<br>
        با تجربه در پروژه‌های ملی و منطقه‌ای
      </p>
      <div class="hero-stats">
        <div>
          <span class="hero-stat-num">+۱۵</span>
          <span class="hero-stat-label">سال تجربه</span>
        </div>
        <div>
          <span class="hero-stat-num">+۸۰</span>
          <span class="hero-stat-label">پروژه انجام‌شده</span>
        </div>
        <div>
          <span class="hero-stat-num">۴</span>
          <span class="hero-stat-label">گواهینامه تخصصی</span>
        </div>
      </div>
      <div class="hero-btns">
        <a href="#contact" class="btn-primary">مشاوره رایگان</a>
        <a href="#projects" class="btn-outline">مشاهده پروژه‌ها</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-map-wrap">
        <div class="orbit-dot od1"></div>
        <div class="orbit-dot od2"></div>
        <div class="orbit-dot od3"></div>
        <div class="orbit-dot od4"></div>
        <div class="hero-map-inner">
          <svg width="80" height="80" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="40" cy="40" r="36" stroke="#5DCAA5" stroke-width="1.5" stroke-dasharray="4 4"/>
            <circle cx="40" cy="40" r="6" fill="#5DCAA5"/>
            <line x1="40" y1="4" x2="40" y2="76" stroke="#5DCAA5" stroke-width="0.75" stroke-dasharray="3 3"/>
            <line x1="4" y1="40" x2="76" y2="40" stroke="#5DCAA5" stroke-width="0.75" stroke-dasharray="3 3"/>
            <path d="M40 4 Q55 20 55 40 Q55 60 40 76 Q25 60 25 40 Q25 20 40 4Z" stroke="#5DCAA5" stroke-width="0.75" fill="none"/>
            <circle cx="58" cy="26" r="4" fill="#5DCAA5" opacity="0.7"/>
            <circle cx="22" cy="54" r="3" fill="#9FE1CB" opacity="0.7"/>
            <circle cx="52" cy="60" r="3.5" fill="#5DCAA5" opacity="0.5"/>
          </svg>
          <div class="hero-map-label">
            نقشه‌برداری دقیق
            <span>GIS · RS · GPS</span>
          </div>
        </div>
        <div class="floating-card fc1">📍 دقت موقعیت‌یابی: ±۱ سانتی‌متر</div>
        <div class="floating-card fc2">🛰️ پردازش تصاویر ماهواره‌ای</div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="section-inner">
    <div class="fade-in">
      <div class="section-eyebrow">خدمات تخصصی</div>
      <h2 class="section-h2">چه خدماتی ارائه می‌دهم؟</h2>
      <p class="section-desc">طیف گسترده‌ای از خدمات نقشه‌برداری و GIS با بالاترین دقت و استانداردهای فنی</p>
    </div>
    <div class="services-grid">
      <div class="service-card fade-in">
        <div class="service-icon">🗺️</div>
        <div class="service-title">نقشه‌برداری زمینی</div>
        <div class="service-desc">اجرای عملیات نقشه‌برداری زمینی با استفاده از تئودولیت‌های دیجیتال، توتال استیشن و GPS دیفرانسیل با دقت بالا</div>
        <div class="service-tags">
          <span class="tag">توتال استیشن</span>
          <span class="tag">GPS RTK</span>
          <span class="tag">ترازیابی دقیق</span>
        </div>
      </div>
      <div class="service-card fade-in">
        <div class="service-icon">🌍</div>
        <div class="service-title">سیستم اطلاعات جغرافیایی</div>
        <div class="service-desc">طراحی، پیاده‌سازی و مدیریت پایگاه‌های داده مکانی، تحلیل‌های فضایی پیشرفته و تولید نقشه‌های موضوعی</div>
        <div class="service-tags">
          <span class="tag">ArcGIS</span>
          <span class="tag">QGIS</span>
          <span class="tag">WebGIS</span>
        </div>
      </div>
      <div class="service-card fade-in">
        <div class="service-icon">🛰️</div>
        <div class="service-title">سنجش از دور و فتوگرامتری</div>
        <div class="service-desc">پردازش تصاویر ماهواره‌ای و هوایی، استخراج اطلاعات از تصاویر رادار و اپتیک، مدل‌سازی ارتفاعی</div>
        <div class="service-tags">
          <span class="tag">تصاویر ماهواره‌ای</span>
          <span class="tag">DEM</span>
          <span class="tag">ENVI</span>
        </div>
      </div>
      <div class="service-card fade-in">
        <div class="service-icon">✈️</div>
        <div class="service-title">نقشه‌برداری هوایی (UAV)</div>
        <div class="service-desc">اجرای عملیات فتوگرامتری هوایی با پهپاد، تهیه ارتوفتوموزاییک، مدل رقومی سطح و ابر نقاط سه‌بعدی</div>
        <div class="service-tags">
          <span class="tag">Pix4D</span>
          <span class="tag">ارتوفتو</span>
          <span class="tag">Point Cloud</span>
        </div>
      </div>
      <div class="service-card fade-in">
        <div class="service-icon">🏗️</div>
        <div class="service-title">نقشه‌برداری عمرانی و صنعتی</div>
        <div class="service-desc">پیاده‌سازی نقشه‌های ساختمانی و راه‌سازی، پایش تغییر شکل سازه‌ها، نقشه‌برداری معدن و سدسازی</div>
        <div class="service-tags">
          <span class="tag">پیاده‌سازی</span>
          <span class="tag">پایش سازه</span>
          <span class="tag">معدن</span>
        </div>
      </div>
      <div class="service-card fade-in">
        <div class="service-icon">📊</div>
        <div class="service-title">کاداستر و ثبت اراضی</div>
        <div class="service-desc">تهیه نقشه‌های کاداستر، افراز و تفکیک اراضی، تعیین حدود مالکیت و خدمات مرتبط با ثبت اسناد</div>
        <div class="service-tags">
          <span class="tag">کاداستر</span>
          <span class="tag">افراز</span>
          <span class="tag">تفکیک اراضی</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <div class="fade-in">
      <div class="section-eyebrow">درباره من</div>
      <h2 class="section-h2">آشنایی با مهندس کرباسی</h2>
    </div>
    <div class="about-grid">
      <div style="display:flex;flex-direction:column;align-items:center;gap:24px;">
        <div class="about-portrait fade-in">
          <div class="portrait-initials">ع.ک</div>
          <div class="portrait-badge">🏆 کارشناس ارشد GIS</div>
        </div>
        <div class="about-highlights fade-in">
          <div class="highlight-item">
            <div class="hi-icon">🎓</div>
            <div>
              <div class="hi-label">مدرک تحصیلی</div>
              <div class="hi-val">کارشناسی ارشد GIS</div>
            </div>
          </div>
          <div class="highlight-item">
            <div class="hi-icon">📍</div>
            <div>
              <div class="hi-label">محل فعالیت</div>
              <div class="hi-val">سراسر ایران</div>
            </div>
          </div>
          <div class="highlight-item">
            <div class="hi-icon">⏱️</div>
            <div>
              <div class="hi-label">سابقه کار</div>
              <div class="hi-val">بیش از ۱۵ سال</div>
            </div>
          </div>
          <div class="highlight-item">
            <div class="hi-icon">📜</div>
            <div>
              <div class="hi-label">نظام مهندسی</div>
              <div class="hi-val">عضو رسمی</div>
            </div>
          </div>
        </div>
      </div>
      <div class="fade-in">
        <p class="about-intro">
          مهندس عباس کرباسی، کارشناس نقشه‌برداری و کارشناس ارشد سیستم‌های اطلاعات جغرافیایی (GIS) با بیش از یک دهه و نیم تجربه عملی در پروژه‌های ملی و منطقه‌ای در حوزه‌های عمران، معدن، محیط زیست و مدیریت اراضی.
        </p>
        <p class="about-intro" style="font-size:14px;">
          با تسلط به ابزارهای پیشرفته نقشه‌برداری و نرم‌افزارهای GIS، خدمات دقیق، به‌موقع و استاندارد در اختیار کارفرمایان دولتی و خصوصی قرار می‌دهم. تخصص اصلی من ترکیب داده‌های میدانی با تحلیل‌های فضایی پیچیده برای حل مسائل واقعی است.
        </p>
        <div class="skills-section">
          <div class="skills-title">سطح تخصص در حوزه‌های کلیدی</div>
          <div class="skill-bar-item">
            <div class="skill-bar-top"><span class="skill-bar-name">نقشه‌برداری زمینی</span><span class="skill-bar-pct">98%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:98%"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-top"><span class="skill-bar-name">ArcGIS / QGIS</span><span class="skill-bar-pct">95%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:95%"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-top"><span class="skill-bar-name">سنجش از دور</span><span class="skill-bar-pct">88%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:88%"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-top"><span class="skill-bar-name">پهپاد و فتوگرامتری</span><span class="skill-bar-pct">82%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:82%"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-top"><span class="skill-bar-name">WebGIS و پایگاه داده مکانی</span><span class="skill-bar-pct">78%</span></div>
            <div class="skill-bar-bg"><div class="skill-bar-fill" style="width:78%"></div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-inner">
    <div class="fade-in">
      <div class="section-eyebrow">نمونه کارها</div>
      <h2 class="section-h2">پروژه‌های اجراشده</h2>
      <p class="section-desc">نمونه‌ای از پروژه‌های موفق در حوزه نقشه‌برداری و GIS</p>
    </div>
    <div class="projects-grid">
      <div class="project-card fade-in">
        <div class="project-img project-img-1">
          <span>🗺️</span>
          <span class="project-img-label">۱۴۰۲</span>
        </div>
        <div class="project-body">
          <div class="project-cat">نقشه‌برداری زیرساخت</div>
          <div class="project-name">پروژه نقشه‌برداری شبکه آبرسانی شهری</div>
          <div class="project-desc">نقشه‌برداری کامل شبکه توزیع آب شهر با استفاده از GPS دیفرانسیل و تهیه GIS جامع زیرساخت‌ها</div>
        </div>
      </div>
      <div class="project-card fade-in">
        <div class="project-img project-img-2">
          <span>🏞️</span>
          <span class="project-img-label">۱۴۰۱</span>
        </div>
        <div class="project-body">
          <div class="project-cat">سنجش از دور</div>
          <div class="project-name">پایش تغییرات کاربری اراضی با تصاویر ماهواره‌ای</div>
          <div class="project-desc">آنالیز تغییرات پوشش زمین در بازه ۲۰ ساله با استفاده از تصاویر لندست و سنتینل</div>
        </div>
      </div>
      <div class="project-card fade-in">
        <div class="project-img project-img-3">
          <span>⛰️</span>
          <span class="project-img-label">۱۴۰۱</span>
        </div>
        <div class="project-body">
          <div class="project-cat">نقشه‌برداری معدن</div>
          <div class="project-name">نقشه‌برداری جامع معدن سنگ آهن</div>
          <div class="project-desc">تهیه نقشه‌های توپوگرافی معدن، محاسبه حجم ذخیره و پیاده‌سازی سیستم پایش ماهانه</div>
        </div>
      </div>
      <div class="project-card fade-in">
        <div class="project-img project-img-4">
          <span>🏙️</span>
          <span class="project-img-label">۱۴۰۰</span>
        </div>
        <div class="project-body">
          <div class="project-cat">GIS شهری</div>
          <div class="project-name">سیستم اطلاعات جغرافیایی شهرداری</div>
          <div class="project-desc">طراحی و پیاده‌سازی WebGIS کامل برای مدیریت اطلاعات مکانی شهرداری با لایه‌های چندگانه</div>
        </div>
      </div>
      <div class="project-card fade-in">
        <div class="project-img project-img-5">
          <span>🌱</span>
          <span class="project-img-label">۱۴۰۰</span>
        </div>
        <div class="project-body">
          <div class="project-cat">محیط زیست</div>
          <div class="project-name">نقشه‌برداری اراضی ملی و مرتعی</div>
          <div class="project-desc">تعیین حریم و محدوده اراضی ملی با GPS دقیق و ثبت مختصات برای حفاظت از منابع طبیعی</div>
        </div>
      </div>
      <div class="project-card fade-in">
        <div class="project-img project-img-6">
          <span>✈️</span>
          <span class="project-img-label">۱۳۹۹</span>
        </div>
        <div class="project-body">
          <div class="project-cat">فتوگرامتری هوایی</div>
          <div class="project-name">نقشه‌برداری با پهپاد - پروژه راه‌سازی</div>
          <div class="project-desc">تهیه ارتوفتوموزاییک و مدل رقومی ارتفاعی مسیر ۱۸۰ کیلومتری جاده با دقت ۳ سانتی‌متر</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GIS -->
<section id="gis">
  <div class="section-inner">
    <div class="fade-in">
      <div class="section-eyebrow">تخصص GIS</div>
      <h2 class="section-h2">سیستم اطلاعات جغرافیایی</h2>
      <p class="section-desc">تخصص کارشناسی ارشد در تحلیل‌های مکانی پیشرفته، مدل‌سازی و مدیریت داده‌های جغرافیایی</p>
    </div>
    <div class="gis-grid">
      <div class="gis-card fade-in">
        <div class="gis-icon">🗃️</div>
        <div class="gis-title">مدیریت پایگاه داده مکانی</div>
        <div class="gis-desc">طراحی و پیاده‌سازی پایگاه‌های داده جغرافیایی در PostgreSQL/PostGIS و File Geodatabase</div>
      </div>
      <div class="gis-card fade-in">
        <div class="gis-icon">📈</div>
        <div class="gis-title">تحلیل‌های فضایی</div>
        <div class="gis-desc">آنالیز شبکه، مدل‌سازی هیدرولوژی، تحلیل دیدرس، درون‌یابی و خوشه‌بندی مکانی</div>
      </div>
      <div class="gis-card fade-in">
        <div class="gis-icon">🌐</div>
        <div class="gis-title">WebGIS و نقشه‌برداری آنلاین</div>
        <div class="gis-desc">توسعه سرویس‌های تحت وب با ArcGIS Server، GeoServer و یکپارچه‌سازی با Leaflet و OpenLayers</div>
      </div>
      <div class="gis-card fade-in">
        <div class="gis-icon">🤖</div>
        <div class="gis-title">هوش مصنوعی در GIS</div>
        <div class="gis-desc">کاربرد یادگیری ماشین برای طبقه‌بندی تصاویر، تشخیص تغییرات و پیش‌بینی الگوهای مکانی</div>
      </div>
    </div>
    <div class="gis-software fade-in">
      <div class="gis-sw-title">نرم‌افزارها و ابزارهای تخصصی</div>
      <div class="gis-sw-list">
        <span class="sw-pill">ArcGIS Pro</span>
        <span class="sw-pill">QGIS</span>
        <span class="sw-pill">AutoCAD Civil 3D</span>
        <span class="sw-pill">ENVI</span>
        <span class="sw-pill">Pix4D</span>
        <span class="sw-pill">Agisoft Metashape</span>
        <span class="sw-pill">Google Earth Engine</span>
        <span class="sw-pill">MapInfo</span>
        <span class="sw-pill">Global Mapper</span>
        <span class="sw-pill">Erdas Imagine</span>
        <span class="sw-pill">PostGIS</span>
        <span class="sw-pill">MATLAB</span>
        <span class="sw-pill">Python (GeoPandas)</span>
        <span class="sw-pill">Leica Cyclone</span>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-inner">
    <div class="fade-in">
      <div class="section-eyebrow">سوابق علمی</div>
      <h2 class="section-h2">تحصیلات و گواهینامه‌ها</h2>
    </div>
    <div class="edu-timeline fade-in">
      <div class="edu-item">
        <div class="edu-dot">🎓</div>
        <div class="edu-body">
          <div class="edu-degree">کارشناسی ارشد</div>
          <div class="edu-field">سیستم اطلاعات جغرافیایی (GIS)</div>
          <div class="edu-meta">دانشگاه آزاد اسلامی واحد استهبان · شیراز</div>
        </div>
      </div>
      <div class="edu-item">
        <div class="edu-dot">🎓</div>
        <div class="edu-body">
          <div class="edu-degree">کارشناسی</div>
          <div class="edu-field">مهندسی نقشه‌برداری</div>
          <div class="edu-meta">دانشگاه آزاد اسلامی · شیراز</div>
        </div>
      </div>
      <div class="edu-item">
        <div class="edu-dot edu-dot-gray">📜</div>
        <div class="edu-body">
          <div class="edu-degree">عضو رسمی سازمان نظام مهندسی</div>
          <div class="edu-field">پروانه اشتغال به کار</div>
          <div class="edu-meta">سازمان نظام مهندسی ساختمان کشور</div>
        </div>
      </div>
      <div class="edu-item">
        <div class="edu-dot edu-dot-gray">🏅</div>
        <div class="edu-body">
          <div class="edu-degree">گواهینامه‌های تخصصی</div>
          <div class="edu-field">ArcGIS Pro · Pix4D · Google Earth Engine · GPS دیفرانسیل</div>
          <div class="edu-meta">دوره‌های آموزشی معتبر بین‌المللی</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <div class="fade-in">
      <div class="section-eyebrow">تماس با من</div>
      <h2 class="section-h2">با من در تماس باشید</h2>
      <p class="section-desc">برای مشاوره رایگان، ارائه پیشنهاد قیمت یا همکاری در پروژه‌های شما آماده‌ام</p>
    </div>
    <div class="contact-grid fade-in">
      <div>
        <div class="contact-info-list">
          <div class="contact-item">
            <div class="ci-icon">📞</div>
            <div>
              <div class="ci-label">شماره تماس</div>
              <div class="ci-val">۰۹۱۷۲۹۴۷۲۳۹</div>
            </div>
          </div>
          <div class="contact-item">
            <div class="ci-icon">📧</div>
            <div>
              <div class="ci-label">ایمیل</div>
              <div class="ci-val">abbas_karbasi71@yahoo.com</div>
            </div>
          </div>
          <div class="contact-item">
            <div class="ci-icon">📍</div>
            <div>
              <div class="ci-label">محل فعالیت</div>
              <div class="ci-val">تهران و سراسر ایران</div>
            </div>
          </div>
          <div class="contact-item">
            <div class="ci-icon">⏰</div>
            <div>
              <div class="ci-label">ساعات پاسخگویی</div>
              <div class="ci-val">شنبه تا پنجشنبه · ۸ صبح تا ۶ عصر</div>
            </div>
          </div>
          <div class="contact-item">
            <div class="ci-icon">💬</div>
            <div>
              <div class="ci-label">پیام‌رسان</div>
              <div class="ci-val">واتساپ · تلگرام</div>
            </div>
          </div>
        </div>
      </div>
      <div>
        <form class="contact-form" onsubmit="handleSubmit(event)">
          <div class="form-row">
            <div class="form-group">
              <label class="form-label">نام و نام خانوادگی</label>
              <input type="text" class="form-input" placeholder="نام شما">
            </div>
            <div class="form-group">
              <label class="form-label">شماره تماس</label>
              <input type="tel" class="form-input" placeholder="۰۹۱۷-XXX-XXXX">
            </div>
          </div>
          <div class="form-group">
            <label class="form-label">ایمیل</label>
            <input type="email" class="form-input" placeholder="example@email.com">
          </div>
          <div class="form-group">
            <label class="form-label">موضوع</label>
            <input type="text" class="form-input" placeholder="موضوع درخواست شما">
          </div>
          <div class="form-group">
            <label class="form-label">پیام</label>
            <textarea class="form-textarea" placeholder="شرح کامل پروژه یا درخواست خود را بنویسید..."></textarea>
          </div>
          <button type="submit" class="form-submit" id="submitBtn">ارسال پیام</button>
        </form>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo-row">
    <div class="footer-logo">ک</div>
    <span class="footer-name">مهندس عباس کرباسی</span>
  </div>
  <div class="footer-links">
    <a href="#services">خدمات</a>
    <a href="#about">درباره من</a>
    <a href="#projects">پروژه‌ها</a>
    <a href="#gis">GIS</a>
    <a href="#education">تحصیلات</a>
    <a href="#contact">تماس</a>
  </div>
  <p class="footer-copy">© ۱۴۰۳ مهندس عباس کرباسی | کارشناس نقشه‌برداری و کارشناس ارشد GIS | تمامی حقوق محفوظ است</p>
</footer>

<script>
  document.getElementById('hamburger').addEventListener('click',function(){
    document.getElementById('mobileMenu').classList.toggle('open');
  });
  function closeMobile(){
    document.getElementById('mobileMenu').classList.remove('open');
  }
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('visible'); obs.unobserve(e.target); } });
  },{threshold:0.1});
  document.querySelectorAll('.fade-in').forEach(el=>obs.observe(el));
  function handleSubmit(e){
    e.preventDefault();
    const btn=document.getElementById('submitBtn');
    btn.textContent='✅ پیام ارسال شد!';
    btn.style.background='#0B3D2E';
    setTimeout(()=>{ btn.textContent='ارسال پیام'; btn.style.background=''; e.target.reset(); },3500);
  }
</script>
</body>
</html>
