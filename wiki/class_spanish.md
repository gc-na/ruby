<!--
Meta Description: # Clase en Ruby: Definición, Uso y Ejemplos ## Sinopsis En Ruby, una clase es un plano para crear objetos. Define métodos y propiedades que los objeto...
Meta Keywords: ruby, clase, end, que, clases
-->

# Clase en Ruby: Definición, Uso y Ejemplos

## Sinopsis
En Ruby, una clase es un plano para crear objetos. Define métodos y propiedades que los objetos instanciados a partir de la clase pueden usar. Las clases son fundamentales en la programación orientada a objetos y permiten la encapsulación y la reutilización de código.

## Documentación
Las clases en Ruby se definen utilizando la palabra clave `class`, seguida del nombre de la clase y un bloque que contiene las definiciones de métodos y atributos. Al crear una clase, puedes definir tanto métodos de instancia como métodos de clase.

### Propósito
Las clases permiten organizar el código de manera lógica y estructurada, facilitando la creación de objetos que representan conceptos del mundo real.

### Uso
Para definir una clase en Ruby, se utiliza la siguiente sintaxis básica:

```ruby
class NombreDeLaClase
  def metodo
    # código del método
  end
end
```

Puedes crear un objeto de la clase utilizando el método `new`:

```ruby
objeto = NombreDeLaClase.new
```

### Detalles
Las clases pueden heredar de otras clases, lo que permite la creación de jerarquías de clases. Ruby también soporta módulos que permiten la mezcla de funcionalidades en clases. 

## Ejemplos

### Ejemplo 1: Clase simple
```ruby
class Perro
  def ladrar
    puts "¡Guau!"
  end
end

mi_perro = Perro.new
mi_perro.ladrar  # Salida: ¡Guau!
```

### Ejemplo 2: Clase con atributos
```ruby
class Gato
  attr_accessor :nombre
  
  def initialize(nombre)
    @nombre = nombre
  end
  
  def maullar
    puts "#{@nombre} dice: ¡Miau!"
  end
end

mi_gato = Gato.new("Felix")
mi_gato.maullar  # Salida: Felix dice: ¡Miau!
```

### Ejemplo 3: Herencia
```ruby
class Animal
  def hablar
    "El animal hace un sonido"
  end
end

class Pajaro < Animal
  def hablar
    "El pájaro canta"
  end
end

pajaro = Pajaro.new
puts pajaro.hablar  # Salida: El pájaro canta
```

## Explicación
Un error común al trabajar con clases en Ruby es olvidar el uso del método `initialize`, que actúa como un constructor para inicializar los atributos del objeto. También es importante recordar que los nombres de las clases deben comenzar con una letra mayúscula, y el uso de `attr_accessor`, `attr_reader` y `attr_writer` facilita la creación de métodos de acceso a los atributos.

Además, hay que tener cuidado con el alcance de las variables de instancia (prefijadas con `@`), ya que son accesibles solo dentro de la instancia de la clase donde se definen.

## Resumen en una línea
Las clases en Ruby son estructuras que permiten definir objetos, encapsulando métodos y atributos para facilitar la programación orientada a objetos.