<!--
Meta Description: # Array en Ruby: Todo lo que necesitas saber sobre los arreglos ## Sinopsis El tipo de dato **Array** en Ruby es una estructura fundamental que permit...
Meta Keywords: array, ruby, que, elementos, los
-->

# Array en Ruby: Todo lo que necesitas saber sobre los arreglos

## Sinopsis
El tipo de dato **Array** en Ruby es una estructura fundamental que permite almacenar colecciones de elementos. Con su flexibilidad y métodos integrados, los arrays son esenciales para manejar datos en la programación con Ruby.

## Documentación
En Ruby, un **Array** es una colección ordenada de elementos que pueden ser de diferentes tipos, incluyendo números, cadenas, objetos e incluso otros arrays. Los arrays son dinámicos, lo que significa que su tamaño puede cambiar durante la ejecución del programa.

### Propósito
El propósito principal de un array es almacenar y gestionar múltiples valores en una sola variable, facilitando el acceso y la manipulación de estos datos.

### Uso
Para crear un array en Ruby, puedes utilizar corchetes `[]`, o el método `Array.new`. Los elementos dentro del array se separan por comas.

#### Ejemplo de creación:
```ruby
mi_array = [1, 2, 3, 4, 5]
otro_array = Array.new([6, 7, 8, 9, 10])
```

### Métodos Comunes
Ruby ofrece una variedad de métodos para trabajar con arrays. Algunos de los más comunes incluyen:
- `push`: Agrega un elemento al final del array.
- `pop`: Elimina y devuelve el último elemento del array.
- `shift`: Elimina y devuelve el primer elemento del array.
- `unshift`: Agrega un elemento al inicio del array.
- `length`: Devuelve la cantidad de elementos en el array.

## Ejemplos
### Ejemplo 1: Crear y manipular un array
```ruby
# Crear un array
numeros = [10, 20, 30, 40]

# Agregar un elemento
numeros.push(50)

# Eliminar el último elemento
numeros.pop

puts numeros.inspect # Salida: [10, 20, 30, 40]
```

### Ejemplo 2: Iterar sobre un array
```ruby
nombres = ["Ana", "Luis", "Pedro"]

nombres.each do |nombre|
  puts "Hola, #{nombre}!"
end
```

### Ejemplo 3: Acceder a elementos
```ruby
dias = ["Lunes", "Martes", "Miércoles"]

puts dias[0] # Salida: Lunes
puts dias[-1] # Salida: Miércoles
```

## Explicación
Al trabajar con arrays en Ruby, es importante tener en cuenta algunos puntos críticos:
- **Índices Negativos**: Ruby permite acceder a elementos desde el final del array usando índices negativos. Por ejemplo, `array[-1]` accede al último elemento.
- **Mutabilidad**: Los arrays en Ruby son mutables, lo que significa que puedes cambiar su contenido después de haber sido creado.
- **Elementos de Diferentes Tipos**: Un array puede contener diferentes tipos de datos. Sin embargo, es buena práctica mantener la homogeneidad para evitar confusiones.

## Resumen en una línea
Los arrays en Ruby son estructuras dinámicas que permiten almacenar colecciones de elementos de diferentes tipos, facilitando su manipulación y acceso eficiente.