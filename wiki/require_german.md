<!--
Meta Description: # Ruby `require`: Grundlagen und Anwendung in der Programmierung ## Synopsis Der Ruby-Befehl `require` wird verwendet, um externe Dateien oder Bibliot...
Meta Keywords: require, die, ruby, datei, der
-->

# Ruby `require`: Grundlagen und Anwendung in der Programmierung

## Synopsis
Der Ruby-Befehl `require` wird verwendet, um externe Dateien oder Bibliotheken in ein Ruby-Skript zu laden. Dies ermöglicht den Zugriff auf Funktionen und Klassen, die in anderen Dateien definiert sind.

## Dokumentation
### Zweck
Der Hauptzweck von `require` ist es, Code aus anderen Ruby-Dateien oder -Bibliotheken zu integrieren, um die Modularität und Wiederverwendbarkeit des Codes zu fördern. Es erleichtert die Organisation von Projekten und die Nutzung von Drittanbieter-Bibliotheken.

### Verwendung
Der Befehl `require` wird typischerweise am Anfang eines Ruby-Skripts verwendet. Die Syntax ist wie folgt:

```ruby
require 'date'
```

In diesem Beispiel wird die integrierte Datum-Bibliothek geladen. Der Pfad kann auch relativ oder absolut angegeben werden:

```ruby
require './lib/my_library' # relativ
require '/absolute/path/to/my_library' # absolut
```

### Details
- `require` lädt die Datei nur einmal. Wenn die Datei bereits geladen wurde, wird sie nicht erneut geladen.
- Um eine Datei nur einmal zu laden, kann auch `require_relative` verwendet werden, um auf Dateien im gleichen Verzeichnis oder in Unterverzeichnissen zuzugreifen.
- Wenn die angegebene Datei nicht gefunden wird, wirft `require` einen LoadError.

## Beispiele
Hier sind einige grundlegende Beispiele für die Verwendung von `require`:

1. **Laden einer Standardbibliothek:**
   ```ruby
   require 'json'
   data = JSON.parse('{"name": "John", "age": 30}')
   puts data['name'] # Ausgabe: John
   ```

2. **Laden einer benutzerdefinierten Datei:**
   Angenommen, Sie haben eine Datei `calculator.rb` im `lib`-Verzeichnis:
   ```ruby
   # lib/calculator.rb
   class Calculator
     def add(a, b)
       a + b
     end
   end
   ```

   Dann können Sie sie wie folgt laden:
   ```ruby
   require './lib/calculator'
   calc = Calculator.new
   puts calc.add(5, 3) # Ausgabe: 8
   ```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `require` ist die richtige Angabe des Pfades zur Datei. Achten Sie darauf, dass der Pfad korrekt ist und die Datei existiert, um einen LoadError zu vermeiden. Außerdem sollten Sie darauf achten, dass Sie nicht versehentlich dieselbe Datei mehrfach laden, da dies zu unerwartetem Verhalten führen kann.

Ein weiterer Punkt ist die Unterscheidung zwischen `require` und `require_relative`. Während `require` in der Regel für System- und Standardbibliotheken verwendet wird, ist `require_relative` nützlich, um lokale Dateien zu laden, da es den Pfad relativ zur aktuellen Datei interpretiert.

## Ein-Satz-Zusammenfassung
Der `require`-Befehl in Ruby lädt externe Dateien oder Bibliotheken in ein Skript, um die Wiederverwendbarkeit und Modularität des Codes zu erhöhen.