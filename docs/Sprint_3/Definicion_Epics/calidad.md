## 1. Objetivo

Dividir **Pide y Pam** en objetivos grandes (epics) que guíen el desarrollo y acordar una **Definition of Done (DoD)** con indicadores medibles, de forma que cualquier miembro sepa cuándo una tarea está terminada de verdad.

## 2. Resumen de los epics

| #   | Epic                    | Módulos del Sprint 2         | Responsable | Apoyo |
| --- | ----------------------- | ---------------------------- | ----------- | ----- |
| E1  | Pedido por QR           | App del cliente              |             |       |
| E2  | Pago y ticket           | Pago (Stripe), Backend       |             |       |
| E3  | Panel de cocina         | Panel de cocina              |             |       |
| E4  | Panel de camarero       | Panel de camarero            |             |       |
| E5  | Administración          | Panel de administración      |             |       |
| E6  | Plataforma y despliegue | Backend / API, Base de datos |             |       |

**Flujo del pedido que recorren los epics:**
`pendiente de pago` (E1) → `pagado` (E2) → `en preparación` → `listo` (E3) → `servido` (E4)

## 3. Detalle de los epics

### E1 · Pedido por QR

**Objetivo:** que el cliente pida desde su móvil sin descargar nada, solo escaneando el QR de la mesa.

**Historias previstas:**

- Como cliente, quiero escanear el QR de la mesa y que la app sepa en qué mesa estoy.
- Como cliente, quiero ver la carta por categorías con foto, precio y alérgenos.
- Como cliente, quiero añadir, quitar y modificar platos en el carrito.
- Como cliente, quiero ver el estado de mi pedido en tiempo real.

**Criterios de aceptación del epic:**

- Desde el escaneo hasta tener el carrito listo para pagar se tarda **menos de 2 minutos** con un usuario de prueba.
- La carta carga en **menos de 3 segundos** en móvil con red 4G.
- Funciona en Chrome y Safari de móvil.

### E2 · Pago y ticket

**Objetivo:** cobrar el pedido dentro de la app y entregar un ticket.

**Historias previstas:**

- Como cliente, quiero pagar con tarjeta desde la app (Stripe).
- Como sistema, quiero recibir la confirmación de Stripe (webhook) para pasar el pedido a `pagado`.
- Como cliente, quiero recibir un ticket después de pagar (en pantalla y descargable).
- Como cliente, quiero un aviso claro si el pago falla y poder reintentarlo.

**Criterios de aceptación del epic:**

- El **100 %** de los pagos con las tarjetas de prueba de Stripe cambian el estado del pedido correctamente.
- El ticket se genera en **menos de 5 segundos** tras el pago.
- Un pedido no llega a cocina si no está `pagado`.

### E3 · Panel de cocina

**Objetivo:** que la cocina vea los pedidos pagados al momento y marque su avance.

**Historias previstas:**

- Como cocinero, quiero ver los pedidos pagados en orden de llegada.
- Como cocinero, quiero marcar un pedido como `en preparación` y `listo`.
- Como cocinero, quiero ver las notas del cliente (alérgenos, sin cebolla…).

**Criterios de aceptación del epic:**

- Un pedido pagado aparece en el panel en **menos de 3 segundos** sin recargar la página.
- Se ve bien en una tablet horizontal.

### E4 · Panel de camarero

**Objetivo:** que el camarero sepa qué servir y a qué mesa, y pueda atender avisos.

**Historias previstas:**

- Como camarero, quiero ver los pedidos `listo` agrupados por mesa.
- Como camarero, quiero marcar un pedido como `servido`.
- Como camarero, quiero recibir avisos de las mesas (llamar al camarero, pedir la cuenta).
- Como camarero, quiero tomar nota de un pedido a mano para clientes sin móvil.

**Criterios de aceptación del epic:**

- El aviso de una mesa llega al panel en **menos de 3 segundos**.
- Marcar un pedido como servido requiere **2 toques o menos**.

### E5 · Administración

**Objetivo:** que el dueño del restaurante gestione su negocio sin ayuda técnica.

**Historias previstas:**

- Como administrador, quiero crear, editar y ocultar platos y categorías de la carta.
- Como administrador, quiero dar de alta mesas y generar e imprimir sus QR.
- Como administrador, quiero gestionar el personal y sus roles (cocina, camarero, admin).
- Como administrador, quiero ver las ventas por día y los platos más vendidos.

