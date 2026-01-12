<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Dog Company - Residencia Canina</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700&family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">

<style>
body{margin:0;font-family:'Poppins',sans-serif;color:#333;line-height:1.6}
a{text-decoration:none}

/* DECORACIONES DE HUELLAS */
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

/* RESTO IGUAL */
header{
position:fixed;top:0;width:100%;z-index:999;
display:flex;justify-content:space-between;align-items:center;
padding:15px 40px;background:rgba(255,255,255,.95)
}
nav a{margin-left:25px;color:#333;font-weight:600}
nav a:hover{color:#128C7E}

.logo-container{position:relative;display:inline-block;margin-left:-40px}
.logo-container::before{
content:"";position:absolute;top:0;left:0;
width:420px;height:100px;background:#F5C223;
border-bottom-right-radius:25px;z-index:-1
}
.logo{
font-family:'Playfair Display',serif;
font-size:2em;font-weight:bold;
padding:25px 20px;color:black
}

/* CARRUSEL */
.hero-slider{position:relative;height:65vh;overflow:hidden}
.slide{
position:absolute;width:100%;height:100%;
background-size:cover;background-position:center;
opacity:0;transition:opacity 1s
}
.slide.active{opacity:1}

.hero-text{
position:absolute;top:50%;left:50%;
transform:translate(-50%,-50%);
text-align:center;color:white;z-index:2
}
.hero-text h1{
font-family:'Playfair Display',serif;
font-size:3em;text-shadow:2px 2px 8px rgba(0,0,0,.6)
}
.hero-text p{
font-size:1.3em;text-shadow:1px 1px 5px rgba(0,0,0,.6)
}
.hero-text .btn{
background:#25D366;color:white;
padding:15px 35px;border-radius:30px;font-weight:bold
}

/* RESTO IGUAL */
section{padding:80px 20px;max-width:1000px;margin:auto}
.presentacion{
font-family:'Merriweather',serif;
font-size:1.4em;text-align:center;margin:50px 0
}
.services{
display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px
}
.service-box{
padding:25px;border-radius:15px;
background:#f9f9f9;box-shadow:0 6px 18px rgba(0,0,0,.12);
text-align:center
}
.horarios{
color:#F5C223;font-size:1.6em;font-weight:bold
}
footer{
background:#222;color:white;text-align:center;padding:60px 20px
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

<!-- CARRUSEL CON TUS FOTOS -->
<div class="hero-slider">
  <div class="slide active" style="background-image:url('data:image/jpeg;base64,kwZ9a77gDZYWUvIlSszXMdnbdlDOpbYKwIUDyNdlaXqYTAwDjFVz9R1W2fW3CtAK...');"></div>
  <div class="slide" style="background-image:url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEASABIAAD...');"></div>
  <div class="slide" style="background-image:url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD...');"></div>

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

</body>
</html>
