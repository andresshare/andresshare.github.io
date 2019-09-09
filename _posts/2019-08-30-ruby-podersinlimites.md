---
layout: post
title:  "RUBY -PODER SIN LIMITES 💎"
date:   2019-08-30 19:30:20 +0530
categories: Ruby
---

![Ruby poder sin limites](https://media.giphy.com/media/HChtj3gzcVsXK/giphy.gif)


# RUBY - PODER SIN LIMITES  💎

Mi intencion es empezar de 0 con el lenguaje de **RUBY** creado por **Yukihiro Matsumoto** y tocar los puntos mas importantes para su uso.

**Adelante!!**


despues de instalar ruby en nuestro sistema operativo, corremos IRB en la consola del sistema operativo

---
### FLUJO DE TRABAJO

 Creamos nuestro: 
 
    Archivo.rb >  💎 IRB interprete  > 💻 ejecutamos el programa


 **Vamos al primer script**



 Despues de crear **Archivo.rb** en **IRB** escribimos
 
```rb

puts "HELLO RB"
```

⌨️ Ejecutamos en modo consola


> ruby Archivo.rb

Salida del programa

> HELLO RB

**🐵** Clave: **IRB** [for Interactive Ruby)]

---

**OPERADORES MATEMATICOS**

| OPERADOR  | USO|
------------- | -------------
`+`  | Suma
`-` | Resta
`/` | Division
`*` | Multiplicacion
`**` | Potencia
`%` | Residuo de la division
`+=` | Sumar y asignar el valor a una variable
`-=` | restar y asignar el valor a una variable
`*=` | multiplicar y asignar el valor a una variable
`/=` | Dividir y asignar el valor a una variable
`%=` | Busca el residuo en una division  y asignar el valor a una variable


---
SUMA `IRB`

```RUBY
>> 100 + 13
=> 113
```
RESTA `IRB`

```RUBY
>> 100 - 13
=> 87
```
DIVISION `IRB`

```RUBY
>> 13 / 13
=> 1
```
MULTIPLICACION `IRB`

```RUBY
>> 100 + 13
=> 1300
```
POTENCIA `IRB`

```RUBY
>> 100 ** 13
=> 100000000000000000000000000 

```
RESIDUO DE LA DIVISION `IRB`

```RUBY
>> 100 % 13
=> 9
```
SUMA CON ASIGNACION `IRB`

```RUBY
>> ruby = 100
=> 100
>> ruby += 24
=> 124
>> ruby
=> 124
```
RESTA CON ASIGNACION `IRB`

```RUBY
>> ruby = 100
=> 100
>> ruby -= 24
=> 76
>> ruby
=> 76
```
DIVIDIR CON ASIGNACION `IRB`

```RUBY
>> ruby = 100
=> 100
>> ruby /= 24
=> 4
>> ruby
=> 4
```
---
### **STRINGS**

Son una cadena en serie de caracteres de texto.

`IRB`
```ruby
>> "ruby"
=> "ruby" 
``` 
### VARIABLES

Son nombres que hacen referencia a valores,si en un cajon
guardamos relojes, obtendremos relojes

`IRB`
```ruby
>> cajon = "relojes"
=> "relojes" 
```
Al  declarar variables se permite letra minuscula, numeros, guiones _  y una buena practica es escribir las variables modo SNAKE CASE asi : **ganancia_total**

Esta prohibido y causara errores:

- Crear variables con espacio:  **ganancia total**
- Usar caracteres especiales:  **$ganancia_total**
- Iniciar con un numero: **1ganancia_total**
- Iniciar con mayusculas: **Ganancia_total**



### CONSTANTES

Nos encontraremos problemas que tendremos que resolver con constantes lo que significa que su valor sera eterno dentro del programa ejemplo

`IRB`
```ruby
Numero = 12 
=> 12 
```
en su sintaxis iniciara con mayuscula 


### OBJETOS

Ruby es un lenguaje orientado a objetos. esto nos permite manejar las cadenas de caracteres de manera rapida Veamos

`IRB`
```ruby
# Contamos la logitud de la cadena
"Hi developer!!".length
=> 14 
```
`IRB`
```ruby
# Invertimos la cadena
"Hi developer!!".reverse
 => "!!repoleved iH" 
```

