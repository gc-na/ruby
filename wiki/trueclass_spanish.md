<!--
Meta Description: # TrueClass en Ruby: Comprendiendo la Clase Boolean ## Sinopsis TrueClass es una clase en Ruby que representa el valor booleano verdadero (`true`). Se...
Meta Keywords: true, trueclass, ruby, que, métodos
-->

# TrueClass en Ruby: Comprendiendo la Clase Boolean

## Sinopsis
TrueClass es una clase en Ruby que representa el valor booleano verdadero (`true`). Se utiliza en la evaluación de condiciones y en la lógica del programa, siendo fundamental en la estructura de control del flujo en Ruby.

## Documentación
TrueClass es una de las dos clases booleanas en Ruby, siendo la otra FalseClass, que representa el valor `false`. En Ruby, `true` es un objeto de la clase TrueClass, lo que significa que puedes llamar a métodos sobre él como lo harías con cualquier otro objeto.

### Propósito
La clase TrueClass permite a los desarrolladores trabajar con valores booleanos de manera efectiva, facilitando la toma de decisiones en el código.

### Uso
Algunas funciones y métodos asociados a TrueClass incluyen:

- **Métodos de comparación**: Puedes utilizar `true` en expresiones condicionales.
- **Métodos de objeto**: Al ser un objeto, `true` puede invocar métodos como `class`, `to_s`, entre otros.

### Detalles
- **Instancia única**: En Ruby, solo existe una instancia de TrueClass, que es el valor `true`.
- **Booleano como objeto**: A diferencia de otros lenguajes donde los booleanos son primitivos, en Ruby, `true` es un objeto, lo que permite la extensión de su funcionalidad.

## Ejemplos
```ruby
# Ejemplo básico de uso de true
if true
  puts "Esto se ejecutará porque la condición es verdadera."
end

# Uso de métodos de TrueClass
puts true.class      # Salida: TrueClass
puts true.to_s       # Salida: "true"
puts true.inspect    # Salida: "true"
```

## Explicación
Al trabajar con TrueClass, es importante recordar que:

- **Siempre verdadero**: El valor `true` siempre evaluará a verdadero en condiciones.
- **No a confundir con nil**: En Ruby, `nil` y `false` son los únicos valores que se consideran falsos. Cualquier otro valor, incluidos los objetos y `true`, se consideran verdaderos en condiciones.
- **Métodos no siempre disponibles**: Algunos métodos pueden no ser aplicables a true en contextos donde se esperan otros tipos de datos.

## Resumen en una línea
TrueClass en Ruby representa el valor booleano verdadero, permitiendo una programación lógica y estructurada.