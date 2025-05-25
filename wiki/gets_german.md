<!--
Meta Description: # Die Ruby-Methode "gets": Benutzerinteraktion durch Eingabe von Benutzerdaten ## Synopsis Die Ruby-Methode `gets` dient dazu, Eingaben vom Benutzer ü...
Meta Keywords: die, gets, ruby, eingabe, der
-->

# Die Ruby-Methode "gets": Benutzerinteraktion durch Eingabe von Benutzerdaten

## Synopsis
Die Ruby-Methode `gets` dient dazu, Eingaben vom Benutzer über die Standard-Eingabe (in der Regel die Tastatur) zu erfassen. Sie liest eine Zeile von der Konsole und gibt diese als String zurück.

## Dokumentation
Die `gets`-Methode ist ein grundlegendes Werkzeug in Ruby, um Benutzereingaben zu verarbeiten. Sie wird häufig in CLI-Anwendungen verwendet, um Daten zu sammeln, die der Benutzer eingibt. Die Methode blockiert den Programmfluss, bis der Benutzer die Eingabetaste drückt.

### Verwendung
Um `gets` zu verwenden, rufen Sie einfach die Methode ohne Argumente auf:

```ruby
input = gets
```

Hierbei wird die Eingabe des Benutzers in die Variable `input` gespeichert. Standardmäßig wird die Eingabe mit einem Zeilenumbruch (`\n`) enden.

### Details
- **Rückgabewert**: `gets` gibt einen String zurück, der die eingegebene Zeile enthält. Wenn das Ende der Datei (EOF) erreicht wird, gibt sie `nil` zurück.
- **Trimmen von Zeilenumbrüchen**: Um das abschließende Zeilenumbruchzeichen zu entfernen, kann die Methode `chomp` verwendet werden:

```ruby
input = gets.chomp
```

- **Funktion in Schleifen**: `gets` kann innerhalb von Schleifen verwendet werden, um wiederholt Eingaben zu erfassen.

## Beispiele
Hier sind einige grundlegende Verwendungsmöglichkeiten von `gets`:

### Beispiel 1: Einfache Eingabe
```ruby
puts "Bitte geben Sie Ihren Namen ein:"
name = gets.chomp
puts "Hallo, #{name}!"
```

### Beispiel 2: Zahlen eingeben und summieren
```ruby
puts "Geben Sie eine Zahl ein (oder 'exit' zum Beenden):"
while (input = gets.chomp) != 'exit'
  number = input.to_i
  puts "Die Zahl ist: #{number}"
  puts "Geben Sie eine andere Zahl ein (oder 'exit' zum Beenden):"
end
```

### Beispiel 3: Mehrfache Eingaben
```ruby
puts "Geben Sie mehrere Namen ein (drücken Sie Enter ohne Eingabe zum Beenden):"
names = []
while (input = gets.chomp) != ""
  names << input
end
puts "Die eingegebenen Namen sind: #{names.join(', ')}"
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `gets` ist, dass viele Entwickler nicht beachten, dass die Methode einen Zeilenumbruch am Ende der Eingabe beibehält. Um unerwünschte Zeilenumbrüche zu vermeiden, sollte immer `chomp` verwendet werden. 

Ein weiterer Punkt ist, dass `gets` blockiert, bis der Benutzer etwas eingibt und die Eingabetaste drückt. Dies kann in Skripten, die ohne Benutzerinteraktion laufen sollen, unerwünscht sein. In solchen Fällen sollten alternative Methoden zur Eingabe verwendet werden, wie z.B. das Lesen aus Dateien.

## Ein-Satz-Zusammenfassung
Die Ruby-Methode `gets` ermöglicht es, Benutzereingaben über die Standard-Eingabe zu erfassen und als String zurückzugeben.