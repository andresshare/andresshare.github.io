---
layout: post
title:  "Recursividad"
date:   2019-01-17 15:00:36 +0530
categories: Javascript
---

![recursivad](https://media.giphy.com/media/pX4qCZekYXTYQ/giphy.gif)

* La recursividad consiste en funciones que se llaman a sí mismas, evitando el uso de bucles y otros iteradores.


```javascript
function factorial(n) {
    if (n<=1) return 1;
    return n* factorial(n-1);
}

//other way
const U = f => f (f)

const Y = U (h => f => f (x => U (h) (f) (x)))

const factorial = Y (f => x =>
  x === 0 ? 1 :  x * f (x - 1))

console.log (factorial (5)) // 120

```
**APLICACION**

> El ejemplo típico sería el recorrer un árbol de elementos para hacer algo con todos ellos. Imagínate un sistema de archivos con carpetas y subcarpetas y archivos dentro de estas carpetas, o el árbol de elementos (DOM) de una página web donde unos elementos incluyen a su vez otros y no sabes cuántos hay en cada uno. En este tipo de situaciones la manera más eficiente de hacer una función que recorra todos los elementos es mediante recursión. Es decir, creas una función que recorra todos los elementos hijo del nodo que le pases y que se llame a sí misma para hacer lo mismo con los sub-nodos que haya. En el caso del sistema de archivos le pasarías una carpeta y se llamaría a sí misma por cada subcarpeta que hubiese, y así sucesivamente con todas las demás. Con una sola llamada inicial recorrerá automáticamente toda la estructura del sistema de archivos.