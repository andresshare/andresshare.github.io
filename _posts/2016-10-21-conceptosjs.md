---
layout: post
title: "Conceptos JS"
date: 2016-10-20 20:9:21 +0530
categories: javascript
---

![OOP](https://media.giphy.com/media/88SCuVTIoAJ8Y/source.gif)

#**CONCEPTOS JS**

Con este post planeo mostrar variados de javascript
para el manejo del lenguaje

Empecemos!!

##Variables
Son valores asignados a memoria

```javascript
var foo = 1;
console.log(foo); //1
//reasignar valor
foo = 2;
console.log(foo); //2
```

\*No asignar variables con valor numerico al inicio de la variable:
~~1valor~~
ó
~~%valor~~,
o usar palabras reservadas como **function\***, **class**

javascript usa el ****camelCase**** las variables se debe declarar asi:

```
 -  costoFactura
 -  imprimirPorcentaje
 -  costoTotal
```

Continuemos con las asignacion de variables

```javascript
var x,
  y,
  z = 1; //Solo se asigna el valor a x
//comprobando
console.log(x); //1
console.log(y); //
console.log(z); //

//Asignando lo valores de manera independiente

var x = 1,
  y = 2,
  z = 3;
console.log(x); //1
console.log(y); //2
console.log(z); //3

//Asignacion entre variables
var x = 1,
  y = x + 2,
  z = y + 3;

console.log(x); //1
console.log(y); //3
console.log(z); //6
```

### LET VAR CONST

var n = 12
let numero = 1
const numeros = 123

**var** : si no declaramos valor con n,mostrara en consola un **undefined**

**let** : tambien se mostrara como **undefined**,si no declaramos un valor

**const**: mostrara un **SyntaxError: Missing initializer in const declaration**
por los cual SIEMPRE se debe declarar un valor

##valores primitivos en las variables

```javascript
var numero = 1
var booleano = true
var string 'cadenas de caracteres'
var nulo = 'null' // un solo valor y es nulll
var indefinido = undefinded;

//las variables si no se les asigna
//un valor viene por defecto como indefinido
```

Para conocer el tipo de valor de la varible con un **typeof**

Ejemplo

```javascript
console.log(typeof numero); //number
```

Atención JS desde su creacion tomas los null como un **object** para corergir esto entre "" dejo este pequeño hack

```javascript
if(nulo ==== null){
console.log('is null')
}
```

#### OBJETOS

Un objeto es un a referencia a una coleccion que contiene un conjunto de propiedades y valores

```javascript

var objecto = {
    name : andres,
    lastName: share
};

//copia del objeto

var objectoDos = objecto
console.log(objectoDos) |

//A tener en cuenta los objetos son unicos
// con sus propiedades y metodos ...

```

### Arrays

son colecciones de valores con indices numericos

```javascript
var array = [a, b, c, d];
console.log(array[0]); //a
```

### Computed property names

```javascript
var id = 0;

function generarId() {
  return "id_" + ++id;
}

var obj = {
  [generarId()]: "valor1",
  [generarId()]: "valor2"
};

console.log(obj);
```

}

### For - in

```javascript
var automovil = {
  model: "golf",
  make: "volskwagen",
  year: "2010",
  color: "red",
  doors: 4
};

for (var key in automovil) {
  console.log(key + ":" + automovil[key]);
}

//model:golf
//make:volskwagen
//year:2010
//color:red
//doors:4
```

### Convertir objeto a array

```javascript
var location = window.location;
var array = [];
for (var key in location) {
  if (typeof location[key] === "string") {
    array.push({ key: key, value: location[key] });
  }
}

console.log(array);
```

### **FOR OF**  recorre strings,array objetos mapas

```javascript
// filtrar solo numeros
var string = ' '123213,,,,sdkljfhksjdfh,345,rhfdk,ujy,,,,,'
var array = []
for(var value of string){
var number = parseInt(value)
if(!isNaN(number)){
    console.log(value + 'tipo' + typeof number)
    array.push(number)
}
console.log(array)

////123213345
```

### Filtrar emails

```javascript
var mapservicios = {}
for( var correo of correos) {
    var dominio = correo.split('@')[1]
    if( dominio  in mapservicios){
        mapservicios[dominio]++
    }else{
        mapservicios[dominio]= 1
    }
}

console.log(mapservicios)

```
##Convertir objeto a arrays

```javascript
function sumarNumero(){
    Array.from(arguments),reduce(function(a + b) return (a + b))
}
var resultado = sumarNumeros(1,2,3,34,5,6,7,7)

```

#HOSTING

```javascript
//funcion llamada antes..
mensaje()
function mensaje(){
    console.log("mensaje)
}

```


#function expresion

```javascript
//funcion llamada antes..
function foo()
{
    console.log('nuevo mensaje')
}
//js siempre manda a llamar la ultima
//function declarad
var msj = function(){
    console.log("mensaje)
}
msj()
```



# anonymus  function

```javascript

function (){
    console.log('funcion anonima')
}
///funcion anonima que reconre varios arreglos
[1,2,2,3].forEach(function(elemento){
    console.log(elemento)
})


```

# named  function expression

```javascript

var almaceda = function fool(){
    console.log('mensaje function expre')
}
console.log(almacena.name)
```

## IIFE
Aisla piezas de codigo del global scope
y se ejecuta inmediatamente


```javascript
(function(){
    console.log('IIFE')
}());
```

### Clousure

la funcion va a guardar la variable en el external scope
funcion que contine un estaod interno si su
variable esta en local

siempre tiene un vinculo con sus variables
declaradas por eso se llama CLOUSURE
```javascript

let numero =1

function fn(){
  console.log(numero)
}

function ejecutafn(callback)
{
callback();
}
ejecutafn(fn)

```

