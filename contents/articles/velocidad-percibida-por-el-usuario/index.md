---
title: Velocidad percibida por el usuario
author: Lean Linares
date: 2015-05-11
template: article.jade
---

# The experience of waiting

Hace un tiempo leí un artículo sobre el aeropuerto de Houston.

Ellos recibían muchísimas quejas sobre el tiempo de espera para retirar el equipaje.

Aumentaron la cantidad de personal que transportaba el equipaje y mejoraron bastante la **velocidad de entrega**.

Igualmente seguía siendo muy lento (unos 8 minutos) y seguían recibiendo quejas.

Se dieron cuenta que a los pasajeros les tomaba solamente 1 minuto en ir desde el avión hasta donde se retira el equipaje, y 7 minutos en recibir las valijas. **Pasaban el 88% de su tiempo esperando.**

Entonces, alejando la zona de equipaje de las puertas de abordaje, **eliminaron (virtualmente) la molestia y stress del tiempo de espera**.

**La gente pasó mucho menos tiempo esperando, y así redujeron las quejas casi a cero.**

El artículo: [Why Waiting Is Torture](http://www.nytimes.com/2012/08/19/opinion/sunday/why-waiting-in-line-is-torture.html)

# Percepción de velocidad en los flows críticos

Un usuario común de MercadoLibre suele moverse, por ejemplo, desde la homepage o resultados de busqueda hacia la página de un producto.

Si tenemos en cuenta algunas buenas técnicas, podemos aprovechar al máximo esa relación.

# 1. Prefetching

Si generáramos un mapa de calor con Crazy Egg (http://crazyegg.com) podríamos predecir en la homepage y en el Search, cual es la ubicación de los artículos que son altamente probables que sean visitados.

Sabiendo esto, **en la carga inicial de esas páginas podemos pre-cargar (de fondo) las páginas de producto que son altamente probables que el usuario visite**.

Para eso, en la homepage y Search deberíamos especificar qué artículos podrían ser los próximos en ser visitados:

```
<link rel="prefetch" href="http://articulo.ml.com.ar/MLA-123-foo-_JM" />
<link rel="prefetch" href="http://articulo.ml.com.ar/MLA-456-bar-_JM" />
<link rel="prefetch" href="http://articulo.ml.com.ar/MLA-789-baz-_JM" />
```

De esta forma, cuando se hace clic en un artículo, la carga de la página de producto es instantánea.

Esto mismo pueden verlo al buscar en Google. Ellos pre-cargan siempre el primer resultado (denle unos segundos, a veces tarda en pre-cargarse).

Este post de Mozilla contesta las dudas más comunes sobre el tema:

[Link prefetching FAQ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Link_prefetching_FAQ)

# 2. Critical path

Para mejorar significativamente la performance, se recomienda pegar el CSS del contenido visible **directamente en el HTML**.

Esto le permite al browser tener lista, mucho antes, la experiencia "above-the-fold".

Para esto tenemos que determinar qué estilos representan al contenido que se muestra en el primer pantallazo para la mayoría de los usuarios.

La idea es incluir esos estilos en un `<style>` dentro del `<head>`.

El resto de los estilos deberían cargarse antes del cierre del `</body>` o asíncronamente con JS.

Les dejo algunas recomendaciones de PageSpeed Insights (by Google):

[Reduce the size of the above-the-fold content](https://developers.google.com/speed/docs/insights/PrioritizeVisibleContent)

# 3. Progressive Enhancement

## La mínima expresión de un producto

De la mano con Critical Path, una página de producto podría tratarse solo de un **título, precio, foto (una), y el botón Comprar**.

Todo eso con sus estilos impresos directamente en el `<head>`.

El resto del contenido puede traerse con JS después del onload (carga de la página).

Entonces, **en el primer request de la página, ya tendríamos impresa la mínima expresión de un producto**.

## No perder el contenido indexable

Para no perder la descripción y demás contenido indexable, podemos especificar lo que necesitemos a través de microdata, e incluirla dentro del primer request.

También podríamos parsear las descripciones de producto que están compuestas enteramente de imágenes, extraer el texto, y usarlo para indexar con ese contenido.

Les dejo un link con toda la información sobre microdata:

http://schema.org/

## No perder el acceso a las secciones adicionales

Para cubrir el caso mínimo de HTML, se pueden incluir links dentro de `<noscript>`, y cargar la sección correspondiente si hay JS:

```
<noscript>
    <a href="/description">Descripción del producto</a>
</noscript>
```
