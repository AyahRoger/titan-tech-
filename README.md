<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titan Tech - L'intelligence du futur</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&family=Exo:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* Reset et variables CSS */
        :root {
            --primary-color: #00f0ff;
            --secondary-color: #0066ff;
            --dark-bg: #0a0a1a;
            --darker-bg: #050510;
            --text-color: #e0e0ff;
            --text-muted: #a0a0c0;
            --neon-glow: 0 0 10px rgba(0, 240, 255, 0.7);
            --section-padding: 5rem 0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Exo', sans-serif;
            background-color: var(--dark-bg);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(0, 102, 255, 0.1) 0%, transparent 20%),
                radial-gradient(circle at 80% 70%, rgba(0, 240, 255, 0.1) 0%, transparent 20%),
                linear-gradient(to bottom, var(--darker-bg), var(--dark-bg));
            background-attachment: fixed;
        }

        h1, h2, h3, h4 {
            font-family: 'Orbitron', sans-serif;
            font-weight: 700;
            letter-spacing: 1px;
            margin-bottom: 1.5rem;
        }

        p {
            margin-bottom: 1.5rem;
            color: var(--text-muted);
        }

        a {
            color: var(--primary-color);
            text-decoration: none;
            transition: all 0.3s ease;
        }

        a:hover {
            color: white;
            text-shadow: var(--neon-glow);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: var(--section-padding);
            position: relative;
        }

        /* Styles du header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 1.5rem 0;
            background-color: rgba(10, 10, 26, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0, 240, 255, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            font-family: 'Orbitron', sans-serif;
            font-weight: 900;
            font-size: 1.8rem;
            color: var(--primary-color);
        }

        .logo-icon {
            margin-right: 10px;
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: var(--neon-glow);
        }

        .logo-icon::before {
            content: "T";
            font-family: 'Orbitron', sans-serif;
            font-weight: 900;
            color: var(--darker-bg);
            font-size: 1.5rem;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            position: relative;
            padding: 0.5rem 0;
            font-family: 'Orbitron', sans-serif;
            font-weight: 500;
            font-size: 0.9rem;
            text-transform: uppercase;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary-color);
            transition: width 0.3s ease;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--primary-color);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Styles du hero */
        .hero {
            height: 100vh;
            min-height: 800px;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            padding-top: 80px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 70% 30%, rgba(0, 102, 255, 0.2) 0%, transparent 30%),
                radial-gradient(circle at 30% 70%, rgba(0, 240, 255, 0.2) 0%, transparent 30%);
            z-index: -1;
        }

        .hero-content {
            max-width: 800px;
            position: relative;
            z-index: 1;
        }

        .hero h1 {
            font-size: 4rem;
            line-height: 1.2;
            margin-bottom: 2rem;
            text-transform: uppercase;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 20px rgba(0, 240, 255, 0.3);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 600px;
            margin-bottom: 3rem;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: var(--darker-bg);
            font-family: 'Orbitron', sans-serif;
            font-weight: 700;
            border-radius: 4px;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            overflow: hidden;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 0 15px rgba(0, 240, 255, 0.5);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 25px rgba(0, 240, 255, 0.8);
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: all 0.5s ease;
        }

        .btn:hover::before {
            left: 100%;
        }

        .tech-diagram {
            position: absolute;
            right: -100px;
            top: 50%;
            transform: translateY(-50%);
            width: 600px;
            height: 600px;
            opacity: 0.7;
            z-index: 0;
        }

        /* Styles des sections */
        .section-title {
            text-align: center;
            margin-bottom: 5rem;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            display: inline-block;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            position: relative;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
        }

        /* Styles des services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: rgba(15, 15, 35, 0.7);
            border-radius: 8px;
            padding: 2.5rem 2rem;
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 240, 255, 0.1);
            backdrop-filter: blur(5px);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0, 240, 255, 0.2);
            border-color: rgba(0, 240, 255, 0.3);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0, 240, 255, 0.05), transparent);
            z-index: -1;
        }

        .service-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            box-shadow: var(--neon-glow);
        }

        .service-icon svg {
            width: 30px;
            height: 30px;
            fill: var(--darker-bg);
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        /* Styles de la section À propos */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-image {
            position: relative;
            height: 500px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 500"><path d="M50,50 L450,50 L450,450 L50,450 Z" fill="none" stroke="%2300f0ff" stroke-width="2"/><circle cx="250" cy="250" r="150" fill="none" stroke="%230066ff" stroke-width="2"/><line x1="50" y1="250" x2="450" y2="250" stroke="%2300f0ff" stroke-width="1"/><line x1="250" y1="50" x2="250" y2="450" stroke="%2300f0ff" stroke-width="1"/></svg>') center/contain no-repeat;
            background-color: rgba(10, 15, 30, 0.5);
            border-radius: 8px;
            border: 1px solid rgba(0, 240, 255, 0.2);
        }

        .about-text {
            position: relative;
        }

        .about-item {
            margin-bottom: 2rem;
            padding-left: 2rem;
            border-left: 2px solid var(--primary-color);
        }

        .about-item h3 {
            font-size: 1.2rem;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .about-item p {
            color: var(--text-color);
        }

        /* Styles de la section Contact */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-form {
            background: rgba(15, 15, 35, 0.7);
            padding: 2.5rem;
            border-radius: 8px;
            border: 1px solid rgba(0, 240, 255, 0.1);
            backdrop-filter: blur(5px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-family: 'Orbitron', sans-serif;
            font-weight: 500;
            color: var(--primary-color);
        }

        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            background: rgba(10, 10, 25, 0.8);
            border: 1px solid rgba(0, 240, 255, 0.2);
            border-radius: 4px;
            color: var(--text-color);
            font-family: 'Exo', sans-serif;
            transition: all 0.3s ease;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 10px rgba(0, 240, 255, 0.3);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        .contact-info {
            padding: 2rem;
        }

        .contact-info h3 {
            color: var(--primary-color);
            margin-bottom: 2rem;
        }

        .contact-details {
            margin-bottom: 3rem;
        }

        .contact-detail {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .contact-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1rem;
            flex-shrink: 0;
        }

        .contact-icon svg {
            width: 20px;
            height: 20px;
            fill: var(--darker-bg);
        }

        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(0, 240, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 240, 255, 0.2);
        }

        .social-link:hover {
            background: rgba(0, 240, 255, 0.2);
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 240, 255, 0.3);
        }

        .social-link svg {
            width: 24px;
            height: 24px;
            fill: var(--primary-color);
        }

        /* Styles du footer */
        footer {
            background: var(--darker-bg);
            padding: 3rem 0;
            text-align: center;
            border-top: 1px solid rgba(0, 240, 255, 0.1);
        }

        .footer-logo {
            font-family: 'Orbitron', sans-serif;
            font-weight: 900;
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            display: inline-block;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-links a {
            font-family: 'Orbitron', sans-serif;
            font-weight: 500;
            font-size: 0.9rem;
            text-transform: uppercase;
        }

        .copyright {
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Styles des appareils électroniques */
        .device-showcase {
            margin-top: 5rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .device-card {
            background: rgba(15, 15, 35, 0.7);
            border-radius: 8px;
            padding: 2rem;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 240, 255, 0.1);
            transition: all 0.3s ease;
        }

        .device-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 240, 255, 0.1);
        }

        .device-image {
            height: 200px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 200"><rect x="20" y="20" width="260" height="160" rx="10" fill="%2310151f" stroke="%2300f0ff" stroke-width="1"/><rect x="40" y="40" width="220" height="120" fill="%23050a15"/><circle cx="260" cy="50" r="5" fill="%2300f0ff"/><circle cx="240" cy="50" r="5" fill="%230066ff"/></svg>') center/contain no-repeat;
            margin-bottom: 1.5rem;
        }

        .device-card h3 {
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .device-specs {
            list-style: none;
        }

        .device-specs li {
            margin-bottom: 0.5rem;
            position: relative;
            padding-left: 1.5rem;
            color: var(--text-muted);
        }

        .device-specs li::before {
            content: '';
            position: absolute;
            left: 0;
            top: 8px;
            width: 8px;
            height: 2px;
            background: var(--primary-color);
        }

        /* Styles des diagrammes */
        .diagram-container {
            margin: 5rem auto;
            max-width: 800px;
            background: rgba(15, 15, 35, 0.7);
            border-radius: 8px;
            padding: 2rem;
            border: 1px solid rgba(0, 240, 255, 0.1);
        }

        .diagram-title {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary-color);
        }

        .diagram {
            height: 400px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 400"><path d="M50,350 L150,150 L250,250 L350,100 L450,300 L550,200 L650,350 L750,50" fill="none" stroke="%2300f0ff" stroke-width="3"/><circle cx="50" cy="350" r="5" fill="%2300f0ff"/><circle cx="150" cy="150" r="5" fill="%2300f0ff"/><circle cx="250" cy="250" r="5" fill="%2300f0ff"/><circle cx="350" cy="100" r="5" fill="%2300f0ff"/><circle cx="450" cy="300" r="5" fill="%2300f0ff"/><circle cx="550" cy="200" r="5" fill="%2300f0ff"/><circle cx="650" cy="350" r="5" fill="%2300f0ff"/><circle cx="750" cy="50" r="5" fill="%2300f0ff"/><text x="50" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q1</text><text x="150" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q2</text><text x="250" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q3</text><text x="350" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q4</text><text x="450" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q5</text><text x="550" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q6</text><text x="650" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q7</text><text x="750" y="380" font-family="Arial" font-size="12" fill="%2300f0ff" text-anchor="middle">Q8</text><text x="400" y="30" font-family="Arial" font-size="14" fill="%2300f0ff" text-anchor="middle">Performances technologiques</text></svg>') center/contain no-repeat;
        }

        /* Styles responsives */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3rem;
            }

            .about-content, .contact-container {
                grid-template-columns: 1fr;
            }

            .about-image {
                height: 300px;
                order: -1;
            }
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                text-align: center;
            }

            .logo {
                margin-bottom: 1rem;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
            }

            nav ul li {
                margin: 0.5rem 0;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .tech-diagram {
                display: none;
            }

            .section-title h2 {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .btn {
                padding: 0.8rem 1.5rem;
                font-size: 0.9rem;
            }

            .section-title h2 {
                font-size: 1.8rem;
            }

            .service-card, .device-card {
                padding: 1.5rem;
            }
        }

        /* Animations */
        @keyframes pulse {
            0% { opacity: 0.5; }
            50% { opacity: 1; }
            100% { opacity: 0.5; }
        }

        .pulse {
            animation: pulse 2s infinite ease-in-out;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }

        .float {
            animation: float 3s infinite ease-in-out;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <div class="logo-icon"></div>
                <span>TITAN TECH</span>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Accueil</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#about">À propos</a></li>
                    <li><a href="#devices">Technologies</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Titan Tech — L'intelligence du futur, aujourd'hui.</h1>
                <p>Titan Tech est une entreprise pionnière dans l'innovation technologique. Notre mission : concevoir les technologies de demain pour transformer le monde d'aujourd'hui.</p>
                <a href="#about" class="btn">En savoir plus</a>
            </div>
        </div>
        <div class="tech-diagram float">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 600">
                <circle cx="300" cy="300" r="250" fill="none" stroke="rgba(0, 240, 255, 0.2)" stroke-width="1"/>
                <circle cx="300" cy="300" r="200" fill="none" stroke="rgba(0, 240, 255, 0.2)" stroke-width="1"/>
                <circle cx="300" cy="300" r="150" fill="none" stroke="rgba(0, 240, 255, 0.2)" stroke-width="1"/>
                <circle cx="300" cy="300" r="100" fill="none" stroke="rgba(0, 240, 255, 0.2)" stroke-width="1"/>
                <line x1="50" y1="300" x2="550" y2="300" stroke="rgba(0, 240, 255, 0.2)" stroke-width="1"/>
                <line x1="300" y1="50" x2="300" y2="550" stroke="rgba(0, 240, 255, 0.2)" stroke-width="1"/>
                <path d="M300,50 L350,150 L250,200 L350,250 L250,350 L350,400 L300,500 L250,400 L350,350 L250,250 L350,200 L250,150 Z" fill="none" stroke="#00f0ff" stroke-width="2" fill-opacity="0.1"/>
                <circle cx="300" cy="300" r="10" fill="#00f0ff"/>
            </svg>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <div class="section-title">
                <h2>Nos Services</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M20.5 11H19V7a2 2 0 0 0-2-2h-4V3.5a2.5 2.5 0 0 0-5 0V5H4a2 2 0 0 0-2 2v4H1.5a2.5 2.5 0 0 0 0 5H4v4a2 2 0 0 0 2 2h4v1.5a2.5 2.5 0 0 0 5 0V19h4a2 2 0 0 0 2-2v-4h1.5a2.5 2.5 0 0 0 0-5z"/>
                        </svg>
                    </div>
                    <h3>Développement logiciel sur mesure</h3>
                    <p>Solutions logicielles personnalisées conçues pour répondre précisément à vos besoins métiers avec les dernières technologies.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 3L1 9l11 6 9-4.91V17h2V9M5 13.18v4L12 21l7-3.82v-4L12 17l-7-3.82z"/>
                        </svg>
                    </div>
                    <h3>Cybersécurité avancée</h3>
                    <p>Protection complète de vos systèmes et données contre les cybermenaces avec nos solutions de sécurité de pointe.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M19 3H5a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2zm0 16H5V5h14v14zM7 12h2v5H7zm4-7h2v12h-2zm4 5h2v7h-2z"/>
                        </svg>
                    </div>
                    <h3>Solutions cloud intelligentes</h3>
                    <p>Migration, gestion et optimisation de votre infrastructure cloud pour une performance et une évolutivité maximales.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 2a2 2 0 0 0-2 2c0 1.11.89 2 2 2 1.11 0 2-.89 2-2a2 2 0 0 0-2-2m9 7v6h-2v6h-2v2H9v-2H7v-6H5V9h2V3h2v2h6V3h2v6h2z"/>
                        </svg>
                    </div>
                    <h3>Intelligence Artificielle personnalisée</h3>
                    <p>Implémentation de solutions IA adaptées à votre secteur d'activité pour automatiser et optimiser vos processus.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="bg-dark">
        <div class="container">
            <div class="section-title">
                <h2>À propos</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <div class="about-item">
                        <h3>Mission</h3>
                        <p>"Innover sans limites." Nous repoussons les frontières technologiques pour créer des solutions qui redéfinissent les possibles.</p>
                    </div>
                    <div class="about-item">
                        <h3>Vision</h3>
                        <p>"Connecter l'humain au futur grâce à la technologie." Nous croyons en une symbiose harmonieuse entre l'homme et la machine.</p>
                    </div>
                    <div class="about-item">
                        <h3>Valeurs</h3>
                        <p>"Transparence, Éthique, Excellence, Créativité." Ces principes guident chacune de nos décisions et innovations.</p>
                    </div>
                </div>
                <div class="about-image pulse"></div>
            </div>
        </div>
    </section>

    <!-- Devices Section -->
    <section id="devices">
        <div class="container">
            <div class="section-title">
                <h2>Nos Technologies</h2>
            </div>
            <div class="device-showcase">
                <div class="device-card">
                    <div class="device-image"></div>
                    <h3>Titan Neural Core</h3>
                    <ul class="device-specs">
                        <li>Processeur quantique 128 qubits</li>
                        <li>Architecture neuronale biomimétique</li>
                        <li>Consommation énergétique réduite de 60%</li>
                        <li>Compatibilité avec les réseaux 7G</li>
                    </ul>
                </div>
                <div class="device-card">
                    <div class="device-image"></div>
                    <h3>CyberShield X9</h3>
                    <ul class="device-specs">
                        <li>Protection contre les attaques quantiques</li>
                        <li>Détection des menaces en temps réel</li>
                        <li>Chiffrement post-quantique</li>
                        <li>Interface de gestion holographique</li>
                    </ul>
                </div>
                <div class="device-card">
                    <div class="device-image"></div>
                    <h3>Nebula Cloud Node</h3>
                    <ul class="device-specs">
                        <li>Stockage distribué sécurisé</li>
                        <li>Latence inférieure à 1ms</li>
                        <li>Auto-évolutivité intelligente</li>
                        <li>Intégration IA native</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Diagram Section -->
    <section>
        <div class="container">
            <div class="diagram-container">
                <div class="diagram-title">
                    <h3>Performances de nos solutions</h3>
                </div>
                <div class="diagram"></div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contactez-nous</h2>
            </div>
            <div class="contact-container">
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Nom</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn">Envoyer</button>
                    </form>
                </div>
                <div class="contact-info">
                    <h3>Coordonnées</h3>
                    <div class="contact-details">
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                    <path d="M20 8l-8 5-8-5V6l8 5 8-5m0-2H4c-1.11 0-2 .89-2 2v12a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2z"/>
                                </svg>
                            </div>
                            <div>
                                <p>Email</p>
                                <a href="mailto:TITANtech233@gmail.com">TITANtech233@gmail.com</a>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                    <path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/>
                                </svg>
                            </div>
                            <div>
                                <p>Téléphone</p>
                                <a href="tel:+22890855001">+228 90855001</a>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-icon">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                    <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/>
                                </svg>
                            </div>
                            <div>
                                <p>Adresse</p>
                                <p>42 Avenue de la technologie, Lomé,TOGO</p>
                            </div>
                        </div>
                    </div>
                    <h3>Réseaux sociaux</h3>
                    <div class="social-links">
                        <a href="https://facebook.com/Roger AyAh" class="social-link" target="_blank">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 4.84 3.44 8.87 8 9.8V15H8v-3h2V9.5C10 7.57 11.57 6 13.5 6H16v3h-2c-.55 0-1 .45-1 1v2h3v3h-3v6.95c5.05-.5 9-4.76 9-9.95z"/>
                            </svg>
                        </a>
                        <a href="https://instagram.com/ayah.roger" class="social-link" target="_blank">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M12 2.16c2.67 0 2.99.01 4.04.05 2.64.12 3.48 1.46 3.61 3.61.04 1.05.05 1.37.05 4.04s-.01 2.99-.05 4.04c-.12 2.65-1.46 3.49-3.61 3.61-1.05.04-1.37.05-4.04.05s-2.99-.01-4.04-.05c-2.65-.12-3.49-1.46-3.61-3.61-.04-1.05-.05-1.37-.05-4.04s.01-2.99.05-4.04c.12-2.65 1.46-3.49 3.61-3.61 1.05-.04 1.37-.05 4.04-.05m0-1.6c-2.72 0-3.07.01-4.13.05-3.38.16-4.93 1.71-5.09 5.09-.04 1.06-.05 1.41-.05 4.13s.01 3.07.05 4.13c.16 3.38 1.71 4.93 5.09 5.09 1.06.04 1.41.05 4.13.05s3.07-.01 4.13-.05c3.38-.16 4.93-1.71 5.09-5.09.04-1.06.05-1.41.05-4.13s-.01-3.07-.05-4.13c-.16-3.38-1.71-4.93-5.09-5.09-1.06-.04-1.41-.05-4.13-.05zM12 6.34c-3.13 0-5.66 2.53-5.66 5.66S8.87 17.66 12 17.66s5.66-2.53 5.66-5.66S15.13 6.34 12 6.34zm0 9.33c-2.02 0-3.66-1.64-3.66-3.66S9.98 8.35 12 8.35s3.66 1.64 3.66 3.66-1.64 3.66-3.66 3.66zM16.5 5.5c0 .83-.67 1.5-1.5 1.5s-1.5-.67-1.5-1.5.67-1.5 1.5-1.5 1.5.67 1.5 1.5z"/>
                            </svg>
                        </a>
                        <a href="https://twitter.com/ayah kossi Roger" class="social-link" target="_blank">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M22.46 6c-.77.35-1.6.58-2.46.69.88-.53 1.56-1.37 1.88-2.38-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29 0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15 0 1.49.75 2.81 1.91 3.56-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07 4.28 4.28 0 0 0 4 2.98 8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21 16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56.84-.6 1.56-1.36 2.14-2.23z"/>
                            </svg>
                        </a>
                        <a href="https://wa.me/90855001" class="social-link" target="_blank">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-6.29-11.96c-5.297 0-9.588 4.29-9.588 9.586 0 1.908.56 3.682 1.516 5.177L1.71 20.8l5.59-1.548a9.545 9.545 0 0 0 4.874 1.329c5.297 0 9.589-4.289 9.589-9.585 0-5.297-4.292-9.586-9.589-9.586m0 16.553a6.952 6.952 0 0 1-3.53-.943l-.253-.152-2.821.78.753-2.733-.177-.282a6.96 6.96 0 0 1-1.071-3.704c0-3.85 3.13-6.978 6.98-6.978 3.85 0 6.978 3.13 6.978 6.978 0 3.85-3.13 6.98-6.978 6.98z"/>
                            </svg>
                        </a>
                        <a href="https://tiktok.com/@cylaces" class="social-link" target="_blank">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                            </svg>
                        </a>
                        <a href="https://youtube.com/@rogerayah8043" class="social-link" target="_blank">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M10 15l5.19-3L10 9v6m11.56-7.83c.13.47.22 1.1.28 1.87.05.77.08 1.67.08 2.68v.53c0 1.1-.01 2.01-.08 2.78-.06.77-.15 1.4-.28 1.87-.13.47-.32.89-.56 1.24-.24.35-.54.65-.89.89-.35.24-.77.43-1.24.56-.47.13-1.1.22-1.87.28-.77.05-1.67.08-2.68.08h-.53c-1.1 0-2.01-.01-2.78-.08-.77-.06-1.4-.15-1.87-.28-.47-.13-.89-.32-1.24-.56-.35-.24-.65-.54-.89-.89-.24-.35-.43-.77-.56-1.24-.13-.47-.22-1.1-.28-1.87A31 31 0 0 1 3 11.5v-.53c0-1.1.01-2.01.08-2.78.06-.77.15-1.4.28-1.87.13-.47.32-.89.56-1.24.24-.35.54-.65.89-.89.35-.24.77-.43 1.24-.56.47-.13 1.1-.22 1.87-.28.77-.05 1.67-.08 2.68-.08h.53c1.1 0 2.01.01 2.78.08.77.06 1.4.15 1.87.28.47.13.89.32 1.24.56.35.24.65.54.89.89.24.35.43.77.56 1.24z"/>
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-logo">TITAN TECH</div>
            <div class="footer-links">
                <a href="#home">Accueil</a>
                <a href="#services">Services</a>
                <a href="#about">À propos</a>
                <a href="#devices">Technologies</a>
                <a href="#contact">Contact</a>
                <a href="#">Mentions légales</a>
                <a href="#">Politique de confidentialité</a>
            </div>
            <div class="copyright">
                © 2023 Titan Tech. Tous droits réservés.
            </div>
        </div>
    </footer>
</body>
</html>
