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