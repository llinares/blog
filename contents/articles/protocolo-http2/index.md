---
title: Protocolo HTTP/2
author: lean
date: 2015-03-03
template: article.jade
topics: code
---

El protocolo de intercambio de datos que usa la web hoy en día es lento y bastante antiguo (HTTP 1.1, es de 1999).

Para pedir cada archivo (html, css, js, imágenes, etc.) al servidor, se ejecuta un proceso bastante costoso en el que cliente y servidor se comunican y tratan de entenderse.

Con el tiempo esto nos fue empujando a usar técnicas como:

- Juntar varias imágenes en una sola (sprites).
- Juntar varios archivos JS o CSS en uno solo (bundles).
- Tener distintos sub-dominios para servir archivos estáticos.

Dentro de poco HTTP/2 va a dejar de ser borrador. Está basado en el conocido SPDY (de Google) que **ya está en todos los browsers**.

HTTP/2, en resumidas cuentas, mejora muchísimo el tiempo de carga de una página.

Algunos puntos importantes sobre esta versión:

- Deja la conexión con el server abierta, y así nos evitamos todos los siguientes handshakes.
- Comprime el tamaño del request, lo que lo hace mucho más rápido.
- Puede enviar y recibir muchas cosas al mismo tiempo a través de una única conexión.

Lo bueno es que esta tecnología **es totalmente compatible con sitios que no la aprovechen**.
