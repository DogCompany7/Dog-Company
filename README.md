<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dog Company – Residencia Canina</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    color: #222;
    background: #fff;
}

/* HEADER */
header {
    display: flex;
    align-items: center;
    padding: 20px 40px;
    position: relative;
}

.header-accent {
    background: #f2c94c;
    padding: 18px 40px 18px 30px;
    border-radius: 0 40px 40px 0;
}

header h1 {
    margin: 0;
    color: #000;
    font-size: 28px;
    font-weight: 600;
}

/* HERO */
.hero {
    padding: 20px 40px;
}

.hero p {
    max-width: 600px;
    font-size: 17px;
    line-height: 1.6;
}

/* CARRUSEL */
.carousel {
    margin: 40px;
    height: 320px;
    background: #eee;
    border-radius: 18px;
}

/* SEPARADOR ORGÁNICO */
.separator {
    margin: 80px 0;
    text-align: center;
}

.separator svg {
    width: 120px;
}

/* SERVICIOS */
.section {
    padding: 40px;
    max-width: 900px;
}

.section h2 {
    font-size: 26px;
    font-weight: 600;
    text-decoration: underline;
}

.service {
    margin: 30px 0;
}

.service h3 {
    margin-bottom: 10px;
    font-size: 20px;
}

.service p {
    margin: 6px 0;
}

/* HORARIOS */
.horarios {
    margin-top: 40px;
    font-size: 22px;
    font-weight: 600;
    color: red;
    text-transform: uppercase;
}

/* BOTÓN */
.button {
    display: inline-block;
    margin: 50px 40px;
    padding: 14px 28px;
    background: #25d366;
    color: white;
    text-decoration: none;
    border-radius: 30px;
    font-weight: 600;
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

    <div class="horarios">
        HORARIOS DE APERTURA Y ATENCIÓN AL CLIENTE<br>
        10:00H A 20:00H · LUNES A DOMINGO
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
