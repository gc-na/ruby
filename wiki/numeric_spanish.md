<!--
Meta Description: # Numeric en Ruby: Tipos y Operaciones ## Sinopsis Numeric es una clase base en Ruby que representa números, incluyendo enteros, flotantes y racionale...
Meta Keywords: numeric, números, ruby, operaciones, clase
-->

# Numeric en Ruby: Tipos y Operaciones

## Sinopsis
Numeric es una clase base en Ruby que representa números, incluyendo enteros, flotantes y racionales. Esta clase permite realizar operaciones matemáticas comunes y proporciona métodos para manipular y convertir números.

## Documentación
La clase Numeric en Ruby es una de las clases fundamentales que permiten trabajar con diferentes tipos de números. Ruby incluye varias subclases de Numeric, tales como Integer (números enteros) y Float (números de punto flotante). Numeric proporciona métodos útiles que se pueden usar para realizar cálculos, conversiones y comparaciones.

### Propósito
El propósito de la clase Numeric es permitir a los desarrolladores realizar operaciones matemáticas de manera sencilla, y facilitar la manipulación de datos numéricos en sus aplicaciones.

### Uso
Para utilizar la clase Numeric, simplemente se pueden crear instancias de sus subclases (Integer o Float) o usar números directamente en expresiones. La clase Numeric se extiende con métodos que permiten realizar operaciones como suma, resta, multiplicación, división, y mucho más.

### Detalles
- **Subclases**: Numeric tiene subclases como Integer, Float, y Rational.
- **Métodos**: Algunos métodos importantes incluyen `+, -, *, /, **` para operaciones aritméticas, así como `to_i`, `to_f`, y `to_s` para conversiones de tipo.
- **Comparaciones**: También permite comparaciones, utilizando operadores como `==`, `>`, `<`, entre otros.

## Ejemplos
```ruby
# Creación de números
numero_entero = 10
numero_flotante = 3.14

# Operaciones básicas
suma = numero_entero + numero_flotante  # => 13.14
resta = numero_entero - 5                # => 5
multiplicacion = numero_entero * 2       # => 20
division = numero_entero / 2.0           # => 5.0

# Conversión de tipos
entero_a_flotante = numero_entero.to_f   # => 10.0
flotante_a_entero = numero_flotante.to_i  # => 3
```

## Explicación
Al trabajar con la clase Numeric, es importante tener en cuenta algunas consideraciones:
- **Precisión**: Los números en punto flotante pueden presentar problemas de precisión debido a la forma en que se representan en la memoria.
- **División entre enteros**: Al dividir dos enteros, el resultado será un número entero en Ruby 2.4 y versiones anteriores. Para obtener un resultado flotante, al menos uno de los operandos debe ser un flotante.
- **Coerción automática**: Ruby maneja la coerción automática de tipos, lo que significa que puedes mezclar enteros y flotantes en operaciones sin errores.

## Resumen en una línea
Numeric en Ruby es la clase base para la representación y manipulación de números, que incluye enteros y flotantes, facilitando operaciones matemáticas y conversiones.