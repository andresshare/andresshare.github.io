---
layout: post
title:  "Que es prototype"
date:   2014-04-01 22:15:04 +0530
categories: javascript
---

![OOP](https://media.giphy.com/media/dXICCcws9oxxK/giphy.gif)



todos los objetos en JavaScript provienen de Object; todos los objetos heredan métodos y propiedades de Object.prototype, aunque pueden ser sobrecargados. Sin embargo, un Object puede ser deliberadamente creado para que esto no sea cierto (por ejemplo usando Object.create(null)), o bien alterado para que no cumpla esta propiedad (por ejemplo usando Object.setPrototypeOf). 