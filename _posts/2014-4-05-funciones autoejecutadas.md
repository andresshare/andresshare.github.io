---
layout: post
title:  "Que son las funciones autoejecutadas"
date:   2014-04-02 23:45:04 +0530
categories: javascript
---

![OOP](https://media.giphy.com/media/3ohze3pdoPu1xXSmmQ/giphy.gif)

Encapsula el código y previene que pueda ser alterado desde el exterior. 

```javascript
(function() {
console.log("hola MENSAJE/a")
})()
```

----
 Según wikpedia, un IFFE es «un lenguaje de lenguaje de programación JavaScript que produce un alcance léxico utilizando el alcance de la función de JavaScript».

Pero supongamos que el alcance léxico, la elevación variable y el alcance de la función no son términos con los que no este claro el conceptoa, no se preocupe, veamos qué hace realmente un IFFE, con ejemplos, un paso a la vez

Básicamente y IIFE es:

- Una función
- evaluado inmediatamente
- devolviendo un objeto
- con atributos públicos (métodos y valores)
- que puede referirse a los no públicos
- y no exponiendo a los privados

```js
f1 = function(){
  let secret_a = 1;
  function secret_b(){
    return 2;
  }

  return { public_a: secret_a, public_b: secret_b };
}

let obj1 = f1()

console.log('obj1.public_a: ' + obj1.public_a);         // obj1.public_a: 1
console.log('obj1.public_b: ' + obj1.public_b());       // obj1.public_b() 2
console.log('obj1.secret_a: ' + typeof(obj1.secret_a)); // obj1.secret_a: undefined
console.log('obj1.secret_b: ' + typeof(obj1.secret_b)); // obj1.secret_b: undefined
```
Ahora imagine que reemplazamos f1 con todo lo que estaba a la derecha de f1 =

```js
let obj2 = (
  // here starts f1
  function(){
    let secret_a = 1;
    function secret_b(){
      return 2;
    }

    return { public_a: secret_a, public_b: secret_b };
  } 
  // here ends f1
)()

console.log('obj2.public_a: ' + obj2.public_a);         // obj2.public_a: 1
console.log('obj2.public_b: ' + obj2.public_b());       // obj2.public_b() 2
console.log('obj2.secret_a: ' + typeof(obj2.secret_a)); // obj2.secret_a: undefined
console.log('obj2.secret_b: ' + typeof(obj2.secret_b)); // obj2.secret_b: undefined
```


Esto tiene el mismo efecto, y ya reconocemos la famosa forma IIFE.

```js
(function(){ ... })()
```

Pero un IIFE no solo puede devolver un nuevo objeto, también puede agregar cosas a uno:

```js
let obj3 = { prop1: 3 };

let obj4 = (function(expose){ // we call expose what comes from outside
  function secret_b(){
    return 2;
  }

  expose.public_b = function(){ // we add properties to expose
    return secret_b() + expose.prop1; // and read from it
  }

  return expose; // we return the received object with extra stuff
})(obj3); // we call the IIFE with some object

console.log('obj4.prop1: ' + obj4.prop1);         // obj4.prop1: 3
console.log('obj4.public_b: ' + obj4.public_b()); // obj4.public_b() 5
```


Observe que hubo cuatro cambios aquí:

- let obj4 = (función (exponer) {nombramos el argumento que esperamos
- expose.public_b = function () {agregamos cosas al objeto recibido
- return expose; devolvemos el objeto enriquecido
- }) (obj3); llamamos al IIFE con una discusión desde afuera


Pero hoy en día, todo el mundo está cargando varios archivos que tienen pipelines complejas, y aquí IIFES puede ayudarlo a enriquecerse:

```js
// file 1
MyObj = (function(expose){
  let secret_b = 4;

  expose.public_b = function(){
    return secret_b;
  }
  return expose;
})(window.MyObj || {});

// file 2
MyObj = (function(expose){
  expose.public_c = function(){
    return expose.public_b() + 5;
  }
  return expose;
})(window.MyObj || {});

console.log('myObj.secret_b: ' + typeof(MyObj.secret_b)); // myObj.secret_b(): undefined
console.log('myObj.public_b: ' + MyObj.public_c());       // myObj.public_b() 9

```

Esto funciona para cualquier archivo de pedido 1 y el archivo 2 se carga, por lo que puede tener algunas cosas básicas / compartidas en su objeto y aumentarlas según sea necesario en ciertas páginas, pero solo si el usuario las carga.

Esto puede volverse bastante loco pronto, por lo que es mejor imponerle algunas convenciones, para que sepa qué esperar y dónde colocar las cosas:

```js
// Use you company or app name here to keep or your stuff namespaced
// separatedly from 3rd party libraries
window.Namespace = window.Namespace || {};

// Componen documentation
// What it does: functional description
// Example usage:
//   Namespace.Component.init({ selector: '#some_id', some_param: 30 });
window.Namespace.Component = (function(expose){
  let private_some;

  function private_helper(){
    // stuff
  }

  expose.public_method = function(){
    // stuff
  }

  expose.init = function(options){
    private_some = option.some;
  }

  return expose;
})(window.Namespace.Component || {});
```

se puede usar

```js
Namespace.Component.init({
  selector: '#some_id',
  some_param: 30
});
```


En sus archivos html para que tenga la definición del selector y la referencia en el mismo lugar, fácil de modificar si el html necesita cambiar.

Además, recomendaría usar siempre clases de estilo 'js-xxxx' e identificadores (o atributos de datos) para que no interfieran con las tareas de diseño / diseño.


