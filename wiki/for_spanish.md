<!--
Meta Description: # Bucle "for" en Ruby: Guía Completa y Ejemplos ## Sinopsis El bucle "for" en Ruby es una estructura de control que permite iterar sobre elementos de ...
Meta Keywords: bucle, que, ruby, una, del
-->

# Bucle "for" en Ruby: Guía Completa y Ejemplos

## Sinopsis
El bucle "for" en Ruby es una estructura de control que permite iterar sobre elementos de una colección, como arreglos o rangos, de manera sencilla y legible. Es una herramienta fundamental para realizar operaciones repetitivas.

## Documentación
El bucle "for" en Ruby se utiliza para recorrer elementos de una colección. Su sintaxis es sencilla y permite ejecutar un bloque de código para cada elemento en el conjunto.

### Propósito
El objetivo principal del bucle "for" es facilitar la iteración sobre colecciones de datos sin necesidad de manejar índices manualmente, lo que mejora la legibilidad del código.

### Uso
La sintaxis básica del bucle "for" es la siguiente:

```ruby
for variable in colección
  # Código a ejecutar
end
```

- **variable**: Es el nombre de la variable que contendrá cada elemento de la colección en cada iteración.
- **colección**: Puede ser un arreglo, un rango, o cualquier objeto que se pueda iterar.

### Detalles
- El bucle "for" es menos común que otros métodos de iteración como `each`, pero sigue siendo útil en ciertas situaciones.
- A diferencia del bloque `each`, el bucle "for" no crea un nuevo contexto de variable, lo que significa que cualquier variable definida dentro del bloque estará disponible fuera de él.

## Ejemplos
### Ejemplo 1: Iterar sobre un arreglo
```ruby
arreglo = [1, 2, 3, 4, 5]
for numero in arreglo
  puts numero
end
```
**Salida:**
```
1
2
3
4
5
```

### Ejemplo 2: Iterar sobre un rango
```ruby
for i in 1..5
  puts "Número: #{i}"
end
```
**Salida:**
```
Número: 1
Número: 2
Número: 3
Número: 4
Número: 5
```

## Explicación
Al usar el bucle "for", es importante tener en cuenta lo siguiente:

- **Alcance de variables**: Las variables definidas en el bloque del bucle "for" están disponibles fuera de él, lo que puede causar confusiones si se utilizan nombres de variables similares en diferentes contextos.
- **Preferencia por métodos de iteración**: Aunque el bucle "for" es útil, en muchos casos, se prefiere usar métodos como `each`, `map`, o `select` que son más idiomáticos en Ruby y a menudo ofrecen una mayor flexibilidad y claridad.

## Resumen en Una Línea
El bucle "for" en Ruby permite iterar fácilmente sobre colecciones, ejecutando un bloque de código por cada elemento.