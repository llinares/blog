---
title: Evitar redundancia de roles ARIA
author: Lean Linares
date: 2014-02-24
template: article.jade
tags: code, html
---

Encontré en 2 implementaciones distintas estos casos que me llamaron la atención:

Checkout flow:

```
<div class="main" role="main">
```

Homepage:

```
<main id="main" role="main">
```

Si bien no están mal, hay algunas definiciones que pueden ser de utilidad en estos casos:

# 1. ARIA role (accesibilidad)

La mayoría de los elementos HTML tienen un *role* por defecto.

Por ejemplo, el rol de un `<a>` es `link`, pudiendo hacer:

```
<a href="foo.html" role="link">foo</a>
```

Los browsers que soportan accesibilidad ya definen este rol internamente, por lo que sería lo mismo hacer:

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

Entonces:

```
<div class="main" role="main"> <!-- Está ok! -->
<main id="main" role="main"> <!-- No está mal, pero es redundante. -->
```

# 2. Div vs. Main

Los divs no le aportan ningún significado a los contenidos que envuelven (igual que los `<span>`).

Deberían usarse en casos donde hay una división visual. Donde no se esté haciendo una división semántica del contenido.

El tag `<main>` representa el contenido principal de la página.

**No puede haber más de un main dentro de un body ni puede estar dentro de un article, aside, footer, header o nav.**

Entonces, ya que debería haber un solo `<main>` o `role="main"`...

```
<div class="main" role="main"> <!-- No necesita class para CSS. Uso: [role="main"] {...} -->
<main id="main" role="main"> <!-- No necesita id para CSS. Uso: main {...} -->
```

Además este caso:

```
<div class="main" role="main">
```

...podría ser directamente un `<main>` (excepto si no cumple los requisitos).

# Conclusión

Es un ejemplo muy chiquito y muy específico, pero lo que quiero que se vea es la importancia de entender para qué sirve cada cosa y poder elegir lo que resuelva mejor nuestro problema.

Yo para estos 2 casos elegiría un simple `<main>`. Sin clases, roles o ids.

# Referencias

- [The Roles Model](http://www.w3.org/TR/wai-aria/roles)
- [HTML role attributes](http://knowledge.onsubject.com/html-role-attributes/)
- [Generic containers - the div and span elements](http://www.w3.org/wiki/Generic_containers_-_the_div_and_span_elements)
- [Main - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main)
