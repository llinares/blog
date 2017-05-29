---
title: Card pattern
author: lean
date: 2015-05-19
template: article.jade
topics: ux
---

Si bien la definición de qué es una Card es subjetiva, se suele usar para referirse a una caja blanca con bordes y sombra.

Pero más allá del diseño, las Cards se enfocan en cómo interactúa el usuario con ese elemento.

En un artículo encontré esto que me parece bastante textual:

> "Designers can call the things on the screen "cards" simply because those rectangular regions look like the small physical cards that have fit into our pockets for centuries. However, beyond how they look, the cards I’m talking about have interactive qualities.".

# Interacción con el usuario

**Las Cards se tratan acerca de interacciones.** Por ejemplo:

- Dar vuelta una card para ver más datos.
- Correr la card un poco al costado para descubrir acciones.
- Hacer "pinch" en la imagen para agrandarla temporalmente.
- Compartirla tal cual está en una red social.
- Moverla para generar distintas acciones.

Un acercamiento a Cards que veo implementado en [MercadoLibre](http://www.mercadolibre.com/) son los artículos en la homepage:

![Artículo de la homepage](item.gif)

En un estado inicial se ve la foto y el precio del artículo. Al pasar por encima con el cursor se ve además: título, cuotas, envío y la acción de agregar a favoritos.

Más allá de que está pensado únicamente para usuarios que tienen un mouse/cursor, creo que se acerca muchísimo al concepto de Cards.

# Portabilidad

Otra característica que me parece importante de las Cards es la portabilidad. Entonces, **una Card de una página de búsqueda podría usarse también en la homepage, en una página de producto y en un listado de Mi cuenta**. No solo la interacción, sino también la implementación (HTML, CSS, JS).

Más info sobre este patrón:

- [Scroll down: The future of online media is in the cards](http://pando.com/2013/05/16/scroll-down-the-future-of-online-media-is-in-the-cards/)
- [Cards: The Next Paradigm?](http://echouser.com/blog/cards-the-next-paradigm/)
- [Why cards are the future of the web](http://insideintercom.io/why-cards-are-the-future-of-the-web/)
