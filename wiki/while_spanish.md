<!--
Meta Description: # "while" en Ruby: Uso y Ejemplos Prácticos ## Sinopsis El bucle `while` en Ruby permite ejecutar un bloque de código repetidamente mientras una condi...
Meta Keywords: while, bucle, contador, condición, una
-->

# "while" en Ruby: Uso y Ejemplos Prácticos

## Sinopsis
El bucle `while` en Ruby permite ejecutar un bloque de código repetidamente mientras una condición especificada sea verdadera. Es una herramienta fundamental para el control de flujo en programación.

## Documentación
El bucle `while` es una estructura de control que se utiliza para repetir un bloque de código mientras se cumpla una condición. Su sintaxis es la siguiente:

```ruby
while condición
  # código a ejecutar
end
```

### Propósito
El propósito del bucle `while` es permitir la ejecución repetitiva de un código basado en una condición booleana. Si la condición es verdadera, el bloque de código se ejecutará; si es falsa, se detendrá.

### Uso
El bucle `while` se utiliza principalmente en situaciones donde no se conoce de antemano cuántas veces se debe ejecutar el bloque de código. A diferencia de un bucle `for`, que itera sobre un rango o colección, el `while` se basa enteramente en la evaluación de una condición.

## Ejemplos

### Ejemplo 1: Contador simple
```ruby
contador = 0
while contador < 5
  puts "El contador es: #{contador}"
  contador += 1
end
```
**Salida:**
```
El contador es: 0
El contador es: 1
El contador es: 2
El contador es: 3
El contador es: 4
```

### Ejemplo 2: Solicitar entrada hasta que sea válida
```ruby
entrada = ""
while entrada != "salir"
  puts "Escribe 'salir' para salir"
  entrada = gets.chomp
end
```

### Ejemplo 3: Bucle infinito (uso con precaución)
```ruby
while true
  puts "Esto se ejecutará indefinidamente. Presiona Ctrl+C para detener."
end
```

## Explicación
Al usar `while`, es importante asegurarse de que la condición eventualmente se vuelva falsa; de lo contrario, se puede crear un bucle infinito, lo que puede causar que el programa se cuelgue. Además, el incremento o modificación de la variable de control debe estar cuidadosamente diseñado para evitar que el bucle se ejecute indefinidamente.

### Errores comunes
- **Bucle infinito:** Si la condición nunca se vuelve falsa, el programa se quedará atascado en el bucle.
- **Modificación de variables:** Asegúrate de que las variables utilizadas en la condición se modifiquen dentro del bloque para evitar condiciones inesperadas.

## Resumen en una línea
El bucle `while` en Ruby permite ejecutar un bloque de código repetidamente mientras una condición sea verdadera, siendo fundamental para la manipulación de flujos de control.