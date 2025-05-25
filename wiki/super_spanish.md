<!--
Meta Description: # Uso de "super" en Ruby: Guía Completa para Desarrolladores ## Sinopsis El uso de la palabra clave "super" en Ruby permite a los desarrolladores llam...
Meta Keywords: clase, padre, super, desde, hijo
-->

# Uso de "super" en Ruby: Guía Completa para Desarrolladores

## Sinopsis
El uso de la palabra clave "super" en Ruby permite a los desarrolladores llamar a métodos de la clase padre desde una clase hija, facilitando así la herencia y permitiendo extensiones en el comportamiento de los métodos.

## Documentación
La palabra clave `super` se utiliza en Ruby para invocar un método de la clase padre de un objeto. Es especialmente útil en el contexto de la herencia, donde una clase hija puede querer extender o modificar el comportamiento de un método definido en su clase padre.

### Propósito
El propósito principal de `super` es permitir que las clases hijas accedan a la implementación de métodos de sus clases padres, manteniendo la funcionalidad original mientras se agrega o modifica el comportamiento.

### Uso
Para utilizar `super`, simplemente se debe incluir la palabra clave dentro de un método en la clase hija. Si se llama a `super` sin argumentos, se pasan los argumentos que se recibieron en el método actual. Si se llaman a `super` con argumentos, se pueden especificar diferentes argumentos que se pasan al método de la clase padre.

### Detalles
- **Sin argumentos**: Llama al método padre con los mismos argumentos que recibió el método hijo.
- **Con argumentos**: Llama al método padre con los argumentos especificados.
- **Sin parámetros**: Si el método padre no acepta parámetros, se puede invocar `super` sin argumentos.

## Ejemplos

### Ejemplo básico sin argumentos
```ruby
class Padre
  def saludo
    puts "Hola desde la clase Padre"
  end
end

class Hijo < Padre
  def saludo
    super
    puts "Hola desde la clase Hijo"
  end
end

h = Hijo.new
h.saludo
# Salida:
# Hola desde la clase Padre
# Hola desde la clase Hijo
```

### Ejemplo con argumentos
```ruby
class Padre
  def saludo(nombre)
    puts "Hola, #{nombre} desde la clase Padre"
  end
end

class Hijo < Padre
  def saludo(nombre)
    super(nombre)
    puts "Hola, #{nombre} desde la clase Hijo"
  end
end

h = Hijo.new
h.saludo("Carlos")
# Salida:
# Hola, Carlos desde la clase Padre
# Hola, Carlos desde la clase Hijo
```

### Ejemplo con argumentos personalizados
```ruby
class Padre
  def saludo(nombre)
    puts "Hola, #{nombre} desde la clase Padre"
  end
end

class Hijo < Padre
  def saludo(nombre)
    super("amigo #{nombre}")
    puts "Hola, #{nombre} desde la clase Hijo"
  end
end

h = Hijo.new
h.saludo("Carlos")
# Salida:
# Hola, amigo Carlos desde la clase Padre
# Hola, Carlos desde la clase Hijo
```

## Explicación
Al usar `super`, es importante recordar:
- **Métodos no definidos**: Si intentas usar `super` para un método que no está definido en la clase padre, se generará un error `NoMethodError`.
- **No se puede anidar indefinidamente**: Si `super` se llama en una cadena de herencia, la llamada se propaga a la clase padre más cercana que contiene el método.
- **Contexto de instancia**: `super` se utiliza generalmente dentro de métodos de instancia, por lo que no tendrá efecto si se usa en métodos de clase o en contextos donde no hay una relación de herencia directa.

## Resumen en una línea
La palabra clave `super` en Ruby permite a las clases hijas invocar métodos de sus clases padres, facilitando la herencia y la modificación del comportamiento.