<!--
Meta Description: # Uso de "then" en Ruby: Guía Completa ## Sinopsis El comando `then` en Ruby es una palabra clave que se utiliza para mejorar la legibilidad de las es...
Meta Keywords: then, uso, ruby, que, código
-->

# Uso de "then" en Ruby: Guía Completa

## Sinopsis
El comando `then` en Ruby es una palabra clave que se utiliza para mejorar la legibilidad de las estructuras condicionales, permitiendo una sintaxis más clara en ciertas expresiones.

## Documentación
### Propósito
`then` se utiliza principalmente en sentencias condicionales `if` y `case`. Su función es separar la condición del bloque de código que se ejecutará si la condición es verdadera, lo que puede facilitar la lectura del código en situaciones complejas.

### Uso
La forma más común de utilizar `then` es en combinación con el `if`. La sintaxis básica es la siguiente:

```ruby
if condición then
  # código a ejecutar si la condición es verdadera
end
```

Sin embargo, es importante notar que el uso de `then` es opcional y, a menudo, se prefiere una sintaxis más directa sin su inclusión.

### Detalles
- `then` permite que el código sea más legible, especialmente en estructuras de control anidadas.
- Se puede usar en bloques `case` también, aunque su uso es menos común en este contexto.
- Aunque es una característica de Ruby, no todos los programadores la utilizan, por lo que su uso puede ser considerado una cuestión de estilo.

## Ejemplos
### Ejemplo 1: Uso básico con `if`

```ruby
edad = 18

if edad >= 18 then
  puts "Eres mayor de edad."
end
```

### Ejemplo 2: Uso con `case`

```ruby
opcion = 2

case opcion
when 1 then puts "Opción uno seleccionada."
when 2 then puts "Opción dos seleccionada."
else puts "Opción no válida."
end
```

### Ejemplo 3: Uso en una línea

```ruby
puts "Bienvenido" if nombre == "Juan" then puts "¡Hola, Juan!" end
```

## Explicación
### Errores Comunes
- **Sobrecarga de Sintaxis**: Muchos desarrolladores optan por no usar `then`, lo que puede hacer que el código sea más compacto y legible. El uso excesivo de `then` puede llevar a un código más difícil de entender.
- **Confusión con la Indentación**: En bloques grandes, la inclusión de `then` puede llevar a confusiones sobre el alcance del bloque de código. Mantener una buena indentación es clave.
- **Desuso en la Comunidad**: Algunos programadores novatos pueden sentirse confundidos o poco seguros al usar `then`, ya que es menos común en el código Ruby contemporáneo.

## Resumen en una línea
El comando `then` en Ruby se utiliza para mejorar la legibilidad de las estructuras condicionales, separando la condición del código a ejecutar.