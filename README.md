<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ژئوماتیک مدرن کرمان | مهندسی نقشه‌برداری</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@100;300;400;500;700;900&display=swap');

        :root {
            --green: #00ff9d;
            --blue: #00a2ff;
            --pink: #ff009a;
            --dark: #0a0a0a;
            --dark2: #1a1a2e;
            --dark3: #16213e;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Vazirmatn', sans-serif;
            background: linear-gradient(135deg, var(--dark) 0%, var(--dark2) 50%, var(--dark3) 100%);
            color: #fff;
            overflow-x: hidden;
        }

        /* ========== SCROLLBAR ========== */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--dark2); }
        ::-webkit-scrollbar-thumb { background: linear-gradient(45deg, var(--green), var(--blue)); border-radius: 4px; }

        /* ========== NAVBAR ========== */
        .navbar {
            position: fixed; top: 0; width: 100%;
            padding: 18px 50px;
            background: rgba(16,32,62,0.88);
            backdrop-filter: blur(20px);
            z-index: 1000;
            transition: all .3s ease;
            border-bottom: 1px solid rgba(0,255,157,0.1);
        }
        .navbar.scrolled { padding: 12px 50px; background: rgba(16,32,62,0.97); }
        .nav-container { display: flex; justify-content: space-between; align-items: center; max-width: 1200px; margin: 0 auto; }
        .logo { font-size: 1.6rem; font-weight: 900; background: linear-gradient(45deg, var(--green), var(--blue)); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent; letter-spacing: 1px; }
        .nav-links { display: flex; list-style: none; gap: 28px; }
        .nav-links a { color: #fff; text-decoration: none; font-weight: 500; font-size: .95rem; position: relative; transition: color .3s; }
        .nav-links a::after { content: ''; position: absolute; bottom: -5px; left: 0; width: 0; height: 2px; background: linear-gradient(45deg, var(--green), var(--blue)); transition: width .3s ease; }
        .nav-links a:hover { color: var(--green); }
        .nav-links a:hover::after { width: 100%; }

        /* ========== HERO ========== */
        .hero {
            height: 100vh; position: relative;
            display: flex; align-items: center; justify-content: center;
            overflow: hidden;
        }
        .hero-bg {
            position: absolute; inset: 0;
            background:
                radial-gradient(circle at 20% 20%, rgba(0,255,157,.12) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(0,162,255,.12) 0%, transparent 50%),
                radial-gradient(circle at 60% 40%, rgba(255,0,150,.06) 0%, transparent 50%);
            animation: floating 20s ease-in-out infinite;
        }
        @keyframes floating { 0%,100%{transform:translateY(0) rotate(0)} 50%{transform:translateY(-18px) rotate(1.5deg)} }

        .hero-grid {
            position: absolute; inset: 0; opacity: .08;
            background-image: linear-gradient(rgba(0,255,157,.4) 1px, transparent 1px), linear-gradient(90deg, rgba(0,255,157,.4) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: gridPulse 4s ease-in-out infinite;
        }
        @keyframes gridPulse { 0%,100%{opacity:.08} 50%{opacity:.22} }

        .hero-content { text-align: center; z-index: 10; max-width: 860px; padding: 0 20px; }
        .hero-badge {
            display: inline-block; margin-bottom: 20px;
            padding: 8px 22px; border-radius: 50px;
            border: 1px solid rgba(0,255,157,.4);
            font-size: .85rem; letter-spacing: 2px; color: var(--green);
            background: rgba(0,255,157,.06);
        }
        .hero h1 {
            font-size: 4.2rem; font-weight: 900; line-height: 1.15; margin-bottom: 22px;
            background: linear-gradient(45deg, var(--green), var(--blue), var(--pink));
            -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent;
            animation: titleGlow 3s ease-in-out infinite;
        }
        @keyframes titleGlow {
            0%,100%{filter:drop-shadow(0 0 18px rgba(0,255,157,.5))}
            50%{filter:drop-shadow(0 0 38px rgba(0,162,255,.8))}
        }
        .hero p { font-size: 1.3rem; opacity: .88; line-height: 1.7; margin-bottom: 14px; }
        .hero-btns { display: flex; gap: 16px; justify-content: center; margin-top: 32px; flex-wrap: wrap; }
        .cta-button {
            display: inline-block; padding: 14px 38px;
            background: linear-gradient(45deg, var(--green), var(--blue));
            border: none; border-radius: 50px;
            color: #000; font-weight: 700; font-size: 1rem;
            text-decoration: none; cursor: pointer;
            transition: all .3s ease; position: relative; overflow: hidden;
        }
        .cta-button:hover { transform: translateY(-3px); box-shadow: 0 15px 35px rgba(0,255,157,.35); }
        .cta-outline {
            display: inline-block; padding: 14px 38px;
            background: transparent;
            border: 2px solid var(--green); border-radius: 50px;
            color: var(--green); font-weight: 700; font-size: 1rem;
            text-decoration: none; cursor: pointer;
            transition: all .3s ease;
        }
        .cta-outline:hover { background: rgba(0,255,157,.1); transform: translateY(-3px); }

        /* ========== INTRO CLIP SECTION ========== */
        #intro-clip {
            padding: 100px 20px;
            background: rgba(0,0,0,.25);
        }
        .clip-container { max-width: 1100px; margin: 0 auto; }
        .clip-inner {
            position: relative;
            background: rgba(255,255,255,.03);
            border: 1px solid rgba(0,255,157,.2);
            border-radius: 24px;
            overflow: hidden;
        }
        /* ---- Animated Intro Video (CSS/Canvas) ---- */
        #geoCanvas {
            width: 100%;
            height: 500px;
            display: block;
            background: #050d1a;
            cursor: pointer;
        }
        .clip-overlay-btn {
            position: absolute; top: 50%; left: 50%;
            transform: translate(-50%,-50%);
            width: 80px; height: 80px;
            background: rgba(0,255,157,.2);
            border: 3px solid var(--green);
            border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            font-size: 2rem; cursor: pointer;
            transition: all .3s ease;
            z-index: 5;
        }
        .clip-overlay-btn:hover { background: rgba(0,255,157,.35); transform: translate(-50%,-50%) scale(1.1); }
        .clip-overlay-btn.hidden { opacity: 0; pointer-events: none; }

        .clip-info { padding: 32px 40px; }
        .clip-info h3 { font-size: 1.7rem; font-weight: 700; margin-bottom: 12px; color: var(--green); }
        .clip-info p { opacity: .8; line-height: 1.8; font-size: 1rem; }
        .clip-tags { display: flex; gap: 10px; flex-wrap: wrap; margin-top: 16px; }
        .clip-tag {
            padding: 5px 14px; border-radius: 20px; font-size: .8rem;
            background: rgba(0,162,255,.1); border: 1px solid rgba(0,162,255,.3); color: var(--blue);
        }

        /* ========== STATS ========== */
        .stats-section { padding: 70px 20px; }
        .stats-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr)); gap: 24px; max-width: 1000px; margin: 0 auto; }
        .stat-card {
            text-align: center; padding: 36px 20px;
            background: rgba(255,255,255,.04);
            border: 1px solid rgba(0,255,157,.15);
            border-radius: 18px;
            transition: all .3s ease;
        }
        .stat-card:hover { border-color: var(--green); transform: translateY(-5px); background: rgba(0,255,157,.05); }
        .stat-number { font-size: 3rem; font-weight: 900; background: linear-gradient(45deg, var(--green), var(--blue)); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent; }
        .stat-label { margin-top: 8px; opacity: .75; font-size: .95rem; }

        /* ========== SERVICES ========== */
        .services { padding: 100px 20px; max-width: 1200px; margin: 0 auto; }
        .section-title {
            text-align: center; font-size: 2.8rem; font-weight: 700; margin-bottom: 16px;
            background: linear-gradient(45deg, var(--green), var(--blue));
            -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent;
        }
        .section-sub { text-align: center; opacity: .65; margin-bottom: 60px; font-size: 1.05rem; }
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(330px,1fr)); gap: 28px; }
        .service-card {
            background: rgba(255,255,255,.04); border: 1px solid rgba(0,255,157,.18);
            border-radius: 20px; padding: 38px; text-align: center;
            transition: all .4s ease; position: relative; overflow: hidden;
        }
        .service-card::before {
            content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0,255,157,.08), transparent);
            transition: left .6s ease;
        }
        .service-card:hover::before { left: 100%; }
        .service-card:hover { transform: translateY(-10px); border-color: rgba(0,255,157,.5); box-shadow: 0 20px 60px rgba(0,255,157,.15); }
        .service-icon { font-size: 3.5rem; margin-bottom: 18px; }
        .service-card h3 { font-size: 1.35rem; margin-bottom: 12px; font-weight: 600; }
        .service-card p { opacity: .75; line-height: 1.7; font-size: .95rem; }

        /* ========== TECHNOLOGY ========== */
        .technology { padding: 100px 20px; background: rgba(0,0,0,.25); }
        .tech-container { max-width: 1200px; margin: 0 auto; text-align: center; }
        .tech-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(190px,1fr)); gap: 18px; margin-top: 50px; }
        .tech-item {
            padding: 28px 18px; background: rgba(255,255,255,.04);
            border-radius: 14px; transition: all .3s ease;
            border: 1px solid rgba(0,162,255,.2);
        }
        .tech-item:hover { background: rgba(0,162,255,.08); transform: scale(1.05); border-color: var(--blue); }
        .tech-item h4 { font-size: 1.05rem; margin-bottom: 8px; color: var(--blue); }
        .tech-item p { opacity: .7; font-size: .88rem; }

        /* ========== ABOUT ========== */
        .about-section { padding: 100px 20px; }
        .about-container { max-width: 1100px; margin: 0 auto; display: grid; grid-template-columns: 1fr 1fr; gap: 60px; align-items: center; }
        .about-text h2 { font-size: 2.4rem; font-weight: 700; margin-bottom: 20px; background: linear-gradient(45deg,var(--green),var(--blue)); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent; }
        .about-text p { opacity: .8; line-height: 1.9; margin-bottom: 16px; }
        .about-visual { position: relative; }
        .about-map-anim { width: 100%; height: 320px; border-radius: 20px; border: 1px solid rgba(0,255,157,.2); overflow: hidden; }
        #mapCanvas { width: 100%; height: 100%; display: block; background: #050d1a; }

        /* ========== CONTACT ========== */
        .contact { padding: 100px 20px; max-width: 800px; margin: 0 auto; }
        .contact-form { background: rgba(255,255,255,.04); border-radius: 20px; padding: 40px; border: 1px solid rgba(0,255,157,.2); }
        .form-group { margin-bottom: 22px; }
        .form-group label { display: block; margin-bottom: 8px; font-weight: 500; font-size: .95rem; }
        .form-group input, .form-group textarea, .form-group select {
            width: 100%; padding: 14px; background: rgba(255,255,255,.08);
            border: 1px solid rgba(0,255,157,.25); border-radius: 10px;
            color: #fff; font-family: inherit; font-size: .95rem;
            transition: all .3s ease;
        }
        .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
            outline: none; border-color: var(--green); background: rgba(0,255,157,.05);
        }
        .form-group select option { background: #1a1a2e; }
        .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 18px; }

        /* ========== FOOTER ========== */
        footer {
            text-align: center; padding: 40px 20px;
            border-top: 1px solid rgba(0,255,157,.1);
            opacity: .6; font-size: .9rem;
        }

        /* ========== FLOATING PARTICLES ========== */
        .floating-element {
            position: fixed; width: 4px; height: 4px;
            background: var(--green); border-radius: 50%;
            animation: floatUp 8s linear infinite;
            pointer-events: none; z-index: 0;
        }
        @keyframes floatUp {
            0%{transform:translateY(100vh) translateX(0);opacity:0}
            10%{opacity:1} 90%{opacity:1}
            100%{transform:translateY(-100px) translateX(80px);opacity:0}
        }

        /* ========== RESPONSIVE ========== */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.4rem; }
            .hero p { font-size: 1.1rem; }
            .navbar { padding: 14px 18px; }
            .nav-links { display: none; }
            .services-grid { grid-template-columns: 1fr; }
            .about-container { grid-template-columns: 1fr; }
            .form-row { grid-template-columns: 1fr; }
            #geoCanvas { height: 300px; }
            .clip-info { padding: 24px 20px; }
        }
    </style>
