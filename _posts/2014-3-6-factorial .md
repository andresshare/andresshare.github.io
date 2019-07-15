---
layout: post
title:  "Obtener el factorial de un numero"
date:   2014-03-06 21:03:36 +0530
categories: Javascript
---

![factorial](https://media.giphy.com/media/cg5FwpvDmhIcM/giphy.gif)

Lo primero es definir que un factorial es la multiplicación de todos los numeros  **[ENTEROS]** positivos. Que inician desde **1**.

Como lo podemos ver en el siguiente ejemplo creado con javascript


```javascript

function factorialize(num) {

  if (num < 0) 
        return -1;
  else if (num == 0) 

      return 1;
  
  else {
      return (num * factorialize(num - 1));
  
  }

}

factorialize(5);

```

La **Recursión** es una función que se llama así misma para resolver una instancia de un problema. se aplica cuando al llamar la misma función repetidamente con diferentes parámetros desde un bucle. da solución a diferentes problemas, el más común es iterar sobre una estructura de datos hasta encontrar, calcular o ordenar y obtener el resultado. 