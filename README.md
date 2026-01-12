<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<style>
body { margin:0; font-family:'Poppins', sans-serif; color:#333; }
a { text-decoration:none; }

/* DECORACIONES DE FONDO */
body::before{
  content:"";
  position:fixed;
  top:10%;
  left:5%;
  width:120px;
  height:120px;
  background:url('https://www.svgrepo.com/show/50205/dog-paw.svg') no-repeat center/contain;
  opacity:0.15;
  pointer-events:none;
}
body::after{
  content:"";
  position:fixed;
  bottom:15%;
  right:5%;
  width:150px;
  height:150px;
  background:url('https://www.svgrepo.com/show/7200426/dog-paw-prints.svg') no-repeat center/contain;
  opacity:0.15;
  pointer-events:none;
}

/* HEADER */
header{
  position:fixed; top:0; width:100%; z-index:999;
  display:flex; justify-content:space-between; align-items:center;
  padding:15px 40px; background:rgba(255,255,255,0.95);
}
nav a{ margin-left:25px; color:#333; font-weight:600; }

.logo-container{ position:relative; margin-left:-40px; }
.logo-container::before{
  content:""; position:absolute; top:50%; transform:translateY(-50%);
  width:380px; height:90px; background:#F5C223;
  border-bottom-right-radius:25px; z-index:-1;
}
.logo{
  font-family:'Playfair Display', serif;
  font-size:2em; font-weight:bold; padding:20px;
}

/* HERO */
.hero-slider{ position:relative; height:55vh; overflow:hidden; margin-top:90px; }
.slide{
  position:absolute; width:100%; height:100%;
  background-size:cover; background-position:center;
  opacity:0; transition:opacity 1s;
}
.slide.active{ opacity:1; }

.hero-overlay{
  position:absolute; inset:0;
  background:rgba(0,0,0,0.35);
}

.hero-text{
  position:absolute; top:50%; left:50%;
  transform:translate(-50%,-50%);
  text-align:center; color:white; z-index:2;
}
.hero-text h1{
  font-family:'Playfair Display', serif;
  font-size:2.2em; margin-bottom:10px;
}
.hero-text p{ font-size:1.1em; margin-bottom:20px; }
.hero-text .btn{
  background:#25D366; color:white;
  padding:12px 30px; border-radius:30px;
  font-weight:bold;
}

/* SECCIONES */
section{ padding:80px 20px; max-width:1000px; margin:auto; }
.presentacion{
  font-family:'Merriweather', serif;
  font-size:1.3em; text-align:center; color:#444;
}

/* SERVICIOS */
.services{
  display:flex; gap:20px; flex-wrap:wrap; align-items:stretch;
}
.service-box{
  flex:1 1 250px;
  background:#f9f9f9;
  border-radius:12px;
  padding:20px;
  box-shadow:0 4px 12px rgba(0,0,0,.12);
  text-align:center;
}
.service-box h3{
  font-family:'Playfair Display', serif;
  display:flex; justify-content:center; gap:8px;
}
.precio-fijo{ font-weight:bold; text-decoration:underline; }

.horario-box{ background:#FFF3B0; }
.horarios{ font-weight:bold; line-height:1.4; }

/* FORM */
.reserva-form{
  max-width:420px; margin:40px auto 0;
  display:flex; flex-direction:column; gap:15px;
}
.reserva-form input,
.reserva-form select,
.reserva-form button{
  padding:12px; border-radius:8px; border:1px solid #ccc;
}
.reserva-form button{
  background:#25D366; color:white; font-weight:bold; border:none;
}

/* FOOTER */
footer{
  background:#222; color:white;
  text-align:center; padding:60px 20px;
}
footer .btn{
  background:#25D366; color:white;
  padding:12px 28px; border-radius:30px;
  display:inline-block; margin-top:15px;
}

/* WHATSAPP */
.whatsapp-container{
  position:fixed; bottom:20px; right:20px;
  display:flex; flex-direction:column; gap:10px;
}
.whatsapp-container img{ width:50px; }

@media(max-width:768px){
  .hero-slider{ height:45vh; }
  .services{ flex-direction:column; }
}
</style>
</head>

<body>

<header>
  <div class="logo-container"><div class="logo">Dog Company</div></div>
  <nav>
    <a href="#servicios">Servicios</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>

<!-- HERO CON TUS IMÁGENES -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('06a11129-d358-454c-a15e-bc0f786909b6.jpg')"></div>
  <div class="slide" style="background-image:url('b4c1ee43-8999-4a6c-ac2f-dbf4386ec211.jpg')"></div>
  <div class="slide" style="background-image:url('fff61fbc-7603-43fe-8133-9e453dd67e64.jpg')"></div>

  <div class="hero-overlay"></div>

  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado real, presencia y calma</p>
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

<section>
  <p class="presentacion">
    Residencia canina de ambiente familiar, sin jaulas ni estrés.
  </p>
</section>

<section id="servicios">
  <div class="services">
    <div class="service-box">
      <h3><i class="fa-solid fa-bed"></i> Alojamiento Noche</h3>
      <p>Adulto: <strong>24€ / noche</strong></p>
      <p>Cachorros / especiales: <strong>26€</strong></p>
    </div>

    <div class="service-box">
      <h3><i class="fa-solid fa-sun"></i> Guardería de Día</h3>
      <p>Adulto: <strong>22€</strong></p>
      <p>Cachorros / especiales: <strong>24€</strong></p>
      <p class="precio-fijo">Máx. 6h</p>
    </div>

    <div class="service-box horario-box">
      <h3><i class="fa-regular fa-clock"></i> Horarios</h3>
      <p class="horarios">
        Atención al cliente<br>
        10:00h a 20:00h<br><br>
        Entradas y salidas<br>
        10:00h a 20:00h
      </p>
    </div>
  </div>

  <form id="reservaForm" class="reserva-form">
    <input type="text" name="nombre" placeholder="Tu nombre" required>
    <input type="text" name="telefono" placeholder="Tu teléfono" required>
    <input type="text" name="mascota" placeholder="Nombre de tu perro" required>
    <input type="text" name="descripcion" placeholder="Descripción de tu perro" required>
    <select name="servicio" required>
      <option>Alojamiento Noche</option>
      <option>Guardería de Día</option>
    </select>
    <input type="date" name="fecha" required>
    <button type="submit">Enviar por WhatsApp</button>
  </form>
</section>

<footer id="contacto">
  <p>Alicante Centro</p>
  <a class="btn" href="https://wa.me/34TUNUMERO">WhatsApp</a>
</footer>

<div class="whatsapp-container">
  <a href="https://wa.me/34TUNUMERO"><img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg"></a>
</div>

<script>
document.getElementById('reservaForm').addEventListener('submit',function(e){
  e.preventDefault();
  const f=e.target;
  const msg=`Reserva Dog Company:%0ANombre: ${f.nombre.value}%0ATeléfono: ${f.telefono.value}%0APerro: ${f.mascota.value}%0ADescripción: ${f.descripcion.value}%0AServicio: ${f.servicio.value}%0AFecha: ${f.fecha.value}`;
  window.open(`https://wa.me/34TUNUMERO?text=${msg}`,'_blank');
});
</script>

</body>
</html>
