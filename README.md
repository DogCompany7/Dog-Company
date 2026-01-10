<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
  body { margin:0; font-family:'Poppins', sans-serif; color:#333; line-height:1.6; }
  a { text-decoration:none; }

  /* Header fijo */
  header {
    position: fixed; top:0; width:100%; z-index:999; display:flex;
    justify-content:space-between; align-items:center; padding:15px 40px;
    background: rgba(255,255,255,0.95);
  }

  nav a { margin-left:25px; color:#333; font-weight:600; transition: color 0.3s; }
  nav a:hover { color:#128C7E; }

  /* Logo con banner amarillo alineado a la izquierda */
  .logo-container {
    position: relative;
    display:inline-block;
    margin-left: -40px;
  }

  .logo-container::before {
    content:"";
    position:absolute;
    top:50%; transform:translateY(-50%);
    left:0;
    width:420px;
    height:100px;
    background-color:#F5C223;
    z-index:-1;
    border-bottom-right-radius:25px;
  }

  .logo {
    font-family:'Playfair Display', serif;
    font-size:2em;
    font-weight:bold;
    color:black;
    padding:25px 20px;
  }

  /* Hero / Carrusel */
  .hero-slider { position:relative; height:60vh; overflow:hidden; }
  .slide { position:absolute; width:100%; height:100%; background-size:cover; background-position:center; opacity:0; transition:opacity 1s; }
  .slide.active { opacity:1; }

  .hero-text {
    position:absolute; top:50%; left:50%;
    transform:translate(-50%,-50%);
    text-align:center; color:white; z-index:2;
    max-width:60%;
  }
  .hero-text h1 { font-family:'Playfair Display', serif; font-size:2.2em; margin-bottom:10px; text-shadow:2px 2px 8px rgba(0,0,0,0.6);}
  .hero-text p { font-size:1.1em; margin-bottom:20px; text-shadow:1px 1px 5px rgba(0,0,0,0.6);}
  .hero-text .btn { background:#25D366; color:white; padding:12px 28px; border-radius:30px; font-weight:bold; }

  /* Presentación */
  .presentacion { font-family:'Merriweather', serif; font-size:1.3em; color:#444; text-align:center; margin:50px 0; line-height:1.7; }

  /* Servicios */
  section { padding:80px 20px; max-width:1000px; margin:auto; }
  .services { 
    display:grid; 
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); 
    gap:20px; 
    margin-top:30px; 
  }
  .service-box { 
    padding:20px; 
    border-radius:12px; 
    background:#f9f9f9; 
    box-shadow:0 4px 12px rgba(0,0,0,0.12); 
    text-align:center; 
    transition:transform 0.3s, box-shadow 0.3s; 
    display:flex; 
    flex-direction:column; 
    justify-content:center; 
    height:230px; /* altura uniforme */
  }
  .service-box:hover { transform:translateY(-4px); box-shadow:0 8px 20px rgba(0,0,0,0.15); }
  .service-box h3 { font-family:'Playfair Display', serif; font-size:1.4em; margin-bottom:12px; }
  .service-box p { font-size:1em; margin-bottom:8px; }
  .precio-fijo { font-weight:bold; text-decoration:underline; }
  .horarios { color:red; font-size:1em; font-weight:bold; text-transform:uppercase; margin-top:10px; }

  #servicios h2 { 
    text-align:center; 
    font-family:'Playfair Display', serif; 
    font-size:2em; 
    margin-bottom:40px; 
    color:#333; 
    font-weight:bold; 
    text-decoration:underline;
  }

  .highlight { text-align:center; font-size:1.3em; font-weight:bold; margin:50px 0; }

  footer { background:#222; color:white; text-align:center; padding:60px 20px; }
  footer .ubicacion { font-size:1.2em; margin-bottom:10px; font-weight:bold; }
  footer .btn { background:#25D366; color:white; padding:12px 28px; border-radius:30px; font-weight:bold; text-decoration:none; margin-top:15px; display:inline-block; }

  /* WhatsApp flotante y botón consulta más pequeño */
  .whatsapp-container { position:fixed; bottom:20px; right:20px; z-index:1000; display:flex; flex-direction:column; align-items:flex-end; gap:10px; }
  .whatsapp-container a.btn-consulta { background:#128C7E; color:white; padding:8px 16px; border-radius:20px; font-weight:bold; font-size:0.9em; transition:transform 0.2s; }
  .whatsapp-container a.btn-consulta:hover { transform:scale(1.1); }
  .whatsapp-container img { width:50px; }

  @media(max-width:768px){
    .hero-text { left:50%; max-width:80%; text-align:center; }
    .hero-text h1{font-size:1.8em;}
    .hero-text p{font-size:1em;}
    .services{grid-template-columns:1fr; gap:15px;}
    .logo { font-size:1.8em; }
    .logo-container::before { width:300px; height:80px; }
    .logo-container { margin-left:-20px; }
    .service-box { height:auto; padding:18px; }
  }
</style>
</head>

<body>

<!-- Header -->
<header>
  <div class="logo-container">
    <div class="logo">Dog Company</div>
  </div>
  <nav>
    <a href="#servicios">Servicios</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>

<!-- Hero / Carrusel -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('https://images.unsplash.com/photo-1601758125946-6ec2ef64daf8');"></div>
  <div class="slide" style="background-image:url('https://images.unsplash.com/photo-1583337130417-91ee189f1b9e');"></div>
  <div class="slide" style="background-image:url('https://images.unsplash.com/photo-1558788353-f76d92427f16');"></div>

  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado personalizado, entorno tranquilo y atención como en casa</p>
    <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">Reservar por WhatsApp</a>
  </div>
</div>

<script>
  // Carrusel automático
  let slides=document.querySelectorAll('.slide');
  let current=0;
  setInterval(()=>{
    slides[current].classList.remove('active');
    current=(current+1)%slides.length;
    slides[current].classList.add('active');
  },5000);
</script>

<!-- Presentación -->
<section>
  <p class="presentacion">
    Somos una residencia canina de ambiente familiar donde los perros conviven en calma, con atención individual y respeto por sus ritmos.
  </p>
  <p class="presentacion">
    Aquí no hay jaulas ni estrés: hay presencia, cuidado y cariño real.
  </p>
</section>

<!-- Servicios -->
<section id="servicios">
  <h2>NUESTROS SERVICIOS</h2>
  <div class="services">
    <div class="service-box">
      <h3>Alojamiento Noche</h3>
      <p>Perro adulto: <strong>24€ / noche</strong></p>
      <p>Cachorros 1-12 meses y perritos con cuidados especiales: <strong>26€ / noche</strong></p>
    </div>

    <div class="service-box">
      <h3>Guardería de Día</h3>
      <p>Perro adulto: <strong>22€</strong></p>
      <p>Cachorros 1-12 meses y perritos con cuidados especiales: <strong>24€</strong></p>
      <p class="precio-fijo">Precio fijo hasta un máximo de 6 horas</p>
    </div>

    <div class="service-box">
      <p class="horarios">HORARIOS DE APERTURA: 10:00 A 20:00, LUNES A DOMINGO</p>
    </div>
  </div>
</section>

<!-- Destacado -->
<section class="highlight">
  Tu perro no es un número.<br>Es uno más en casa.
</section>

<!-- Footer -->
<footer id="contacto">
  <p class="ubicacion">Ubicación: Alicante Centro</p>
  <p>Contacto y reservas</p>
  <p>Email: info@dogcompany.com</p>
  <p>Teléfono: +34 TUNUMERO</p>
  <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">Más información por WhatsApp</a>
</footer>

<!-- WhatsApp flotante y consulta más pequeño -->
<div class="whatsapp-container">
  <a class="btn-consulta" href="https://wa.me/34TUNUMERO" target="_blank">Consulta disponibilidad</a>
  <a href="https://wa.me/34TUNUMERO" target="_blank">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
  </a>
</div>

</body>
</html>