</head>
<body>

<!-- NAV -->
<nav class="navbar" id="navbar">
    <div class="nav-container">
        <div class="logo">📐 ژئوماتیک مدرن کرمان</div>
        <ul class="nav-links">
            <li><a href="#home">خانه</a></li>
            <li><a href="#intro-clip">معرفی</a></li>
            <li><a href="#services">خدمات</a></li>
            <li><a href="#technology">تکنولوژی</a></li>
            <li><a href="#about">درباره ما</a></li>
            <li><a href="#contact">تماس</a></li>
        </ul>
    </div>
</nav>

<!-- HERO -->
<section class="hero" id="home">
    <div class="hero-bg"></div>
    <div class="hero-grid"></div>
    <div class="hero-content">
        <div class="hero-badge">MODERN GEOMATICS KERMAN</div>
        <h1>ژئوماتیک مدرن کرمان</h1>
        <p>مهندسی نقشه‌برداری با فناوری‌های روز دنیا</p>
        <p>دقت در هر اندازه‌گیری — کیفیت در هر پروژه — افتخار در هر خدمت</p>
        <div class="hero-btns">
            <a href="#intro-clip" class="cta-button">▶ تماشای معرفی</a>
            <a href="#services" class="cta-outline">مشاهده خدمات</a>
        </div>
    </div>
