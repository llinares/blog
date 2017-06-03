---
title: Dudas comunes de microdata
author: lean
date: 2016-04-19
template: article.jade
topics: code, html
---

Me gustaría aclarar algunas dudas acerca de cómo usar Microdata, ya que recibí varias consultas sobre los mismos temas.

## FAQ 1

A veces hay data en forma de meta tags:

```
<meta itemprop="price" content="123.45"/>
```

Otras veces, hay data en elementos comunes:

```
<span itemprop="priceCurrency" content="ARS">$</span>
```

### ¿Cuál es la correcta?

Según la doc de [schema.org](http://schema.org/) **la data se agrega a los elementos comunes**. Y los meta tags son solamente para aquellos casos en los que:

> ...a web page has information that would be valuable to mark up, but the information can't be marked up because of the way it appears on the page.

## FAQ 2

¿Qué pasa si tengo, por ejemplo, muchos `itemprop="price"` en una misma página?

Esta ok, pero todo depende del scope que se le defina a su contenedor.

Los scopes pueden anidarse y se recomienda que su "tipo" esté definido:

```
<div itemscope itemtype="http://schema.org/Product">
```

Les recomiendo echarle un vistazo al [Getting started de Schema.org](http://schema.org/docs/gs.html). Muy completo y no lleva más de 5 minutos de lectura.
