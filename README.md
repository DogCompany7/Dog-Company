<form id="reservaForm">
  <input type="text" name="nombre" placeholder="Nombre" required>
  <input type="text" name="telefono" placeholder="Teléfono" required>
  <input type="text" name="mascota" placeholder="Nombre del perro" required>
  <select name="servicio" required>
    <option value="Alojamiento">Alojamiento Noche</option>
    <option value="Guardería">Guardería de Día</option>
  </select>
  <input type="date" name="fecha" required>
  <button type="submit">Enviar por WhatsApp</button>
</form>

<script>
document.getElementById('reservaForm').addEventListener('submit', function(e){
  e.preventDefault();
  const form = e.target;
  const nombre = form.nombre.value;
  const telefono = form.telefono.value;
  const mascota = form.mascota.value;
  const servicio = form.servicio.value;
  const fecha = form.fecha.value;

  // Mensaje que se enviará
  const mensaje = `Reserva Dog Company:%0ANombre: ${nombre}%0ATeléfono: ${telefono}%0ANombre del perro: ${mascota}%0AServicio: ${servicio}%0AFecha: ${fecha}`;

  // Abre WhatsApp con el mensaje
  window.open(`https://wa.me/34TUNUMERO?text=${mensaje}`, '_blank');
});
</script>
