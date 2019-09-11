---
layout: post
title:  "Que es la herencia?"
date:   2014-03-13 19:11:10 +0530
categories: Concepto javascript
---

![OOP](https://media.giphy.com/media/l0ExhcMymdL6TrZ84/giphy-downsized-large.gif)

Un concepto donde una clase comparte la estructura y el comportamiento definido en otra clase. 

```javascript
class SuperClass {
constructor() {
this.logger = console.log;
}
log() {
this.logger(`Hello ${this.name}`);
}
}
class SubClass extends SuperClass {
constructor() {
super();
this.name = 'subclass';
}
}
const subClass = new SubClass();
subClass.log(); // logs: "Hello subclass"
```

Revisemos esto con mas profundidad aplicado para js

---
JavaScript utiliza la herencia prototípica para la creación de objetos. ¿Qué significa esto? Una forma de pensar en los objetos en JavaScript es que son como una colección de pares de valores clave. 

En JavaScript, un objeto es simplemente una instanciación de una función que produce una variable usando estas claves y valores (más sobre constructores de objetos). 

Esa función usualmente usa el método constructor que es parte del prototipo **JavaScript Object.prototype** (clase base para todos los objetos JavaScript) y para ser más explícitos, las propiedades y métodos se definen en la propiedad prototipo en la función constructora Object, no en las instancias del objeto en sí. .

```js
/*for example creating an Automobile 
object with properties
*/
function Automobile(make, model, year, fuelType) {
    this.make = make;
    this.model= model;
    this.year = year;
    this.fuel = fuelType;
}

//and instantiating a new Auto object looks like this. 
var familyVan = new Automobile('Honda', 'Odyssey', 2014, 'Gas');
```


Lo que sucede es que estamos llamando a la función constructora heredada de la clase de objeto base cuando usamos la nueva palabra clave mientras llamamos a la función Automóvil. 

Hay algunas diferencias entre las especificaciones ES5 y ES6, que no estoy dispuesto a abordar en este momento, pero ES6 puede ayudar a eliminar parte de la repetición de asignar valores a las propiedades de objeto de su creación. Pero la mayor parte de esto es solo sugar sintax y no cambia la forma en que JavaScript crea nuevos objetos. Tenga en cuenta que tampoco vamos a tocar la palabra clave de clase ES6.

### Modificando el objeto

Es posible que haya declarado un objeto utilizando este método siguiente creando un objeto anónimo como variable y luego utilizando corchetes o notación de puntos para modificar aún más el objeto.

```js
var yota= {make:"Toyota", model:"4Runner", year: 1992, color:"blue"};

//and then to modify it say adding a new function to it done something like 
yota.goOffRoad = function(){
  console.log('4 wheelin!'); 
};
//then you could call this new function on our yota variable 
yota.goOffRoad(); //'4 wheelin!'  
```

Esto funciona, en un objeto anónimo o también en un objeto creado como nuestro anterior familyVan. Pero esto no funcionaría si intentáramos crear la función siguiendo la definición de nuestra función Automóvil, así:

```js

function Automobile(make, model, year, fuelType) {
    this.make = make;
    this.model= model;
    this.year = year;
    this.fuel = fuelType;
}

Automobile.driveTrain= function(driveType){
   this.driveType = driveType; 
};

//create our familyVan again
var familyVan = new Automobile('Honda', 'Odyssey', 2015, 'Gas');
//but if we attempt to call the driveType function to set the property..
familyVan.driveTrain('Front Wheel Drive'); //Throws an Unexpected TypeError, that familyVan.driveType is not a function
```

Si observa el objeto real a través de **console.log (familyVan)** verá que no hay una función definida para nuestro familyVan.driveTrain. Aquí es donde es necesario acceder al prototipo de nuestro objeto para modificar nuestro constructor de automóviles es su creación inicial. Debemos asignar nuevas propiedades o métodos de esta manera usando el siguiente método accediendo al **Object.prototype.**

![herencia -javascript](https://media.giphy.com/media/S9KONwQSMU2tQ5ey0X/giphy.gif)
