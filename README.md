# libro_dino2
libro dinosaurios2
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Libro: Dinosaurios</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&family=Playwrite+GB+S:ital,wght@0,100..400;1,100..400&display=swap" rel="stylesheet">
    
    <style>
        /* Paleta de colores cálida y vibrante con armonía análoga basada en la maqueta */
        :root {
            --bg-dark: #1b2e24; /* Fondo verde oscuro de la maqueta */
            --primary-accent: #ff6b4a; /* Naranja vibrante del botón de la maqueta */
            --gold-light: #ccd173; /* Tono verde/amarillo claro de los botones */
            --gold-dark: #9da352; /* Tono verde/oliva del título principal */
            --blue-soft: #b9cbe3; /* El azul claro de las figuras superiores */
            --purple-soft: #bcadb8; /* El lila de los botones inferiores */
            --text-light: #ffffff;
            --text-muted: #e2e8f0;
        }

        /* Estilos base */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Nunito Sans', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Tipografías especiales para títulos */
        h1, h2, h3, .badge-libro {
            font-family: 'Playwrite GB S', cursive;
            font-weight: 400;
        }

        /* Contenedor principal */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Encabezado / Hero al estilo de la maqueta */
        .hero {
            display: table;
            width: 100%;
            margin-top: 40px;
            margin-bottom: 60px;
        }

        .hero-row {
            display: table-row;
        }

        .hero-image-cell {
            display: table-cell;
            width: 40%;
            vertical-align: middle;
            position: relative;
        }

        .hero-image-wrapper {
            width: 100%;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; /* Silueta orgánica como en la maqueta */
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0,0,0,0.5);
            background: #2c4236;
        }

        .hero-image-wrapper img {
            width: 100%;
            display: block;
            object-fit: cover;
            min-height: 420px;
        }

        .hero-content-cell {
            display: table-cell;
            width: 60%;
            vertical-align: middle;
            padding-left: 5%;
        }

        /* Elementos decorativos superiores */
        .decorations {
            margin-bottom: 30px;
        }

        .shape-circles {
            display: inline-block;
            background-color: var(--blue-soft);
            width: 90px;
            height: 50px;
            border-radius: 25px;
            margin-right: 15px;
            opacity: 0.9;
            vertical-align: middle;
        }

        .shape-single-circle {
            display: inline-block;
            background-color: var(--blue-soft);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 15px;
            vertical-align: middle;
        }

        .badge-libro {
            display: inline-block;
            background-color: var(--gold-dark);
            color: #000;
            padding: 6px 35px;
            border-radius: 25px;
            font-size: 1.4rem;
            vertical-align: middle;
        }

        /* Título Principal de la Maqueta */
        .main-title-container {
            position: relative;
            margin-bottom: 40px;
            background-color: var(--gold-dark);
            padding: 15px 40px;
            border-radius: 40px;
            display: inline-block;
            width: 85%;
        }

        .main-title-container h1 {
            color: #000;
            font-size: 2.8rem;
            margin: 0;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* Botón Naranja con Flecha de la Maqueta */
        .btn-next {
            position: absolute;
            right: -35px;
            top: 50%;
            transform: translateY(-50%);
            background-color: var(--primary-accent);
            color: #000;
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            font-size: 2.2rem;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            transition: transform 0.3s, background-color 0.3s;
        }

        .btn-next:hover {
            transform: translateY(-50%) scale(1.08);
            background-color: #ff856a;
        }

        /* Botones de Navegación de Secciones */
        .section-nav {
            display: table;
            width: 100%;
            border-collapse: separate;
            border-spacing: 15px;
        }

        .nav-row {
            display: table-row;
        }

        .nav-button {
            display: table-cell;
            text-align: center;
            padding: 18px 20px;
            border-radius: 25px;
            color: #000;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: opacity 0.3s, transform 0.2s;
        }

        .nav-button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        .nav-sinopsis { background-color: var(--gold-light); }
        .nav-proceso { background-color: var(--blue-soft); }
        .nav-empaque { background-color: #8fa499; }
        .nav-fotos { background-color: var(--purple-soft); }

        /* Secciones de Contenido */
        .section-content {
            padding: 60px 0;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        .section-content h2 {
            font-size: 2.2rem;
            color: var(--gold-light);
            margin-bottom: 25px;
            border-left: 5px solid var(--primary-accent);
            padding-left: 15px;
        }

        .grid-2 {
            display: table;
            width: 100%;
        }

        .grid-2-cell {
            display: table-cell;
            width: 50%;
            vertical-align: top;
            padding: 15px;
        }

        .proceso-paso {
            background-color: rgba(255,255,255,0.05);
            padding: 20px;
            border-radius: 15px;
            margin-bottom: 20px;
            border-left: 4px solid var(--blue-soft);
        }

        .proceso-paso h3 {
            color: var(--blue-soft);
            margin-bottom: 10px;
            font-family: 'Nunito Sans', sans-serif;
            font-weight: bold;
        }

        /* Galería de Fotos del Producto */
        .gallery-grid {
            display: table;
            width: 100%;
            border-collapse: separate;
            border-spacing: 15px;
        }

        .gallery-row {
            display: table-row;
        }

        .gallery-cell {
            display: table-cell;
            width: 33.33%;
            background: #2c4236;
            border-radius: 15px;
            overflow: hidden;
            height: 280px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
        }

        .gallery-cell img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.3s;
        }

        .gallery-cell:hover img {
            transform: scale(1.05);
        }

        /* Caja de Autora y Redes Sociales */
        .author-box {
            background: linear-gradient(135deg, #243d30, #14211a);
            padding: 50px 40px;
            border-radius: 25px;
            margin-top: 40px;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.05);
        }

        .social-links {
            margin-top: 30px;
        }

        .social-btn {
            display: inline-block;
            background-color: var(--primary-accent);
            color: #000;
            padding: 12px 30px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            margin: 10px;
            transition: background-color 0.3s, transform 0.2s;
        }

        .social-btn:hover {
            background-color: var(--gold-light);
            transform: translateY(-2px);
        }

        footer {
            text-align: center;
            padding: 50px 0;
            font-size: 0.9rem;
            color: rgba(255,255,255,0.4);
        }

        /* RESPONSIVIDAD (MÓVIL Y TABLETS) */
        @media (max-width: 768px) {
            .hero, .hero-row, .hero-image-cell, .hero-content-cell,
            .section-nav, .nav-row, .nav-button,
            .grid-2, .grid-2-cell,
            .gallery-grid, .gallery-row, .gallery-cell {
                display: block !important;
                width: 100% !important;
                padding-left: 0 !important;
                padding-right: 0 !important;
                margin-bottom: 20px !important;
            }

            .hero-image-wrapper img {
                min-height: 280px;
            }

            .main-title-container {
                width: 100%;
                text-align: center;
                padding: 15px 20px;
            }

            .main-title-container h1 {
                font-size: 2.2rem;
            }

            .btn-next {
                position: relative;
                right: 0;
                top: 0;
                transform: none;
                margin: 20px auto 0 auto;
            }

            .decorations {
                text-align: center;
            }

            .gallery-cell {
                height: 220px;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        
        <header class="hero">
            <div class="hero-row">
                
                <div class="hero-image-cell">
                    <div class="hero-image-wrapper">
                        <img src="https://images.unsplash.com/photo-1569336415962-a4bd9f69cd83?auto=format&fit=crop&q=80&w=800" alt="Tiranosaurio Rex - Libro Dinosaurios">
                    </div>
                </div>

                <div class="hero-content-cell">
                    
                    <div class="decorations">
                        <div class="shape-circles"></div>
                        <div class="shape-single-circle"></div>
                        <div class="badge-libro">Libro</div>
                    </div>

                    <div class="main-title-container">
                        <h1>Dinosaurios</h1>
                        <a href="#sinopsis" class="btn-next" aria-label="Ver sinopsis">&#8250;</a>
                    </div>

                    <nav class="section-nav">
                        <div class="nav-row">
                            <a href="#sinopsis" class="nav-button nav-sinopsis">Sinopsis</a>
                            <a href="#proceso" class="nav-button nav-proceso">El proceso creativo</a>
                        </div>
                        <div class="nav-row">
                            <a href="#empaque" class="nav-button nav-empaque">Diseño de empaque</a>
                            <a href="#fotografias" class="nav-button nav-fotos">Fotografías del producto</a>
                        </div>
                    </nav>

                </div>
            </div>
        </header>

        <section id="sinopsis" class="section-content">
            <h2>Sinopsis</h2>
            <div class="grid-2">
                <div class="grid-2-cell">
                    <p style="font-size: 1.2rem; margin-bottom: 15px; color: var(--gold-light);">
                        <strong>Una ventana inmersiva hacia la era de los gigantes.</strong>
                    </p>
                    <p>
                        El libro "Dinosaurios" fusiona de manera magistral la ilustración de vanguardia con las últimas revelaciones de la paleontología moderna. Diseñado no solo para informar, sino para impactar visualmente, transporta al espectador a paisajes jurásicos y cretácicos mediante una composición de color análoga y texturas salvajes nunca antes vistas en el diseño editorial.
                    </p>
                </div>
                <div class="grid-2-cell">
                    <div style="background-color: rgba(255,255,255,0.03); padding: 30px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.1); text-align: center;">
                        <h3 style="font-size: 1.4rem; color: var(--primary-accent); margin-bottom: 10px; font-family: 'Nunito Sans', sans-serif; font-weight: bold;">Edición Exclusiva</h3>
                        <p style="font-size: 0.95rem; margin-bottom: 20px;">Consigue acceso anticipado a la preventa oficial firmada por la autora.</p>
                        <a href="#" class="social-btn" style="margin: 0; width: 100%;">Reservar Mi Libro</a>
                    </div>
                </div>
            </div>
        </section>

        <section id="proceso" class="section-content">
            <h2>El Proceso Creativo</h2>
            <p style="margin-bottom: 30px; max-width: 800px;">La construcción de este libro requirió meses de reconstrucción conceptual y gráfica para recrear la majestuosidad de la fauna prehistórica:</p>
            
            <div class="proceso-paso">
                <h3>1. Curaduría Científica</h3>
                <p>Estudio anatómico riguroso a partir de fósiles reales para determinar proporciones, posturas dinámicas y la biomecánica de cada ejemplar.</p>
            </div>
            
            <div class="proceso-paso">
                <h3>2. Ilustración y Armonía Cromática</h3>
                <p>Aplicación de una paleta análoga cálida y vibrante con el fin de evocar el clima denso y los paisajes indómitos característicos de sus eras correspondientes.</p>
            </div>

            <div class="proceso-paso">
                <h3>3. Maquetación Editorial</h3>
                <p>Integración armónica del texto educativo con dobles páginas de impacto visual absoluto para generar una experiencia fluida y sorprendente.</p>
            </div>
        </section>

        <section id="empaque" class="section-content">
            <h2>Diseño de Empaque</h2>
            <div class="grid-2">
                <div class="grid-2-cell">
                    <p>
                        El concepto detrás del empaque sigue la premisa de un <em>"descubrimiento arqueológico"</em>. Cada libro viene protegido por una caja contenedora rígida texturizada de edición limitada.
                    </p>
                    <p style="margin-top: 15px;">
                        Los materiales utilizados reflejan robustez y sustentabilidad, protegiendo las páginas e invitando al lector a un ritual de apertura único antes de tocar el primer capítulo.
                    </p>
                </div>
                <div class="grid-2-cell">
                    <div style="background-color: #243d30; padding: 25px; border-radius: 15px; border-left: 4px solid #8fa499;">
                        <ul style="list-style: none;">
                            <li style="margin-bottom: 10px;"><strong>Material:</strong> Cartón prensado ecológico de 1200g.</li>
                            <li style="margin-bottom: 10px;"><strong>Acabados:</strong> Estampado en seco y detalles con barniz de relieve.</li>
                            <li><strong>Seguridad:</strong> Cierre con solapa imantada invisible.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section id="fotografias" class="section-content">
            <h2>Fotografías del Producto</h2>
            <p style="margin-bottom: 30px;">Una mirada detallada al volumen físico, los acabados del papel mate y la nitidez de la impresión:</p>
            
            <div class="gallery-grid">
                <div class="gallery-row">
                    <div class="gallery-cell">
                        <img src="https://images.unsplash.com/photo-1544947950-fa07a98d237f?auto=format&fit=crop&q=80&w=500" alt="Fotografía de portada del libro">
                    </div>
                    <div class="gallery-cell">
                        <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?auto=format&fit=crop&q=80&w=500" alt="Fotografía de páginas del libro">
                    </div>
                    <div class="gallery-cell">
                        <img src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&q=80&w=500" alt="Fotografía del empaque cerrado">
                    </div>
                </div>
            </div>
        </section>

        <section class="author-box">
            <h2 style="border: none; padding: 0; color: #fff; margin-bottom: 15px;">Sobre la Autora</h2>
            <p style="max-width: 650px; margin: 0 auto; color: var(--text-muted); font-size: 1.1rem;">
                Diseñadora visual especializada en ilustración conceptual y proyectos editoriales inspirados en la naturaleza y el registro histórico.
            </p>
            
            <div class="social-links">
                <a href="#" class="social-btn" target="_blank" rel="noopener">Instagram</a>
                <a href="#" class="social-btn" target="_blank" rel="noopener">Behance</a>
                <a href="#" class="social-btn" target="_blank" rel="noopener">LinkedIn</a>
            </div>
        </section>

        <footer>
            <p>&copy; 2026 Landing Page Oficial - Libro Dinosaurios.</p>
        </footer>

    </div>

</body>
</html>
