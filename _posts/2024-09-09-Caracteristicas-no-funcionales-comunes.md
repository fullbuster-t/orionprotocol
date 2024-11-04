---
layout: post
title: "Características no funcionales comunes"
date: 2024-09-09 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Fundamentos de arquitectura de software]
description: adios otra vez
img: /assets/img/5.png
---

Las características no funcionales, comúnmente llamadas “características estructurales de calidad o arquitectónicas”, son aquellas que el sistema tiene como características de calidad, que además puede hacer, pero que no están completamente relacionadas con el dominio.

Son ampliamente importantes, ya que en algunas ocasiones su desarrollo requiere conocer nuevos conceptos. Adicionalmente, debemos entender que estas características tienen cierto roce entre sí. Por ejemplo, el establecimiento de seguridad puede no completarse debido a un requerimiento de mantenibilidad, como se explicaba en el post de Tradeoffs. Aquí se hace un análisis de equilibrio que es muy específico, dependiendo del software que se esté desarrollando y las necesidades que debe cubrir.

A continuación, ejemplificamos algunas de estas características basándonos en preguntas:

* Disponibilidad:
    * ¿Puedo acceder al sistema cuando lo necesito?
    * ¿Cuánto tiempo pasa sin que pueda acceder por año, mes, semana o día?
    * Como diseñadores, debemos pensar en cuánto se requiere que el sistema esté disponible. Debemos tener en cuenta que aumentar la disponibilidad a veces es muy caro. Suele expresarse en porcentajes.

* Rendimiento:
    * ¿Cuánto tiempo tarda en responder desde que sale mi petición?
    * ¿Qué tan rápido es el sistema?
    * ¿Cuánto tiempo tarda en completarse la tarea principal?
    * Se define como qué tan eficiente es el sistema al momento de responder a las peticiones de los usuarios. Como es de suponer, un sistema rápido implica costos elevados; nuestro trabajo como arquitectos de software es concientizar a los clientes sobre esta situación y tomar la mejor decisión para el desarrollo del proyecto.

* Extensibilidad:
    * ¿Puedo agregar nuevas funcionalidades de manera sencilla?
    * ¿Se pueden crear nuevas funciones sin programar?
    * Mientras más extensible sea el sistema, más difícil y costoso es desarrollarlo respecto a recursos y habilidades técnicas.

* Escalabilidad:
    * ¿Puedo hacer crecer el sistema para que atienda a más usuarios?
    * ¿Cuánto esfuerzo se requiere para atender a más usuarios de manera simultánea?
    * ¿Qué se necesita para que pueda procesar más datos/atender más peticiones?
    * Es una de las características de las que más se habla dentro del mundo del desarrollo de software; es también de las más complicadas de implementar e, inclusive, la más cara. Usualmente se menciona en el entorno de startups.


* Tolerancia a fallos:
    * ¿Puedo soportar fallos en el uso sin perder disponibilidad?
    * ¿Puede seguir disponible aunque falle el hardware que lo soporta?
    * ¿Qué pasa si se producen fallos intencionales?
    * Todo esto puede lograrse mediante técnicas específicas que veremos más adelante. La tolerancia a fallos ayuda a evitar errores por parte de los usuarios, ya sea porque no saben utilizar el software. Suele estar relacionada con la disponibilidad del sistema.

* Consistencia:
    * ¿Es la misma información consultada a través de diferentes dispositivos u ocasiones?

* Confiabilidad:
    * ¿Se puede comprobar que la información que el sistema presenta es correcta y exacta?
    * Se puede considerar como un atributo intermedio entre los requerimientos funcionales y no funcionales.

* Seguridad:
    * ¿Pueden acceder a la información solo los usuarios autorizados?
    * ¿Pueden acceder al sistema solo los usuarios autorizados?
    * ¿Está protegido el sistema contra ataques de personas malintencionadas?
    * Es el atributo de software más importante que existe actualmente. Al ser tan importante, el costo de su implementación es elevado y suele competir con otras características debido al choque que hay entre ellas.

* Auditabilidad:
    * ¿Puedo saber qué es lo que está pasando dentro del sistema?
    * ¿Puedo inspeccionar la información para saber por qué está respondiendo de cierta forma?
    * Es requerida cuando se habla de temas gubernamentales, buscando responder qué está haciendo el sistema y por qué lo está haciendo.

* Monitoreabilidad:
    * ¿El sistema comunica métricas sobre su estado actual?
    * ¿Puedo agregar o expandir estas métricas de manera sencilla?
    * Está relacionada con el estado general del sistema.

* Interoperabilidad:
    * ¿Puede el sistema usarse fácilmente con otros sistemas?
    * Se enfoca en que el sistema pueda complementarse con otros sin tener que programar módulos extras.

Todas estas características ayudan a lograr los objetivos como arquitecto. Se logra de dos formas: mediante aspectos relacionados con el dominio del negocio y atributos que permiten que el software funcione de la manera en que se espera.