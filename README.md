<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dog Company – Residencia Canina</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Lato', sans-serif;
    color: #222;
    background: #fff;
}

/* HEADER */
header {
    display: flex;
    align-items: center;
    padding: 25px 40px;
}

.header-accent {
    background: #f2c94c;
    padding: 22px 50px 22px 35px;
    border-radius: 0 50px 50px 0;
}

header h1 {
    margin: 0;
    font-family: 'Playfair Display', serif;
    color: #000;
    font-size: 30px;
    font-weight: 600;
}

/* HERO */
.hero {
    padding: 20px 40px;
}

.hero p {
    max-width: 650px;
    font-size: 18px;
    line-height: 1.7;
}

/* CARRUSEL */
.carousel {
    margin: 40px;
    height: 320px;
    background: #eee;
    border-radius: 20px;
}

/* SEPARADOR */
.separator {
    margin: 80px 0;
    text-align: center;
}

.separator svg {
    width: 140px;
}

/* SECCIONES */
.section {
    padding: 40px;
    max-width: 1000px;
}

.section h2 {
    font-family: 'Playfair Display', serif;
    font-size: 28px;
    font-weight: 600;
    text-decoration: underline;
    margin-bottom: 40px;
}

/* TARJETAS */
.service {
    background: #fafafa;
    padding: 30px;
    border-radius: 18px;
    margin-bottom: 30px;
}

.service h3 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    margin-bottom: 15px;
}

.service p {
    margin: 8px 0;
    font-size: 17px;
}

/* HORARIOS */
.horarios-box {
    background: #fff3f3;
    border-radius: 18px;
    padding: 40px 30px;
    text-align: center;
}

.horarios-box p {
    margin: 0;
    font-size: 28px;
    font-weight: 700;
    color: red;
    text-transform: uppercase;
    line-height: 1.5;
}

/* BOTÓN */
.button {
    display: inline-block;
    margin: 60px 40px;
    padding: 15px 32px;
    background: #25d366;
    color: white;
    text-decoration: none;
    border-radius: 30px;
    font-weight: 700;
    font-size: 16px;
}

/* WHATSAPP FLOAT */
.whatsapp-float {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25d366;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.whatsapp-float img {
    width: 34px;
}
</style>
</head>

<body>

<header>
    <div class="header-accent">
        <h1>DOG COMPANY</h1>
    </div>
</header>

<section class="hero">
    <p>
        Residencia canina privada en entorno familiar.  
        Cuidado personalizado, atención consciente y bienestar real.
        <br><strong>📍 Alicante centro</strong>
    </p>
</section>

<div class="carousel"></div>

<div class="separator">
<svg viewBox="0 0 200 40">
<path d="M10 20 Q50 0 90 20 T170 20" fill="none" stroke="#f2c94c" stroke-width="4"/>
</svg>
</div>

<section class="section">
    <h2>NUESTROS SERVICIOS</h2>

    <div class="service">
        <h3>Alojamiento noche</h3>
        <p>Perro adulto: <strong>24€</strong></p>
        <p>Cachorros (1–12 meses) o cuidados especiales: <strong>26€</strong></p>
    </div>

    <div class="service">
        <h3>Guardería de día</h3>
        <p><strong><u>Precio fijo hasta un máximo de 6 horas</u></strong></p>
        <p>Perro adulto: <strong>22€</strong></p>
        <p>Cachorros o cuidados especiales: <strong>24€</strong></p>
    </div>

    <div class="horarios-box">
        <p>
            HORARIOS DE APERTURA Y ATENCIÓN AL CLIENTE<br>
            10:00H A 20:00H · LUNES A DOMINGO
        </p>
    </div>
</section>

<a class="button" href="https://wa.me/34XXXXXXXXX" target="_blank">
Más información por WhatsApp
</a>

<a class="whatsapp-float" href="https://wa.me/34XXXXXXXXX" target="_blank">
<img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg">
</a>

</body>
</html>