`IRB`
```ruby
# Asigna la Mayuscula al primer caracter
 "hi developer!!".capitalize 
 => "Hi developer!!"
```

`IRB`
```ruby
# Convierte la cadena a mayusculas
 "hi developer!!".upcase 
  => "HI DEVELOPER!!" 
```


`IRB`
```ruby
# Convierte la cadena a minusculas
 "HI DEVELOPER!!".downcase
 => "hi developer!!" 
```


`IRB`
```ruby
# Imprime la siguiente cadena logica
 "Hi developer!!".next
 =>   "Hi developes!!" 
```

`IRB`
```ruby
# devuelve TRUE si la cadena esta vacia
# al contrario su valor sera FALSE
 "Hi developer!!".empty
 =>   "Hi developes!!" 
```


**🐵** Clave: si queremos saber que valor tiene la variable


`IRB`
```ruby
#Esto aplica para STR,BOOLEAN,FLOAT
numero = 100
numero.class
 => Integer  
```


### CONCATENAR STRINGS

 Unir cadenas con diferentes nombres de variable o constantes

`IRB`

```ruby
frase_uno = "¿Internet? ¿Todavía anda eso por ahí?"
autor = " --Homero Simpson " 

frase_completa = frase_uno + autor

frase_completa
=> "¿Internet? ¿Todavía anda eso por ahí? --Homero Simpson " 


```
### CAPTURAR DATOS
`IRB`
```ruby
print "Que dia es hoy?"
#gets en un metodo para leer la entrada de caracteres en la ventana
dia = gets()
 => "Viernes\n" 
# #{dia} nos permite sustituir el valor en el nombre variable de la cadena
puts "hoy es: #{dia}"
 => hoy es: Lunes

``` 
**🐵** Clave: **[** `puts` and  `print` **]** la diferencia esta en que `puts` al escribir muestra los datos en la linea. Mientras `print` da un espacio en blanco para poder escribir el dato que nos solicita. Recuerda que son metodos.


###CHOMP
 
 Ahora veamos el metodo `CHOMP`, su funcion es si el último carácter de una cadena es una nueva línea, el método `chomp`  la elimina. con esto limpiamos cadenas devueltas por `gets`.



`IRB`
```ruby
print "Numero favorito? "
input = gets
 => "13\n" 
#se recibe la cadena con el metodo chomp
numero = input.chomp
#Sustuimos el valor en el nombre de la variable
puts "Buen numero, #{numero}!"
 => "Buen numero: 13" 
```

### CONDICIONALES

### **IF**

Al crear una sentencia y queremos comprobar si se 
cumple la condicion

`IRB`
```ruby

puts "Adivina la marca de auto,entre Mazda,Fiat,Tesla. Escoje!  "
marca = gets.chop
#la condicion es verdadera
puts "#{marca} Eres un campeon!!" if marca == "Tesla"
#la condicion es falsa
puts "#{marca} Escribe una marca de nuevo" if name != "Tesla"

```

Un programa  puede tener variadas soluciones


`IRB`
```ruby

print "Adivina la marca de auto,entre Mazda,Fiat,Tesla. Escoje!  "
marca = gets.chop
if marca == "Tesla"
  puts "#{marca} Eres un campeon!!"
else
  puts "#{marca} Escribe una marca de nuevo"
end

```

La diferencia es cómo se representa la lógica dentro del programa.

Comienza como se declara el `if` con su cierre `end` 
entonces valida `if marca =="Tesla"`  como  es verdadero muestra `Eres un campeon!!"`

`else` se activa si la condicion es falsa


### Elsif



Cuando usamos `if` y `else`, el código  `if` se ejecuta si se cumple la condición, de lo contrario, el código baja a la sección  de `else` y se ejecuta. 

Creemos  un nuevo escenario donde el código no se cumple, entonces el programa salta a `else`, ahora la condicion nos indica que verifiquemos otra condicion en la linea del `else`



