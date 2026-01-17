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

/* HEADER */
header{
  position:fixed;
  top:0;
  width:100%;
  z-index:999;
  background:rgba(255,255,255,0.95);
  height:90px;
  display:flex;
  align-items:center;
}

/* NAV IZQUIERDA */
header nav{
  display:flex;
  gap:25px;
  font-weight:600;
  margin-left:40px;
}

/* LOGO CENTRADO CON FONDO AMARILLO */
.logo-container{
  position:absolute;
  left:50%;
  transform:translateX(-50%);
}
.logo-container::before{
  content:"";
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  width:420px;
  height:90px;
  background:#F5C223;
  border-bottom-right-radius:30px;
  z-index:-1;
}
.logo{
  font-family:'Playfair Display', serif;
  font-size:2em;
  font-weight:bold;
  color:black;
  padding:25px 40px;
}

/* BOTÓN RESERVAS DERECHA */
.btn-reservar{
  margin-left:auto;
  margin-right:40px;
  background:#F5C223;
  color:black;
  padding:12px 30px;
  border-radius:30px;
  font-weight:bold;
}

/* HERO */
.hero-slider{ position:relative; height:60vh; overflow:hidden; margin-top:90px; }
.slide{
  position:absolute;
  width:100%;
  height:100%;
  background-size:cover;
  background-position:center;
  opacity:0;
  transition:opacity 1s;
}
.slide.active{ opacity:1; }
.hero-overlay{
  position:absolute;
  width:100%;
  height:100%;
  background:rgba(0,0,0,0.3);
}
.hero-text{
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  text-align:center;
  color:white;
  z-index:2;
}
.hero-text h1{
  font-family:'Playfair Display', serif;
  font-size:2.2em;
}
.hero-text .btn{
  background:#25D366;
  color:white;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
}

/* FORMULARIO */
.reserva-form{
  display:flex;
  flex-direction:column;
  gap:15px;
  max-width:400px;
  margin:30px auto 0;
}
.reserva-form input,
.reserva-form select,
.reserva-form button{
  padding:12px;
  border-radius:8px;
  border:1px solid #ccc;
}
.reserva-form button{
  background:#25D366;
  color:white;
  font-weight:bold;
  border:none;
  cursor:pointer;
}

/* TESTIMONIOS */
.testimonios{
  display:flex;
  gap:20px;
  flex-wrap:wrap;
  justify-content:center;
}
.testimonio-box{
  flex:1 1 250px;
  background:#f9f9f9;
  padding:20px;
  border-radius:12px;
  box-shadow:0 4px 12px rgba(0,0,0,0.12);
}

/* FOOTER */
footer{
  background:#222;
  color:white;
  text-align:center;
  padding:60px 20px;
}

/* RESPONSIVE */
@media(max-width:768px){
  header{
    flex-direction:column;
    height:auto;
    padding:10px 0;
  }
  header nav{
    margin:10px 0;
  }
  .btn-reservar{
    margin:10px 0;
  }
  .logo-container::before{
    width:300px;
  }
}
</style>
</head>

<body>

<header>
  <nav>
    <a href="#servicios">Servicios</a>
    <a href="#resenas-footer">Reseñas</a>
    <a href="#quienes-somos-footer">Quiénes somos</a>
  </nav>

  <div class="logo-container">
    <div class="logo">Dog Company</div>
  </div>

  <a href="#reserva-formulario" class="btn-reservar">Reservas</a>
</header>

<!-- HERO -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('https://raw.githubusercontent.com/DogCompany7/Dog-Company/15b5e6d0237709b3b90e694c0a7ade6bb6a71a46/b4c1ee43-8999-4a6c-ac2f-dbf4386ec211.jpg');"></div>
  <div class="hero-overlay"></div>
  <div class="hero-text">
    <h1>Dog Company</h1>
    <p>Cuidado personalizado, entorno tranquilo y atención como en casa</p>
    <a class="btn" href="https://wa.me/34TUNUMERO">Reservar por WhatsApp</a>
  </div>
</div>

<!-- FORMULARIO -->
<section id="reserva-formulario">
  <h2 style="text-align:center;">
    <span style="color:#000;">Consulta disponibilidad</span>
    <span style="color:#F5C223;">Haz tu reserva</span>
  </h2>

  <form class="reserva-form">
    <input type="text" placeholder="Tu nombre" required>
    <input type="text" placeholder="Tu teléfono" required>
    <input type="text" placeholder="Nombre de tu perro" required>
    <input type="date" required>
    <button>Enviar por WhatsApp</button>
  </form>
</section>

<footer>
  <p>Ubicación: Alicante Centro</p>
</footer>

</body>
</html>
