<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dog Company</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --amarillo:#E6B800;
      --verde:#2E7D32;
      --gris:#555;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    body{
      font-family:'Poppins',sans-serif;
      color:#222;
      background:#fafafa;
    }
    header{
      padding:20px 0 10px 0;
    }
    .top-bar{
      max-width:1100px;
      margin:0 auto;
      padding:14px 20px;
      background:var(--amarillo);
      display:flex;
      align-items:center;
    }
    .logo{
      font-size:28px;
      font-weight:700;
      color:#000;
    }
    .hero{
      max-width:1100px;
      margin:0 auto;
      padding:20px;
    }
    .carousel{
      height:260px;
      background:#ddd;
      border-radius:12px;
      display:flex;
      align-items:center;
      justify-content:center;
      color:#777;
      margin-bottom:40px;
    }
    .section-title{
      font-size:28px;
      font-weight:700;
      margin-bottom:20px;
      text-decoration:underline;
    }
    .services{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:20px;
      margin-bottom:40px;
    }
    .card{
      background:#fff;
      border-radius:16px;
      padding:24px;
      box-shadow:0 6px 20px rgba(0,0,0,.08);
      position:relative;
      overflow:hidden;
    }
    .card svg{
      position:absolute;
      top:-20px;
      right:-20px;
      width:120px;
      opacity:0.08;
    }
    .card h3{
      font-size:20px;
      margin-bottom:12px;
    }
    .price{
      font-size:18px;
      font-weight:700;
      margin:10px 0;
    }
    .price span{font-weight:400;color:var(--gris)}
    .highlight{
      font-weight:700;
      text-decoration:underline;
    }
    .hours-box{
      background:#fff;
      border-radius:16px;
      padding:24px;
      box-shadow:0 6px 20px rgba(0,0,0,.08);
      display:flex;
      align-items:center;
      justify-content:center;
      text-align:center;
      min-height:160px;
    }
    .hours-box p{
      font-size:20px;
      font-weight:600;
      color:#c62828;
      line-height:1.4;
    }
    .about{
      max-width:1100px;
      margin:0 auto 40px auto;
      padding:0 20px;
      font-size:17px;
      line-height:1.7;
      font-family:'Poppins',sans-serif;
    }
    .whatsapp{
      max-width:1100px;
      margin:0 auto 60px auto;
      padding:0 20px;
      text-align:right;
    }
    .whatsapp a{
      display:inline-block;
      background:#25D366;
      color:#fff;
      padding:12px 18px;
      border-radius:30px;
      text-decoration:none;
      font-weight:600;
      font-size:15px;
    }
  </style>
</head>
<body>

<header>
  <div class="top-bar">
    <div class="logo">DOG COMPANY</div>
  </div>
</header>

<section class="hero">
  <div class="carousel">Carrusel de imágenes</div>

  <h2 class="section-title">Nuestros servicios</h2>

  <div class="services">
    <div class="card">
      <svg viewBox="0 0 64 64"><path d="M32 36c-8 0-14 6-14 14h28c0-8-6-14-14-14z"/></svg>
      <h3>Alojamiento noche</h3>
      <p class="price"><strong>24€</strong> <span>por perro adulto</span></p>
      <p class="price"><strong>26€</strong> <span>cachorros (1–12 meses) y cuidados especiales</span></p>
    </div>

    <div class="card">
      <svg viewBox="0 0 64 64"><path d="M32 36c-8 0-14 6-14 14h28c0-8-6-14-14-14z"/></svg>
      <h3>Guardería de día</h3>
      <p class="highlight">Precio fijo hasta un máximo de 6 horas</p>
      <p class="price"><strong>22€</strong> <span>perro adulto</span></p>
      <p class="price"><strong>24€</strong> <span>cachorros y cuidados especiales</span></p>
    </div>

    <div class="hours-box">
      <p>HORARIOS DE APERTURA Y ATENCIÓN AL CLIENTE<br>LUNES A DOMINGO<br>10:00h – 20:00h</p>
    </div>
  </div>
</section>

<section class="about">
  <p>
    Somos Dog Company, residencia canina ubicada en <strong>Alicante centro</strong>. 
    Ofrecemos un entorno familiar, tranquilo y seguro, donde cada perro recibe atención personalizada, respeto por sus ritmos y mucho cariño.
  </p>
</section>

<div class="whatsapp">
  <a href="#">Más información por WhatsApp</a>
</div>

</body>
</html>
