# OOP - Klassen: Variablen

#OOP #programmieren

- Variablen, die innerhalb des Constructor deklariert werden, nennt man Instanz-Variablen
```python
class Wall:
   def __init__(self):
      self.height = 10
```

- Klassen-Variablen werden dagegen oben in der Klasse erstellt
```python
class Wall:
   height = 10
```

- Instanz-Variablen gelten nur für eine Instanz
- Wenn du dagegen eine Klassen-Variable veränderst, verändert das _alle_ Instanzen dieser Klasse
- Deshalb sollte man Klassen-Variablen eher meiden
