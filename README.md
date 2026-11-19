# sistema-luciapatino-demo

Demo navegable del **sistema de gestión** de Lucía Patiño, especialista en color (Cuenca, Azuay · Ecuador).

Es el complemento de la landing: la web pública atrae y agenda; este panel es lo que la colorista usa todos los días.

## Qué incluye

Aplicación de una sola página (`index.html`, CSS y JS inline, sin backend ni dependencias externas salvo Google Fonts):

- **Entrada simulada**: usuario demo precargado y botón «Entrar en modo demostración» (sin autenticación real).
- **Escritorio**: citas de hoy, horas ocupadas, ingresos del día, próxima clienta y avisos (por confirmar, retoques que vencen, por cobrar).
- **Agenda**: vista de semana y de día. Cada cita ocupa un bloque **proporcional a la duración real del servicio** (un balayage de 150 min ocupa media jornada; un corte de 45 min, apenas una franja). Detalle de cada cita y creación real de citas desde el formulario (clienta, servicio, día, hora, duración); avisa si la hora se cruza con otra cita de la misma profesional.
- **Clientas**: buscador y ficha con contacto, historial de visitas, **fórmula de color** (mezcla, oxidante y tiempo de exposición) con la nota del último trabajo, estado del **retoque de raíz**, packs y fotos de evolución (simuladas).
- **Mensajes**: bandeja tipo WhatsApp con recordatorios de turno, **avisos de retoque** («ya toca retocar la raíz, ¿le reservamos?») y confirmaciones.
- **Pagos**: cobros del mes con fecha, clienta, servicio, método (efectivo, transferencia, tarjeta) y estado, con totales y ticket promedio.
- **Informes**: citas por semana, estado de las citas (donut, confirmadas vs. canceladas), servicios más pedidos, ingresos por mes y horas ocupadas por semana. Todo hecho con SVG y CSS, sin librerías.
- **Ajustes**: catálogo de servicios editable en memoria (nombre, precio y duración en minutos), horarios de atención y recordatorios (horas antes del turno y semanas para el retoque), con vistas previas de los mensajes.
- Menú de usuario con acceso a la web pública, y pie con la nota de demo.

Los datos son de ejemplo y se generan en el navegador, relativos a la fecha en que se abre el demo: 25 clientas, ~55 citas del mes, 6 packs, retoques con fecha de vencimiento, pagos en dólares y una colorista (Lucía) con su ayudante.

## Despliegue

`Dockerfile` de dos líneas (`nginx:alpine` + copia de los archivos) publicado desde este repositorio en EasyPanel:

- Sistema: https://clientes-sistema-luciapatino.rddxeh.easypanel.host/
- Web pública: https://clientes-demo-luciapatino.rddxeh.easypanel.host/

## Nota

Demo de referencia hecho por Nocodeveloper. No envía mensajes, no guarda datos y no incluye información real de terceros; en el sistema real se cargan los datos de la clienta.
