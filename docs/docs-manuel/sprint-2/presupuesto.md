# Presupuesto de lanzamiento: Pide y Pam!

**Epic:** #10 · **Sprint:** 2 · **Criterio de rúbrica:** RA2.h
**Horizonte:** primer año de funcionamiento (12 meses)
**Nota:** proyecto ficticio. Los importes son estimaciones basadas en precios públicos de empresas reales (2026), sin IVA salvo que se indique.

## 1. Material fungible y equipamiento

| Concepto | Detalle | Coste |
|---|---|---|
| Equipos de desarrollo | Portátiles personales del equipo (ya disponibles, no se imputan) | 0,00 € |
| Dispositivo de pruebas | Móvil personal para probar el pedido por QR | 0,00 € |
| Papelería y material de oficina | Folios, post-its y rotuladores para el tablero físico (estimación propia) | 20,00 € |
| Impresión de QR y cartelería de demo | Códigos QR en mesa para la presentación (estimación propia) | 30,00 € |
| **Subtotal** | | **50,00 €** |

## 2. Licencias de software

| Licencia | Proveedor | Plan | Coste |
|---|---|---|---|
| Control de versiones y tablero Kanban | GitHub | Free | 0,00 € |
| Prototipos UI/UX | Figma | Starter (gratuito) | 0,00 € |
| Editor de código / IDE | VS Code o equivalente | Gratuito | 0,00 € |
| **Subtotal** | | | **0,00 €** |


## 3. Servicios externos

| Servicio | Proveedor de referencia | Cálculo | Coste (12 meses) |
|---|---|---|---|
| Hosting | Hetzner Cloud (CX23, 2 vCPU / 4 GB, IPv4 incluida) | 5,99 €/mes × 12 | 71,88 € |
| Dominio | Dinahosting (.com) | 10,99 €/año | 10,99 € |
| Comisiones de la pasarela de pago | Stripe | 150 pedidos de 20 € en los 3 primeros meses × (1,5 % + 0,25 €) = 0,55 € por pedido | 82,50 € |
| Asesoría de protección de datos (RGPD) | Atico34 | Empresa pequeña: 180–280 €/año (se toma 200 €) | 200,00 € |
| **Subtotal** | | | **364,37 €** |


## 4. Local de reuniones (oficina)

Alquiler de espacio de oficina por uso, con una tarifa de **6 € por persona y día** (dato localizado por el equipo en una búsqueda de alquiler de oficinas). Se acude **una vez a la semana** (52 semanas) con los 3 miembros del equipo y 1 o 2 clientes.

| Concepto | Personas | Cálculo semanal | Cálculo anual (52 semanas) |
|---|---|---|---|
| Equipo PAM | 3 | 3 × 6 € = 18 € | 936,00 € |
| Cliente(s) | 1 o 2 | 1 × 6 € = 6 € / 2 × 6 € = 12 € | 312,00 € / 624,00 € |

| Escenario | Personas por reunión | Coste semanal | **Coste anual** |
|---|---|---|---|
| **A: viene 1 cliente** | 4 | 24 € | **1.248,00 €** |
| **B: vienen 2 clientes** | 5 | 30 € | **1.560,00 €** |

> El coste de los clientes lo asume el equipo, porque se les invita a la reunión.

## 5. Resumen, contingencia y total

| Bloque | Escenario A (1 cliente) | Escenario B (2 clientes) |
|---|---|---|
| Material fungible y equipamiento | 50,00 € | 50,00 € |
| Licencias de software | 0,00 € | 0,00 € |
| Servicios externos | 364,37 € | 364,37 € |
| Local de reuniones | 1.248,00 € | 1.560,00 € |
| **Subtotal costes directos** | **1.662,37 €** | **1.974,37 €** |
| Contingencia (12 %) | 199,48 € | 236,92 € |
| **TOTAL estimado** | **1.861,85 €** | **2.211,29 €** |
| Rango con contingencia 10 % – 15 % | 1.828,61 € – 1.911,73 € | 2.171,81 € – 2.270,53 € |
| Coste mensual equivalente | ≈ 155 €/mes | ≈ 184 €/mes |

## 6. Fuentes de los precios

- Hetzner Cloud: precios 2026 de la serie CX (bitdoze.com).
- Dinahosting y Arsys: precios de dominio .com.
- Stripe España: 1,5 % + 0,25 € por tarjeta europea estándar.
- Atico34: consultoría RGPD desde 120 € + IVA/año; empresa pequeña, 180–280 €.
- Figma: plan Starter gratuito; Professional, 16 $ por editor al mes.
- Oficina: tarifa de 6 € por persona y día, aportada por el equipo a partir de una búsqueda en Google (sin proveedor concreto).

## 7. Hipótesis y puntos a revisar

- El material fungible no está sacado de un proveedor concreto, es una estimación del equipo.
- El volumen de pedidos (150 en 3 meses) es una suposición para calcular comisiones.
- Se asume una reunión semanal durante 52 semanas; si se reduce el número de semanas, el coste de la oficina baja proporcionalmente.
- Se cuentan 3 miembros del equipo. Si asistiera también el cuarto (Sergio Montes, Product Owner), el coste sube 6 € por semana (312 € al año).
- Hetzner subió precios dos veces en 2026, así que conviene confirmar la cifra final en su web.
- Todos los importes van sin IVA.