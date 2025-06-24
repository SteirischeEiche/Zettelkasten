# OOP: Polymorphism

#OOP #programmieren

- Polymorphism (Vielfältigkeit) bedeutet, dass Variablen, Funktionen und Objekte verschiedene Formen annehmen können
- Es bedeutet, dass man dasselbe Interface für verschiedene Formen (Datentypen) hat
- So können zB Geschwister-Klassen alle eine Methode mit demselben Namen haben, die aber unterschiedliche Körper haben (etwas anderes tun)

```python
class Creature():
    def move(self):
        print("the creature moves")

class Dragon(Creature):
    def move(self):
        print("the dragon flies")

class Kraken(Creature):
    def move(self):
        print("the kraken swims")

for creature in [Creature(), Dragon(), Kraken()]:
    creature.move()
# prints:
# the creature moves
# the dragon flies
# the kraken swims
```

- Zwei Funktionen (oder Methoden) haben dieselbe __Signatur__, wenn sie denselben Namen, dieselben Inputs und dieselben Outputs (Datentyp der Outputs) haben
