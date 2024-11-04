---
layout: post
title: "Arquitectura vs diseño"
date: 2024-08-30 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Fundamentos de arquitectura de software]
description: hola otra vez
img: /assets/img/5.png
---

Dentro del proceso de desarrollo de software, debemos tener en cuenta dónde empieza y dónde termina la arquitectura y el diseño de software, así como cuál es la responsabilidad de cada uno. Esto nos ayuda a definir quién debe tomar las decisiones y quiénes deben colaborar durante el proceso, así como el grado de colaboración entre arquitectos y desarrolladores.

![alt text](/assets/img/arq-013.png){: width="600" }

En este gráfico, se denotan, del lado izquierdo, todas las decisiones que corresponden a la arquitectura de software, y en el lado superior derecho, las decisiones respecto al diseño de software. En el medio, podemos definir que se encuentra el punto de colaboración entre desarrolladores y arquitectos.

Si nos enfocamos en la imagen, podemos decir que para determinar el tipo de decisión se toman los siguientes criterios:

* Si la decisión tiene que ver más con estrategia, se puede decir que es de arquitectura. Cuando se menciona estrategia, se incluyen decisiones que tienen implicaciones a largo plazo; estas decisiones tienen un impacto directo sobre otras.

* Si la decisión tiene que ver con táctica, se dice que no tiene correlación con otras, por lo cual se consideran independientes.

A continuación damos algunos ejemplos de decisiones:

Decisión de arquitectura: cambiar el estilo de arquitectura de monolito a microservicios. Este tipo de decisiones conlleva un esfuerzo mayor que una decisión más táctica, como puede ser dividir un servicio en distintos servicios.

Como se puede observar, las dos figuras que se desarrollan en este contexto son tanto el desarrollador como el arquitecto.

![alt text](/assets/img/arq-014.png){: width="600" }

Para el arquitecto las principales funciones son:

* Determinar las características que corresponden al sistema; estas características se obtienen directamente de las necesidades de las funcionalidades que el negocio requiere.

* Determinar el estilo; qué estilo se adapta mejor a las necesidades del negocio.
* Denotar las decisiones de arquitectura respecto a qué modelos se deben utilizar.
* Principios; nos ayudan a proporcionar un marco de desarrollo de código limpio, mantenible y escalable.
* Interacción de los componentes; cómo se comunican los componentes en las distintas fases evolutivas del sistema.

A través de la toma de decisiones en la arquitectura, se crean artefactos que posteriormente el desarrollador debe implementar.

- Clases: que clases se implementan y componen el sistema.
- UI: hace referencia a la interfaz gráfica que tiene el sistema.
- Código: el desarrollo del código que hace funcional el sistema.





