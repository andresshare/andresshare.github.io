---
layout: post
title:  "🙂 Programacion Funcional"
date:   2018-10-27 20:01:00 +0530
categories: javascript
---

![OOP](https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif)


Al hablar de programación funcional pondré sobre la mesa dos conceptos importantes el primero es resolver problemas por medio de este paradigma, el segundo permite que el valor de salida de una función dependa de los argumentos que son la entrada a la función, así eliminando efectos secundarios como los cambios de estado. Para empezar mira este excelente POST: 

> http://juanmirod.github.io/2017/06/16/introduccion-programacion-funcional-javascript.html

**Funciones de Primera Clase** Cuando decimos Funciones de Primera Clase no hablamos de una Clase como tal, nos referimos al tipo de dato, por ejemplo: un número o una cadena de caracteres puede ser una Función de Primera Clase. Esto significa que podemos tratar Funciones como cualquier tipo de dato (en vez de tomar un número o cadena), no existe ningún método, palabra clave o algo especial para definirlas, en este caso decimos que las funciones se pueden asignar en una variable, objecto o incluso un vector. Veamos unos simples ejemplos en código. un número se puede asignar a una variable y así asignamos una función retornando un número:


```javascript
  var number = function() { return 2120 };
```
* Un número se puede asignar a un espacio en un vector y así una función:

```javascript
  var arrayNumbers = [20, function() { return 24 }];
```

* Un número puede ser asignado a un campo de un objeto y así una función:

```javascript
  var objectNumbers = {
   number: 22, 
   fun: function() { return 24 }
};
```

* Un número puede ser creado como sea necesario y también una función:

```javascript
  20 + (function() { return 24 })(); // => 44
```

* Un número puede ser pasado a una función y así puede hacerlo una función: un número puede ser retornado desde una función y así puede hacerlo una función:

```javascript
  function sumFunc(n, f) { return n + f() }
    sumFunc(20, function() { return 24 }); // => 44
```
* un número puede ser retornado desde una función y así puede hacerlo una función: 

```javascript
return 42;
return function() { return 42 };
```


Como se ve en los ejemplos las Funciones de Primera Clase no tienen nada de especial, solo las tomamos como cualquier otro tipo de dato pero en este caso es una función retornando un valor. Los últimos dos ejemplos le llamamos Funciones de Orden Superior que es el siguiente tema a tratar.

  

**Funciones de Orden Superior** En esta capítulo del Post vamos a extender nuestra idea de Funciones de Primera Clase, aqui voy a describir que las funciones no solo puede ser asignadas a una variable, objeto, vector o pasadas como cualquier tipo de dato, ellas también pueden ser retornadas desde otras funciones. Las Funciones de Orden Superior toman dos acciones claves: toman una función como un argumento y retorna una función como un resultado, fundamental para el paradigma de Programación Funcional, ahora ya estas listo para ver la explicación en código! Vamos a desglosar este tópico en un programa muy sencillo para su buen entendimiento del mismo, vamos allá!


```javascript
var add = function(x) {
    return function(y) {
       return x + y;
    };
};
var sum = add(2);
sum(2); // => 4
```

Bien, ahora vamos a dividir esta explicación en partes:

Primero he asignado una función a una variable llamada **add** como si fuese un tipo de dato (Funciones de Primera Clase que vimos anteriormente), este tipo de funciones son también conocidas como Funciones Anónimas o algunos lenguajes de programación se les conoce como **Lambda**, esta función anónima toma un argumento. Luego dentro del ámbito (Es decir, es un _closure_) de add retornamos otra función anónima con su argumento y así tomando el argumento del closure y la de esta para retornar una suma de los dos argumentos. 

Para llamar la función debemos asignarla a una variable con su respectivo parámetro a la primera función (la asignamos a una variable porque no queremos que se ejecute, si solo ejecutamos la primera función no va a devolver el resultado), luego ejecutamos la segunda función asignandole su respectivo parámetro y listo nos devuelve el resultado.

 Es algo tedioso llamar las Funciones de Orden Superior (te puedes imaginar si tienes muchas más funciones que este simple ejemplo? xD), para esto usamos una técnica llamada **Currying** muy usada en el paradigma de Programación Funcional. Pero que diablos es Currying?  


## Currying

**Currying** es una forma de construir funciones por partes mientras que permita la aplicación parcial de los argumentos de una función. Es decir podriamos pasar todo los argumentos de una función en partes y ejecutarla de una vez, muy simple y así reduce la complejidad en el código, vamos a ejecutar el ejemplo de arriba usando Currying, veamos! 


```javascript
var add = function(x) {
    return function(y) {
        return x + y;
    };
};

add(2)(2); // => 4

```


Muy simple! así solo tenemos que llamar la función una sola vez pasandole los argumentos o resto de elementos a las funciones en parcial. 

En lenguajes como Haskell, Scala, ya vienen por default con esta feature ya que son lenguajes funcionales totalmente, en cambio en JavaScript no viene por default, la técnica de Currying se aplica como un tipo de truco o hack para hacerlo trabajar como Currying. Sin embargo podemos usar alguna librería Open Source que nos facilite mucho la vida para estos procesos funcionales, voy a tomar el mismo ejemplo pero usando Lodash, vamos alla! 

```javascript

var add = _.curry(function (x, y) {
    return x + y;
})

add(2)(2); // => 4

```

El método curry de Lodash toma una función como argumento (un callback) transformando los argumentos de este callback en una función Currying. Map, Reduce y Filter Pues si, JavaScript tiene funciones pre-construidas (a partir de ES5) que toman una función como argumento y retornan un valor y esas funciones son **map(), reduce() y filter()** para vectores, veamos un ejemplo de cada una tomando esta simple estructuras de datos: 
```javascript
var students = [
    { name: 'Anna', grade: 6 },
    { name: 'John', grade: 4 },
    { name: 'Maria', grade: 9 }
]; 

```

### filter() 

```javascript
students.filter(function(student) {
    return student.grade >= 6;
});
```
// [ { name: 'Anna', grade: 6 }, { name: 'Maria', grade: 9 } ]
### con map() 

```javascript
students.map(function(obj) {
    return obj.name;
}); 

// [ 'Anna', 'John', 'Maria' ]
````
### reduce()

```javascript
students.reduce(function(sum, student) { 
    return sum + student.grade;
}, 0)
// 19
```

Encadenando métodos Como vemos **map(), reduce() y filter()** son Funciones de Orden Superior que vienen en el core de JavaScript, estas funciones toman datos de un vector pasandolo al callback y retornan un valor transformado sin mutar el vector original, luego veremos en profundida la parte de las Funciones Puras e Immutabilidad, la próxima parada es para la Composición de Funciones. 

```javascript
students
  .filter(function (student) { 
    return student.grade >= 6 
  })
  .map(function (obj) {
    return obj.name;
  })

// ['Anna', 'Maria']

```
  
 

---

> mas info y autor de este post: https://medium.com/elblogdejavascript/programaci%C3%B3n-funcional-5da872a080fe



