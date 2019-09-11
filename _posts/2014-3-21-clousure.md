---
layout: post
title:  "🤔 Que es clousure?"
date:   2014-03-21 10:30:01 +0530
categories: Concepto javascript
---

![OOP](https://media.giphy.com/media/ReImZejkBnqYU/giphy.gif)


Un closure es una función que es libre de variables, esto quiere decir que las variables de la función padre funcionan, pero el closure no tiene variables propias. 

```javascript
function padre() {
var a = 1;
function closure() {
console.log(a);
}
closure();
}
padre();

```


 Profundicemos ,un **clousure** es una función con estado que es devuelta por otra función. Actúa como un contenedor para recordar variables y parámetros de su ámbito principal, incluso si la función principal ha terminado de ejecutarse. Considere este simple ejemplo.

```js
function sayHello() {
  const greeting = "Hello World";

  return function() { // anonymous function/nameless function
    console.log(greeting)
  }
}


const hello = sayHello(); // hello holds the returned function
hello(); // -> Hello World
```

¡Observe! ¡Tenemos una función que devuelve una función! La función devuelta se guarda en una variable e invoca la línea a continuación.

### ¡Muchas formas de escribir el mismo código!


Ahora que sabe qué es un clousure en un nivel básico, aquí hay algunas formas de escribir el mismo código que el anterior

```js
// original
function sayHello() {
  const greeting = "Hello World";

  return function() { // anonymous function
    console.log(greeting)
  }
}


// #1
function sayHello() {
  const greeting = "Hello World";

  return function hello() { // named function
    console.log(greeting)
  }
}


// #2
function sayHello() {
  const greeting = "Hello World";

  function hello() { // named function
    console.log(greeting)
  }

  return hello; // return inner function on a different line
}


// #3
function sayHello() {
  const greeting = "Hello World";
  const hello = () => { // arrow function
    console.log(greeting)
  }

  return hello;
}
```


¡Elija un estilo que más le guste y manténgalo porque todas las variaciones anteriores seguirán imprimiendo el mismo resultado!

```js
const hello = sayHello();
hello(); // -> Hello World
```


### Beneficios de clousure y cómo puede ser práctico



**Private Namespace**

Es genial que la función interna recuerde el entorno en el que se creó, pero ¿qué uso tiene? Una pareja. Primero, puede mantener sus variables privadas. Aquí está el clásico ejemplo contrario.

```js
function counter() {
  let count = 0;
  return function() {
    count += 1;
    return count;
  }
}


const increment = counter();
console.log(increment()); // 1
console.log(increment()); // 2
console.log(count) // Reference error: count is not defined
```

Intentar acceder a la variable de conteo nos da un error de referencia porque no está expuesto al entorno global. Lo que nos ayuda a reducir los errores porque nuestro estado está más estrictamente controlado por métodos específicos


**Estados reusables**


```js
function counter() {
  let count = 0;
  return function() {
    count += 1;
    return count;
  }
}

const incrementBananaCount = counter();
const incrementAppleCount = counter();
console.log(incrementBananaCount()); // 1
console.log(incrementBananaCount()); // 2
console.log(incrementAppleCount()); // 1

```

**Modulo diseño patrones**

El patrón de diseño del módulo es una convención popular para diseñar sus aplicaciones JavaScript. Utiliza IIFE (Expresión de función invocada inmediatamente) para devolver objetos y expone solo las variables y métodos que desea hacer públicos.

```js
let Dog1 = (function() {
  let name = "Suzy";

  const getName = () => {
    return name;
  }

  const changeName = (newName) => {
    name = newName;
  }

  return {
    getName: getName,
    changeName: changeName
  }
}())

console.log(name); // undefined
Dog1.getName() // Suzy
Dog1.changeName("Pink")
Dog1.getName() // Pink
```

Tan pronto como se ejecuta este código, la función se ejecuta y devuelve un objeto que se guarda en Dog1. Este patrón vuelve a mantener nuestro espacio de nombres privado y solo revela lo que queremos como métodos y variables públicas a través de la forma de un objeto. ¡El estado está encapsulado!

**La pregunta famosa en entrevistas**

![closure](https://media.giphy.com/media/xT0GqssRweIhlz209i/giphy.gif)

¿Cuál es el resultado de ejecutar la siguiente función?
```js
for(var i=0; i<5; i++) {
  setTimeout(function() {
    console.log(i)
  }, 1000)
}
```
¿Por qué es esta una pregunta de entrevista tan popular? ¡Porque pone a prueba su conocimiento del alcance de la función / alcance del bloque, cierre, setTimeout y función anónima! La respuesta imprime cinco 5 después de 1 segundo.

```
5
5
5
5
5
```

¿Cómo? Bueno, setTimeout se ejecuta 5 veces en el ciclo después de 1 segundo. Después del retraso de tiempo, ejecutan funciones dentro, lo que simplemente cierra la sesión i. Cuando ha pasado 1 segundo, el ciclo ya terminó y me convertí en 5. Se imprimen cinco 5s. ¿No es lo que esperabas? Probablemente quiera ver los números 1 a 5 de forma iterativa.

**La respuesta**


Hay algunas soluciones, ¡pero centrémonos en usar el cierre!

```js
for(var i=0; i<5; i++) {
  setTimeout((function(index) {
    return function() {
      console.log(index);
    }
  }(i)), 2000)
}
```
Tenemos nuestro closure que es devuelto por una función anónima para recibir 'i' actuales como argumentos y generarlos como 'index'. Al hacerlo, captura la variable actual i para cada función. y muestra el resultado

```
0 (...1000ms have passed)
1 (...1000ms have passed)
2 (...1000ms have passed)
3 (...1000ms have passed)
4 (...1000ms have passed)
5 (loop exits)
```

¡Felicidades! 🎉 ¡Ahora está más preparado para su próxima entrevista! 😉 Solo recuerde que 

> El clousure es una función que tiene acceso al alcance que encierra esa función.

