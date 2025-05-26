Python: Computing

#Python #programmieren

- Integer = Ganzzahl
- Float = Dezimalzahl/-bruch, Kommazahl

## Floor Division
- = Ganzzahldivision
- Dh alles nach dem Komma wird ignoriert (oder abgeschnitten, das Ergebnis ist ein Integer)
- Man fragt sich: Wie oft passt _die ganze Zahl_ in die andere?
- Bsp.: 6,9 -> 6; -4,1 -> -5
- In Python macht man das mit `//`

## Exponenten
- ...sind eigentlich total einfach
- $2^3$ heißt wir haben zweimal zwei "Dinger", die ebenfalls aus zwei Teilen bestehen (also insges. 8 "Dinger")
- In Python schreibt man Exponenten so: $5^3$ = `5 ** 3`

## Variablen mit sich selbst verrechnen
- `variable = variable + 1` funktioniert in Python (auch wenn es mathematisch nicht korrekt ist),...
- ...weil Python folgendermaßen vorgeht: Weise `variable` den aktuellen Wert von `variable` plus `1` zu
- (Das kann man auch abkürzen: `variable += 1`)

## Wissenschaftliche Notation
```python
print(16e3)
# Prints 16000.0

print(7.1e-2)
# Prints 0.071
```
- Die Zahl nach dem `e` gibt an, um wie viele Stellen das Komma nach rechts verschoben wird
- Oder nach links, wenn sie negativ ist

---

- Subset heißt auf Deutsch Teilmenge
- Superset ist das [Gegenteil](https://www.youtube.com/watch?v=1wsF9GpGd00) von Teilmenge
