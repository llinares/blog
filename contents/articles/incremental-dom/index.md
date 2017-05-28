---
title: Incremental DOM
author: Lean Linares
date: 2015-07-27
template: article.jade
---

Google estuvo mejorando uno de los mejores features de React: el virtual DOM.

Cuando una Single Page App re-renderiza una vista completa, se redibujan elementos que quizás no cambiaron.

# Virtual DOM

Es básicamente un DOM paralelo, en el que se aplica el redibujo de la vista completa.

Entonces se analizan cuales son las diferencias y se aplica al DOM real solo lo que cambió.

Esto significa un aumento considerable en la velocidad de render.

La desventaja es que cuando el DOM tree es grande, la performance sufre por tener que replicar todo el DOM.

# Incremental DOM

Google redujo el uso de memoria de esta forma:

> "While creating the new (virtual) DOM tree walk along the existing tree and figure out changes as you go. Allocate no memory if there is no change; if there is, mutate the existing tree (only allocating memory if absolutely necessary) and apply the diff to the physical DOM."

Les dejo el link del artículo:

https://github.com/google/incremental-dom﻿
