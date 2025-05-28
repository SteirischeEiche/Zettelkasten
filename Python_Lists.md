# Python: Lists

#Python #programmieren

- List und Array sind Synonym
- Eine Liste kann Elemente jeden Datentyps enthalten
- Die Elemente einer Liste sind indiziert (Reihenfolge). Es beginnt mit 0.
- Die Funktion `len()` gibt die Länge einer Liste (die Anzahl der enthaltenen Elemente) aus
- Mit `name_liste.append("name_element")` kann man ein Element an eine Liste anhängen (dh das neue Element ist das letzte in der Liste)
- Die Funktion `.pop()` ist das Gegenteil von `.append()`. Sie löscht das letzte Element aus der Liste und gibt es als Rückgabewert zurück.

## Syntax ohne Index
- Man kann auch ohne Index auf die Elemente einer Liste zugreifen (s. Kapitel 9, Lektion 11 ff.)
- Das führt zu besser lesbarem Code (wenn einem der Index egal ist und es nur um den Wert geht)

## Slicing
- Mit Slicing kann man Elemente aus einer Liste rausschneiden
```python
scores = [50, 70, 30, 20, 90, 10, 50]
# Display list
print(scores[1:5:2])
# Prints [70, 20]
```
- Das Ergebnis ist wieder eine Liste
- Dabei kann man den Start, das Ende und die Schritte bestimmen

## Tupel
- Tupel haben eine Reihenfolge, die sich nicht ändert
- In Listen sollte man keine Elemente verschiedenen Datentyps speichern
- Dafür eignen sich aber Tupel, wegen der festen Reihenfolge
- Tupel können Elemente einer Liste sein
