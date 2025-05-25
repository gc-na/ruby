<!--
Meta Description: # Rückgabewert in Ruby: Verwendung und Bedeutung des "return"-Schlüsselworts ## Synopsis Das Schlüsselwort `return` in Ruby ermöglicht es Entwicklern,...
Meta Keywords: return, methode, ruby, wird, verwendet
-->

# Rückgabewert in Ruby: Verwendung und Bedeutung des "return"-Schlüsselworts

## Synopsis
Das Schlüsselwort `return` in Ruby ermöglicht es Entwicklern, den Rückgabewert einer Methode festzulegen und die Ausführung der Methode vorzeitig zu beenden.

## Dokumentation
In Ruby wird das `return`-Schlüsselwort verwendet, um den Rückgabewert einer Methode zu definieren und die Ausführung der Methode an einer bestimmten Stelle zu beenden. Wenn `return` aufgerufen wird, wird die Methode sofort beendet und der angegebene Wert wird zurückgegeben. Wenn kein Wert angegeben wird, gibt die Methode `nil` zurück.

### Verwendung
Das `return`-Schlüsselwort wird typischerweise innerhalb einer Methode verwendet. Hier ist die grundlegende Syntax:

```ruby
def method_name
  # Anweisungen
  return value
end
```

Wenn `return` ohne einen Wert verwendet wird, wird `nil` zurückgegeben:

```ruby
def example
  return
end

puts example # => nil
```

### Details
- **Rückgabewert**: Der Wert, der nach dem `return`-Schlüsselwort angegeben wird, wird als Rückgabewert der Methode verwendet.
- **Frühes Beenden**: `return` kann verwendet werden, um die Ausführung einer Methode vorzeitig zu beenden, was besonders nützlich in Bedingungen ist.
- **Rückgabe von mehreren Werten**: Ruby ermöglicht die Rückgabe von mehreren Werten, indem ein Array oder mehrere Werte hinter `return` gesetzt werden.

## Beispiele
### Beispiel 1: Einfache Verwendung von `return`
```ruby
def add(a, b)
  return a + b
end

puts add(2, 3) # => 5
```

### Beispiel 2: Vorzeitiges Beenden einer Methode
```ruby
def check_number(num)
  return "Zahl ist negativ" if num < 0
  return "Zahl ist positiv"
end

puts check_number(-5) # => "Zahl ist negativ"
puts check_number(5)  # => "Zahl ist positiv"
```

### Beispiel 3: Rückgabe mehrerer Werte
```ruby
def coordinates
  return [10, 20]
end

x, y = coordinates
puts "X: #{x}, Y: #{y}" # => "X: 10, Y: 20"
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `return` ist das Missverständnis darüber, wo und wie oft es verwendet werden kann. `return` kann nur innerhalb von Methoden verwendet werden, nicht in anderen Kontexten wie Schleifen oder Conditionals. Wenn man `return` in einem Block oder einer Lambda verwendet, kann es das Verhalten der umgebenden Methode beeinflussen. Zudem ist zu beachten, dass es in Ruby nicht erforderlich ist, `return` zu verwenden, um den letzten Ausdruck einer Methode zurückzugeben; Ruby gibt immer den letzten Ausdruck zurück, wenn kein `return` verwendet wird.

## Ein Satz Zusammenfassung
Das Schlüsselwort `return` in Ruby wird verwendet, um den Rückgabewert einer Methode festzulegen und die Ausführung der Methode vorzeitig zu beenden.