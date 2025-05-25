<!--
Meta Description: # Módulo en Ruby: Definición, Uso y Ejemplos ## Sinopsis Un módulo en Ruby es un contenedor que agrupa métodos, clases y constantes, permitiendo la or...
Meta Keywords: módulo, métodos, los, una, end
-->

# Módulo en Ruby: Definición, Uso y Ejemplos

## Sinopsis
Un módulo en Ruby es un contenedor que agrupa métodos, clases y constantes, permitiendo la organización del código y la inclusión de funcionalidades en otras clases sin necesidad de herencia.

## Documentación
### Propósito
Los módulos en Ruby tienen varios propósitos fundamentales:
1. **Agrupación de Métodos**: Permiten organizar métodos relacionados que pueden ser utilizados en diferentes partes de una aplicación.
2. **Espacio de Nombres**: Ayudan a evitar conflictos de nombres entre métodos y clases, proporcionando un contexto para su uso.
3. **Mezcla de Funcionalidades (Mixins)**: Facilitan la inclusión de métodos en otras clases a través de la palabra clave `include`, permitiendo una forma de reutilización de código.

### Uso
Para definir un módulo, se utiliza la palabra clave `module`, seguida del nombre del módulo. Los métodos se definen dentro del módulo de la misma manera que en una clase. Para incluir un módulo en una clase, se utiliza la palabra clave `include`.

```ruby
module MiModulo
  def saludo
    "¡Hola desde el módulo!"
  end
end

class MiClase
  include MiModulo
end

objeto = MiClase.new
puts objeto.saludo  # Salida: ¡Hola desde el módulo!
```

### Detalles
- Los módulos no pueden ser instanciados directamente. Sin embargo, pueden ser incluidos en clases o extendidos en objetos.
- Los métodos de un módulo pueden ser definidos como `module_function`, lo que los convierte en métodos de módulo y de instancia al mismo tiempo.
- Los módulos pueden anidarse, lo cual ayuda a organizar mejor el código.

## Ejemplos
### Ejemplo Básico de Módulo
```ruby
module Matemáticas
  def self.sumar(a, b)
    a + b
  end
end

puts Matemáticas.sumar(3, 5)  # Salida: 8
```

### Ejemplo con Mezcla de Funcionalidades
```ruby
module Mensajes
  def mostrar_mensaje
    "Este es un mensaje."
  end
end

class Notificador
  include Mensajes
end

notificador = Notificador.new
puts notificador.mostrar_mensaje  # Salida: Este es un mensaje.
```

## Explicación
Al utilizar módulos, es importante recordar que:
- Los métodos definidos en un módulo no son accesibles directamente a menos que se incluyan en una clase.
- La inclusión de un módulo en una clase puede causar conflictos si hay métodos con el mismo nombre en la clase y el módulo. Es recomendable utilizar nombres únicos para evitar este problema.
- Los módulos no soportan herencia, por lo que no puedes crear una subclase de un módulo.

## Resumen en una Frase
Los módulos en Ruby son herramientas poderosas para agrupar métodos y constantes, facilitando la organización y reutilización del código a través de mixins.