<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ravi Singh | Senior Software Engineer</title>

    <!-- SEO -->
    <meta name="description" content="Ravi Singh - Senior Software Engineer specializing in Finacle E-Banking, Core Java, API Integration, FEBA customization, and Production Support." />
    <meta name="keywords" content="Ravi Singh, Senior Software Engineer, Java Developer, FEBA, Finacle, API Integration, Portfolio" />
    <meta name="author" content="Ravi Singh" />

    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet" />
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
    
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
            color: #1e293b;
            line-height: 1.6;
            transition: all 0.3s ease;
        }

        body.dark {
            background: linear-gradient(135deg, #0f172a 0%, #1a1f35 100%);
            color: #f1f5f9;
        }

        /* Navbar */
        nav {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.08);
            padding: 16px 20px;
            transition: all 0.3s ease;
        }

        body.dark nav {
            background: rgba(15, 23, 42, 0.85);
            border-bottom-color: rgba(255, 255, 255, 0.08);
        }

        .nav-container {
            max-width: 1200px;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
        }

        .logo {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            font-size: 1.25rem;
            background: linear-gradient(135deg, #3b82f6 0%, #06b6d4 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 32px;
            align-items: center;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: #475569;
            text-decoration: none;
            font-size: 0.95rem;
            font-weight: 500;
            transition: 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -6px;
            left: 0;
            background: linear-gradient(135deg, #3b82f6, #06b6d4);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        body.dark .nav-links a {
            color: #cbd5e1;
        }

        .theme-btn {
            border: none;
            background: linear-gradient(135deg, #3b82f6, #06b6d4);
            color: white;
            padding: 10px 18px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.9rem;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
            transition: all 0.3s ease;
        }

        .theme-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #3b82f6 0%, #1e40af 50%, #0c4a6e 100%);
            color: white;
            text-align: center;
            padding: 100px 20px;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            top: -100px;
            right: -100px;
            animation: float 6s ease-in-out infinite;
        }

        header::after {
            content: "";
            position: absolute;
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(255,255,255,0.08) 0%, transparent 70%);
            bottom: -50px;
            left: -50px;
            animation: float 8s ease-in-out infinite reverse;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(30px); }
        }

        .header-content {
            position: relative;
            z-index: 2;
        }

        .profile-pic {
            width: 150px;
            height: 150px;
            border-radius: 12px;
            object-fit: cover;
            border: 4px solid rgba(255,255,255,0.3);
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
            margin-bottom: 24px;
            transition: transform 0.3s ease;
            animation: slideDown 0.8s ease;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .profile-pic:hover {
            transform: scale(1.05);
        }

        header h1 {
            font-family: 'Poppins', sans-serif;
            font-size: 3.5rem;
            font-weight: 800;
            letter-spacing: -1px;
            margin-bottom: 8px;
            animation: slideDown 0.8s ease 0.1s both;
        }

        header p {
            font-size: 1.15rem;
            color: rgba(255,255,255,0.95);
            margin-bottom: 28px;
            font-weight: 400;
            letter-spacing: 0.3px;
            animation: slideDown 0.8s ease 0.2s both;
        }

        .header-buttons {
            display: flex;
            justify-content: center;
            gap: 16px;
            flex-wrap: wrap;
            animation: slideDown 0.8s ease 0.3s both;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 28px;
            background: white;
            color: #3b82f6;
            text-decoration: none;
            border-radius: 8px;
            font-weight: 600;
            font-size: 0.95rem;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
        }

        .btn-secondary {
            background: rgba(255,255,255,0.15);
            color: white;
            border: 1.5px solid rgba(255,255,255,0.3);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255,255,255,0.25);
            border-color: rgba(255,255,255,0.5);
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 70px 20px;
        }

        section {
            margin-bottom: 80px;
        }

        .section-heading {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 50px;
        }

        .section-title {
            font-family: 'Poppins', sans-serif;
            font-size: 2.2rem;
            font-weight: 700;
            color: #1e293b;
            letter-spacing: -0.5px;
        }

        body.dark .section-title {
            color: #f1f5f9;
        }

        .section-heading::before {
            content: '';
            display: block;
            width: 4px;
            height: 40px;
            background: linear-gradient(135deg, #3b82f6, #06b6d4);
            border-radius: 2px;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 24px;
        }

        .skill-card {
            background: white;
            padding: 28px;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            transition: all 0.3s ease;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
        }

        .skill-card:hover {
            transform: translateY(-6px);
            border-color: #3b82f6;
            box-shadow: 0 12px 25px rgba(59, 130, 246, 0.15);
        }

        body.dark .skill-card {
            background: #1e293b;
            border-color: #334155;
        }

        body.dark .skill-card:hover {
            border-color: #3b82f6;
        }

        .skill-card h3 {
            font-family: 'Poppins', sans-serif;
            font-size: 1.15rem;
            font-weight: 700;
            margin-bottom: 16px;
            color: #1e293b;
        }

        body.dark .skill-card h3 {
            color: #f1f5f9;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill-tag {
            display: inline-block;
            background: #f0f4f8;
            color: #3b82f6;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .skill-tag:hover {
            background: #3b82f6;
            color: white;
            transform: scale(1.05);
        }

        body.dark .skill-tag {
            background: #334155;
            color: #93c5fd;
        }

        body.dark .skill-tag:hover {
            background: #3b82f6;
            color: white;
        }

        /* Experience Timeline */
        .timeline {
            position: relative;
            padding: 20px 0;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 40px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(180deg, #3b82f6 0%, #06b6d4 100%);
        }

        .experience-item {
            margin-bottom: 40px;
            margin-left: 120px;
            position: relative;
            animation: slideInLeft 0.6s ease;
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .experience-item::before {
            content: '';
            position: absolute;
            width: 12px;
            height: 12px;
            background: #3b82f6;
            border: 3px solid white;
            border-radius: 50%;
            left: -130px;
            top: 8px;
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.1);
        }

        body.dark .experience-item::before {
            border-color: #1a1f35;
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.2);
        }

        .experience-item h3 {
            font-family: 'Poppins', sans-serif;
            font-size: 1.25rem;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 4px;
        }

        body.dark .experience-item h3 {
            color: #f1f5f9;
        }

        .experience-item .meta {
            color: #64748b;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 12px;
        }

        body.dark .experience-item .meta {
            color: #94a3b8;
        }

        .experience-item ul {
            list-style: none;
            padding: 0;
        }

        .experience-item li {
            color: #475569;
            margin-bottom: 8px;
            padding-left: 20px;
            position: relative;
            font-size: 0.95rem;
        }

        body.dark .experience-item li {
            color: #cbd5e1;
        }

        .experience-item li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: #3b82f6;
            font-weight: bold;
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 28px;
        }

        .project-card {
            background: white;
            padding: 32px;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            transition: all 0.3s ease;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #3b82f6, #06b6d4);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.3s ease;
        }

        .project-card:hover::before {
            transform: scaleX(1);
        }

        .project-card:hover {
            transform: translateY(-8px);
            border-color: #3b82f6;
            box-shadow: 0 12px 30px rgba(59, 130, 246, 0.2);
        }

        body.dark .project-card {
            background: #1e293b;
            border-color: #334155;
        }

        body.dark .project-card:hover {
            border-color: #3b82f6;
        }

        .project-card h3 {
            font-family: 'Poppins', sans-serif;
            font-size: 1.2rem;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 12px;
        }

        body.dark .project-card h3 {
            color: #f1f5f9;
        }

        .project-card p {
            color: #64748b;
            font-size: 0.95rem;
            line-height: 1.6;
            flex-grow: 1;
            margin-bottom: 0;
        }

        body.dark .project-card p {
            color: #cbd5e1;
        }

        /* Certifications */
        .two-col {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 28px;
        }

        .cert-box {
            background: white;
            padding: 28px;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            transition: all 0.3s ease;
        }

        .cert-box:hover {
            transform: translateY(-4px);
            border-color: #3b82f6;
            box-shadow: 0 8px 20px rgba(59, 130, 246, 0.15);
        }

        body.dark .cert-box {
            background: #1e293b;
            border-color: #334155;
        }

        body.dark .cert-box:hover {
            border-color: #3b82f6;
        }

        .cert-box h3 {
            font-family: 'Poppins', sans-serif;
            font-size: 1.15rem;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 18px;
        }

        body.dark .cert-box h3 {
            color: #f1f5f9;
        }

        .cert-box ul {
            list-style: none;
        }

        .cert-box li {
            color: #475569;
            padding: 8px 0;
            padding-left: 24px;
            position: relative;
            font-size: 0.95rem;
        }

        body.dark .cert-box li {
            color: #cbd5e1;
        }

        .cert-box li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #06b6d4;
            font-weight: bold;
            font-size: 1.1rem;
        }

        /* Achievements */
        .achievements-list {
            background: white;
            padding: 32px;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
        }

        body.dark .achievements-list {
            background: #1e293b;
            border-color: #334155;
        }

        .achievements-list ul {
            list-style: none;
        }

        .achievements-list li {
            color: #475569;
            padding: 14px 0;
            padding-left: 28px;
            position: relative;
            font-size: 0.95rem;
            border-bottom: 1px solid #e2e8f0;
        }

        body.dark .achievements-list li {
            color: #cbd5e1;
            border-bottom-color: #334155;
        }

        .achievements-list li:last-child {
            border-bottom: none;
        }

        .achievements-list li::before {
            content: '⭐';
            position: absolute;
            left: 0;
            font-size: 1rem;
        }

        /* Fun Zone */
        .fun-box {
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(6, 182, 212, 0.1) 100%);
            padding: 40px;
            border-radius: 12px;
            border: 1px solid rgba(59, 130, 246, 0.2);
            text-align: center;
        }

        body.dark .fun-box {
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.15) 0%, rgba(6, 182, 212, 0.15) 100%);
            border-color: rgba(59, 130, 246, 0.3);
        }

        .fun-input-group {
            display: flex;
            gap: 12px;
            margin-bottom: 24px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .fun-input-group input {
            padding: 12px 18px;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            font-size: 0.95rem;
            width: 250px;
            max-width: 100%;
            background: white;
            color: #1e293b;
            transition: all 0.3s ease;
        }

        body.dark .fun-input-group input {
            background: #334155;
            border-color: #475569;
            color: #f1f5f9;
        }

        .fun-input-group input:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }

        #surpriseText {
            font-size: 1.1rem;
            font-weight: 600;
            color: #3b82f6;
            min-height: 30px;
            animation: bounceIn 0.5s ease;
        }

        body.dark #surpriseText {
            color: #93c5fd;
        }

        @keyframes bounceIn {
            0% { opacity: 0; transform: scale(0.8); }
            100% { opacity: 1; transform: scale(1); }
        }

        /* Contact Form */
        .contact-form {
            background: white;
            padding: 40px;
            border-radius: 12px;
            border: 1px solid #e2e8f0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            max-width: 600px;
            margin: 0 auto;
        }

        body.dark .contact-form {
            background: #1e293b;
            border-color: #334155;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 14px 16px;
            margin-bottom: 16px;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            font-family: 'Inter', sans-serif;
            font-size: 0.95rem;
            color: #1e293b;
            background: white;
            transition: all 0.3s ease;
        }

        body.dark .contact-form input,
        body.dark .contact-form textarea {
            background: #334155;
            border-color: #475569;
            color: #f1f5f9;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }

        .contact-form button {
            width: 100%;
            padding: 14px;
            font-size: 1rem;
            font-weight: 600;
        }

        /* Contact Links */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 24px;
        }

        .contact-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #3b82f6;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            padding: 10px 16px;
            border-radius: 8px;
            border: 1px solid transparent;
        }

        body.dark .contact-link {
            color: #93c5fd;
        }

        .contact-link:hover {
            border-color: #3b82f6;
            background: rgba(59, 130, 246, 0.1);
            transform: translateY(-2px);
        }

        .contact-link i {
            font-size: 1.2rem;
        }

        /* Footer */
        footer {
            background: white;
            color: #64748b;
            text-align: center;
            padding: 30px 20px;
            border-top: 1px solid #e2e8f0;
            margin-top: 60px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        body.dark footer {
            background: #0f172a;
            border-top-color: #334155;
            color: #94a3b8;
        }

        /* Responsive */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2.2rem;
            }

            .section-title {
                font-size: 1.8rem;
            }

            .nav-links {
                gap: 16px;
            }

            .timeline::before {
                left: 25px;
            }

            .experience-item {
                margin-left: 80px;
            }

            .experience-item::before {
                left: -90px;
            }

            .skills-grid,
            .projects-grid,
            .two-col {
                grid-template-columns: 1fr;
            }

            .fun-input-group input {
                width: 100%;
            }

            .contact-form {
                padding: 28px;
            }
        }

        @media (max-width: 480px) {
            .header-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
                justify-content: center;
            }

            .nav-links {
                display: none;
            }

            header h1 {
                font-size: 1.8rem;
            }

            header {
                padding: 60px 20px;
            }

            .container {
                padding: 50px 16px;
            }

            .contact-links {
                gap: 12px;
            }

            .contact-link {
                padding: 8px 12px;
                font-size: 0.85rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">RS</div>
            <div class="nav-links">
                <a href="#skills">Skills</a>
                <a href="#experience">Experience</a>
                <a href="#projects">Projects</a>
                <a href="#certifications">Certifications</a>
                <a href="#contact">Contact</a>
            </div>
            <button class="theme-btn" onclick="toggleTheme()">
                <i class="fas fa-moon"></i> Theme
            </button>
        </div>
    </nav>

    <!-- Header -->
    <header>
        <div class="header-content">
            <img src="https://via.placeholder.com/150?text=RS" alt="Ravi Singh" class="profile-pic">
            <h1>Ravi Singh</h1>
            <p>Software Engineer | 3 Years Experience</p>
            <p>Finacle E-Banking (FEBA) | Core Java Developer | DEH Beginner</p>
            <div class="header-buttons">
                <a href="#projects" class="btn">
                    <i class="fas fa-code"></i> View Projects
                </a>
                <a href="#contact" class="btn btn-secondary">
                    <i class="fas fa-envelope"></i> Get In Touch
                </a>
				<a class="btn" href="Ravi_Singh.pdf" target="_blank">Download Resume</a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <div class="container">
        <!-- Skills Section -->
        <section id="skills">
            <div class="section-heading">
                <h2 class="section-title">Skills</h2>
            </div>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>Backend & Core</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Java</span>
                        <span class="skill-tag">Spring Boot</span>
                        <span class="skill-tag">REST API</span>
                        <span class="skill-tag">Microservices</span>
                    </div>
                </div>
                <div class="skill-card">
                    <h3>Banking & Fintech</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Finacle</span>
                        <span class="skill-tag">FEBA</span>
                        <span class="skill-tag">Core Banking</span>
                        <span class="skill-tag">Payment Systems</span>
                    </div>
                </div>
                <div class="skill-card">
                    <h3>Databases & Tools</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">SQL</span>
                        <span class="skill-tag">Oracle</span>
                        <span class="skill-tag">Git</span>
                        <span class="skill-tag">Kubernetes</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Experience Section -->
        <section id="experience">
            <div class="section-heading">
                <h2 class="section-title">Experience</h2>
            </div>
            <div class="timeline">
                <div class="experience-item">
                    <h3>Software Engineer</h3>
                    <p><strong>Modus Information Systems Pvt Ltd</strong> | Aug 2023 - Dec 2024</p>
                    <ul>
                        <li>Extensive experience in Canara Bank RRB project with FEBA Framework, Core Java, Servlets, and JSP.</li>
                        <li>Worked on L2 production support, customization, module development, UI enhancements, and live issue resolution.</li>
                        <li>Contributed to automation, batch scheduling, and internet banking production support.</li>
                        <li>Handled Oracle upgrades, new FEBA installations, and production environment support.</li>
                        <li>Worked on CKYC, AEPS, and Re-KYC modules in banking systems.</li>
                        <li>Worked on transaction batches, bulk salary transfer initiation, log analysis, server bounce, DAT file checks, and email issue troubleshooting.</li>
                        <li>Customized FEBA menus, FormGroups, FormManagement, VO, Service Requests in DAL (Data Access Layer), and TSPC.</li>
                    </ul>
                </div>

                <div class="experience-item">
                    <h3>Software Engineer</h3>
                    <p><strong>Infosys – Meethaq Oman Bank Project</strong> | Dec 2024 - Mar 2025</p>
                    <ul>
                        <li>Worked on FEBA customization and observation fixes to ensure smooth banking operations.</li>
                        <li>Developed UI enhancements to improve banking module performance and user experience.</li>
                        <li>Resolved system observations and production issues ensuring compliance and stability.</li>
                    </ul>
                </div>

                <div class="experience-item">
                    <h3>Software Engineer</h3>
                    <p><strong>Natsave Bank Project</strong> | Jul 2025 - Present</p>
                    <ul>
                        <li>Worked on NI Mastercard integration for end-to-end card lifecycle management.</li>
                        <li>Implemented card creation, activation, PIN setup, and client/account linking flows.</li>
                        <li>Integrated core banking system using FI calls to fetch customer and account data.</li>
                        <li>Validated core data before sending API requests to external systems.</li>
                        <li>Handled both personal and non-personal card creation workflows.</li>
                        <li>Managed API responses and ensured proper success/failure handling in the application.</li>
                        <li>Performed validations and resolved functional issues to ensure smooth card processing.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <div class="section-heading">
                <h2 class="section-title">Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>🏦 Natsave Bank – Mastercard Integration</h3>
                    <p>Integrated NI Mastercard services into the Finacle E-Banking platform. Worked on card lifecycle processes including card issuance, activation, PIN setup, card limits, and control handling.</p>
                </div>

                <div class="project-card">
                    <h3>🔐 CKYC Integration</h3>
                    <p>Implemented Central KYC integration to enable customer verification and onboarding through external government APIs, ensuring regulatory compliance.</p>
                </div>

                <div class="project-card">
                    <h3>💳 AEPS Services</h3>
                    <p>Developed and supported Aadhaar Enabled Payment System functionalities for banking customers including authentication and transaction validation.</p>
                </div>

                <div class="project-card">
                    <h3>📋 Re-KYC Module</h3>
                    <p>Enhanced customer compliance processes by implementing Re-KYC workflows, validations, and regulatory checks for financial institutions.</p>
                </div>
            </div>
        </section>

        <!-- Certifications Section -->
        <section id="certifications">
            <div class="section-heading">
                <h2 class="section-title">Certifications & Learning</h2>
            </div>
            <div class="two-col">
                <div class="cert-box">
                    <h3>Certifications</h3>
                    <ul>
                        <li>Java Programming Certification</li>
                        <li>Selenium Automation Training</li>
                        <li>SQL / Database Testing Training</li>
                        <li>Finacle / FEBA E-Banking Domain Learning</li>
						<li>Claude AI & API Certification</li>
                    </ul>
                </div>

                <div class="cert-box">
                    <h3>Currently Learning</h3>
                    <ul>
                        <li>Spring Boot</li>
                        <li>Microservices</li>
                  
                        <li>Advanced API Integration</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Achievements Section -->
        <section id="achievements">
            <div class="section-heading">
                <h2 class="section-title">Achievements</h2>
            </div>
            <div class="achievements-list">
                <ul>
                    <li>Successfully worked on multiple FEBA customizations and banking integrations</li>
                    <li>Contributed to CKYC, Re-KYC, AEPS, and Mastercard-related banking modules</li>
                    <li>Provided L2 Production Support for critical banking applications and incident resolution</li>
                    <li>Improved issue debugging and root-cause analysis for banking production environments</li>
                    <li>Supported deployment activities, batch monitoring, and application stability</li>
                    <li>Worked directly on customer/account validations and API success-failure handling workflows</li>
                </ul>
            </div>
        </section>

        <!-- Fun Zone -->
        <section id="fun">
            <div class="section-heading">
                <h2 class="section-title">Quick Fun Zone</h2>
            </div>
            <div class="fun-box">
                <div class="fun-input-group">
                    <input type="text" id="userInput" placeholder="Type something (e.g. happy, sad, coffee)">
                    <button class="btn" onclick="showCustomSurprise()">
                        <i class="fas fa-gift"></i> Get Surprise
                    </button>
                </div>
                <p id="surpriseText"></p>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <div class="section-heading">
                <h2 class="section-title">Contact</h2>
            </div>
            <form class="contact-form">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <input type="tel" name="phone" placeholder="Phone Number">
                <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
                <button type="submit" class="btn">
                    <i class="fas fa-paper-plane"></i> Send Message
                </button>
                <input type="hidden" name="_captcha" value="false">
            </form>

            <div class="contact-links">
                <a href="mailto:Ravi.singh2@ust.com" class="contact-link">
                    <i class="fas fa-envelope"></i> Email
                </a>
                <a href="https://github.com/ravisinghpatna" target="_blank" class="contact-link">
                    <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://www.linkedin.com/in/ravisinghpatna" target="_blank" class="contact-link">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer>
        <p>© 2026 Ravi Singh | Software Engineer </p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
    <script>
        // Dark mode toggle
        function toggleTheme() {
            document.body.classList.toggle("dark");
            localStorage.setItem("theme", document.body.classList.contains("dark") ? "dark" : "light");
        }

        // Load saved theme
        window.addEventListener("DOMContentLoaded", function() {
            const savedTheme = localStorage.getItem("theme") || "light";
            if (savedTheme === "dark") {
                document.body.classList.add("dark");
            }
        });

        // Surprise box
        function showCustomSurprise() {
            const input = document.getElementById("userInput").value.toLowerCase().trim();
            let message = "";

            if (input.includes("happy")) {
                message = "😄 Keep smiling, you're doing great!";
            } else if (input.includes("sad")) {
                message = "🌈 It's okay, tough times don't last!";
            } else if (input.includes("coffee")) {
                message = "☕ Coffee + Code = Perfect Combo!";
            } else if (input.includes("ravi")) {
                message = "😎 I know you are the boss, Ravi!";
            } else if (input.includes("singh")) {
                message = "👋 Hello Boss!";
            } else if (input.includes("code") || input.includes("developer")) {
                message = "💻 Keep building awesome things!";
            } else if (input === "") {
                message = "⚠️ Type something first!";
            } else {
                message = "✨ Interesting input! Keep exploring!";
            }

            document.getElementById("surpriseText").innerText = message;
        }

        // Email JS integration
        emailjs.init({
            publicKey: "4NfwDy_Fbk3EZ5pjq"
        });

        document.querySelector(".contact-form").addEventListener("submit", function(e) {
            e.preventDefault();

            emailjs.send("service_yejy39b", "template_3z41zd7", {
                name: this.name.value,
                email: this.email.value,
                phone: this.phone.value,
                message: this.message.value
            })
            .then((response) => {
                console.log("SUCCESS:", response);
                alert("Message sent successfully! 🎉");
                this.reset();
            })
            .catch((error) => {
                console.error("FAILED:", error);
                alert("Failed to send message. Please try again.");
            });
        });
    </script>
</body>
</html>
