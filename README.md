<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Luxury Transfers Riviera - Transporte Premium</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    
    <style>
        /* --- VARIABLES --- */
        :root { 
            --primary-blue: #003580; --action-green: #00a651; --action-green-hover: #008c44;
            --text-dark: #1a1a1a; --white: #ffffff; 
            --navy-bg: #002855;      
            --gold-accent: #d4af37; --gold-hover: #febb02;
            --orange-btn: #ff8c00; --wa-green: #25d366;
            --font-main: 'Montserrat', sans-serif; --font-title: 'Playfair Display', serif;
        }
        body { font-family: var(--font-main); margin: 0; padding: 0; background-color: #f9f9f9; color: var(--text-dark); overflow-x: hidden; }

        /* --- NAVBAR --- */
        .navbar { 
            position: fixed; top: 0; left: 0; width: 100%; 
            background: rgba(0, 40, 85, 0.98); 
            backdrop-filter: blur(10px); 
            padding: 10px 0; 
            z-index: 1000; 
            box-shadow: 0 4px 20px rgba(0,0,0,0.3); 
            border-bottom: 1px solid rgba(212, 175, 55, 0.3); 
        }
        .nav-container { 
            width: 90%; max-width: 1200px; margin: 0 auto; 
            display: flex; justify-content: space-between; align-items: center; 
        }
        .nav-logo { display: flex; align-items: center; text-decoration: none; gap: 5px; }
        .nav-logo img { height: 60px; width: auto; object-fit: contain; filter: drop-shadow(0 2px 4px rgba(0,0,0,0.3)); }
        .nav-logo-text { font-family: var(--font-title); color: var(--white); font-size: 24px; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; line-height: 1; display: flex; flex-direction: column; }
        .nav-links { display: flex; gap: 30px; align-items: center; }
        .nav-link { color: var(--white); text-decoration: none; font-weight: 600; font-size: 14px; text-transform: uppercase; letter-spacing: 1px; transition: 0.3s; padding: 5px 0; }
        .nav-link:hover { color: var(--gold-accent); border-bottom: 2px solid var(--gold-accent); }

        /* --- HERO SECTION --- */
        .hero-section {
            position: relative; min-height: 100vh;
            background: url('https://images.unsplash.com/photo-1590523741831-ab7e8b8f9c7f?q=80&w=2069&auto=format&fit=crop') no-repeat center center;
            background-size: cover; background-attachment: fixed; 
            display: flex; flex-direction: column; align-items: center; justify-content: center; 
            padding: 140px 20px 60px 20px; 
        }
        .overlay { position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: linear-gradient(to bottom, rgba(0, 40, 85, 0.5), rgba(0, 30, 80, 0.7)); z-index: 1; }
        .hero-content { position: relative; z-index: 10; text-align: center; margin-bottom: 40px; color: var(--white); }
        .hero-title { font-family: var(--font-title); font-size: 52px; font-weight: 700; margin-bottom: 15px; text-transform: uppercase; text-shadow: 0 4px 20px rgba(0,0,0,0.6); letter-spacing: 2px; }
        .hero-subtitle { font-size: 18px; font-weight: 300; letter-spacing: 1px; opacity: 0.95; text-shadow: 0 2px 10px rgba(0,0,0,0.5); }

        /* --- COTIZADOR --- */
        .main-container { position: relative; z-index: 10; width: 100%; max-width: 1100px; }
        .search-box-container { background-color: var(--gold-accent); padding: 3px; border-radius: 12px; box-shadow: 0 20px 50px rgba(0,0,0,0.5); }
        .search-box-inner { background-color: var(--white); padding: 25px; border-radius: 9px; }
        .options-bar { display: flex; justify-content: space-between; margin-bottom: 20px; align-items: center; border-bottom: 1px solid #eee; padding-bottom: 15px; }
        .radio-group { display: flex; gap: 20px; }
        .radio-label { display: flex; align-items: center; cursor: pointer; font-size: 14px; font-weight: 700; color: var(--primary-blue); }
        .radio-label input { margin-right: 8px; accent-color: var(--primary-blue); width: 18px; height: 18px; }
        .direction-tabs { display: flex; gap: 10px; margin-bottom: 20px; flex-wrap: wrap; }
        .tab-btn { background: #f0f2f5; color: var(--text-gray); border: 1px solid #ddd; padding: 12px 20px; border-radius: 50px; cursor: pointer; font-size: 13px; font-weight: 600; transition: 0.3s; display: flex; align-items: center; gap: 8px; flex: 1; justify-content: center; }
        .tab-btn.active { background: var(--primary-blue); color: var(--white); border-color: var(--primary-blue); font-weight: 800; box-shadow: 0 5px 15px rgba(0,53,128,0.3); transform: translateY(-2px); }
        .form-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 15px; padding: 10px; border-radius: 10px; background: #f9f9f9; border: 1px solid #eee; }
        .input-wrapper { background: var(--white); padding: 12px 15px; display: flex; flex-direction: column; justify-content: center; border-radius: 8px; border: 1px solid #ddd; transition: 0.2s; }
        .input-wrapper:focus-within { border-color: var(--gold-accent); box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2); }
        .input-wrapper label { font-size: 11px; color: var(--primary-blue); font-weight: 800; margin-bottom: 4px; text-transform: uppercase; }
        .input-wrapper input, .input-wrapper select, .input-wrapper textarea { border: none; outline: none; width: 100%; font-size: 15px; font-weight: 600; color: var(--text-dark); background: transparent; font-family: var(--font-main); padding: 0; }
        .contact-section { grid-column: 1 / -1; display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 15px; margin-top: 15px; border-top: 2px dashed #ddd; padding-top: 20px; }
        .btn-cotizar { grid-column: 1 / -1; background-color: var(--action-green); color: white; font-size: 18px; font-weight: 800; border: none; padding: 18px; border-radius: 8px; cursor: pointer; margin-top: 10px; transition: all 0.2s; text-transform: uppercase; letter-spacing: 1px; box-shadow: 0 5px 0 #007a3d; width: 100%; }
        .btn-cotizar:hover { background-color: var(--action-green-hover); transform: translateY(2px); }

        /* --- SECCIÓNES GENÉRICAS --- */
        .section-wrapper { padding: 80px 20px; text-align: center; }
        .section-bg-gray { background-color: #f0f0f0; }
        .section-header h2 { font-family: var(--font-title); font-size: 42px; color: var(--navy-bg); font-weight: 700; margin-bottom: 10px; letter-spacing: -1px; }
        .section-header p { color: #666; font-size: 16px; margin-bottom: 60px; max-width: 700px; margin: 0 auto 60px auto; }

        /* --- SECCIÓN SERVICIOS --- */
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 30px; max-width: 1200px; margin: 0 auto; }
        .service-card { background-color: var(--navy-bg); border: 1px solid var(--gold-accent); border-radius: 15px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.3); transition: all 0.4s ease; position: relative; display: flex; flex-direction: column; }
        .service-card:hover { transform: translateY(-10px); box-shadow: 0 20px 40px rgba(212, 175, 55, 0.3); border-color: var(--gold-hover); }
        .service-img { height: 220px; width: 100%; object-fit: cover; mask-image: linear-gradient(to bottom, black 70%, transparent 100%); -webkit-mask-image: linear-gradient(to bottom, black 70%, transparent 100%); }
        .service-info { padding: 10px 30px 40px 30px; text-align: center; margin-top: -20px; position: relative; z-index: 2; }
        .service-icon { font-size: 40px; color: var(--gold-accent); margin-bottom: 20px; text-shadow: 0 2px 10px rgba(0,0,0,0.5); }
        .service-title { font-family: var(--font-title); font-size: 26px; color: var(--white); margin-bottom: 15px; font-weight: 700; }
        .service-desc { font-size: 14px; color: #cbd5e1; line-height: 1.6; font-weight: 400; }

        /* =========================================
           NUEVOS ESTILOS DEL CARRUSEL (CON FLECHAS Y PUNTOS)
        ========================================= */
        .new-carousel-container {
            position: relative;
            max-width: 900px; /* Ancho máximo del carrusel */
            margin: 0 auto;
            background: #fff;
            border-radius: 20px;
            box-shadow: 0 25px 50px rgba(0,0,0,0.15);
            overflow: hidden;
        }
        .new-carousel-track-container {
            position: relative;
            overflow: hidden;
            /* Altura automática basada en el contenido */
        }
        .new-carousel-track {
            padding: 0; margin: 0; list-style: none;
            position: relative;
            display: flex; /* Alinea los slides horizontalmente */
            transition: transform 0.5s ease-in-out;
        }
        .new-carousel-slide {
            min-width: 100%; /* Cada slide ocupa el 100% del ancho */
            box-sizing: border-box;
            position: relative; /* Importante para el posicionamiento JS */
        }
        .new-carousel-image {
            width: 100%;
            height: 350px; /* Altura fija para las imágenes */
            object-fit: cover;
            border-bottom: 4px solid var(--gold-accent);
        }
        .new-carousel-content {
            padding: 40px;
            text-align: center;
        }
        .new-carousel-content h3 {
            font-family: var(--font-title);
            font-size: 32px;
            color: var(--navy-bg);
            margin-bottom: 15px;
            font-weight: 700;
        }
        .new-carousel-content p {
            font-size: 16px;
            color: #555;
            line-height: 1.6;
            margin-bottom: 25px;
            max-width: 600px;
            margin-left: auto; margin-right: auto;
        }
        .capacity-badge {
            display: inline-block;
            background: var(--navy-bg);
            padding: 8px 25px;
            border-radius: 50px;
            font-weight: 700;
            color: var(--gold-accent);
            font-size: 14px;
            box-shadow: 0 5px 15px rgba(0, 40, 85, 0.2);
        }
        /* Flechas de Navegación */
        .new-carousel-btn {
            position: absolute;
            top: 40%; /* Alineado verticalmente con la imagen */
            transform: translateY(-50%);
            background: rgba(255, 255, 255, 0.8);
            color: var(--navy-bg);
            border: none;
            width: 50px; height: 50px;
            border-radius: 50%;
            font-size: 20px;
            cursor: pointer;
            z-index: 10;
            transition: 0.3s;
            display: flex; align-items: center; justify-content: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            backdrop-filter: blur(5px);
        }
        .new-carousel-btn:hover { background: var(--navy-bg); color: var(--gold-accent); }
        .new-carousel-btn--left { left: 20px; }
        .new-carousel-btn--right { right: 20px; }
        /* Clase para ocultar flechas al inicio/final */
        .is-hidden { display: none; }

        /* Puntos de Navegación (Dots) */
        .new-carousel-nav {
            display: flex;
            justify-content: center;
            padding: 20px 0 30px 0; /* Espacio abajo */
            gap: 10px;
        }
        .new-carousel-dot {
            border: none;
            width: 12px; height: 12px;
            border-radius: 50%;
            background: #ddd;
            cursor: pointer;
            transition: 0.3s all ease;
        }
        .new-carousel-dot.current-slide {
            background: var(--navy-bg);
            width: 35px; /* Se estira al estar activo */
            border-radius: 10px;
        }


        /* --- FOOTER & OTROS --- */
        footer { background: var(--navy-bg); color: #94a3b8; padding: 40px 20px; text-align: center; font-size: 14px; border-top: 1px solid rgba(255,255,255,0.1); }
        #resultados { margin-top: 30px; display: none; width: 100%; }
        .ruta-header { background: var(--navy-bg); color: white; padding: 15px; border-radius: 8px; margin-bottom: 20px; text-align: center; font-weight: 600; border-left: 5px solid var(--gold-accent); }
        .tarjeta { background: var(--white); border-radius: 16px; padding: 25px; margin-bottom: 25px; box-shadow: 0 10px 30px rgba(0,0,0,0.08); display: flex; flex-wrap: wrap; gap: 25px; border: 1px solid #eee; }
        .tarjeta:hover { transform: translateY(-5px); border-color: var(--primary-blue); }
        .tarjeta-img { flex: 0 0 220px; display: flex; align-items: center; justify-content: center; }
        .tarjeta-img img { width: 100%; max-height: 140px; object-fit: contain; }
        .tarjeta-info { flex: 1; display: flex; flex-direction: column; justify-content: center; }
        .tarjeta-price { flex: 0 0 180px; text-align: right; display: flex; flex-direction: column; justify-content: center; border-left: 2px solid #f5f5f5; padding-left: 25px; }
        .price-current { font-size: 32px; font-weight: 900; color: var(--action-green); }
        .modal-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); z-index: 2000; display: none; align-items: center; justify-content: center; backdrop-filter: blur(5px); }
        .modal-box { background: white; width: 90%; max-width: 450px; padding: 30px; border-radius: 20px; text-align: center; position: relative; }
        .loading-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(255,255,255,0.95); z-index: 3000; display: none; align-items: center; justify-content: center; flex-direction: column; }
        .spinner { width: 50px; height: 50px; border: 5px solid #eee; border-top: 5px solid var(--action-green); border-radius: 50%; animation: spin 1s linear infinite; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }

        @media (max-width: 768px) {
            .hero-title { font-size: 32px; } .nav-links { display: none; } .nav-container { justify-content: center; }
            .nav-logo img { height: 40px; } .nav-logo-text { font-size: 16px; }
            .form-grid, .contact-section { grid-template-columns: 1fr; }
            /* Ajustes del nuevo carrusel en móvil */
            .new-carousel-image { height: 220px; }
            .new-carousel-content { padding: 25px 20px; }
            .new-carousel-content h3 { font-size: 26px; }
            .new-carousel-btn { width: 40px; height: 40px; font-size: 16px; }
            .new-carousel-btn--left { left: 10px; } .new-carousel-btn--right { right: 10px; }

            .tarjeta { flex-direction: column; text-align: left; }
            .tarjeta-price { border-left: none; padding-left: 0; border-top: 1px solid #eee; padding-top: 15px; text-align: left; flex-direction: row; justify-content: space-between; align-items: center; }
        }
    </style>
</head>
<body>

<nav class="navbar">
    <div class="nav-container">
        <a href="#" class="nav-logo">
            <img src="https://i.imgur.com/lS3Crlx.png" alt="Luxury Transfers Riviera">
            <span class="nav-logo-text">Luxury Transfers Riviera</span>
        </a>
        <div class="nav-links">
            <a href="#inicio" class="nav-link">Inicio</a>
            <a href="#servicios" class="nav-link">Servicios</a>
            <a href="#flota" class="nav-link">Flota</a>
        </div>
    </div>
</nav>

<div class="loading-overlay" id="loadingOverlay"><div class="spinner"></div><p style="margin-top:15px; font-weight:700;">PROCESANDO...</p></div>
<div class="modal-overlay" id="modalTyC"><div class="modal-box" style="text-align: left;"><button style="position:absolute; top:15px; right:15px; border:none; background:transparent; font-weight:bold; cursor:pointer;" onclick="cerrarTyC()">X</button><h3 style="color:var(--primary-blue);">Términos y Condiciones</h3><div style="font-size:13px; line-height:1.5; color:#555;"><p>1. Cancelaciones 24h antes: 100% reembolso.</p><p>2. Espera máxima: 60 min aeropuerto, 15 min hotel.</p><p>3. Multa limpieza: $2,500 MXN.</p></div><button class="btn-cotizar" onclick="cerrarTyC()" style="margin-top:15px;">ENTENDIDO</button></div></div>
<div class="modal-overlay" id="modalConfirmacion"><div class="modal-box"><button style="position:absolute; top:15px; right:15px; border:none; background:transparent; font-weight:bold; cursor:pointer;" onclick="cerrarModal()">X</button><div style="font-size:60px; color:var(--action-green); margin-bottom:15px;"><i class="fas fa-check-circle"></i></div><h2 style="color:var(--primary-blue); margin:0;">¡Solicitud Recibida!</h2><p style="color:#888; font-size:12px; margin-top:5px;">CÓDIGO DE REFERENCIA:</p><div id="codigoDisplay" style="font-size:28px; font-weight:900; color:var(--primary-blue); letter-spacing:2px; margin-bottom:15px;">LTR-????</div><p style="color:#555; font-size:14px;">Hemos recibido tu solicitud. Un asesor te contactará lo más breve posible.</p><div style="display:flex; flex-direction:column; gap:10px; margin-top:20px;"><a href="#" target="_blank" id="btnWhatsapp" style="background:#25d366; color:white; padding:12px; border-radius:8px; text-decoration:none; font-weight:bold;"><i class="fab fa-whatsapp"></i> Confirmar por WhatsApp</a><a href="#" id="btnMail" style="background:#333; color:white; padding:12px; border-radius:8px; text-decoration:none; font-weight:bold;"><i class="fas fa-envelope"></i> Enviar Correo</a></div></div></div>

<section id="inicio" class="hero-section">
    <div class="overlay"></div>
    <div class="hero-content">
        <h1 class="hero-title">Transporte Premium</h1>
        <div class="hero-subtitle">Excelencia, Seguridad y Confort en la Riviera Maya</div>
    </div>
    <div class="main-container"><div class="search-box-container"><div class="search-box-inner"><div class="options-bar"><div class="radio-group"><label class="radio-label"><input type="radio" name="tipoViaje" value="SENCILLO" checked onchange="updateTipoServicio('SENCILLO')"> Solo Ida</label><label class="radio-label"><input type="radio" name="tipoViaje" value="REDONDO" onchange="updateTipoServicio('REDONDO')"> Ida y Vuelta</label></div><select id="tipoServicio" style="display:none;"><option value="SENCILLO">Sencillo</option><option value="REDONDO">Redondo</option></select><div style="width:100px;"><select id="moneda" onchange="limpiarResultados()" style="width:100%; padding:8px; font-weight:700; border-radius:5px;"><option value="MXN">MXN</option><option value="USD">USD</option></select></div></div><div class="direction-tabs"><div class="tab-btn active" id="btnDesdeAero" onclick="setDireccion('desdeAero')"><i class="fas fa-plane-arrival"></i> Desde Aeropuerto</div><div class="tab-btn" id="btnHaciaAero" onclick="setDireccion('haciaAero')"><i class="fas fa-plane-departure"></i> Hacia Aeropuerto</div><div class="tab-btn" id="btnPersonalizado" onclick="setDireccion('personalizado')"><i class="fas fa-map-marker-alt"></i> Punto a Punto</div></div><div class="form-grid"><div class="input-wrapper"><label><i class="fas fa-map-pin"></i> Origen</label><input type="text" id="origen" placeholder="Aeropuerto Cancún (CUN)" readonly></div><div class="input-wrapper"><label><i class="fas fa-map-marker-alt"></i> Destino</label><input type="text" id="destino" placeholder="Hotel, Airbnb o Destino..."></div><div class="input-wrapper"><label><i class="far fa-calendar-alt"></i> Fecha Ida</label><input type="date" id="fechaIda"></div><div class="input-wrapper" id="divFechaVuelta" style="display:none;"><label><i class="far fa-calendar-check"></i> F
