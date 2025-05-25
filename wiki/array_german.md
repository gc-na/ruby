<!--
Meta Description: # Arrays in Ruby: Eine umfassende Anleitung ## Synopsis Arrays in Ruby sind geordnete Sammlungen von Elementen, die eine Vielzahl von Datentypen entha...
Meta Keywords: arrays, ruby, eine, sind, von
-->

# Arrays in Ruby: Eine umfassende Anleitung

## Synopsis
Arrays in Ruby sind geordnete Sammlungen von Elementen, die eine Vielzahl von Datentypen enthalten können. Sie bieten eine effiziente Möglichkeit, Daten zu speichern und zu manipulieren.

## Dokumentation
### Zweck
Arrays sind eine fundamentale Datenstruktur in Ruby, die es ermöglicht, mehrere Werte in einer einzigen Variablen zu speichern. Sie sind dynamisch, das heißt, ihre Größe kann zur Laufzeit geändert werden.

### Verwendung
Ein Array wird in Ruby durch eine Liste von Elementen, die in eckige Klammern `[]` eingeschlossen sind, definiert. Elemente innerhalb eines Arrays sind durch Kommas getrennt.

#### Erstellung eines Arrays
```ruby
früchte = ["Äpfel", "Bananen", "Kirschen"]
```

#### Zugriff auf Array-Elemente
Der Zugriff auf Elemente erfolgt über ihren Index, wobei der Index bei 0 beginnt:
```ruby
puts früchte[0]  # Gibt "Äpfel" aus
```

#### Array-Methoden
Ruby bietet eine Vielzahl von Methoden zur Manipulation von Arrays, z. B.:
- `push`: Fügt ein Element am Ende des Arrays hinzu.
- `pop`: Entfernt das letzte Element des Arrays.
- `shift`: Entfernt das erste Element des Arrays.
- `unshift`: Fügt ein Element am Anfang des Arrays hinzu.
- `map`: Wendet eine Blockoperation auf jedes Element des Arrays an.

## Beispiele
### Erstellen und Bearbeiten eines Arrays
```ruby
zahlen = [1, 2, 3, 4, 5]
zahlen.push(6)          # Fügt 6 hinzu
zahlen.pop              # Entfernt das letzte Element (6)
zahlen.unshift(0)      # Fügt 0 am Anfang hinzu
puts zahlen.inspect     # Gibt [0, 1, 2, 3, 4, 5] aus
```

### Iteration über ein Array
```ruby
früchte.each do |frucht|
  puts frucht
end
```

### Array-Slicing
```ruby
teil_array = früchte[1..2]  # Gibt ein Teilarray zurück: ["Bananen", "Kirschen"]
```

## Erklärung
Obwohl Arrays in Ruby sehr vielseitig sind, gibt es einige häufige Fallstricke:
- **Mutabilität**: Arrays sind veränderlich. Änderungen an einem Array wirken sich auf alle Referenzen aus.
- **Indexierung**: Negative Indizes können verwendet werden, um von hinten auf das Array zuzugreifen (z. B. `früchte[-1]` gibt das letzte Element zurück).
- **Typen**: Arrays können verschiedene Datentypen enthalten, was zu unerwartetem Verhalten führen kann, wenn nicht darauf geachtet wird.

## Ein-Satz-Zusammenfassung
Arrays in Ruby sind flexible und dynamische Datenstrukturen, die eine geordnete Sammlung von Elementen bieten und eine Vielzahl von Methoden zur Manipulation und Iteration unterstützen.