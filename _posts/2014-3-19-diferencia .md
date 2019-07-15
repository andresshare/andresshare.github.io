---
layout: post
title:  "Cuál es la diferencia entre cookie localStorage, sessionStorage e indexedDB?"
date:   2014-03-19 20:02:00 +0530
categories: Concepto
---

![OOP](https://media.giphy.com/media/l0HlyXQUez0jHop2g/giphy.gif)


**Cookie** Pequeño set de información enviada por un sitio Web y almacenado en el navegador de un usuario. Se guarda en el disco, por lo que esta data es persistente. Es posible guardar y recuperar la data usando JS de la siguiente manera. Pueden guardar poca data (4KB). Son enviadas en cada request.
**sessionStorage.** La propiedad sessionStorage permite acceder al objeto local Storage pero solo durante la sesión del usuario. Una sesión dura hasta que el navegador es cerrado. La data sobrevive a recargas de página. Una nueva “tab” o “ventana” genera una nueva sesión. ~5MB de storage por dominio

**localStorage.** La propiedad localStorage permite acceder al objeto local Storage La data no tiene una fecha de expiración y es accesible desde múltiples ventanas o tabs del mismo dominio y navegador. ~5MB de storage por dominio. Las propiedades del localStorage solo pueden ser accedidas por páginas con el mismo dominio que la página que definió (set o seteó) las propiedades. Por ejemplo, si una página como ejemplo.com setea algo en el localStorage puede ser accedida por ejemplo.com/xxxxx, ejemplo.com/yyyyy, ejemplo.com/xxxxx/zzzzz y así.

_Como nota muy importante_: los datos guardados en localStorage y en sessionStorage son específicos al protocolo de la página. No es lo mismo **http://ejemplo.com** que **https://ejemplo.com**, por lo que los datos a los que acceden/escriben son distintos. 