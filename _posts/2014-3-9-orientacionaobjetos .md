---
layout: post
title:  "OOP [Programacion orientada a objetos] "
date:   2014-03-09 20:00:15 +0530
categories: Concepto
---

![OOP](https://media.giphy.com/media/40DRc0W00UbgQ/giphy.gif)


Programacion orientada a objetos] Los programas son considerados como una coleccion de objetos.
Donde el **objeto** no es mas que una instancia de una clase. 

### Listado de conceptos basicos de OOP 

 * Abstraccion 
 * Encapsulacion 
 * Herencia 
 * Polimorfismo 


Veamos un poco estos conceptos aplicados al lenguaje Ruby

#### Casi todo es objeto

```ruby
# a es un objeto 
  # a.object_id da el identificador
  a = 10

  # igualmente b es también objeto
  b = "Hoola !"

```


Las matrices son objeto, la clase es objeto, los módulos son objeto, el rango también es objeto, los bloques de código pueden ser objeto, nada es también objeto que representa la nada y casi todo es objeto en rubí.

### Clases

La sintaxis para escribir la clase en ruby ​​es sencilla, solo debe escribir la palabra clave **class** y **class name**. El método dentro de la clase es pequeño y la sintaxis de mayúsculas y minúsculas es más preferida. La variable de instancia de clase en ruby ​​se puede iniciar con el **símbolo @**.

E **initialize** es la función especial de la clase que se llama automáticamente cuando se crea el objeto. Para crear el Objeto de la clase podemos usar la sintaxis **ClassName.new.** Uno de los ejemplos simples es el siguiente.


```ruby
require 'date'

class User
  def initialize(date_of_birth)
    days_since_birth = Date.today - Date.parse(date_of_birth)
    @age = days_since_birth / 365
  end
  def is_kid?
    @age <= 18
  end
end

john = User.new("2006-02-12")
puts john.is_kid? # Returns False
```

El método de inicialización se llama automáticamente cuando se crea el objeto, y el fragmento de código anterior se trata de la creación del objeto de la clase Usuario. La edad es la variable de clase.

### Metodos

Los métodos son bastante fundamentales para Ruby, el método solo comienza por el símbolo def, el nombre del método sin ninguno o más parámetros

```ruby
def another_method(first_arg, last_arg)
        "You passed in #{first_arg} and #{second_arg}"
    end
```

Es posible crear el nombre del método con mayúscula, pero no lo haga. Por lo tanto, escriba siempre el método en minúscula, este último conectado por el guión bajo.

```ruby
def ThisIsPossible
        # Please do not do this
end

```

Los métodos que devuelven verdadero o falso (valor booleano) siempre terminan con un signo de interrogación.

```ruby
 def is_not_boy?
      @gender != 'boy'
    end
```
Signo de exclamación ! al final del método en ruby ​​significa lookout, eso significa que el valor de referencia original de la propiedad también se cambia, así que tenga en cuenta. por ejemplo

```ruby
    message = "Hello World"
    message.downcase! # This change message value to 'hello world'
```


También podemos definir el argumento opcional en ruby, el argumento opcional siempre debe ser el último argumento en el método.

```ruby
 def greet(name, informal = false)
      if informal
        "hi #{name}"
      end
      else
        "Hello #{name}"
      end      
    end
```
Digamos que hay tres argumentos y dos de los argumentos son opcionales. no necesitamos enviar el valor predeterminado, pero si el tercer argumento es diferente del valor predeterminado del argumento, entonces deberíamos pasar los tres argumentos durante la llamada al método, ¿verdad? dejemos claro del ejemplo

```ruby

def greet(name, informal = false, shout = false)
      greeting = if informal then "hi" else "hello" end
      message = "#{greeting} #{name}"
      if shout
        message.upcase
      else
        message
      end
    end

    greet("John", false, true)
```

¡Para solucionar esto, podemos hacerlo así! Esta es una forma mucho más clara de pasar los argumentos en métodos ruby.

```ruby
def greet(name, informal: false, shout: false)
      greeting = if informal then "hi" else "hello" end
      message = "#{greeting} #{name}"
      if shout
        message.upcase
      else
        message
      end
    end

    greet("John", shout: true)
```

Normalmente no necesitamos devolver el valor en los métodos, el último valor del método es devuelto automáticamente por el método. Pero en algún momento deberíamos devolver si hay alguna condición, entonces podemos devolver el valor utilizando la palabra clave return como esta.

```ruby
class MyClass
      def odd_or_even(num)
        return unless num.respond_to?(:odd?)
        if num.odd? then  "odd" else "even" end
      end
    end

    MyClass.new.odd_or_even(3)
```

### Herencia

Ruby solo admite herencia única, lo que significa que cada clase en ruby ​​tiene exactamente una superclase. Podemos especificar una superclase escribiendo el signo '<' seguido del nombre de la superclase. La clase hereda los métodos de la superclase.

```ruby
class User
      attr_reder :name
      def initilize(name)
        @name = name
      end    
    end

    # child class of User class
    class Admin < User
      def is_admin
        true
      end
    end

    user = Admin.new("Madhu Sudhan")
    user.name # will results 'Madhu Sudhan'
    user.is_admin? # will return true
```

Aquí está el ejemplo de cómo una clase contiene exactamente una superclase. Vea el siguiente ejemplo

```ruby
Admin.superclass
    => User
    User.superclass
    => Object
    Object.superclass
    => BasicObject
    BasicObject.superclass
    => nil
```

### Modulos

Los módulos en ruby ​​son realmente solo una colección de métodos y la clase también es un tipo especial de módulo. Podemos definir módulos de la misma manera que una clase.
```ruby
require 'date'

module Employee
  attr_accessor :start_date

  def employment_length
    days = Date.today - start_date.to_date
    "#{days.to_i} days"
  end
end

class User
  include Employee
end

u = User.new
u.start_date = Date.today - 365
puts u.employment_length

```


Extender es otra forma de usar el módulo y es mucho más interesante, antes de usar la palabra clave include que el módulo define en la clase, pero también podemos usar la palabra clave extender para decirle al método una sola instancia de clase,

```ruby
require 'date'

module Employee
  attr_accessor :start_date

  def employment_length
    days = Date.today - start_date.to_date
    "#{days.to_i} days"
  end
end

class User
end

u = User.new
u.extend(Employee)
u.start_date = Date.today - 365
puts u.employment_length
```

### Constantes

Las constantes en rubí son muy similares a las constantes en cualquier otro idioma, violan la mutación del valor. Parece variable pero comienza con mayúscula. Es una convención que toda la letra de la constante debe estar en mayúscula.
```ruby
 PI = 3.14 # is good

    Pi = 3.14 # is possible but not do it
```


Usando las constantes en clase y Módulos se puede acceder de esta manera

```ruby
module Geometry
      PI = 3.14
    end

    class Circle
      PI = 3.142
    end

    puts Geometry::PI == Circle::PI # false
```

Es realmente interesante aprender el lenguaje de programación ruby ​​y también es fácil.