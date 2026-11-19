## 1. Wireframe

**Wireframe:** [Wireframes de Experiencia Gastronómica (Figma)](https://www.figma.com/make/c2xQl1PyyYO2feekhvsx0k/Wireframes-de-Experiencia-Gastron%C3%B3mica?t=ZUkySVPbghsirCEb-20&fullscreen=1)

## 2. Equipo

| Miembro         | Rol Scrum                 | Rol fijo              |
| --------------- | ------------------------- | --------------------- |
| Sergio Montes   | Product Owner             | Revisión del proyecto |
| Pablo Barrera   | Scrum Master y desarrollo | DevOps                |
| Adrián González | Desarrollo                | Backend               |
| Manuel Arenas   | Desarrollo                | Frontend              |

**Stack:** Laravel (API REST y autenticación por roles), React (interfaces), MySQL o PostgreSQL, Figma (prototipos), Git y GitHub Projects (DevOps). Apoyo cruzado con revisión de código por pares.

## 3. Módulos

1. **App del cliente (React):** QR de mesa, carta, carrito, pago y estado del pedido.
2. **Pago (Stripe):** cobro con tarjeta y confirmación al backend.
3. **Panel de cocina (React):** pedidos pagados en tiempo real; marcar _en preparación_ y _listo_.
4. **Panel de camarero (React):** pedidos listos por mesa, marcar _servido_, avisos de mesa y toma de nota manual.
5. **Panel de administración (React):** carta, mesas y QR, personal y ventas.
6. **Backend / API (Laravel):** lógica de negocio, roles, estados, ticket y avisos en tiempo real.
7. **Base de datos:** mesas, platos, pedidos, pagos y usuarios (solo accesible desde el backend).

**Estados del pedido:** `pendiente de pago` → `pagado` → `en preparación` → `listo` → `servido`

## 4. Recursos

- **Materiales:** equipos personales, GitHub y tablero Kanban.
- **Proveedores:** Hetzner Cloud (hosting), Dinahosting (dominio) y Stripe (pagos).
- **Asesoría:** profesor de IPE II y Atico34 (protección de datos).
- **Local:** oficina de alquiler por uso, una reunión semanal.
