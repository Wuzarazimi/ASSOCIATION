<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Association GOLLUM NOEL - Vieillir en Santé</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap');
        
        :root {
            --primary-green: #2E8B57;
            --secondary-teal: #20B2AA;
            --accent-blue: #4682B4;
            --warm-orange: #2E8B57 --#FF6B35;
            --light-gray: #f8f9fa;
            --text-dark: #333333;
            --text-light: #666666;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            overflow-x: hidden;
        }
        
        /* Header */
        .header {
            background: linear-gradient(135deg, var(--primary-green) 0%, var(--secondary-teal) 50%, var(--accent-blue) 100%);
            color: white;
            padding: 2rem 0;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -20%;
            width: 400px;
            height: 400px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        .header::after {
            content: '';
            position: absolute;
            bottom: -30%;
            left: -10%;
            width: 300px;
            height: 300px;
            background: rgba(255,255,255,0.05);
            border-radius: 50%;
            animation: float 8s ease-in-out infinite reverse;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }
        
        .header-content {
            display: flex;
            align-items: center;
            gap: 2rem;
        }
        
        .logo-section {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }
        
        .logo {
            width: 100px;
            height: 100px;
            background: linear-gradient(45deg, var(--warm-orange), #F7931E);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 8px 25px rgba(0,0,0,0.2);
            border: 4px solid rgba(255,255,255,0.3);
        }
        
        .logo svg {
            width: 50px;
            height: 50px;
            fill: white;
        }
        
        .brand-info h1 {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .tagline {
            font-size: 1.2rem;
            opacity: 0.95;
            font-style: italic;
        }
        
        .project-highlight {
            background: rgba(255,255,255,0.15);
            padding: 1rem 1.5rem;
            border-radius: 10px;
            backdrop-filter: blur(10px);
            margin-top: 1rem;
        }
        
        /* Navigation */
        .nav {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }
        
        .nav-content {
            display: flex;
            justify-content: center;
            gap: 2rem;
        }
        
        .nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            transition: all 0.3s ease;
        }
        
        .nav a:hover {
            background: var(--primary-green);
            color: white;
            transform: translateY(-2px);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(46,139,87,0.05), rgba(32,178,170,0.05));
            padding: 4rem 0;
            text-align: center;
        }
        
        .hero h2 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--primary-green);
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            color: var(--text-light);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .stat-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 800;
            color: var(--primary-green);
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            color: var(--text-light);
            font-weight: 500;
        }
        
        /* Section Styles */
        .section {
            padding: 4rem 0;
        }
        
        .section-alt {
            background: var(--light-gray);
        }
        
        .section h3 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
            color: var(--primary-green);
        }
        
        /* Mission Section */
        .mission-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .mission-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-left: 4px solid var(--primary-green);
        }
        
        .mission-card h4 {
            color: var(--primary-green);
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }
        
        /* Team Section */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .team-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        .team-card:hover {
            transform: translateY(-5px);
        }
        
        .team-role {
            color: var(--primary-green);
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        
        /* Results Section */
        .results-content {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            margin: 2rem 0;
        }
        
        .results-highlight {
            background: linear-gradient(135deg, var(--primary-green), var(--secondary-teal));
            color: white;
            padding: 2rem;
            border-radius: 15px;
            margin: 2rem 0;
            text-align: center;
        }
        
        .results-highlight h4 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .contact-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }
        
        .contact-item svg {
            width: 20px;
            height: 20px;
            margin-right: 10px;
            fill: var(--primary-green);
        }
        
        /* Footer */
        .footer {
            background: linear-gradient(135deg, var(--primary-green), var(--secondary-teal));
            color: white;
            padding: 3rem 0 2rem;
            text-align: center;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-section h4 {
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }
        
        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.2);
            padding-top: 2rem;
            margin-top: 2rem;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            .brand-info h1 {
                font-size: 2rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .nav-content {
                flex-wrap: wrap;
                gap: 1rem;
            }
            
            .container {
                padding: 0 1rem;
            }
        }
        
        /* Scroll Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.6s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <div class="header-content">
                <div class="logo-section">
                    <div class="logo">
                        <svg viewBox="0 0 24 24">
                            <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                        </svg>
                    </div>
                    <div class="brand-info">
                        <h1>ASSOCIATION GOLLUM NOEL</h1>
                        <p class="tagline">Sensibilisation et prise en charge en kinésithérapie</p>
                        <div class="project-highlight">
                            <strong>Projet Pilote "VIEILLIR EN SANTÉ"</strong>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="nav">
        <div class="container">
            <div class="nav-content">
                <a href="#mission">Notre Mission</a>
                <a href="#projet">Le Projet</a>
                <a href="#resultats">Résultats</a>
                <a href="#equipe">Notre Équipe</a>
                <a href="#contact">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2 class="fade-in">Améliorer la vie des seniors</h2>
            <p class="fade-in">L'Association GOLLUM NOEL œuvre pour l'intégration des personnes vivant avec un handicap moteur dans un programme de rééducation fonctionnelle soutenu par la kinésithérapie.</p>
            
            <div class="stats-grid">
                <div class="stat-card fade-in">
                    <div class="stat-number">438</div>
                    <div class="stat-label">Personnes enregistrées</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number">306</div>
                    <div class="stat-label">Patients traités</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number">589</div>
                    <div class="stat-label">Séances de kinésithérapie</div>
                </div>
                <div class="stat-card fade-in">
                    <div class="stat-number">100%</div>
                    <div class="stat-label">Taux de satisfaction</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mission Section -->
    <section id="mission" class="section">
        <div class="container">
            <h3 class="fade-in">Notre Mission</h3>
            <div class="mission-grid">
                <div class="mission-card fade-in">
                    <h4>Rééducation Fonctionnelle</h4>
                    <p>Nous nous engageons à intégrer les personnes vivant avec un handicap moteur dans un programme de rééducation fonctionnelle adapté et personnalisé.</p>
                </div>
                <div class="mission-card fade-in">
                    <h4>Kinésithérapie Spécialisée</h4>
                    <p>Notre équipe propose des soins de kinésithérapie ciblés pour améliorer la capacité physique et augmenter l'autonomie dans les activités quotidiennes.</p>
                </div>
                <div class="mission-card fade-in">
                    <h4>Accompagnement Holistique</h4>
                    <p>Nous offrons un accompagnement complet incluant l'éducation thérapeutique, les conseils d'économie articulaire et le soutien psychosocial.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projet Section -->
    <section id="projet" class="section section-alt">
        <div class="container">
            <h3 class="fade-in">Le Projet "Vieillir en Santé"</h3>
            <div class="results-content fade-in">
                <p style="font-size: 1.1rem; margin-bottom: 2rem; text-align: center;">
                    Motivé par la loi N° 83/13 du 21 juillet 1983 relative à la protection et la promotion de la personne handicapée, ce projet pilote s'est déroulé du <strong>26 novembre au 11 décembre 2024</strong> au Centre de Santé Intégré de Souari (CSIS).
                </p>
                
                <div class="results-highlight">
                    <h4>Un succès dépassant nos objectifs</h4>
                    <p>Objectif initial : 200 patients - Résultat : 306 patients traités avec 589 séances de kinésithérapie</p>
                </div>
                
                <div class="mission-grid">
                    <div class="mission-card">
                        <h4>Pathologies traitées</h4>
                        <ul style="list-style: none; padding: 0;">
                            <li>• Troubles de la marche</li>
                            <li>• Atrophies musculaires</li>
                            <li>• Troubles respiratoires</li>
                            <li>• Problèmes articulaires</li>
                            <li>• Séquelles d'AVC</li>
                        </ul>
                    </div>
                    <div class="mission-card">
                        <h4>Techniques utilisées</h4>
                        <ul style="list-style: none; padding: 0;">
                            <li>• Thermothérapie infrarouge</li>
                            <li>• Massothérapie au beurre de karité</li>
                            <li>• Renforcement musculaire</li>
                            <li>• École du dos</li>
                            <li>• Conseils d'économie articulaire</li>
                        </ul>
                    </div>
                    <div class="mission-card">
                        <h4>Population ciblée</h4>
                        <ul style="list-style: none; padding: 0;">
                            <li>• 132 patients hypertendus détectés</li>
                            <li>• 13 patients diabétiques</li>
                            <li>• Majorité âgée de 40-70 ans</li>
                            <li>• 70% de femmes</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Résultats Section -->
    <section id="resultats" class="section">
        <div class="container">
            <h3 class="fade-in">Résultats du Questionnaire</h3>
            <div class="results-content fade-in">
                <p style="text-align: center; margin-bottom: 2rem; font-size: 1.1rem;">
                    84 patients présents le dernier jour ont répondu à notre questionnaire de satisfaction
                </p>
                
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number">100%</div>
                        <div class="stat-label">Satisfaction des patients</div>
                        <p style="font-size: 0.9rem; margin-top: 0.5rem;">Tous les patients se déclarent satisfaits de la prise en charge</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">100%</div>
                        <div class="stat-label">Volonté de renouvellement</div>
                        <p style="font-size: 0.9rem; margin-top: 0.5rem;">Tous souhaitent revivre cette expérience</p>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">58%</div>
                        <div class="stat-label">Contribution financière</div>
                        <p style="font-size: 0.9rem; margin-top: 0.5rem;">49/84 patients prêts à payer 1000-2000 FCFA/séance</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Équipe Section -->
    <section id="equipe" class="section section-alt">
        <div class="container">
            <h3 class="fade-in">Notre Équipe</h3>
            <div class="team-grid">
                <div class="team-card fade-in">
                    <div class="team-role">Président</div>
                    <h4>PEDENE DERBOUNE NOEL</h4>
                    <p>Kinésithérapeute et coordinateur du projet</p>
                </div>
                <div class="team-card fade-in">
                    <div class="team-role">Équipe Médicale</div>
                    <h4>Professionnels de Santé</h4>
                    <p>6 médecins généralistes, 1 urgentiste, 1 rhumatologue, 2 étudiants en médecine</p>
                </div>
                <div class="team-card fade-in">
                    <div class="team-role">Kinésithérapeutes</div>
                    <h4>Spécialistes Rééducation</h4>
                    <p>2 kinésithérapeutes diplômés et 2 assistants kinésithérapeutes</p>
                </div>
                <div class="team-card fade-in">
                    <div class="team-role">Support</div>
                    <h4>Personnel d'Appui</h4>
                    <p>Assistants d'accueil, secrétaire, trésorier et équipe logistique</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <h3 class="fade-in">Nous Contacter</h3>
            <div class="contact-grid">
                <div class="contact-card fade-in">
                    <h4 style="color: var(--primary-green); margin-bottom: 1.5rem;">Informations Légales</h4>
                    <div class="contact-item">
                        <svg viewBox="0 0 24 24"><path d="M9 11H7v2h2v-2zm4 0h-2v2h2v-2zm4 0h-2v2h2v-2zm2-7h-1V2h-2v2H8V2H6v2H5c-1.1 0-1.99.9-1.99 2L3 20c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 16H5V9h14v11z"/></svg>
                        <span>Créée le 9 février 2024</span>
                    </div>
                    <div class="contact-item">
                        <svg viewBox="0 0 24 24"><path d="M14,2H6A2,2 0 0,0 4,4V20A2,2 0 0,0 6,22H18A2,2 0 0,0 20,20V8L14,2M18,20H6V4H13V9H18V20Z"/></svg>
                        <span>Récépissé N°027/RDA/D04.01/SAAJP du 11 MARS 2024</span>
                    </div>
                </div>
                
                <div class="contact-card fade-in">
                    <h4 style="color: var(--primary-green); margin-bottom: 1.5rem;">Localisation</h4>
                    <div class="contact-item">
                        <svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
                        <span>Garoua, Région du Nord, Cameroun</span>
                    </div>
                    <div class="contact-item">
                        <svg viewBox="0 0 24 24"><path d="M12,11.5A2.5,2.5 0 0,1 9.5,9A2.5,2.5 0 0,1 12,6.5A2.5,2.5 0 0,1 14.5,9A2.5,2.5 0 0,1 12,11.5M12,2A7,7 0 0,0 5,9C5,14.25 12,22 12,22S19,14.25 19,9A7,7 0 0,0 12,2Z"/></svg>
                        <span>Centre de Santé Intégré de Souari</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>Notre Mission</h4>
                    <p>"Améliorer significativement les conditions de vie des populations seniors par la kinésithérapie"</p>
                </div>
                <div class="footer-section">
                    <h4>Nos Valeurs</h4>
                    <p>Solidarité collective, expertise médicale, accompagnement humain et dignité des personnes âgées</p>
                </div>
                <div class="footer-section">
                    <h4>Nos Partenaires</h4>
                    <p>Ministère de la Santé, CSIS, Autorités locales et équipe médicale bénévole</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Association GOLLUM NOEL. Tous droits réservés.</p>
                <p>Projet "Vieillir en Santé" - Garoua, Cameroun</p>
            </div>
        </div>
    </footer>

    <script>
        // Animations au scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Smooth scroll pour la navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Animation des statistiques au chargement
        function animateNumbers() {
            const statNumbers = document.querySelectorAll('.stat-number');
            statNumbers.forEach(stat => {
                const target = parseInt(stat.textContent);
                if (isNaN(target)) return;
                
                let current = 0;
                const increment = target / 50;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        current = target;
                        clearInterval(timer);
                    }
                    stat.textContent = Math.floor(current) + (stat.textContent.includes('%') ? '%' : '');
                }, 30);
            });
        }

        // Déclencher l'animation des chiffres quand la section est visible
        const statsSection = document.querySelector('.stats-grid');
        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateNumbers();
                    statsObserver.unobserve(entry.target);
                }
            });
        });

        if (statsSection) {
            statsObserver.observe(statsSection);
        }
    </script>
</body>
</html>
