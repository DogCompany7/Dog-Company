<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dog Company - Residencia Canina</title>
<style>
    /* Reset básico */
    * {margin:0; padding:0; box-sizing:border-box; font-family: 'Arial', sans-serif;}
    body {background:#f9f9f9; color:#333; line-height:1.6;}
    a {text-decoration:none; color:#fff;}
    img {width:100%; display:block; border-radius:10px;}

    /* Cabecera y menú */
    header {position:relative;}
    nav {
        position:absolute; top:10px; right:20px;
        display:flex; gap:10px; background:rgba(0,0,0,0.5);
        padding:10px 15px; border-radius:8px;
    }
    nav a {color:#fff; font-weight:bold;}

    /* Carrusel */
    .carousel {position:relative; overflow:hidden; max-height:400px;}
    .carousel img {width:100%; height:400px; object-fit:cover;}
    .carousel-buttons {
        position:absolute; top:50%; width:100%; display:flex; justify-content:space-between;
        transform:translateY(-50%);
    }
    .carousel-buttons button {
        background:rgba(0,0,0,0.5); border:none; color:#fff; font-size:2rem; padding:5px 10px; cursor:pointer;
    }

    /* Secciones */
    section {padding:50px 20px; max-width:1000px; margin:0 auto;}
    h2 {text-align:center; margin-bottom:30px; font-size:2rem; color:#444;}
    .services, .testimonials, .gallery {display:grid; gap:20px;}
    .services {grid-template-columns:repeat(auto-fit, minmax(250px, 1fr));}
    .service {background:#fff; padding:20px; border-radius:10px; box-shadow:0 4px 10px rgba(0,0,0,0.1);}
    .service h3 {margin-bottom:10px; color:#e07b39;}
    .service ul {margin-top:10px; list-style:disc; padding-left:20px;}

    /* Horarios */
    .horarios {display:flex; justify-content:center; flex-wrap:wrap; gap:20px; margin-top:20px;}
    .horario {background:#fff; padding:15px 20px; border-radius:10px; box-shadow:0 2px 8px rgba(0,0,0,0.1); text-align:center; min-width:150px;}
    .horario h4 {margin-bottom:5px; color:#e07b39;}

    /* Testimonios */
    .testimonial {background:#fff; padding:20px; border-radius:10px; box-shadow:0 2px 8px rgba(0,0,0,0.1); font-style:italic;}
    .testimonial p {margin-bottom:10px;}

    /* Galería */
    .gallery {grid-template-columns:repeat(auto-fit, minmax(200px, 1fr));}

    /* Botón de WhatsApp */
    .whatsapp {position:fixed; bottom:20px; right:20px; background:#25D366; color:#fff; padding:15px 20px; border-radius:50px; font-weight:bold; box-shadow:0 4px 8px rgba(0,0,0,0.2); z-index:1000;}

    /* Footer */
    footer {text-align:center; padding:20px; background:#eee; margin-top:50px;}
</style>
</head>
<body>

<!-- Cabecera y Carrusel -->
<header>
    <div class="carousel">
        <img src="https://via.placeholder.com/1200x400?text=Perro+1" alt="Perro feliz jugando">
        <img src="https://via.placeholder.com/1200x400?text=Perro+2" alt="Perro descansando">
        <img src="https://via.placeholder.com/1200x400?text=Instalaciones" alt="Instalaciones">
    </div>
    <nav>
        <a href="#servicios">Servicios</a>
        <a href="#horarios">Horarios</a>
        <a href="#testimonios">Testimonios</a>
        <a href="#contacto">Contacto</a>
    </nav>
</header>

<!-- Sección Servicios -->
<section id="servicios">
    <h2>Servicios y Precios</h2>
    <div class="services">
        <div class="service">
            <h3>Residencia Canina</h3>
            <p><strong>25€ / noche</strong></p>
            <ul>
                <li>Alojamiento cómodo</li>
                <li>Paseos diarios</li>
                <li>Juegos y estimulación</li>
                <li>Alimentación según rutina del perro</li>
                <li>Medicación si es necesaria</li>
            </ul>
            <p>Entrada y salida flexibles</p>
        </div>
        <div class="service">
            <h3>Guardería de Día</h3>
            <p><strong>Desde 15€ / día</strong></p>
            <ul>
                <li>Socialización controlada</li>
                <li>Paseos</li>
                <li>Descanso en ambiente familiar</li>
            </ul>
        </div>
    </div>
</section>

<!-- Sección Horarios -->
<section id="horarios">
    <h2>Horarios</h2>
    <div class="horarios">
        <div class="horario">
            <h4>Entrada</h4>
            <p>9:00 – 11:00</p>
        </div>
        <div class="horario">
            <h4>Salida</h4>
            <p>18:00 – 20:00</p>
        </div>
        <div class="horario">
            <h4>Otros</h4>
            <p>Bajo consulta</p>
        </div>
    </div>
</section>

<!-- Testimonios -->
<section id="testimonios">
    <h2>Testimonios</h2>
    <div class="testimonials">
        <div class="testimonial">
            <p>“Mi perro volvió tranquilo y feliz. Se nota el cuidado y el amor.”</p>
            <p><strong>— Cliente real</strong></p>
        </div>
        <div class="testimonial">
            <p>“Por fin un sitio donde confío dejar a mi perro.”</p>
            <p><strong>— Cliente real</strong></p>
        </div>
    </div>
</section>

<!-- Galería -->
<section id="galeria">
    <h2>Galería</h2>
    <div class="gallery">
        <img src="https://via.placeholder.com/400x300?text=Perros+jugando" alt="Perros jugando">
        <img src="https://via.placeholder.com/400x300?text=Perro+descansando" alt="Perro descansando">
        <img src="https://via.placeholder.com/400x300?text=Instalaciones" alt="Instalaciones">
    </div>
</section>

<!-- Contacto -->
<section id="contacto">
    <h2>Contacto</h2>
    <p>Alicante capital</p>
    <p>Email: contacto@dogcompany.com</p>
    <p>¿Quieres reservar o preguntar disponibilidad? Escríbenos sin compromiso.</p>
    <a class="whatsapp" href="https://wa.me/tu-numero" target="_blank">Reservar por WhatsApp</a>
</section>

<!-- Footer -->
<footer>
    © Dog Company – Residencia Canina en Alicante
</footer>

<script>
    // Carrusel simple
    const carousel = document.querySelector('.carousel');
    const images = carousel.querySelectorAll('img');
    let index = 0;
    images.forEach((img,i)=>{if(i!==0) img.style.display='none';});
    setInterval(()=>{
        images[index].style.display='none';
        index = (index+1)%images.length;
        images[index].style.display='block';
    },4000);
</script>

</body>
</html>
