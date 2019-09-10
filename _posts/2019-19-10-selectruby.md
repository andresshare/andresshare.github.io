---
layout: post
title:  "Como funciona metodo select en Ruby"
date:   2019-19-10 22:08:10 +0530
categories: ruby
---


![.select en Ruby](https://media.giphy.com/media/xUn3CftPBajoflzROU/giphy-downsized-large.gif)


Su usa para filtrar una matriz de objetos.

revise este ejemplo

```ruby
numeros_pares = []
[1,2,3,4,5,6].each do |n|
  if n.even?
    numeros_pares << n
  end
end

```

En el codigo anterior, muestro una de las formas de obtener los numeros pares ahora 
usando **.select** se hace mas facil

```ruby
[1,2,3,4,5,6].select { |n| n.even? }
```


si queremos mas simplicidad

```ruby
[1,2,3,4,5,6].select(&:even?)
```

si no le es familiar esta expresion ```&:even?```
significa que se llama al metodo directamente


Por otra parte es comun usar .select en ```HASHES```


```ruby
carrros = {
  volskwagen: 10,
  fiat: 5,
  mazda: 1
}
carros.select { |k, v| v > 1 }
```

En el ejemplo anterior buscamos
carros > 1 , las letras `K` viene de key y `v` valor


Si queremos tener un poco mas de poder con `enumerable`

```ruby
carros =%w(volskwagen,fiat,mazda)
carros.select.with_index { |palabra, idx| idx.even?}
```

Esto le permite filtrar usando el índice, en lugar del objeto para este caso, una cadena en sí

# Creando un nuevo array

Al usar  `select` se crea una nueva matriz

si va a cambiar la matriz use
`select!`


```ruby
carros = %w(volskwagen fiatmazda)
carros.select! { |carros| carros.start_with? "v" }
```
Recuerde que en Ruby trabajamos convencion sobre configuracion

En el camino se preguntara si escojer entre **FIND** o **SELECT**

Select funciona muy bien si ud quiere filtrar una lista y devolver un array con los resultados

Pero si usted solo quiere enconrar un objeto

use **FIND**

```ruby
palabras= %w(o one ones juanes)
palabras.find { |l| l.size == 3 }
palabras.find { |l| l.size == 8 }
```

si encuentra en el resultado la palabra `nil` significa que el resultado no fue encontrado

ahora,veamos el metodo ``` find_all``` como lo relacionamos con ```FIND``` y ``` SELECT```

Eureka!


``` find_all``` es un alias para ```select```
```find``` le permite buscar un objeto especifico.

en ruby 2.6 añade otro alias para  ```select```

```ruby
filter
```

si se ha preguntado cual es el OPUESTO de select 


```ruby

[1,2,3,4,5,6].select { |n| n != 4 }
```
en el ejemplo anterior puede eliminar elementos que no quiere. evitado la opcion de los que si quiere

entonces con ```reject```

```ruby
[1,2,3,4,5,6].reject { |n| n == 4 }
```

esta opcion no tiene mejora en rendimiento.lo que si ocurrira es mas legible.

HABLEMOS DE **RAILS**

Si ha trabajado con rails & models sabe que tambien puede usar  ```select```

```ruby
Car.select(:id, model:, :color)
```
Al usar ```ActiveRecord``` con `select` se hace asi por cuestiones de rendimiento

Me despido hasta la proxima !
les dejo una guia de ruby 

💎 [Ruby poder sin limites](https://andresshare.github.io/ruby/2019/08/30/ruby-podersinlimites.html)