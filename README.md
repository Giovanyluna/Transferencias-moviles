<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ana González | SPA Y MAS - Masajes y Lencería Premium</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Fuentes y variables de color premium */
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Inter:wght@300;400;500;600;700&display=swap');
        
        :root {
            --primary-rose: #E8B4CB;
            --deep-rose: #B85450;
            --accent-gold: #D4AF37;
            --cream-white: #FDF8F5;
            --pearl-gray: #F7F3F0;
            --charcoal: #2C2C2C;
            --soft-shadow: rgba(184, 84, 80, 0.15);
            --gradient-primary: linear-gradient(135deg, #E8B4CB 0%, #B85450 100%);
            --gradient-secondary: linear-gradient(135deg, #D4AF37 0%, #F4E4BC 100%);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--cream-white);
            color: var(--charcoal);
            overflow-x: hidden;
            scroll-behavior: smooth;
        }
        
        /* Header con diseño premium */
        header {
            background: linear-gradient(rgba(253, 248, 245, 0.95), rgba(247, 243, 240, 0.95)), 
                        url('https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2340&q=80') center/cover;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            position: relative;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at center, transparent 0%, rgba(232, 180, 203, 0.1) 100%);
            pointer-events: none;
        }
        
        .logo {
            margin-bottom: 2rem;
            animation: luxuryFadeIn 2s ease-out;
            position: relative;
            z-index: 2;
        }
        
        .logo h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            font-weight: 600;
            background: var(--gradient-primary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 4px 8px var(--soft-shadow);
            letter-spacing: -1px;
        }
        
        .logo p {
            font-family: 'Inter', sans-serif;
            font-weight: 300;
            font-size: 1.2rem;
            color: var(--deep-rose);
            margin-top: 0.5rem;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        
        .slogan {
            font-family: 'Playfair Display', serif;
            font-style: italic;
            font-size: 1.8rem;
            color: var(--deep-rose);
            margin-bottom: 3rem;
            animation: luxurySlideUp 2.5s ease-out;
            position: relative;
            z-index: 2;
        }
        
        .cta-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            justify-content: center;
            animation: luxurySlideUp 3s ease-out;
            position: relative;
            z-index: 2;
        }
        
        .btn-luxury {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: var(--gradient-primary);
            color: white;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 8px 25px var(--soft-shadow);
            border: 2px solid transparent;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .btn-luxury:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 40px rgba(184, 84, 80, 0.3);
            background: var(--gradient-secondary);
            color: var(--charcoal);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid var(--deep-rose);
            color: var(--deep-rose);
        }
        
        .btn-outline:hover {
            background: var(--deep-rose);
            color: white;
        }
        
        /* Sección de servicios premium */
        .services {
            padding: 8rem 2rem;
            background: linear-gradient(180deg, var(--cream-white) 0%, var(--pearl-gray) 100%);
            position: relative;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 600;
            text-align: center;
            margin-bottom: 1rem;
            background: var(--gradient-primary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .section-subtitle {
            text-align: center;
            font-size: 1.1rem;
            color: var(--deep-rose);
            margin-bottom: 4rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 2.5rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .service-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(44, 44, 44, 0.1);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            opacity: 0;
            transform: translateY(30px);
            position: relative;
        }
        
        .service-card.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .service-card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 25px 60px rgba(44, 44, 44, 0.15);
        }
        
        .service-img {
            height: 250px;
            overflow: hidden;
            position: relative;
        }
        
        .service-img::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(232, 180, 203, 0.2) 0%, rgba(184, 84, 80, 0.2) 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: 1;
        }
        
        .service-card:hover .service-img::before {
            opacity: 1;
        }
        
        .service-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .service-card:hover .service-img img {
            transform: scale(1.1);
        }
        
        .service-info {
            padding: 2rem;
        }
        
        .service-header {
            margin-bottom: 1rem;
        }
        
        .service-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--deep-rose);
            line-height: 1.2;
        }
        
        .service-description {
            color: var(--charcoal);
            line-height: 1.6;
            margin-bottom: 1.5rem;
            font-size: 0.95rem;
        }
        
        .service-details {
            display: flex;
            justify-content: center;
        }
        
        .btn-service {
            background: var(--gradient-primary);
            color: white;
            padding: 12px 25px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .btn-service:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px var(--soft-shadow);
        }
        
        /* Sección de productos premium */
        .products {
            padding: 8rem 2rem;
            background: linear-gradient(135deg, var(--primary-rose) 0%, var(--cream-white) 50%, var(--pearl-gray) 100%);
            position: relative;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2.5rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(44, 44, 44, 0.1);
            transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            opacity: 0;
            transform: translateY(30px);
            position: relative;
        }
        
        .product-card.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .product-card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 25px 60px rgba(44, 44, 44, 0.15);
        }
        
        .product-img {
            height: 300px;
            overflow: hidden;
            position: relative;
        }
        
        .product-img::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(232, 180, 203, 0.2) 0%, rgba(184, 84, 80, 0.2) 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: 1;
        }
        
        .product-card:hover .product-img::before {
            opacity: 1;
        }
        
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 2rem;
            text-align: center;
        }
        
        .product-header {
            margin-bottom: 1rem;
        }
        
        .product-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            font-weight: 600;
            color: var(--deep-rose);
            line-height: 1.2;
            margin-bottom: 0.5rem;
        }
        
        .product-price {
            font-family: 'Inter', sans-serif;
            font-size: 1.3rem;
            color: var(--charcoal);
            font-weight: 600;
            margin-bottom: 1rem;
        }
        
        .product-description {
            color: var(--charcoal);
            line-height: 1.6;
            margin-bottom: 1.5rem;
            font-size: 0.95rem;
        }
        
        .product-details {
            display: flex;
            justify-content: center;
            gap: 1rem;
        }
        
        .purchase-methods {
            margin-top: 4rem;
            text-align: center;
        }
        
        .methods-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            max-width: 1000px;
            margin: 2rem auto 0;
        }
        
        .method-card {
            background: white;
            padding: 1.5rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(44, 44, 44, 0.1);
            transition: all 0.3s ease;
        }
        
        .method-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(44, 44, 44, 0.15);
        }
        
        .method-icon {
            font-size: 2rem;
            color: var(--deep-rose);
            margin-bottom: 1rem;
        }
        
        /* Sección de contacto premium */
        .contact {
            padding: 6rem 2rem;
            background: var(--charcoal);
            color: white;
            text-align: center;
        }
        
        .contact .section-title {
            color: white;
            background: var(--gradient-secondary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 900px;
            margin: 3rem auto 0;
        }
        
        .contact-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }
        
        .contact-card:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-5px);
        }
        
        .contact-icon {
            font-size: 2.5rem;
            color: var(--accent-gold);
            margin-bottom: 1rem;
        }
        
        /* Footer premium */
        footer {
            background: linear-gradient(135deg, var(--deep-rose) 0%, var(--charcoal) 100%);
            color: white;
            padding: 4rem 2rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://www.transparenttextures.com/patterns/black-linen.png');
            opacity: 0.1;
            pointer-events: none;
        }
        
        .footer-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }
        
        .footer-logo {
            margin-bottom: 2rem;
        }
        
        .footer-logo h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            margin-bottom: 0.5rem;
            background: var(--gradient-secondary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .footer-logo p {
            opacity: 0.8;
            font-size: 0.9rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 2rem 0;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            font-size: 1.2rem;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background: var(--accent-gold);
            transform: translateY(-3px) scale(1.1);
            color: var(--charcoal);
        }
        
        .business-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
            margin: 2rem 0;
        }
        
        .info-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 1.5rem;
            border-radius: 15px;
            min-width: 250px;
            backdrop-filter: blur(10px);
        }
        
        .info-card h4 {
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: var(--accent-gold);
        }
        
        .copyright {
            margin-top: 2rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }
        
        /* Animaciones premium */
        @keyframes luxuryFadeIn {
            from { 
                opacity: 0;
                transform: translateY(-30px) scale(0.9);
            }
            to { 
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }
        
        @keyframes luxurySlideUp {
            from { 
                opacity: 0;
                transform: translateY(50px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .logo h1 { font-size: 3rem; }
            .slogan { font-size: 1.4rem; }
            .section-title { font-size: 2.5rem; }
            .services-grid, .products-grid, .contact-grid { grid-template-columns: 1fr; }
            .cta-buttons { flex-direction: column; align-items: center; }
            .service-header { flex-direction: column; gap: 1rem; }
            .business-info { flex-direction: column; align-items: center; }
        }
        
        /* Efectos especiales */
        .floating-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            pointer-events: none;
        }
        
        .floating-element {
            position: absolute;
            background: var(--accent-gold);
            border-radius: 50%;
            opacity: 0.1;
            animation: float 20s infinite linear;
        }
        
        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100px) rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Elementos flotantes decorativos -->
    <div class="floating-elements">
        <div class="floating-element" style="left: 10%; width: 20px; height: 20px; animation-delay: 0s;"></div>
        <div class="floating-element" style="left: 20%; width: 15px; height: 15px; animation-delay: 5s;"></div>
        <div class="floating-element" style="left: 80%; width: 25px; height: 25px; animation-delay: 10s;"></div>
    </div>

    <!-- Header Premium -->
    <header>
        <div class="logo">
            <h1>Ana González</h1>
            <p>Spa y Mas</p>
        </div>
        <p class="slogan">Donde la belleza se encuentra con la excelencia</p>
        <div class="cta-buttons">
            <a href="#services" class="btn-luxury">
                <i class="fas fa-spa"></i>
                Servicios Exclusivos
            </a>
            <a href="#products" class="btn-luxury btn-outline">
                <i class="fas fa-shopping-bag"></i>
                Productos Premium
            </a>
        </div>
    </header>
    
    <!-- Servicios Premium -->
    <section class="services" id="services">
        <h2 class="section-title">Servicios de Belleza Exclusivos</h2>
      