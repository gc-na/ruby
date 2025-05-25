<!--
Meta Description: # Cuando Usar "when" en Ruby: Guía Completa ## Sinopsis El comando "when" en Ruby se utiliza dentro de una estructura de control de flujo llamada `cas...
Meta Keywords: when, case, que, una, expresión
-->

# Cuando Usar "when" en Ruby: Guía Completa

## Sinopsis
El comando "when" en Ruby se utiliza dentro de una estructura de control de flujo llamada `case`. Permite evaluar una expresión y ejecutar diferentes bloques de código según el resultado de esa evaluación, ofreciendo una forma más limpia y legible de manejar múltiples condiciones.

## Documentación
El `when` se utiliza junto con la palabra clave `case` para realizar comparaciones. Es especialmente útil cuando se tienen múltiples condiciones que se pueden evaluar de manera similar, ya que mejora la legibilidad del código en comparación con múltiples `if` y `elsif`.

### Propósito
El propósito de `when` es simplificar las decisiones en el flujo del programa. Permite evaluar una sola expresión y manejar múltiples resultados posibles sin necesidad de anidar estructuras condicionales.

### Uso
La sintaxis básica de `case` y `when` es la siguiente:

```ruby
case expresión
when valor1
  # Código a ejecutar si expresión == valor1
when valor2
  # Código a ejecutar si expresión == valor2
else
  # Código a ejecutar si no coincide con ninguno de los valores anteriores
end
```

## Ejemplos
### Ejemplo 1: Uso básico de `case` y `when`
```ruby
dia = "Lunes"

case dia
when "Lunes"
  puts "Es el inicio de la semana."
when "Viernes"
  puts "Es casi fin de semana."
else
  puts "Es un día normal."
end
```
**Salida:** `Es el inicio de la semana.`

### Ejemplo 2: Múltiples valores en un `when`
```ruby
mes = "Mayo"

case mes
when "Enero", "Febrero", "Marzo"
  puts "Es el primer trimestre del año."
when "Abril", "Mayo", "Junio"
  puts "Es el segundo trimestre del año."
else
  puts "Es el tercer trimestre del año."
end
```
**Salida:** `Es el segundo trimestre del año.`

## Explicación
Al usar `when`, es importante tener en cuenta que:

1. **Evaluación de igualdad:** `when` evalúa la igualdad usando `===`, lo que significa que también puede ser utilizado para evaluar patrones, como en el caso de clases.
2. **Orden de evaluación:** El primer `when` que coincide con la expresión se ejecutará, y el resto será ignorado.
3. **Uso de `else`:** Incluir un bloque `else` es opcional, pero es recomendable para manejar casos no considerados.
4. **Valores múltiples:** Puedes listar varios valores en una sola línea de `when` separándolos por comas.

### Errores comunes
- **Falta de `else`:** No incluir un bloque `else` puede llevar a resultados inesperados si la expresión no coincide con ningún `when`.
- **Confusión con `if`:** Recordar que `case` y `when` son más adecuados para múltiples condiciones, mientras que `if` puede ser mejor para condiciones más complejas o anidadas.

## Resumen en una línea
El comando `when` en Ruby se utiliza dentro de una estructura `case` para evaluar expresiones y ejecutar bloques de código según los resultados, mejorando la legibilidad del flujo de control.