</section>

<!-- STATS -->
<section class="stats-section">
    <div class="stats-grid">
        <div class="stat-card">
            <div class="stat-number" data-target="15">0</div>
            <div class="stat-label">سال تجربه</div>
        </div>
        <div class="stat-card">
            <div class="stat-number" data-target="500">0</div>
            <div class="stat-label">پروژه موفق</div>
        </div>
        <div class="stat-card">
            <div class="stat-number" data-target="120">0</div>
            <div class="stat-label">مشتری راضی</div>
        </div>
        <div class="stat-card">
            <div class="stat-number" data-target="8">0</div>
            <div class="stat-label">متخصص حرفه‌ای</div>
        </div>
    </div>
</section>

<!-- INTRO CLIP -->
<section id="intro-clip">
    <div class="clip-container">
        <div class="section-title">کلیپ معرفی</div>
        <div class="section-sub">ژئوماتیک مدرن — آینده اندازه‌گیری زمین</div>
        <div class="clip-inner">
            <canvas id="geoCanvas"></canvas>
            <div class="clip-overlay-btn" id="playBtn" onclick="toggleAnimation()">▶</div>
            <div class="clip-info">
                <h3>🌐 ژئوماتیک مدرن کرمان</h3>
                <p>
                    ژئوماتیک (Geomatics) علم جمع‌آوری، پردازش و مدیریت داده‌های مکانی است.
                    این رشته ترکیبی از نقشه‌برداری کلاسیک، سیستم‌های اطلاعات جغرافیایی (GIS)،
                    سنجش از دور، فتوگرامتری و فناوری GPS/GNSS می‌باشد.
                    در کرمان، با توجه به گستردگی زمین‌های کشاورزی، معادن و پروژه‌های عمرانی،
                    نقشه‌برداری دقیق از اهمیت ویژه‌ای برخوردار است.
                </p>
                <div class="clip-tags">
                    <span class="clip-tag">GIS</span>
                    <span class="clip-tag">GPS/GNSS</span>
                    <span class="clip-tag">فتوگرامتری</span>
                    <span class="clip-tag">سنجش از دور</span>
                    <span class="clip-tag">کاداستر</span>
                    <span class="clip-tag">پهپاد</span>
                    <span class="clip-tag">لیزراسکن</span>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
    <h2 class="section-title">خدمات تخصصی</h2>
    <p class="section-sub">طیف کاملی از خدمات نقشه‌برداری با بهترین تجهیزات و متخصصان مجرب</p>
    <div class="services-grid">
        <div class="service-card">
            <div class="service-icon">🗺️</div>
            <h3>نقشه‌برداری توپوگرافی</h3>
            <p>تهیه نقشه‌های دقیق از وضعیت طبیعی زمین با استفاده از ابزارهای پیشرفته و روش‌های نوین اندازه‌گیری</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🏗️</div>
            <h3>نقشه‌برداری کاداستر</h3>
            <p>تعیین حدود و حقوق املاک، تهیه نقشه‌های کاداستری و انجام عملیات تفکیک و ادغام زمین</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🛰️</div>
            <h3>نقشه‌برداری GNSS</h3>
            <p>استفاده از تکنولوژی GPS/GNSS با دقت میلی‌متری برای پروژه‌های بزرگ مقیاس و کنترل شبکه</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🚁</div>
            <h3>فتوگرامتری پهپادی</h3>
            <p>تهیه نقشه‌های هوایی با پهپادهای پیشرفته و پردازش تصاویر با نرم‌افزارهای حرفه‌ای</p>
        </div>
        <div class="service-card">
            <div class="service-icon">🔬</div>
            <h3>اسکن لیزری سه‌بعدی</h3>
            <p>مستندسازی دقیق سازه‌ها، ساختمان‌ها و محیط‌های صنعتی با اسکنر لیزری پیشرفته</p>
        </div>
        <div class="service-card">
            <div class="service-icon">💻</div>
            <h3>GIS و مدل‌سازی</h3>
            <p>تحلیل داده‌های مکانی، مدل‌سازی سه‌بعدی، ایجاد پایگاه داده جغرافیایی و گزارش‌گیری</p>
        </div>
    </div>
