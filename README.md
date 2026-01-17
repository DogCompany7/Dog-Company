<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
  font-family:Poppins, sans-serif;
  background:#fff;
  color:#111;
}

/* CONTENEDOR GENERAL */
.wrapper{
  max-width:1200px;
  margin:0 auto;
  padding:0 20px;
}

/* HEADER */
header{
  border-bottom:1px solid #eee;
}
.header-inner{
  display:grid;
  grid-template-columns:1fr auto 1fr;
  align-items:center;
  height:80px;
}

/* MENÚ IZQUIERDA */
nav ul{
  list-style:none;
  display:flex;
  gap:25px;
}
nav a{
  text-decoration:none;
  color:#111;
  font-weight:500;
}

/* LOGO CENTRO */
.logo-wrap{
  display:flex;
  justify-content:center;
}
.logo{
  background:#FFD600;
  padding:10px 28px;
  border-radius:40px;
  font-weight:700;
  font-size:20px;
}

/* BOTÓN RESERVAR DERECHA */
.reserve-wrap{
  display:flex;
  justify-content:flex-end;
}
.reserve-btn{
  background:#FFD600;
  padding:12px 26px;
  border-radius:40px;
  font-weight:600;
  text-decoration:none;
  color:#111;
}

/* CARRUSEL */
.carousel{
  margin:40px auto;
  overflow:hidden;
  border-radius:18px;
}
.carousel img{
  width:100%;
  display:block;
}

/* SECCIONES */
section{
  margin:80px 0;
  text-align:center;
}
section h2{
  font-size:28px;
  margin-bottom:30px;
}

/* SERVICIOS */
.services{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:30px;
}
.service{
  border:1px solid #eee;
  padding:30px;
  border-radius:18px;
}

/* RESEÑAS */
.reviews{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
  gap:30px;
}
.review{
  background:#f9f9f9;
  padding:25px;
  border-radius:18px;
}

/* FORMULARIO */
form{
  max-width:500px;
  margin:0 auto;
  display:flex;
  flex-direction:column;
  gap:15px;
}
input, textarea{
  padding:14px;
  border-radius:12px;
  border:1px solid #ccc;
  font-family:inherit;
}
.form-actions{
  display:flex;
  gap:15px;
  justify-content:center;
}
.btn-black{
  background:#000;
  color:#000;
  border:none;
  padding:14px 22px;
  border-radius:30px;
  font-weight:600;
  background:#fff;
  border:2px solid #000;
}
.btn-yellow{
  background:#FFD600;
  color:#111;
  border:none;
  padding:14px 22px;
  border-radius:30px;
  font-weight:600;
}

/* FOOTER */
footer{
  border-top:1px solid #eee;
  padding:30px 0;
  text-align:center;
  font-weight:600;
}
</style>
</head>

<body>

<header>
  <div class="wrapper header-inner">
    <nav>
      <ul>
        <li><a href="#servicios">Servicios</a></li>
        <li><a href="#quienes">Quiénes somos</a></li>
        <li><a href="#resenas">Reseñas</a></li>
      </ul>
    </nav>

    <div class="logo-wrap">
      <div class="logo">Dog Company</div>
    </div>

    <div class="reserve-wrap">
      <a href="#reserva-formulario" class="reserve-btn">Reservar</a>
    </div>
  </div>
</header>

<div class="wrapper">
  <div class="carousel">
    <img src="https://images.unsplash.com/photo-1601758125946-6ec2ef64daf8" alt="Perros felices">
  </div>

  <section id="servicios">
    <h2>Servicios</h2>
    <div class="services">
      <div class="service">Residencia canina</div>
      <div class="service">Guardería de día</div>
      <div class="service">Paseos personalizados</div>
    </div>
  </section>

  <section id="quienes">
    <h2>Quiénes somos</h2>
    <p>Cuidado familiar, consciente y respetuoso. Aquí los perros se sienten en casa.</p>
  </section>

  <section id="resenas">
    <h2>Reseñas</h2>
    <div class="reviews">
      <div class="review">“Mi perro feliz como nunca.”</div>
      <div class="review">“Confianza total, repetiremos.”</div>
    </div>
  </section>

  <section id="reserva-formulario">
    <h2>Reserva</h2>
    <form>
      <input type="text" placeholder="Nombre">
      <input type="email" placeholder="Email">
      <textarea placeholder="Mensaje"></textarea>
      <div class="form-actions">
        <button class="btn-black" type="button">Consulta disponibilidad</button>
        <button class="btn-yellow" type="submit">Haz tu reserva</button>
      </div>
    </form>
  </section>
</div>

<footer>
  Dog Company
</footer>

</body>
</html>
