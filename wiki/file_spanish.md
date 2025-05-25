<!--
Meta Description: # Archivo en Ruby: Uso y Manipulación de Archivos ## Sinopsis El módulo `File` en Ruby proporciona una interfaz para manipular archivos en el sistema ...
Meta Keywords: archivo, file, ruby, archivos, para
-->

# Archivo en Ruby: Uso y Manipulación de Archivos

## Sinopsis
El módulo `File` en Ruby proporciona una interfaz para manipular archivos en el sistema operativo, permitiendo la creación, lectura, escritura y eliminación de archivos de manera sencilla y eficiente.

## Documentación
El módulo `File` es parte de la biblioteca estándar de Ruby y se utiliza para interactuar con el sistema de archivos. Permite realizar diversas operaciones sobre archivos como abrir, leer, escribir, y cerrar archivos, entre otras. 

### Propósito
El objetivo principal del módulo `File` es proporcionar una forma fácil y segura de trabajar con archivos en Ruby, facilitando a los desarrolladores la gestión de datos persistentes.

### Uso
Para utilizar el módulo `File`, simplemente se invoca a través de su nombre seguido de los métodos deseados. Aquí hay algunos de los métodos más comunes:

- `File.open`: Abre un archivo y permite su lectura o escritura.
- `File.read`: Lee el contenido completo de un archivo.
- `File.write`: Escribe datos en un archivo.
- `File.delete`: Elimina un archivo del sistema.
- `File.exist?`: Verifica si un archivo existe.

## Ejemplos

### 1. Leer un Archivo
```ruby
contenido = File.read("archivo.txt")
puts contenido
```

### 2. Escribir en un Archivo
```ruby
File.open("archivo.txt", "w") do |f|
  f.write("Hola, mundo!")
end
```

### 3. Comprobar si un Archivo Existe
```ruby
if File.exist?("archivo.txt")
  puts "El archivo existe."
else
  puts "El archivo no existe."
end
```

### 4. Eliminar un Archivo
```ruby
File.delete("archivo.txt") if File.exist?("archivo.txt")
```

## Explicación
Al trabajar con archivos en Ruby, es crucial tener en cuenta algunos aspectos:

- **Modos de Apertura**: Al abrir un archivo, se pueden especificar diferentes modos como `r` (lectura), `w` (escritura) y `a` (adición). Elegir el modo correcto es esencial para evitar la pérdida de datos.
- **Manejo de Errores**: Siempre es recomendable manejar excepciones al trabajar con archivos, por ejemplo, usando `begin...rescue` para capturar errores en caso de que el archivo no exista o no se pueda acceder.
- **Cierre Automático**: Usar el bloque con `File.open` asegura que el archivo se cierre automáticamente una vez que se sale del bloque, lo que ayuda a liberar recursos.

## Resumen en una Línea
El módulo `File` en Ruby permite la manipulación eficiente de archivos para operaciones como lectura, escritura y eliminación.