<!--
Meta Description: # Cargar Archivos en Ruby: Uso del Método `load` ## Sinopsis El método `load` en Ruby se utiliza para cargar y ejecutar un archivo Ruby en el contexto...
Meta Keywords: archivo, load, ruby, que, cargar
-->

# Cargar Archivos en Ruby: Uso del Método `load`

## Sinopsis
El método `load` en Ruby se utiliza para cargar y ejecutar un archivo Ruby en el contexto actual. Permite la reejecución de scripts y es útil para trabajar con código que puede cambiar dinámicamente.

## Documentación
### Propósito
El método `load` se utiliza para cargar un archivo Ruby y ejecutar su contenido en el contexto del programa actual. A diferencia de `require`, el método `load` permite volver a cargar el archivo cada vez que se llama, lo que es útil durante el desarrollo y la depuración.

### Uso
La sintaxis básica del método `load` es la siguiente:

```ruby
load('ruta/al/archivo.rb')
```

### Detalles
- **Ruta del Archivo**: Debe proporcionar una ruta válida al archivo Ruby que desea cargar. Puede ser una ruta relativa o absoluta.
- **Reejecución**: Cada vez que se llama a `load`, el archivo se vuelve a cargar y se ejecuta desde el principio.
- **Extensión**: Asegúrese de incluir la extensión `.rb` en el nombre del archivo, ya que `load` no la asumirá automáticamente.
- **Variables Globales**: Las variables definidas en el archivo cargado estarán disponibles en el contexto donde se llamó a `load`.

## Ejemplos
### Ejemplo Básico
```ruby
# archivo.rb
def saludo
  puts "¡Hola, mundo!"
end

# archivo_principal.rb
load('archivo.rb')
saludo  # Esto imprimirá "¡Hola, mundo!"
```

### Reejecución de un Archivo
```ruby
# archivo.rb
$contador ||= 0
$contador += 1
puts "Contador: #{$contador}"

# archivo_principal.rb
load('archivo.rb')  # Salida: Contador: 1
load('archivo.rb')  # Salida: Contador: 2
```

## Explicación
### Errores Comunes
- **Ruta Incorrecta**: Si la ruta del archivo es incorrecta, Ruby lanzará un error `LoadError`. Asegúrese de que la ruta sea correcta.
- **Reejecución No Deseada**: Si no desea que un archivo se ejecute varias veces, considere usar `require` en su lugar, ya que este solo carga el archivo una vez.
- **Variables Globales**: Tenga cuidado al usar variables globales, ya que pueden llevar a comportamientos inesperados si se redefinen en el archivo cargado.

## Resumen en Una Línea
El método `load` en Ruby permite cargar y ejecutar un archivo Ruby en el contexto actual, permitiendo su reejecución en cualquier momento.