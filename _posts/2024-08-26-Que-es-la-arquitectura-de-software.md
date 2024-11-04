---
layout: post
title: "¿Qué es la arquitectura de software?"
date: 2024-08-26 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Fundamentos de arquitectura de software]
description: ¿Qué es la arquitectura de software?
img: /assets/img/5.png
---

## Arquitectura de software

Es un concepto muy utilizado en la industria de la tecnología. A pesar de que hay distintas definiciones para este concepto, no existe un estándar que lo defina.

Nosotros tomaremos dos definiciones:

- La primera es de Martin Fowler, quien define la arquitectura de software como las distintas cosas que son difíciles de cambiar. 
- La segunda es de Ralph Johnson, quien enuncia que la arquitectura de software son todas las cosas importantes.

En otras definiciones, se suele hacer referencia a los planos arquitectónicos de una casa. Esto, llevado al software, nos permite imaginar los planos bien definidos de los componentes, cómo interactúan entre sí y cómo está construido el sistema.

![alt text](/assets/img/arq-001.png){: width="200" }

También se tiene el plano a un roadmap, que hace referencia a cómo se va desarrollando el sistema en el tiempo.

![alt text](/assets/img/arq-002.png){: width="400" }

![alt text](/assets/img/arq-003.png){: width="600" }

Debido a que existen múltiples definiciones nos enfocaremos en 4 dimensiones: 

* Características del sistema (requerimientos no funcionales): normalmente se asocian a requerimientos técnicos y cualidades de un sistema, definiendo el criterio de éxito de este. Son necesarios para que el sistema funcione de manera correcta.
    * Ejemplos: disponibilidad, seguridad, escalabilidad.

![alt text](/assets/img/arq-004.png){: width="500" }

* Decisiones arquitectónicas: son reglas sobre cómo se debe construir el sistema. Es buena práctica documentar estas decisiones y explicar por qué se toman. En general, son restricciones que impactan la implementación de los desarrolladores.
    * Ejemplo: se puede definir que la capa de presentación no tendrá acceso directo a la base de datos; únicamente se podrá acceder a la base de datos a través de una capa de servicios o de negocios.

![alt text](/assets/img/arq-005.png){: width="500" }

* Principios de diseño: son una guía para la implementación del sistema.
    * Ejemplo: establecer un principio de diseño como el apalancamiento de mensajería entre componentes, mejorando el rendimiento.

![alt text](/assets/img/arq-006.png){: width="500" }

Estilo arquitectónico: generalmente se refiere al estilo o la estructura. Cuando nos preguntan sobre la arquitectura del sistema, generalmente hablamos de esta dimensión.

![alt text](/assets/img/arq-007.png){: width="500" }

**4 dimensiones de la arquitectura de software**

![alt text](/assets/img/arq-008.png){: width="600" }