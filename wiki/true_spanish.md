<!--
Meta Description: # "true" en Ruby: Comprendiendo el Valor Booleano Verdadero ## Sinopsis En Ruby, `true` es uno de los dos valores booleanos primarios que representan ...
Meta Keywords: true, ruby, que, valor, como
-->

# "true" en Ruby: Comprendiendo el Valor Booleano Verdadero

## Sinopsis
En Ruby, `true` es uno de los dos valores booleanos primarios que representan la verdad en las evaluaciones lógicas y condicionales. Junto con `false`, `true` es fundamental para la toma de decisiones en la programación.

## Documentación
### Propósito
El valor `true` en Ruby se utiliza para indicar que una condición es verdadera. Este valor es esencial en estructuras de control como `if`, `while` y en expresiones booleanas.

### Uso
`true` se puede utilizar directamente en expresiones, así como en comparaciones y condicionales. Es un objeto de la clase `TrueClass`, y siempre se evalúa como verdadero en contextos booleanos.

### Detalles
- **Clase**: `TrueClass`
- **Valor**: `true` es un singleton, es decir, hay una única instancia de `true` en Ruby.
- **Comparaciones**: Se puede comparar con otros valores booleanos, pero solo es igual a sí mismo y a `!false`.

## Ejemplos
### Ejemplo 1: Uso básico en una condición
```ruby
if true
  puts "Esto se imprimirá porque la condición es verdadera."
end
```

### Ejemplo 2: Comparación de booleanos
```ruby
puts true == true  # Imprime: true
puts true == false # Imprime: false
```

### Ejemplo 3: Uso en bucles
```ruby
counter = 0
while true
  puts "Contador: #{counter}"
  counter += 1
  break if counter >= 5
end
```

## Explicación
Un error común al trabajar con `true` es confundirlo con otros valores que pueden evaluarse como verdaderos, como el número 1 o el string "verdadero". En Ruby, solo `true` y `false` son valores booleanos. Además, `nil` se considera falso, mientras que cualquier otro objeto se evalúa como verdadero. Recuerda que `true` es distinto de `TrueClass` en el sentido de que el primero es un valor y el segundo es su clase.

## Resumen en una línea
En Ruby, `true` es el valor booleano que representa la verdad y se utiliza en expresiones y estructuras de control.