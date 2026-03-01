<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Faisal Arshad · mobile studio</title>
    <!-- Font & icons -->
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
        .hero {
            background: linear-gradient(125deg, #0a4b7a 0%, #1e7e5c 60%, #5b3b8c 100%);
            border-radius: 2rem;
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
        /* project cards */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.8rem;
            margin: 2rem 0;
        }
        .project-card {
            background: #ffffff;
            border: 1px solid #e9eef3;
            border-radius: 28px;
            padding: 1.5rem 1.2rem;
            box-shadow: 0 10px 18px -8px rgba(0,0,0,0.05);
            transition: all 0.2s;
            display: flex;
            flex-direction: column;
        }
        .project-card:hover {
            border-color: #b1c3d8;
            box-shadow: 0 24px 30px -14px rgba(0,115,230,0.12);
            transform: translateY(-4px);
        }
        .project-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 0.8rem;
        }
        .project-name {
            font-size: 1.4rem;
            font-weight: 700;
            line-height: 1.3;
        }
        .project-date {
            background: #eaf1fb;
            border-radius: 30px;
            padding: 0.2rem 0.9rem;
            font-size: 0.75rem;
            font-weight: 600;
            color: #0b4a7c;
            white-space: nowrap;
        }
        .company {
            font-weight: 500;
            color: #2c3e50;
            margin: 0.2rem 0 0.8rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .company i {
            color: #4f6f8f;
        }
        .description {
            color: #2d3c4c;
            font-size: 0.95rem;
            margin: 0.8rem 0 1rem;
            flex: 1;
        }
        .skill-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.4rem 0.6rem;
            margin: 0.8rem 0 1rem;
        }
        .skill-tag {
            background: #e4eaf2;
            padding: 0.2rem 1rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
        }
        .preview-link {
            color: #0f5fa3;
            font-weight: 600;
            font-size: 0.9rem;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            margin-top: 0.5rem;
        }
        .preview-link i {
            font-size: 1rem;
        }
        hr {
            border: none;
            border-top: 2px dashed #d9e2ef;
            margin: 2rem 0;
        }
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
        }
        .repo-card i {
            color: #24292e;
        }
        .repo-card:hover {
            background: #e6edf5;
        }
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
        .footer-note {
            text-align: center;
            font-size: 1.2rem;
            font-weight: 400;
            background: #f0f7ff;
            padding: 1.5rem;
            border-radius: 60px;
            margin-top: 2rem;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="inner">
        <!-- Hero banner unchanged (personal info) -->
        <div class="hero">
            <div class="hero-content">
                <h1>Faisal Arshad</h1>
                <div class="sub">
                    <span>📱 Mobile App Engineer · 5+ Years</span>
                    <span>⚡ 10+ Published Apps</span>
                </div>
                <div class="typing-tag">
                    <i class="fa-regular fa-keyboard"></i> React Native · Flutter · FlutterFlow · AI/ML Kit · Make.com
                </div>
                <div class="contact-row">
                    <a href="mailto:faisalarshadciit@gmail.com" class="badge-btn"><i class="fa-regular fa-envelope"></i> Email</a>
                    <a href="https://wa.me/+923088649850" class="badge-btn"><i class="fa-brands fa-whatsapp"></i> WhatsApp</a>
                    <a href="https://www.linkedin.com/in/faisal-arshad-bb5ab1153" class="badge-btn"><i class="fa-brands fa-linkedin-in"></i> LinkedIn</a>
                    <a href="https://twitter.com/faisalarshad850" class="badge-btn"><i class="fa-brands fa-x-twitter"></i> X</a>
                </div>
                <div class="contact-row">
                    <a href="https://www.upwork.com/freelancers/~0143722ece1833a4ed" class="badge-btn"><i class="fa-brands fa-upwork"></i> Upwork</a>
                    <a href="https://www.fiverr.com/faisalarshad850" class="badge-btn"><i class="fa-brands fa-fiverr"></i> Fiverr</a>
                </div>
                <div class="profile-badges">
                    <span><i class="fa-regular fa-star"></i> 130+ GitHub stars</span>
                    <span><i class="fa-regular fa-user"></i> 20+ followers</span>
                    <span><i class="fa-regular fa-eye"></i> 4.2k profile views</span>
                </div>
                <div style="margin-top: 1.8rem;">
                    <span class="cta-box"><i class="fa-regular fa-hand-point-right"></i> Open for freelance & full‑time opportunities 🚀</span>
                </div>
            </div>
        </div>

        <!-- short about -->
        <div style="margin: 1.8rem 0 0.5rem;">
            <h2 class="section-title"><i class="fa-regular fa-user"></i> about</h2>
            <p style="font-size: 1.1rem; color: #1e293b;">👨‍💻 Mobile developer with <strong>5+ years</strong> building cross‑platform & native apps (React Native, Flutter, Android, iOS). Skilled in <strong>AI/ML Kit, SMS parsing, revenue models</strong>, and fast prototyping. Certified Make.com automation specialist. Currently focused on React Native and intelligent mobile solutions.</p>
        </div>

        <!-- tech stack (quick) -->
        <h2 class="section-title"><i class="fa-solid fa-code"></i> core stack</h2>
        <div class="badge-cloud">
            <span class="tech-badge"><i class="fa-brands fa-react"></i> React Native</span>
            <span class="tech-badge"><i class="fa-brands fa-flutter"></i> Flutter</span>
            <span class="tech-badge"><i class="fa-solid fa-database"></i> SQLite</span>
            <span class="tech-badge"><i class="fa-solid fa-fire"></i> Firebase</span>
            <span class="tech-badge"><i class="fa-solid fa-brain"></i> ML Kit</span>
            <span class="tech-badge"><i class="fa-regular fa-image"></i> OCR</span>
            <span class="tech-badge"><i class="fa-brands fa-google"></i> Gemini AI</span>
            <span class="tech-badge"><i class="fa-solid fa-chart-simple"></i> ContextApi</span>
            <span class="tech-badge"><i class="fa-solid fa-chart-line"></i> Chart</span>
            <span class="tech-badge"><i class="fa-regular fa-message"></i> SMS</span>
            <span class="tech-badge"><i class="fa-solid fa-crop"></i> Document scanner</span>
        </div>

        <!-- PROJECTS SECTION (replacing old apps) -->
        <h2 class="section-title"><i class="fa-regular fa-folder-open"></i> featured projects</h2>
        <div class="project-grid">

            <!-- Finance Manager (SMS Parsing) -->
            <div class="project-card">
                <div class="project-header">
                    <span class="project-name">Finance Manager (SMS Parsing)</span>
                    <span class="project-date">Apr 2025 - Jun 2025</span>
                </div>
                <div class="company">
                    <i class="fa-regular fa-building"></i> Atrule Technologies
                </div>
                <div class="description">
                    React Native app that automatically tracks finances by reading SMS. Extracts transaction details using built-in/custom regex, lets you approve & categorize, displays income/expenses per account. Visualize spending with charts, manage multiple accounts.
                </div>
                <div class="skill-list">
                    <span class="skill-tag">React Native</span>
                    <span class="skill-tag">SQLite</span>
                    <span class="skill-tag">ContextApi</span>
                    <span class="skill-tag">Chart</span>
                    <span class="skill-tag">Regex</span>
                </div>
                <a href="#" class="preview-link"><i class="fa-regular fa-eye"></i> App Preview</a>
            </div>

            <!-- Smart Scan App -->
            <div class="project-card">
                <div class="project-header">
                    <span class="project-name">Smart Scan App</span>
                    <span class="project-date">Feb 2025 - Apr 2025</span>
                </div>
                <div class="company">
                    <i class="fa-regular fa-building"></i> Atrule Technologies
                </div>
                <div class="description">
                    Multifunctional React Native app: barcode/QR scanning (ML Kit + Barcode Mask), OCR text extraction, document scanning, image crop, HTML→PDF, rich text editor (Tentap), and SMS chat interface. All-in-one scanning & communication tool.
                </div>
                <div class="skill-list">
                    <span class="skill-tag">React Native</span>
                    <span class="skill-tag">SQLite</span>
                    <span class="skill-tag">ML Kit</span>
                    <span class="skill-tag">OCR</span>
                    <span class="skill-tag">Hooks</span>
                </div>
                <a href="#" class="preview-link"><i class="fa-regular fa-eye"></i> App Preview</a>
            </div>

            <!-- AI Travel Planner UI -->
            <div class="project-card">
                <div class="project-header">
                    <span class="project-name">AI Travel Planner UI</span>
                    <span class="project-date">Jan 2025</span>
                </div>
                <!-- no company mention, keep minimal -->
                <div class="description">
                    Clean, modern travel planner interface built with React Native. Focus on smooth styles and component architecture. (UI concept)
                </div>
                <div class="skill-list">
                    <span class="skill-tag">React Native</span>
                    <span class="skill-tag">Styles</span>
                </div>
                <a href="#" class="preview-link"><i class="fa-regular fa-image"></i> Main Screens</a>
            </div>

            <!-- Fruit Identification (Gemini AI) + Weather Forecast -->
            <div class="project-card">
                <div class="project-header">
                    <span class="project-name">Fruit ID (Gemini AI) & Weather</span>
                    <span class="project-date">Nov 2024 - Dec 2024</span>
                </div>
                <div class="company">
                    <i class="fa-regular fa-building"></i> National College Of Business Administration & Economics
                </div>
                <div class="description">
                    Uses Gemini AI for real‑time fruit identification via images, plus WeatherAPI for forecasts. Firebase Auth & Firestore store user fruit data. React Native, Gemini, WeatherApi.
                </div>
                <div class="skill-list">
                    <span class="skill-tag">React Native</span>
                    <span class="skill-tag">Google Gemini</span>
                    <span class="skill-tag">WeatherApi</span>
                    <span class="skill-tag">Firebase</span>
                </div>
                <a href="#" class="preview-link"><i class="fa-regular fa-eye"></i> App Preview</a>
            </div>
        </div>

        <!-- additional note: all projects listed above replace previous apps -->
        <p style="margin-top: -0.5rem; color:#336699"><i class="fa-regular fa-circle-check"></i> Full project details available on request — each with published code/demo.</p>

        <!-- Featured repositories (light) -->
        <h2 class="section-title"><i class="fa-regular fa-folder-open"></i> open source</h2>
        <div class="repo-row">
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> QRCode-Generator-Android</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> Flutter-FoodDelivery-UI</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> WeatherApp-Flutter</a>
            <a href="#" class="repo-card"><i class="fa-brands fa-github"></i> LinkedIn-Post-Fetcher</a>
        </div>

        <!-- github stats summary -->
        <h2 class="section-title"><i class="fa-regular fa-chart-bar"></i> GitHub activity</h2>
        <div class="stats-flex">
            <div class="stat-item"><i class="fa-regular fa-rectangle-ad"></i> 12 public repos</div>
            <div class="stat-item"><i class="fa-regular fa-star"></i> 130+ stars</div>
            <div class="stat-item"><i class="fa-regular fa-calendar"></i> 480+ contributions</div>
        </div>
        <div style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: center; margin: 1.5rem 0;">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=faisalarshadciit&layout=compact&theme=graywhite&hide_border=true" alt="languages" style="border-radius: 20px; border:1px solid #e0e8f0;">
            <img src="https://github-readme-streak-stats.herokuapp.com?user=faisalarshadciit&theme=default&hide_border=true" alt="streak" style="border-radius: 20px; border:1px solid #e0e8f0;">
        </div>

        <!-- certifications -->
        <h2 class="section-title"><i class="fa-regular fa-certificate"></i> certifications</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 0.7rem;">
            <div class="cert-badge"><i class="fa-regular fa-badge-check" style="color:#0a7e3a;"></i> Make.com Basics</div>
            <div class="cert-badge"><i class="fa-regular fa-badge-check" style="color:#0a7e3a;"></i> Make.com Foundation</div>
        </div>
        <hr>
        <div class="footer-note">
            “Let’s build something fast, beautiful, and intelligent.” <i class="fa-regular fa-hand-peace"></i>
        </div>
    </div>
</div>
</body>
</html>
