## 1. Wireframe

**Wireframe:** [Wireframes de Experiencia Gastronómica (Figma)](https://www.figma.com/make/c2xQl1PyyYO2feekhvsx0k/Wireframes-de-Experiencia-Gastron%C3%B3mica?t=ZUkySVPbghsirCEb-20&fullscreen=1)

## 2. Equipo

| Miembro | Rol Scrum | Rol fijo |
|---|---|---|
| Sergio Montes | Product Owner | Revisión del proyecto |
| Pablo Barrera | Scrum Master y desarrollo | DevOps |
| Adrián González | Desarrollo | Backend |
| Manuel Arenas | Desarrollo | Frontend |

**Stack:** Laravel (API REST y autenticación por roles), React (interfaces), MySQL o PostgreSQL, Figma (prototipos), Git y GitHub Projects (DevOps). Apoyo cruzado con revisión de código por pares.

## 3. Módulos

1. **App del cliente (React):** QR de mesa, carta, carrito, pago y estado del pedido.
2. **Pago (Stripe):** cobro con tarjeta y confirmación al backend.
3. **Panel de cocina (React):** pedidos pagados en tiempo real; marcar *en preparación* y *listo*.
4. **Panel de camarero (React):** pedidos listos por mesa, marcar *servido*, avisos de mesa y toma de nota manual.
5. **Panel de administración (React):** carta, mesas y QR, personal y ventas.
6. **Backend / API (Laravel):** lógica de negocio, roles, estados, ticket y avisos en tiempo real.
7. **Base de datos:** mesas, platos, pedidos, pagos y usuarios (solo accesible desde el backend).

**Estados del pedido:** `pendiente de pago` → `pagado` → `en preparación` → `listo` → `servido`

## 4. Recursos

- **Materiales:** equipos personales, GitHub y tablero Kanban.
- **Proveedores:** Hetzner Cloud (hosting), Dinahosting (dominio) y Stripe (pagos).
- **Asesoría:** profesor de IPE II y Atico34 (protección de datos).
- **Local:** oficina de alquiler por uso, una reunión semanal.

## 5. Presupuesto del primer año

| Bloque | Detalle | Coste |
|---|---|---|
| Material fungible y equipamiento | Equipos propios (0 €), papelería y QR de demo (estimación propia) | 50,00 € |
| Licencias | GitHub Free, Figma Starter, VS Code | 0,00 € |
| Hosting | Hetzner CX23, 5,99 €/mes × 12 | 71,88 € |
| Dominio | Dinahosting .com | 10,99 € |
| Comisiones de pago | Stripe: 150 pedidos × 0,55 € (1,5 % + 0,25 €) | 82,50 € |
| Asesoría RGPD | Atico34 | 200,00 € |
| **Subtotal sin oficina** | | **415,37 €** |

**Oficina:** 6 € por persona y día, 52 reuniones, 3 miembros del equipo más clientes (el equipo asume su coste).

| | Escenario A (1 cliente) | Escenario B (2 clientes) |
|---|---|---|
| Personas por reunión | 4 | 5 |
| Oficina al año | 1.248,00 € | 1.560,00 € |
| **Subtotal** | **1.662,37 €** | **1.974,37 €** |
| Contingencia (12 %) | 199,48 € | 236,92 € |
| **TOTAL** | **1.861,85 €** | **2.211,29 €** |
| Rango con 10–15 % | 1.828,61 € – 1.911,73 € | 2.171,81 € – 2.270,53 € |
| Coste mensual | ≈ 155 € | ≈ 184 € |