# Python Variablen

#Python #programmieren

- Es gibt anscheinend nur implizite Deklaration

## Datentypen
- Der `NoneType` bedeutet, dass in einer Variable (noch) _kein Wert_ gespeichert ist. Sie ist _leer_.
```python
variable = None
```
- Das ist etwas anderes als die Werte `false` und `0`
- Es ist auch _kein String_

## Dynamische Typisierung
- Python hat Dynamische Typisierung (im Gegensatz zu zB Go)
- Dh jede Variable kann jeden Wert (Typ) abspeichern
- Der Typ kann sich ändern...
- ..._aber das sollte man niemals machen_
- Vorteil: Weniger Syntax; du kannst dich auf die eigentliche Aufgabe konzentrieren
- Nachteil: Könnte zu Bugs führen

## Strings: Konkatenation (Verkettung) und Interpolation
- Mit __Konkatenation__ kannst du Strings "aneinanderkleben"
```python
first_name = "Lane "
last_name = "Wagner"
full_name = first_name + last_name
print(full_name)
# prints "Lane Wagner"
```
- Es wird jedoch empfohlen, lieber __Interpolation__ zu verwenden, mit `f-strings`
- Interpolation bedeutet so viel wie: Etwas nachträglich einfügen
