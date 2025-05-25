<!--
Meta Description: # Operador "or" en Ruby: Uso y Ejemplos ## Sinopsis El operador `or` en Ruby es un operador lógico que se utiliza para combinar expresiones booleanas....
Meta Keywords: true, ruby, que, una, resultado
-->

# Operador "or" en Ruby: Uso y Ejemplos

## Sinopsis
El operador `or` en Ruby es un operador lógico que se utiliza para combinar expresiones booleanas. Se evalúa de izquierda a derecha y devuelve `true` si al menos una de las expresiones es verdadera.

## Documentación
El operador `or` es una forma de realizar operaciones lógicas en Ruby. Su propósito principal es evaluar dos o más condiciones y devolver un valor booleano (`true` o `false`). A diferencia del operador `||`, que también realiza una operación lógica "o", `or` tiene una menor precedencia, lo que afecta cómo se agrupan las expresiones en una evaluación.

### Uso
El uso del operador `or` es bastante sencillo. Se puede utilizar en estructuras de control, asignaciones de variables y en cualquier lugar donde se requiera una evaluación booleana. La sintaxis básica es:

```ruby
resultado = condicion1 or condicion2
```

En este caso, `resultado` será `true` si al menos una de las condiciones es verdadera.

## Ejemplos
### Ejemplo 1: Uso básico
```ruby
a = true
b = false
resultado = a or b  # resultado será true
```

### Ejemplo 2: Evaluación de condiciones
```ruby
x = 10
y = 20
resultado = (x < 5) or (y > 15)  # resultado será true, ya que y > 15 es verdadero
```

### Ejemplo 3: Uso en estructuras de control
```ruby
usuario_autenticado = false
es_admin = true

if usuario_autenticado or es_admin
  puts "Acceso concedido"
else
  puts "Acceso denegado"
end
```

## Explicación
Es importante tener en cuenta que el operador `or` tiene una menor precedencia que otros operadores, como `and`, `&&` o incluso la asignación `=`, lo que puede conducir a resultados inesperados si no se utiliza adecuadamente. Por ejemplo:

```ruby
resultado = false or true
puts resultado  # Imprimirá false, no true
```

Esto se debe a que la asignación se evalúa antes que `or`. Para evitar confusiones, es recomendable usar paréntesis para definir claramente el orden de evaluación:

```ruby
resultado = (false or true)
puts resultado  # Imprimirá true
```

## Resumen en una línea
El operador `or` en Ruby es un operador lógico que devuelve `true` si al menos una de las condiciones evaluadas es verdadera, y se caracteriza por su menor precedencia en comparación con otros operadores lógicos.