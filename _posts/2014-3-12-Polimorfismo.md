---
layout: post
title:  " Que es polimorfismo? "
date:   2014-03-12 20:15:01 +0530
categories: Concepto
---

![OOP](https://media.giphy.com/media/10MGOmsKZGXqNi/giphy.gif)

No es nada más que un comportamiento o valor en una **subclase** de algo que ya fue declarado en la clase principal Simplemente **polimorfismo** mas de una forma. 


Otra manera de explicarme es que
Si ha estado tratando de encontrar una definición de polimorfismo que tenga sentido, espero que esto lo ayude.

En pocas palabras, el polimorfismo significa que puede usar la misma interfaz para diferentes tipos de datos subyacentes. Un ejemplo simple de polimorfismo en acción es la matemática básica. 

 Usted Puede agregar un entero y un flotante juntos y no tendrá ningún problema debido a los tipos de datos no coincidentes.

La forma más notable de ver el polimorfismo es en clases. Este concepto se relaciona con la herencia porque se trata de clases derivadas que pueden sobrescribir las propiedades y métodos de la superclase. Cuando una clase derivada ha sobrescrito un método o propiedad de superclase, entonces el código se referirá a la clase derivada para ese método o propiedad.

![polimorfismo](https://media.giphy.com/media/l50vzxM2lBM2fQbka9/giphy.gif)

En este caso, la cena es la **superclase** y el tailandés, el italiano y el peruano son clases derivadas. Como puede ver, cada método de receta en las clases derivadas es diferente. Entonces, por ejemplo, cuando declara un objeto usando la **clase Dinner** y crea una nueva instancia de un objeto peruano, puede usar el método **Recipe ()** y no preocuparse por el código que se ejecutará. Se transferirá automáticamente al código para el método **Recipe ()** definido en la clase peruana.

Eso es lo que es el polimorfismo. Un método de una clase derivada puede sobrescribir el método para una superclase. Por lo tanto, puede definir un objeto con una superclase y luego instanciarlo con una clase derivada. Luego, cuando acceda al método, el bloque de código correcto se ejecutará cada vez.