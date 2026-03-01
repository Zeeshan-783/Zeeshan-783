<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Faisal Arshad · mobile studio</title>
    <!-- Font & icon sets (minimal) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            background: #f7fafc;
            color: #1a202c;
            line-height: 1.5;
            padding: 2rem 1rem;
        }
        .container {
            max-width: 1280px;
            margin: 0 auto;
            background: white;
            border-radius: 2.5rem;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.15);
            overflow: hidden;
            border: 1px solid #edf2f7;
        }
        .inner {
            padding: 2.5rem 2rem;
        }
        /* header banner emulation using gradient + wave feel */
        .hero {
            background: linear-gradient(125deg, #0a4b7a 0%, #1e7e5c 60%, #5b3b8c 100%);
            border-radius: 2rem 2rem 2rem 2rem;
            padding: 3rem 2rem 2.5rem 2rem;
            margin-bottom: 2rem;
            color: white;
            position: relative;
            isolation: isolate;
            box-shadow: inset 0 -2px 4px rgba(255,255,255,0.1);
        }
        .hero::after {
            content: '';
            position: absolute;
            inset: 0;
            background: radial-gradient(circle at 70% 30%, rgba(255,255,255,0.1) 0%, transparent 50%);
            pointer-events: none;
            z-index: 0;
            border-radius: inherit;
        }
        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
        }
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            line-height: 1.2;
            text-shadow: 0 4px 12px rgba(0,0,0,0.2);
        }
        .hero .sub {
            font-size: 1.3rem;
            font-weight: 400;
            margin-top: 0.5rem;
            opacity: 0.9;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.75rem;
            flex-wrap: wrap;
        }
        .hero .sub span {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(4px);
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.95rem;
            font-weight: 500;
            border: 1px solid rgba(255,255,255,0.2);
        }
        /* typing bar – simplified as static highlight */
        .typing-tag {
            background: rgba(0,0,0,0.3);
            border-radius: 60px;
            padding: 0.9rem 1.8rem;
            margin: 2rem auto 0;
            max-width: 800px;
            border: 1px solid rgba(255,255,255,0.15);
            color: #f0f9ff;
            font-size: 1.1rem;
            font-weight: 400;
            backdrop-filter: blur(4px);
        }
        .typing-tag i {
            color: #fcd34d;
            margin-right: 8px;
        }
        /* contact row */
        .contact-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.75rem;
            margin: 1.8rem 0 0.5rem;
        }
        .badge-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(255,255,255,0.1);
            border: 1px solid rgba(255,255,255,0.2);
            color: white;
            padding: 0.6rem 1.4rem;
            border-radius: 60px;
            font-weight: 500;
            font-size: 0.95rem;
            transition: 0.2s;
            backdrop-filter: blur(4px);
            text-decoration: none;
        }
        .badge-btn:hover {
            background: rgba(255,255,255,0.25);
            transform: scale(1.02);
            border-color: white;
        }
        .badge-btn i {
            font-size: 1.1rem;
        }
        .profile-badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.5rem 1rem;
            margin: 1rem 0;
            color: #e2e8f0;
        }
        .profile-badges span {
            background: #2d3748;
            padding: 0.3rem 1rem;
            border-radius: 30px;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }
        .cta-box {
            background: #f1f5f9;
            border-left: 6px solid #0ea5e9;
            border-radius: 20px;
            padding: 1rem 2rem;
            margin: 2rem 0 1rem;
            font-weight: 600;
            font-size: 1.2rem;
            display: inline-block;
            color: #0c4a6e;
        }
        /* section titles */
        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin: 2.5rem 0 1.5rem;
            letter-spacing: -0.01em;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 3px solid #e2e8f0;
            padding-bottom: 0.5rem;
        }
        .section-title i {
            color: #0ea5e9;
            font-size: 2rem;
        }
        .badge-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin: 1.2rem 0;
        }
        .tech-badge {
            background: #eef2ff;
            color: #1e293b;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            font-weight: 500;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            border: 1px solid #cbd5e1;
            transition: 0.1s;
        }
        .tech-badge i {
            color: #2563eb;
        }
        /* app grid & cards */
        .app-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.2rem;
            margin: 1.5rem 0;
        }
        .app-card {
            background: #ffffff;
            border: 1px solid #e9eef3;
            border-radius: 24px;
            padding: 1.2rem 0.8rem;
            text-align: center;
            box-shadow: 0 8px 15px -6px rgba(0,0,0,0.05);
            transition: all 0.15s;
        }
        .app-card:hover {
            border-color: #b1c3d8;
            box-shadow: 0 20px 25px -12px rgba(0,115,230,0.15);
            transform: translateY(-4px);
        }
        .app-icon {
            width: 64px;
            height: 64px;
            border-radius: 18px;
            margin: 0 auto 0.8rem;
            background: #f1f4f9;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: #1f2a44;
            box-shadow: 0 4px 8px rgba(0,0,0,0.02);
        }
        .app-icon img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 18px;
        }
        .app-name {
            font-weight: 700;
            margin-bottom: 0.25rem;
        }
        .app-meta {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.4rem;
            margin: 0.6rem 0;
            font-size: 0.7rem;
        }
        .store-badge-small {
            background: #2c3e50;
            color: white;
            padding: 0.2rem 0.6rem;
            border-radius: 30px;
            font-size: 0.7rem;
            display: inline-block;
            text-decoration: none;
        }
        .rating {
            background: #fbbf24;
            color: #1e293b;
            padding: 0.2rem 0.7rem;
            border-radius: 30px;
            font-weight: 600;
            font-size: 0.75rem;
        }
        /* featured repos */
        .repo-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin: 1.5rem 0;
        }
        .repo-card {
            background: #f8fafc;
            border: 1px solid #dee7ef;
            border-radius: 40px;
            padding: 0.5rem 1.2rem;
            font-size: 0.9rem;
            font-weight: 500;
            color: #0f2b42;
            transition: 0.1s;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            text-decoration: none;
            flex: 0 1 auto;
        }
        .repo-card i {
            color: #24292e;
        }
        .repo-card:hover {
            background: #e6edf5;
            border-color: #6f8fbb;
        }
        /* github stats row */
        .stats-flex {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
            justify-content: center;
            margin: 2rem 0 0.5rem;
        }
        .stat-item {
            background: #f1f6fc;
            border-radius: 30px;
            padding: 0.8rem 2rem;
            border: 1px solid #cfdeed;
        }
        .cert-badge {
            background: #ebf5ff;
            border-radius: 40px;
            padding: 0.8rem 1.8rem;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            font-weight: 500;
            margin: 0.2rem;
            border: 1px solid #b7d3f0;
        }
        hr {
            border: none;
            border-top: 2px dashed #d9e2ef;
            margin: 2rem 0;
        }
        .footer-note {
            text-align: center;
            font-size: 1.2rem;
            font-weight: 400;
            background: #f0f7ff;
            padding: 1.5rem;
            border-radius: 60px;
            margin-top: 2rem;
        }
        /* spacing */
        .mt-2 { margin-top: 1rem; }
        .mb-1 { margin-bottom: 0.5rem; }
        .text-muted { color: #4b5b6b; }
        i { margin-right: 4px; }
    </style>
</head>
<body>
<div class="container">
    <div class="inner">
        <!-- Hero banner (modern wave interpretation) -->
        <div class="hero">
            <div class="hero-content">
                <h1>Faisal Arshad</h1>
                <div class="sub">
                    <span>📱 Mobile App Engineer · 5+ Years</span>
                    <span>⚡ 10+ Published Apps</span>
                </div>

                <!-- Typing animation replacement (clean marquee style) -->
                <div class="typing-tag">
                    <i class="fa-regular fa-keyboard"></i> Cross‑platform · Native · FlutterFlow · Payments · CI/CD · Make.com automation
                </div>

                <!-- Contact row 1 -->
                <div class="contact-row">
                    <a href="mailto:faisalarshadciit@gmail.com" class="badge-btn"><i class="fa-regular fa-envelope"></i> Email</a>
                    <a href="https://wa.me/+923088649850" class="badge-btn"><i class="fa-brands fa-whatsapp"></i> WhatsApp</a>
                    <a href="https://www.linkedin.com/in/faisal-arshad-bb5ab1153" class="badge-btn"><i class="fa-brands fa-linkedin-in"></i> LinkedIn</a>
                    <a href="https://twitter.com/faisalarshad850" class="badge-btn"><i class="fa-brands fa-x-twitter"></i> X</a>
                </div>
                <!-- Row 2 freelance -->
                <div class="contact-row">
                    <a href="https://www.upwork.com/freelancers/~0143722ece1833a4ed" class="badge-btn"><i class="fa-brands fa-upwork"></i> Upwork</a>
                    <a href="https://www.fiverr.com/faisalarshad850" class="badge-btn"><i class="fa-brands fa-fiverr"></i> Fiverr</a>
                </div>

                <!-- profile badges -->
                <div class="profile-badges">
                    <span><i class="fa-regular fa-star"></i> 130+ GitHub stars</span>
                    <span><i class="fa-regular fa-user"></i> 20+ followers</span>
                    <span><i class="fa-regular fa-eye"></i> 4.2k profile views</span>
                </div>

                <!-- callout -->
                <div style="margin-top: 1.8rem;">
                    <span class="cta-box"><i class="fa-regular fa-hand-point-right"></i> Open for freelance & full‑time opportunities 🚀</span>
                </div>
            </div>
        </div>

        <!-- about section simplified -->
        <div style="display: flex; flex-wrap: wrap; gap: 1.8rem; margin: 1.8rem 0 0.5rem;">
            <div style="flex: 2; min-width: 280px;">
                <h2 class="section-title"><i class="fa-regular fa-user"></i> about</h2>
                <p style="font-size: 1.1rem; color: #1e293b;">👨‍💻 Mobile developer with <strong>5+ years</strong> building cross‑platform & native apps (Flutter, FlutterFlow, Android/Kotlin, Swift, KMP). Skilled in <strong>payment integrations, monetization (RevenueCat, Qonversion, AdMob)</strong>, and fast prototyping. Published 10+ apps serving thousands of users daily. Certified Make.com automation specialist.</p>
                <p style="margin-top: 0.8rem;">✨ <em>“I build apps that are fast, reliable, and delightful to use.”</em></p>
            </div>
        </div>

        <!-- tech stack (condensed but complete) -->
        <h2 class="section-title"><i class="fa-solid fa-code"></i> tech stack</h2>
        <div class="badge-cloud">
            <span class="tech-badge"><i class="fa-brands fa-java"></i> Java</span>
            <span class="tech-badge"><i class="fa-solid fa-leaf"></i> Kotlin</span>
            <span class="tech-badge"><i class="fa-brands fa-dart"></i> Dart</span>
            <span class="tech-badge"><i class="fa-brands fa-swift"></i> Swift</span>
            <span class="tech-badge"><i class="fa-brands fa-flutter"></i> Flutter</span>
            <span class="tech-badge"><i class="fa-solid fa-water"></i> FlutterFlow</span>
            <span class="tech-badge"><i class="fa-brands fa-android"></i> Android</span>
            <span class="tech-badge"><i class="fa-brands fa-apple"></i> iOS</span>
            <span class="tech-badge"><i class="fa-solid fa-cube"></i> Provider</span>
            <span class="tech-badge"><i class="fa-solid fa-bolt"></i> GetX</span>
            <span class="tech-badge"><i class="fa-solid fa-droplet"></i> Riverpod</span>
            <span class="tech-badge"><i class="fa-solid fa-fire"></i> Firebase</span>
            <span class="tech-badge"><i class="fa-solid fa-database"></i> Supabase</span>
            <span class="tech-badge"><i class="fa-solid fa-chart-line"></i> RevenueCat</span>
            <span class="tech-badge"><i class="fa-solid fa-bell"></i> OneSignal</span>
            <span class="tech-badge"><i class="fa-solid fa-credit-card"></i> Stripe</span>
            <span class="tech-badge"><i class="fa-regular fa-credit-card"></i> Google Pay</span>
            <span class="tech-badge"><i class="fa-brands fa-apple-pay"></i> Apple Pay</span>
            <span class="tech-badge"><i class="fa-solid fa-wallet"></i> JazzCash</span>
            <span class="tech-badge"><i class="fa-brands fa-git-alt"></i> Git</span>
            <span class="tech-badge"><i class="fa-brands fa-github"></i> GitHub</span>
            <span class="tech-badge"><i class="fa-brands fa-gitlab"></i> GitLab</span>
            <span class="tech-badge"><i class="fa-brands fa-jira"></i> Jira</span>
            <span class="tech-badge"><i class="fa-brands fa-figma"></i> Figma</span>
            <span class="tech-badge"><i class="fa-brands fa-android-studio"></i> Android Studio</span>
            <span class="tech-badge"><i class="fa-brands fa-xcode"></i> Xcode</span>
            <span class="tech-badge"><i class="fa-solid fa-rocket"></i> GitHub Actions</span>
            <span class="tech-badge"><i class="fa-solid fa-bolt"></i> Shorebird</span>
            <span class="tech-badge"><i class="fa-solid fa-robot"></i> Make.com</span>
        </div>

        <!-- published apps summary + grid -->
        <h2 class="section-title"><i class="fa-solid fa-mobile-screen"></i> published apps (10+ total)</h2>
        <div style="display: flex; gap: 1rem; flex-wrap: wrap; margin-bottom: 1.5rem;">
            <span class="tech-badge" style="background:#dbeafe;"><i class="fa-brands fa-google-play"></i> 200K+ Installs</span>
            <span class="tech-badge" style="background:#dbeafe;"><i class="fa-regular fa-star"></i> 4.6★ avg (6K+ reviews)</span>
        </div>

        <div class="app-grid">
            <!-- Kivora -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/Th7gvhrIMUAleNekY22tEY4JDe5EavV2xyA0t6z8zDcnhP_iG1uyXWFq9HBb_jhke90=w240-h480" alt="Kivora"></div>
                <div class="app-name">Kivora – Trading Mindset</div>
                <div class="app-meta"><span class="rating">5.0★</span><span>1K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- Market Countdown -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/tU7NVq3N_BtfVvlHUtcOpFs3D-9s7TXg4or_G9p2z5jbAzl63NZNZoG41MO50XJ0kg=w240-h480" alt="Market Countdown"></div>
                <div class="app-name">Market Countdown Times</div>
                <div class="app-meta"><span class="rating">4.96★</span><span>5K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- MarketBeats -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/DZftg28SuucshlLeWKvzCDfYwFm7ucUbY0Zv-bcDdP-M7_7AeIoqq_ZkyRK7b1_ZQRE=w240-h480" alt="MarketBeats"></div>
                <div class="app-name">MarketBeats – Activity</div>
                <div class="app-meta"><span class="rating">5.0★</span><span>5K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- Market Opens -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/B3NMFWjUx5B5iXyHLOC1_o70Thzq0XCLQEkp2bt3CCKkhHKOjhE6_ycKj1qMTJhMlHo=w240-h480" alt="Market Opens"></div>
                <div class="app-name">Market Opens</div>
                <div class="app-meta"><span class="rating">4.7★</span><span>10K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- Pakistan Petrol Price -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/ydoQ92cr0Z_PHVXur-YuVvRSNbi46DzqH35tQ19I4nWuCGs9d0_4BpOkP09vT4IxEg=w240-h480" alt="Petrol Price"></div>
                <div class="app-name">Pakistan Petrol Price</div>
                <div class="app-meta"><span class="rating">4.5★</span><span>100K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- Pakistani Brands -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/3DlnF-fz8otJnyX6poWXHaiM8qPWDiiMdiSWwXnhNKkPcWoo00E4Jf8rLCCl0q8be4M=w240-h480" alt="Pakistani Brands"></div>
                <div class="app-name">Pakistani Brands</div>
                <div class="app-meta"><span class="rating">4.1★</span><span>5K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- Motorway Conditions -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/kdQxi_pECUJQbMop-Aid-H4xc88eHplmhELPO4S31lkecDMnlk_0xVMwZMdIb13qmQ=w240-h480" alt="Motorway Conditions"></div>
                <div class="app-name">Motorway Road Conditions</div>
                <div class="app-meta"><span class="rating">4.6★</span><span>10K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
            <!-- Moye Moye -->
            <div class="app-card">
                <div class="app-icon"><img src="https://play-lh.googleusercontent.com/DTQJK3HLPx539hWwb_-DqPph34qrUql9d5ynuST6WepHMe42Z73xr5HV5eHVQX5JDU0=w240-h480" alt="Moye Moye"></div>
                <div class="app-name">Moye Moye – Weather Fun</div>
                <div class="app-meta"><span class="rating">5.0★</span><span>1K+</span></div>
                <div><a href="#" class="store-badge-small">Google</a> <a href="#" class="store-badge-small">App Store</a></div>
            </div>
        </div>
        <p class="text-muted" style="margin-top: -0.5rem;">➕ many more: STINU, Position Pal, FX Meter, Aajizz, Food Calories, Pakistan Quotes, LylaCart…</p>

        <!-- featured repositories -->
        <h2 class="section-title"><i class="fa-regular fa-folder-open"></i> featured repositories</h2>
        <div class="repo-row">
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> QRCode-Generator-Android</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> Flutter-FoodDelivery-UI</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> WeatherApp-Flutter</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> LinkedIn-Post-Fetcher</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> EventBooking-UI-Flutter</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> GoogleAdMob-Flutter</a>
        </div>

        <!-- github stats (cards simulated) -->
        <h2 class="section-title"><i class="fa-regular fa-chart-bar"></i> GitHub stats</h2>
        <div class="stats-flex">
            <div class="stat-item"><i class="fa-regular fa-rectangle-ad"></i> 12 public repos</div>
            <div class="stat-item"><i class="fa-regular fa-star"></i> 130+ stars</div>
            <div class="stat-item"><i class="fa-regular fa-calendar"></i> 480+ contributions (last year)</div>
        </div>
        <div style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: center;">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=faisalarshadciit&layout=compact&theme=graywhite&hide_border=true" alt="languages" style="border-radius: 20px; border:1px solid #e0e8f0;">
            <img src="https://github-readme-streak-stats.herokuapp.com?user=faisalarshadciit&theme=default&hide_border=true" alt="streak" style="border-radius: 20px; border:1px solid #e0e8f0;">
        </div>

        <!-- certifications -->
        <h2 class="section-title"><i class="fa-regular fa-certificate"></i> certifications</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 0.7rem;">
            <div class="cert-badge"><i class="fa-regular fa-badge-check" style="color:#0a7e3a;"></i> Make.com Basics</div>
            <div class="cert-badge"><i class="fa-regular fa-badge-check" style="color:#0a7e3a;"></i> Make.com Foundation</div>
        </div>
        <p style="margin-top: 0.5rem;"><i class="fa-regular fa-circle-check" style="color:#0f7b3a;"></i> Certified in workflow automation, control flow, and data integration.</p>
        <hr>
        <div class="footer-note">
            “Let’s build something fast, beautiful, and reliable.” <i class="fa-regular fa-hand-peace"></i>
        </div>
    </div>
</div>
</body>
</html>