</section>

<!-- TECHNOLOGY -->
<section class="technology" id="technology">
    <div class="tech-container">
        <h2 class="section-title">تکنولوژی‌های پیشرفته</h2>
        <p class="section-sub">مجهز به روزآمدترین تجهیزات نقشه‌برداری کشور</p>
        <div class="tech-grid">
            <div class="tech-item"><h4>Total Station</h4><p>دستگاه‌های الکترونیکی دقیق</p></div>
            <div class="tech-item"><h4>GPS/GNSS RTK</h4><p>موقعیت‌یابی بلادرنگ دقیق</p></div>
            <div class="tech-item"><h4>Laser Scanner</h4><p>اسکن سه‌بعدی لیزری</p></div>
            <div class="tech-item"><h4>UAV / Drone</h4><p>پهپادهای نقشه‌برداری</p></div>
            <div class="tech-item"><h4>AutoCAD / Civil3D</h4><p>طراحی مهندسی کامپیوتری</p></div>
            <div class="tech-item"><h4>ArcGIS / QGIS</h4><p>سیستم اطلاعات جغرافیایی</p></div>
            <div class="tech-item"><h4>Pix4D / Agisoft</h4><p>پردازش تصاویر هوایی</p></div>
            <div class="tech-item"><h4>CORS Network</h4><p>شبکه ایستگاه‌های دائمی</p></div>
        </div>
    </div>
