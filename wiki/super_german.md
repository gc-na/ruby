<!--
Meta Description: # Das Schlüsselwort "super" in Ruby: Eine umfassende Anleitung ## Synopsis Das Schlüsselwort „super“ in Ruby wird verwendet, um die Methode der überge...
Meta Keywords: super, die, methode, der, ein
-->

# Das Schlüsselwort "super" in Ruby: Eine umfassende Anleitung

## Synopsis
Das Schlüsselwort „super“ in Ruby wird verwendet, um die Methode der übergeordneten Klasse aufzurufen. Es ist ein wichtiges Konzept in der objektorientierten Programmierung, das das Vererben von Eigenschaften und Methoden zwischen Klassen erleichtert.

## Dokumentation
In Ruby ermöglicht das Schlüsselwort „super“ den Zugriff auf Methoden von übergeordneten Klassen. Es wird häufig in der Methode eines Unterklassenobjekts verwendet, um die Implementierung der übergeordneten Methode zu erweitern oder zu ergänzen. Wenn „super“ ohne Argumente aufgerufen wird, werden die Argumente, die an die Methode übergeben wurden, auch an die übergeordnete Methode weitergeleitet.

### Verwendung
- **Aufruf der übergeordneten Methode:** Mit „super“ können Sie die Logik einer Methode in der übergeordneten Klasse ansprechen.
- **Argumentübergabe:** „super“ übergibt automatisch die Argumente der aktuellen Methode an die übergeordnete Methode.

### Details
- **Syntax:** `super` oder `super(arguments)`
- **Kontext:** Es kann nur innerhalb von Methoden verwendet werden und muss sich in einer Klasse befinden, die von einer anderen Klasse erbt.
- **Keine Rückgabewerte:** Wenn die übergeordnete Methode nicht existiert, wird ein Fehler ausgelöst.

## Beispiele

### Beispiel 1: Einfacher `super`-Aufruf
```ruby
class Tier
  def sprich
    "Ich bin ein Tier."
  end
end

class Hund < Tier
  def sprich
    super + " Ich bin ein Hund."
  end
end

hund = Hund.new
puts hund.sprich  # Ausgabe: "Ich bin ein Tier. Ich bin ein Hund."
```

### Beispiel 2: `super` mit Argumenten
```ruby
class Rechnung
  def initialize(betrag)
    @betrag = betrag
  end
end

class SteuerRechnung < Rechnung
  def initialize(betrag, steuer)
    super(betrag)
    @steuer = steuer
  end
end

rechnung = SteuerRechnung.new(100, 19)
```

## Erklärung
Ein häufiger Fehler ist es, „super“ in der falschen Methode zu verwenden. Wenn „super“ in einer Methode aufgerufen wird, die nicht von einer übergeordneten Klasse erbt, führt dies zu einem Fehler. Achten Sie auch darauf, dass die übergeordnete Methode tatsächlich existiert, sonst wird ein `NoMethodError` ausgelöst.

Ein weiteres häufiges Missverständnis ist die Verwendung von „super“ mit Argumenten. Wenn „super` ohne Argumente aufgerufen wird, werden alle an die Methode übergebenen Argumente an die übergeordnete Methode weitergegeben. Wenn Sie jedoch spezifische Argumente übergeben möchten, können Sie diese in den Klammern angeben.

## Ein-Satz-Zusammenfassung
Das Schlüsselwort „super“ in Ruby ermöglicht es, Methoden der übergeordneten Klasse aufzurufen und dabei die Argumente der aktuellen Methode weiterzugeben.