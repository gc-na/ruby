<!--
Meta Description: # Die Verwendung von "when" in Ruby: Ein umfassender Leitfaden ## Synopsis Der `when`-Befehl in Ruby ist ein essenzieller Bestandteil der `case`-Anwei...
Meta Keywords: when, die, case, puts, von
-->

# Die Verwendung von "when" in Ruby: Ein umfassender Leitfaden

## Synopsis
Der `when`-Befehl in Ruby ist ein essenzieller Bestandteil der `case`-Anweisung, die eine elegante Möglichkeit bietet, mehrere Bedingungen zu überprüfen und basierend auf dem Ergebnis unterschiedliche Codeabschnitte auszuführen.

## Documentation
Die `when`-Anweisung wird innerhalb einer `case`-Struktur verwendet, um die Ausführung von Codeblöcken zu steuern, abhängig von bestimmten Bedingungen. Die `case`-Anweisung ermöglicht es, einen Ausdruck zu überprüfen und mehrere mögliche Werte zu definieren, die dieser Ausdruck annehmen kann. Jedes `when` wird verwendet, um einen spezifischen Fall zu definieren.

### Zweck
Der Hauptzweck von `when` ist es, die Lesbarkeit und Wartbarkeit von Code zu verbessern, indem mehrere `if`-Anweisungen durch eine klarere Struktur ersetzt werden.

### Verwendung
Die grundlegende Syntax der `case`-Anweisung mit `when` sieht wie folgt aus:

```ruby
case Ausdruck
when Bedingung1
  # Code für Bedingung1
when Bedingung2
  # Code für Bedingung2
else
  # Code, wenn keine der Bedingungen zutrifft
end
```

## Examples
Hier sind einige einfache Beispiele für die Verwendung von `when` in Ruby:

### Beispiel 1: Einfache Fallunterscheidung
```ruby
farbe = "rot"

case farbe
when "blau"
  puts "Die Farbe ist blau."
when "rot"
  puts "Die Farbe ist rot."
else
  puts "Unbekannte Farbe."
end
```

### Beispiel 2: Mehrere Bedingungen
```ruby
zahl = 3

case zahl
when 1, 2
  puts "Die Zahl ist entweder 1 oder 2."
when 3
  puts "Die Zahl ist 3."
else
  puts "Eine andere Zahl."
end
```

### Beispiel 3: Vergleich mit einer Bedingung
```ruby
note = 4

case note
when 1..2
  puts "Sehr gut!"
when 3..4
  puts "Gut!"
when 5..6
  puts "Nicht bestanden."
else
  puts "Ungültige Note."
end
```

## Explanation
Ein häufiges Missverständnis bei der Verwendung von `when` ist, dass der Code möglicherweise nicht wie erwartet funktioniert, wenn die Bedingungen nicht korrekt definiert sind. Achten Sie darauf, dass die Bedingungen in den `when`-Klauseln genau den erwarteten Werten entsprechen. Ein weiteres häufiges Problem ist die Verwendung von `case` ohne `else`, was dazu führen kann, dass kein Code ausgeführt wird, falls keine der Bedingungen zutrifft.

Verwenden Sie `case` mit Bedacht und prüfen Sie, ob eine `else`-Klausel erforderlich ist, um unerwartete Ergebnisse zu vermeiden.

## One Line Summary
Der `when`-Befehl in Ruby ermöglicht die einfache und lesbare Handhabung von Mehrfachbedingungen innerhalb einer `case`-Anweisung.