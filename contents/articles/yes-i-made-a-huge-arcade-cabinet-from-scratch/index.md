---
title: Yes, I made a huge arcade cabinet from scratch
description: It took me over a year, but teach me a lot on the road. Here every detail behind building an entire arcade machine from the very scratch.
date: 2017-10-03
template: article.jade
topics: diy
lang: en
draft: true
---

Everithing started back in 2013, when i suddenly won a raspberry pi (a model 1 btw) on an unspected concourse. I never win annyting and actually I never suscribed to this concourse. All I know is one day an email comes up saying i just wno a raspberry pi:

[!The Raspberry Pi that I won]()

That must be the very best for a maker and that, but I really didnt know what to build.

Everytime I looked for something I found so many shit.

## RetroPie

gdsgd

So I installed, and uploaded some roms to test.

suddenly I was playing Super Mario Bros. 3 on my tv 😱

[!Super Mario Bros. 3 running on RetroPie]()

I [tried and tried and trid](#) until it workds.

---

## The idea

Finnaly got something good use for that polvojuntadorea plaqueta.

so busque por todos lados gabinetes hechos mierda para restaurar, pero eran extremadamente caros y literalmente hechos mierda, irrecuperables y dificiles de transportar y de un tamaño no apto para un depto.

[!arcade feo]()

## Open Source all the things!

despues de buscar imagenes de lo que seria un arcade ideal, encontre qeu mucha gente construia sus propios arcades.

y no solo eso, sino que habia disponibles planos open source para construir un arcade.

asi fue como llegue a [project mame](http://www.koenigs.dk/mame/eng/draw.htm) de koenigs.

aunque estaba hecha para soportar un joystick comprado y un teclado, era una adaptacion que estaba preparada para recibir un monitor flat. un viejo conocido transformado a los tiempos modernos.

por suerte encontre [alguien](http://zonaarcade.forumcommunity.net/?t=48865036) que no solo mejoro levemente el modelo, sino que [mejoro los planos](http://img543.imageshack.us/img543/5624/repordiviciacosplanos.gif) y armo un [modelo 3d]() en [Google SketchUp](https://www.sketchup.com/):

[!Paper Mario Arcade Cabinet]()

De paso también compartió el [sideart](http://zonaarcade.forumcommunity.net/?t=45015457), aunque preferi no usarlo.

no todo es color de rosas. los planos me resultaron algo complicados de seguir, por lo que preferi armar mis propios [planos detallados]().

[!Detailed plans based on pr]()

---

## Wood

mdf or melamina. busque tutoriales en video y escritos sobre como trabajar ambos materiales.

algunas caracteristicas que encontre de trabajar con ambos materiales:

### MDF

-

### Melamine

-

la verdad es que si hubiese sabido lo fino que es el aserrin del mdf y lo dificil de pintar, hubiese elegido la melamina. pero como para ser inteligente hay que cometer muchos errores, use mdf.

[!MDF assrrine]()

### The thickness

i found que las maquinas originales eran de 18mm (x inches) de grosor. pero cualquier tipo de madera de ese grosor seria pesadisima. asi que despues de mucho buscar, decidi que el grosor ideal era 15mm (x inches) por la relacion peso/tamaño.

[!mdf 15mm]()

### The method

de tantos tutoriales llegue a  2 tecnicas con las que se pueden unir perpendicularmente 2 maderas.

#### Direct

la primera forma que se nos viene a todos a la cabeza: hacer un agujero mientras alguien nos ayuda a sostener la madera en su lugar, y encontes apretar los tornillos mientras esa otra eprsona sigue manteniendo en su lugar la madera.

[!chabon sosteniendo madera]()

#### Slats

listones que se atornillan primero, apoyados contra la madera. la segunda madera se atornilla sobre el liston tambien.

de esta forma el liston es quien une ambas maderas con una **precision milimetrica y sin necesitar ayuda alguna**.

[!the top corner of the arcade cabinet, holded by slats]()

the use of cola vinilica no es necesaria. yo elegi usarla, pero fue totalmente innecesaria ya que los tornillos ajustan la madera perfectamente. si planeas desarmar las maderas, entonces **no las pegues** pues sera totalmente imposible despegar mdf una vez curado.

i tried myself to despegar una pieza de madera de la cual me arrepenti poner, para cambiarla una mas chica. termine casi destrozando ña madera entera.

compre bocha de listones de pino de 4x2 un poco mas chicos que las piezas que unirian:

foto listones

### ranura t

---

## Hardware

ademas de la obviamente basica raspberry pi que tenia muchas ganas de usar, necesite algunas otras partes. Trate de usar las piezas que ya tenia disponibles en casa, para evitar comprar la mayor cantidad de hardware posible.

### Screen

tenia un monitor LCD bastante viejo, un sambusn t260n de 26" asi que decidi usarlo. es gigante para los oled que estamos acostumbrados, pesado, without contrast cuando lo miras de costado y too big para mostrar juegos de 100x100px cuando emulas una NES. Pero es esa antiguedad mezclado con modernidad lo que hizo que no me imprtaran esas imperfecciones. Ademas me estaba ahorrando unos cuantos dolares.

[!the monitor used in the arcade cabinet]()

there was a constrain, este monitor fue concebido para ser bello en su parte trasera, por lo que no posee tornillos para amurarlo y solo puede ser usado con su base.

[!the back part of monitor]()

Busque y por suerte encontre un soporte (no oficial ni estandar) para ese monitor. es un reemplazo del pie, que genera el agarre de un soporte comun y corriente:

[!the support mounted]()

### Subwoofer

i remember when i first get a job. lo primero que hice fue comprar tecnologia, y una de las primeras cosas que siepre quise era un subwoofer para escuchar musica.

el mejor subwoofer que encontre en relacion precio/calidad en 2007 fue el genius 23131241. beautiful and clean sound as the price of a Genius periferic. me acompaño toda la vida: quien iba a pensar que 9 años despues lo convertiria en algo aun mas interesante.

[!genius 432423]()

### Xin-mo controller

todo el mundo en internet recomendaba sanwa... cuando busque, son realmente caros... es lo mejor de lo mejor, pero no amerita para construir un arcade casero.

[!xin-mo controller]()

tambien compre la placa para concectarlo via usb pero hace poco me hicieron dar cuenta que no es necesaria si se sueldan los cables directamente al input ede la raspberry pi.

[!controller soldado a raspberry pi ]()

### LED light tube

iba a poner una tira de led, pero el tuvo phillips de 58cm (x inches) de largo tiene todo resuelto, incluso el enchufe universal

### An stabilizator

otra de las primeras cosas que me compre, para cuidar todos mis electrodomesticos fue el estabilizador atomlux dsadsad, que hasta hoy nunca me fallo.

[!atomlux dsad]()

tiene 6 entradas, 2 de las cuales estan filtradas, asi que las use para el monitor y los parlantes, que son ambos los responsables de la mayor cantidad de interferencia generada.

---

## Materials

### Wood

compre la madera segun el plano

detalle de pedazos con medidas

foto con las maderas contra la pared

la marque toda, incluso usando un compas viejo del colegio para las curvas

foto de curvas dibujadas

### Screws

dsa

### Press


### Tape

### wheels

---

## maqueta

foto coso de carton

---

## Cutting

### Needed

caladora de un amigo carpintero link al coso de seba

barbijo

anteojos

### cortes

pegue las 2 maderas grandes

foto maderas antes

foto contra la pared del primer corte

tambien incli un corte para mas adelante poder colocar ruedas, que solo se apoyen cuando el gabinete es apoyado hacia atras.
foto corte ruedas

### listones

foto listones

### cosas que aprendi

- **mdf larga polvillo muy fino:** por mas que usara proteccion, lo respire, me quedaba en el pelo y en la ropa por dias. Era imposible de barrer e incluso me arruino una aspiradora de mano.
  foto del aserrin
- **la sierra caliente quema la madera:** es mejor dejar descansar la sierra cada 2-3 minutes. Sino la madera se quema de tanta temperatura que tienela sierra.
  foto de partes quemadas de la madera
- **la sierra se curva:** cuanto mas lejos de la caladora estas cortando, mas se curva la cierra, y genera un corte diagonal que no queremos. asi que es mejor cortar 2 piezas iguales por separado que sumar el alto de las 2 piezas, ya que la segunda va a hacer que la cierra se curve.

## Lijing

nunca la pase tan mal como lijando madera. actually la pase peor lijando pintura, pero ya vamos a llegar a esos errores que cometi.

foto en la pared lijados

---

## juntando todo

### listones

despues de cortarlos use esta tecnica para atornillarlos milimetricamente sin ayuda:


---

## controllers place

---

mecha

aguheros maderas

acrilico

---

## detalles

parlantes agujersos

ptapa parlantes detalle y por que

mencionar que probe todo en la maqueta


---

## acrilicos

---

## configuracion

post
