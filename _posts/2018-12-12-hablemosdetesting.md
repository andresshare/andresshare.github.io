---
layout: post
title:  "Hablemos de testing -python 🐍"
date:   2018-12-12 19:05:10 +0530
categories: python 🐍
---

![Que es testing](https://media.giphy.com/media/f9SgNsok0zsxI3vS56/giphy.gif
)



Programar es escribir código para resolver problemas😎. La ingeniería de software es la práctica de utilizar un proceso estructurado para resolver problemas. 

Tener una base de código que podamos cambiar, ampliar y refactorizar según sea necesario. 

Las pruebas aseguran que nuestro programa funciona según lo previsto y que los cambios en la base de código no rompen la funcionalidad existente.

![Que es testing](https://media.giphy.com/media/DUrdT2xEmJWbS/giphy.gif)


Se trata de ser pragmático en lo que probamos, 😌 **cómo lo hacemos y cuándo lo hacemos** debemos aprovechar las herramientas y técnicas que nos permiten probar nuestro código de la manera más eficiente posible. Las pruebas deben ser fáciles y sin barreras

Tenemos que entrar en el código porque no hay pruebas o las pruebas que existen son tan debiles que nos vemos obligados a reescribir las pruebas a medida que escribimos el código. De esto no se trata la Ingeniería del Software. 

Las pruebas deberían permitir la refactorización, no obstaculizar nuestra capacidad de realizar cambios en la base de código. Deberíamos pasar nuestro tiempo escribiendo  💻 **lógica de negocios**, no luchando con pruebas.

En mi experiencia parece que hay muchos consejos contradictorios, y eso es porque los hay. Las pruebas son dificiles, más que cualquier otra disciplina de ingeniería de software. con mis colegas siempre estamos discutiendo sobre 📝 **Qué evaluamos**, **cómo evaluamos** y **cuándo evaluamos**.

```Aqui escribo mi proceso de pensamiento sobre cómo hago para agregar pruebas a una base de código. ```

antes de esto hago un resumen de como funciona la cosa,para  que en lo posible hablemos el mismo lenguaje

# QUE DIABLOS ES TESTING!

![Que es testing](https://media.giphy.com/media/l49JD2nWqfZ7exBzW/giphy.gif)
Cuando escribimos código, necesitamos ejecutarlo para asegurarnos de que está haciendo lo que esperamos. 

> Las pruebas son un contrato con nuestro código: dado un valor, esperamos que se devuelva un determinado resultado.

Las pruebas en ejecución pueden considerarse como un mecanismo de retroalimentación que nos informa si nuestro programa funciona según lo previsto

no he escuchado a nadie decir

> Escribí muchas pruebas, pero no valió la pena, así que las eliminé,el programa funciona como pense.

Si bien pasar las pruebas no puede probar los errores de ausencia, nos informan que nuestro código funciona de la manera definida por la prueba. En contraste, una prueba fallida indica que algo no está bien. Necesitamos entender por qué nuestra prueba falló para poder modificar el código y / o las pruebas, según sea necesario.

> 👨 => **Corro Test** => ☑️ ok, ✖️falla
entonces **resultado del proceso** => 👨 y de nuevo...

Si bien pasar las pruebas no puede probar los errores de ausencia, nos informan que nuestro código funciona de la manera definida por la prueba. En contraste, una prueba fallida indica que algo no está bien. Necesitamos entender por qué nuestra prueba falló para poder modificar el código y / o las pruebas, según sea necesario.

### Propiedades de los test

- **Rapido**: Las pruebas nos dan la confianza de que nuestro código funciona según lo previsto. Un ciclo de retroalimentación más lento dificulta el desarrollo ya que nos lleva más tiempo descubrir si nuestro cambio fue correcto. Si nuestro flujo de trabajo está plagado de pruebas lentas, no las ejecutaremos con tanta frecuencia. Esto conducirá a problemas en el futuro.


- **Determinista:** Las pruebas deben ser deterministas, es decir, la misma entrada siempre dará como resultado la misma salida. Si las pruebas no son deterministas, tenemos que encontrar una manera de explicar el comportamiento aleatorio dentro de nuestras pruebas. Si bien definitivamente hay un código no determinista en producción (es decir, Machine learning o IA), debemos tratar de hacer que todo nuestro código no probabilístico sea lo más determinista posible. No tiene sentido hacer trabajo adicional a menos que nuestro programa lo requiera.


- **Automatizado** Podemos confirmar que nuestro programa funciona ejecutándolo. Esto podría ejecutarse manualmente un comando en REPL o actualizar una página web; en ambos casos, estamos buscando ver si nuestro programa hace lo que se supone que debe hacer.
  
  Si bien las pruebas manuales están bien para proyectos pequeños, se vuelven inmanejables a medida que nuestro proyecto crece en complejidad. Al automatizar nuestro conjunto de pruebas, podemos verificar rápidamente que nuestro programa funciona a pedido. 


### Vocabulario en comun

> input > System under Test **(sut)** >  Output > **Salidas validas** >  ☑️ test ok, ✖️ test falla

Un sistema bajo prueba (SUT) es la entidad que se está probando actualmente. Esto podría ser una línea de código, un método o un programa completo.

**Los criterios de aceptación** se refieren a la verificación que realizamos que nos permite aceptar la salida del sistema. La especificidad y el rango de los criterios de aceptación dependen de lo que estamos probando: los dispositivos médicos y el sector aeroespacial requieren que las pruebas sean específicas, ya que hay mucho menos margen de error.

Si Amazon hace una mala recomendación, no es el fin del mundo. Si Watson de IBM sugiere una cirugía incorrecta, puede ser mortal.

**Las pruebas** se refieren al proceso de ingresar entradas en nuestro sistema bajo prueba y validar las salidas según nuestros criterios de aceptación:

- Si la salida está bien, nuestra prueba pasa.
- Si la salida no está bien, nuestra prueba falla y tenemos que depurar.

> Idenficar fallos temprano: 
**Los errores cuestan dinero**. **💰** `Cuánto` depende de cuándo los encuentres.

La corrección de errores se vuelve más costosa cuanto más se encuentre en el Ciclo de vida del desarrollo de software (SDLC). El verdadero costo de un error de software profundiza en este problema.

Mejorar el diseño del sistema

Este es un poco controvertido, pero creo que escribir código teniendo en cuenta las pruebas mejora el diseño del sistema. 

Un completo conjunto de pruebas muestra que el desarrollador realmente ha pensado en el problema con cierta profundidad. Escribir pruebas te obliga a usar tu propia API; Con suerte, esto da como resultado una mejor interfaz.

Todos los proyectos tienen limitaciones de tiempo y es bastante fácil acostumbrarse a tomar atajos que aumentan el acoplamiento entre módulos que conducen a interdependencias complejas. Tenemos que ser conscientes de resolver problemas con el código de espagueti.

Saber que tenemos que probar nuestro código nos obliga a escribir código modular. Si algo es torpe para probar, podría haber una mejor interfaz que podamos implementar. Tomarse el tiempo para escribir exámenes nos obliga a estar atentos; respiramos profundamente antes de ver el problema desde la perspectiva de un usuario.

Una vez que escriba código comprobable utilizando patrones como la inyección de dependencias, verá cómo agregar una estructura que hace más fácil verificar que nuestro código está haciendo lo que esperamos.



### Black Box contra White Box 

![pyramid test](https://media.giphy.com/media/l2JegI3GShJoyHEwo/giphy.gif)

Las pruebas se pueden clasificar ampliamente en dos grandes categorías: pruebas de Black Box y pruebas de White Box.

**Black Box Testing**: se refiere a técnicas de prueba en las que el tester no puede ver el funcionamiento interno del elemento que se está probando.

 > entrada > 📦 > salida

 **White Box Testing**: es la técnica en la que el tester puede ver el funcionamiento interno del elemento que se está probando.

 > entrada > 📤 > salida



Como desarrolladores, realizamos pruebas de White Box. Escribimos el código dentro de la caja y sabemos cómo probarlo a fondo. Esto no quiere decir que no sea necesario realizar pruebas de caja negra, aún deberíamos hacer que alguien realice las pruebas a un nivel superior; `La proximidad al código puede conducir a puntos ciegos en nuestras pruebas.`

### Piramide de prueba

La Pirámide de prueba no es una regla difícil y rápida, pero proporciona un buen lugar para comenzar a pensar en una estrategia de prueba. Una buena regla general es escribir tantas pruebas en cada nivel como sea necesario para tener confianza en su sistema. Deberíamos escribir pruebas a medida que escribimos código, iterando hacia una estrategia de prueba que funcione para el proyecto en el que estamos trabajando


![pyramid test](https://media.giphy.com/media/J341kHWTGLqflpLcGb/giphy.gif)


La Pirámide de prueba no es una regla difícil y rápida, pero proporciona un buen lugar para comenzar a pensar en una estrategia de prueba. 

Una buena regla general es escribir tantas pruebas en cada nivel como sea necesario para tener confianza en su sistema. Deberíamos escribir pruebas a medida que escribimos código, iterando hacia una estrategia de prueba que funcione para el proyecto en el que estamos trabajando

### UNIT test


Las pruebas unitarias son pruebas de bajo nivel que se centran en probar una parte específica de nuestro sistema. Son baratos de escribir y rápidos de ejecutar. Las fallas en las pruebas deben proporcionar suficiente información contextual para identificar la fuente del error. Los desarrolladores suelen escribir estas pruebas durante la fase de implementación del Ciclo de vida del desarrollo de software (SDLC).

Las pruebas unitarias deben ser independientes y aisladas; interactuar con componentes externos aumenta tanto el alcance de nuestras pruebas como el tiempo que tardan en ejecutarse.  reemplazar las dependencias con dobles de prueba da como resultado pruebas deterministas que se ejecutan rápidamente.

**¿Qué tan grande debe ser nuestra prueba de unidad?** Como todo lo demás en programación, `depende` de lo que estamos tratando de hacer. Pensar en términos de una unidad de comportamiento nos permite escribir pruebas alrededor de bloques lógicos de código.

**Test Pyramid** recomienda realizar muchas pruebas unitarias en nuestro conjunto de pruebas. Estas pruebas nos dan la confianza de que nuestro programa funciona como se esperaba. Escribir un código nuevo o modificar el código existente puede requerir que reescribamos algunas de nuestras pruebas. Esta es una práctica estándar, nuestro conjunto de pruebas crece con nuestra base de código.

Intente ser consciente de que nuestro conjunto de pruebas crece en complejidad. Recuerde, el código que prueba nuestro código de producción también **es código de producción.** Tómese el tiempo para refactorizar sus pruebas para asegurarse de que sean **eficientes y efectivas.**

vamos al codigo!

Supongamos que tenemos la siguiente función que toma una lista de palabras y devuelve la palabra más común y el número de apariciones de esa palabra:

```python
 def buscar_palabra_principal(palabras)
    # Devuelve las palabras y ocurrencias más comunes
    contador_palabras = Counter(palabras)
    return contador_palabras.most_common(1)[0]
```

Podemos probar esta función creando una lista, ejecutando la función `buscar_palabra_principal` sobre esa lista y comparando los resultados de la función con el valor que esperamos:


```python
def buscar_palabra_principal():
    palabras = ["foo", "bar", "bat", "baz", "foo", "baz", "foo"]
    resultado = buscar_palabra_principal(palabras)
    assert resultado[0] == "foo"
    assert resultado[1] == 3 
```
Si alguna vez quisimos cambiar la implementación de `buscar_palabra_principal`, podemos hacerlo sin temor. Nuestra prueba asegura que la funcionalidad de `buscar_palabra_principal` no puede cambiar sin causar una falla en la prueba.

### Test de integracion

![pyramid test](https://media.giphy.com/media/i5RWkVZzVScmY/giphy.gif)

Cada aplicación compleja tiene componentes internos y externos que trabajan juntos para hacer algo interesante. A diferencia de las pruebas de unidades que se centran en componentes individuales, las pruebas de integración combinan varias partes del sistema y las prueban juntas como un grupo. Las pruebas de integración también pueden referirse a las pruebas en los límites de servicio de nuestra aplicación, es decir, cuando salen a la base de datos, sistema de archivos o API externa.

Estas pruebas suelen ser escritas por desarrolladores, pero no tienen que ser así. Por definición, las pruebas de integración tienen un alcance mayor y tardan más en ejecutarse que las pruebas unitarias. Esto significa que las fallas de la prueba requieren cierta investigación: sabemos que uno de los componentes de nuestra prueba no funciona, pero es necesario encontrar la ubicación exacta de la falla. Esto contrasta con las pruebas unitarias que son de menor alcance e indican exactamente dónde fallaron las cosas.

Deberíamos intentar ejecutar pruebas de integración en un entorno similar a la producción; Esto minimiza la posibilidad de que las pruebas fallen debido a diferencias en la configuración.
Ejemplo de prueba de integración

Supongamos que tenemos la siguiente función que toma una URL y una tupla de (palabra, ocurrencias). Nuestra función crea un registro y lo guarda en la base de datos:

```python
def save_to_db(url, top_word):
    record = TopWord()
    record.url = url
    record.word = top_word[0]
    record.num_occurrences = top_word[1]

    db.session.add(record)
    db.session.commit()

    return record
```


Probamos esta función pasando información conocida; la función debe guardar la información que ingresamos en la base de datos. Nuestro código de prueba extrae el registro recién guardado de la base de datos y confirma que sus campos coinciden con la entrada que ingresamos.

```python
def test_save_to_db():
    url = "http://test_url.com"
    most_common_word_details = ("Python", 42)

    word = save_to_db(url, most_common_word_details)

    inserted_record = TopWord.query.get(word.id)
    assert inserted_record.url == "http://test_url.com"
    assert inserted_record.word == "Python"
    assert inserted_record.num_occurrences == 42

```

Observe cómo este es el tipo de prueba que hacemos manualmente para confirmar que las cosas funcionan como se esperaba. Automatizar esta prueba nos evita tener que verificar repetidamente esta funcionalidad cada vez que hacemos un cambio en el código.

### End-to-End 

![pyramid test](https://media.giphy.com/media/49zC0Bm1kbu36/giphy.gif)

Las pruebas de End to End verifican si el sistema cumple con nuestros requisitos comerciales definidos. Una prueba común es trazar una ruta a través del sistema de la misma manera que un usuario lo experimentaría. Por ejemplo, podemos probar un nuevo flujo de trabajo del usuario: simular la creación de una cuenta, "hacer clic" en el enlace en el correo electrónico de activación, iniciar sesión por primera vez e interactuar con la ventana emergente modal de nuestra aplicación web.

Podemos realizar pruebas de extremo a extremo a través de nuestra interfaz de usuario (UI) aprovechando una herramienta de automatización del navegador como Selenium. Esto crea una dependencia entre nuestra interfaz de usuario y nuestras pruebas, lo que hace que nuestras pruebas sean frágiles: un cambio en el front-end requiere que cambiemos las pruebas. Esto no es sostenible ya que nuestro front-end se volverá estático o nuestras pruebas no se ejecutarán.

Una mejor solución es probar la capa subcutánea, es decir, la capa justo debajo de nuestra interfaz de usuario. Para una aplicación web, esto sería probar la **API REST**, tanto enviando JSON como sacando **JSON.**

Nuestras pruebas subcutáneas son nuestros contratos con nuestro front-end; pueden ser utilizados por nuestros desarrolladores front-end como una especificación de la **API REST**. Las herramientas, como **swagger-meqa**, que se basan en la especificación **OpenAPI** pueden ayudarnos a automatizar este proceso. También podríamos contar con herramientas completas como **Postman** para probar, depurar y validar nuestra API.

Las pruebas de extremo a extremo se consideran recuadro negro, ya que no necesitamos saber nada sobre la implementación para realizar las pruebas. Esto también significa que las fallas en las pruebas no proporcionan una indicación de lo que salió mal; necesitaríamos usar registros para ayudarnos a rastrear el error y diagnosticar la falla del sistema.

vamos al codigo!

Aquí estamos utilizando el cliente **Flask Test** para ejecutar pruebas subcutáneas en nuestra **API REST**. Hay muchas cosas que suceden detrás de escena y el resultado que recibimos **(código de estado HTTP)** nos permite saber que la prueba pasó o falló.


```python
def test_end_to_end():
    client = app.test_client()

    body = {"url": "https://www.python.org"}
    response = client.post("/top-word", json=body)

    assert response.status_code == HTTPStatus.OK

```

### Structuring Tests 


Cada caso de prueba se puede separar en las siguientes fases:

    - configurar el sistema bajo prueba (SUT) en el entorno requerido por el caso de prueba (condiciones previas)
    - realizando la acción que queremos probar en SUT
    verificar si se produjo el resultado esperado (postcondiciones)
    - derribar SUT y devolver el medio ambiente al estado en que lo encontramos

Hay dos marcos ampliamente utilizados para estructurar pruebas: Arrange-Act-Assert y Given-When-Then.
Organizar-Actuar-Afirmar (AAA)

El patrón AAA es una abstracción para separar las diferentes partes de nuestras pruebas:

    - Organizar todas las condiciones previas necesarias
    - Actuar sobre el SUT
    - Afirmar que se cumplen nuestras condiciones posteriores




Vamos la codigo!
```python
def test_find_top_word():
    # Arrange
    words = ["foo", "bar", "bat", "baz", "foo", "baz", "foo"]

    # Act
    result = find_top_word(words)

    # Assert
    assert result[0] == "foo"
    assert result[1] == 3

```

### GWT 

GWT proporciona una abstracción útil para separar las diferentes fases de nuestra prueba:

    - Dado un conjunto de condiciones previas
    - Cuando realizamos una acción en el SUT
    - Entonces nuestras condiciones posteriores deben ser las siguientes

GWT es ampliamente utilizado en Behavior Driven Development (BDD).


```python
def test_find_top_word():
    # Given a list of word
    words = ["foo", "bar", "bat", "baz", "foo", "baz", "foo"]

    # When we run the function over the list
    result = find_top_word(words)

    # Then we should see `foo` occurring 3 times
    assert result[0] == "foo"
    assert result[1] == 3

```


### Que testear!

![pyramid test](https://media.giphy.com/media/7MZ0v9KynmiSA/giphy.gif)

Para probar que nuestro programa es correcto, tenemos que probarlo contra cada combinación concebible de valores de entrada. Este tipo de prueba exhaustiva no es práctica, por lo que debemos emplear estrategias de prueba que nos permitan seleccionar casos de prueba en los que es más probable que se produzcan errores.

Los desarrolladores experimentados pueden equilibrar la escritura de código para resolver problemas comerciales con pruebas de escritura para garantizar la corrección y evitar la regresión. Encontrar este equilibrio y saber qué probar puede sentirse más como un arte que como una ciencia. Afortunadamente, hay algunas reglas generales que podemos seguir para asegurarnos de que nuestras pruebas sean exhaustivas.
Requerimientos funcionales

Queremos asegurarnos de que se hayan implementado todos los requisitos relevantes. Nuestros casos de prueba deben ser lo suficientemente detallados para verificar los requisitos comerciales. No tiene sentido construir algo si no cumple con los criterios establecidos.
Prueba de ruta de base

Tenemos que probar cada declaración al menos una vez. Si la declaración tiene un condicional (si o mientras), tenemos que variar nuestras pruebas para asegurarnos de probar todas las ramas del condicional. Por ejemplo, si tenemos el siguiente código:

```python
if x > 18:
    # statement1
elif 18 >= x >= 35:
    # statement2
else:
    # statement3
```

Para asegurarnos de alcanzar todas las ramas del condicional anterior, necesitamos escribir las siguientes pruebas:


   1. x < 18
   2. 18 <= x <= 35
   3. x > 35


### Partición de equivalencia

Se dice que dos casos de prueba que resultan en la misma salida son equivalentes. Solo requerimos uno de los casos de prueba para cubrir esa clase de errores.
Análisis de límites

- "Hay 2 problemas difíciles en Ciencias de la Computación: invalidación de caché, nombres de cosas y errores fuera de 1".

Este es uno de los chistes más antiguos de la programación, pero hay mucha verdad detrás, a menudo confundimos si necesitamos un **< o un <=**. Es por eso que siempre debemos probar las condiciones de emtorno. 


```python
if x > 18:
    # statement1
else:
    # statement2
```

Para asegurarnos de probar a fondo las condiciones de entorno del fragmento de código anterior, deberíamos tener casos de prueba para **x = 17, x = 18 yx = 19.** Tenga en cuenta que escribir casos de prueba se vuelve más complicado si nuestro límite tiene condicionales compuestos.



### Clases de datos incorrectos

Esto se refiere a cualquiera de los siguientes casos:

   - Muy pocos datos (o sin datos)
    - Demasiados datos
    - Datos inválidos
    - Tamaño incorrecto de datos
    - Datos no inicializados

### Prueba de flujo de datos

Se enfoca en rastrear el flujo de control del programa con un enfoque en explorar la secuencia de eventos relacionados con el estado de los objetos de datos. Por ejemplo, recibimos un error si intentamos acceder a una variable que ha sido eliminada. Podemos utilizar las pruebas de flujo de datos para obtener casos de prueba adicionales para variables que no han sido probadas por otras pruebas.

### Error Adivinando

La experiencia pasada proporciona información sobre partes de nuestra base de código que puede conducir a errores. Mantener un registro de los errores anteriores puede mejorar la probabilidad de que no vuelva a cometer el mismo error en el futuro.
Resumen

Averiguar qué probar y hacerlo de manera eficiente es a lo que me refiero cuando digo **Art of Developer Testing**. La única manera de mejorar en las pruebas es escribiendo pruebas, presentando mejores estrategias de prueba y aprendiendo sobre diferentes técnicas de prueba. Al igual que en el desarrollo de software, cuanto más sepa sobre algo, mejor se convertirá en eso.

**Cuando escribir pruebas**
Si bien hay mucha discusión interesante sobre cuándo escribir pruebas, creo que se lleva lejos del punto de prueba. No importa cuando escribes pruebas, solo importa que escribas pruebas.



**Tip**

 El problema con las pruebas unitarias a menudo es que se realizan demasiadas pruebas triviales, que es solo un código adicional que debe mantenerse ... si se hace mal, es más un obstáculo que un beneficio ... es por eso que decidir qué probar es tan importante ... pensar antes de actuar.




y esta en es una breve introduccion
nos vemos en el siguiente post

Hasta pronto!






