---
title: Background offset en CSS
description: Cómo reposicionar cualquier background CSS
date: 2014-01-13
template: article.jade
topic: code
lang: es
---

Hoy en día, en el AutoComplete de [Chico UI](http://chico.mercadolibre.com/) (v1.0.0) tenemos un loading spinner agregado como background de CSS, alineado a la derecha como `right center`.

Eso hace que el spinner quede literalmente **pegado al borde derecho**:

![Before](before.png)

Buscando un poco, encontré que `background-position` **puede recibir un offset!**:

```
/* 10px es el offset */
background-position: right 3em bottom 10px;
```

Se incluyó en la especificación de CSS3 y lo soportan todos los browsers, excepto IE8 y anteriores. Más específicamente es soportado en Opera 11+, IE9+, FF 13+, Chrome y Safari.

Aplicando `right 10px center` al AutoComplete, podemos separar el spinner del borde derecho unos 10px:

![After](after.png)

---

### Antes:

```
.ch-autocomplete-loading {
    background: url('../assets/loading-small.gif') no-repeat right center;
}
```

### Después:

```
.ch-autocomplete-loading {
    background: url('../assets/loading-small.gif') no-repeat right 10px center;
}
```
