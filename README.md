<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio BTS Communication 2025/2026</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700;900&family=Playfair+Display:wght@400;700;900&display=swap');
        
        :root {
            --primary: #FF4D80;
            --secondary: #00C2CB;
            --dark: #1A1A2E;
            --light: #F5F5F5;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--light);
            color: var(--dark);
            overflow-x: hidden;
        }
        
        .title-font {
            font-family: 'Playfair Display', serif;
        }
        
        .gradient-text {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
        }
        
        .card-hover {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .menu-item {
            position: relative;
        }
        
        .menu-item::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--primary);
            transition: width 0.3s ease;
        }
        
        .menu-item:hover::after {
            width: 100%;
        }
        
        .hero-pattern {
            background-image: radial-gradient(circle at 25% 25%, rgba(255, 77, 128, 0.1) 0%, rgba(0, 194, 203, 0.1) 100%);
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            left: -10px;
            top: 0;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            width: 2px;
            height: 100%;
            left: 0;
            top: 0;
            background: linear-gradient(to bottom, var(--primary), var(--secondary));
        }
        
        .project-card {
            perspective: 1000px;
        }
        
        .project-inner {
            transition: transform 0.6s;
            transform-style: preserve-3d;
        }
        
        .project-card:hover .project-inner {
            transform: rotateY(180deg);
        }
        
        .project-front, .project-back {
            backface-visibility: hidden;
        }
        
        .project-back {
            transform: rotateY(180deg);
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        .delay-1 {
            animation-delay: 0.5s;
        }
        
        .delay-2 {
            animation-delay: 1s;
        }
    </style>
</head>
<body class="min-h-screen">
    <!-- Navigation -->
    <nav class="fixed w-full z-50 bg-white bg-opacity-90 backdrop-filter backdrop-blur-lg shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <a href="#" class="text-xl font-bold title-font gradient-text">PORTFOLIO<span class="text-indigo-600">2026</span></a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="menu-item text-gray-900 px-3 py-2 text-sm font-medium">Accueil</a>
                    <a href="#story" class="menu-item text-gray-900 px-3 py-2 text-sm font-medium">Mon Parcours</a>
                    <a href="#works" class="menu-item text-gray-900 px-3 py-2 text-sm font-medium">Réalisations</a>
                    <a href="#projects" class="menu-item text-gray-900 px-3 py-2 text-sm font-medium">Projets</a>
                    <a href="#contact" class="gradient-bg text-white px-4 py-2 rounded-full text-sm font-medium shadow-lg hover:shadow-xl transition duration-300">Contact</a>
                </div>
                <div class="md:hidden flex items-center">
                    <button id="menu-btn" class="text-gray-900">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white py-2 px-4 shadow-lg">
            <a href="#home" class="block px-3 py-2 text-base font-medium text-gray-900">Accueil</a>
            <a href="#story" class="block px-3 py-2 text-base font-medium text-gray-900">Mon Parcours</a>
            <a href="#works" class="block px-3 py-2 text-base font-medium text-gray-900">Réalisations</a>
            <a href="#projects" class="block px-3 py-2 text-base font-medium text-gray-900">Projets</a>
            <a href="#contact" class="block gradient-bg text-white px-3 py-2 rounded-full text-center font-medium mt-2">Contact</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-pattern pt-32 pb-20 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-6xl font-bold title-font mb-6">
                        <span class="gradient-text">Je m'appelle</span><br>
                        <span class="text-indigo-900">[Prénom Nom]</span>
                    </h1>
                    <p class="text-lg text-gray-700 mb-8 max-w-lg">
                        Étudiant en BTS Communication 2025/2026, passionné par la création visuelle, le storytelling et les stratégies de communication innovantes.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#story" class="gradient-bg text-white px-6 py-3 rounded-full font-medium shadow-lg hover:shadow-xl transition duration-300">
                            Découvrir mon parcours
                        </a>
                        <a href="#works" class="border-2 border-indigo-900 text-indigo-900 px-6 py-3 rounded-full font-medium hover:bg-indigo-900 hover:text-white transition duration-300">
                            Voir mes réalisations
                        </a>
                    </div>
                </div>
                <div class="md:w-1/2 relative">
                    <div class="relative w-full max-w-md mx-auto">
                        <div class="absolute -top-10 -left-10 w-32 h-32 bg-pink-200 rounded-full opacity-70 filter blur-xl"></div>
                        <div class="absolute -bottom-10 -right-10 w-32 h-32 bg-teal-200 rounded-full opacity-70 filter blur-xl"></div>
                        <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=774&q=80" alt="Portrait étudiant" class="relative z-10 w-full h-auto rounded-2xl shadow-2xl border-8 border-white floating">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Décoration" class="absolute -right-20 -bottom-20 w-40 h-40 rounded-full shadow-xl border-4 border-white floating delay-1">
                        <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1064&q=80" alt="Décoration" class="absolute -left-20 -top-20 w-32 h-32 rounded-2xl shadow-xl border-4 border-white floating delay-2">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Storytelling Section -->
    <section id="story" class="py-20 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-5xl font-bold title-font mb-4">
                    <span class="gradient-text">Mon Parcours</span> 
                    <span class="text-indigo-900">et Mon Histoire</span>
                </h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Découvrez mon évolution, mes passions et ce qui m'a conduit à choisir la communication comme voie professionnelle.
                </p>
            </div>
            
            <div class="relative pl-8 md:pl-16 mt-10">
                <div class="timeline absolute left-0 top-0 h-full"></div>
                
                <div class="mb-12 relative timeline-item">
                    <div class="bg-gray-50 p-6 rounded-xl shadow-sm hover:shadow-md transition duration-300">
                        <div class="flex items-center mb-4">
                            <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center text-white font-bold text-xl mr-4">1</div>
                            <h3 class="text-xl font-bold title-font text-indigo-900">Mes débuts dans la création</h3>
                        </div>
                        <p class="text-gray-700">
                            Dès mon plus jeune âge, j'ai été fasciné par le pouvoir des images et des mots. À 15 ans, je créais déjà des montages vidéo pour mes amis et des designs pour les réseaux sociaux. Cette passion m'a naturellement conduit vers des études artistiques.
                        </p>
                    </div>
                </div>
                
                <div class="mb-12 relative timeline-item">
                    <div class="bg-gray-50 p-6 rounded-xl shadow-sm hover:shadow-md transition duration-300">
                        <div class="flex items-center mb-4">
                            <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center text-white font-bold text-xl mr-4">2</div>
                            <h3 class="text-xl font-bold title-font text-indigo-900">Bac STMG option Marketing</h3>
                        </div>
                        <p class="text-gray-700">
                            Mon baccalauréat STMG spécialité Marketing a été une révélation. J'ai découvert les stratégies de communication, l'étude des consommateurs et la création de campagnes. Ce diplôme a confirmé mon envie de travailler dans ce domaine dynamique et créatif.
                        </p>
                    </div>
                </div>
                
                <div class="mb-12 relative timeline-item">
                    <div class="bg-gray-50 p-6 rounded-xl shadow-sm hover:shadow-md transition duration-300">
                        <div class="flex items-center mb-4">
                            <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center text-white font-bold text-xl mr-4">3</div>
                            <h3 class="text-xl font-bold title-font text-indigo-900">BTS Communication</h3>
                        </div>
                        <p class="text-gray-700">
                            Actuellement en BTS Communication, j'acquiers des compétences techniques et stratégiques complètes. De la création graphique à la planification média, en passant par la rédaction publicitaire, je me forme à tous les aspects du métier pour devenir un professionnel polyvalent.
                        </p>
                    </div>
                </div>
                
                <div class="relative timeline-item">
                    <div class="bg-gray-50 p-6 rounded-xl shadow-sm hover:shadow-md transition duration-300">
                        <div class="flex items-center mb-4">
                            <div class="w-12 h-12 gradient-bg rounded-full flex items-center justify-center text-white font-bold text-xl mr-4">4</div>
                            <h3 class="text-xl font-bold title-font text-indigo-900">Mes aspirations futures</h3>
                        </div>
                        <p class="text-gray-700">
                            À l'issue de mon BTS, je souhaite poursuivre en licence professionnelle en stratégie digitale ou en création publicitaire. Mon objectif à long terme est de travailler en agence comme directeur artistique ou concepteur-rédacteur, pour créer des campagnes marquantes et innovantes.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="py-16 px-4 sm:px-6 lg:px-8 gradient-bg text-white">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-5xl font-bold title-font mb-4">
                    Mes <span class="text-indigo-100">Compétences</span>
                </h2>
                <p class="text-lg text-indigo-100 max-w-3xl mx-auto">
                    Un panel de savoir-faire techniques et créatifs acquis au cours de ma formation
                </p>
            </div>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
                <div class="bg-white bg-opacity-10 p-6 rounded-xl backdrop-filter backdrop-blur-lg border border-white border-opacity-20 card-hover">
                    <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-pen-fancy text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-center mb-2">Création Graphique</h3>
                    <p class="text-sm text-indigo-100 text-center">Photoshop, Illustrator, InDesign, Canva</p>
                </div>
                
                <div class="bg-white bg-opacity-10 p-6 rounded-xl backdrop-filter backdrop-blur-lg border border-white border-opacity-20 card-hover">
                    <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-code text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-center mb-2">Web Design</h3>
                    <p class="text-sm text-indigo-100 text-center">HTML/CSS, WordPress, Figma, UX/UI</p>
                </div>
                
                <div class="bg-white bg-opacity-10 p-6 rounded-xl backdrop-filter backdrop-blur-lg border border-white border-opacity-20 card-hover">
                    <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-video text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-center mb-2">Audiovisuel</h3>
                    <p class="text-sm text-indigo-100 text-center">Premiere Pro, After Effects, DaVinci Resolve</p>
                </div>
                
                <div class="bg-white bg-opacity-10 p-6 rounded-xl backdrop-filter backdrop-blur-lg border border-white border-opacity-20 card-hover">
                    <div class="w-16 h-16 bg-white bg-opacity-20 rounded-full flex items-center justify-center mb-4 mx-auto">
                        <i class="fas fa-chart-line text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold text-center mb-2">Stratégie</h3>
                    <p class="text-sm text-indigo-100 text-center">Plan de com, Benchmark, Analytics, SEO</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Works Section -->
    <section id="works" class="py-20 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-5xl font-bold title-font mb-4">
                    <span class="gradient-text">Mes Réalisations</span>
                </h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Découvrez une sélection de mes travaux classés par catégories
                </p>
            </div>
            
            <div class="flex flex-wrap justify-center mb-12">
                <button class="filter-btn active px-4 py-2 m-1 rounded-full gradient-bg text-white font-medium" data-filter="all">Tous</button>
                <button class="filter-btn px-4 py-2 m-1 rounded-full border border-indigo-900 text-indigo-900 font-medium hover:bg-indigo-900 hover:text-white transition duration-300" data-filter="print">Print</button>
                <button class="filter-btn px-4 py-2 m-1 rounded-full border border-indigo-900 text-indigo-900 font-medium hover:bg-indigo-900 hover:text-white transition duration-300" data-filter="digital">Digital</button>
                <button class="filter-btn px-4 py-2 m-1 rounded-full border border-indigo-900 text-indigo-900 font-medium hover:bg-indigo-900 hover:text-white transition duration-300" data-filter="video">Vidéo</button>
                <button class="filter-btn px-4 py-2 m-1 rounded-full border border-indigo-900 text-indigo-900 font-medium hover:bg-indigo-900 hover:text-white transition duration-300" data-filter="photo">Photo</button>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Print Item -->
                <div class="work-item print card-hover">
                    <div class="bg-gray-100 rounded-xl overflow-hidden shadow-md">
                        <img src="https://images.unsplash.com/photo-1542621334-a254cf47733d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Affiche publicitaire" class="w-full h-64 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Affiche Événementielle</h3>
                            <p class="text-gray-700 mb-4">Création d'une affiche pour un festival de musique local avec contraintes techniques spécifiques.</p>
                            <div class="flex justify-between items-center">
                                <span class="text-sm font-medium px-3 py-1 rounded-full bg-indigo-100 text-indigo-900">Print</span>
                                <a href="#" class="text-indigo-900 font-medium hover:text-indigo-600 transition duration-300">Voir plus <i class="fas fa-arrow-right ml-1"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Digital Item -->
                <div class="work-item digital card-hover">
                    <div class="bg-gray-100 rounded-xl overflow-hidden shadow-md">
                        <img src="https://images.unsplash.com/photo-1559028012-481c04fa702d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1736&q=80" alt="Site web" class="w-full h-64 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Site Vitrine</h3>
                            <p class="text-gray-700 mb-4">Conception et développement d'un site web responsive pour un artisan local.</p>
                            <div class="flex justify-between items-center">
                                <span class="text-sm font-medium px-3 py-1 rounded-full bg-teal-100 text-teal-900">Digital</span>
                                <a href="#" class="text-indigo-900 font-medium hover:text-indigo-600 transition duration-300">Voir plus <i class="fas fa-arrow-right ml-1"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Video Item -->
                <div class="work-item video card-hover">
                    <div class="bg-gray-100 rounded-xl overflow-hidden shadow-md">
                        <img src="https://images.unsplash.com/photo-1551818255-e6e10975bc17?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1732&q=80" alt="Spot publicitaire" class="w-full h-64 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Spot Publicitaire</h3>
                            <p class="text-gray-700 mb-4">Réalisation d'un spot de 30 secondes pour une marque de vêtements éco-responsables.</p>
                            <div class="flex justify-between items-center">
                                <span class="text-sm font-medium px-3 py-1 rounded-full bg-pink-100 text-pink-900">Vidéo</span>
                                <a href="#" class="text-indigo-900 font-medium hover:text-indigo-600 transition duration-300">Voir plus <i class="fas fa-arrow-right ml-1"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Photo Item -->
                <div class="work-item photo card-hover">
                    <div class="bg-gray-100 rounded-xl overflow-hidden shadow-md">
                        <img src="https://images.unsplash.com/photo-1522542550221-31fd19575a2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Série photo" class="w-full h-64 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Série Photographique</h3>
                            <p class="text-gray-700 mb-4">Reportage sur le thème "L'art dans la rue" avec post-production Lightroom.</p>
                            <div class="flex justify-between items-center">
                                <span class="text-sm font-medium px-3 py-1 rounded-full bg-purple-100 text-purple-900">Photo</span>
                                <a href="#" class="text-indigo-900 font-medium hover:text-indigo-600 transition duration-300">Voir plus <i class="fas fa-arrow-right ml-1"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Print Item -->
                <div class="work-item print card-hover">
                    <div class="bg-gray-100 rounded-xl overflow-hidden shadow-md">
                        <img src="https://images.unsplash.com/photo-1607748859297-3bc329e5a8d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Identité visuelle" class="w-full h-64 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Identité Visuelle</h3>
                            <p class="text-gray-700 mb-4">Création d'une charte graphique complète pour une startup tech (logo, couleurs, typo).</p>
                            <div class="flex justify-between items-center">
                                <span class="text-sm font-medium px-3 py-1 rounded-full bg-indigo-100 text-indigo-900">Print</span>
                                <a href="#" class="text-indigo-900 font-medium hover:text-indigo-600 transition duration-300">Voir plus <i class="fas fa-arrow-right ml-1"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Digital Item -->
                <div class="work-item digital card-hover">
                    <div class="bg-gray-100 rounded-xl overflow-hidden shadow-md">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Réseaux sociaux" class="w-full h-64 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Stratégie Social Media</h3>
                            <p class="text-gray-700 mb-4">Création de contenu et planning éditorial pour une marque de cosmétiques sur Instagram.</p>
                            <div class="flex justify-between items-center">
                                <span class="text-sm font-medium px-3 py-1 rounded-full bg-teal-100 text-teal-900">Digital</span>
                                <a href="#" class="text-indigo-900 font-medium hover:text-indigo-600 transition duration-300">Voir plus <i class="fas fa-arrow-right ml-1"></i></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="inline-block gradient-bg text-white px-8 py-3 rounded-full font-medium shadow-lg hover:shadow-xl transition duration-300">
                    Voir toutes mes réalisations
                </a>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 px-4 sm:px-6 lg:px-8 bg-gray-50">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-5xl font-bold title-font mb-4">
                    <span class="text-indigo-900">Mes Projets</span> 
                    <span class="gradient-text">Phares</span>
                </h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Trois situations de projet mettant en œuvre des compétences variées et complémentaires
                </p>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card">
                    <div class="project-inner h-full">
                        <div class="project-front h-full bg-white rounded-xl shadow-md overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1738&q=80" alt="Projet 1" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Campagne 360°</h3>
                                <p class="text-gray-700 mb-4">Stratégie de communication intégrée pour le lancement d'un produit.</p>
                                <div class="flex flex-wrap gap-2 mb-4">
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-indigo-100 text-indigo-900">Stratégie</span>
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-pink-100 text-pink-900">Création</span>
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-teal-100 text-teal-900">Digital</span>
                                </div>
                                <button class="view-details-btn w-full gradient-bg text-white py-2 rounded-full font-medium">
                                    Voir les détails
                                </button>
                            </div>
                        </div>
                        <div class="project-back absolute inset-0 bg-indigo-900 rounded-xl shadow-md p-6 flex flex-col justify-center">
                            <h3 class="text-xl font-bold title-font text-white mb-4">Compétences Mobilisées</h3>
                            <ul class="text-gray-200 mb-6 space-y-2">
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Analyse du brief client</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Benchmark concurrentiel</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Création d'un plan média</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Conception d'éléments graphiques</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Rédaction de messages clés</li>
                            </ul>
                            <button class="close-details-btn w-full bg-white text-indigo-900 py-2 rounded-full font-medium mt-auto">
                                Retour
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card">
                    <div class="project-inner h-full">
                        <div class="project-front h-full bg-white rounded-xl shadow-md overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Projet 2" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Refonte Digitale</h3>
                                <p class="text-gray-700 mb-4">Modernisation de l'identité en ligne d'une institution culturelle.</p>
                                <div class="flex flex-wrap gap-2 mb-4">
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-purple-100 text-purple-900">UX/UI</span>
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-teal-100 text-teal-900">Web</span>
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-yellow-100 text-yellow-900">SEO</span>
                                </div>
                                <button class="view-details-btn w-full gradient-bg text-white py-2 rounded-full font-medium">
                                    Voir les détails
                                </button>
                            </div>
                        </div>
                        <div class="project-back absolute inset-0 bg-indigo-900 rounded-xl shadow-md p-6 flex flex-col justify-center">
                            <h3 class="text-xl font-bold title-font text-white mb-4">Compétences Mobilisées</h3>
                            <ul class="text-gray-200 mb-6 space-y-2">
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Audit de l'existant</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Personas et parcours utilisateur</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Maquettage Figma</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Intégration WordPress</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Stratégie de contenu</li>
                            </ul>
                            <button class="close-details-btn w-full bg-white text-indigo-900 py-2 rounded-full font-medium mt-auto">
                                Retour
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card">
                    <div class="project-inner h-full">
                        <div class="project-front h-full bg-white rounded-xl shadow-md overflow-hidden">
                            <img src="https://images.unsplash.com/photo-1522542550221-31fd19575a2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" alt="Projet 3" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <h3 class="text-xl font-bold title-font text-indigo-900 mb-2">Événementiel Immersif</h3>
                                <p class="text-gray-700 mb-4">Organisation d'une expérience client innovante pour une marque.</p>
                                <div class="flex flex-wrap gap-2 mb-4">
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-pink-100 text-pink-900">Événementiel</span>
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-green-100 text-green-900">Scénographie</span>
                                    <span class="text-xs font-medium px-2 py-1 rounded-full bg-blue-100 text-blue-900">RP</span>
                                </div>
                                <button class="view-details-btn w-full gradient-bg text-white py-2 rounded-full font-medium">
                                    Voir les détails
                                </button>
                            </div>
                        </div>
                        <div class="project-back absolute inset-0 bg-indigo-900 rounded-xl shadow-md p-6 flex flex-col justify-center">
                            <h3 class="text-xl font-bold title-font text-white mb-4">Compétences Mobilisées</h3>
                            <ul class="text-gray-200 mb-6 space-y-2">
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Conception du concept créatif</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Scénarisation de l'expérience</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Gestion des prestataires</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Relations presse</li>
                                <li class="flex items-center"><i class="fas fa-check-circle text-pink-400 mr-2"></i> Reporting et analyse ROI</li>
                            </ul>
                            <button class="close-details-btn w-full bg-white text-indigo-900 py-2 rounded-full font-medium mt-auto">
                                Retour
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-4 sm:px-6 lg:px-8 bg-white">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-5xl font-bold title-font mb-4">
                    <span class="gradient-text">Restons</span> 
                    <span class="text-indigo-900">en Contact</span>
                </h2>
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">
                    Vous souhaitez en savoir plus sur mon travail ou discuter d'un projet ? N'hésitez pas à me contacter !
                </p>
            </div>
            
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-10 md:mb-0 md:pr-10">
                    <div class="bg-gray-50 p-8 rounded-xl shadow-sm">
                        <h3 class="text-xl font-bold title-font text-indigo-900 mb-6">Mes Coordonnées</h3>
                        
                        <div class="space-y-6">
                            <div class="flex items-start">
                                <div class="w-10 h-10 gradient-bg rounded-full flex items-center justify-center text-white mr-4 flex-shrink-0">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium text-gray-900">Email</h4>
                                    <p class="text-gray-600">prenom.nom@etudiant.fr</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="w-10 h-10 gradient-bg rounded-full flex items-center justify-center text-white mr-4 flex-shrink-0">
                                    <i class="fas fa-phone-alt"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium text-gray-900">Téléphone</h4>
                                    <p class="text-gray-600">+33 6 12 34 56 78</p>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="w-10 h-10 gradient-bg rounded-full flex items-center justify-center text-white mr-4 flex-shrink-0">
                                    <i class="fas fa-map-marker-alt"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium text-gray-900">Adresse</h4>
                                    <p class="text-gray-600">École de Communication<br>123 Rue des Étudiants, 75000 Paris</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="mt-8">
                            <h4 class="font-medium text-gray-900 mb-4">Suivez-moi</h4>
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center text-gray-700 hover:bg-indigo-900 hover:text-white transition duration-300">
                                    <i class="fab fa-behance"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center text-gray-700 hover:bg-indigo-900 hover:text-white transition duration-300">
                                    <i class="fab fa-linkedin-in"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center text-gray-700 hover:bg-indigo-900 hover:text-white transition duration-300">
                                    <i class="fab fa-instagram"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full border border-gray-300 flex items-center justify-center text-gray-700 hover:bg-indigo-900 hover:text-white transition duration-300">
                                    <i class="fab fa-dribbble"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="md:w-1/2">
                    <form class="bg-gray-50 p-8 rounded-xl shadow-sm">
                        <h3 class="text-xl font-bold title-font text-indigo-900 mb-6">Envoyez-moi un message</h3>
                        
                        <div class="grid grid-cols-1 gap-6">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Nom complet</label>
                                <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500">
                            </div>
                            
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email</label>
                                <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500">
                            </div>
                            
                            <div>
                                <label for="subject" class="block text-sm font-medium text-gray-700 mb-1">Sujet</label>
                                <input type="text" id="subject" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500">
                            </div>
                            
                            <div>
                                <label for="message" class="block text-sm font-medium text-gray-700 mb-1">Message</label>
                                <textarea id="message" rows="4" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-indigo-500"></textarea>
                            </div>
                            
                            <div>
                                <button type="submit" class="w-full gradient-bg text-white px-6 py-3 rounded-lg font-medium shadow-lg hover:shadow-xl transition duration-300">
                                    Envoyer le message
                                </button>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-indigo-900 text-white py-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <a href="#" class="text-xl font-bold title-font text-white">PORTFOLIO<span class="text-pink-300">2026</span></a>
                    <p class="mt-2 text-indigo-200">Portfolio BTS Communication 2025/2026</p>
                </div>
                
                <div class="flex flex-col items-center md:items-end">
                    <div class="flex space-x-6 mb-4">
                        <a href="#" class="text-indigo-200 hover:text-white transition duration-300">
                            <i class="fab fa-behance text-xl"></i>
                        </a>
                        <a href="#" class="text-indigo-200 hover:text-white transition duration-300">
                            <i class="fab fa-linkedin-in text-xl"></i>
                        </a>
                        <a href="#" class="text-indigo-200 hover:text-white transition duration-300">
                            <i class="fab fa-instagram text-xl"></i>
                        </a>
                        <a href="#" class="text-indigo-200 hover:text-white transition duration-300">
                            <i class="fab fa-dribbble text-xl"></i>
                        </a>
                    </div>
                    <p class="text-sm text-indigo-300">© 2025-2026 Tous droits réservés</p>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById('menu-btn').addEventListener('click', function() {
            document.getElementById('mobile-menu').classList.toggle('hidden');
        });

        // Filter works
        const filterBtns = document.querySelectorAll('.filter-btn');
        const workItems = document.querySelectorAll('.work-item');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                // Remove active class from all buttons
                filterBtns.forEach(b => b.classList.remove('active', 'gradient-bg', 'text-white'));
                filterBtns.forEach(b => b.classList.add('border', 'border-indigo-900', 'text-indigo-900'));
                
                // Add active class to clicked button
                this.classList.add('active', 'gradient-bg', 'text-white');
                this.classList.remove('border', 'border-indigo-900', 'text-indigo-900');
                
                const filter = this.getAttribute('data-filter');
                
                workItems.forEach(item => {
                    if (filter === 'all' || item.classList.contains(filter)) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });

        // Project cards flip
        const projectCards = document.querySelectorAll('.project-card');
        
        projectCards.forEach(card => {
            const viewBtn = card.querySelector('.view-details-btn');
            const closeBtn = card.querySelector('.close-details-btn');
            const inner = card.querySelector('.project-inner');
            
            viewBtn.addEventListener('click', function(e) {
                e.stopPropagation();
                inner.style.transform = 'rotateY(180deg)';
            });
            
            closeBtn.addEventListener('click', function(e) {
                e.stopPropagation();
                inner.style.transform = 'rotateY(0deg)';
            });
        });

        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Close mobile menu if open
                document.getElementById('mobile-menu').classList.add('hidden');
            });
        });
    </script>
</body>
</html>
