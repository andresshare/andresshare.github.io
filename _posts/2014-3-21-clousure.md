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