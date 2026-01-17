<header>
  <nav class="nav-left">
    <a href="#servicios">Servicios</a>
    <a href="#resenas-footer">Reseñas</a>
    <a href="#quienes-somos-footer">Quiénes somos</a>
  </nav>

  <div class="logo-container">
    <div class="logo">Dog Company</div>
  </div>

  <div class="reserva-btn-container">
    <a class="reserva-btn" href="https://wa.me/34TUNUMERO" target="_blank">Reservas</a>
  </div>
</header>

<style>
/* HEADER MODIFICADO */
header {
  position: absolute; /* para alinearse sobre el carrusel */
  top: 0;
  width: 100%;
  display: flex;
  align-items: flex-start; /* alineado arriba */
  justify-content: space-between;
  padding: 15px 40px;
  z-index: 999;
  background: transparent; /* mantener fondo del carrusel */
}

.nav-left {
  display: flex;
  gap: 25px;
  font-weight: 600;
  align-items: flex-start;
}

.logo-container {
  position: relative;
  display: flex;
  justify-content: center;
  flex: 1;
}

.logo-container::before {
  content:"";
  position:absolute;
  top:50%;
  left:50%;
  transform:translate(-50%, -50%);
  width:420px;
  height:100px;
  background-color:#F5C223;
  z-index:-1;
  border-radius:25px;
}

.logo {
  font-family:'Playfair Display', serif;
  font-size:2em;
  font-weight:bold;
  color:black;
  padding:25px 20px;
}

.reserva-btn-container {
  display: flex;
  align-items: flex-start;
}

.reserva-btn {
  display: inline-block;
  background-color: #F5C223;
  color: black;
  font-weight: bold;
  padding: 12px 25px;
  border-radius: 12px;
  text-decoration: none;
}
</style>
