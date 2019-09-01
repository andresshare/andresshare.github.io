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



