## Módulos del sistema y cómo se integran

Dividimos **Pide y Pam** en 7 módulos. Cada uno tiene una responsabilidad clara, para poder repartir el desarrollo entre los tres y trabajar en paralelo.

### Tabla de módulos

| #   | Módulo                                 | Responsabilidad                                                                                                                                | Se comunica con              |
| --- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- |
| 1   | **App del cliente** (React)            | Abrir la mesa al escanear el QR, mostrar la carta, gestionar el carrito, lanzar el pago y enseñar el ticket y el estado del pedido             | Backend/API, Pago            |
| 2   | **Pago** (Stripe)                      | Cobrar el pedido con tarjeta y confirmar al backend si el pago se ha hecho                                                                     | App del cliente, Backend/API |
| 3   | **Panel de cocina** (React)            | Mostrar en tiempo real los pedidos pagados y marcarlos como _en preparación_ y _listo_                                                         | Backend/API                  |
| 4   | **Panel de camarero** (React)          | Ver qué pedidos están listos y en qué mesa, marcarlos como _servido_, atender avisos de mesa y tomar nota si el cliente no puede usar el móvil | Backend/API                  |
| 5   | **Panel de administración** (React)    | Gestionar carta (platos, precios, categorías, disponibilidad), mesas y sus QR, usuarios del personal y ver ventas                              | Backend/API                  |
| 6   | **Backend / API** (Laravel)            | Lógica de negocio: API REST, autenticación por roles, estados del pedido, generación del ticket, avisos en tiempo real a los paneles           | Todos los módulos            |
| 7   | **Base de datos** (MySQL o PostgreSQL) | Guardar mesas, platos, pedidos, líneas de pedido, pagos y usuarios                                                                             | Solo Backend/API             |

### Estados del pedido

`pendiente de pago` → `pagado` → `en preparación` → `listo` → `servido`
