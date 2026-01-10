<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<!-- Font Awesome para iconos -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

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
  .hero-overlay { position:absolute; width:100%; height:100%; background: rgba(0,0,0,0.3); top:0; left:0; }

  .hero-text {
    position:absolute; top:50%; left:50%;
    transform:translate(-50%,-50%);
    text-align:center; color:white; z-index:2;
    max-width:70%;
  }
  .hero-text h1 { font-family:'Playfair Display', serif; font-size:2.2em; margin-bottom:10px; text-shadow:2px 2px 8px rgba(0,0,0,0.6);}
  .hero-text p { font-size:1.1em; margin-bottom:20px; text-shadow:1px 1px 5px rgba(0,0,0,0.6);}
  .hero-text .btn { background:#25D366; color:white; padding:12px 28px; border-radius:30px; font-weight:bold; }

  /* Presentación */
  .presentacion { font-family:'Merriweather', serif; font-size:1.3em; color:#444; text-align:center; margin:50px 0; line-height:1.7; }

  /* Servicios */
  section { padding:80px 20px; max-width:1000px; margin:auto; }
  #servicios h2 { 
    text-align:center; 
    font-family:'Playfair Display', serif; 
    font-size:2em; 
    margin-bottom:40px; 
    color:#333; 
    font-weight:bold; 
    text-decoration:underline;
  }
  .services { 
    display:flex; 
    gap:20px; 
    margin-top:30px; 
    align-items:stretch; 
    flex-wrap:wrap;
  }
  .service-box { 
    flex:1 1 250px; 
    padding:20px; 
    border-radius:12px; 
    background:#f9f9f9; 
    box-shadow:0 4px 12px rgba(0,0,0,0.12); 
    text-align:center; 
    transition:transform 0.3s, box-shadow 0.3s; 
    display:flex; 
    flex-direction:column; 
    justify-content:flex-start; 
  }
  .service-box:hover { transform:translateY(-4px); box-shadow:0 8px 20px rgba(0,0,0,0.15); }
  .service-box h3 { font-family:'Playfair Display', serif; font-size:1.4em; margin-bottom:12px; display:flex; align-items:center; justify-content:center; gap:8px; }
  .service-box p { font-size:1em; margin-bottom:8px; }
  .precio-fijo { font-weight:bold; text-decoration:underline; }

  /* Horarios con fondo amarillo suave */
  .service-box.horario-box { background:#FFF3B0; }
  .horarios { 
    color:#333; 
    font-size:1em; 
    font-weight:bold; 
    text-align:center;
    line-height:1.4;
    margin-top:10px; 
  }

  /* Formulario WhatsApp */
  .reserva-form { 
    display:flex; flex-direction:column; gap:15px; margin-top:30px; 
    max-width:400px; margin:auto; 
  }
  .reserva-form input, .reserva-form select, .reserva-form button {
    padding:12px; border-radius:8px; border:1px solid #ccc; font-size:1em;
  }
  .reserva-form button { background:#25D366; color:white; font-weight:bold; border:none; cursor:pointer; transition:transform 0.2s; }
  .reserva-form button:hover { transform:scale(1.05); }

  /* Destacado */
  .highlight { text-align:center; font-size:1.3em; font-weight:bold; margin:50px 0; }

  /* Footer */
  footer { background:#222; color:white; text-align:center; padding:60px 20px; }
  footer .ubicacion { font-size:1.2em; margin-bottom:10px; font-weight:bold; }
  footer .btn { background:#25D366; color:white; padding:12px 28px; border-radius:30px; font-weight:bold; text-decoration:none; margin-top:15px; display:inline-block; }

  /* WhatsApp flotante */
  .whatsapp-container { position:fixed; bottom:20px; right:20px; z-index:1000; display:flex; flex-direction:column; align-items:flex-end; gap:10px; }
  .whatsapp-container a.btn-consulta { background:#128C7E; color:white; padding:8px 16px; border-radius:20px; font-weight:bold; font-size:0.9em; transition:transform 0.2s; }
  .whatsapp-container a.btn-consulta:hover { transform:scale(1.1); }
  .whatsapp-container img { width:50px; }

  @media(max-width:768px){
    .hero-text { left:50%; max-width:80%; text-align:center; }
    .hero-text h1{font-size:1.8em;}
    .hero-text p{font-size:1em;}
    .services{flex-direction:column; gap:15px;}
    .logo { font-size:1.8em; }
    .logo-container::before { width:300px; height:80px; }
    .logo-container { margin-left:-20px; }
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
  <div class="hero-overlay"></div>

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
      <h3><i class="fa-solid fa-bed"></i> Alojamiento Noche</h3>
      <p>Perro adulto: <strong>24€ / noche</strong></p>
      <p>Cachorros 1-12 meses y perritos con cuidados especiales: <strong>26€ / noche</strong></p>
    </div>

    <div class="service-box">
      <h3><i class="fa-solid fa-sun"></i> Guardería de Día</h3>
      <p>Perro adulto: <strong>22€</strong></p>
      <p>Cachorros 1-12 meses y perritos con cuidados especiales: <strong>24€</strong></p>
      <p class="precio-fijo">Precio fijo hasta un máximo de 6 horas</p>
    </div>

    <div class="service-box horario-box">
      <h3><i class="fa-regular fa-clock"></i> Horarios</h3>
      <p class="horarios">
        Horario de atención al cliente:<br>
        10:00h a 20:00h, de lunes a domingo<br><br>
        Horario de entrada y salida de reservas:<br>
        10:00h a 20:00h
      </p>
    </div>
  </div>

  <!-- Formulario de reserva WhatsApp -->
  <form id="reservaForm" class="reserva-form">
    <input type="text" name="nombre" placeholder="Tu nombre" required>
    <input type="text" name="telefono" placeholder="Tu teléfono" required>
    <input type="text" name="mascota" placeholder="Nombre de tu perro" required>
    <input type="text" name="descripcion" placeholder="Descripción de tu perro" required>
    <select name="servicio" required>
      <option value="Alojamiento Noche">Alojamiento Noche</option>
      <option value="Guardería de Día">Guardería de Día</option>
    </select>
    <input type="date" name="fecha" required>
    <button type="submit">Enviar por WhatsApp</button>
  </form>

  <script>
    document.getElementById('reservaForm').addEventListener('submit', function(e){
      e.preventDefault();
      const form = e.target;
      const nombre = form.nombre.value;
      const telefono = form.telefono.value;
      const mascota = form.mascota.value;
      const descripcion = form.descripcion.value;
      const servicio = form.servicio.value;
      const fecha = form.fecha.value;

      const mensaje = `Reserva Dog Company:%0ANombre: ${nombre}%0ATeléfono: ${telefono}%0ANombre del perro: ${mascota}%0ADescripción: ${descripcion}%0AServicio: ${servicio}%0AFecha: ${fecha}`;
      window.open(`https://wa.me/34TUNUMERO?text=${mensaje}`, '_blank');
    });
  </script>
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

<!-- WhatsApp flotante -->
<div class="whatsapp-container">
  <a class="btn-consulta" href="https://wa.me/34TUNUMERO" target="_blank">Consulta disponibilidad</a>
  <a href="https://wa.me/34TUNUMERO" target="_blank">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
  </a>
</div>

</body>
</html>
