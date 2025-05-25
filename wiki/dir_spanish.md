<!--
Meta Description: # Dir en Ruby: Manipulación de Directorios y Archivos ## Sinopsis `Dir` es una clase en Ruby que proporciona métodos para interactuar con el sistema d...
Meta Keywords: dir, directorio, archivos, directorios, clase
-->

# Dir en Ruby: Manipulación de Directorios y Archivos

## Sinopsis
`Dir` es una clase en Ruby que proporciona métodos para interactuar con el sistema de archivos, permitiendo la creación, eliminación y manipulación de directorios y archivos de manera sencilla y eficiente.

## Documentación
La clase `Dir` en Ruby se utiliza para acceder y manipular el sistema de archivos. Permite realizar diversas operaciones como listar archivos en un directorio, cambiar el directorio de trabajo actual, y crear o eliminar directorios. Su uso es fundamental para el manejo de archivos en aplicaciones Ruby, facilitando la interacción con el sistema operativo.

### Propósito
El propósito principal de la clase `Dir` es simplificar la gestión de directorios y archivos, proporcionando una interfaz clara y concisa para realizar operaciones comunes.

### Uso
Para utilizar la clase `Dir`, primero necesitas incluirla en tu código, aunque generalmente está disponible de manera predeterminada. A continuación se presentan algunos de los métodos más comunes de la clase `Dir`:

- `Dir.pwd`: Devuelve el directorio de trabajo actual.
- `Dir.chdir(directory)`: Cambia el directorio de trabajo a `directory`.
- `Dir.entries(directory)`: Devuelve un array con todos los archivos y directorios en `directory`.
- `Dir.mkdir(directory)`: Crea un nuevo directorio.
- `Dir.rmdir(directory)`: Elimina un directorio vacío.

## Ejemplos
A continuación se presentan algunos ejemplos básicos de cómo utilizar la clase `Dir` en Ruby:

```ruby
# Obtener el directorio de trabajo actual
puts Dir.pwd

# Cambiar el directorio de trabajo
Dir.chdir('/ruta/al/nuevo/directorio')
puts "Nuevo directorio: #{Dir.pwd}"

# Listar archivos en un directorio
puts Dir.entries('/ruta/al/directorio')

# Crear un nuevo directorio
Dir.mkdir('nuevo_directorio')

# Eliminar un directorio vacío
Dir.rmdir('nuevo_directorio')
```

## Explicación
Al trabajar con la clase `Dir`, es importante tener en cuenta algunas consideraciones:

- **Permisos**: Asegúrate de tener los permisos adecuados para crear, eliminar o cambiar directorios en el sistema de archivos. De lo contrario, podrías encontrar errores de permisos.
- **Directorio vacío**: La eliminación de un directorio con `Dir.rmdir` solo es posible si el directorio está vacío. Si contiene archivos o subdirectorios, se generará un error.
- **Cambio de directorios**: Cambiar el directorio de trabajo con `Dir.chdir` afectará todas las operaciones posteriores que dependan de la ruta relativa.

## Resumen en una línea
`Dir` es una clase en Ruby que facilita la manipulación de directorios y archivos, permitiendo operaciones como listar, crear y eliminar directorios de forma sencilla.