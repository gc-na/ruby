<!--
Meta Description: # Uso de `rescue` en Ruby: Manejo de Excepciones Eficaz ## Sinopsis El comando `rescue` en Ruby se utiliza para manejar excepciones, permitiendo a los...
Meta Keywords: rescue, que, excepciones, ruby, error
-->

# Uso de `rescue` en Ruby: Manejo de Excepciones Eficaz

## Sinopsis
El comando `rescue` en Ruby se utiliza para manejar excepciones, permitiendo a los desarrolladores controlar el flujo de un programa en caso de que ocurran errores. Es una herramienta fundamental para construir aplicaciones robustas y resilientes.

## Documentación
El `rescue` es parte del mecanismo de manejo de errores en Ruby, que permite interceptar excepciones que pueden ocurrir durante la ejecución del código. Su propósito principal es prevenir que un programa se detenga abruptamente debido a errores no manejados. 

### Propósito
- Capturar excepciones específicas o generales.
- Proporcionar una forma de recuperación o manejo de errores.
- Mantener la ejecución del programa en un estado controlado.

### Uso
La sintaxis básica de `rescue` se integra dentro de un bloque `begin...end` o se puede usar directamente en métodos. Aquí hay un ejemplo básico:

```ruby
begin
  # Código que puede generar una excepción
  resultado = 10 / 0
rescue ZeroDivisionError
  puts "Error: No se puede dividir por cero."
end
```

En este caso, si ocurre una excepción de tipo `ZeroDivisionError`, el programa no se detendrá y se ejecutará la línea dentro del bloque `rescue`.

### Detalles
- Se pueden manejar múltiples tipos de excepciones usando múltiples cláusulas `rescue`.
- También se puede usar `rescue` sin especificar un tipo de excepción, lo que capturará cualquier error.

```ruby
begin
  # Código potencialmente problemático
  archivo = File.open("archivo_inexistente.txt")
rescue Errno::ENOENT
  puts "Error: El archivo no existe."
rescue => e
  puts "Se produjo un error: #{e.message}"
end
```

En este ejemplo, el primer bloque `rescue` maneja específicamente un error de archivo no encontrado, mientras que el segundo captura cualquier otro tipo de error.

## Ejemplos
### Ejemplo 1: Manejo de error de archivo
```ruby
begin
  contenido = File.read("documento.txt")
  puts contenido
rescue Errno::ENOENT
  puts "El archivo 'documento.txt' no se encontró."
end
```

### Ejemplo 2: Manejo de múltiples excepciones
```ruby
begin
  num = Integer('texto')
rescue ArgumentError
  puts "No se puede convertir el texto a un número."
rescue TypeError
  puts "Error de tipo."
end
```

## Explicación
Al utilizar `rescue`, es importante tener en cuenta algunos puntos críticos:
- **Orden de las excepciones**: Las cláusulas `rescue` se evalúan de arriba hacia abajo. Si una excepción es capturada por una cláusula, las siguientes no se evaluarán.
- **Rescue en métodos**: También se puede usar `rescue` dentro de métodos para manejar excepciones que puedan surgir durante su ejecución.
- **No usar `rescue` de manera excesiva**: Es recomendable no abusar de `rescue` para manejar situaciones que deberían ser evitadas mediante validaciones previas.

## Resumen en Una Línea
El comando `rescue` en Ruby permite manejar excepciones de manera efectiva, evitando que los programas se detengan abruptamente debido a errores.