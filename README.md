<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<style>
body { margin:0; font-family:'Poppins', sans-serif; color:#333; line-height:1.6; }
a { text-decoration:none; }

/* Header fijo */
header {
  position: fixed; top:0; width:100%; z-index:999; display:flex;
  align-items:center; padding:15px 40px;
  background: rgba(255,255,255,0.95);
}
nav { margin-left:120px; }
nav a { margin-left:25px; color:#333; font-weight:600; }

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
.hero-slider { position:relative; height:60vh; overflow:hidden; margin-top:90px; }
.slide {
  position:absolute;
  width:100%;
  height:100%;
  background-size:cover;
  background-position:center;
  opacity:0;
  transition:opacity 1s;
}
.slide.active { opacity:1; }

.hero-overlay {
  position:absolute;
  width:100%;
  height:100%;
  background: rgba(0,0,0,0.35);
  top:0; left:0;
}

.hero-text {
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  text-align:center;
  color:white;
  z-index:2;
  max-width:70%;
}
.hero-text h1 {
  font-family:'Playfair Display', serif;
  font-size:2.2em;
  margin-bottom:10px;
}
.hero-text p {
  font-size:1.1em;
  margin-bottom:20px;
}
.hero-text .btn {
  background:#25D366;
  color:white;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
}

/* Presentación */
.presentacion {
  font-family:'Merriweather', serif;
  font-size:1.3em;
  color:#444;
  text-align:center;
  margin:50px 0;
}

/* Servicios */
section { padding:80px 20px; max-width:1000px; margin:auto; }

#servicios h2 {
  text-align:center;
  font-family:'Playfair Display', serif;
  font-size:2em;
  margin-bottom:40px;
  text-decoration:underline;
}

.services {
  display:flex;
  gap:20px;
  flex-wrap:wrap;
}

.service-box {
  flex:1 1 250px;
  padding:20px;
  border-radius:12px;
  background:#f9f9f9;
  box-shadow:0 4px 12px rgba(0,0,0,0.12);
  text-align:center;
}

.service-box h3 {
  font-family:'Playfair Display', serif;
  font-size:1.4em;
  margin-bottom:12px;
}

.service-box.horario-box { background:#FFF3B0; }

/* Footer */
footer {
  background:#222;
  color:white;
  text-align:center;
  padding:60px 20px;
}
footer .btn {
  background:#25D366;
  color:white;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
  display:inline-block;
  margin-top:15px;
}

/* WhatsApp flotante */
.whatsapp-container {
  position:fixed;
  bottom:20px;
  right:20px;
  z-index:1000;
}
.whatsapp-container img { width:50px; }
</style>
</head>

<body>

<header>
  <div class="logo-container">
    <div class="logo">Dog Company</div>
  </div>
  <nav>
    <a href="#servicios">Servicios</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>

<!-- CARRUSEL FUNCIONANDO -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('data:image/jpeg;base64,AAA_PRIMERA_IMAGEN');"></div>
  <div class="slide" style="background-image:url('data:image/jpeg;base64,AAA_SEGUNDA_IMAGEN');"></div>
  <div class="slide" style="background-image:url('data:image/jpeg;base64,AAA_TERCERA_IMAGEN');"></div>

  <div class="hero-overlay"></div>

  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado personalizado, entorno tranquilo y atención como en casa</p>
    <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">
      Reservar por WhatsApp
    </a>
  </div>
</div>

<script>
let slides=document.querySelectorAll('.slide');
let current=0;
setInterval(()=>{
  slides[current].classList.remove('active');
  current=(current+1)%slides.length;
  slides[current].classList.add('active');
},5000);
</script>

<section id="servicios">
  <h2>NUESTROS SERVICIOS</h2>
</section>

<footer id="contacto">
  <p>Ubicación: Alicante Centro</p>
  <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">
    Más información por WhatsApp
  </a>
</footer>

<div class="whatsapp-container">
  <a href="https://wa.me/34TUNUMERO" target="_blank">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg">
  </a>
</div>

</body>
</html>
