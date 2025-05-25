<!--
Meta Description: # Ruby Strings: Eine umfassende Anleitung zur Verwendung und Manipulation von Zeichenfolgen ## Synopsis In Ruby sind Strings eine grundlegende Datenst...
Meta Keywords: ruby, strings, von, und, text
-->

# Ruby Strings: Eine umfassende Anleitung zur Verwendung und Manipulation von Zeichenfolgen

## Synopsis
In Ruby sind Strings eine grundlegende Datenstruktur zur Speicherung und Manipulation von Text. Sie bieten eine Vielzahl von Methoden für die Bearbeitung, Formatierung und Analyse von Zeichenfolgen.

## Dokumentation
Strings in Ruby sind Objekte der Klasse `String` und können durch einfache oder doppelte Anführungszeichen erstellt werden. Sie unterstützen Unicode und können somit eine breite Palette von Zeichen darstellen. Strings sind unveränderlich, was bedeutet, dass jede Modifikation einen neuen String erstellt.

### Erstellung von Strings
Strings können auf verschiedene Arten erstellt werden:
```ruby
string1 = 'Hallo, Welt!'
string2 = "Ruby ist mächtig."
```

### Wichtige Methoden
Ruby bietet viele eingebaute Methoden zur Manipulation von Strings, darunter:
- `.length`: Gibt die Länge des Strings zurück.
- `.upcase`: Wandelt alle Zeichen in Großbuchstaben um.
- `.downcase`: Wandelt alle Zeichen in Kleinbuchstaben um.
- `.strip`: Entfernt führende und nachfolgende Leerzeichen.
- `.split`: Teilt den String anhand eines Trennzeichens.

### Beispielhafte Nutzung
```ruby
text = "  Ruby Programmierung  "
puts text.strip             # => "Ruby Programmierung"
puts text.length            # => 20
puts text.upcase           # => "  RUBY PROGRAMMIERUNG  "
puts text.split(" ")       # => ["", "Ruby", "Programmierung", ""]
```

## Erklärung
Ein häufiges Missverständnis ist, dass Strings in Ruby veränderlich sind. Tatsächlich wird bei jeder Modifikation ein neuer String erzeugt. Ein weiteres wichtiges Detail ist der Umgang mit Escape-Zeichen: In doppelten Anführungszeichen können Escape-Sequenzen wie `\n` (neue Zeile) oder `\t` (Tabulator) verwendet werden, während einfache Anführungszeichen dies ignorieren.

Ein Beispiel für einen häufigen Fehler:
```ruby
string = 'Ruby ist cool\n'  # Einfache Anführungszeichen - '\n' wird nicht als neue Zeile interpretiert
puts string                # => "Ruby ist cool\n"
```

## Ein-Satz-Zusammenfassung
Strings in Ruby sind leistungsstarke und vielseitige Objekte, die eine Vielzahl von Methoden zur Manipulation und Analyse von Text bieten.