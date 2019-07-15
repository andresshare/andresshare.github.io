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