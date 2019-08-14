---
layout: post
title:  "Ordenar Array"
date:   2019-08-13 23:04:05 +0530
categories: Javascript
---

![algoritmo](https://media.giphy.com/media/Zc8c0DRlusDWU/giphy.gif)


Al tener un array

```
var  arr = [2,3,4,3,2,1,2,2,];
```
y como argumento numero
```
numero = 2
```
el resultado
```
el resultado sera :4

```

**Mi solucion**

```javascript
var  arr = [2,3,4,3,2,1,2,2,];

const numeroRepetido=(arr, ent)=> arr.filter((item) => (item === ent)).length;


console.log(numeroRepetido(arr,2))

```