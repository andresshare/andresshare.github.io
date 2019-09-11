---
layout: post
title:  "Que es un callback?"
date:   2014-05-17 20:15:01 +0530
categories: javascript
---

![OOP](https://media.giphy.com/media/35Kf7OnQCkPj2Ojtf6/giphy.gif)

Que cuando cierta función termina de realizar todo lo que tiene que hacer, ejecutará una función que le fue pasada como argumento. 


```javascript
function primerPaso(callback) {
console.log("Este es el primer paso");
callback();
};
function segundoPaso() {
console.log("Este es el segundo paso");
};
primerPaso(segundoPaso);
```

---


Todavía hay un montón de diferentes tipos de funciones por ahí. Ya sabe acerca de las arrow function, pero ¿qué pasa con las callback funcions 

Se habla mucho de las funciones de callback, pero ¿qué es exactamente un callback? Para abreviar, 
un **callback** es básicamente una función que se llama cuando sucede algo. Por ejemplo, cuando alguien envía un formulario en su sitio web, debe ejecutar validaciones, lo que significa que hay algunas funciones que deben ejecutarse en segundo plano.

Entonces, cuando el usuario envió el formulario, esa acción activó **callback**  que inició todas las validaciones. Si no estaba utilizando un **callback**, su código quedaría bloqueado en las validaciones y se quedaría allí hasta que alguien enviara un formulario. Definitivamente esa no es la forma en que desea que se comporte su sitio web.

Un **callback** permite ejecutar su código hasta que un evento lo active. Luego se ejecuta la devolución de llamada y luego vuelve a su función original. Aquí hay una ilustración de una función de devolución de llamada en acción:

![callback](https://media.giphy.com/media/LR0xmepPAZA09fgbdz/giphy.gif)

Puede ver que **callback** está esperando hasta que algo suceda antes de que haga algo y, tan pronto como **callback** vuelve,el código vuelve a hacer cosas. 

Eso es realmente todo lo que hay para la función de devolución de llamada. Sí,eso es realmente todo lo que es.