`IRB`
```ruby
primer_numero,segundo_numero,tercer_numero = 2,13,7
# >= mayor igual
if primer_numero >= segundo_numero and primer_numero >= tercer_numero
  puts "primer_numero = #{primer_numero} Es el numero MAYOR"
elsif segundo_numero >= tercer_numero and segundo_numero >= primer_numero
  puts "segundo_numero = #{segundo_numero} Es el numero MAYOR"
else puts "Tercer_numero = #{tercer numero} Es el numero MAYOR"
end

```


## IF THEN ELSE
En mi experiencia no es muy usado, sin embargo es bueno saber que existe

`IRB`
```ruby
#Saber si un numero es par
number = 12

if number % 2 == 0
  then
  puts "Par"
  else
    puts "Impar"
end
```

### **UNLESS**

Una manera diferente de evaluar condiciones.el opuesto de if es `unless`
la condicion solo se ejecutara si es falsa,claro que se puede usar el `else` para continuar el programa

`IRB`
```ruby
unless true
    puts "Este mensaje no se vera en pantalla!"
else 
    puts 13
end
```

### LOOPS

### While
Mientras la condicion se cumpla,contiuara ejecutandose


`IRB`
```ruby
#Contar hasta 10
numero = 1
while numero <= 10
puts numero
#incremeta el valor de numero
numero += 1
end
```

### OPERARDOR TERNARIO

`IRB`
```ruby
a=10
b=5
#evalua la condicion y muestra el mensaje
#forma abreviada de if/else
numero_mayor = a > b  ? "hola" : "bye"
=> "hola"
```

### Times

`IRB`
```ruby
13.times{
  #se mostrara 13 veces en pantalla
  puts "mensaje"
}
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
mensaje
 => 13 


``` 

### Upto

Recorre e imprime los valores de manera inversa

`IRB`
```ruby
13.upto 20 do |i|
  print "#{i}, "
end

=> 13, 14, 15, 16, 17, 18, 19, 20,  
=> 13 

```

### UNTIL
Mientras el `while` se ejecuta hasta que la condicion sea falsa
con `until` lo hace hasta que sea verdadera
`IRB`

```ruby
i=1
until i > 10 do
  print "#{i}, "
  i+=1
end

1, 2, 3, 4, 5, 6, 7, 8, 9, 10,  => nil 

```

### ARRAYS

Las matrices nos permite organizar cualquier tipo de dato
para luego clasificarlo
y modificarlo de acuerdo al problema que tengamos que solucionar

`IRB`
```ruby
##array vacio
un_array = []
un_array << "Elemento"
```
`IRB`
```ruby
un_array << 234234
un_array << Time.now
```
para recorrerlos se usa:

`IRB`
```ruby
un_array.each do |elemento|
  puts elemento
end

```

Se puede recorrer con un for

`IRB`

```ruby 

# Array.new crea un array vacio
un_array = Array.new
un_array.push("Message")
un_array.push 123
un_array << Time.now

for elemento in un_array
  puts elemento
end

```

Funciones ejecutads al array

`irb`
```ruby
array.length
=> 3
array.join(', ')
=> "Message, 123, Mon Aug 31 20:30:41 +0530 2010"
array.push(5)
=> ["Message", 123, Mon Aug 31 20:30:41 +0530 2010, 5]
array.pop
=> 5
array
=> ["Message", 123, Mon Aug 31 20:30:41 +0530 2010, 5]
```

Consultemos un array anidado

`irb`
```ruby
array = [1, 5, [7, 9, 11, ["Ruby on rails"], "Sigma"]]
=> [1, 5, [7, 9, 11, ["Ruby on rails"], "Sigma"]]
array.dig(2, 3, 0)
=> "Ruby on rails"
``` 

Usemos intersecciones,uniones, saque sus conclusiones
al revisar este script

```ruby

Real_madrid=["Eden hazard", "James rodriguez", "Keilor navas", "Mariano", "Marcelo"]

Jugadores=["Messi","Pele","James rodriguez","Keilor navas","Ronaldinho"]


Real_madrid & Jugadores

Real_madrid | Jugadores

Real_madrid + Jugadores

Real_madrid - Jugadores

```

Link de toda las informacion de arrays

