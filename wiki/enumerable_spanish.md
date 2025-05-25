<!--
Meta Description: # Enumerable en Ruby: Guía Completa y Ejemplos ## Sinopsis Enumerable es un módulo fundamental en Ruby que proporciona un conjunto de métodos para tra...
Meta Keywords: ruby, que, métodos, enumerable, con
-->

# Enumerable en Ruby: Guía Completa y Ejemplos

## Sinopsis
Enumerable es un módulo fundamental en Ruby que proporciona un conjunto de métodos para trabajar con colecciones de datos. Permite la iteración y manipulación eficiente de arrays, hashes y otros objetos enumerables, facilitando tareas comunes como la búsqueda, filtrado y transformación de datos.

## Documentación
El módulo Enumerable se incluye en Ruby para proporcionar métodos que se pueden utilizar en objetos que implementan el método `each`. Esto incluye, pero no se limita a, arrays y hashes. Al incluir el módulo Enumerable en una clase, se pueden aprovechar métodos como `map`, `select`, `reject`, `find`, entre otros.

### Propósito
El propósito de Enumerable es ofrecer una interfaz clara y consistente para iterar y manipular colecciones de datos, lo que facilita el trabajo con conjuntos de elementos.

### Uso
Para utilizar los métodos de Enumerable, una clase debe incluir este módulo. La mayoría de las colecciones de Ruby ya lo incluyen, como Array y Hash.

### Métodos Comunes
Algunos de los métodos más utilizados de Enumerable incluyen:
- `map`: Aplica un bloque a cada elemento y devuelve un nuevo array con los resultados.
- `select`: Filtra los elementos que cumplen con la condición dada en el bloque.
- `reject`: Devuelve un nuevo array con los elementos que no cumplen con la condición.
- `each`: Itera sobre cada elemento de la colección.
- `reduce`: Combina todos los elementos de la colección usando un bloque y devuelve un solo resultado.

## Ejemplos

### Ejemplo 1: Uso de `map`
```ruby
numeros = [1, 2, 3, 4, 5]
cuadrados = numeros.map { |n| n ** 2 }
puts cuadrados # Salida: [1, 4, 9, 16, 25]
```

### Ejemplo 2: Uso de `select`
```ruby
numeros = [1, 2, 3, 4, 5]
pares = numeros.select { |n| n.even? }
puts pares # Salida: [2, 4]
```

### Ejemplo 3: Uso de `reject`
```ruby
numeros = [1, 2, 3, 4, 5]
impares = numeros.reject { |n| n.even? }
puts impares # Salida: [1, 3, 5]
```

### Ejemplo 4: Uso de `each`
```ruby
nombres = ["Ana", "Luis", "Carlos"]
nombres.each { |nombre| puts "Hola, #{nombre}!" }
# Salida:
# Hola, Ana!
# Hola, Luis!
# Hola, Carlos!
```

### Ejemplo 5: Uso de `reduce`
```ruby
numeros = [1, 2, 3, 4, 5]
suma = numeros.reduce(0) { |acc, n| acc + n }
puts suma # Salida: 15
```

## Explicación
Al trabajar con Enumerable, es importante recordar que la mayoría de sus métodos no modifican la colección original. En su lugar, devuelven nuevas colecciones. Esto puede ser un punto de confusión para los principiantes. Además, se debe tener cuidado con el uso de bloques; si un bloque no se proporciona, algunos métodos pueden generar errores.

Otro aspecto a considerar es que el uso de métodos como `find` y `select` puede implicar un rendimiento distinto en colecciones grandes, así que se recomienda realizar pruebas de rendimiento en casos críticos.

## Resumen en Una Línea
Enumerable es un módulo en Ruby que facilita la iteración y manipulación de colecciones de datos mediante métodos como map, select y reduce.