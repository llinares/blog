---
title: Single Page Apps y cómo mejorar la UX (parte 2)
author: Lean Linares
date: 2015-04-20
template: article.jade
---

Para recapitular sobre el tema, denle una leída a la [Parte 1](#) del artículo.

Igualmente, repaso el punto 1 y 2 agregando un poco de info, y sumo un tercer punto:

# 1. Cero tiempo de carga

En una Single Page App el usuario **no percibe un tiempo de espera entre una página y la otra**. **Todo es instantáneo, literalmente.**

Lo que sí tiene tiempo de carga es la información, pero no la UI.

Con algunos compañeros de trabajo empezamos a notar que cada vez más productos de primera linea aprovechan este feature.

Buscando más info con el team de front-end, llegamos a la conclusión de que no tiene un nombre definido.

Encontramos estos 2 artículos super detallados sobre la percepción de velocidad del usuario y como mejorar la UX evitando bloquear la UI:

- [Non-blocking UI's with interface previews](http://www.callumhart.com/blog/non-blocking-uis-with-interface-previews)
- [A Beginner's Guide to Perceived Performance: 4 Ways to Make Your Mobile Site Feel Like a Native App](http://www.mobify.com/blog/beginners-guide-to-perceived-performance/)

# 2. Flujos que dejan de ser lineales

La página no se recarga nunca cuando el usuario navega. Esto nos permite hacer tareas en el fondo.

La primera vez que escuché sobre aprovechar las tareas de background, fue de la mano de Instagram.

Ellos comparten algunos trucos para darle a los usuarios una sensación de constante respuesta.

Según [este artículo](http://www.fastcodesign.com/1669788/the-3-white-lies-behind-instagrams-lightning-speed) que lei hace un tiempo, las 3 "mentiras blancas" de Instagram son:

- La UI siempre finge que está trabajando.
- Se carga contenido basado en la importancia, no en el orden.
- Se anticipan a cada movimiento del usuario. Por ejemplo, ¿por qué esperar a que cliquee "Enviar" para empezar a enviar información sin que lo perciba?

# 3. La conexión a internet como una capa de mejora

> "We live in a disconnected & battery powered world, but our technology and best practices are a leftover from the always connected & steadily powered past."

Este feature es conocido como **offline-first** y es un paso más a mobile-first.

Esto implica también re-pensar la forma en que el usuario interactúa con la UI.

Por ejemplo, un usuario podría responder preguntas en Mercado Libre sin conexión a internet, enviándolas cuando tenga red.

O podría cargar fotos y datos en el flujo de venta y que, sin tener conexión, recupere los datos si cerró la ventana.

Esta técnica también puede ser util para evitar la carga inicial de una SPA.

De esta forma el usuario tiene **cero segundos de carga inicial y cero segundos de carga entre pantallas**.

Esto va de la mano con la idea de que **la web empieza a parecerse a las Apps nativas**.

Les dejo este artículo de A list apart sobre [Designing Offline-First Web Apps](http://alistapart.com/article/offline-first).

# Conclusión

Las SPA se enfocan en la velocidad y percepción de velocidad de la UI/UX.

Cada vez vamos a ver más front-ends con éstos features y necesitamos aprovecharlos al máximo.

Todo esto cambia bastante la forma de diseñar las interacciones, y necesitamos empezar a pensar distinto de como lo venimos haciendo.

La web dejó de ser estática hace tiempo y nos obliga a adaptarnos a estos nuevos tipos de interacciones.
