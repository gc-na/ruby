<!--
Meta Description: # Ruby "rescue": Fehlerbehandlung in Ruby ## Synopsis Das Schlüsselwort `rescue` in Ruby wird verwendet, um Ausnahmen zu behandeln und robustere Progr...
Meta Keywords: rescue, die, ruby, wird, fehler
-->

# Ruby "rescue": Fehlerbehandlung in Ruby

## Synopsis
Das Schlüsselwort `rescue` in Ruby wird verwendet, um Ausnahmen zu behandeln und robustere Programme zu schreiben, die gegen Laufzeitfehler gewappnet sind.

## Dokumentation
In Ruby ermöglicht das `rescue`-Schlüsselwort die Abfederung von Fehlern, die während der Programmausführung auftreten können. Es wird typischerweise innerhalb eines `begin`-Blocks verwendet, wo potenziell gefährlicher Code platziert wird. Wenn eine Ausnahme auftritt, springt Ruby zum entsprechenden `rescue`-Block, um die Fehlerbehandlung zu übernehmen.

### Verwendung
Die grundlegende Syntax sieht wie folgt aus:

```ruby
begin
  # Potenziell fehlerhafter Code
rescue StandardError => e
  # Fehlerbehandlung
end
```

In diesem Beispiel wird ein Fehler im `begin`-Block abgefangen, und der `rescue`-Block wird aktiviert, um den Fehler zu behandeln. Der Fehler kann über die Variable `e` angesprochen werden, die die Ausnahmeinstanz darstellt.

### Details
- Es ist möglich, mehrere `rescue`-Blöcke zu definieren, um verschiedene Arten von Ausnahmen zu behandeln.
- Das `rescue`-Schlüsselwort kann auch ohne `begin` verwendet werden, um direkt nach einem Fehler zu handeln.
- Man kann auch einen `ensure`-Block hinzufügen, der unabhängig von einer Ausnahme immer ausgeführt wird, um Aufräumarbeiten durchzuführen.

## Beispiele
### Einfaches Beispiel
```ruby
begin
  puts 10 / 0
rescue ZeroDivisionError => e
  puts "Ein Fehler ist aufgetreten: #{e.message}"
end
```
**Ausgabe:** Ein Fehler ist aufgetreten: divided by 0

### Mehrere Ausnahmen
```ruby
begin
  # Potenziell fehlerhafter Code
  raise ArgumentError, "Dies ist ein Argumentfehler"
rescue ZeroDivisionError => e
  puts "Division durch Null: #{e.message}"
rescue ArgumentError => e
  puts "Argumentfehler: #{e.message}"
end
```
**Ausgabe:** Argumentfehler: Dies ist ein Argumentfehler

### Verwendung von `ensure`
```ruby
begin
  puts "Versuche, eine Datei zu öffnen."
  file = File.open("nicht_existierende_datei.txt")
rescue Errno::ENOENT => e
  puts "Datei nicht gefunden: #{e.message}"
ensure
  puts "Dieser Block wird immer ausgeführt."
end
```
**Ausgabe:**
```
Versuche, eine Datei zu öffnen.
Datei nicht gefunden: No such file or directory - nicht_existierende_datei.txt
Dieser Block wird immer ausgeführt.
```

## Erklärung
Ein häufiger Fehler bei der Verwendung von `rescue` ist das Abfangen von Ausnahmen, die nicht behandelt werden sollten, wie z.B. `StandardError`, ohne spezifische Ausnahmetypen zu spezifizieren. Dies kann dazu führen, dass unerwartete Fehler stillschweigend ignoriert werden. Zudem sollte man darauf achten, dass der Code im `begin`-Block nicht zu umfangreich wird, um die Fehlersuche zu erleichtern. Es wird empfohlen, Fehler so spezifisch wie möglich zu behandeln, um die Kontrolle über den Programmfluss zu behalten.

## Ein Satz Zusammenfassung
Das `rescue`-Schlüsselwort in Ruby ermöglicht die effiziente Fehlerbehandlung, indem es Ausnahmen abfängt und entsprechende Maßnahmen ergreift.