<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<style>
body { margin:0; font-family:'Poppins', sans-serif; color:#333; line-height:1.6; scroll-behavior:smooth; }
a { text-decoration:none; }

/* HEADER MODIFICADO */
header {
  position: absolute; /* sobre el carrusel */
  top: 0;
  width: 100%;
  display: flex;
  align-items: flex-start; /* alineado arriba */
  justify-content: space-between;
  padding: 15px 40px;
  z-index: 999;
  background: transparent;
}

.nav-left {
  display: flex;
  gap: 25px;
  font-weight: 600;
  align-items: flex-start;
}

/* ELIMINADO EL LOGO DEL HEADER */

/* BOTÓN RESERVAS */
.reserva-btn-container {
  display: flex;
  align-items: flex-start;
}

.reserva-btn {
  display: inline-block;
  background-color: #F5C223;
  color: black;
  font-weight: bold;
  padding: 12px 25px;
  border-radius: 12px;
  text-decoration: none;
}

/* Hero / Carrusel */
.hero-slider { position:relative; height:60vh; overflow:hidden; margin-top:0; }

.hero-slider::before {
  content:"";
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%, -50%);
  width:420px;
  height:100px;
  background-color:#F5C223;
  z-index:1;
  border-radius:25px;
}

.slide {
  position:absolute;
  width:100%;
  height:100%;
  background-size:cover;
  background-position:center;
  opacity:0;
  transition:opacity 1s;
  z-index:0;
}
.slide.active { opacity:1; }

.hero-overlay {
  position:absolute;
  width:100%;
  height:100%;
  background: rgba(0,0,0,0.3);
  top:0; left:0;
  z-index:2;
}

.hero-text {
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  text-align:center;
  color:black;
  z-index:3;
  max-width:70%;
  font-family:'Playfair Display', serif;
  font-size:2em;
  font-weight:bold;
}

/* Botón dentro del carrusel */
.hero-text .btn {
  background:#F5C223;
  color:black;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
  text-decoration:none;
  display:inline-block;
  margin-top:20px;
}

/* resto del CSS sin cambios */
body { margin:0; font-family:'Poppins', sans-serif; color:#333; line-height:1.6; scroll-behavior:smooth; }
a { text-decoration:none; }

/* Presentación */
.presentacion {
  font-family:'Merriweather', serif;
  font-size:1.3em;
  color:#444;
  text-align:center;
  margin:50px 0;
  line-height:1.7;
}

/* Servicios */
section { padding:80px 20px; max-width:1000px; margin:auto; position:relative; }

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
  align-items:stretch;
  position:relative;
}

.service-box {
  flex:1 1 250px;
  padding:20px;
  border-radius:12px;
  background:#f9f9f9;
  box-shadow:0 4px 12px rgba(0,0,0,0.12);
  text-align:center;
  position:relative;
  z-index:1;
}

.service-box h3 {
  font-family:'Playfair Display', serif;
  font-size:1.4em;
  margin-bottom:12px;
  display:flex;
  align-items:center;
  justify-content:center;
  gap:8px;
}

.service-box p { font-size:1em; margin-bottom:8px; }
.precio-fijo { font-weight:bold; text-decoration:underline; }

.service-box.horario-box { background:#FFF3B0; }

.horarios {
  color:#333;
  font-size:1em;
  font-weight:bold;
  line-height:1.4;
}

/* Formulario */
.reserva-form {
  display:flex;
  flex-direction:column;
  gap:15px;
  margin-top:30px;
  max-width:400px;
  margin-left:auto;
  margin-right:auto;
}
.reserva-form input,
.reserva-form select,
.reserva-form button {
  padding:12px;
  border-radius:8px;
  border:1px solid #ccc;
  font-size:1em;
}
.reserva-form button {
  background:#25D366;
  color:white;
  font-weight:bold;
  border:none;
  cursor:pointer;
}

/* Destacado */
.highlight {
  text-align:center;
  font-size:1.3em;
  font-weight:bold;
  margin:50px 0;
}

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
  text-decoration:none;
  display:inline-block;
  margin-top:15px;
}

/* WhatsApp flotante */
.whatsapp-container {
  position:fixed;
  bottom:20px;
  right:20px;
  z-index:1000;
  display:flex;
  flex-direction:column;
  gap:10px;
}
.whatsapp-container img { width:50px; }

.testimonios {
  display:flex; flex-wrap:wrap; gap:20px; justify-content:flex-start;
}
.testimonio-box {
  flex:1 1 250px;
  background:#f9f9f9; padding:20px; border-radius:12px;
  box-shadow:0 4px 12px rgba(0,0,0,0.12); text-align:left;
}
.testimonio-box p { font-size:1em; margin-bottom:10px; color:#333; }
.testimonio-box .autor { font-weight:bold; color:#25D366; }

@media(max-width:768px){
  .hero-slider { height:45vh; }
  .services, .testimonios { flex-direction:column; }

  header {
    flex-direction: column;
    align-items: center;
    padding: 10px 20px;
  }
  .nav-left { margin-bottom: 10px; }
  .reserva-btn-container { margin-top: 10px; }
}
</style>
</head>

<body>

<header>
  <nav class="nav-left">
    <a href="#servicios">Servicios</a>
    <a href="#resenas-footer">Reseñas</a>
    <a href="#quienes-somos-footer">Quiénes somos</a>
  </nav>

  <div class="reserva-btn-container">
    <a class="reserva-btn" href="https://wa.me/34TUNUMERO" target="_blank">Reservas</a>
  </div>
</header>

<!-- 🔁 CARRUSEL -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/15b5e6d0237709b3b90e694c0a7ade6bb6a71a46/b4c1ee43-8999-4a6c-ac2f-dbf4386ec211.jpg');"></div>

  <div class="slide" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/162e09159041e7aa0d2f8fe0fb38146b550eaea7/06a11129-d358-454c-a15e-bc0f786909b6.jpg');"></div>

  <div class="slide" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/162e09159041e7aa0d2f8fe0fb38146b550eaea7/fff61fbc-7603-43fe-8133-9e453dd67e64.jpg');"></div>

  <div class="hero-overlay"></div>

  <div class="hero-text">
    Dog Company
    <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">
      Reservar por WhatsApp
    </a>
  </div>
</div>

<script>
document.getElementById('reservaForm').addEventListener('submit', function(e){
  e.preventDefault();
  const f=e.target;
  const msg=`Reserva Dog Company:%0ANombre: ${f.nombre.value}%0ATeléfono: ${f.telefono.value}%0APerro: ${f.mascota.value}%0ADescripción: ${f.descripcion.value}%0AServicio: ${f.servicio.value}%0AFecha: ${f.fecha.value}`;
  window.open(`https://wa.me/34TUNUMERO?text=${msg}`,'_blank');
});

let slides=document.querySelectorAll('.slide');
let current=0;
setInterval(()=>{ slides[current].classList.remove('active'); current=(current+1)%slides.length; slides[current].classList.add('active'); },5000);
</script>

<!-- resto de tu código permanece igual -->
