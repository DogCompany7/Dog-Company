<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Dog Company - Residencia Canina</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

  <style>
    /* Estilos generales */
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      color: #333;
      line-height: 1.6;
    }

    a {
      text-decoration: none;
    }

    /* Hero / Carrusel */
    .hero-slider {
      position: relative;
      height: 100vh;
      overflow: hidden;
    }

    .slide {
      position: absolute;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-position: center;
      opacity: 0;
      transition: opacity 1s ease-in-out;
    }

    .slide.active {
      opacity: 1;
    }

    .hero-text {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      color: white;
    }

    .hero-text h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3em;
      margin-bottom: 10px;
    }

    .hero-text p {
      font-size: 1.3em;
      margin-bottom: 20px;
    }

    .hero-text .btn {
      background: #25D366;
      color: white;
      padding: 15px 30px;
      border-radius: 30px;
      font-weight: bold;
    }

    /* Secciones */
    section {
      padding: 60px 20px;
      max-width: 900px;
      margin: auto;
    }

    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      text-align: center;
    }

    .service-box {
      padding: 20px;
      border-radius: 10px;
      background: #f5f5f5;
    }

    .highlight {
      text-align: center;
      font-size: 1.4em;
      font-weight: bold;
      margin: 40px 0;
    }

    footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 40px 20px;
    }

    footer .btn {
      background: #25D366;
      color: white;
      padding: 15px 30px;
      border-radius: 30px;
      font-weight: bold;
    }

    /* Botón WhatsApp minimalista */
    .whatsapp-icon {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 1000;
    }

    .whatsapp-icon img {
      width: 60px;
      display: block;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .hero-text h1 {
        font-size: 2em;
      }
      .hero-text p {
        font-size: 1.1em;
      }
    }
  </style>
</head>

<body>

<!-- Hero / Carrusel -->
<div class="hero-slider">
  <div class="slide active" style="background-image: url('https://images.unsplash.com/photo-1601758125946-6ec2ef64daf8');"></div>
  <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1583337130417-91ee189f1b9e');"></div>
  <div class="slide" style="background-image: url('https://images.unsplash.com/photo-1558788353-f76d92427f16');"></div>

  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado personalizado, entorno tranquilo y atención como en casa</p>
    <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">Reservar por WhatsApp</a>
  </div>
</div>

<script>
  // Carrusel automático
  let slides = document.querySelectorAll('.slide');
  let current = 0;
  setInterval(() => {
    slides[current].classList.remove('active');
    current = (current + 1) % slides.length;
    slides[current].classList.add('active');
  }, 5000);
</script>

<!-- Presentación -->
<section>
  <p>
    Somos una residencia canina de ambiente familiar donde los perros conviven en calma,
    con atención individual y respeto por sus ritmos.
  </p>
  <p>
    Aquí no hay jaulas ni estrés: hay presencia, cuidado y cariño real.
  </p>
</section>

<!-- Servicios -->
<section class="services">
  <div class="service-box">
    <h3>Alojamiento familiar</h3>
    <p>Convivencia en entorno seguro y tranquilo.</p>
  </div>
  <div class="service-box">
    <h3>Atención personalizada</h3>
    <p>Adaptada a cada perro y su carácter.</p>
  </div>
  <div class="service-box">
    <h3>Contacto directo</h3>
    <p>Comunicación constante por WhatsApp.</p>
  </div>
</section>

<!-- Destacado -->
<section class="highlight">
  Tu perro no es un número. <br>
  Es uno más en casa.
</section>

<!-- Footer -->
<footer>
  <p>Para reservas y consultas</p>
  <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">Escríbeme por WhatsApp</a>
</footer>

<!-- WhatsApp icon flotante -->
<a class="whatsapp-icon" href="https://wa.me/34TUNUMERO" target="_blank">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp">
</a>

</body>
</html>
