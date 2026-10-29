## Viabilidad técnica

Comprobamos si podemos construir **Pide y Pam**, una web por QR con pedido, pago, cocina, camarero y administración, con los medios y conocimientos que tenemos.

### Tecnologías

| Parte                           | Decisión                                                                             | Por qué                                                                                |
| ------------------------------- | ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| Frontend (cliente y paneles)    | **React**                                                                            | Interfaces rápidas y adaptadas a móvil, con componentes reutilizables entre paneles    |
| Backend / API                   | **Laravel (PHP)**                                                                    | API REST, autenticación por roles                                                      |
| Tiempo real (cocina y camarero) | Laravel                                                                              | El pedido aparece en cocina al momento, sin recargar                                   |
| Base de datos                   | _Por definir:_ MySQL o PostgreSQL                                                    | Relacional (mesas, platos, pedidos, pagos); las dos funcionan directamente con Laravel |
| Hosting                         | _Por definir:_ Railway, Render o un VPS para el backend; Vercel o Netlify para React | Planes gratuitos o baratos, suficientes para la demo                                   |
| Pasarela de pago                | Stripe en modo pruebas                                                               | Tarjetas de prueba y SDK para PHP y React                                              |

### Infraestructura y material

- **Desarrollo:** nuestros portátiles, VS Code, PHP + Composer, Node.js, Git y GitHub (repo y Projects). Coste: 0 €.
- **Servidor y base de datos:** plan gratuito o de estudiante en la nube. Coste: 0 €, o pocos euros al mes, durante el proyecto.
- **Pruebas:** nuestros móviles (Android e iPhone) como clientes y un portátil o tablet como pantalla de cocina.
- **Demo:** QR impresos en papel para simular las mesas.

### Competencias del equipo

| Necesitamos                   | ¿Lo tenemos?                                        |
| ----------------------------- | --------------------------------------------------- |
| JavaScript y React            | Por confirmar                                       |
| PHP y Laravel                 | Por confirmar                                       |
| Bases de datos SQL            | Revisión                                            |
| Integración de pagos (Stripe) | Hay que aprenderlo (Stripe tiene guías paso a paso) |

### Limitaciones técnicas

- **Pagos solo en modo pruebas:** cobrar de verdad exige una empresa dada de alta y un contrato con la pasarela.
- **Depende de la conexión del cliente:** sin internet no se puede pedir, así que el camarero mantiene su panel para tomar nota.
- **Sin integración con TPV reales:** conectar con las cajas que ya usa el restaurante queda fuera del alcance.
- **Seguridad del QR:** hay que evitar pedidos falsos. El pedido solo pasa a cocina después de pagar.
- **Tiempo y equipo:** somos tres personas, así que el alcance se limita a un MVP con carta, carrito, pago, ticket y los paneles de cocina, camarero y administración.

### Conclusión

**El proyecto es viable.** React y Laravel cubren todo lo que necesitamos, y la base de datos y el hosting tienen opciones gratuitas compatibles. Lo nuevo (tiempo real y Stripe) está bien documentado y se puede aprender dentro del proyecto. La principal limitación es que el pago será simulado.

---