[Documentacion Arrays](https://ruby-doc.org/core-2.5.1/Array.html "Arrays")


###  Hashes y simbolos

Los hashes son matrices con índice definido por el programa o  un usuario. no por el intérprete de Ruby.
Un array asociativo contiene elementos que se pueden acceder, no a través de índices numéricos secuenciales, sino a través de claves que pueden tener cualquier tipo de valor. Estos arrays se conocen a veces como hash o diccionario.




```ruby
mark = Hash.new
mark['English'] = 50
mark['Math'] = 70
mark['Science'] = 75
print "Nombre de la materia:"
sub = gets.chop
puts "Mark en #{sub} es #{mark[sub]}"

```

A diferencia de una matriz, el hash puede tener un objeto como índice.

¿Qué pasa si el índice no tiene un valor definido?


```ruby

mark = Hash.new 0 # Asignamos el valor de mark es cero
mark['English'] = 50
mark['Math'] = 70
mark['Science'] = 75
print "Nombre de la materia:"
sub = gets.chop
puts "Mark en #{sub} es #{mark[sub]}"

=> Mark en Science es 0:
```
Mire la salida, no hemos definido un valor para la marca ['Química'], sin embargo, cuando el nombre del sujeto se especifica como Química, obtenemos 0 como resultado. 

Esto es así porque hemos establecido cero como valor predeterminado. Por lo tanto, al establecer el valor predeterminado, tendremos un valor para aquellos índices que aún no hemos definido.

### Recorramos hashes
`ìrb` 
```ruby
mark = Hash.new 0 # Asignamos el valor de mark es cero
mark['English'] = 50
mark['Math'] = 70
mark['Science'] = 75
total = 0
mark.each { |key,value|
  total += value
}
puts "Total marks = "+total.to_s

=> Total marks = 195
``` 

En el programa anterior, hemos calculado el total de todas las marcas almacenadas en la marca Hash. Tenga en cuenta cómo usamos cada bucle. Tenga en cuenta que obtenemos el par clave-valor usando | clave, valor | en el cuerpo del bucle. 

La clave contiene el índice del hash y el valor contiene el valor almacenado en ese índice particular [25]. Cada vez que se ejecuta el bucle, agregamos valor al total, por lo que al final el total de la variable tiene el total de los valores almacenados en el hash. Por fin imprimimos el total.


`ìrb`
```ruby
mark = Hash.new 0 # signamos el valor de mark es cero
mark['English'] = 50
mark['Math'] = 70
mark['Science'] = 75
total = 0
puts "Key => Value"
mark.each { |a,b|
  puts "#{a} => #{b}"

```


### SIMBOLOS

los simbolos es una instancia única de la clase Symbol que generalmente se usa para identificar un recurso específico. Un recurso puede ser:

* Un metodo
* una variable
* un hash key
* un stado
* etc..

Un símbolo es uniq porque solo se puede crear una instancia de la clase Symbol para un símbolo específico en un programa en ejecución

```ruby

:pending.object_id # => 1277788
:pending.object_id # => 1277788

```


Aquí, podemos ver que el símbolo: :pending solo se crea una vez ya que las dos llamadas a: pending.objeto_id devuelven el mismo identificador de objeto.

Los símbolos a menudo se comparan con las cadenas. Pero la principal diferencia entre ellos radica en el hecho de que se crea un nuevo objeto String para cada cadena llamada, incluso si son idénticos


```ruby
'pending'.object_id # => 70324176174080
'pending'.object_id # => 70324176168090

```
Ahora que estamos más familiarizados con los símbolos, veamos la clase Symbol y la API que proporciona.




#### EL SYMBOL DE LA CLASE


Esta clase es parte de la Biblioteca principal de Ruby (también conocida como core-lib).


Esta clase no es públicamente instanciable

```ruby
irb> Symbol.new
NoMethodError (undefined method `new' for Symbol:Class)


```
De lo contrario, un objeto Symbol se instancia implícitamente cuando se declara un nuevo símbolo

```ruby

irb> :dummy_symbol.class
 => Symbol
```

Echemos un vistazo a su cadena de antepasados

```ruby

irb> Symbol.ancestors
 => [Symbol, Comparable, Object, Kernel, BasicObject]
```
La clase Symbol hereda de la clase padre predeterminada Object.


Tenga en cuenta que incluye el módulo Comparable.

Esta clase comparte exactamente la misma cadena de antepasados ​​que las clases String y Numeric.

Esta clase también proporciona un montón de métodos de instancia interesantes para comparar, modificar y unir símbolos.

La mayoría de los métodos para modificar y unir símbolos utilizan el método Symbol # to_s para trabajar con la representación de cadena del símbolo.



Como los símbolos son, para cada uno de ellos, una instancia única de la clase Symbol, entonces Ruby tiene que hacer un seguimiento de cada uno de ellos para poder garantizar su singularidad.


Para hacerlo, Ruby proporciona una tabla interna llamada global_symbols que se encarga de realizar un seguimiento de todos los símbolos de su programa en ejecución.

> Tenga en cuenta que los símbolos solo se guardan en la memoria una vez. Esto los hace muy eficientes de usar. Pero permanecen en la memoria hasta que sale el programa. Esto es cierto para todas las versiones de Ruby <2.2.0. De lo contrario, los símbolos usan el garbage collector.

El método Symbol.all_symbols devuelve una matriz que representa el contenido de la tabla global_symbols en el momento de la llamada al método

```ruby
Symbol.all_symbols.length                      # => 3893
Symbol.all_symbols.grep(/Struct/)              # => [:Struct]

:dummy_symbol
Symbol.all_symbols.length                      # => 3894
Symbol.all_symbols.grep(/dummy_symbol/)        # => [:dummy_symbol]

dummy_variable = nil
Symbol.all_symbols.length                      # => 3895
Symbol.all_symbols.grep(/dummy_variable/)      # => [:dummy_variable]

def dummy_method; end
Symbol.all_symbols.length                      # => 3896
Symbol.all_symbols.grep(/dummy_method/)        # => [:dummy_method]

class DummyClass; end
Symbol.all_symbols.length                      # => 3897
Symbol.all_symbols.grep(/DummyClass/)          # => [:DummyClass]

Symbol.all_symbols.grep(/Hash/)                # => [:Hash]
class Hash; end
Symbol.all_symbols.length                      # => 3897

```

Primero, podemos ver que la tabla global_symbols no está vacía.


En efecto, en la configuración del programa, esta tabla se completa con todos los métodos, variables y clases incluidos en la Biblioteca principal de Ruby. Estos recursos se insertan en la tabla como símbolo.

> Por ejemplo, la clase Struct es parte de la Biblioteca principal de Ruby.

Luego, podemos ver que un símbolo que representa un recurso se agrega a la tabla global_symbols cuando definimos:



un nuevo símbolo
una nueva variable
un nuevo método
una nueva clase / módulo

Luego, podemos ver que no se agrega ningún símbolo nuevo a la tabla cuando volvemos a abrir la clase Hash. Esto se debe a que el símbolo: Hash ya está incluido en la tabla global_symbols. Este mecanismo es el mismo para símbolos, variables y métodos.


>Tenga en cuenta que esta tabla se usa cada vez que tiene que lidiar con símbolos

>Tenga en cuenta que los operadores == y === están utilizando una comparación a nivel de objeto.

>Pero para todos los demás métodos de comparación, utiliza la representación de cadena del símbolo para la comparación.


> HASHES articulo de referencia : https://medium.com/rubycademy/symbol-in-ruby-daca5abd4ab2


# Ranges

Algunas veces necesitamos tener un rango de valores, por ejemplo en un sistema de calificación. Si un estudiante obtiene una calificación de 60 a 100 puntos, su calificación es A, de 50 a 59 su calificación es B y así sucesivamente. Cuando necesitemos lidiar con un rango de valores

```ruby

(1..5).each {|a| print "#{a}, " }

1, 2, 3, 4, 5,  => 1..5 

```

OK, ¿qué es eso (1..5) en la declaración anterior, esto se llama Rango. El rango es un objeto que tiene un valor superior y un valor inferior y todos los valores intermedios. Tenga en cuenta que, al igual que la matriz, todos y cada uno de los valores de un rango se pueden obtener utilizando cada método como se muestra arriba.


```ruby

 ("bad".."bag").each {|a| print "#{a}, " }

=> bad, bae, baf, bag, => "bad".."bag"
```

Otro Ejemplo

```ruby

a = -4..10
=> -4..10
```
```ruby
a.class
=> Range
```

Como podemos ver, pertenece a la clase Range

Para obtener el valor máximo en un rango, use el método max como se muestra

```range
>> a.max
```

```
=> 10
```

Para obtener el mínimo en un rango, use el método min como se muestra

```ruby
>> a.min

```

```
=> -4
``` 

Es posible convertir el rango a una matriz usando el método to_a como se muestra


```ruby
a.to_a
```
```ruby
=> [-4, -3, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

```

Comprobemos intervalos

Otro uso de Rangos es verificar si algo está ubicado en un intervalo particular.

```ruby
print "Ingrese una letra "
letra = gets.chop

puts "Digito una minuscula" if  ('a'..'z') === letra
puts "Digito una mayuscula" if  ('A'..'Z') === letra
```

Salida

```ruby
Ingrese una letra : R
Digito una mayuscula
```

Usando 3 puntos


```ruby
>> (1..5).to_a
=> [1, 2, 3, 4, 5]
>> (1...5).to_a
=> [1, 2, 3, 4]
```

Consulte el fragmento de código anterior cuando escribo (1..5) .to_a obtenemos una salida de matriz como [1, 2, 3, 4, 5], pero para (1 ... 5) .to_a obtenemos una salida como [1 , 2, 3, 4]. Los puntos triples ignoran el último valor en el rango.


# Funciones


```ruby
| def print_line
  puts '_'*20
end

print_line
puts "TITULO"
print_line

``` 

###Paso de argumento en las funciones

```ruby
def print_line length
  puts '_'*length
end

10.step(50,10) do |x|
  print_line x
end

40.step(10,-10) do |x|
   print_line x
 end

```

### Argumentos predeterminados en las funciones


```ruby

def print_line length = 20
  puts '_'*length
end

print_line
print_line 40

```


Puede ver en el programa, en la función print_line al dar length = 20, hemos indicado que si no se pasa ningún argumento, la función debe asumir que el valor de length es 20. Si se pasa, este valor se anulará con el valor que pase. Como puede ver en la primera llamada a la función, simplemente llamamos a la función simplemente por su nombre print_line, no nos molestamos en pasarle el valor de la longitud, pero vemos que se imprime una línea de 20 unidades de longitud en la salida.

# Pasando arrays a las funciones



```ruby
def array_changer array
  array << 6
end

some_array = [1, 2, 3, 4, 5]
p some_array
array_changer some_array
p some_array


``` 
salida
```
[1, 2, 3, 4, 5]
[1, 2, 3, 4, 5, 6]

```
Si es un recién llegado a la programación, esto puede no ser sorprendente, pero cuando una variable se pasa a una función, no se supone que cambie su valor. Pero en el caso de la matriz, dentro de la función array_changer, le estamos agregando un elemento y cambia. Bueno, este es un comportamiento peculiar de una matriz que se pasa a una función.

Para evitar tal comportamiento, pruebe el siguiente programa

```ruby
def array_changer array
  array << 6
end

some_array = [1, 2, 3, 4, 5]
p some_array
array_changer Marshal.load(Marshal.dump(some_array))
p some_array

```
Salida

```
[1, 2, 3, 4, 5]
[1, 2, 3, 4, 5]
```

Aquí la matriz no se cambia, mira la línea array_changer Marshal.load (Marshal.dump (some_array)), este código copia some_array al argumento de la función para que incluso cuando se cambia dentro de la función, no se cambie fuera de la función.

#Retornar valores


Hasta ahora hemos visto que la función toma argumentos, ahora veremos que la función puede devolver valores que pueden usarse para algún propósito. Ahora veamos el programa function_return.rb, estudiemos el código, lo escribimos y lo ejecutamos.

```ruby
def addition x, y
  sum = x+y
  return sum
end

a, b = 3, 5

puts addition a,b
```
salida
``` 
8
```


El resultado que sale después de ejecutar es 8. Tenga en cuenta el método denominado adición en el programa anterior. Acepta dos argumentos **x** e **y**, dentro del método declaramos una variable llamada suma que se asigna a la suma de **x** con **y**. La siguiente declaración es el héroe aquí, vea que hemos usado una palabra clave return, esto devuelve el valor de la función. En el programa anterior, devolvemos la suma y, por lo tanto, cuando obtenemos la respuesta.

No es que debamos usar la declaración return para devolver un valor. La última instrucción que se ejecuta en una función Ruby se devuelve por defecto. 

Considere el programa **function_last_gets_returned.rb** que se muestra a continuación. En él tenemos un método llamado **square_it** que acepta un solo argumento llamado **x**. Tiene una sola declaración **x ** 2**, que también es la última declaración.


```ruby
def square_it x
  x**2
end

puts square_it 5
```
Salida

```
25
```

Como puede ver, hemos llamado square_it 5 y obtenemos 25 como resultado. Es posible porque en Ruby el resultado de la última declaración ejecutada se devuelve por defecto.


# Argumentos clasve[Keyword arguments]

```ruby
def say_hello name: "Martin", age: 33
  puts "Hello #{name} your age is #{age}"
end

say_hello name: "Joseph", age: 7
say_hello age: 21, name: "Vignesh"
say_hello
```


Salida
```
Hello Joseph your age is 7
Hello Vignesh your age is 21
Hello Martin your age is 33
```

Entonces, para ver cómo funciona esta característica, analicemos el código. Mire la definición de la función de say_hello, es como se muestra a continuación

```ruby
def say_hello name: "Martin", age: 33
  puts "Hello #{name} your age is #{age}"
end
```

Mire la parte resaltada def say_hello name: "Martin", edad: 33. Aquí no especificamos argumentos como def say_hello name = "Martin", age = 33, sino que usamos un nombre especial: "Martin", hemos eliminado el signo igual y reemplazado con dos puntos. Entonces, ¿de qué sirve? Ahora observe la parte donde se llama la función


```ruby
say_hello name: "Joseph", age: 7
say_hello age: 21, name: "Vignesh"
say_hello
```

La primera línea es directa say_hello name: "Joseph", edad: 7, aquí el primer argumento es name y el segundo argumento es age. Pero mire el código say_hello age: 21, nombre: "Vignesh", aquí el primer argumento es age y el segundo es name. Pero como la palabra clave insinúa el argumento, su posición es irrelevante y el método imprime una cadena como esperamos.

La tercera línea say_hello es solo para mostrar lo que sucede si se pierden los argumentos, ya que hemos especificado valores predeterminados, toma los predeterminados. ¿Es posible utilizar argumentos de palabras clave con valores predeterminados? Absolutamente sí.

```ruby

def say_hello name:, age:
    puts "Hello #{name} your age is #{age}"
  end

  say_hello name: "Joseph", age: 7
  say_hello age: 21, name: "Vignesh"
  # say_hello # uncomment it and try it out
  # say_hello "Karthik", 32 # uncomment it and try it out
```

# Funciones Recursivas

 Todas las computadoras usan una cosa llamada álgebra booleana para hacer todas las tareas. No diría que debes ser matemático para ser programador, pero saber matemáticas ayuda.

OK, ¿qué es un factorial? Tome un número, tomemos **3**, ahora lo que será **3 X 2 X 1**, ¡serán seis! ¿No es simple? **6** es factorial de **3**. Bueno, tomaremos **4** ahora, por lo que **4 X 3 X 2 X 1** será **24**, de manera similar el factorial de **2** será **2 X 1**, que es **2**. Habiendo equipado con este conocimiento, ahora construiremos un programa que nos dará factorial de un número.

```Ruby

# factorial

def factorial num
  fact = 1
  1.upto(num) { |a|
    fact = fact * a
  }
  fact
end

number = 17
puts "Factorial of #{number} = #{factorial number}"
```
Salida 
```
Factorial of 17 = 355687428096000

```

En el ejemplo anterior (en la función factorial) hemos tomado todos los números del uno al número particular, lo hemos multiplicado y tenemos factorial. 

Veamos este codigo:

```ruby
def factorial num
  return 1 if num == 1
  return num * factorial(num-1)
end

number = 17
puts "Factorial of #{number} = #{factorial number}"
```

Salida
```ruby
Factorial of 17 = 355687428096000
```

La salida es la misma que la del programa anterior factorial.rb. Observe muy de cerca la función denominada factorial en el programa anterior. Déjame enumerarlo para que lo veas

```ruby

def factorial num
        return 1 if num == 1
        return num * factorial(num-1)
end
```


Tome el número 1. El factorial es 1. Entonces, si se encuentra 1, se devuelve 1 como se muestra en el código 


Ahora tome el número 2. Factorial de 2 X 1, que es 2 factorial multiplicado de 1. En otras palabras, podemos escribirlo como 2 multiplicado por factorial de 2-1. Entonces, si se encuentra el número dos en la función factorial, omite la primera instrucción if y la segunda instrucción return num * factorial (num-1) a continuación se ejecuta


En esto sucede algo interesante. Aquí se llama factorial (2-1), es decir, la función factorial se llama a sí misma. Entonces, cuando se llama factorial de 2-1, es decir, factorial de 1, devuelve 1, este 1 se multiplica por 2 y se devuelve, por lo que en este caso 2 se devuelve finalmente.

Ahora tome el número 3. Su factorial es 3 X 2 X 1. Esto se puede escribir como 3 multiplicado por el factorial 2. El factorial 2 se traduce como 2 multiplicado por el factorial 1. Por lo tanto, el resultado se obtiene finalmente. Para cualquier número mayor que 1, la función factorial se llama a sí misma repetidamente. El proceso de la función que se llama a sí mismo se llama **recursividad**.

# Numero de argumentos Variables

Digamos que no sabe cuántos argumentos se pasan a una función, digamos que está escribiendo una función para agregar N números, el valor de N no se conoce, entonces, ¿cómo podría obtener un número variable de argumentos? Bueno, escriba el programa function_variable_arguments.rb que se proporciona a continuación y ejecútelo.

```ruby

def some_function a, *others
  puts a
  puts "Others are:"
  for x in others
    puts x
  end
end

some_function 1,2,3,4,5

```

Salida

```
1
Others are:
2
3
4
5
```


Entonces la salida del programa se muestra arriba. Como ve, pasamos 1,2,3,4,5 como argumentos, entonces a es solo una variable y, por lo tanto, toma el valor 1, las otras variables son absorbidas por la variable otras (tenga en cuenta la estrella antes del nombre de la variable) que es un tipo especial de argumento, toma el resto de los argumentos que no son absorbidos por las variables de argumento anteriores y lo almacena en el nombre de la variable otros (como una matriz). 


```ruby

for x in others
        puts x
end
```
Bueno, eso es todo. Ahora intente escribir una función para encontrar el máximo de n números y escriba otra función para encontrar el mínimo de n números y escriba un programa para encontrar el máximo y mínimo de un grupo de números.

# Hashes como argumentos en las funciones

Otra forma de colarse en múltiples argumentos en una función es pasarlos como hashes. Mire el programa a continuación, tenemos una función llamada some_function que obtiene dos argumentos, el primero llamado first_arg y el segundo llamado others_as_hash, llamamos a esta función en la siguiente línea some_function "Yoda", {jedi: 100, espada: 100 , coming_future: 100}, ejecútelo y observe la salida


```ruby
def some_function first_arg, others_as_hash
  puts "Your first argument is: #{first_arg}"
  puts "Other arguments are:"
  p others_as_hash
end

some_function "Yoda", {jedi: 100, sword: 100, seeing_future: 100}
```

Salida
```
Your first argument is: Yoda
Other arguments are:
{:jedi=>100, :sword=>100, :seeing_future=>100}
```

Como esperábamos, el programa imprime el primer argumento y el hash pasó a otros_como_hash, bueno, este no es una sorpresa, pero eche un vistazo al programa hashes_to_function_1.rb a continuación, ejecútelo, su salida será la misma que el programa anterior

```ruby
def some_function first_arg, others_as_hash
  puts "Your first argument is: #{first_arg}"
  puts "Other arguments are:"
  p others_as_hash
end

some_function "Yoda", jedi: 100, sword: 100, seeing_future: 100
```


Pero solo tenga en cuenta esta parte, hemos llamado a alguna_función como se muestra

```
some_function "Yoda", jedi: 100, sword: 100, seeing_future: 100
```


En la función pasamos el segundo argumento como un hash pero se da como se muestra arriba, tenga en cuenta que hemos evitado convenientemente las llaves y todavía funciona. Ese es el punto