</section>

<!-- ABOUT -->
<section class="about-section" id="about">
    <div class="about-container">
        <div class="about-text">
            <h2>درباره ژئوماتیک مدرن کرمان</h2>
            <p>
                شرکت ژئوماتیک مدرن کرمان با بیش از ۱۵ سال تجربه در حوزه مهندسی نقشه‌برداری،
                یکی از پیشگامان این صنعت در استان کرمان است.
            </p>
            <p>
                با بهره‌گیری از متخصصان مجرب و فناوری‌های روز دنیا، خدمات جامعی در حوزه‌های
                توپوگرافی، کاداستر، GIS، فتوگرامتری و سنجش از دور ارائه می‌دهیم.
            </p>
            <p>
                هدف ما ارتقاء کیفیت پروژه‌های عمرانی، معدنی و شهری استان کرمان از طریق
                اندازه‌گیری‌های دقیق و داده‌های قابل اعتماد است.
            </p>
            <a href="#contact" class="cta-button" style="margin-top:20px; display:inline-block">تماس با ما</a>
        </div>
        <div class="about-visual">
            <div class="about-map-anim">
                <canvas id="mapCanvas"></canvas>
            </div>
        </div>
    </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
    <h2 class="section-title">تماس با ما</h2>
    <p class="section-sub">برای دریافت مشاوره رایگان با ما در تماس باشید</p>
    <div class="contact-form">
        <div class="form-row">
            <div class="form-group">
                <label for="name">نام و نام خانوادگی *</label>
                <input type="text" id="name" placeholder="مثال: علی احمدی">
            </div>
            <div class="form-group">
                <label for="phone">شماره تماس *</label>
                <input type="tel" id="phone" placeholder="09XX-XXX-XXXX">
            </div>
        </div>
        <div class="form-group">
            <label for="email">ایمیل</label>
            <input type="email" id="email" placeholder="example@gmail.com">
        </div>
        <div class="form-group">
            <label for="project">نوع پروژه</label>
            <select id="project">
                <option value="">انتخاب کنید...</option>
                <option>نقشه‌برداری توپوگرافی</option>
                <option>کاداستر و تفکیک</option>
                <option>فتوگرامتری هوایی</option>
                <option>اسکن لیزری</option>
                <option>GIS و سیستم اطلاعات جغرافیایی</option>
                <option>GNSS و موقعیت‌یابی</option>
                <option>سایر</option>
            </select>
        </div>
        <div class="form-group">
            <label for="message">توضیحات پروژه</label>
            <textarea id="message" rows="4" placeholder="لطفاً جزئیات پروژه خود را بنویسید..."></textarea>
        </div>
        <button class="cta-button" onclick="submitForm()" style="width:100%;font-size:1.05rem;padding:16px">ارسال درخواست مشاوره</button>
    </div>
</section>

<!-- FOOTER -->
<footer>
    <p>© ۱۴۰۳ ژئوماتیک مدرن کرمان — تمامی حقوق محفوظ است</p>
    <p style="margin-top:8px; font-size:.8rem">📍 کرمان، ایران &nbsp;|&nbsp; 📞 ۰۳۴-XXXX-XXXX &nbsp;|&nbsp; 📧 info@geomatics-kerman.ir</p>
</footer>

<!-- PARTICLES -->
<div class="floating-element" style="left:8%;animation-delay:0s"></div>
<div class="floating-element" style="left:22%;animation-delay:2s;background:#00a2ff"></div>
<div class="floating-element" style="left:55%;animation-delay:5s"></div>
<div class="floating-element" style="left:75%;animation-delay:3s;background:#ff009a"></div>
<div class="floating-element" style="left:90%;animation-delay:7s;background:#00a2ff"></div>

<script>
/* ===================== NAVBAR ===================== */
window.addEventListener('scroll', () => {
    document.getElementById('navbar').classList.toggle('scrolled', window.scrollY > 50);
});