**Criterios de aceptación del epic:**

- Un cambio en la carta se ve en la app del cliente en **menos de 1 minuto**.
- Cada rol solo accede a su panel (comprobado con un test por rol).

### E6 · Plataforma y despliegue

**Objetivo:** la base técnica común: API, base de datos, roles, tiempo real y servidor.

**Historias previstas:**

- Como equipo, quiero una API REST en Laravel con autenticación por roles.
- Como equipo, quiero el modelo de base de datos (mesas, platos, pedidos, pagos, usuarios) con migraciones.
- Como equipo, quiero avisos en tiempo real (Laravel broadcasting) para cocina y camarero.
- Como equipo, quiero un pipeline en GitHub Actions que pase los tests en cada pull request.
- Como equipo, quiero desplegar en Hetzner con el dominio y HTTPS.

**Criterios de aceptación del epic:**

- El **p95** de respuesta de la API es **menor de 500 ms** con datos de prueba.
- El pipeline se ejecuta en **cada pull request** y bloquea el merge si falla.
- El despliegue a producción se hace con un único comando o acción.

## 4. Definition of Done

Una historia solo pasa a la columna **Done** del tablero si cumple **todos** estos puntos.

### 4.1 Calidad del código

| #   | Criterio                                 | Cómo se mide                                                    |
| --- | ---------------------------------------- | --------------------------------------------------------------- |
| 1   | Cumple todos sus criterios de aceptación | Checklist de la issue marcada al 100 %                          |
| 2   | Revisado por otro miembro del equipo     | Pull request con al menos **1 aprobación** que no sea del autor |
| 3   | Tests pasados                            | **100 %** de los tests en verde en GitHub Actions               |
| 4   | Cobertura de tests del backend           | **≥ 70 %** de líneas (PHPUnit)                                  |
| 5   | Sin errores de estilo                    | **0 errores** en el linter (Laravel Pint y ESLint)              |
| 6   | Sin errores graves                       | **0 bugs** críticos o bloqueantes abiertos sobre la historia    |

### 4.2 Producto

| #   | Criterio                | Cómo se mide                                                                                             |
| --- | ----------------------- | -------------------------------------------------------------------------------------------------------- |
| 7   | Rendimiento en móvil    | Lighthouse **≥ 80** en rendimiento y **≥ 90** en accesibilidad (pantallas del cliente)                   |
| 8   | Tiempo de respuesta     | API p95 **< 500 ms**; avisos en tiempo real **< 3 s**                                                    |
| 9   | Seguridad               | Rutas protegidas por rol; ningún dato de tarjeta se guarda en nuestra base de datos (lo gestiona Stripe) |
| 10  | Probado en entorno real | Desplegado en el servidor de pruebas y probado en un móvil de verdad                                     |

### 4.3 Equipo y proceso

| #   | Criterio           | Cómo se mide                                                           |
| --- | ------------------ | ---------------------------------------------------------------------- |
| 11  | Documentado        | README o `docs/` actualizado si cambia la API, la instalación o el uso |
| 12  | Integrado          | Pull request mergeada en `dev` y rama borrada                          |
| 13  | Validado por el PO | Sergio lo acepta en la Sprint Review                                   |
| 14  | Tablero al día     | Issue cerrada y tarjeta en **Done**                                    |

### 4.4 Done de un epic

Un epic está terminado cuando **todas** sus historias cumplen la DoD y además se cumplen los criterios de aceptación del propio epic (sección 3).

## 5. Cómo lo haremos real en GitHub (cuando esté aprobado)

1. **Etiquetas nuevas:** `epic-producto`, `E1-pedido-qr`, `E2-pago-ticket`, `E3-cocina`, `E4-camarero`, `E5-admin`, `E6-plataforma`.
2. **Issues de epic:** una por cada epic (`[EPIC] E1 · Pedido por QR`, …) con su objetivo y sus criterios de aceptación como checklist.
3. **Historias:** una issue por cada historia de la sección 3, enlazada como sub-issue de su epic, con la etiqueta `historia de usuario`.
4. **Asignación:** el responsable del epic queda asignado al epic; las historias se reparten en la planificación entre Pablo, Adrián y Manuel.
5. **Tablero:** añadir los epics e historias a GitHub Projects en la columna **Backlog**.
