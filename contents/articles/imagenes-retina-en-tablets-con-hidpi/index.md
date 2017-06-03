---
title: Imágenes retina en tablets con HiDPI
author: lean
date: 2015-06-11
template: article.jade
topics: code, css
---

Revisando una landing page en el trabajo nos dimos cuenta que, así como estamos prestándole atención a pantallas retina en nuestra version *mobile* del sitio, deberíamos hacerlo en nuestra versión *desktop*.

El problema surge a partir de que servimos la version *mobile* sólo para teléfonos celulares. Y ya que la resolución de pantalla de las tablets son similares a la de un monitor de escritorio, ambos comparten la version *desktop* del sitio.

La gran mayoría de tablets que probamos tienen pantalla con alta densidad de pixels (HiDPI). Entonces cualquier imagen que vemos en las tablets más usadas, hoy en día está aumentada y pixelada.

Deberíamos asegurarnos de cubrir los siguientes casos:

- Imagen común para **mobile**.
- Imagen retina para **mobile@2x**.
- Imagen común para **desktop**: *En algunos casos se puede aprovechar la mobile@2x.*
- Imagen retina para **desktop@2x**: *En algunos casos podría ser la original a 4x.*

Para implementarlas, yo vengo usando las imágenes como background y re-defino los valores dentro de esta media query:

```
@media(-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi), (min-resolution: 2dppx) {
```

Sólo lo venía haciendo para *mobile*. Tendríamos que hacer exactamente lo mismo en *desktop*.

También, cuando las circunstancias nos lo permita, la opción más viable puede ser usar SVG (imágenes vectoriales). Son más simples de exportar y de implementar, y se escalan al tamaño que se necesite sin pérdida de calidad. Los browsers más viejos (ie8, android 2.x) no soportan SVG, pero el fallback es simple de implementar con una imagen.

Sé que también se está trabajando en un estandar de implementación para imágenes multi-size: http://html5hub.com/html5-picture-element/

No me acuerdo en que estado está, pero es bastante reciente.
