## Python Module

#Python #programmieren

- Es wäre blöde, wenn wir das ganze Programm in eine Datei schreiben müssten
- Jede `.py`-Datei ist ein __Modul__. Wir können Funktionen, Variablen und Klassen aus einem Modul importieren.
- Best Practice: Nicht mit `*` alles importieren sondern explizit einzelne Daten. Das erleichtert das Debuggen.

```python
# import everything from the module
# database.py into the current file
from database import *
```

## Ein Modul schrieben

```python
if __name__ == "__main__":
    main()
```

- Dieser Code hat zur Folge, dass die `main()`-Funktion nur ausgeführt wird, wenn das Programm direkt ausgeführt wird
- Wird das Programm jedoch als Modul in ein anderes Programm importiert, wird `main()` nicht ausgeführt
