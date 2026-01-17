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
a { text-decoration:none; color:#333; }

/* ===== HEADER CORREGIDO ===== */
.header-fixed{
  position:fixed;
  top:0;
  width:100%;
  height:90px;
  background:rgba(255,255,255,0.95);
  display:grid;
  grid-template-columns: 1fr auto 1fr;
  align-items:center;
  z-index:999;
}

/* izquierda */
.nav-left{
  display:flex;
  gap:25px;
  margin-left:40px;
  font-weight:600;
}

/* centro real */
.logo-wrapper{
  position:relative;
  justify-self:center;
}
.logo-wrapper::before{
  content:"";
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  width:420px;
  height:90px;
  background:#F5C223;
  border-bottom-right-radius:25px;
  z-index:-1;
}
.logo{
  font-family:'Playfair Display', serif;
  font-size:2em;
  font-weight:bold;
  color:black;
  padding:25px 40px;
}

/* derecha */
.nav-right{
  justify-self:end;
  margin-right:40px;
}
.btn-reservas{
  background:#F5C223;
  color:black;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
}

/* ===== HERO ===== */
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
  background: rgba(0,0,0,0.3);
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
  text-shadow:2px 2px 8px rgba(0,0,0,0.6);
}
.hero-text p {
  font-size:1.1em;
  margin-bottom:20px;
  text-shadow:1px 1px 5px rgba(0,0,0,0.6);
}
.hero-text .btn {
  background:#25D366;
  color:white;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
}

/* resto del CSS SIN CAMBIOS */
.presentacion {
  font-family:'Merriweather', serif;
  font-size:1.3em;
  color:#444;
  text-align:center;
  margin:50px 0;
  line-height:1.7;
}

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

.service-box.horario-box { background:#FFF3B0; }

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
}

.highlight {
  text-align:center;
  font-size:1.3em;
  font-weight:bold;
  margin:50px 0;
}

footer {
  background:#222;
  color:white;
  text-align:center;
  padding:60px 20px;
}

.whatsapp-container {
  position:fixed;
  bottom:20px;
  right:20px;
}
.whatsapp-container img { width:50px; }

@media(max-width:768px){
  .hero-slider { height:45vh; }
}
</style>
</head>

<body>

<header class="header-fixed">
  <nav class="nav-left">
    <a href="#servicios">Servicios</a>
    <a href="#resenas-footer">Reseñas</a>
    <a href="#quienes-somos-footer">Quiénes somos</a>
  </nav>

  <div class="logo-wrapper">
    <div class="logo">Dog Company</div>
  </div>

  <div class="nav-right">
    <a href="#reservaForm" class="btn-reservas">Reservas</a>
  </div>
</header>

<!-- CARRUSEL -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/15b5e6d0237709b3b90e694c0a7ade6bb6a71a46/b4c1ee43-8999-4a6c-ac2f-dbf4386ec211.jpg');"></div>
  <div class="slide" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/162e09159041e7aa0d2f8fe0fb38146b550eaea7/06a11129-d358-454c-a15e-bc0f786909b6.jpg');"></div>
  <div class="slide" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/162e09159041e7aa0d2f8fe0fb38146b550eaea7/fff61fbc-7603-43fe-8133-9e453dd67e64.jpg');"></div>

  <div class="hero-overlay"></div>

  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado personalizado, entorno tranquilo y atención como en casa</p>
    <a class="btn" href="https://wa.me/34TUNUMERO" target="_blank">Reservar por WhatsApp</a>
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

</body>
</html>
