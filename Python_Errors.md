# Python: Errors

#Python #programmieren #boot.dev

- Syntaxfehler: Dein Code entspricht nicht den Regeln von Python
- Selbst wenn dein Code syntaktisch korrekt ist, können beim Ausführen Fehler auftreten
- Diese nennt man Exceptions (Laufzeitfehler)

## Try-except-Blöcke
- Wenn du zB folgenden Code ausführst
```python
print(10 / 0)
```
- ...würde das Programm wegen Division durch Null abstürzen
- Dies kann man mit `try`-`except`-Blöcken vermeiden
```python
try:
  10 / 0
except Exception:
  print("can't divide by zero")
```
- In den `try`-Block schreibt man Code, der eine Ausnahme auslösen könnte
- Wenn ein Fehler auftritt, wird der `except`-Block ausgeführt
- Dadurch stürzt das Programm nicht ab, sondern behandelt den Fehler kontrolliert

## Bugs vs. Errors (Fehler)
- Bug: Das Programm verhält sich nicht so, wie es soll
- Fehler: Dinge, die wir nicht wollen, die wir aber erwarten
- Deshalb schreiben wir Code, der mit dem Fehler umgehen kann
- Bsp.: Der User gibt sein Geburtsdatum ein, wo er eigentlich seine E-Mail eingeben sollte
> Bugs are fixed, errors are handled
- Fehler sind außerhalb unserer Kontrolle. Das Einzige, was wir tun können, ist, Code zu schreiben, der die Fehler behandelt (zB eine Fehlermeldung)
- Das machen wir mit Exceptions (s.o.)
- Bugs liegen in unserem Einflussbereich, wir müssen sie beheben

## Eigene Ausnahmen auslösen
- Es gibt eine Reihe von Standard-Ausnahmen, die der Python-Interpreter auslöst (zB bei Division durch 0)
- Dies deckt aber nicht alle möglichen Fehler in deinem Programm ab
- Deshalb musst du selber Fehler antizipieren und Ausnahmen auslösen
- Das geht so:
```python
def craft_sword(metal_bar):
    if metal_bar == "bronze":
        return "bronze sword"
    if metal_bar == "iron":
        return "iron sword"
    if metal_bar == "steel":
        return "steel sword"
    raise Exception("invalid metal bar")
```
- Die Ausnahme soll nicht in der Funktion selbst abgefangen/behandelt werden. Stattdessen soll die Ausnahme an den Funktionsaufrufer zurückgegeben werden.
- Einen Fehler zu behandeln heißt, einen `try`-`except`-Block zu schreiben. Im Gegensatz dazu kann mit `raise Exception("Hier kommt eine Beschreibung des Fehlers hin")` eine Ausnahme _lediglich auslösen_.

## Arten von Ausnahmen
- Es gibt spezifische (zB `ZeroDivisionError` oder `IndexError`) und grds. Ausnahmen (zB `Exception`)
- Man sollte spezifische Ausnahmen zuerst abfangen, denn Python hört auf nach Ausnahmen zu suchen sobald eine ausgelöst wurde
```python
try:
    nums = [0, 1]
    print(nums[2])
except Exception:
    print("An error occurred")
except IndexError:
    print("Index error")
```
- In diesem Bsp. wird `IndexError` niemals ausgelöst

### Ausnahme-Typen müssen zueinander passen
```python
try:
    raise Exception("zero division")
except ZeroDivisionError as e:
    print("zero")
```
- In diesem Bsp. erwartet der `except`-Block die Ausnahme `ZeroDivisionError`
- Der `try`-Block löst jedoch `Exception` aus
- Die Folge: Das Programm stürzt ab
