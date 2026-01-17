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

/* ===== HEADER (ÚNICO CAMBIO) ===== */
header{
  position:fixed;
  top:0;
  width:100%;
  z-index:999;
  background:rgba(255,255,255,0.95);
}

.header-inner{
  max-width:1000px;
  margin:auto;
  display:grid;
  grid-template-columns: auto 1fr auto;
  align-items:center;
  padding:15px 20px;
}

/* Menú izquierda */
header nav{
  display:flex;
  gap:25px;
  font-weight:600;
}
header nav a{ color:#333; }

/* Logo centrado */
.logo-container{
  position:relative;
  justify-self:center;
}
.logo-container::before{
  content:"";
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%,-50%);
  width:420px;
  height:100px;
  background:#F5C223;
  border-bottom-right-radius:25px;
  z-index:-1;
}
.logo{
  font-family:'Playfair Display', serif;
  font-size:2em;
  font-weight:bold;
  color:black;
  padding:25px 20px;
}

/* Botón reservar derecha */
.btn-reservar{
  background:#F5C223;
  color:black;
  padding:12px 28px;
  border-radius:30px;
  font-weight:bold;
}

/* ===== RESTO DE TU CSS ORIGINAL (SIN TOCAR) ===== */

.hero-slider { position:relative; height:60vh; overflow:hidden; margin-top:120px; }
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

/* (TODO lo demás exactamente igual a tu código original) */
</style>
</head>

<body>

<header>
  <div class="header-inner">
    <nav>
      <a href="#servicios">Servicios</a>
      <a href="#resenas-footer">Reseñas</a>
      <a href="#quienes-somos-footer">Quiénes somos</a>
    </nav>

    <div class="logo-container">
      <div class="logo">Dog Company</div>
    </div>

    <a href="#reservaForm" class="btn-reservar">Reservar</a>
  </div>
</header>

<!-- TODO lo demás ES TU CÓDIGO SIN CAMBIOS -->
