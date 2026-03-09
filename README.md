<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yasas Nirmitha Wanigaarachchi | Portfolio</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Outfit:wght@300;400;600;700;800&display=swap"
        rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --bg-dark: #07090e;
            --glass-bg: rgba(25, 30, 45, 0.4);
            --glass-border: rgba(255, 255, 255, 0.08);
            --glass-hover: rgba(255, 255, 255, 0.12);
            --accent-blue: #004e92;
            --accent-cyan: #00c6ff;
            --accent-purple: #8e2de2;
            --text-primary: #ffffff;
            --text-secondary: #94a3b8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Outfit', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* Ambient Background */
        .ambient-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            z-index: -1;
            overflow: hidden;
            background: radial-gradient(circle at 15% 50%, rgba(0, 78, 146, 0.15), transparent 25%),
                radial-gradient(circle at 85% 30%, rgba(142, 45, 226, 0.12), transparent 25%);
        }

        .blob {
            position: absolute;
            filter: blur(80px);
            z-index: -1;
            opacity: 0.6;
            animation: float 10s infinite alternate ease-in-out;
            border-radius: 50%;
        }

        .blob-1 {
            top: -10%;
            left: -10%;
            width: 50vw;
            height: 50vw;
            background: rgba(0, 198, 255, 0.08);
        }

        .blob-2 {
            bottom: -10%;
            right: -10%;
            width: 40vw;
            height: 40vw;
            background: rgba(142, 45, 226, 0.08);
            animation-delay: -5s;
        }

        @keyframes float {
            0% {
                transform: translate(0, 0) scale(1);
            }

            100% {
                transform: translate(30px, 60px) scale(1.05);
            }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* Glassmorphism */
        .glass {
            background: var(--glass-bg);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
        }

        /* Navigation */
        nav {
            padding: 20px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 100;
            background: rgba(7, 9, 14, 0.7);
            backdrop-filter: blur(15px);
            border-bottom: 1px solid var(--glass-border);
            transition: all 0.3s ease;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: 0.5px;
            background: linear-gradient(90deg, #fff, var(--accent-cyan));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-links {
            display: flex;
            gap: 32px;
            align-items: center;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--text-primary);
        }

        /* Hero */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 120px 0 60px;
        }

        .profile-views {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 6px 16px;
            border-radius: 50px;
            font-size: 0.9rem;
            margin-bottom: 24px;
            animation: fadeInDown 1s ease;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 6vw, 5rem);
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 16px;
            background: linear-gradient(to right, #ffffff, #aaaaaa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .hero h2 {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: var(--text-secondary);
            font-weight: 400;
            margin-bottom: 30px;
            max-width: 800px;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .hero h2 span {
            color: var(--accent-cyan);
            font-weight: 600;
        }

        .typing-container {
            margin: 10px 0 40px;
            height: 40px;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .typing-container img {
            max-width: 100%;
            height: auto;
        }

        .social-row {
            display: flex;
            gap: 16px;
            margin-bottom: 40px;
            animation: fadeInUp 1s ease 0.8s both;
            flex-wrap: wrap;
            justify-content: center;
        }

        .social-btn {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 24px;
            border-radius: 12px;
            text-decoration: none;
            color: var(--text-primary);
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            background: var(--glass-bg);
            border: 1px solid var(--glass-border);
        }

        .social-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.2);
        }

        .social-btn.github:hover {
            background: #181717;
        }

        .social-btn.linkedin:hover {
            background: #0077b5;
        }

        .social-btn.email:hover {
            background: #ea4335;
        }

        .tag-container {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
            max-width: 800px;
            animation: fadeInUp 1s ease 1s both;
        }

        .badge {
            padding: 8px 18px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }

        .badge-blue {
            background: rgba(0, 196, 255, 0.1);
            color: #00c4ff;
            border: 1px solid rgba(0, 196, 255, 0.2);
        }

        .badge-orange {
            background: rgba(255, 140, 0, 0.1);
            color: #ff8c00;
            border: 1px solid rgba(255, 140, 0, 0.2);
        }

        .badge-red {
            background: rgba(227, 79, 38, 0.1);
            color: #e34f26;
            border: 1px solid rgba(227, 79, 38, 0.2);
        }

        .badge-dark {
            background: rgba(255, 255, 255, 0.05);
            color: #fff;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .badge-green {
            background: rgba(102, 255, 153, 0.1);
            color: #66ff99;
            border: 1px solid rgba(102, 255, 153, 0.2);
        }

        /* Sections */
        section {
            padding: 90px 0;
            position: relative;
        }

        .section-header {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 50px;
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .section-header i {
            color: var(--accent-cyan);
        }

        .section-header::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-cyan), transparent);
            border-radius: 2px;
            margin-top: 10px;
        }

        /* About Section */
        .about-grid {
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-content {
            padding: 40px;
        }

        .about-content p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 24px;
        }

        .about-list {
            list-style: none;
        }

        .about-list li {
            margin-bottom: 20px;
            display: flex;
            align-items: flex-start;
            gap: 15px;
            font-size: 1.05rem;
        }

        .about-list i {
            color: var(--accent-cyan);
            font-size: 1.2rem;
            margin-top: 4px;
        }

        .about-image {
            display: flex;
            justify-content: center;
            position: relative;
        }

        .about-image img {
            width: 100%;
            max-width: 400px;
            border-radius: 30px;
            object-fit: cover;
            z-index: 2;
            position: relative;
        }

        .image-backdrop {
            position: absolute;
            width: 100%;
            max-width: 400px;
            height: 100%;
            background: linear-gradient(45deg, var(--accent-blue), var(--accent-purple));
            border-radius: 30px;
            top: 20px;
            left: 20px;
            z-index: 1;
            opacity: 0.5;
            filter: blur(10px);
        }

        /* Tech Stack */
        .tech-container {
            padding: 50px 30px;
            text-align: center;
        }

        .tech-icons {
            margin-top: 40px;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }

        .tech-icons img {
            max-width: 100%;
            height: auto;
            filter: drop-shadow(0 10px 15px rgba(0, 0, 0, 0.3));
            transition: transform 0.3s;
        }

        .tech-icons img:hover {
            transform: scale(1.02);
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .project-card {
            padding: 35px;
            transition: transform 0.4s ease, border-color 0.4s ease;
            display: flex;
            flex-direction: column;
            height: 100%;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-cyan), var(--accent-purple));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: rgba(255, 255, 255, 0.2);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-icon {
            width: 60px;
            height: 60px;
            background: rgba(0, 198, 255, 0.1);
            border-radius: 16px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.8rem;
            color: var(--accent-cyan);
            margin-bottom: 25px;
        }

        .project-card h3 {
            font-size: 1.5rem;
            margin-bottom: 12px;
        }

        .project-card p {
            color: var(--text-secondary);
            flex-grow: 1;
            margin-bottom: 25px;
        }

        .tech-tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
        }

        .tech-tags span {
            padding: 6px 14px;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            font-size: 0.8rem;
            font-family: 'Inter', sans-serif;
            color: #cbd5e1;
        }

        /* Stats Section */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-bottom: 30px;
        }

        .stats-card {
            padding: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .stats-card img {
            max-width: 100%;
            border-radius: 12px;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s ease;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        footer {
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid var(--glass-border);
            margin-top: 50px;
            color: var(--text-secondary);
            background: rgba(0, 0, 0, 0.2);
        }

        @media (max-width: 992px) {
            .about-grid {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .about-list li {
                justify-content: center;
                text-align: left;
                display: inline-flex;
                width: 100%;
                max-width: 400px;
            }

            .about-list {
                display: flex;
                flex-direction: column;
                align-items: center;
            }

            .section-header {
                justify-content: center;
            }

            .section-header::after {
                margin: 10px auto 0;
            }

            .stats-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero {
                padding-top: 150px;
            }

            .tag-container {
                gap: 8px;
            }

            .badge {
                padding: 6px 12px;
                font-size: 0.75rem;
            }
        }
    </style>
</head>

<body>
    <!-- Ambient Background -->
    <div class="ambient-bg">
        <div class="blob blob-1"></div>
        <div class="blob blob-2"></div>
    </div>

    <!-- Navigation -->
    <nav>
        <div class="container" style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
            <a href="#" class="logo">
                <i class="fa-solid fa-code"></i> YWANIGA
            </a>
            <div class="nav-links">
                <a href="#about">About</a>
                <a href="#tech">Tech Stack</a>
                <a href="#projects">Projects</a>
                <a href="#github">GitHub</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container" style="display: flex; flex-direction: column; align-items: center;">
            <div class="profile-views glass">
                <i class="fa-solid fa-eye" style="color: var(--accent-cyan);"></i> Profile Views:
                <img src="https://komarev.com/ghpvc/?username=ywanigaarachchi&label=%20&color=00c6ff&style=flat"
                    alt="ywanigaarachchi" />
            </div>

            <h1>Yasas Nirmitha <br />Wanigaarachchi</h1>

            <h2>Building Scalable <span>Microservices</span> & <span>Cloud Solutions</span></h2>

            <div class="typing-container">
                <a href="https://git.io/typing-svg">
                    <img src="https://readme-typing-svg.herokuapp.com?font=Outfit&weight=600&pause=1000&color=00C6FF&center=true&vCenter=true&width=500&lines=Passionate+about+Distributed+Systems;Building+Auto+Hub+Logistics+Platform;Mastering+Cloud+Native+Technologies"
                        alt="Typing SVG" />
                </a>
            </div>

            <div class="social-row">
                <a href="https://github.com/YWanigaarachchi" class="social-btn github">
                    <i class="fa-brands fa-github"></i> GitHub
                </a>
                <a href="https://linkedin.com/in/your-linkedin-handle" class="social-btn linkedin">
                    <i class="fa-brands fa-linkedin"></i> LinkedIn
                </a>
                <a href="mailto:ynwanigaarachchi@gmail.com" class="social-btn email">
                    <i class="fa-solid fa-envelope"></i> Email
                </a>
            </div>

            <div class="tag-container">
                <span class="badge badge-blue">Full-Stack Developer</span>
                <span class="badge badge-orange">Cloud Native</span>
                <span class="badge badge-red">DevOps</span>
                <span class="badge badge-dark">Open Source Contributor</span>
                <span class="badge badge-green">System Design</span>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-header reveal">
                <i class="fa-solid fa-user-astronaut"></i> About Me
            </h2>
            <div class="about-grid">
                <div class="about-content glass reveal">
                    <p>I am a Software Engineering Student at ICBT and an Open Source Contributor. I specialize in
                        building robust backend systems, intuitive frontends, and dynamic cloud architectures.</p>

                    <ul class="about-list">
                        <li>
                            <i class="fa-solid fa-microchip"></i>
                            <div>Passionate about <strong>modern software engineering & cloud-native systems</strong>
                            </div>
                        </li>
                        <li>
                            <i class="fa-solid fa-layer-group"></i>
                            <div>Skilled in <strong>Full-Stack Web Development | Microservices | System Design</strong>
                            </div>
                        </li>
                        <li>
                            <i class="fa-solid fa-cloud"></i>
                            <div>Currently mastering <strong>Kubernetes, AWS, and Advanced Cloud Solutions</strong>
                            </div>
                        </li>
                        <li>
                            <i class="fa-solid fa-pen-nib"></i>
                            <div>Writing blogs at <a href="https://dev.to/"
                                    style="color: var(--accent-cyan); text-decoration: none;">dev.to</a></div>
                        </li>
                        <li>
                            <i class="fa-solid fa-bullseye"></i>
                            <div><strong>2025 Goals:</strong> AWS Certified • Open Source Contributor • Tech Conference
                                Speaker</div>
                        </li>
                    </ul>
                </div>
                <div class="about-image reveal">
                    <div class="image-backdrop"></div>
                    <!-- Using giphy as specified in their current layout, framed beautifully -->
                    <img src="https://media.giphy.com/media/TEnXkcsHrP4YedChhA/giphy.gif" alt="Coding GIF">
                </div>
            </div>
        </div>
    </section>

    <!-- Tech Stack Section -->
    <section id="tech">
        <div class="container">
            <h2 class="section-header reveal">
                <i class="fa-solid fa-laptop-code"></i> Tech Stack
            </h2>
            <div class="tech-container glass reveal">
                <p style="color: var(--text-secondary); font-size: 1.1rem; margin-bottom: 20px;">Technologies,
                    frameworks, and tools I work with to bring ideas to life.</p>
                <div class="tech-icons">
                    <img src="https://skillicons.dev/icons?i=react,nextjs,python,flask,java,php,nodejs,express,html,css,js,ts,kotlin,dart,mysql,mongodb,sqlite,firebase,aws,docker,linux,git,github,figma,canva&perline=10"
                        alt="Tech Stack" />
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-header reveal">
                <i class="fa-solid fa-rocket"></i> Project Highlights
            </h2>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card glass reveal">
                    <div class="project-icon">
                        <i class="fa-solid fa-truck-fast"></i>
                    </div>
                    <h3>Distributed Hub</h3>
                    <p>Microservices logistics system with Shop Nodes (5001-5003), API Hub & Live Analytics Dashboard.
                    </p>
                    <div class="tech-tags">
                        <span>Python</span>
                        <span>Flask</span>
                        <span>Gradio</span>
                        <span>Microservices</span>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card glass reveal" style="transition-delay: 0.1s;">
                    <div class="project-icon">
                        <i class="fa-solid fa-ring"></i>
                    </div>
                    <h3>Waram.lk</h3>
                    <p>Matrimony platform connecting the Tamil community with secure profiles and seamless matchmaking
                        capabilities.</p>
                    <div class="tech-tags">
                        <span>React</span>
                        <span>PHP</span>
                        <span>MySQL</span>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card glass reveal" style="transition-delay: 0.2s;">
                    <div class="project-icon">
                        <i class="fa-solid fa-leaf"></i>
                    </div>
                    <h3>GreenLife</h3>
                    <p>Wellness Center Management System for streamlined scheduling and comprehensive patient records.
                    </p>
                    <div class="tech-tags">
                        <span>HTML5</span>
                        <span>JavaScript</span>
                        <span>CSS3</span>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="project-card glass reveal" style="transition-delay: 0.3s;">
                    <div class="project-icon">
                        <i class="fa-solid fa-briefcase-medical"></i>
                    </div>
                    <h3>TechCare</h3>
                    <p>Native Android Medical Application crafted meticulously for reliable and efficient patient
                        tracking.</p>
                    <div class="tech-tags">
                        <span>Java</span>
                        <span>Android SDK</span>
                        <span>Mobile</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- GitHub Metrics Section -->
    <section id="github">
        <div class="container">
            <h2 class="section-header reveal">
                <i class="fa-brands fa-github-alt"></i> GitHub Analytics
            </h2>

            <div class="stats-grid">
                <div class="stats-card glass reveal">
                    <img src="https://github-readme-stats.vercel.app/api?username=YWanigaarachchi&theme=tokyonight&show_icons=true&hide_border=true&bg_color=0f172a00"
                        alt="GitHub Stats" />
                </div>
                <div class="stats-card glass reveal" style="transition-delay: 0.1s;">
                    <img src="https://streak-stats.demolab.com?user=YWanigaarachchi&theme=tokyonight&hide_border=true&background=0f172a00"
                        alt="GitHub Streak" />
                </div>
            </div>

            <div class="stats-card glass reveal" style="margin-bottom: 24px;">
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=YWanigaarachchi&theme=react-dark&hide_border=true&area=true&bg_color=0f172a00"
                    alt="Contribution Graph" style="width: 100%;" />
            </div>

            <div class="stats-grid" style="margin-bottom: 24px;">
                <div class="stats-card glass reveal">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YWanigaarachchi&layout=compact&theme=tokyonight&hide_border=true&bg_color=0f172a00"
                        alt="Top Languages" />
                </div>
                <div class="stats-card glass reveal" style="transition-delay: 0.1s;">
                    <img src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=YWanigaarachchi&theme=tokyonight&utcOffset=+5.5"
                        alt="Productive Time" />
                </div>
            </div>

            <div class="stats-card glass reveal">
                <img src="https://github-profile-trophy.vercel.app/?username=YWanigaarachchi&theme=radical&no-frame=true&margin-w=15&margin-h=15"
                    alt="Trophies" />
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>Designed with <i class="fa-solid fa-heart" style="color: #e23636;"></i> by Yasas Nirmitha Wanigaarachchi
            </p>
            <p style="margin-top: 10px; font-size: 0.9rem; color: #64748b;">Building the future of Cloud &
                Interconnected Systems.</p>
        </div>
    </footer>

    <script>
        // Scroll Reveal Animation
        function reveal() {
            var reveals = document.querySelectorAll(".reveal");
            for (var i = 0; i < reveals.length; i++) {
                var windowHeight = window.innerHeight;
                var elementTop = reveals[i].getBoundingClientRect().top;
                var elementVisible = 100;

                if (elementTop < windowHeight - elementVisible) {
                    reveals[i].classList.add("active");
                }
            }
        }
        window.addEventListener("scroll", reveal);
        // Trigger once on load
        reveal();

        // Navbar scroll effect
        window.addEventListener("scroll", function () {
            var nav = document.querySelector("nav");
            if (window.scrollY > 50) {
                nav.style.padding = "15px 0";
                nav.style.background = "rgba(7, 9, 14, 0.9)";
                nav.style.boxShadow = "0 4px 30px rgba(0,0,0,0.5)";
            } else {
                nav.style.padding = "20px 0";
                nav.style.background = "rgba(7, 9, 14, 0.7)";
                nav.style.boxShadow = "none";
            }
        });
    </script>
</body>

</html>
