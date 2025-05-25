<!--
Meta Description: # Hash en Ruby: Guía Completa y Ejemplos Prácticos ## Sinopsis Los hashes en Ruby son estructuras de datos que almacenan pares clave-valor, permitiend...
Meta Keywords: ruby, hash, que, clave, valor
-->

# Hash en Ruby: Guía Completa y Ejemplos Prácticos

## Sinopsis
Los hashes en Ruby son estructuras de datos que almacenan pares clave-valor, permitiendo un acceso rápido y eficiente a los datos. Son ideales para representar colecciones de información donde se necesita asociar valores específicos a claves únicas.

## Documentación
### Propósito
El propósito principal de un hash en Ruby es almacenar datos de una manera que permita un acceso rápido a los valores mediante sus claves. A diferencia de los arrays, que utilizan índices numéricos, los hashes utilizan claves que pueden ser de cualquier tipo de objeto.

### Uso
Para crear un hash en Ruby, se pueden usar llaves `{}` o el método `Hash.new`. Las claves pueden ser símbolos, strings, o cualquier otro tipo de objeto, y los valores pueden ser de cualquier tipo. 

#### Sintaxis básica:
```ruby
mi_hash = { clave1: 'valor1', clave2: 'valor2' }
```

#### Creación de un hash vacío:
```ruby
mi_hash_vacio = {}
```

#### Usando el método Hash.new:
```ruby
mi_hash = Hash.new
```

### Detalles
Los hashes en Ruby son mutables, lo que significa que puedes agregar, eliminar o modificar pares clave-valor después de su creación. También son iterables, lo que permite recorrer sus elementos utilizando métodos como `each`, `map`, y `select`.

## Ejemplos
1. **Creación de un hash:**
   ```ruby
   frutas = { 'manzana' => 3, 'naranja' => 5, 'plátano' => 2 }
   ```

2. **Acceso a valores:**
   ```ruby
   puts frutas['manzana']  # Salida: 3
   ```

3. **Agregar un nuevo par clave-valor:**
   ```ruby
   frutas['pera'] = 4
   ```

4. **Eliminar un par clave-valor:**
   ```ruby
   frutas.delete('naranja')
   ```

5. **Iterar sobre un hash:**
   ```ruby
   frutas.each do |clave, valor|
     puts "#{clave}: #{valor}"
   end
   ```

## Explicación
Al trabajar con hashes, es importante tener en cuenta que las claves deben ser únicas. Si se intenta agregar un nuevo valor con una clave que ya existe, el valor anterior será sobrescrito. Además, los hashes no tienen un orden garantizado hasta Ruby 1.9, donde se hizo un cambio para preservar el orden de inserción.

### Errores Comunes
- **Olvidar usar claves únicas:** Si se define un hash con claves duplicadas, solo se conservará el último valor asignado a esa clave.
- **Confusión con el acceso a valores:** No utilizar el tipo correcto de clave al acceder a valores puede resultar en `nil`.

## Resumen en Una Línea
Los hashes en Ruby son colecciones de pares clave-valor que permiten un acceso rápido y eficiente a datos, ideales para representar datos asociativos.