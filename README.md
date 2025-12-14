<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CreduxAI - KI-Chatbots für lokale Unternehmen</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #3a86ff;
            --primary-dark: #2667cc;
            --secondary: #8338ec;
            --dark: #212529;
            --light: #f8f9fa;
            --gray: #6c757d;
            --success: #38b000;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            --radius: 10px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Navigation */
        header {
            background-color: white;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo i {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .nav-cta {
            background-color: var(--primary);
            color: white;
            padding: 10px 25px;
            border-radius: var(--radius);
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .nav-cta:hover {
            background-color: var(--primary-dark);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--primary);
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            padding: 100px 0;
            background: linear-gradient(135deg, #f5f7ff 0%, #e9edff 100%);
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .hero h1 span {
            color: var(--primary);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 40px;
            color: var(--gray);
        }
        
        .hero-btns {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 30px;
        }
        
        .btn-primary, .btn-secondary {
            padding: 15px 30px;
            border-radius: var(--radius);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            display: inline-block;
            transition: all 0.3s;
        }
        
        .btn-primary {
            background-color: var(--primary);
            color: white;
        }
        
        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }
        
        .btn-secondary {
            background-color: white;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .btn-secondary:hover {
            background-color: var(--light);
            transform: translateY(-3px);
            box-shadow: var(--shadow);
        }
        
        /* Services Section */
        .section {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: white;
            border-radius: var(--radius);
            padding: 40px 30px;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-icon {
            width: 70px;
            height: 70px;
            background-color: rgba(58, 134, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 25px;
        }
        
        .service-icon i {
            font-size: 1.8rem;
            color: var(--primary);
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        /* Features Section */
        .features {
            background-color: #f8f9ff;
        }
        
        .feature {
            display: flex;
            align-items: center;
            margin-bottom: 60px;
            gap: 50px;
        }
        
        .feature:nth-child(even) {
            flex-direction: row-reverse;
        }
        
        .feature-image {
            flex: 1;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
        }
        
        .feature-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .feature-content {
            flex: 1;
        }
        
        .feature-content h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--dark);
        }
        
        .feature-content ul {
            list-style-position: inside;
            margin-top: 20px;
        }
        
        .feature-content li {
            margin-bottom: 10px;
            color: var(--gray);
        }
        
        /* Pricing Section */
        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .pricing-card {
            background-color: white;
            border-radius: var(--radius);
            padding: 40px 30px;
            box-shadow: var(--shadow);
            text-align: center;
            position: relative;
        }
        
        .pricing-card.popular {
            border: 2px solid var(--primary);
            transform: scale(1.05);
        }
        
        .popular-badge {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            background-color: var(--primary);
            color: white;
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 0.9rem;
        }
        
        .pricing-header h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .price {
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        .price span {
            font-size: 1rem;
            color: var(--gray);
        }
        
        .pricing-features {
            margin: 30px 0;
            text-align: left;
        }
        
        .pricing-features li {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .pricing-features i {
            color: var(--success);
        }
        
        /* Contact Section */
        .contact {
            background-color: var(--dark);
            color: white;
        }
        
        .contact .section-title h2 {
            color: white;
        }
        
        .contact .section-title p {
            color: #adb5bd;
        }
        
        .contact-container {
            display: flex;
            gap: 50px;
        }
        
        .contact-info {
            flex: 1;
        }
        
        .contact-form {
            flex: 1;
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 30px;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .contact-icon i {
            font-size: 1.2rem;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            border-radius: var(--radius);
            border: none;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1rem;
        }
        
        .form-control:focus {
            outline: 2px solid var(--primary);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: #1a1a1a;
            color: #adb5bd;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .footer-links h4 {
            color: white;
            margin-bottom: 20px;
            font-size: 1.2rem;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #adb5bd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
        }
        
        /* Platform Recommendations */
        .platforms {
            background-color: #f8f9ff;
            text-align: center;
        }
        
        .platform-cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
        }
        
        .platform-card {
            background-color: white;
            border-radius: var(--radius);
            padding: 30px;
            width: 250px;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }
        
        .platform-card:hover {
            transform: translateY(-5px);
        }
        
        .platform-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .platform-card h3 {
            margin-bottom: 15px;
            color: var(--dark);
        }
        
        .platform-card a {
            display: inline-block;
            margin-top: 15px;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .feature {
                flex-direction: column;
                gap: 30px;
            }
            
            .feature:nth-child(even) {
                flex-direction: column;
            }
            
            .contact-container {
                flex-direction: column;
            }
        }
        
        @media (max-width: 768px) {
            .navbar {
                flex-wrap: wrap;
            }
            
            .nav-links {
                display: none;
                width: 100%;
                flex-direction: column;
                text-align: center;
                margin-top: 20px;
                gap: 15px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero-btns {
                flex-direction: column;
                align-items: center;
            }
            
            .btn-primary, .btn-secondary {
                width: 100%;
                max-width: 300px;
                text-align: center;
            }
            
            .pricing-card.popular {
                transform: none;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .section {
                padding: 60px 0;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">
                    <i class="fas fa-robot"></i>
                    CreduxAI
                </a>
                
                <ul class="nav-links">
                    <li><a href="#home">Start</a></li>
                    <li><a href="#services">Leistungen</a></li>
                    <li><a href="#features">Vorteile</a></li>
                    <li><a href="#pricing">Preise</a></li>
                    <li><a href="#platforms">Plattformen</a></li>
                    <li><a href="#contact">Kontakt</a></li>
                </ul>
                
                <a href="#contact" class="nav-cta">Kostenlose Beratung</a>
                
                <button class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </button>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>KI-Chatbots für <span>lokale Unternehmen</span></h1>
            <p>CreduxAI entwickelt intelligente Chatbot-Lösungen, die Ihren Kundenservice automatisieren, Leads generieren und Ihr Unternehmen 24/7 verfügbar machen.</p>
            
            <div class="hero-btns">
                <a href="#services" class="btn-primary">Unsere Lösungen entdecken</a>
                <a href="#contact" class="btn-secondary">Kostenlose Demo anfordern</a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="section" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Unsere Chatbot-Leistungen</h2>
                <p>Maßgeschneiderte KI-Lösungen für verschiedene Geschäftsanforderungen</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>Kundenservice-Chatbot</h3>
                    <p>Beantwortet häufige Kundenfragen rund um die Uhr, entlastet Ihr Personal und sorgt für zufriedene Kunden.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h3>Verkaufs- & Buchungsbot</h3>
                    <p>Unterstützt Kunden bei der Produktauswahl, nimmt Bestellungen entgegen und vereinbart Termine automatisch.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-comments"></i>
                    </div>
                    <h3>Multi-Channel Integration</h3>
                    <p>Ihr Chatbot ist auf Website, WhatsApp, Facebook und Instagram verfügbar - alles aus einer Hand.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="section features" id="features">
        <div class="container">
            <div class="section-title">
                <h2>Warum CreduxAI wählen?</h2>
                <p>Unsere KI-Chatbots bieten mehr als nur automatische Antworten</p>
            </div>
            
            <div class="feature">
                <div class="feature-image">
                    <!-- Platzhalter für Bild -->
                    <div style="background-color: var(--primary); height: 300px; display: flex; align-items: center; justify-content: center; color: white; font-size: 1.5rem;">
                        KI-Chatbot Dashboard
                    </div>
                </div>
                <div class="feature-content">
                    <h3>Maßgeschneidert für Ihr Unternehmen</h3>
                    <p>Wir entwickeln keine Standardlösungen. Jeder CreduxAI-Chatbot wird individuell auf Ihre Geschäftsprozesse, Produkte und Dienstleistungen abgestimmt.</p>
                    <ul>
                        <li>Individuelle Trainingsdaten für Ihre Branche</li>
                        <li>Integration in bestehende Systeme (CRM, Buchungssysteme)</li>
                        <li>Anpassung an Ihren Unternehmens-Tonfall</li>
                    </ul>
                </div>
            </div>
            
            <div class="feature">
                <div class="feature-image">
                    <!-- Platzhalter für Bild -->
                    <div style="background-color: var(--secondary); height: 300px; display: flex; align-items: center; justify-content: center; color: white; font-size: 1.5rem;">
                        Analytics & Reporting
                    </div>
                </div>
                <div class="feature-content">
                    <h3>Datengetriebene Optimierung</h3>
                    <p>Unsere Chatbots lernen kontinuierlich aus Kundeninteraktionen und liefern wertvolle Einblicke in Kundenbedürfnisse.</p>
                    <ul>
                        <li>Detaillierte Analytics zu Kundenanfragen</li>
                        <li>Erkennung häufiger Probleme und Fragen</li>
                        <li>Automatische Performance-Berichte</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section class="section" id="pricing">
        <div class="container">
            <div class="section-title">
                <h2>Transparente Preisgestaltung</h2>
                <p>Flexible Pakete für jedes Budget</p>
            </div>
            
            <div class="pricing-grid">
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Starter</h3>
                        <div class="price">€99<span>/Monat</span></div>
                        <p>Für kleine Unternehmen und Einzelhändler</p>
                    </div>
                    
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Basis-Chatbot für Website</li>
                        <li><i class="fas fa-check"></i> Bis zu 500 Gespräche/Monat</li>
                        <li><i class="fas fa-check"></i> E-Mail Integration</li>
                        <li><i class="fas fa-check"></i> Standard-Training</li>
                        <li><i class="fas fa-times"></i> Keine Social Media Integration</li>
                    </ul>
                    
                    <a href="#contact" class="btn-secondary">Starter wählen</a>
                </div>
                
                <div class="pricing-card popular">
                    <div class="popular-badge">Am beliebtesten</div>
                    <div class="pricing-header">
                        <h3>Business</h3>
                        <div class="price">€249<span>/Monat</span></div>
                        <p>Für wachsende Unternehmen mit mehreren Standorten</p>
                    </div>
                    
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Erweiterter KI-Chatbot</li>
                        <li><i class="fas fa-check"></i> Bis zu 2.000 Gespräche/Monat</li>
                        <li><i class="fas fa-check"></i> WhatsApp & Facebook Integration</li>
                        <li><i class="fas fa-check"></i> Erweitertes Training</li>
                        <li><i class="fas fa-check"></i> CRM-Anbindung</li>
                    </ul>
                    
                    <a href="#contact" class="btn-primary">Business wählen</a>
                </div>
                
                <div class="pricing-card">
                    <div class="pricing-header">
                        <h3>Enterprise</h3>
                        <div class="price">Individuell</div>
                        <p>Für große Unternehmen mit speziellen Anforderungen</p>
                    </div>
                    
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Vollständig angepasster Chatbot</li>
                        <li><i class="fas fa-check"></i> Unbegrenzte Gespräche</li>
                        <li><i class="fas fa-check"></i> Multi-Channel auf allen Plattformen</li>
                        <li><i class="fas fa-check"></i> API-Zugang & eigene Integrationen</li>
                        <li><i class="fas fa-check"></i> Prioritäts-Support 24/7</li>
                    </ul>
                    
                    <a href="#contact" class="btn-secondary">Individuelles Angebot</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Platforms Section -->
    <section class="section platforms" id="platforms">
        <div class="container">
            <div class="section-title">
                <h2>Wo können Sie die Website erstellen?</h2>
                <p>Empfohlene Plattformen für die Entwicklung und das Hosting Ihrer CreduxAI-Website</p>
            </div>
            
            <div class="platform-cards">
                <div class="platform-card">
                    <div class="platform-icon">
                        <i class="fab fa-wordpress"></i>
                    </div>
                    <h3>WordPress</h3>
                    <p>Flexibel, erweiterbar und perfekt für Content-Management. Viele Plugins verfügbar.</p>
                    <a href="https://wordpress.org" target="_blank">Zur Website →</a>
                </div>
                
                <div class="platform-card">
                    <div class="platform-icon">
                        <i class="fab fa-wix"></i>
                    </div>
                    <h3>Wix</h3>
                    <p>Benutzerfreundlicher Drag-and-Drop-Editor, ideal für Anfänger ohne Programmierkenntnisse.</p>
                    <a href="https://www.wix.com" target="_blank">Zur Website →</a>
                </div>
                
                <div class="platform-card">
                    <div class="platform-icon">
                        <i class="fas fa-cloud"></i>
                    </div>
                    <h3>Webflow</h3>
                    <p>Professionelles Design mit visuellem Editor und flexiblen Hosting-Optionen.</p>
                    <a href="https://webflow.com" target="_blank">Zur Website →</a>
                </div>
                
                <div class="platform-card">
                    <div class="platform-icon">
                        <i class="fab fa-squarespace"></i>
                    </div>
                    <h3>Squarespace</h3>
                    <p>Hochwertige Templates und alles-in-einem-Lösung für anspruchsvolle Designs.</p>
                    <a href="https://www.squarespace.com" target="_blank">Zur Website →</a>
                </div>
            </div>
            
            <div style="margin-top: 50px; background-color: white; padding: 30px; border-radius: var(--radius); box-shadow: var(--shadow);">
                <h3 style="color: var(--dark); margin-bottom: 15px;">Empfehlung für CreduxAI</h3>
                <p style="color: var(--gray);">Für eine professionelle Service-Website wie CreduxAI empfehlen wir <strong>WordPress mit Elementor</strong> oder <strong>Webflow</strong>. Diese Plattformen bieten maximale Flexibilität für die Integration von Chatbot-Demonstrationen, Buchungssystemen und Kundendashboards. Bei Bedarf können wir Ihnen bei der Umsetzung helfen!</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="section contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Kontaktieren Sie uns</h2>
                <p>Vereinbaren Sie ein kostenloses Beratungsgespräch für Ihre Chatbot-Lösung</p>
            </div>
            
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Adresse</h3>
                            <p>Musterstraße 123<br>10115 Berlin, Deutschland</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Telefon</h3>
                            <p>+49 (0)30 12345678</p>
                            <p>Mo-Fr: 9:00-18:00 Uhr</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>E-Mail</h3>
                            <p>info@creduxai.de</p>
                            <p>support@creduxai.de</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Ihr Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Max Mustermann" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Ihre E-Mail</label>
                            <input type="email" id="email" class="form-control" placeholder="name@beispiel.de" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="business">Unternehmen & Branche</label>
                            <input type="text" id="business" class="form-control" placeholder="z.B. Restaurant, Einzelhandel, Dienstleistung" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Ihre Nachricht</label>
                            <textarea id="message" class="form-control" placeholder="Beschreiben Sie kurz Ihr Vorhaben und welche Art von Chatbot Sie benötigen..." required></textarea>
                        </div>
                        
                        <button type="submit" class="btn-primary" style="width: 100%;">Nachricht senden</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">
                        <i class="fas fa-robot"></i>
                        CreduxAI
                    </div>
                    <p>Wir entwickeln intelligente Chatbot-Lösungen für lokale Unternehmen, um Kundenservice zu optimieren und Umsätze zu steigern.</p>
                    
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h4>Schnelllinks</h4>
                    <ul>
                        <li><a href="#home">Start</a></li>
                        <li><a href="#services">Leistungen</a></li>
                        <li><a href="#features">Vorteile</a></li>
                        <li><a href="#pricing">Preise</a></li>
                        <li><a href="#platforms">Plattformen</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h4>Rechtliches</h4>
                    <ul>
                        <li><a href="#">Impressum</a></li>
                        <li><a href="#">Datenschutz</a></li>
                        <li><a href="#">AGB</a></li>
                        <li><a href="#">Cookie-Richtlinie</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h4>Ressourcen</h4>
                    <ul>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Chatbot-Beispiele</a></li>
                        <li><a href="#">Dokumentation</a></li>
                        <li><a href="#">Support-Center</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 CreduxAI. Alle Rechte vorbehalten.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Navigation Toggle
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    // Close mobile menu if open
                    document.querySelector('.nav-links').classList.remove('active');
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Contact form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const business = document.getElementById('business').value;
            const message = document.getElementById('message').value;
            
            // In a real application, you would send this data to a server
            // For this demo, we'll just show an alert
            alert(`Vielen Dank, ${name}! Wir haben Ihre Anfrage erhalten und melden uns innerhalb von 24 Stunden bei Ihnen unter ${email}.`);
            
            // Reset form
            this.reset();
        });
        
        // Add scroll effect to header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if(window.scrollY > 100) {
                header.style.boxShadow = '0 5px 20px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.1)';
            }
        });
    </script>
</body>
</html>
