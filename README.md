<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
body { margin:0; font-family:'Poppins', sans-serif; color:#333; line-height:1.6; background:#fff; }
a { text-decoration:none; }

/* ================= HEADER ================= */
header {
  position: fixed; top:0; width:100%; z-index:999;
  display:flex; justify-content:space-between; align-items:center;
  padding:15px 40px; background: rgba(255,255,255,0.95);
}

nav a { margin-left:25px; color:#333; font-weight:600; }
nav a:hover { color:#128C7E; }

.logo-container { position: relative; display:inline-block; margin-left: -40px; }
.logo-container::before {
  content:""; position:absolute; top:0; left:0;
  width:420px; height:100px; background-color:#F5C223;
  z-index:-1; border-bottom-right-radius:25px;
}
.logo {
  font-family:'Playfair Display', serif;
  font-size:2em; font-weight:bold; color:black;
  padding:25px 20px;
}

/* ================= CARRUSEL (NO TOCADO) ================= */
.hero-slider { position:relative; height:65vh; overflow:hidden; }
.slide {
  position:absolute; width:100%; height:100%;
  background-size:cover; background-position:center;
  opacity:0; transition:opacity 1s;
}
.slide.active { opacity:1; }

.hero-text {
  position:absolute; top:50%; left:50%;
  transform:translate(-50%,-50%);
  text-align:center; color:white; z-index:2;
}
.hero-text h1 {
  font-family:'Playfair Display', serif;
  font-size:3em; text-shadow:2px 2px 8px rgba(0,0,0,0.6);
}
.hero-text p {
  font-size:1.3em; text-shadow:1px 1px 5px rgba(0,0,0,0.6);
}
.hero-text .btn {
  background:#25D366; color:white;
  padding:15px 35px; border-radius:30px; font-weight:bold;
}

/* ================= SECCIONES ================= */
section {
  padding:80px 20px;
  max-width:1000px;
  margin:auto;
  position:relative; /* necesario para decoración */
}

/* ===== Decoración patitas fondo ===== */
section::before {
  content:"";
  position:absolute;
  inset:0;
  background-image:url("data:image/svg+xml;utf8,\
<svg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 100 100'>\
<g fill='%23F5C223' fill-opacity='0.08'>\
<circle cx='30' cy='30' r='8'/>\
<circle cx='50' cy='20' r='8'/>\
<circle cx='70' cy='30' r='8'/>\
<ellipse cx='50' cy='60' rx='15' ry='18'/>\
</g></svg>");
  background-repeat:repeat;
  z-index:-1;
}

/* ================= PRESENTACIÓN ================= */
.presentacion {
  font-family:'Merriweather', serif;
  font-size:1.4em;
  text-align:center;
  margin:50px 0;
}

/* ================= SERVICIOS ================= */
.services {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
  gap:25px;
  margin-top:40px;
}

.service-box {
  padding:25px;
  border-radius:15px;
  background:#f9f9f9;
  box-shadow:0 6px 18px rgba(0,0,0,0.12);
  text-align:center;
}

.horarios {
  color:#F5C223;
  font-size:1.6em;
  font-weight:bold;
}

/* ================= FOOTER ================= */
footer {
  background:#222;
  color:white;
  text-align:center;
  padding:60px 20px;
  position:relative;
}

footer::before {
  content:"🐾 🐾 🐾";
  position:absolute;
  top:15px;
  left:50%;
  transform:translateX(-50%);
  opacity:0.2;
  font-size:1.5em;
}
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

<!-- TODO EL RESTO DE TU HTML VA EXACTAMENTE IGUAL -->
<!-- (carrusel, servicios, textos, horarios, footer…) -->

</body>
</html>
