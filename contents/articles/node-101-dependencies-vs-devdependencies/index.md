---
title: Node 101 - dependencies vs. devDependencies
description: Definición totalmente básica sobre las dependencias de Node JS.
date: 2016-08-12
template: article.jade
topics: code
lang: es
---

Es un tema bastante básico pero que veo que se repite en varias implementaciones. Me encontré con varios package.json en los que las dependencias no están ubicadas en el lugar correcto. Suelen estar todas en `"dependencies"` o todas en `"devDependencies"`. A veces también las veo bastante mezcladas.

En realidad hay diferencia.

## Dependencies

Son recursos que van a formar parte de los files descargables. Es decir que, cuando alguien instale el módulo, va a descargar también todas esas dependencias.

Un ejemplo correcto sería:

```
"dependencies": {
  "jquery": "2.2.1",
  "backbone": "1.2.3",
  "backbone.marionette": "2.4.4",
  "underscore": "1.8.3"
}
```

## Dev dependencies

Son recursos que se van a usar **solo para desarrollar el módulo**.

Es decir que, cuando alguien lo instale, no va a necesitar descargar todas estas dependencias.

Éstas pueden ser herramientas de tests, de documentación, task runners, etc.

Un ejemplo correcto sería:

```
"devDependencies": {
  "mocha": "2.3.4",
  "gulp": "3.9.1"
}
```

Para más info, les dejo la [doc oficial de npm](https://docs.npmjs.com/files/package.json#dependencies).
