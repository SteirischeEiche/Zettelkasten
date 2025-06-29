# Pygame: Gruppen

#Python #Pygame #programmieren

- In einem Spiel verwaltet man viele Objekte (zB Spieler, Gegner, Projektile, etc.)
- Es ist blöde, wenn wir Methoden (wie `.draw()`) auf jedes Objekt einzeln anwenden müssen
- Das müllt unseren Code (genauer die Spiel-Schleife) zu
- Pygame hat dafür eine Lösung: Man kann Objekte in __Gruppen__ zusammenfassen
- Ein Objekt kann Element mehrerer Gruppen sein

## Verwendung von Gruppen - Beispiele

- Eine leere Gruppe erstellen:
```python
my_group = pygame.sprite.Group()
```

- Durch das `containers`-Feld kann man Objekte _automatisch in Gruppen einsortieren_
- Alle Objekte der Klasse `Player` den Gruppen `group_a` sowie `group_b` zuordnen:
```python
Player.containers = (group_a, group_b)
```

- Mann kann über die Objekte in einer Gruppe iterieren (wie bei Listen)
- Die `.update()`-Methode für alle Mitglieder der Gruppe gleichzeitig aufrufen:
```python
group.update(dt)
```
