<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brand Builders Investment - Maximiza tus Inversiones en Wall Street</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: #1a1a1a;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #3b82f6, #06b6d4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
            color: white;
            padding: 120px 0 80px;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%234f46e5' fill-opacity='0.1'%3E%3Ccircle cx='30' cy='30' r='2'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E") repeat;
            animation: float 20s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 1.5rem;
            background: linear-gradient(45deg, #ffffff, #06b6d4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin: 3rem 0;
            flex-wrap: wrap;
        }
        
        .stat {
            text-align: center;
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: 800;
            color: #06b6d4;
            display: block;
        }
        
        .stat-label {
            font-size: 1rem;
            opacity: 0.8;
        }
        
        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #3b82f6, #06b6d4);
            color: white;
            padding: 18px 40px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
            border: none;
            cursor: pointer;
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 20px 40px rgba(59, 130, 246, 0.4);
        }
        
        /* Services Section */
        .services {
            padding: 100px 0;
            background: #f8fafc;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: #1a1a1a;
        }
        
        .section-subtitle {
            text-align: center;
            font-size: 1.2rem;
            color: #64748b;
            margin-bottom: 4rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border: 1px solid #e2e8f0;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.15);
        }
        
        .service-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(45deg, #3b82f6, #06b6d4);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            color: white;
            font-size: 1.5rem;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #1a1a1a;
        }
        
        .service-card p {
            color: #64748b;
            line-height: 1.7;
        }
        
        /* Benefits Section */
        .benefits {
            padding: 100px 0;
            background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
            color: white;
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .benefit {
            text-align: center;
            padding: 2rem;
        }
        
        .benefit-icon {
            width: 80px;
            height: 80px;
            background: rgba(59, 130, 246, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            font-size: 2rem;
        }
        
        .benefit h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }
        
        .benefit p {
            opacity: 0.9;
        }
        
        /* Pricing Section */
        .pricing {
            padding: 100px 0;
            background: white;
        }
        
        .pricing-card {
            max-width: 400px;
            margin: 3rem auto 0;
            background: linear-gradient(135deg, #f8fafc 0%, #ffffff 100%);
            border-radius: 20px;
            padding: 3rem;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            border: 2px solid #e2e8f0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .pricing-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(45deg, #3b82f6, #06b6d4);
        }
        
        .price {
            font-size: 3.5rem;
            font-weight: 800;
            color: #3b82f6;
            margin-bottom: 0.5rem;
        }
        
        .price-subtitle {
            color: #64748b;
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }
        
        .features-list {
            list-style: none;
            margin-bottom: 2.5rem;
            text-align: left;
        }
        
        .features-list li {
            padding: 0.75rem 0;
            border-bottom: 1px solid #e2e8f0;
            position: relative;
            padding-left: 2rem;
        }
        
        .features-list li:before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #10b981;
            font-weight: bold;
        }
        
        .features-list li:last-child {
            border-bottom: none;
        }
        .contact {
            padding: 100px 0;
            background: white;
        }
        
        .form-container {
            max-width: 600px;
            margin: 0 auto;
            background: #f8fafc;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: #374151;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #e2e8f0;
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }
        
        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }
        
        .submit-btn {
            width: 100%;
            background: linear-gradient(45deg, #3b82f6, #06b6d4);
            color: white;
            padding: 18px;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
        }
        
        /* Footer */
        footer {
            background: #0f172a;
            color: white;
            text-align: center;
            padding: 3rem 0;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .stats {
                gap: 2rem;
            }
            
            .stat-number {
                font-size: 2rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .benefits-grid {
                grid-template-columns: 1fr;
            }
            
            .form-container {
                margin: 0 20px;
                padding: 2rem;
            }
            
            .whatsapp-btn {
                width: 55px;
                height: 55px;
                bottom: 20px;
                right: 20px;
                font-size: 1.6rem;
            }
            
            .whatsapp-text {
                bottom: 85px;
                right: 20px;
                font-size: 0.8rem;
            }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* WhatsApp Button */
        .whatsapp-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25d366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            text-decoration: none;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.4);
            z-index: 1000;
            transition: all 0.3s ease;
            animation: bounce 2s infinite;
        }
        
        .whatsapp-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 30px rgba(37, 211, 102, 0.6);
        }
        
        @keyframes bounce {
            0%, 20%, 53%, 80%, 100% {
                transform: translate3d(0,0,0);
            }
            40%, 43% {
                transform: translate3d(0, -8px, 0);
            }
            70% {
                transform: translate3d(0, -4px, 0);
            }
        }
        
        .whatsapp-btn::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            border: 2px solid #25d366;
            animation: ping 2s infinite;
        }
        
        @keyframes ping {
            0% {
                transform: scale(1);
                opacity: 1;
            }
            75%, 100% {
                transform: scale(2);
                opacity: 0;
            }
        }
        
        .whatsapp-text {
            position: fixed;
            bottom: 100px;
            right: 30px;
            background: #25d366;
            color: white;
            padding: 10px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            z-index: 999;
            opacity: 0;
            animation: fadeInOut 4s infinite;
            white-space: nowrap;
        }
        
        .whatsapp-text::after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 20px;
            width: 0;
            height: 0;
            border-left: 8px solid transparent;
            border-right: 8px solid transparent;
            border-top: 8px solid #25d366;
        }
        
        @keyframes fadeInOut {
            0%, 100% { opacity: 0; transform: translateY(10px); }
            20%, 80% { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">Brand Builders Investment</div>
            <button class="cta-button" onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'})">
                Comenzar Ahora
            </button>
        </nav>
    </header>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Maximiza tus Inversiones en Wall Street</h1>
                <p>Recibe señales expertas de compra y venta para las acciones más prometedoras del mercado estadounidense</p>
                
                <div class="stats">
                    <div class="stat">
                        <span class="stat-number">20%</span>
                        <span class="stat-label">Rentabilidad Objetivo</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">$200</span>
                        <span class="stat-label">Desde Solo</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">24/7</span>
                        <span class="stat-label">Monitoreo del Mercado</span>
                    </div>
                </div>
                
                <button class="cta-button pulse" onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'})">
                    Obtener Señales Ahora
                </button>
            </div>
        </div>
    </section>

    <section class="services">
        <div class="container">
            <h2 class="section-title">Nuestros Servicios</h2>
            <p class="section-subtitle">Te proporcionamos las herramientas y conocimiento necesario para maximizar tus inversiones</p>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📈</div>
                    <h3>Señales de Compra</h3>
                    <p>Identifica las mejores oportunidades de entrada al mercado con nuestro análisis técnico y fundamental avanzado.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">📉</div>
                    <h3>Señales de Venta</h3>
                    <p>Protege tus ganancias y minimiza pérdidas con nuestras alertas de salida estratégica basadas en datos.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">🎯</div>
                    <h3>Análisis de Acciones</h3>
                    <p>Obtén análisis detallados de las acciones más prometedoras del mercado estadounidense seleccionadas por expertos.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="benefits">
        <div class="container">
            <h2 class="section-title">¿Por qué elegir Brand Builders Investment?</h2>
            <p class="section-subtitle">Nuestra experiencia y metodología probada te dan la ventaja que necesitas</p>
            
            <div class="benefits-grid">
                <div class="benefit">
                    <div class="benefit-icon">🚀</div>
                    <h3>Alta Rentabilidad</h3>
                    <p>Objetivo de hasta 20% de rentabilidad con estrategias probadas</p>
                </div>
                
                <div class="benefit">
                    <div class="benefit-icon">⚡</div>
                    <h3>Alertas en Tiempo Real</h3>
                    <p>Recibe señales instantáneas para no perder ninguna oportunidad</p>
                </div>
                
                <div class="benefit">
                    <div class="benefit-icon">🛡️</div>
                    <h3>Gestión de Riesgo</h3>
                    <p>Protege tu capital con nuestros sistemas de stop-loss inteligente</p>
                </div>
                
                <div class="benefit">
                    <div class="benefit-icon">🎓</div>
                    <h3>Asesoría Experta</h3>
                    <p>Equipo de analistas con años de experiencia en Wall Street</p>
                </div>
            </div>
        </div>
    </section>

    <section class="pricing">
        <div class="container">
            <h2 class="section-title">Acceso a Señales Profesionales</h2>
            <p class="section-subtitle">Obtén acceso completo a nuestras señales de inversión y análisis experto</p>
            
            <div class="pricing-card">
                <div class="price">$200</div>
                <div class="price-subtitle">Acceso mensual a señales premium</div>
                
                <ul class="features-list">
                    <li>Señales de compra y venta en tiempo real</li>
                    <li>Análisis técnico y fundamental detallado</li>
                    <li>Alertas push instantáneas</li>
                    <li>Acciones más prometedoras del mercado US</li>
                    <li>Gestión de riesgo y stop-loss</li>
                    <li>Soporte por WhatsApp/Telegram</li>
                    <li>Reportes de rendimiento semanales</li>
                </ul>
                
                <button class="cta-button pulse" onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'})">
                    Contratar Ahora - $200/mes
                </button>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Comienza a Invertir Hoy</h2>
            <p class="section-subtitle">Completa el formulario y uno de nuestros expertos se pondrá en contacto contigo</p>
            
            <div class="form-container">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="name">Nombre Completo *</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email *</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="phone">Teléfono</label>
                        <input type="tel" id="phone" name="phone">
                    </div>
                    
                    <div class="form-group">
                        <label for="plan">Plan de Interés *</label>
                        <select id="plan" name="plan" required style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1rem;">
                            <option value="">Selecciona una opción</option>
                            <option value="consulta">Consulta gratuita primero</option>
                            <option value="suscripcion">Suscripción mensual - $200</option>
                            <option value="informacion">Más información sobre servicios</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="investment">Capital de Inversión Aproximado</label>
                        <input type="text" id="investment" name="investment" placeholder="Ej: $10,000 - $50,000">
                    </div>
                    
                    <div class="form-group">
                        <label for="message">¿Cuáles son tus objetivos de inversión?</label>
                        <textarea id="message" name="message" placeholder="Cuéntanos sobre tu experiencia y objetivos..."></textarea>
                    </div>
                    
                    <button type="submit" class="submit-btn">Solicitar Consulta Gratuita</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Brand Builders Investment. Todos los derechos reservados.</p>
            <p style="margin-top: 10px; opacity: 0.7; font-size: 0.9rem;">
                * Los rendimientos pasados no garantizan resultados futuros. Las inversiones conllevan riesgo.
            </p>
        </div>
    </footer>

    <!-- WhatsApp Button -->
    <div class="whatsapp-text">💬 ¿Necesitas ayuda?</div>
    <a href="https://wa.me/41779751831?text=Hola,%20estoy%20interesado%20en%20los%20servicios%20de%20Brand%20Builders%20Investment%20para%20señales%20de%20inversión" 
       target="_blank" 
       class="whatsapp-btn"
       title="Contactar por WhatsApp">
        💬
    </a>

    <script>
        // Form submission handler
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form data
            const formData = new FormData(this);
            const data = Object.fromEntries(formData);
            
            // Simple validation
            if (!data.name || !data.email || !data.plan) {
                alert('Por favor completa los campos obligatorios');
                return;
            }
            
            // Simulate form submission
            const submitBtn = document.querySelector('.submit-btn');
            const originalText = submitBtn.textContent;
            
            submitBtn.textContent = 'Enviando...';
            submitBtn.disabled = true;
            
            setTimeout(() => {
                alert('¡Gracias por tu interés! Nos pondremos en contacto contigo pronto.');
                this.reset();
                submitBtn.textContent = originalText;
                submitBtn.disabled = false;
            }, 2000);
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add scroll effect to header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(15, 23, 42, 0.95)';
            } else {
                header.style.background = 'linear-gradient(135deg, #0f172a 0%, #1e293b 100%)';
            }
        });
    </script>
</body>
</html>
