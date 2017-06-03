---
title: Evitar redundancia de roles ARIA
author: lean
date: 2014-02-24
template: article.jade
topics: code, html
---

Encontré en 2 implementaciones distintas estos casos que me llamaron la atención:

Checkout:

```
<div class="main" role="main">
```

Homepage:

```
<main id="main" role="main">
```

En principio ninguna de las dos está mal. Pero hay algunas definiciones que pueden ser de utilidad en estos casos:

## 1. ARIA role (accesibilidad)

La mayoría de los elementos HTML tienen un `role` por defecto.

Por ejemplo, el role de un `<a>` es `link`, pudiendo hacer:

```
<a href="foo.html" role="link">foo</a>
```

Los browsers que soportan accesibilidad ya definen este rol internamente, por lo que el ejemplo anterior es lo mismo que el siguiente:

```
<a href="foo.html">foo</a>
```

Entonces, para qué sirve el atributo role?: Para **marcar la funcionalidad de un contenido**.

Los ejemplos más claros pueden ser:

```
<header role="banner">
```

Va a contener el encabezado principal de la página. Donde va el logo, título, navegación principal, etc.

```
<form role="search">
```

Va a ser el formulario usado para hacer búsquedas en el sitio.

Basados en eso, el primer caso está ok!:

```
<div role="main">
```

Y el segundo no está mal, pero es redundante:

```
<main role="main">
```

## 2. Div vs. Main

Los divs no le aportan ningún significado a los contenidos que envuelven (igual que los `<span>`). Deberían usarse en casos donde hay una división visual. Donde no se esté haciendo una división semántica del contenido.

El tag `<main>` representa el contenido principal de la página.

> No puede haber más de un main dentro de un body ni puede estar dentro de un article, aside, footer, header o nav.

Entonces, ya que debería haber un solo `<main>` o `role="main"` el primer caso no necesita una `class` definida para CSS:

```
<div role="main">
```

Se pueden aplicar estilos por atributo: `[role="main"] { ... }`

El segundo caso no necesita un `id` definido para CSS:

```
<main role="main">
```

Se pueden aplicar estilos usando un selector por etiqueta: `main { ... }`

---

Es un ejemplo muy chiquito y muy específico, pero lo que quiero que se vea es la importancia de entender para qué sirve cada cosa y poder elegir lo que resuelva mejor el problema.

**Yo para estos 2 casos elegiría un simple `<main>` a secas. Sin clases, roles o ids.**

Algunas referencias:

- [The Roles Model](http://www.w3.org/TR/wai-aria/roles)
- [HTML role attributes](http://knowledge.onsubject.com/html-role-attributes/)
- [Generic containers - the div and span elements](http://www.w3.org/wiki/Generic_containers_-_the_div_and_span_elements)
- [Main - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)