/* ===================== COUNTERS ===================== */
function animateCounter(el) {
    const target = parseInt(el.dataset.target);
    let current = 0;
    const step = Math.ceil(target / 60);
    const timer = setInterval(() => {
        current = Math.min(current + step, target);
        el.textContent = current + (target >= 100 ? '+' : '');
        if (current >= target) clearInterval(timer);
    }, 30);
}
const counterObserver = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) { animateCounter(e.target); counterObserver.unobserve(e.target); } });
}, { threshold: 0.5 });
document.querySelectorAll('.stat-number').forEach(el => counterObserver.observe(el));

/* ===================== SCROLL ANIMATIONS ===================== */
const fadeObserver = new IntersectionObserver(entries => {
    entries.forEach(e => {
        if (e.isIntersecting) { e.target.style.opacity = '1'; e.target.style.transform = 'translateY(0)'; }
    });
}, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });
document.querySelectorAll('.service-card, .tech-item, .stat-card').forEach(el => {
    el.style.opacity = '0'; el.style.transform = 'translateY(28px)';
    el.style.transition = 'opacity .6s ease, transform .6s ease';
    fadeObserver.observe(el);
});

/* ===================== FORM ===================== */
function submitForm() {
    const name = document.getElementById('name').value.trim();
    const phone = document.getElementById('phone').value.trim();
    if (!name || !phone) { alert('لطفاً نام و شماره تماس را وارد کنید.'); return; }
    alert('✅ درخواست شما با موفقیت ارسال شد!\nبه زودی کارشناسان ما با شما تماس خواهند گرفت.');
    ['name','phone','email','message'].forEach(id => document.getElementById(id).value = '');
    document.getElementById('project').value = '';
}

/* ===================== DYNAMIC PARTICLES ===================== */
setInterval(() => {
    const p = document.createElement('div');
    p.className = 'floating-element';
    p.style.cssText = `left:${Math.random()*100}%;animation-delay:0s;animation-duration:${8+Math.random()*5}s;position:fixed;background:${['#00ff9d','#00a2ff','#ff009a'][Math.floor(Math.random()*3)]};z-index:0`;
    document.body.appendChild(p);
    setTimeout(() => p.remove(), 13000);
}, 2500);

/* ===================== INTRO CLIP CANVAS ===================== */
const canvas = document.getElementById('geoCanvas');
const ctx = canvas.getContext('2d');
let animRunning = false;
let animFrame;
let phase = 0;
let dots = [];
let connections = [];
let scanLine = 0;
let textAlpha = 0;
let textPhase = 0;

function resizeCanvas() {
    canvas.width = canvas.offsetWidth;
    canvas.height = canvas.offsetHeight;
}
resizeCanvas();
window.addEventListener('resize', resizeCanvas);

// Geo nodes
function initDots() {
    dots = [];
    const n = 28;
    for (let i = 0; i < n; i++) {
        dots.push({
            x: Math.random() * canvas.width,
            y: Math.random() * canvas.height,
            vx: (Math.random() - 0.5) * 0.4,
            vy: (Math.random() - 0.5) * 0.4,
            r: Math.random() * 3 + 1.5,
            pulse: Math.random() * Math.PI * 2
        });
    }
}
initDots();

const introTexts = [
    { text: 'ژئوماتیک مدرن کرمان', size: 42, color: '#00ff9d', t: 0 },
    { text: 'Modern Geomatics Kerman', size: 22, color: '#00a2ff', t: 80 },
    { text: 'نقشه‌برداری · GIS · فتوگرامتری · GNSS', size: 18, color: '#ffffff', t: 160 },
    { text: 'دقت در هر اندازه‌گیری', size: 20, color: '#ff009a', t: 240 },
];

