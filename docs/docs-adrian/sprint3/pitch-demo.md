# Pitch final — Pide y Pam

**Duración objetivo:** 12 minutos
**Equipo:** Pablo, Adrián y Manuel
**Proyecto:** Pide y Pam
**Objetivo:** Convencer a los stakeholders del valor de nuestra solución para restaurantes.

---

## 1. Presentación y problema — Pablo (0:00–2:00)

Buenos días. Somos el equipo PAM y hoy os presentamos **Pide y Pam**, una solución tecnológica pensada para mejorar la experiencia en restaurantes y facilitar el trabajo del personal.

Imaginad que estáis en un restaurante. Ya sabéis qué queréis pedir, pero el camarero está ocupado atendiendo otras mesas. Esperáis para pedir, esperáis para solicitar la cuenta y, en ocasiones, incluso termináis renunciando a pedir algo más.

Este problema no afecta solamente al cliente. También afecta al camarero, que tiene que atender muchas tareas repetitivas, y al dueño del restaurante, que puede perder ventas por las esperas.

En nuestro análisis encontramos algunos datos relevantes:

- El 84 % de los clientes se frustra al tener que buscar al camarero.
- Cerca del 60 % ha dejado de pedir un postre o una segunda bebida por no encontrarlo.
- El 54 % tiene en cuenta la velocidad del servicio al elegir restaurante.

Por tanto, hemos detectado una necesidad clara: **agilizar los pedidos y los pagos sin perder la atención humana que caracteriza a un buen restaurante.**

Y ahí es donde entra Pide y Pam.

## 2. Nuestra solución y propuesta de valor — Adrián (2:00–4:00)

Pide y Pam es una aplicación web a la que el cliente accede escaneando un código QR situado en su mesa.

No necesita descargar ninguna aplicación ni registrarse. Desde su propio móvil puede:

1. Consultar la carta.
2. Añadir productos al carrito.
3. Realizar el pago.
4. Recibir un ticket y consultar el estado del pedido.

Cuando el pago se confirma, el pedido llega al panel de cocina, donde el personal puede gestionarlo. El camarero también dispone de su propio panel para consultar los pedidos listos, atender avisos y registrar pedidos cuando un cliente no puede utilizar el móvil.

Además, el panel de administración permite gestionar la carta, los precios, las mesas, los códigos QR y los usuarios del personal.

Nuestra propuesta de valor se basa en dos ideas:

- **Una solución integrada:** cliente, cocina, camarero y administración trabajan conectados.
- **Una experiencia sencilla y rápida:** el cliente puede pedir sin esperar a que el camarero esté disponible.

Queremos dejar claro algo importante: no buscamos sustituir al camarero. Queremos liberar parte de su trabajo repetitivo para que pueda dedicar más tiempo a atender al cliente.

## 3. Demostración del prototipo — Manuel (4:00–7:00)

Ahora vamos a enseñar cómo funcionaría Pide y Pam desde el punto de vista de un cliente y del personal del restaurante.

**Paso 1. Acceso mediante QR**

El cliente escanea el código QR de su mesa y entra directamente en la aplicación web. No tiene que instalar nada.

**Paso 2. Consulta de la carta**

Aparecen los productos organizados por categorías, con sus precios y opciones para añadirlos al carrito.

**Paso 3. Carrito**

El cliente revisa los productos seleccionados, modifica las cantidades y comprueba el importe total.

**Paso 4. Pago**

El cliente llega a la pantalla de pago. En nuestra demostración utilizaremos Stripe en modo pruebas, ya que los cobros reales quedan fuera del alcance del proyecto académico.

**Paso 5. Ticket**

Una vez confirmado el pago de prueba, se muestra el ticket con el número de pedido, la mesa y el importe.

**Paso 6. Panel de cocina**

El pedido pagado aparece en el panel de cocina. El personal puede marcarlo como «en preparación» y después como «listo».

**Paso 7. Panel de camarero**

El camarero consulta los pedidos listos, identifica la mesa y puede marcar el pedido como servido. También puede atender avisos y registrar pedidos manualmente.

Con esta demostración vemos cómo se conectan las diferentes partes del sistema y cómo se simplifica el proceso desde que el cliente pide hasta que recibe su comida.

## 4. Tecnología, viabilidad y diferenciación — Pablo (7:00–9:00)

Para desarrollar Pide y Pam hemos seleccionado tecnologías que permiten construir una aplicación web moderna y adaptable.

- **React:** para la aplicación del cliente y los paneles.
- **Laravel y PHP:** para el backend y la API REST.
- **MySQL o PostgreSQL:** para almacenar la información.
- **Stripe:** para simular los pagos durante las pruebas.
- **Laravel:** para gestionar las actualizaciones de los pedidos en tiempo real.

El proyecto es técnicamente viable porque podemos desarrollar el MVP con los conocimientos y recursos del equipo, utilizando herramientas gratuitas y opciones económicas de alojamiento.

También hemos analizado otras soluciones del mercado, como Sinqro, Cuatroochenta, McDonald's y Revo XEF.

Nuestra intención es ofrecer una experiencia sencilla que conecte el pedido, el pago y la gestión de cocina sin obligar al cliente a descargar una aplicación ni al restaurante a comprar una tablet para cada mesa.

Somos conscientes de las limitaciones del proyecto: los pagos serán de prueba, dependeremos de la conexión a Internet y no tendremos integración con TPV reales en este MVP.

## 5. Beneficios y oportunidad — Adrián (9:00–10:30)

¿Qué aporta Pide y Pam a cada persona implicada?

**Para el cliente:**

- Menos esperas para pedir y pagar.
- Acceso rápido a la carta.
- Más control sobre su pedido.

**Para el camarero:**

- Menos tiempo dedicado a tomar pedidos y gestionar cobros.
- Información más clara sobre los pedidos.
- Más tiempo para atender a los clientes.

**Para el restaurante:**

- Un proceso de pedido más ágil.
- Menos oportunidades de perder ventas por las esperas.
- Una herramienta digital sin necesidad de comprar dispositivos para cada mesa.

Creemos que existe una oportunidad para restaurantes que quieren digitalizar parte de su servicio sin implantar sistemas demasiado complejos o costosos.

## 6. Cierre y conclusión — Manuel (10:30–12:00)

Para terminar, queremos volver a la idea con la que empezamos.

El cliente no quiere perseguir al camarero para pedir o pagar. Quiere disfrutar de su experiencia en el restaurante.

Pide y Pam permite que el cliente gestione su pedido desde el móvil, que cocina reciba la información y que el camarero pueda centrarse más en atender.

No pretendemos eliminar el trato personal. Queremos utilizar la tecnología para mejorarlo.

Somos conscientes de que todavía hay pasos por desarrollar y validar, pero contamos con una propuesta clara, una arquitectura definida y un MVP con un alcance realista.

**Pide y Pam: pide fácil, paga rápido y disfruta más.**

Muchas gracias por vuestra atención. Estamos disponibles para responder a vuestras preguntas.

---

# 7. Demo o prototipo navegable

Para la presentación, prepararemos un prototipo navegable en Figma o una demo de la aplicación.

**Recorrido que se debe enseñar:**

1. Escanear QR y entrar en la mesa.
2. Consultar la carta y añadir productos.
3. Revisar el carrito.
4. Simular el pago.
5. Mostrar el ticket.
6. Enseñar cómo aparece el pedido en cocina.
7. Mostrar cómo el camarero lo marca como servido.






