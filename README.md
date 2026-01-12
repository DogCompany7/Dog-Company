<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<style>
body{margin:0;font-family:'Poppins',sans-serif;color:#333}
header{position:fixed;top:0;width:100%;z-index:999;display:flex;justify-content:space-between;align-items:center;padding:15px 40px;background:rgba(255,255,255,.95)}
.logo-container{position:relative;margin-left:-40px}
.logo-container::before{content:"";position:absolute;top:50%;transform:translateY(-50%);width:380px;height:90px;background:#F5C223;border-bottom-right-radius:25px;z-index:-1}
.logo{font-family:'Playfair Display',serif;font-size:2em;font-weight:bold;padding:20px}
nav a{margin-left:25px;color:#333;font-weight:600}
.hero-slider{position:relative;height:55vh;overflow:hidden;margin-top:90px}
.slide{position:absolute;width:100%;height:100%;background-size:cover;background-position:center;opacity:0;transition:opacity 1s}
.slide.active{opacity:1}
.hero-overlay{position:absolute;inset:0;background:rgba(0,0,0,.35)}
.hero-text{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);text-align:center;color:white;z-index:2}
.hero-text h1{font-family:'Playfair Display',serif;font-size:2.2em}
.hero-text .btn{background:#25D366;color:white;padding:12px 30px;border-radius:30px;font-weight:bold}
section{padding:80px 20px;max-width:1000px;margin:auto}
.services{display:flex;gap:20px;flex-wrap:wrap}
.service-box{flex:1 1 250px;background:#f9f9f9;border-radius:12px;padding:20px;box-shadow:0 4px 12px rgba(0,0,0,.12);text-align:center}
.horario-box{background:#FFF3B0}
.reserva-form{max-width:420px;margin:40px auto;display:flex;flex-direction:column;gap:15px}
.reserva-form input,.reserva-form select,.reserva-form button{padding:12px;border-radius:8px;border:1px solid #ccc}
.reserva-form button{background:#25D366;color:white;font-weight:bold;border:none}
footer{background:#222;color:white;text-align:center;padding:60px 20px}
</style>
</head>

<body>

<header>
  <div class="logo-container"><div class="logo">Dog Company</div></div>
  <nav><a href="#servicios">Servicios</a><a href="#contacto">Contacto</a></nav>
</header>

<div class="hero-slider">
  <div class="slide active" style="background-image:url('data:image/jpeg;base64,{{IMG1}}')"></div>
  <div class="slide" style="background-image:url('data:image/jpeg;base64,{{IMG2}}')"></div>
  <div class="slide" style="background-image:url('data:image/jpeg;base64,{{IMG3}}')"></div>
  <div class="hero-overlay"></div>
  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado real, presencia y calma</p>
    <a class="btn" href="https://wa.me/34TUNUMERO">Reservar por WhatsApp</a>
  </div>
</div>

<script>
let slides=document.querySelectorAll('.slide'),c=0;
setInterval(()=>{slides[c].classList.remove('active');c=(c+1)%slides.length;slides[c].classList.add('active')},5000);
</script>

<section id="servicios">
  <div class="services">
    <div class="service-box"><h3>Alojamiento Noche</h3><p>24€ / noche</p></div>
    <div class="service-box"><h3>Guardería de Día</h3><p>22€</p></div>
    <div class="service-box horario-box"><h3>Horarios</h3><p>10:00h – 20:00h<br>Lunes a Domingo</p></div>
  </div>

  <form id="reservaForm" class="reserva-form">
    <input name="nombre" placeholder="Tu nombre" required>
    <input name="telefono" placeholder="Teléfono" required>
    <input name="mascota" placeholder="Nombre del perro" required>
    <input name="descripcion" placeholder="Descripción del perro" required>
    <select name="servicio"><option>Alojamiento</option><option>Guardería</option></select>
    <input type="date" name="fecha" required>
    <button>Enviar por WhatsApp</button>
  </form>
</section>

<footer id="contacto">
  <p>Alicante Centro</p>
</footer>

<script>
document.getElementById('reservaForm').onsubmit=e=>{
e.preventDefault();
const f=e.target;
const msg=`Reserva:%0A${f.nombre.value}%0A${f.telefono.value}%0A${f.mascota.value}%0A${f.descripcion.value}`;
window.open(`https://wa.me/34TUNUMERO?text=${msg}`,'_blank');
}
</script>

</body>
</html>