function drawIntro(t) {
    const W = canvas.width, H = canvas.height;
    ctx.clearRect(0, 0, W, H);

    // Background
    const bg = ctx.createRadialGradient(W/2, H/2, 0, W/2, H/2, Math.max(W,H)/1.4);
    bg.addColorStop(0, '#071428');
    bg.addColorStop(1, '#020810');
    ctx.fillStyle = bg; ctx.fillRect(0, 0, W, H);

    // Grid
    ctx.strokeStyle = 'rgba(0,255,157,0.06)';
    ctx.lineWidth = 1;
    for (let x = 0; x < W; x += 50) { ctx.beginPath(); ctx.moveTo(x,0); ctx.lineTo(x,H); ctx.stroke(); }
    for (let y = 0; y < H; y += 50) { ctx.beginPath(); ctx.moveTo(0,y); ctx.lineTo(W,y); ctx.stroke(); }

    // Scan line
    scanLine = (scanLine + 1.2) % H;
    const sg = ctx.createLinearGradient(0, scanLine-12, 0, scanLine+12);
    sg.addColorStop(0,'rgba(0,255,157,0)');
    sg.addColorStop(0.5,'rgba(0,255,157,0.25)');
    sg.addColorStop(1,'rgba(0,255,157,0)');
    ctx.fillStyle = sg; ctx.fillRect(0, scanLine-12, W, 24);

    // Update & draw dots
    dots.forEach(d => {
        d.x += d.vx; d.y += d.vy;
        if (d.x < 0 || d.x > W) d.vx *= -1;
        if (d.y < 0 || d.y > H) d.vy *= -1;
        d.pulse += 0.04;
        const glow = Math.sin(d.pulse) * 0.5 + 0.5;
        const grd = ctx.createRadialGradient(d.x, d.y, 0, d.x, d.y, d.r * 3);
        grd.addColorStop(0, `rgba(0,255,157,${0.6 + glow*0.4})`);
        grd.addColorStop(1, 'rgba(0,255,157,0)');
        ctx.beginPath(); ctx.arc(d.x, d.y, d.r * (1 + glow*0.4), 0, Math.PI*2);
        ctx.fillStyle = grd; ctx.fill();
    });

    // Connections
    for (let i = 0; i < dots.length; i++) {
        for (let j = i+1; j < dots.length; j++) {
            const dx = dots[i].x - dots[j].x, dy = dots[i].y - dots[j].y;
            const dist = Math.sqrt(dx*dx + dy*dy);
            if (dist < 150) {
                const alpha = (1 - dist/150) * 0.35;
                ctx.strokeStyle = `rgba(0,162,255,${alpha})`;
                ctx.lineWidth = 1;
                ctx.beginPath(); ctx.moveTo(dots[i].x, dots[i].y); ctx.lineTo(dots[j].x, dots[j].y); ctx.stroke();
            }
        }
    }

    // Rotating circle
    const cx = W/2, cy = H/2;
    ctx.save();
    ctx.translate(cx, cy);
    ctx.rotate(t * 0.008);
    ctx.strokeStyle = 'rgba(0,255,157,0.15)';
    ctx.lineWidth = 1;
    ctx.setLineDash([8,12]);
    ctx.beginPath(); ctx.arc(0, 0, Math.min(W,H)*0.32, 0, Math.PI*2); ctx.stroke();
    ctx.setLineDash([4,18]);
    ctx.strokeStyle = 'rgba(0,162,255,0.1)';
    ctx.beginPath(); ctx.arc(0, 0, Math.min(W,H)*0.22, 0, Math.PI*2); ctx.stroke();
    ctx.setLineDash([]);
    ctx.restore();

    // Target crosshair
    const cr = 36;
    ctx.strokeStyle = 'rgba(0,255,157,0.5)'; ctx.lineWidth = 1.5;
    ctx.beginPath(); ctx.moveTo(cx-cr, cy); ctx.lineTo(cx-8, cy);
    ctx.moveTo(cx+8, cy); ctx.lineTo(cx+cr, cy);
    ctx.moveTo(cx, cy-cr); ctx.lineTo(cx, cy-8);
    ctx.moveTo(cx, cy+8); ctx.lineTo(cx, cy+cr);
    ctx.stroke();
    ctx.strokeStyle = 'rgba(0,255,157,0.3)';
    ctx.beginPath(); ctx.arc(cx, cy, 18, 0, Math.PI*2); ctx.stroke();

    // Coordinates display
    ctx.font = '11px monospace';
    ctx.fillStyle = 'rgba(0,255,157,0.5)';
    ctx.fillText(`LAT: 30°17'N  LON: 57°04'E`, 16, H-30);
    ctx.fillText(`ALT: 1755m  KERN: ${(Math.sin(t*0.02)*0.001+0.001).toFixed(4)}m`, 16, H-14);

    // Intro texts
    textPhase = t;
    introTexts.forEach(item => {
        const elapsed = t - item.t;
        if (elapsed < 0) return;
        let alpha = Math.min(elapsed / 25, 1);
        if (elapsed > 60) alpha = Math.max(1 - (elapsed-60)/20, 0);
        if (alpha <= 0) return;
        ctx.save();
        ctx.globalAlpha = alpha;
        ctx.font = `bold ${item.size}px Vazirmatn, sans-serif`;
        ctx.fillStyle = item.color;
        ctx.textAlign = 'center';
        const yOff = item.t === 0 ? H/2 - 20 : item.t === 80 ? H/2 + 22 : item.t === 160 ? H/2 + 56 : H/2 + 88;
        ctx.fillText(item.text, W/2, yOff);
        ctx.restore();
    });

    // Corner brackets
    const bS = 22, bT = 2;
    ctx.strokeStyle = 'rgba(0,255,157,0.4)'; ctx.lineWidth = bT;
    [[16,16,1,1],[W-16,16,-1,1],[16,H-16,1,-1],[W-16,H-16,-1,-1]].forEach(([x,y,sx,sy]) => {
        ctx.beginPath();
        ctx.moveTo(x, y+sy*bS); ctx.lineTo(x, y); ctx.lineTo(x+sx*bS, y);
        ctx.stroke();
    });
}

