---
layout: post
title: "Tradeoffs"
date: 2024-09-02 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Fundamentos de arquitectura de software]
description: hola de nuevo
img: /assets/img/5.png
---

Son conocidos como compensaciones. En la arquitectura de software, todo es un tradeoff, por lo cual es importante analizarlos y buscar tanto ventajas como desventajas.

![alt text](/assets/img/arq-015.png){: width="600" }

Con ayuda de este gráfico podemos diferenciar distintos tipos de tradeoffs:

* El lado izquierdo representa tradeoffs con mayor impacto, es decir, decisiones que necesitamos analizar con mayor detalle y tiempo, generalmente corresponden a decisiones de arquitectura.
* El lado derecho corresponde a decisiones que conllevan menos tiempo de análisis e implementación; son tradeoffs del diseño de software.

Imaginemos un caso práctico donde tenemos un e-commerce que tiene distintos componentes y módulos.

![alt text](/assets/img/arq-016.png){: width="700" }

El contexto que usaremos como ejemplo es el carrito de un e-commerce, en donde este debe comunicarse con la pasarela de pago y el control de inventario.
La forma en que se puede implementar nos presenta dos opciones: tópicos y una serie de mensajes.

Del lado izquierdo se tiene la implementación por tópicos. Aquí tenemos al carrito, que produce al tópico, y los suscriptores (en este caso, el consumidor de pagos y el consumidor de inventarios) reciben estas notificaciones y mensajes.

Del lado derecho, tenemos una cola de mensajes. A través de colas independientes, se envían mensajes distintos a cada uno de los consumidores.

Si comparamos estas dos formas de implementación, podemos notar que la implementación por tópicos (izquierda) es más escalable y extensible. Si necesitamos agregar un nuevo consumidor, en este caso, el historial de transacciones, simplemente lo agregamos.

Ahora bien, si quisiéramos agregar un nuevo consumidor a la cola de mensajes, sería necesario crear un mensaje independiente, como una cola de mensajes.

De manera que, en el lado izquierdo, con la misma infraestructura, solo suscribimos al consumidor y listo, mientras que, en el lado derecho, a través de las colas de mensajes, los cambios son más notorios.

![alt text](/assets/img/arq-017.png){: width="700" }

Si nosotros hacemos una comparación para obtener ventajas y desventajas tenemos lo siguiente:

* En la implementación por tópicos (lado izquierdo), el mensaje es homogéneo (igual) para todos los consumidores. Entonces, toda la información enviada es consumida por ellos. Esto supone una carga en el rendimiento (debido a la información adicional) y un riesgo de seguridad (ya que se comparte información idéntica a la que no todos los consumidores deberían tener acceso).

* En la implementación mediante cola de mensajes (lado derecho), tenemos mensajes independientes. Aquí no existe una brecha de seguridad como en la otra implementación.

Aquí es donde el tema de análisis de trade-offs cobra sentido en términos de seguridad y rendimiento. Esto debe ser comparado de acuerdo con el sistema. Es decir, en este ejemplo, la seguridad tiene mayor importancia que la extensibilidad y escalabilidad del sistema.

Por último, es importante mencionar que no solo existen ventajas, sino también desventajas, las cuales mostramos en el siguiente gráfico.

![alt text](/assets/img/arq-018.png){: width="800" }

Implementación por tópicos

* Ventajas:

    * Extensibilidad y desacoplamiento: agregar un nuevo consumidor o servicio es relativamente fácil y sencillo.

* Desventajas:

    * Acceso generalizado a la información bajo el mismo contrato: todos los consumidores y servicios pueden acceder a toda la información.

Implementación de cola de mensajes:

* Ventajas:

    * Acceso granular y contratos únicos: cada consumidor solo tiene acceso a cierto tipo de información.

* Desventajas:

    * Mantenibilidad y acoplamiento: al estar dividido en más módulos y servicios, tiende a crecer de manera desmesurada en algunos casos, dificultando la mantenibilidad.