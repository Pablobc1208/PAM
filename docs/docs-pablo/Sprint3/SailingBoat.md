## 1. La metáfora

| Zona       | Pregunta                    | Qué representa                          |
| ---------- | --------------------------- | --------------------------------------- |
| **Isla**   | ¿A dónde queremos llegar?   | La meta del equipo                      |
| **Viento** | ¿Qué nos ha impulsado?      | Lo que ha funcionado y hay que mantener |
| **Anclas** | ¿Qué nos ha frenado?        | Problemas que ya hemos tenido           |
| **Rocas**  | ¿Qué riesgos vemos delante? | Peligros futuros que pueden hundirnos   |

## 2. Propuestas para el tablero

### Isla (meta)

- Presentar Pide y Pam en la presentación final y el pitch con una nota alta en la rúbrica RA2.a–RA2.j.
- Arrancar el desarrollo con un plan claro: epics E1–E6 y una Definition of Done que todos entendamos.
- Tener el flujo básico funcionando: pedir por QR → pagar → cocina → servir.

### Viento (lo que nos impulsa)

| Propuesta                                           | Dato que la respalda                                                                                             |
| --------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Cumplimos los plazos de cada sprint                 | Los epics #1 (Sprint 1) y #10 (Sprint 2) se cerraron con todas sus historias el día de la review (29/10 y 12/11) |
| Reparto equilibrado del trabajo                     | Cada miembro tiene historias en los tres sprints y commits propios en `dev`                                      |
| Trazabilidad entre commits e issues                 | Casi todos los commits citan su issue (`#3`, `#13`, `#16`, `#23`…)                                               |
| Tablero Kanban en GitHub Projects desde el Sprint 1 | Todas las tareas pasaron por el tablero                                                                          |
| Incorporamos el feedback del profesor cada sprint   | Issues #11 y #20 dedicadas solo a aplicar el feedback                                                            |
| Roles claros                                        | Backend (Adrián), frontend (Manuel), DevOps y Scrum Master (Pablo) en `docs/Sprint_2/Sprint_2.md`                |

### Anclas (lo que nos frena)

| Propuesta                                                 | Dato que la respalda                                                                                                                                   |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Trabajo concentrado el mismo día de la entrega            | El 29/10 entraron 13 commits del Sprint 1 entre las 09:38 y las 12:03; el 19/11 se cerraron #20 y #21 la misma mañana de la entrega                    |
| Casi no usamos pull requests ni revisión entre compañeros | Solo hay una PR en todo el repositorio (#26); el resto se sube directo a `dev`, con varios `Merge branch 'dev'` por trabajar a la vez en la misma rama |
| Retrabajo por feedback                                    | El Sprint 1 tuvo que rehacer costes (portátiles y local) y quitar el apartado de alternativas; el presupuesto del Sprint 2 se rehízo en #20            |
| Rutas y nombres que cambian                               | Las issues pedían `docs/sprint-3/…` y el repositorio usa `docs/Sprint_3/…`; también se renombraron archivos (`AGD.md` → `competencia.md`)              |
| Mensajes de commit sin un criterio común                  | Hay commits en español y en inglés; desde el 19/11 acordamos solo inglés                                                                               |

### Rocas (riesgos que vienen)

| Propuesta                             | Por qué es un riesgo                                                                   |
| ------------------------------------- | -------------------------------------------------------------------------------------- |
| Todavía no hay código                 | Todo lo hecho es documentación; el desarrollo real empieza ahora                       |
| Decisiones técnicas abiertas          | Base de datos (MySQL o PostgreSQL) sin decidir; afecta al epic E6                      |
| Partes técnicas nuevas para el equipo | Pagos con Stripe y avisos en tiempo real (Laravel broadcasting)                        |
| La DoD es exigente                    | Pide revisión en PR, tests en verde y cobertura ≥ 70 %, algo que aún no practicamos    |
| Carga de otras asignaturas            | Si el trabajo se sigue dejando para el último día, el desarrollo no cabe en una semana |
| Presupuesto con cifras estimadas      | Los precios del presupuesto son estimaciones sin validar con proveedores               |

## 4. Acciones de mejora (propuestas)

| #   | Acción                                                                            | Responsable (propuesta) | Cómo lo comprobamos                                     |
| --- | --------------------------------------------------------------------------------- | ----------------------- | ------------------------------------------------------- |
| A1  | Todo cambio entra en `dev` por pull request con 1 aprobación de otro miembro      | Pablo                   | Nº de PR revisadas / nº de cambios en `dev` = 100 %     |
| A2  | Revisión a mitad de sprint (miércoles) para ver qué va con retraso                | Pablo                   | Se ha hecho la revisión cada sprint                     |
| A3  | Fijar en la planificación la ruta y el nombre de cada entregable antes de empezar | Manuel                  | 0 archivos movidos o renombrados después de subirlos    |
| A4  | Decidir la base de datos en la primera semana de desarrollo                       | Adrián                  | Decisión escrita en `docs/` antes de terminar la semana |
| A5  | Hacer una tarea pequeña de prueba con tests y PR para practicar la DoD            | Adrián                  | Primera PR que cumple los 14 puntos de la DoD           |

## 5. Slide de resumen (1 diapositiva)

**Retrospectiva · Sailing Boat**

- **Meta:** presentar Pide y Pam y empezar a desarrollar con epics y DoD claros.
- **Nos impulsa:** cumplimos todos los sprints a tiempo, reparto equilibrado y feedback aplicado.
- **Nos frena:** trabajo al último momento y poca revisión entre compañeros.
- **Riesgos:** aún no hay código, base de datos sin decidir y Stripe/tiempo real nuevos para nosotros.
- **Cambiamos:** pull request con revisión obligatoria, control a mitad de sprint y decidir la base de datos ya.
