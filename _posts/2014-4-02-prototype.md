---
layout: post
title:  "Que es prototype"
date:   2014-04-01 22:15:04 +0530
categories: javascript
---

![OOP](https://media.giphy.com/media/dXICCcws9oxxK/giphy.gif)



Todos los objetos en JavaScript provienen de Object; todos los objetos heredan métodos y propiedades de Object.prototype, aunque pueden ser sobrecargados. 

Sin embargo, un Object puede ser deliberadamente creado para que esto no sea cierto (por ejemplo usando Object.create(null)),

o bien alterado para que no cumpla esta propiedad (por ejemplo usando Object.setPrototypeOf). 

---

### Aclaremos un poco a Prototype
Cada vez que creamos una función en javascript, el motor de javascript crea dos objetos para nosotros.

Los dos objetos que se crean cuando el motor Js procesa la función son,

- Function object  que incorpora la función misma

- Prototype Objects


Prototype en Js se usa principalmente para la herencia, agrega métodos y propiedades en la propiedad prototipo de una función para que esos métodos y propiedades estén disponibles para las instancias de esa función.

```js
function foo() {
console.log("Hello!!");
}
// foo.prototype
```

Cada vez que el motor Js crea el objeto Prototype, también crea una propiedad en función llamada Prototype. Con la ayuda de esta propiedad prototipo en función, podemos acceder al objeto Prototype creado para esa función.

Por ejemplo, hemos visto la función foo que tiene una propiedad llamada Prototype que apunta al objeto Prototype. Para hacer uso del objeto Prototype, creamos un objeto utilizando la nueva palabra clave.

```js
var myObj = new foo();
// myObj
```
Cuando creamos un objeto, el motor myObj Js crea un objeto para nosotros que por defecto tiene un objeto llamado "proto". Que a su vez apunta al objeto  inicial creado por la función.

**A Mover codigo**

Ahora que sabemos que hay un Prototype creado por el motor Js cada vez que creamos un objeto para ver cómo funciona, creemos una propiedad "decir" en el objeto "myObj" con el valor "Hi from myObj itself".

```js

function foo(){}
var myObj = new foo();
myObj.say = "Hi from myObj itself";
```

Cuando accedemos a "myObj.say" sabemos que devolverá el valor "Hi from myObj itself". Creamos otro objeto para el Prototype con la misma propiedad pero con un valor diferente "Hi from proto object"

```js
function foo(){}
var myObj = new foo();
myObj.__proto__.say = "Hi from proto object";
```

> Accediendo al "myObj.proto.say" devolverá "Hi from proto object".

```js
function foo(){}
var myObj = new foo();
myObj.say = "Hi from myObj itself";
// Hi from myObj itself
myObj.__proto__.say = "Hi from proto object";
// Hi from proto object
delete myObj.say;
// true
myObj.say
// Hi from proto object
```

Pero cuando eliminamos el "myObj.say" y accedemos al mismo, el motor Js mira el objeto "proto" para ver, si hay alguna propiedad "decir". Que encontrará la propiedad "myObj.proto.say", con el valor "Hola del objeto proto" y se devolverá al acceder a "myObj.say".


Ahora que sabemos cada vez que creamos un objeto, el motor Js crea otro objeto para nosotros llamado prototipo. Podemos acceder al prototipo usando ".prototype" desde la función. Pero cuando creamos un objeto usando una nueva palabra clave, Js crea "proto", que apunta al objeto prototipo.

Cada vez que buscamos una propiedad en un objeto, el motor Js la devolverá, si la encuentra en el objeto mismo. Si no existe tal propiedad, el motor Js buscará el objeto prototipo