let tick = 0;
function animLoop() {
    drawIntro(tick++);
    if (tick > 320) tick = 0;
    animFrame = requestAnimationFrame(animLoop);
}

function toggleAnimation() {
    const btn = document.getElementById('playBtn');
    if (!animRunning) {
        animRunning = true;
        btn.classList.add('hidden');
        animLoop();
    } else {
        animRunning = false;
        btn.textContent = '▶';
        btn.classList.remove('hidden');
        cancelAnimationFrame(animFrame);
    }
}
canvas.addEventListener('click', () => {
    if (animRunning) toggleAnimation();
});
// Auto-start when visible
const clipObserver = new IntersectionObserver(entries => {
    entries.forEach(e => {
        if (e.isIntersecting && !animRunning) toggleAnimation();
        if (!e.isIntersecting && animRunning) { cancelAnimationFrame(animFrame); animRunning = false; tick = 0; document.getElementById('playBtn').classList.remove('hidden'); }
    });
}, { threshold: 0.4 });
clipObserver.observe(canvas);

/* ===================== MAP CANVAS ===================== */
const mc = document.getElementById('mapCanvas');
const mx = mc.getContext('2d');
function resizeMap() { mc.width = mc.offsetWidth; mc.height = mc.offsetHeight; }
resizeMap();
window.addEventListener('resize', resizeMap);

const mapPoints = [
    {x:.3,y:.4,label:'کرمان'},{x:.5,y:.55,label:'رفسنجان'},{x:.7,y:.3,label:'زرند'},
    {x:.2,y:.7,label:'جیرفت'},{x:.6,y:.2,label:'بافق'},{x:.8,y:.65,label:'بم'},
    {x:.4,y:.8,label:'سیرجان'},{x:.15,y:.3,label:'شهربابک'},
];
let mapTick = 0;
function drawMap() {
    const W = mc.width, H = mc.height;
    mx.clearRect(0,0,W,H);
    const mbg = mx.createLinearGradient(0,0,W,H);
    mbg.addColorStop(0,'#050d1a'); mbg.addColorStop(1,'#071428');
    mx.fillStyle = mbg; mx.fillRect(0,0,W,H);

    mx.strokeStyle='rgba(0,255,157,0.05)'; mx.lineWidth=1;
    for(let x=0;x<W;x+=30){mx.beginPath();mx.moveTo(x,0);mx.lineTo(x,H);mx.stroke();}
    for(let y=0;y<H;y+=30){mx.beginPath();mx.moveTo(0,y);mx.lineTo(W,y);mx.stroke();}

    const pts = mapPoints.map(p => ({x:p.x*W, y:p.y*H, label:p.label}));
    pts.forEach((a,i) => {
        pts.forEach((b,j) => {
            if(j<=i) return;
            const d = Math.hypot(a.x-b.x,a.y-b.y);
            if(d<W*0.45){
                const alpha = (1-d/(W*0.45))*0.3;
                mx.strokeStyle=`rgba(0,162,255,${alpha})`; mx.lineWidth=1;
                mx.beginPath(); mx.moveTo(a.x,a.y); mx.lineTo(b.x,b.y); mx.stroke();
            }
        });
    });

    pts.forEach((p,i) => {
        const pulse = Math.sin(mapTick*0.05 + i) * 0.5 + 0.5;
        const rOuter = 6 + pulse * 6;
        mx.beginPath(); mx.arc(p.x,p.y,rOuter,0,Math.PI*2);
        mx.fillStyle=`rgba(0,255,157,${0.1*pulse})`; mx.fill();
        mx.beginPath(); mx.arc(p.x,p.y,4,0,Math.PI*2);
        mx.fillStyle='#00ff9d'; mx.fill();
        mx.font='bold 11px Vazirmatn,sans-serif';
        mx.fillStyle='rgba(255,255,255,0.85)';
        mx.textAlign='center';
        mx.fillText(p.label, p.x, p.y-10);
    });

    mapTick++;
    requestAnimationFrame(drawMap);
}
drawMap();
</script>
</body>
</html>
