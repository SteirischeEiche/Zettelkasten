# Python Funktionen

#Python #programmieren

- Mit Funktionen kannst du Code wiederverwenden ohne ihn kopieren und einfügen zu müssen
- Den Input für eine Funktion nennt man Parameter
- Variablen, die innerhalb einer Funktion deklariert werden, sind _nur dort_ verfügbar
- Es wird _nur der Wert_ einer Variable an eine Funktion übergeben, nicht die Variable selbst

## Print() vs. return
- `print()` ist eine _Funktion_, die einen Wert ausgibt (ähnlich wie der `echo`-Befehl)
- Sie hat keinen Rückgabewert
- `return` ist ein [[Schlüsselwort]], das die Ausführung einer Funktion beendet und einen Wert an den Aufrufer zurückgibt

## Print() zum Debuggen
- Gib regelmäßig (zB nach dem Aufruf einer Funktion) die Werte von Variablen aus
- Das hilft beim Debuggen

## Wo Funktionen deklarieren?
- Eine Variable muss erstellt werden bevor man sie benutzen kann
- Denn Code wird Zeile für Zeile von oben nach unten ausgeführt
```python
print(my_name)
my_name = 'Lane Wagner'
# NameError: 'my_name' is not defined
```
- Dasselbe gilt für Funktionen

---

- Die meisten Python-Programmierer lösen dieses Problem, indem sie zuerst alle Funktionen definieren...
- ...und dann eine Einstiegsfunktion (konventionell `main` genannt) aufrufen
- Die Reihenfolge, in der die Funktionen definiert werden, ist allerdings egal

## Kein return
- Man kann das `return` bei der Definition einer Funktion weglassen
- In diesem Fall gibt die Funktion `none` zurück

## Reihenfolge von Inputs und Outputs
- (Inputs = Parameter, Outputs = Rückgabewerte)
- Die Reihenfolge der Outputs (und Inputs) ist relevant, ihre Namen nicht
- Dh, wenn eine Funktion zwei Werte ausgibt, werden diese in der Reihenfolge ausgegeben wie es in der Funktons-Definition steht
